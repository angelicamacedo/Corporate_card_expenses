# Corporate_card_expenses-
**This project aims to analyze the expenses of the former president Jair Bolsonaro's corporate card, disclosed by the General Secretariat of the Presidency in January 2023,  with the sole objective of training my skills with MySQL Wokbench** 

# About Dataset #
The data were made available by the General Secretariat of the Presidency based on a request made by [Fiquem Sabendo](https://fiquemsabendo.com.br/gastos-publicos/liberamos-o-acesso-aos-gastos-do-cartao-corporativo-de-bolsonaro-e-de-outros-ex-presidentes/). Here is the raw data [https://docs.google.com/spreadsheets/d/1LbIVxdyGCmxHBAnR-yktvBiYUMIlQB14RkGwrgP7R34/edit#gid=1524870995](url)

**Detail**

**DATA_PGTO** - Date of payments made with the corporate card
**CPF_SERVIDOR** - Individual registration on the public official who made the purchase
**CPF_CNPJ_FORNECEDOR** - National Registry Number of the Legal Entity that made the sale
**FORNECEDOR** - Service provider or trade name
**VALOR** - Amount spent
**SUBELEMENTO_DE_DESPESA** -  Shopping category

# Data cleaning and processing #

**1. Column with date information**
The spreadsheet made available contained data on the use of the corporate card since 2003, that is, information on the management of previous governments. For this analysis, I only wanted information from the administration of Jair Bolsonaro, for this reason, I had select data from the period between 2019 and 2022. 

- My starting point was to disable the SAFE UPDATE function, to modify table records:

![image](https://user-images.githubusercontent.com/120726730/212950561-e625d414-9223-46cb-8a72-8a0375604018.png)

- Converting the Date Format

![image](https://user-images.githubusercontent.com/120726730/212954059-1e8b2569-22a6-4567-9624-5efc8f6d3e51.png)

**2. Column with value information**

- Removing the "R$" symbol from the VALOR column, so that calculations can be done later
![image](https://user-images.githubusercontent.com/120726730/212954891-7c6768e2-60e1-4127-896a-8da47df5248f.png)


# Applying filters on the table #

**1. Selecting the period of action of the Bolsonaro government**

![image](https://user-images.githubusercontent.com/120726730/212956187-d411484b-e31a-4fb1-9534-41b30a076a7c.png)

**2.Selecting the 10 places that Jair Bolsonaro spent the most money**

![image](https://user-images.githubusercontent.com/120726730/212959042-48388d04-1610-489b-8062-b4f0a7e5b2cb.png)

**OUTCOME**

![image](https://user-images.githubusercontent.com/120726730/212959112-a15c7f7d-0449-492d-ba5d-439b4ebbf55b.png)

**3.What is the total amount spent with the supplier "HOTUR S PAULO PART E EMPR LTDA"?**

![image](https://user-images.githubusercontent.com/120726730/212957939-4ae7a2c4-6648-4c89-8fc4-bb7c1717c396.png)

**OUTCOME**

![image](https://user-images.githubusercontent.com/120726730/212958079-15230d33-1df1-4e81-9661-6f6db5902732.png)

**4.What are the 5 types of establishment with the highest expenses in the Bolsonaro Government?**

![image](https://user-images.githubusercontent.com/120726730/212960275-75002ad9-b4a4-4aef-9b21-5419ed62e6f0.png)

**OUTCOME**

![image](https://user-images.githubusercontent.com/120726730/212961202-466b9911-9373-402b-80d9-240959cbf968.png)

**5.Moving average spending spend per day**

![image](https://user-images.githubusercontent.com/120726730/212961785-0e6cb82b-7e5c-42b4-a053-e69ad50ee289.png)

**OUTCOME**

![image](https://user-images.githubusercontent.com/120726730/212961902-4bbdc95c-f5c0-400e-8d71-df4dddd554ea.png)

**6.Amounts spent per year**

![image](https://user-images.githubusercontent.com/120726730/212962232-e2d08d72-9f22-4e41-b80e-34af831d5552.png)

**OUTCOME**

![image](https://user-images.githubusercontent.com/120726730/212962389-2f38b4e1-2a28-42de-9bba-53a6ff9f824e.png)


That is all!
