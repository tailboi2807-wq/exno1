# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output

            <<include your coding and its corressponding output screen shots here>>
~~~
import pandas as pd
a=pd.read_csv("/content/SAMPLEIDS.csv")
print(a)
~~~
<img width="1037" height="611" alt="image" src="https://github.com/user-attachments/assets/ae80b3ef-2abd-4cf2-92e8-0d334c9288d1" />


~~~
a.shape
~~~
<img width="1002" height="57" alt="image" src="https://github.com/user-attachments/assets/a561d5b6-fd38-480c-872d-1c1bb6c4e2e3" />


~~~
a.head()
~~~
<img width="1031" height="345" alt="image" src="https://github.com/user-attachments/assets/d9a66ee8-c2d1-44dd-825d-4254c328a5c5" />



~~~
a.tail()
~~~
<img width="1032" height="270" alt="image" src="https://github.com/user-attachments/assets/c90485a1-66d1-4c29-bc4d-df6ba9492d72" />



~~~
a.tail(3)
~~~
<img width="1037" height="205" alt="image" src="https://github.com/user-attachments/assets/971f90d3-a08d-451c-a14c-78a027a746ae" />



~~~
a.info()
~~~
<img width="1015" height="405" alt="image" src="https://github.com/user-attachments/assets/2e738b56-81a5-42b9-bbd1-f726415bdb21" />



~~~
a.describe()
~~~
<img width="1015" height="405" alt="image" src="https://github.com/user-attachments/assets/09ae1644-60db-447d-9958-3913693f2a5f" />



~~~
a.isnull()
~~~
<img width="1027" height="706" alt="image" src="https://github.com/user-attachments/assets/d90c327c-f7a2-459b-9f76-d337f834713a" />



~~~
a.notnull()
~~~
<img width="952" height="812" alt="image" src="https://github.com/user-attachments/assets/1a2024b8-4b4e-499d-a106-06b76ca3e230" />



~~~
a.isnull().sum()
~~~
<img width="531" height="575" alt="image" src="https://github.com/user-attachments/assets/70f16885-77df-4c33-a32d-2fccdc35a814" />



~~~
a.isnull().any()
~~~
<img width="507" height="577" alt="image" src="https://github.com/user-attachments/assets/ee589925-c28c-44dd-90c8-7d8a62df23ef" />


~~~
a.dropna()
~~~
<img width="1015" height="517" alt="image" src="https://github.com/user-attachments/assets/bcc2dd32-59ce-4823-ab8a-5f8cb529ef59" />


~~~
a.dropna(axis = 1)
~~~
<img width="441" height="797" alt="image" src="https://github.com/user-attachments/assets/5e3502e5-1787-4dfb-a5a6-955e57271ef5" />



~~~
a.fillna(1)
~~~
<img width="982" height="712" alt="image" src="https://github.com/user-attachments/assets/7a2105a9-0f26-4c2f-bcc1-a1190624dcb7" />



~~~
a.fillna(method = 'ffill')
~~~
<img width="1027" height="592" alt="image" src="https://github.com/user-attachments/assets/f9eba22e-7b23-4ae9-a6ae-13c900e61698" />


~~~
a.fillna({'GENDER':'MALE','NAME':'SRI','M4':'10'})
~~~
<img width="1005" height="767" alt="image" src="https://github.com/user-attachments/assets/75d16cd2-d7b5-4bd2-8ecd-12896187ae1d" />



~~~
ir=pd.read_csv("/content/iris.csv")
ir
~~~
<img width="822" height="547" alt="image" src="https://github.com/user-attachments/assets/f09b7afc-013e-46f4-bb1e-ea692d33e039" />
~~~
ir.head()
~~~
<img width="787" height="285" alt="image" src="https://github.com/user-attachments/assets/b009d7c6-eaac-4605-b492-2c799dd32362" />


~~~
ir.tail()
~~~
<img width="727" height="291" alt="image" src="https://github.com/user-attachments/assets/82921fe8-bb40-43f4-938b-2207af237c48" />


~~~
ir.isnull()
~~~
<img width="932" height="531" alt="image" src="https://github.com/user-attachments/assets/b5425010-0b95-411a-8d63-5e27f1499b77" />


~~~
ir.isnull().sum()
~~~
<img width="552" height="320" alt="image" src="https://github.com/user-attachments/assets/98b4e12c-2409-4cbf-8bfc-394a4cd3c044" />



~~~
ir.notnull()
~~~
<img width="762" height="530" alt="image" src="https://github.com/user-attachments/assets/f97238fb-ca82-4976-b50f-c86766c69aa4" />



~~~
import seaborn as sns
sns.boxplot(x='sepal_width',data=ir)
~~~
<img width="735" height="592" alt="image" src="https://github.com/user-attachments/assets/da8da20e-dc4e-41ea-a0c2-c7b43459e7f7" />


~~~
sns.boxplot(x='sepal_length',data=ir)
~~~
<img width="897" height="597" alt="image" src="https://github.com/user-attachments/assets/c4b3c151-c8bc-4789-ae00-c5743d446d6c" />


~~~
sns.boxplot(x='petal_width',data=ir)
~~~
<img width="842" height="582" alt="image" src="https://github.com/user-attachments/assets/f8e3e8d0-0bb3-40f3-94d3-acf345d6cb84" />


~~~
sns.boxplot(x='petal_length',data=ir)
~~~
<img width="792" height="585" alt="image" src="https://github.com/user-attachments/assets/e7a492bd-1fbf-46fe-a217-755aa45a387e" />


~~~
sns.boxplot(x='species',data=ir)
~~~
<img width="845" height="586" alt="image" src="https://github.com/user-attachments/assets/fe9b2e25-bca9-45a8-baa5-cf36f4757351" />


~~~
Q1=ir.sepal_width.quantile(0.25)
Q3=ir.sepal_width.quantile(0.75)
(IQR)=Q3-Q1
print(IQR)
~~~
<img width="587" height="145" alt="image" src="https://github.com/user-attachments/assets/25ac15b1-12df-469f-a360-81b079ac7dd9" />


~~~
ran=ir[((ir.sepal_width<(Q1-1.5*IQR))|(ir.sepal_width>(Q3+1.5*IQR)))]
ran['sepal_width']
~~~
<img width="802" height="311" alt="image" src="https://github.com/user-attachments/assets/b1d98a82-a926-4498-a0ce-9ec233696e10" />



~~~
ran=ir[~((ir.sepal_width<(Q1-1.5*IQR))|(ir.sepal_width>(Q3+1.5*IQR)))]
ran['sepal_width']
~~~
<img width="815" height="607" alt="image" src="https://github.com/user-attachments/assets/647ba8fd-f765-4011-a92b-9f13a8fdc070" />


~~~
sns.boxplot(x='sepal_width',data=ran)
~~~
<img width="746" height="587" alt="image" src="https://github.com/user-attachments/assets/4e2f44a9-5dca-4297-97bc-a3f2d04bf437" />


~~~
import numpy as np
import scipy.stats as stats
z=np.abs(stats.zscore(ir['petal_length'])) 
z
~~~
<img width="992" height="627" alt="image" src="https://github.com/user-attachments/assets/c30e535e-6118-4e21-b507-78bc5d9416ab" />

~~~
ir1=ir[z<3] 
ir1
~~~
<img width="762" height="532" alt="image" src="https://github.com/user-attachments/assets/b44964a7-a161-4cd0-8d31-c6f641b810bf" />

# Result

          Thus the given data successfully performed data cleaning and saved the cleaned data to a file
