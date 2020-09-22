# Video_Super-Resolution

Performed superresolution(low resolution to high resolution) on videos using SRGAN which is a generative adversarial network (GAN)
forimage super-resolution. The implementation of <strong>SRGAN</strong> is followed from the paper  <a href="https://arxiv.org/abs/1609.04802">Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network</a>, CVPR17. 



<pre><code>@InProceedings{ledigsrgan17,    
 author = {Christian Ledig and Lucas Theis and Ferenc Husz&aacuter and Jose Caballero and Andrew Cunningham and Alejandro Acosta and Andrew Aitken and Alykhan Tejani and Johannes Totz and Zehan Wang and Wenzhe Shi},    
 title  = {Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network},    
 booktitle  = {Proceedings of IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},    
 pages = {4681--4690},  
 year = {2017}}
 </code></pre>


# Results of SRGAN 

![Super-Resolution](.\super_resol.jpg)


# Dependencies
pytorch 0.3+, python 3.5, python-box, scikit-image, numpy

# Training set
We used a subset of Imagenet dataset ILSVRC2016_CLS-LOC.tar.gz for training our models. The subset can be found in <code>/subset.txt</code> 

# Training
<pre><code>CUDA_VISIBLE_DEVICES=0 python ./train.py --option ./options/train/SRGAN/SRGAN_x4.json</code></pre>

# Testing
<pre><code>CUDA_VISIBLE_DEVICES=0 python ./test.py --option ./options/test/SRGAN/SRGAN_x4.json</code></pre>

