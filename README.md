Olá. Esses são os códigos utilizados pelo nosso grupo "CoalaTech" para resolver a trilha Stone CO do Hackaton 2024 da Brasa Hacks.

CÓDIGO 1:

import pandas as pd
import matplotlib.pyplot as plt

# Dados
data = {
    "document_id": ["9,13202E+18", "9,13202E+18", "9,13202E+18", "9,13202E+18", "9,13202E+18",
                    "1,52081E+18", "1,52081E+18", "1,52081E+18", "1,52081E+18", "1,52081E+18"],
    "date_time": ["2022-12-08 01:09:53.352600", "2022-12-04 03:04:08.115900", "2022-12-07 03:07:05.865600",
                  "2022-12-05 02:45:01.539400", "2022-12-08 03:10:59.259900",
                  "2022-12-01 17:11:55.749500", "2023-05-17 02:06:09.048800", "2023-03-01 17:52:01.241600",
                  "2023-01-09 00:11:01.052900", "2023-02-20 22:53:02.811500"],
    "value": [240.00, 88.00, 76.00, 48.00, 8.00, 319.80, 9.60, 309.40, 887.32, 120.00],
    "card_number": ["", "", "", "", "", "1,50867E+18", "6,00104E+18", "", "3,18223E+18", "8,11679E+18"],
    "type": ["Pix", "Pix", "Pix", "Pix", "Pix", "Alimentação", "Alimentação", "Alimentação", "Alimentação", "Alimentação"],
    "mcc": [5499, 5499, 5499, 5499, 5499, 5422, 5422, 5422, 5422, 5422],
    "state": ["RN", "RN", "RN", "RN", "RN", "RS", "RS", "RS", "RS", "RS"]
}

df = pd.DataFrame(data)

# Contando as ocorrências de cada estado
state_counts = df['state'].value_counts()

# Criando um gráfico de barras
plt.figure(figsize=(8, 6))
plt.bar(state_counts.index, state_counts.values, color='skyblue')
plt.title('Distribuição de Transações por Estado')
plt.xlabel('Estado')
plt.ylabel('Número de Transações')
plt.show()

# Criando um gráfico de pizza
plt.figure(figsize=(8, 6))
plt.pie(state_counts, labels=state_counts.index, autopct='%1.1f%%', colors=['lightcoral', 'lightblue'])
plt.title('Distribuição Percentual de Transações por Estado')
plt.show()



# Contando as ocorrências de cada type
type_counts = df['type'].value_counts()

# Criando um gráfico de barras
plt.figure(figsize=(8, 6))
plt.bar(type_counts.index, type_counts.values, color='skyblue')
plt.title('Distribuição de Transações por Tipo')
plt.xlabel('Tipo')
plt.ylabel('Número de Transações')
plt.show()

# Criando um gráfico de pizza
plt.figure(figsize=(8, 6))
plt.pie(type_counts, labels=type_counts.index, autopct='%1.1f%%', colors=['lightcoral', 'lightblue'])
plt.title('Distribuição Percentual de Transações por Tipo')
plt.show()

CÓDIGO 2:

import pandas as pd
import matplotlib.pyplot as plt

# Dados
data = {
    "document_id": ["9,13202E+18", "9,13202E+18", "9,13202E+18", "9,13202E+18", "9,13202E+18",
                    "1,52081E+18", "1,52081E+18", "1,52081E+18", "1,52081E+18", "1,52081E+18"],
    "date_time": ["2022-12-08 01:09:53.352600", "2022-12-04 03:04:08.115900", "2022-12-07 03:07:05.865600",
                  "2022-12-05 02:45:01.539400", "2022-12-08 03:10:59.259900",
                  "2022-12-01 17:11:55.749500", "2023-05-17 02:06:09.048800", "2023-03-01 17:52:01.241600",
                  "2023-01-09 00:11:01.052900", "2023-02-20 22:53:02.811500"],
    "value": [240.00, 88.00, 76.00, 48.00, 8.00, 319.80, 9.60, 309.40, 887.32, 120.00],
    "card_number": ["", "", "", "", "", "1,50867E+18", "6,00104E+18", "", "3,18223E+18", "8,11679E+18"],
    "type": ["Pix", "Pix", "Pix", "Pix", "Pix", "Alimentação", "Alimentação", "Alimentação", "Alimentação", "Alimentação"],
    "mcc": [5499, 5499, 5499, 5499, 5499, 5422, 5422, 5422, 5422, 5422],
    "state": ["RN", "RN", "RN", "RN", "RN", "RS", "RS", "RS", "RS", "RS"]
}

df = pd.DataFrame(data)

# Contando as ocorrências de cada estado
state_counts = df['state'].value_counts()

# Criando um gráfico de barras
plt.figure(figsize=(8, 6))
plt.bar(state_counts.index, state_counts.values, color='skyblue')
plt.title('Distribuição de Transações por Estado')
plt.xlabel('Estado')
plt.ylabel('Número de Transações')
plt.show()

# Criando um gráfico de pizza
plt.figure(figsize=(8, 6))
plt.pie(state_counts, labels=state_counts.index, autopct='%1.1f%%', colors=['lightcoral', 'lightblue'])
plt.title('Distribuição Percentual de Transações por Estado')
plt.show()

CÓDIGO 3:

import matplotlib.pyplot as plt

# Dados
data = {
    "document_id": ["9,13202E+18", "9,13202E+18", "9,13202E+18", "9,13202E+18", "9,13202E+18",
                    "1,52081E+18", "1,52081E+18", "1,52081E+18", "1,52081E+18", "1,52081E+18"],
    "date_time": ["2022-12-08 01:09:53.352600", "2022-12-04 03:04:08.115900", "2022-12-07 03:07:05.865600",
                  "2022-12-05 02:45:01.539400", "2022-12-08 03:10:59.259900",
                  "2022-12-01 17:11:55.749500", "2023-05-17 02:06:09.048800", "2023-03-01 17:52:01.241600",
                  "2023-01-09 00:11:01.052900", "2023-02-20 22:53:02.811500"],
    "value": [240.00, 88.00, 76.00, 48.00, 8.00, 319.80, 9.60, 309.40, 887.32, 120.00],
    "card_number": ["", "", "", "", "", "1,50867E+18", "6,00104E+18", "", "3,18223E+18", "8,11679E+18"],
    "type": ["Pix", "Pix", "Pix", "Pix", "Pix", "Alimentação", "Alimentação", "Alimentação", "Alimentação", "Alimentação"],
    "mcc": [5499, 5499, 5499, 5499, 5499, 5422, 5422, 5422, 5422, 5422],
    "state": ["RN", "RN", "RN", "RN", "RN", "RS", "RS", "RS", "RS", "RS"]
}

df = pd.DataFrame(data)

# Contando as ocorrências de cada estado
state_counts = df['state'].value_counts()

# Criando um gráfico de barras
plt.figure(figsize=(8, 6))
plt.bar(state_counts.index, state_counts.values, color='skyblue')
plt.title('Distribuição de Transações por Estado')
plt.xlabel('Estado')
plt.ylabel('Número de Transações')
plt.show()

# Criando um gráfico de pizza
plt.figure(figsize=(8, 6))
plt.pie(state_counts, labels=state_counts.index, autopct='%1.1f%%', colors=['lightcoral', 'lightblue'])
plt.title('Distribuição Percentual de Transações por Estado')
plt.show()
