## Speaker Identification with Gaussian Mixture Models (GMM)

This repository contains Python code for speaker identification using Gaussian Mixture Models (GMMs).

### Dependencies

This code requires the following Python libraries:

* librosa
* numpy
* os
* scikit-learn
* pickle


### Functionality

The code performs the following tasks:

* **Feature extraction**: Extracts Mel-frequency cepstral coefficients (MFCCs) from audio files using librosa.
* **GMM training**: Trains a GMM for each speaker in a given data directory. The GMM learns the statistical distribution of the speaker's MFCCs.
* **Speaker prediction**: Predicts the speaker of a new audio file by comparing its MFCCs to the trained GMMs and selecting the speaker with the highest likelihood.
* **Model saving and loading**: Saves the trained GMM models to a pickle file and allows loading them for future predictions.

### Usage

1. **Data preparation**: 
    * Organize your audio data into folders, one for each speaker.
    * Ensure audio files are in WAV format with a sampling rate of 16 kHz.

2. **Training**:
    * Update the data_folder variable with the path to your data directory.
    * Run the script. This will train GMMs for each speaker in the directory and save them to the gmm_models.pkl file.


**Note**: The script includes example paths for the data directory and sample file. You need to modify these paths with your own data locations.


### Additional Information

* The script uses a fixed set of parameters for MFCC extraction. These parameters can be adjusted based on your specific needs.
* The number of GMM components (`n_components`) can be tuned for better performance.


