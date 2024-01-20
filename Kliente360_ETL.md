# Índice
- [**Importar Biblioteca**](README.md#Importar-Biblioteca)
- [**Ler o Arquivo**](README.md#Ler-o-Arquivo)
- [**Verificando total de linhas do arquivo**](README.md#Verificando-total-de-linhas-do-arquivo)

## Importar Biblioteca



```python
import pandas as pd
```

### Ler o arquivo "Vendas.csv"



```python
vendas = pd.read_csv(r'C:\Users\Usuario\Desktop\Richard Araujo\Currículos\Entrevistas\Testes\Kliente 360\Arquivos\Vendas.csv', sep = ';')
vendas.head(5)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id_data</th>
      <th>id_loja</th>
      <th>id_unidade_negocio</th>
      <th>id_canal</th>
      <th>id_produto</th>
      <th>id_cupom</th>
      <th>id_cliente</th>
      <th>id_endereco_venda</th>
      <th>id_tipo_cliente</th>
      <th>qtde_venda</th>
      <th>valor_venda</th>
      <th>valor_imposto</th>
      <th>valor_custo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2019-09-21</td>
      <td>F)T`P;^+F]5F7YX^S\=+?&amp;</td>
      <td>G[)3/J:=M8+NL&amp;V&lt;"+`H30</td>
      <td>G[)3/J:=M8+NL&amp;V&lt;"+`H30</td>
      <td>AR^$EA+5@,Q]["V`\\VQC,</td>
      <td>N_N,M-K1I34E(DW*-FHTX.</td>
      <td>N$P5WZFC9VKQM(XS1DBJZ*</td>
      <td>H=ZO(L"MR+7D](@#\"/NG)</td>
      <td>A-Z4&lt;6#[I&lt;TA\FNKYY]%:+</td>
      <td>0,6</td>
      <td>16,2</td>
      <td>4,41</td>
      <td>5,736</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2019-08-06</td>
      <td>F!25!6;D=./F%2(E)D;]P0</td>
      <td>G[)3/J:=M8+NL&amp;V&lt;"+`H30</td>
      <td>G[)3/J:=M8+NL&amp;V&lt;"+`H30</td>
      <td>FC^22=\(:F=0J=F6TNPD.&amp;</td>
      <td>OEUPW7V[BY&gt;]:&gt;T;Y3"KM(</td>
      <td>P0K'8UWIADS?T"+9:-W@6*</td>
      <td>F'^..@O;\5E;#O4(^_'$0+</td>
      <td>N3ZH'W$AE#+&amp;45Z8N8"S*#</td>
      <td>0,6</td>
      <td>11,994</td>
      <td>2,154</td>
      <td>3,084</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2019-08-08</td>
      <td>FO1G"YC0G6I&amp;C(,H&amp;(MT3-</td>
      <td>G[)3/J:=M8+NL&amp;V&lt;"+`H30</td>
      <td>G[)3/J:=M8+NL&amp;V&lt;"+`H30</td>
      <td>C2O9ATWBXT.B)L-4@Y-FI$</td>
      <td>B7,9,^VTQPPN)M\$G"/I,,</td>
      <td>E\^N9TRHKU5ABQ1=?;J./'</td>
      <td>E0(*AW^9CG6ACQ2*,&amp;@LL-</td>
      <td>N3ZH'W$AE#+&amp;45Z8N8"S*#</td>
      <td>0,6</td>
      <td>11,172</td>
      <td>3,048</td>
      <td>3,192</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2019-07-28</td>
      <td>FO)5JW59TP?&amp;C:?,ZG$$L*</td>
      <td>G[)3/J:=M8+NL&amp;V&lt;"+`H30</td>
      <td>G[)3/J:=M8+NL&amp;V&lt;"+`H30</td>
      <td>CIJ6#@,X$@9;",SB)891P$</td>
      <td>JT=[J-@0OCG!X.YRK&amp;Q&amp;3!</td>
      <td>K*"!]6VAE;=C*BS-]/@_*%</td>
      <td>H:E2P/CNLQ@T$!(,0BJ,G+</td>
      <td>N3ZH'W$AE#+&amp;45Z8N8"S*#</td>
      <td>0,6</td>
      <td>2,394</td>
      <td>0,222</td>
      <td>0,468</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2019-10-26</td>
      <td>F!25!6;D=./F%2(E)D;]P0</td>
      <td>G[)3/J:=M8+NL&amp;V&lt;"+`H30</td>
      <td>G[)3/J:=M8+NL&amp;V&lt;"+`H30</td>
      <td>NLPPIQIA=`-_&gt;0I1)P[$5"</td>
      <td>E+VB+$M&gt;3GM`:$V#W?V,P*</td>
      <td>EO2UJ\6RWGUP-OSON/+Y)%</td>
      <td>A$ER-0#JA]ENP.WRSZ)#"+</td>
      <td>N3ZH'W$AE#+&amp;45Z8N8"S*#</td>
      <td>1,8</td>
      <td>4,482</td>
      <td>1,224</td>
      <td>1,296</td>
    </tr>
  </tbody>
</table>
</div>



### Verificando total de linhas do arquivo


```python
vendas['id_data'].tail(1)
```




    4081404    2019-08-24
    Name: id_data, dtype: object



### Lendo arquivos "dimensão" para identificar Primary Keys

#### Arquivo "Lojas"


```python
lojas = pd.read_csv(r'C:\Users\Usuario\Desktop\Richard Araujo\Currículos\Entrevistas\Testes\Kliente 360\Arquivos\Lojas2.csv',sep = ';')
lojas.head(1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id_loja</th>
      <th>cod_loja</th>
      <th>ano_abertura</th>
      <th>regional</th>
      <th>distrito</th>
      <th>cidade</th>
      <th>uf</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>F!25!6;D=./F%2(E)D;]P0</td>
      <td>Loja 1</td>
      <td>2013</td>
      <td>Regional 1</td>
      <td>Distrito R1.1</td>
      <td>São Paulo</td>
      <td>SP</td>
    </tr>
  </tbody>
</table>
</div>



#### Arquivo "Unidades de Negócios"


```python
negocios = pd.read_csv(r'C:\Users\Usuario\Desktop\Richard Araujo\Currículos\Entrevistas\Testes\Kliente 360\Arquivos\UnidadesNegócios2.csv', sep = ';')
negocios.head(1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id_unidade_negocio</th>
      <th>unidade_negocio</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>F3/&gt;CC-'$Y5AV(,&gt;T:)SH-</td>
      <td>Serviços</td>
    </tr>
  </tbody>
</table>
</div>



#### Arquivo "Canal"


```python
canais = pd.read_csv(r'C:\Users\Usuario\Desktop\Richard Araujo\Currículos\Entrevistas\Testes\Kliente 360\Arquivos\Canais.csv', sep = ';')
canais.head(1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>cod_canal</th>
      <th>canal</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>F)ZVUM&gt;YP&gt;1!^J;_E\**)(</td>
      <td>Digital</td>
    </tr>
  </tbody>
</table>
</div>



##### Alterado o nome da coluna "cod_canal" para "id_canal"


```python
canais.rename({'cod_canal':'id_canal','canal':'canal'}, axis=1, inplace = True)
canais.head(1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id_canal</th>
      <th>canal</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>F)ZVUM&gt;YP&gt;1!^J;_E\**)(</td>
      <td>Digital</td>
    </tr>
  </tbody>
</table>
</div>



### Arquivo "Produtos"


```python
prod = pd.read_csv(r'C:\Users\Usuario\Desktop\Richard Araujo\Currículos\Entrevistas\Testes\Kliente 360\Arquivos\Produtos.csv', sep = ';')
prod.head(1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>produto</th>
      <th>fornecedor</th>
      <th>produto_nome</th>
      <th>categoria</th>
      <th>sub_categoria</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>K*C+26:7*$6P)3PQ_%U_&amp;+</td>
      <td>Fornecedor 1</td>
      <td>Produto 1</td>
      <td>Categoria 1</td>
      <td>Subcategoria C1.1</td>
    </tr>
  </tbody>
</table>
</div>



#### Alterado o nome da coluna "produto" para "id_produto"


```python
prod.rename({'produto':'id_produto'},axis = 1, inplace=True)
prod.head(1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id_produto</th>
      <th>fornecedor</th>
      <th>produto_nome</th>
      <th>categoria</th>
      <th>sub_categoria</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>K*C+26:7*$6P)3PQ_%U_&amp;+</td>
      <td>Fornecedor 1</td>
      <td>Produto 1</td>
      <td>Categoria 1</td>
      <td>Subcategoria C1.1</td>
    </tr>
  </tbody>
</table>
</div>



### Arquivo "Tipo de Clientes"


```python
tipocliente = pd.read_csv(r'C:\Users\Usuario\Desktop\Richard Araujo\Currículos\Entrevistas\Testes\Kliente 360\Arquivos\TiposClientes2.csv',sep=';')
tipocliente.head(1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id_tipo_cliente</th>
      <th>tipo_cliente</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>B6F5#R\W*56*&amp;9H;E!S?#%</td>
      <td>Identificado</td>
    </tr>
  </tbody>
</table>
</div>



## Realizar os "Joins" / "Merge" dos arquivos


```python
Merge1 = pd.merge(vendas,lojas)
Merge2 = pd.merge(Merge1,negocios)
Merge3 = pd.merge(Merge2,canais)
Merge4 = pd.merge(Merge3,prod)
Merge5 = pd.merge(Merge4,tipocliente)
Merge5.columns
```




    Index(['id_data', 'id_loja', 'id_unidade_negocio', 'id_canal', 'id_produto',
           'id_cupom', 'id_cliente', 'id_endereco_venda', 'id_tipo_cliente',
           'qtde_venda', 'valor_venda', 'valor_imposto', 'valor_custo', 'cod_loja',
           'ano_abertura', 'regional', 'distrito', 'cidade', 'uf',
           'unidade_negocio', 'canal', 'fornecedor', 'produto_nome', 'categoria',
           'sub_categoria', 'tipo_cliente'],
          dtype='object')



### Criando o arquivo a ser utilizado para o Dashboard


```python
database = Merge5[['id_data','id_cupom','id_cliente','qtde_venda','valor_venda','valor_imposto','valor_custo','cod_loja','ano_abertura','regional','distrito','cidade','uf','unidade_negocio','canal','fornecedor','produto_nome','categoria','sub_categoria','tipo_cliente']]
database.columns
```




    Index(['id_data', 'id_cupom', 'id_cliente', 'qtde_venda', 'valor_venda',
           'valor_imposto', 'valor_custo', 'cod_loja', 'ano_abertura', 'regional',
           'distrito', 'cidade', 'uf', 'unidade_negocio', 'canal', 'fornecedor',
           'produto_nome', 'categoria', 'sub_categoria', 'tipo_cliente'],
          dtype='object')



### Salvando o arquivo com extensão .csv


```python
database.to_csv(r'C:\Users\Usuario\Desktop\Richard Araujo\Currículos\Entrevistas\Testes\Kliente 360\Arquivos\database.csv',sep=';')
database.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ano_abertura</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>4.081405e+06</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>2.015403e+03</td>
    </tr>
    <tr>
      <th>std</th>
      <td>2.568718e+00</td>
    </tr>
    <tr>
      <th>min</th>
      <td>2.011000e+03</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2.013000e+03</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>2.017000e+03</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>2.017000e+03</td>
    </tr>
    <tr>
      <th>max</th>
      <td>2.018000e+03</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
