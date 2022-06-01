# Speech-to-Text

In this project we are to create a machine learnin model that takes in the speech audio data and together with the transcripts of them and then we create a model that learns the models. 

Since speech data cannot be directly input into a deep learning model, the speech data undergoes transformations that turns the speech into an image that can be input into a deep learning model. This is the acoustic modelling of the model. 

# Preprocessing. 

The speech is resized, mono files are converted to stereo and a common sample rate and duration is set for all the files. The raw audio goes through augmentation to allow resampling. A spectrogram is generated out of the audio. A spectrogram is an image of the speech showing the frequency and amplitude. SpecAugment methods are use to resample the images of the audios. The image can be a spectrogram or MelSpectrogram, the AudioGenerator class allows a user to choose whether to use a spectrogram or MelSpectrogram. A MelSpectrogram gives the model the ability to perceive frequency and amplitude the way humans speak. The text is converted to numbers using the characters in char_map.py