# Voice-Encode-fMRI-Machine-Learning

Machine learning analysis of auditory fMRI responses using encoding, decoding, and representational similarity analysis (RSA).

## Research Question

Can distributed human brain activity distinguish vocal from non-vocal sounds, and which acoustic representations best explain auditory cortex responses?

This project investigates neural representations of biologically relevant sounds using computational neuroscience and machine learning methods.

## Dataset

OpenNeuro ds000158  
https://openneuro.org/datasets/ds000158

Subjects:
- sub-001 to sub-023

Data include:
- task fMRI BOLD recordings
- anatomical MRI
- auditory stimuli
- event timing files

## Methods

### Acoustic Feature Extraction

Audio stimuli are converted into spectro-temporal representations.

Features include:
- mel spectrograms
- spectral structure
- temporal acoustic information

### Encoding Models

Voxelwise regression predicts fMRI activity from acoustic features.

Framework:

acoustic features → voxel responses

### Decoding Models

Support Vector Machines (SVMs) classify stimulus categories from brain activity patterns.

Main task:
- voice vs non-voice decoding

### Representational Similarity Analysis (RSA)

RSA compares representational geometry between:
- neural activity patterns
- acoustic representations
- machine learning embeddings

## Models

- Ridge Regression
- Linear SVM
- PCA dimensionality reduction
- RSA correlation analysis

## Outputs

The notebook produces:
- decoding accuracy
- voxelwise prediction scores
- confusion matrices
- representational similarity matrices
- subject-level comparisons
- group-level statistics

## Biological Interpretation

Successful decoding indicates that auditory cortex contains distributed information about vocal categories.

Encoding performance suggests that spectro-temporal acoustic structure contributes to neural representation of biologically relevant sounds.

Cross-subject similarity may reflect shared principles of auditory cortical organization.

## References

Naselaris et al. (2011) — Encoding and decoding in fMRI

Kriegeskorte et al. (2008) — Representational Similarity Analysis

Theunissen et al. (2001) — Spectrotemporal receptive fields

Kell et al. (2018) — Deep neural network auditory models

## Requirements

- Python 3.10
- Nilearn
- Nibabel
- Scikit-learn
- Librosa
- Pandas
- Matplotlib

## Future Directions

- HRF-convolved encoding models
- Deep auditory embeddings
- Searchlight decoding
- Permutation statistics
- Cross-subject transfer learning
- CNN-based decoding
