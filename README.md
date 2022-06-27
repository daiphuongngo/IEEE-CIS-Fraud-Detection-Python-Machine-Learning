# IEEE-CIS-Fraud-Detection-Python-Machine-Learning

## Data Cleaning:

### Summary Table Function:

![Screen Shot 2022-06-27 at 4 45 02 AM](https://user-images.githubusercontent.com/70437668/175901849-8c9c582d-be85-4343-a628-51d6319143a0.png)

### Outliers Function:

![Screen Shot 2022-06-27 at 4 45 02 AM](https://user-images.githubusercontent.com/70437668/175901871-c138c28d-097b-43fe-83de-07927a2dfa0e.png)

### Summary Output:

![Screen Shot 2022-06-27 at 4 45 17 AM](https://user-images.githubusercontent.com/70437668/175901883-7f99050b-41ef-45da-a560-21c3b1f39356.png)


![Screen Shot 2022-06-27 at 4 45 17 AM](https://user-images.githubusercontent.com/70437668/175901900-1f7efad1-1ffd-4022-8374-48978a89d79e.png)

### Outliers Output:

![Screenshot 2022-06-27 050249](https://user-images.githubusercontent.com/70437668/175902140-c9ac1847-956f-4669-9ef4-b8a9a017a894.jpg)

## Explore the Data: (as below)

### Identity Information:

`id_01` - `id_11` are continuous features while `id_12` - `id_38` are categorical features. The final two features are even categorical.


`id_01` - `id_11` are continuous features while `id_12` - `id_38` are categorical features. The final two features are even categorical.

The chart illustrates that `id_01` has 77 unique negative values and the majority of them are closer to 0.

Meanwhile, `id_03` has roughly 90% of missing values which are either missing or closer to 0.


Furthermore, `id_11` has 22% of values being closer to 100 and 76% of values being missing. This is an odd case.


The distribution of `id_07` seems quite normal.


Several features are being assumed normalized. But if normalizing all features is required, one step that should be done in advance is leaving already-normalized features from the next normalization step.









Several features above has binary values containing Found or Not Found.

### Countplots for Cards:





`card6` is basically the card type.

### Transaction Data:

The `TransactionDT` feature is a timedelta from a given reference datetime so it is not an actual timestamp. It is notable that the train and test sets are split by time with a gap between both. So the train is split from the earlier period while the test is split from the later period. There might be an impact on the cross-validation techniques but this step will be taken later in the next assignment. But luckily, the dates in both don't overlap, so the validation set will be also split by time.



### Distribution of Target:



The fraud cases in the Total Amount in Transaction Amt have a slightly higher number than the Fraud Transactions. This imbalanced manner would be undersampled or oversampled to get the sets balanced before training any models for prediction or classification.

# Data Storage:

The output of X, y, X, test, df_test are stored in CSV files on Google Drive and can be recalled easily by loading Drive and then imported through CSV. 

### Load Drive, Load Data, Merge into Train & Test sets:

![Screen Shot 2022-06-27 at 4 35 31 AM](https://user-images.githubusercontent.com/70437668/175901439-e39df2e8-16d2-4bd7-907c-e46a86dfaff1.png)



### Save refined data into Drive:

![Screen Shot 2022-06-27 at 4 36 05 AM](https://user-images.githubusercontent.com/70437668/175901464-273d3d07-7a26-4998-8d9b-6b3991157724.png)

![Screen Shot 2022-06-27 at 4 36 40 AM](https://user-images.githubusercontent.com/70437668/175901546-6c0e42ed-4df0-40ad-9b96-95c18a0bd713.png)


## Data Output:

Here are steps for this process as follows:

### Store features with one unique value:

![Screen Shot 2022-06-27 at 4 36 40 AM](https://user-images.githubusercontent.com/70437668/175901582-058eb202-b316-4e0a-80a1-5edfe4ccd825.png)


### Transform the Data by replacing mean (which already showed in the Task 2.3):

![Screen Shot 2022-06-27 at 4 36 40 AM](https://user-images.githubusercontent.com/70437668/175901627-69f4b693-7b1e-4c43-8433-5563bdc5ea2e.png)

### Data Preparation for Modelling:

![Screen Shot 2022-06-27 at 4 40 34 AM](https://user-images.githubusercontent.com/70437668/175901654-0d2bbb4f-bf8a-432b-a2b2-486cce2a78a7.png)

### Label Encoding for categorical features & Split Data into X, y & then Train & Test sets:

![Screen Shot 2022-06-27 at 4 41 04 AM](https://user-images.githubusercontent.com/70437668/175901668-996ced8a-5063-4763-8b97-1aa51a4b418d.png)


### Replace Infinite value by NaN values:

![Screen Shot 2022-06-27 at 4 41 09 AM](https://user-images.githubusercontent.com/70437668/175901740-23eb8d8a-4789-481c-9457-47da2fab719d.png)

