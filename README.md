## Ex-01_DS_Data_Cleansing

## AIM

To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation

Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

## ALGORITHM

## STEP 1

Read the given Data

## STEP 2

Get the information about the data

## STEP 3

Remove the null values from the data

## STEP 4

Save the Clean data to the file

# CODE
Developed by:DHANUMALYA.D
Reg.no:212222230030

## Data_set.csv

import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)

df.info()

df.isnull()

df.isnull().sum()

df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()

df.isnull().sum()

## Loan_data.csv

import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)

df.info()

df.isnull()

df.isnull().sum()

df['Gender']=df['Gender'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Dependents'].mode()[0])
df.head()

df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df.head()

f['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()

df.isnull().sum()

## OUTPUT

## Data_set

## DATA

![ds1](https://user-images.githubusercontent.com/119218812/226126515-4fcdf161-26cc-4b00-95d0-7b5d80cd9a33.png)

![ds11](https://user-images.githubusercontent.com/119218812/226126974-27308211-b658-4175-a483-28148c7758c2.png)

## NON NULL BEFORE

![ds2](https://user-images.githubusercontent.com/119218812/226126522-f624a852-a838-47b4-be63-540d7ad2f059.png)
'
![ds3](https://user-images.githubusercontent.com/119218812/226126724-1bc41ff8-242d-49be-a4c4-d40d1ccb0768.png)

## MODE

![ds4](https://user-images.githubusercontent.com/119218812/226126728-7738d203-d017-4d8a-a798-a4630ade3537.png)

## MEAN

![ds41](https://user-images.githubusercontent.com/119218812/226126741-fb7b0ddd-8e29-49b2-8b3a-386f6b3d4063.png)

## MEDIAN

![ds42](https://user-images.githubusercontent.com/119218812/226126748-f241c460-c4de-4998-8408-7165958953a4.png)

## NON NULL AFTER

![ds5](https://user-images.githubusercontent.com/119218812/226126754-4e3affbc-b18a-4326-aee4-823ad2eb750b.png)


## Loan_data

## DATA

![ld1](https://user-images.githubusercontent.com/119218812/226126582-a6855481-06ce-43aa-99be-1527c1f11ae9.png)

![ld2](https://user-images.githubusercontent.com/119218812/226126591-054df89c-d5c7-4c16-b6b0-98cbbb21fb0a.png)

## NON NULL BEFORE

![ld21](https://user-images.githubusercontent.com/119218812/226126598-d782752a-26ca-47cc-8afb-a0497487a710.png)

![ld3](https://user-images.githubusercontent.com/119218812/226126605-07591a6c-fb68-4920-b990-c4e80bf61653.png)

## MODE

![ld4](https://user-images.githubusercontent.com/119218812/226126618-1608d14a-6b06-4f97-bd25-f3b439112e24.png)

## MEAN

![ld41](https://user-images.githubusercontent.com/119218812/226126625-3497be2e-a69d-4bd9-be2a-4ecfa027008c.png)

## MEDIAN

![ld42](https://user-images.githubusercontent.com/119218812/226126628-7f12c100-96fe-4e50-8039-281dc051b691.png)

## NON NULL AFTER

![ld5](https://user-images.githubusercontent.com/119218812/226126644-09492b12-29e1-4b2e-9596-ed6acbb6ab72.png)


## Result
The Dataset is been successfully cleaned and saved into the python file.
