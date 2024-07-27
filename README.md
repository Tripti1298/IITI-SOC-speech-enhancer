# IITI-SOC-speech-enhancer

Introduction : This project aims to enhance speech quality by reducing noise and improving clarity in audio recordings.
In this project, we will use spectrograms as a representation of sound in order to predict the noise model to be subtracted to a noisy voice spectrogram.

# Prepare the data:
First we downloaded dataset from Kaggle . Then we divided it into two parts: one was for training and the other one was for test.Then we created two separate python functions to add random noise using numpy features.

#Data preprocessing:
To prepare our data to be fed into the model we extracted melspectogram features for each of our individual audio files (training dataset) both for noisy and for clean data.After which we normalized it.Using matplotlib library of python we visualized our melspectograms.

*********insert ss here**************

#Model definition 
We used the U-Net model which is a type of CNN audio denoising.We define the shape of the input data . then we define the encoder.In the first layer of convolution we apply 64 filters of 3X3 size to the input.Similar to the encoder we define the convolution of the decoder.The transposed convolutional layer reconstructs the spatial dimensions.The encoder layer reduces spatial dimensions.In the end the output layer produces the final output.


#Model Training
We finally train the model with a total of 30 epochs.
******ss*************8
#Evaluate the model
we load our model in the new segment of google colab, load the audio files, preprocess the audio files ,convert to spectograms, resize it to consistent shape and after completing all the requirements we evaluate the model.
Earlier we were getting a loss of around 7 with 10 epochs in our model but we were finally able to bring it down to 4.26 with increasing the epochs to 30. 

#Final output
We finally denoised the audio through trained model and saved the enhanced audio in denoised_audio.


