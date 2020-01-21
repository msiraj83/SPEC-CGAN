# SPEC-CGAN
## Prerequisites 
<ul>
  <li>tensorflow r1.1 </li>
  <li>numpy 1.11.0 </li>
  <li>scipy 0.17.0 </li>
  <li>pillow 3.3.0 </li>
</ul>

## Installation 
<ul>
  <li> Install tensorflow from https://github.com/msiraj83/SPEC-CGAN.git </li>
  <li> Clone this repo: </li> 
</ul> 

```
  git clone https://github.com/msiraj83/SPEC-CGAN.git
  cd SPEC-CGAN
```
## Train
<ul>
  <li> Download a dataset (e.g. zebra and horse images from ImageNet): </li>
  
  <li> Train a model: </li>
  
  ```
   CUDA_VISIBLE_DEVICES=0 python main.py --dataset_dir=spec2diff2805
  ``` 
  <li> Use tensorboard to visualize the training details: </li> 
  
  ```
   tensorboard --logdir=./logs
  ```
</ul>

## Test the model

  ```
   CUDA_VISIBLE_DEVICES=0 python main.py --dataset_dir=spec2diff2805 --phase=test --which_direction=AtoB
  ``` 
