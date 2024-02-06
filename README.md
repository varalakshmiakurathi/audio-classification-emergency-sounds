# Audio-classification-EmergencySounds
Emergency vehicle detection using audio 
Detecting emergency vehicle in traffic is essential for saving lives and using audio for this task is a challenging process. 

## Data Preparation:
Considering different online open source audio datasets on Emergency Vehicle sounds such as ambulance, fire engine and police car, I prepared my custom dataset of 2 classes containing emergency and non-emergency classes for the task.
1. UrbanSound8k - https://www.kaggle.com/datasets/chrisfilo/urbansound8k
2. Emergency Vehicle Siren Sounds - https://www.kaggle.com/datasets/vishnu0399/emergency-vehicle-siren-sounds
3. https://drive.google.com/file/d/14ZCIdME9M1CN7Bu7MAbZ5qY9X0HWr0nC/view
4. Large-scale audio dataset for emergency vehicle sirens and road noises - https://figshare.com/articles/media/Large-Scale_Audio_Dataset_for_Emergency_Vehicle_Sirens_and_Road_Noises/19291472
   
 The final dataset contains 2 folders one with emergency sounds and other with non-emergency sounds:-   
   emergency - 2102  
   non-emergency - 2082  
Audio files are in .wav format and from them features are extracted using their spectrographs.  

## Model Training:
Here the concept is to convert the audio files into spectrograms where it is considered as an image and thus makes it easy to apply CNN models.  
I have used simple CNN model with 2 convolutional layers, 1 max pooling layer and a dense layer along with a softmax activation function at the output layer.  
Apart from CNN model, I also trained the dataset on simple LSTM model for 200 epochs.  

## CNN model:
![model2](https://github.com/varalakshmiakurathi/audio-classification-emergency-sounds/assets/158546578/226401f4-bc35-4311-b5fb-b76440cd94e7)

## LSTM model:  
![model](https://github.com/varalakshmiakurathi/audio-classification-emergency-sounds/assets/158546578/915cb66a-60a8-4dea-ac73-939deac5392b)

After training, when new input file is given to the saved model, it is detecting the sound as either an emergency vehicle or not


