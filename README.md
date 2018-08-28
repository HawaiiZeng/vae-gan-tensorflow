# NEW ADD
We simply change CelebA dataset in main.py to Syn dataset, which contains supertoroids rendered images + geometric images.

## Data and Run
Data could be donwloaded:

Unzip the data and put the vae_gan_syn_data folder into the root folder.

[Box] https://wustl.box.com/s/nzev3y1c8g5l13tp9ft9qmt03opqpe81

Running: python3 main.py

# VAE/GAN (The following is the original README file:)
the tensorflow code of [Autoencoding beyond pixels using a learned similarity metric](https://arxiv.org/abs/1512.09300v2)

The paper should be the first one to combine the Variational Autoencoder(VAE) and Generative Adversarial Networks(GAN), by 
using the discrimiator of GAN as the perceptual loss instead of the pixel-wise loss in the original VAE. VAE/GAN also can be used for image 
reconstruction and visual attribution manipulation.

## About training instability

I also found the training is very instability. So, I update the code to stablize the adversarial progress of VAE/GAN. The details is in the below.

- Add a trick, named label smoothing [Improved Techniques for Training GANs](https://arxiv.org/abs/1606.03498) 

## Pretrained models.

The checkpoints files can be downloads from  [Google Drive](https://drive.google.com/open?id=1E5FWN6Xqg65bmXT5mtY8nmuLREz4gLoZ). Please unzip the files inside the project directory. Later, I will update the new models after more training iterations.

## Prerequisites

- tensorflow >=1.4

## dataset requirement

You can download the [Align and Cropped CelebA dataset](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) 
and unzip CelebA into a directory. Noted that this directory don't contain the sub-directory.

## Usage
  
   Train:
    
    $ python main.py --op 0 --path your data path
  
  Test:
  
    $ python main.py --op 1 --path your data path

## Experiments visual result

 Input:
    
 ![](img/real.png)
    
 Reconstruction
    
 ![](img/recon.png)
    
    
 ## Issue
 If you find the bug and problem, Thanks for your issue to propose it.
    

## Reference code

[DCGAN](https://github.com/carpedm20/DCGAN-tensorflow)

[autoencoding_beyond_pixels](https://github.com/andersbll/autoencoding_beyond_pixels)
