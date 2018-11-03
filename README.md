# genre_classification
This is a machine learning project to classify music according to genres.

Dataset Used : GTZAN Dataset
The dataset consists of 1000 songs of 30 second each. It consists of 100 songs for each 10 genres. 

Major Libraries Used: Librosa ( to extract features),
                      PyDub (to convert files to wav format)
 
1) au_to_wav_converter : This python file is made to convert .au file to .wav file. Librosa doesnt accept .au file. Thus it has to be converted. PyDub AudioSegment is used to convert to wav.

2)create_dataset : This script extracts features like ZCR, SpectralCentroid, SpectralRollOff, SpectralContrast,SpectralBandwidth, and MFCCs  and stores the data to data.csv file.Librosa is used to extract features.

3)train_model : This script trains the data extracted on data.csv file. PCA is used to remove the correlated features . StratifiedShuffleSplit is used for uniform distribution of train and test data.StandardScaler is used for feature scaling. LabelEncoder is used to convert label from text to digits. And then classifier algorithms were trained on data . Algorithms on which data is checked : LogisticRegression,DecisionTree,RandomForest,MLPClassifier,SupportVectorMachines,KNearestNeighbors.

