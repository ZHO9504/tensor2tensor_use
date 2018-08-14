# tensor2tensor_use
the use of tensor2tensor

## Install:
The tensorflow version should be better follow the Official document(https://github.com/tensorflow/tensor2tensor/blob/master/setup.py ),then you will meet less error
##### 1.Install Tensorflow: pip3 install --upgrade tensorflow==1.10.0(or other version of tensorflow)
##### 2.Install t2t(tensor2tensor): pip install tensor2tensor
##### 3.Use the example given command to test if the tensor2tensor is installed successfully.:
```
t2t-trainer \
  --generate_data \
  --data_dir=~/t2t_data \
  --output_dir=~/t2t_train/mnist \
  --problem=image_mnist \
  --model=shake_shake \
  --hparams_set=shake_shake_quick \
  --train_steps=1000 \
  --eval_steps=100
```
## You can define a problem by yourself too
fist you should have a dir named 't2t':
```
haiou@gpu3-1080:~/t2t_1/t2t$ ls
decoder  rawdata  self_data  self_script  timit  train
```
and in the dir 'self_script':
```
haiou@gpu3-1080:~/t2t_1/t2t$ ls self_script/
__init__.py  my_problem.py 
```
__init__.py:
```
 from . import my_problem

```
my_problem.py: just reference to the script in:https://github.com/tensorflow/tensor2tensor/tree/master/tensor2tensor/data_generators


