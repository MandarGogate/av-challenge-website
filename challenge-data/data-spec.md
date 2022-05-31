# Data

To obtain the data and baseline code, please see the download page.

# AV noise dataset

Our dataset is built based on the following video and audio data sources:

## Video data:

Video data is obtained from the [LRS3 dataset](https://www.robots.ox.ac.uk/~vgg/data/lip_reading/lrs3.html). LRS3 is composed by spoken sentences from TED and TEDx videos. 

## Audio data:

Audio data can be split into two categories: speech and noise. 

**Speech:** speech signals for both target speakers and competing speakers are from the LRS3 dataset. 

**Noise:** the noise dataset is built based on three different datasets. These are:

- [1st Clarity Enhancement Challenge](https://github.com/claritychallenge/clarity/tree/main/recipes/cec1): The Clarity Challenge noise dataset comprises around 7 hours of domestic noises. 
- [DEMAND](https://zenodo.org/record/1227121#.YpZHLRPMLPY): The DEMAND noise dataset includes multi-channel recordings of 18 soundscapes that account for a little over 1 hour of data. Each soundscape is recorded using 16-channel array. We select only one of the channels to be used in our dataset. Moreover, we don't consider soundscapes assigned to the "domestic" category to avoid overlapping with the sounds of the Clarity Challenge. Additionally, we remove the soundscape labeled as OMEETING because this examples resembles the competing speaker scenario. The selection results in around 1 hours of audio.  
- [Deep Noise Supression challenge (DNS) 2nd version](https://github.com/microsoft/DNS-Challenge): The DNS dataset released in the second version of the challenge is composed by sounds from AudioSet, DEMAND and Freesound. In our selection we only consider audios that are obtained from Freesound. Moreover, we remove sounds that belong to the *Fan* category to avoid overlapping with Clarity Challenge sounds. As a result there are 25 hours of data. 

All audios are single channel, downsampled to 16 KHz and a bit depth of 16.

## Training, development, evaluation data

The dataset is divided into training and development data. 
The evaluation dataset will be released later on. 

The dataset is composed of:

* Training set: 605 speakers (113hrs).
* Development set: 85 speakers (9hrs)

## Training data

Each scene in the training set includes the following files:

- Target.
- Interferer.
- Mix.

Metadata is also provided as a JSON file. Metadata includes information such as scene number, target, masker, masker type (speech/noise) and segment selection offset. 


## Development data

Each scene in the development set includes the following files:

- Target.
- Interferer.
- Mix.

Metadata is also provided as a JSON file.


## Evaluation

The evaluation set will be released later on. 



