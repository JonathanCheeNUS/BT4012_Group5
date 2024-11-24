Fraud Detection Dataset
This repository contains our pipeline for a fraud detection competition where the objective is to predict the probability that an online transaction is fraudulent. The dataset is split into two files: identity and transaction, which are joined by the TransactionID. The task is to predict the target variable isFraud, a binary variable indicating whether a transaction is fraudulent.

Dataset Description
The dataset consists of two main parts: Transaction Data and Identity Data, with the following features:

Transaction Data (train_transaction.csv / test_transaction.csv)
ProductCD: The product code for the transaction.
card1 - card6: Card-related features (1-6).
addr1, addr2: Address-related features.
P_emaildomain: The email domain of the purchaser.
R_emaildomain: The email domain of the recipient.
M1 - M9: A set of 9 binary features indicating various information about the transaction (e.g., account details, transactions).
TransactionDT: The time difference between the transaction and a reference datetime.
Identity Data (train_identity.csv / test_identity.csv)
DeviceType: The type of device used for the transaction.
DeviceInfo: Information related to the device (e.g., model or operating system).
id_12 - id_38: A set of identity-related features that are anonymized.
The training dataset contains a target variable isFraud, which is used to train the model. The test dataset does not contain isFraud and is used for making predictions.

Files
train_transaction.csv: Contains transaction data for training.
train_identity.csv: Contains identity data for training.
test_transaction.csv: Contains transaction data for testing.
test_identity.csv: Contains identity data for testing.
sample_submission.csv: A sample submission file in the correct format.

Objective
Your goal is to predict the probability that each transaction in the test set is fraudulent (isFraud = 1) or not fraudulent (isFraud = 0). The accuracy of your predictions will be measured using the area under the ROC curve (AUC).

Getting Started
To get started with the repository, follow these steps:

Clone the repository:
bash
Copy code
git clone https://github.com/JonathanCheeNUS/BT4012_Group5.git
cd BT4012_Group5
Install the necessary dependencies (create a virtual environment if desired):
bash
Copy code
pip install -r requirements.txt
Place your dataset files (train_transaction.csv, train_identity.csv, test_transaction.csv, test_identity.csv) in the /data/ directory.
