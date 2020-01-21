# SPEC-CGAN
We apply the Cycle GAN concept to the problem of removing specularity from images, resulting in
the Spec-CGAN model shown in Figure 3.11. S and D represent sets of 256 × 256 images with a
specific set of specularity images S and diffuse images D. D S : S 7→ {0, 1} and D D : D 7→ {0, 1}
represent discriminators for S and D. G : S 7→ D and F : D 7→ S are forward and backward
mapping functions. For G, Spec-CGAN uses ResNet with 9 residual blocks, because the image size
is 256 × 256.
<ul>
  <li> The dataset (Spec-Face) avalible free only for research purpose and not for commercial use </li>
  <li> No one is allowed to edit the dataset </li>
</ul>

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
  <li> Download a dataset (The google drive link will provide soon): </li>
  
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
<ul>
  <li> Download the pre-trained model from the following google drive links and place it into SPEC-CGAN directory</li>
  <li> Run the follwoing command </li>
  
   ```
   CUDA_VISIBLE_DEVICES=0 python SPEC_CGAN_main.py --dataset_dir=spec2diff --phase=test --which_direction=AtoB
  ```  
</ul>
  
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
</ul>
