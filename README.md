 
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
- [**Salvando arquivo com extensão .csv**](README.md#Salvando-arquivo-com-extensão-.csv)


<p>  <br>
  </p>
  
>## Importar Biblioteca
```PYTHON
   import pandas as pd
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>

>## Ler um Arquivo CSV
```PYTHON
    vendas = pd.read_csv(r'C:\Users\Usuario\Desktop\Richard Araujo\Currículos\Entrevistas\Testes\Kliente 360\Arquivos\Vendas.csv', sep = ';')
vendas.head(5)
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
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>

>## Criar um Database
```PYTHON
database = Merge5[['id_data','id_cupom','id_cliente','qtde_venda','valor_venda','valor_imposto','valor_custo','cod_loja','ano_abertura','regional','distrito','cidade','uf','unidade_negocio','canal','fornecedor','produto_nome','categoria','sub_categoria','tipo_cliente']]
database.columns
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>

>## Salvando arquivo com extensão .csv
```PYTHON
database.to_csv(r'C:\Users\Usuario\Desktop\Richard Araujo\Currículos\Entrevistas\Testes\Kliente 360\Arquivos\database.csv',sep=';')
database.describe()
```
###### [⏪](README.md#Índice)
<p>  <br>
  </p>
