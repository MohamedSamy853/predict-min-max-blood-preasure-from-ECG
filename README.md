# ECG-based Blood Pressure Prediction Model
This project aims to develop a modular architecture model for predicting the minimum and maximum blood pressure values using electrocardiogram (ECG) data. The model consists of two branches: a Conv1D branch utilizing residual patterns to enhance convergence and extract relevant patterns from the ECG signals, and an LSTM branch to capture the sequential dependencies within the ECG data. The extracted features from both branches are concatenated and passed through fully connected layers for final prediction. Additionally, a hyperloss approach is employed to handle outliers in the data, using mean absolute error loss for outlier points and mean squared error loss for non-outlier points.
## Dataset
The model is trained and tested using a dataset consisting of ECG signals and corresponding minimum and maximum blood pressure values. The dataset should be preprocessed and formatted appropriately for input into the model
# Model Architecture
The model follows a modular architecture, combining Conv1D and LSTM branches to capture relevant features from the ECG signals.
## Conv1D Branch
The Conv1D branch is designed to extract patterns and features from the ECG signals. It utilizes residual connections to facilitate faster convergence and improve the model's ability to learn intricate patterns. The branch employs convolutional layers to process the ECG signals, followed by pooling layers for downsampling and reducing the spatial dimensions. The output of the Conv1D branch is a set of extracted features. 
## LSTM Branch
The LSTM branch focuses on capturing sequential dependencies present in the ECG signals. LSTM layers are employed to model the temporal relationships and long-term dependencies within the data. The LSTM branch processes the ECG signals and outputs a set of learned sequential features.
## Concatenation and Fully Connected Layers
The features obtained from the Conv1D and LSTM branches are concatenated and passed through fully connected layers. The fully connected layers combine the extracted features and learn representations suitable for predicting the minimum and maximum blood pressure values. The architecture of the fully connected layers can be adjusted based on the specific requirements of the task.
## Hyperloss
To handle outliers present in the data, a hyperloss approach is utilized. Mean absolute error (MAE) loss function is used for outlier points, where the predictions are penalized based on the absolute difference between the predicted and actual values. For non-outlier points, mean squared error (MSE) loss function is employed, penalizing predictions based on the squared difference. This approach helps in reducing the impact of outliers on the overall model performance.
