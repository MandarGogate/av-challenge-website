# Data

To obtain the data and baseline code, please see the download page.


# Video and audio data sources

The video and audio data sources are as follows:

## Video data:

Video data is obtained from the [LRS3 dataset](https://www.robots.ox.ac.uk/~vgg/data/lip_reading/lrs3.html). LRS3 is composed by spoken sentences from TED and TEDx videos. 

## Audio data:

Audio data can be split into two main categories: speech and noise. 

**Speech:** speech signals for both target speakers and competing speakers are from the LRS3 dataset. 

**Noise:** the noise dataset is built based on three different datasets. These are:

- [1st Clarity Enhancement Challenge](https://github.com/claritychallenge/clarity/tree/main/recipes/cec1): The Clarity Challenge noise dataset comprises around 6 hours of domestic noises. 
- [DEMAND](https://zenodo.org/record/1227121#.YpZHLRPMLPY): The DEMAND noise dataset includes multi-channel recordings of 18 soundscapes that account for a little over 1 hour of data. Each soundscape is recorded using 16-channel array. We select only one of the channels to be used in our dataset. Moreover, we don't consider soundscapes assigned to the "domestic" category as there can be overlapping to the sounds of the Clarity Challenge. Additionally, 
- [Deep Noise Supression challenge (DNS) 2nd version](https://github.com/microsoft/DNS-Challenge): From the DNS dataset we consider only audios that are obtained from Freesound, that results in around 29 hours of data. 

All audios are single channel downsampled to 16 KHz and a bit depth of 16.

## A. Training, development, evaluation data

The dataset is divided into training and development data. 
The evaluation dataset will be released later on. 

To access the dataset you can either:

- Use the provided scripts to build the scenes. 
- Download the file containing built scenes. 

# Data summary 

Training and development datasets are as follows:

**Training**

The training set consists of 605 speakers (113hrs). 
There are at least 9 minutes of data per speaker.

**Development**

The training development set consists of 85 speakers (9hrs). 
There are 5-9 minutes of data per speaker.


