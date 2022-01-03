# DeepLearning
AUTOENCODERS FOR IMAGE QUALITY IMPROVEMENT

The aim of this project is to show how autoencoders can provide image quality improvement for medical applications. 
Specifically, the target area is skin diagnosis made through images sent by patients to their doctors.
Three different neural networks have been implemented, progressively more advanced,  to improve image defects in terms of brightness, contrast, and blurriness. 

The project is divided into three parts. Firstly, we implemented an autoencoder from scratch. 
This helped us determine what layers were more useful for each block of the encoder and decoder.The code for this part can be found in the AUTOENCODERS file.
Secondly, to further improve our results, skip-connections inspired by the U-Net architecture were implemented. The implementation is stored in the U-Net file.
Brightness and contrast were solved by this last structure. 
However, the images were still blurry. Therefore, in the third part we adopted a GAN model structure taking the U-Net as a Generator and 
implementing the Discriminator from PatchGAN. This last part of the project can be found in the PatchGAN file.

A description of the project and all of its parts can be found in the paper. Moreover, a more detailed explanation of each of the parts and 
its implementation can be seen along the code.

We will now briefly describe what is in each of the files.

-----------------
AUTOENCODERS
-----------------
In this folder you will find: 
	- Autoencoders.ipynb: Jupyter notebook with the main code for the different autoencoder models implemented. From the easiest approach to the more complex ones. 
	- Autoencoders_CNN6.ipynb: A much simpler and cleaner version of the Autoencoders.ipynb notebook. We experiment with the best performing CNN from Autoencoders.ipynb for different batch sizes, number of epoch, losses, etc. 
	- Trained_models: contains .pth files with the weights and parameters that gave lowest training losses from the most relevant models we trained.

-----------------
U-Net
-----------------
In this folder you will find:
    -UNet.ipynb: a jupyter notebook with the UNet implementation and testing
    -Trained_model.pth: file with the trained UNet that has the lowest training loss


-----------------
PatchGAN
-----------------
In this folder you will find:
	- PatchGAN.ipynb: a jupyter notebook with the code
	- jpg : the images of the flower dataset
	- outputs: one image that the Generator has created in every epoch (we have selected a few over the 300 epochs)
	- checkpoints: contains the last checkpoint og the model. (The code runs but we are not able to restore a trained model)


	
