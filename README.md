# Predi_COVID_Fatigue_Vocal_Biomarker
## Background
COVID-19 patients may experience severe and chronic fatigue, affecting their quality of life and treatment adherence. This supports the need for long-term monitoring solutions for these patients. Our aim was to develop a digital vocal biomarker for fatigue monitoring. This biomarker is derived from a trained artificial intelligence-based algorithm predicting the presence of this symptom.

## Content
1. Mel-Spetrograms creation
- The duration of the audio recordings was first preset, because Covolutional Neural Networks do not accept variable input sizes. Type1 and Type2 audios were then concatenated in order to raise the information in the created mel-spectrograms.
2. VGG19 feature extraction and ML models' training
- Features were extracted through VGG19 pre-trained model provided by Keras. The extracted features were then reduced using Prinicipal Component Analysis (PCA) and fed into four machine learning models (K-Nearest Neighbors, Support Vector Machine, Logistic Regression and Voting Classifier). 
- Based on the model selected for each audio set, we derived the trained vocal biomarkers which quantitatively represent the probability of being labeled as fatigued. The vocal biomarker is then plotted according to the true label of the test set samples, and a Student's t-test is performed to confirm that its distribution for each class is different.

## Dependencies
- Pandas 1.1.5
- Numpy 1.19.5
- Matplotlib 3.2.2
- Librosa 0.8.1
- Sklearn 0.22.2
- Seaborn 0.11.2
- Scipy 1.4.1
