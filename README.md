#IITI-SOC Speech Enhancement

#Introduction

This project aims to enhance speech quality by reducing noise and improving clarity in audio recordings. We utilize spectrograms as a representation of sound to predict the noise model, which is then subtracted from a noisy voice spectrogram to achieve a cleaner audio output.

#Prepare the Data

We downloaded the dataset from Kaggle, split it into training and test sets, and created two Python functions to add random noise using numpy features.

***IMAGE IS ATTACHED FOR YOUR REFERENCE***
blob:https://web.whatsapp.com/b50df721-543f-47ed-9e29-efa434fb0167![image](https://github.com/user-attachments/assets/e1ce29fb-6fdf-4fb0-8ed4-98c983913b5a)


#Data Preprocessing

To prepare our data for the model, we extracted mel spectrogram features for each audio file in the training dataset, both noisy and clean. We then normalized these features. Using the matplotlib library, we visualized the mel spectrograms.

***IMAGE IS ATTACHED FOR YOUR REFERENCE***

<img width="1440" alt="Screenshot 2024-07-27 at 11 36 49 PM" src="https://github.com/user-attachments/assets/78eeb015-6240-444c-9768-3fa9391899d2">

<img width="1440" alt="Screenshot 2024-07-27 at 11 37 49 PM" src="https://github.com/user-attachments/assets/8c0a466c-ee70-4b1b-b861-304f3947a4e4">

#Model Definition

We used the U-Net model, a type of CNN, for audio denoising. The input data shape is defined, followed by the encoder and decoder. The first convolutional layer in the encoder applies 64 filters of 3x3 size to the input. The transposed convolutional layer in the decoder reconstructs the spatial dimensions. The encoder layer reduces spatial dimensions. The output layer produces the final denoised output.

***IMAGE IS ATTACHED FOR YOUR REFERENCE***

<img width="1440" alt="Screenshot 2024-07-27 at 11 38 48 PM" src="https://github.com/user-attachments/assets/f78cc4dd-576f-4468-8bdb-9cce117bf1d3">


#Model Training

We trained the model for a total of 30 epochs.



Evaluate the Model

In a new segment of Google Colab, we loaded the trained model and audio files. We preprocessed the audio files, converted them to spectrograms, resized them to a consistent shape, and evaluated the model. Initially, we had a loss of around 7 with 10 epochs, but we managed to reduce it to 4.26 by increasing the epochs to 30.

Final Output

We denoised the audio using the trained model and saved the enhanced audio in the denoised_audio directory.



##Instructions 
*You can clone this repository in Google Colab. And then run the cell blocks 
*While writing the code we integrated it into several blocks/cells to make it easy for us to code. If you may face any error while running it try separating the code and run it in several different blocks. The link to our colab notebook will be provided herewith.

https://colab.research.google.com/drive/1dQ89pkI0xUBFwlDfJ42DzA-TF2dCRuwN?usp=sharing#scrollTo=eOY5qi2mHprH

THANK YOU
