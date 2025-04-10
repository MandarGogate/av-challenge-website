# AVSEC-1 (2022) results
We thank all participants for taking part in the challenge and congratulate the winning teams!

We thank our industry partner, Sonova, for sponsoring the Challenge.

- 1st place: <br /> 
Mandar Gogate <br /> 
Edinburgh Napier University

- 2nd place: <br /> 
Jen-Cheng Hou <br />
Academia Sinica

The AVSEC-1 paper is available in the following link:

[AVSE Challenge: Audio-Visual Speech Enhancement Challenge](https://www.research.ed.ac.uk/en/publications/avse-challenge-audio-visual-speech-enhancement-challenge)

## Word intelligibility scores

|          |                 |          |          |          |            | **Speech** |          |          | **Noise** |          |
|----------|-----------------|----------|----------|----------|------------|------------|----------|----------|-----------|----------|
| System   | Name            | Overall  | Speech   | Noise    | low SNR    | mid SNR    | high SNR | low SNR  | mid SNR   | high SNR |
| A        | Original        | 59.00    | 61.88    | 56.13    | 36.21      | 66.67      | 82.76    | 33.33    | 56.90     | 78.16    |
| B        | Baseline        | 52.30    | 54.41    | 50.19    | 42.53      | 58.62      | 62.07    | 29.31    | 51.15     | 70.11    |
| C        | AVSE01          | 50.29    | 57.09    | 43.49    | 39.08      | 65.52      | 66.67    | 22.41    | 44.25     | 63.79    |
| D        | SLT_AVSE        | 50.19    | 51.53    | 48.85    | 30.46      | 63.79      | 60.34    | 21.84    | 44.83     | 79.89    |
| E        | ENU_AVSE        | 66.57    | 83.72    | 49.43    | 72.41      | 90.80      | 87.93    | 24.71    | 52.87     | 70.69    |
| F        | ENU_AVSE_2      | 68.77    | 80.65    | 56.90    | 66.09      | 83.91      | 91.95    | 35.06    | 58.62     | 77.01    |
| G        | BioASP_CITI     | 66.19    | 79.12    | 53.26    | 77.01      | 86.78      | 73.56    | 27.01    | 52.87     | 79.89    |
| H        | BioASP_CITI_CE1 | 65.23    | 71.84    | 58.62    | 68.39      | 78.16      | 68.97    | 35.63    | 63.22     | 77.01    |
| I        | BioASP_CITI_CE2 | 63.31    | 72.22    | 54.41    | 73.56      | 70.69      | 72.41    | 29.89    | 60.92     | 72.41    |
| J        | CogBiD          | 52.68    | 52.87    | 52.49    | 28.74      | 65.52      | 64.37    | 27.01    | 56.9      | 73.56    |
| LSD      | -               | 3.35     | 4.55     | 4.73     | 8.07       | 7.35       | 7.43     | 8.02     | 7.77      | 7.39     |


Word intelligibility scores (\%) calculated across all conditions (Overall), per masker: Speech (competing speaker) and Noise, and per masker and SNR (low, mid, high). A higher score means more intelligible. Scores were calculated as the percentage of words correctly identified, computed for each participant and averaged across participants. Differences larger than the Fisher's least significant difference (LSD) are significant. Scores were calculated from the responses of 87 participants.


## STOI scores

|        |         |        |       |         |  Speech |          |         | Noise   |          |
|--------|---------|--------|-------|---------|---------|----------|---------|---------|----------|
| System | Overall | Speech | Noise | low SNR | mid SNR | high SNR | low SNR | mid SNR | high SNR |
| A      | 0.593   | 0.593  | 0.594 | 0.415   | 0.595   | 0.769    | 0.420   | 0.597   | 0.764    |
| B      | 0.619   | 0.578  | 0.660 | 0.529   | 0.585   | 0.622    | 0.479   | 0.687   | 0.813    |
| C      | 0.613   | 0.596  | 0.630 | 0.538   | 0.617   | 0.633    | 0.438   | 0.654   | 0.799    |
| D      | 0.633   | 0.643  | 0.624 | 0.572   | 0.674   | 0.682    | 0.446   | 0.647   | 0.779    |
| E      | 0.789   | 0.857  | 0.721 | 0.792   | 0.868   | 0.910    | 0.527   | 0.764   | 0.874    |
| F      | 0.780   | 0.847  | 0.713 | 0.784   | 0.858   | 0.899    | 0.523   | 0.754   | 0.860    |
| G      | 0.754   | 0.803  | 0.705 | 0.766   | 0.851   | 0.791    | 0.495   | 0.759   | 0.862    |
| H      | 0.741   | 0.783  | 0.698 | 0.761   | 0.827   | 0.763    | 0.524   | 0.736   | 0.834    |
| I      | 0.739   | 0.774  | 0.705 | 0.766   | 0.764   | 0.792    | 0.535   | 0.747   | 0.833    |
| J      | 0.653   | 0.632  | 0.674 | 0.542   | 0.663   | 0.690    | 0.501   | 0.708   | 0.813    |

STOI scores (0-1) calculated across all conditions (Overall), per masker: Speech (competing speaker) and Noise, and per masker and SNR (low, mid, high). A higher score means more intelligible. Scores were calculated per sentence and averaged across sentences.

## Systems description

Original refers to the non-enhanced noisy mixes.

The description of baseline cab be found in the AVSE Challenge paper available [here](https://www.research.ed.ac.uk/en/publications/avse-challenge-audio-visual-speech-enhancement-challenge).

One page submission descriptions:  
[AVSE01](https://challenge.cogmhear.org/submissions/2022/AVSE01.pdf)  
[SLT_AVSE](https://challenge.cogmhear.org/submissions/2022/SLT_AVSE.pdf)  
[ENU_AVSE](https://challenge.cogmhear.org/submissions/2022/ENU_AVSE.pdf)  
[ENU_AVSE_2](https://challenge.cogmhear.org/submissions/2022/ENU_AVSE_2.pdf)  
[BioASP_CITI](https://challenge.cogmhear.org/submissions/2022/BioASP_CITI.pdf)  
[BioASP_CITI_CE1](https://challenge.cogmhear.org/submissions/2022/BioASP_CITI_CE1.pdf)  
[BioASP_CITI_CE2](https://challenge.cogmhear.org/submissions/2022/BioASP_CITI_CE2.pdf)  
[CogBiD](https://challenge.cogmhear.org/submissions/2022/CogBiD.pdf)  



