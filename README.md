
# Elastic Distortional Buckling Prediction for Cold-Formed Steel C-Sections
This project builds a simple neural network to predict the elastic distortional buckling load (Kd) of cold-formed steel C-sections, using basic geometric properties as inputs. The network is trained using Levenberg-Marquardt optimization

Problem Description
Goal: Predict the elastic distortional buckling capacity (Kd) of cold-formed steel C-sections.

Inputs (Features):

H — Web height

B — Flange width

D — Lip depth

t — Thickness

Output (Target):

Kd — Elastic distortional buckling load

The model helps engineers quickly estimate buckling loads without needing detailed finite element analysis.

# Project Workflow
Load Dataset

Dataset is read from an Excel file (test.xlsx).

Input features are H, B, D, t, and target is Kd.

Preprocessing

Standardize input features and target using z-score normalization (mean 0, standard deviation 1).

Split dataset into training and testing sets.

Model Definition

# Neural network architecture:

1 hidden layer

2 neurons in the hidden layer

Log-sigmoid activation for hidden layer

Identity (linear) activation for output

Loss function: mean squared error

Training

Optimize weights and biases using Levenberg-Marquardt algorithm (via scipy.optimize.least_squares).

Evaluation

Compute Mean Squared Error (MSE), Mean Absolute Error (MAE), and R² score on both training and test sets.

Compare actual vs predicted values.

Final Output

Reverse the standardization to obtain predictions in the original scale.

Save all the actual and predicted values for further analysis.
