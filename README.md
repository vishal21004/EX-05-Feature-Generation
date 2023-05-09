# EX-05-Feature-Generation


## AIM
To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file


# CODE
import pandas as pd

df=pd.read_csv('/content/Encoding Data.csv')

df.head()

df['ord_2'].unique()

from sklearn.preprocessing import LabelEncoder, OrdinalEncoder

climate = ['Cold', 'Warm', 'Hot']

en= OrdinalEncoder(categories = [climate])

df['ord_2']=en.fit_transform(df[["ord_2"]])

df

le = LabelEncoder()

df['Nom_0'] = le.fit_transform(df[["nom_0"]])

df

!pip install --upgrade category_encoders

from category_encoders import BinaryEncoder

be = BinaryEncoder()

data = be.fit_transform(df['bin_1'])

df = pd.concat([df,data],axis=1)

df

be=BinaryEncoder()

data = be.fit_transform(df['bin_2'])

df = pd.concat([df,data],axis=1)

df

be=BinaryEncoder()

data = be.fit_transform(df['bin_2'])

df = pd.concat([df,data],axis=1)

df

df1['Ord_1'].unique()

climate = ['Cold', 'Warm', 'Hot', 'Very Hot']

en= OrdinalEncoder(categories = [climate])

df1['Ord_1']=en.fit_transform(df1 [["Ord_1"]])

df1

df1['Ord_2'].unique()

cl = ['High School', 'Diploma', 'Bachelors', 'Masters', 'PhD']

en= OrdinalEncoder(categories = [cl])

df1['Ord_2']=en.fit_transform(df1 [["Ord_2"]])

df1

le = LabelEncoder()

df1['City']=le.fit_transform(df1[["City"]])

df1

from category_encoders import BinaryEncoder

be = BinaryEncoder()

data1 = be.fit_transform(df1['bin_2'])

df1 = pd.concat([df1,data1],axis=1)

df1

df2 = pd.read_csv("/content/titanic_dataset.csv")

df2.head()

be = BinaryEncoder()

data2 = be.fit_transform(df2['Sex'])

df1 = pd.concat([df1,data1],axis=1)

df1

df2 = pd.read_csv("/content/titanic_dataset.csv")

df2.head()

be = BinaryEncoder()

data2 = be.fit_transform(df2['Sex'])

df2 = pd.concat([df2,data2],axis=1)

df2

df2 = pd.get_dummies (df2, prefix=["Embarked"],columns=['Embarked'])

df2

# OUPUT
![image](https://user-images.githubusercontent.com/84709944/233913847-974bd76f-f12a-4580-8681-bb8e74eae905.png)
![image](https://user-images.githubusercontent.com/84709944/233913861-dd6e5c9a-1279-4c3d-9a86-7d6d8e90c865.png)
![image](https://user-images.githubusercontent.com/84709944/233913946-7b253882-333e-452b-9e35-09fc5be345c8.png)
![image](https://user-images.githubusercontent.com/84709944/233914008-a5f3d1a9-a5f9-4280-a414-eb3ac24e6ca2.png)
![image](https://user-images.githubusercontent.com/84709944/233914110-36f38021-dcc8-4203-9e4f-a88e1f33c78f.png)
![image](https://user-images.githubusercontent.com/84709944/233914244-651a259b-1770-4d4e-9e09-c978bce18578.png)
![image](https://user-images.githubusercontent.com/84709944/233914330-969e739e-82bb-42bc-a32e-8dc95687a9c7.png)
![image](https://user-images.githubusercontent.com/84709944/233914382-a336dc85-eae2-4360-b8fa-02d7767e864a.png)
![image](https://user-images.githubusercontent.com/84709944/233914430-24939acf-1fea-47e0-946d-8c478e37bca3.png)
![image](https://user-images.githubusercontent.com/84709944/235473114-e8ad2111-f875-42b7-a5b9-2263d5a1ffc6.png)
![image](https://user-images.githubusercontent.com/84709944/235633375-efb029dc-cfb9-46b9-8879-b60bea5aecc8.png)
![image](https://user-images.githubusercontent.com/84709944/235475522-d7b90f38-fbc3-4d9f-b11f-808cc816d321.png)
![image](https://user-images.githubusercontent.com/84709944/235633239-7ece70e4-bcda-4687-9955-ab6505ef3dcc.png)

# RESULT
Hence the given data is read was performed Feature Generation process and save the data to a file.

