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
   CUDA_VISIBLE_DEVICES=0 python SPEC_CGAN_main.py --dataset_dir=spec2diff
  ``` 
  <li> Use tensorboard to visualize the training details: </li> 
  
  ```
   tensorboard --logdir=./logs
  ```
</ul>

## Test the model

  ```
   CUDA_VISIBLE_DEVICES=0 python SPEC_CGAN_main.py --dataset_dir=spec2diff --phase=test --which_direction=AtoB
  ``` 
  
## Citetation of face from testA
Please cite only the faces with following names in your paper.
<ul>
  <li>Chaphan_*.png </li>
  <li>Siraj_*.png </li>
  <li>petch_*.png</li>
  <li>st119573_*.png </li>
  <li>st119818_*.png </li>
</ul>

## Reference
<ul>
  <li> Muhammad, S., Dailey, M. N., Farooq, M., Majeed, M. F., and Ekpanyapong, M. (2019). Spec-Net
and Spec-CGAN: Deep learning models for specularity removal from faces. In Journal of Imag
& Computer Vision, page https://doi.org/10.1016/j.imavis.2019.11.001.</li>
  <li>Zhu, J.-Y., Park, T., Isola, P., and Efros, A. A. (2017). Unpaired image-to-image translation using
cycle-consistent adversarial networks. In Proceedings of the IEEE International Conference on
Computer Vision (CVPR), pages 2223–2232</li>
</ul>
