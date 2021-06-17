#!/usr/bin/env python
# coding: utf-8

# In[1]:


import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
get_ipython().run_line_magic('matplotlib', 'inline')
pd.pandas.set_option('display.max_columns',None)


# In[2]:


df=pd.read_excel("Raw File.xlsx")
df_mis=pd.read_csv("Disbursement MIS (1).csv")
df_para=pd.read_excel("Credit Parameter.xlsx")


# In[3]:


df.head(3)


# In[4]:


df_mis.head()


# In[5]:


df.shape


# In[6]:


df1=pd.merge(df,df_para,on='Loan No',how='left')


# In[7]:


df2=pd.merge(df_mis,df_para,on='Loan No',how='left')


# In[8]:


df1.drop(['mobile','city','pan_number','business_name','city.1','pin.1','brothers_sisters','spouse_parents','processing_time'],axis=1,inplace=True)


# In[9]:


df1.head(3)


# In[10]:


df1['Loan Amt'].value_counts()


# In[11]:


df1.groupby('existing_obligation').agg({"April":"sum"})


# In[12]:


labels=['Low','High']
pd.qcut(df2['existing_obligation'],q=3,duplicates='drop',labels=labels).value_counts()


# In[13]:


labels=['Low','High']
df1['obli']=pd.qcut(df1['existing_obligation'],q=3,duplicates='drop',labels=labels)
df1.groupby('obli').agg({'April':'sum'})


# In[29]:


df2.business_premises_ownership.value_counts()


# In[15]:


df1.head()


# In[28]:


df1.groupby('business_premises_ownership').agg({'April':'sum'})


# In[30]:


df1.groupby('residence_ownership').agg({'April':'sum'})


# In[31]:


df2.residence_ownership.value_counts()


# In[35]:


df2.is_business_residence_same.value_counts()


# In[36]:


df1.groupby('is_business_residence_same').agg({'April':'sum'})


# In[40]:


df1.groupby('applicant_type').agg({'April':'sum'})


# In[41]:


df2['applicant_type'].value_counts()


# In[45]:


df1.groupby(['applicant_type','Bureau Band']).agg({'April':'sum'})


# In[52]:


df2.groupby(['applicant_type','Bureau Band']).agg({'Bureau Band':'count'})


# In[53]:





# In[55]:


19+136


# In[ ]:




