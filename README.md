 
# ETL with Python 
## Extraction, Preparation and Transformation in a Database with Pandas to Create a Power BI Dashboard
<p>  <br>
  </p>

###### by [Richard Gomes de Araújo](https://github.com/RichardGomesDeAraujo) - 20/05/2023
[![Github Badge](https://img.shields.io/badge/-Github-000?style=flat-square&logo=Github&logoColor=white&link=https://github.com/RichardGomesDeAraujo)](https://github.com/RichardGomesDeAraujo)
[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/richardaraujoanalistadedados/)](https://www.linkedin.com/in/richardaraujoanalistadedados/)
[![Youtube Badge](https://img.shields.io/badge/-YouTube-ff0000?style=flat-square&labelColor=ff0000&logo=youtube&logoColor=white&link=https://www.youtube.com/channel/UCc_jlqHut_GkXc8ahgQHOOw)](https://www.youtube.com/channel/UCc_jlqHut_GkXc8ahgQHOOw)
<p>  <br>
  </p>
  
# Índice
- [**Importa Biblioteca**](README.md#Importar-Biblioteca)
- [**Ler um Arquivo CSV**](README.md#Ler-um-Arquivo-CSV)
- [**Verificando total de linhas**](README.md#Verificando-total-de-linhas)
- [**Alterado nome da coluna**](README.md#Alterado-nome-da-coluna)
- [**Realizar Merge**](README.md#Realizar-Merge)
- [**Criar um Database**](README.md#Criar-um-Database)
- [**Salvando arquivo com extensão csv**](README.md#Salvando-arquivo-com-extensão-csv)
- [**Salvando valores agrupados**](README.md#Salvando-valores-agrupados)
- [**Contando valores agrupados**](README.md#Contando-valores-agrupados)
- [**Média dos valores agrupados**](README.md#Média-dos-valores-agrupados)
- [**Visualização Gráfica**](README.md#Visualização-Gráfica)


<p>  <br>
  </p>
  
>## Importar Biblioteca
```PYTHON
import pandas as pd
import numpy as np
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>

>## Ler um Arquivo CSV
```PYTHON
tbl1 = pd.read_csv(r'C:\Users\Usuario\Desktop\Richard Araujo\Currículos\Entrevistas\Testes\Seazone\desafio_details.csv')
tbl2 = pd.read_csv(r'C:\Users\Usuario\Desktop\Richard Araujo\Currículos\Entrevistas\Testes\Seazone\desafio_priceav.csv')
tbl1.head(5)
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>
  
>## Verificando total de linhas
```PYTHON
vendas['id_data'].tail(1)
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>

>## Alterado nome da coluna
```PYTHON
canais.rename({'cod_canal':'id_canal','canal':'canal'}, axis=1, inplace = True)
canais.head(1)
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>

>## Realizar Merge
```PYTHON
Merge1 = pd.merge(vendas,lojas)
Merge2 = pd.merge(Merge1,negocios)
Merge3 = pd.merge(Merge2,canais)
Merge4 = pd.merge(Merge3,prod)
Merge5 = pd.merge(Merge4,tipocliente)
Merge5.columns

tbl_alldata = pd.merge(tbl1,tbl2,on='airbnb_listing_id')
tbl_alldata.head(4)
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>

>## Criar um Database
```PYTHON
database = Merge5[['id_data','id_cupom','id_cliente','qtde_venda','valor_venda','valor_imposto','valor_custo','cod_loja','ano_abertura','regional','distrito','cidade','uf','unidade_negocio','canal','fornecedor','produto_nome','categoria','sub_categoria','tipo_cliente']]
database.columns

t = tbl_alldata[['airbnb_listing_id','suburb','star_rating','booked_on','date','price_string','occupied']]
t.head(4)
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>

>## Salvando arquivo com extensão csv
```PYTHON
database.to_csv(r'C:\Users\Usuario\Desktop\Richard Araujo\Currículos\Entrevistas\Testes\Kliente 360\Arquivos\database.csv',sep=';')
database.describe()
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>

>## Somando valores agrupados
```PYTHON
# RESPONDENDO A PRIMEIRA PERGUNTA CONSIDERANDO QUE "NÚMERO DE LISTING" É O NÚMERO DO ANÚNCIO E NÃO A QUANTIDADE DE ANÚNCIO.
t1.groupby(['suburb','airbnb_listing_id']).sum()
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>

>## Contando valores agrupados
```PYTHON
# RESPONDENDO A PRIMEIRA PERGUNTA CONSIDERANDO QUE "NÚMERO DE LISTINGS" É A QUANTIDADE DE ANÚNCIOS POR BAIRRO
t2=t1.groupby('suburb').count().sort_values('airbnb_listing_id')
t2
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>

>## Média dos valores agrupados
```PYTHON
# RESPONDENDO A SEGUNDA PERGUNTA
t4 = t3.groupby('suburb').mean().sort_values('price_string')
t4
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>

>## Visualização Gráfica
```PYTHON
# CRIANDO UM GRÁFICO PARA A RESPOSTA DA SEGUNDA PERGUNTA
import matplotlib.pyplot as plt
plt.rcParams.update({'font.size':14})
t4.plot(kind='bar',color='red',title='Média de faturamento',xlabel='',ylabel='Vlr Médio')

# CRIANDO UM GRÁFICO PARA A RESPOSTA DA TERCEIRA PERGUNTA
t6.plot(kind='bar',color='red',title='Avaliações vs Faturamento',xlabel='',ylabel='Faturamento')
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>

