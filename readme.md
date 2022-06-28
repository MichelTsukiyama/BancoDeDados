# 1. Banco de Dados

Bancos de dados são ferramentas utilizadas para armazenamento e consulta de dados pelos softwares;

---

<br>

# 2. Sumário
<br>

- [1. Banco de Dados](#1-banco-de-dados)
- [2. Sumário](#2-sumário)
- [3. Introdução a Banco de dados](#3-introdução-a-banco-de-dados)
  - [3.1. Dado e Informação](#31-dado-e-informação)
  - [3.2. Banco de Dados Relacional(SQL) x Não Relacional(NoSQL)](#32-banco-de-dados-relacionalsql-x-não-relacionalnosql)
    - [3.2.1. Banco de Dados Relacional](#321-banco-de-dados-relacional)
    - [3.2.2. Banco de Dados Não Relacional](#322-banco-de-dados-não-relacional)
  - [3.3. Arquitetura Cliente-Servidor](#33-arquitetura-cliente-servidor)
- [4. Modelagem de Dados](#4-modelagem-de-dados)
  - [4.1. Modelagem Conceitual, Lógica e Física](#41-modelagem-conceitual-lógica-e-física)
    - [4.1.1. Modelo conceitual](#411-modelo-conceitual)
    - [4.1.2. Modelo Lógico](#412-modelo-lógico)
    - [4.1.3. Modelo Físico](#413-modelo-físico)
  - [Conceitos essenciais](#conceitos-essenciais)
  - [- **Cardinalidade Mínima** - Define a quantidade mínima de ocorrências, normalmente representadas por 0..1, 1..1, 0..n ou 0..* ('*' significa muitos);](#--cardinalidade-mínima---define-a-quantidade-mínima-de-ocorrências-normalmente-representadas-por-01-11-0n-ou-0--significa-muitos)
  - [4.2. Normalização de dados](#42-normalização-de-dados)
    - [4.2.1. Primeira Forma Normal (1FN)](#421-primeira-forma-normal-1fn)
    - [4.2.2. Segunda Forma Normal (2FN)](#422-segunda-forma-normal-2fn)
    - [4.2.3. Terceira Forma Normal (3FN)](#423-terceira-forma-normal-3fn)
    - [4.2.4. Outras Formas Normais](#424-outras-formas-normais)
  - [](#)

---

<br>

# 3. Introdução a Banco de dados


## 3.1. Dado e Informação
<br>

**Dado** -> Elemento bruto, geralmente proveniente de uma entrada do usuário ou de outros sistemas;
- Pode ser impossível saber o significado de um dado bruto;

Ex.:
. | .
----|---
1200|100
Oeste|Ricardo alves
79154| Sapatos

**Informação** -> Elemento processado/lapidado constituído de dados;
- Conjunto de dados em um contexto, sendo possível obter informações a partir destes;

Ex. tomando como base os dados acima:

Relatório mensal de venda | - | Região Oeste
-----|--------|-------
Vendedor| Ricardo Alves
Código do Empregado | 79154
|  |
Item| Quantidade | Preço Unitário
Sapatos|1200|100

Veja que agora é possível obter informações a partir dos dados organizados e tratados.

-----

<br>

## 3.2. Banco de Dados Relacional(SQL) x Não Relacional(NoSQL)
<br>

- SQL - Structure Query Language (linguagem de consulta estruturada);
- NoSQL - Not only SQL(podem ou não usar o SQL, ou ter comandos diferentes)
- Existem tipos diferentes de bancos de dados, cada um com suas características, vantagens e desvantagens;

---
<br>

### 3.2.1. Banco de Dados Relacional
<br>

- Conceito criado por **Edgar Frank Codd**, 1970;
- Dados armazenados entre tabelas que podem estar relacionadas ou não;
- Os SGBDRs (Sistemas Gerenciadores de Bancos de Dados),oferece aos usuários processos de validação, verificação e garantia de integridades dos dados.
- Oferecem controle de concorrência, recuperação de falhas e segurança, controle de transações, otmização de consulta etc.
  
**Pontos fracos**

- Dificuldade em conciliar o modelo relacional com a demanda por escalabilidade;
- Dificuldade em organizar os dados em umsistema distribuído trabalhando com particionamento de dados.

**Principais Bancos SQL**

- SQL Server;
- MySQL;
- SQLite
- Oracle Database
- PostgreSQL
- etc.

----

<br>

### 3.2.2. Banco de Dados Não Relacional
<br>

- Surgiu em 1998, a partir de uma solução de banco de dados que não oferecia uma interface SQL. Posteriormente o termo NoSQL passou a representar soluções que promoviam uma alternativa ao modelo relacional.
- Sua vantagem é a Performance, por não utilizar um modelo estruturado, consegue-se trabalhar com os dados de maneira mais rápida;
- Promovem alta disponibilidade e maior escalabilidade;

**Algumas implementações oferecem:**

- Particionamento e replicação dos dados;
- Sistemas baseados em armazenamento chave/valor;
- Sistemas orientados a documentos;
- Sistemas orientados a coluna;
- Sistemas baseados em grafos;
- etc.

**Principais Bancos NoSQL**

- MongoDB;
- Redis;
- Oracle Coherence;
- elasticsearch;
- Firebase
- etc.

-----
<br>

## 3.3. Arquitetura Cliente-Servidor
<br>

A arquitetura Cliente-Servidor nada mais é do que um cliente(navegador) fazendo requisições para servidores. Estes buscam o que foi requisitado no banco de dados e devolvem as informações para os clientes;

<center>

![cliente-servidor](src/cliente-servidor.png)

</center>

----
<br>

# 4. Modelagem de Dados
<br>

## 4.1. Modelagem Conceitual, Lógica e Física
<br>

Os modelos são usados para descrever detalhadamente a estrutura de um banco de dados.

Servem com parte importante da documentação de sistemas, auxiliam desenvolvedores e podem ser entregues ao cliente que contratou o serviço de desenvolvimento.

**Atenção**: Um modelo de dados não informa os dados armazenados, somente quais e que tipos de dados contém.

São divididos em três níveis: **Conceitual, Lógico e Físico**;

----
<br>

### 4.1.1. Modelo conceitual
<br>

- modelo de mais alto nível, mais próximo da linguagem humana;
- é desenvolvido com alto nível de abstração, a partir dos requisitos do sistema;
- pode ser elaborado de forma textual ou por diagramas de Entidade e Relacionamento e/ou Diagrama de Classes.

<center>

![modeloconceitual](src/modelo%20conceitual.png)

</center
>

----
<br>

### 4.1.2. Modelo Lógico
<br>

- Descreve como os dados serão armazenados no banco de dados, e também seus relacionamentos;
- Neste modelo pode ser definida a tecnologia a ser utilizada, Relacional ou não Relacional;

<center>

![modelo-logico](src/modelo-logico.png)

</center>

 - Também pode ser apresentado como um tabela, com exemplos de dados;

----

<br>

### 4.1.3. Modelo Físico
<br>

- Também chamado de modelo de implementação;
- descreve por meio de alguma linguagem, normalmente SQL, como será feito o armazenamento no banco;
- Aqui é feita a escolha do SGBD, levando em consideração o modelo lógico adotado.

----

<br>

## Conceitos essenciais
<br>

- **Entidade** - Objeto ou evento do mundo real sobre o qual desejamos manter registros em um banco de dados. Ex.: Carro, Produto, Aluno, Venda...(entidade e tabela são a mesma coisa);
- **Atributo** - Propriedade ou característica que descreve uma entidade. São colunas das tabelas que irão armazenar os dados. Também pode ser chamado de campo;
- **Atributo Chave** - Também conhecido por PK, primary key ou chave primária. É um campo com valor único, não pode se repetir, em todo o conjunto da Entidade. É utilizado como identificador único na tabela;
- **Relacionamentos** - Geralmente as entidades nunca estão sozinhas. Elas são relacionadas a outras entidades. Pode acontecer entre várias entidades;
- **Chave Estrangeira** - Também conhecida por Foreign key ou FK. Semelhante a PK, indica um relacionamento e a chave primária de outra tabela;
- **Grau de Relacionamento** - Indica a quantidade de entidades ligadas a um relacionamento. Pode ser unário, binário, ternário...;
- **Relacionamento Unário** - Uma entidade se relaciona com ela mesma. Ex. Funcionário -> Gerencia (funcionário gerencia outro funcionário);
- **Relacionamento Binário** - Uma entidade se relaciona com outra entidade. Modelo mais comum. Ex.: Vendedor -> Produto, são tabelas diferentes.
- **Relacionamento ternário** - Três entidades estão relacionadas. Ex. Cliente -> Tipo de pagamento -> Vendedor
- **Cardinalidade Máxima** - Quantidade máxima de ocorrências de uma entidade associada a outra entidade. Ex. Uma turma comporta vários alunos (1 : n); Uma entrega tem apenas um endereço de entrega(1 : 1); No caso de muitos para muitos (n : m) são necessárias 3 tabelas;
- **Cardinalidade Mínima** - Define a quantidade mínima de ocorrências, normalmente representadas por 0..1, 1..1, 0..n ou 0..* ('*' significa muitos);
---

<br>

## 4.2. Normalização de dados
<br>

Normalização de dados é o processo formal que examina o documento descritivo gerado pelos analistas de sistemas durante a análise de requisitos. Busca definir as entidades, atributos, relacionamentos, chaves primárias e chaves estrangeiras do banco de dados a ser modelado.

Esse processo é realizado utilizando regras bem estabelecidas conhecidas como ***Formas Normais***.

Um dos objetivos principais é evitar/amenizar anomalias e inconsistências que podem ocorrer durante a inclusão, exclusão, alteração e consulta de registros em bancos de dados.

As vantagens de uma banco de dados normalizado dentro dos padrões é a redução de manutenção, evitar o desperdício de espaço de armazenamento, etc.

Embora existam 5 formas normais, na prática usamos um conjunto de três **Formas Normais**, ou seja, um banco de dados é considerado normalizado se nele foram aplicadas as regras destas três formas normais.

----
<br>

### 4.2.1. Primeira Forma Normal (1FN)
<br>

Uma entidade estará na primeira forma normal se todos os campos forem atômicos(simples) e não multivalorados (com múltiplos valores).

Ex.:

Cód_Cliente|Nome|Telefone|Endereço
-----------|----|--------|--------
c001|Fulano de Tal|99999-9999| Rua tal, 00, cidade tal, 123456-789
c002|Ciclano|91111-1111 <br>92222-2222| Rua do ciclano, 00, cidade ciclano, 123456-000

Está em desacordo com a primeira forma normal

- O campo telefone é multivalorado, possui 2 telefones;
- o campo endereço é multivalorado, possui diversos dados;

Para corrigir o problema o campo endereço precisa ser divido em Rua, Número, Bairro e CEP.

Outra solução seria dividir em tabelas diferentes com chaves estrangeiras:

Cód_Cliente|Telefone
-----------|--------
c001|99999-9999
c002|91111-1111
c002|92222-2222


----
<br>

### 4.2.2. Segunda Forma Normal (2FN)
<br>

Uma entidade estará na 2FN se ela já se encontrar na 1FN e todos os atributos ***NÃO*** chave forem totalmente dependentes da chave primária.

Ex.:

N_pedido|Cod_Produto|Produto|Quant|Valor_Unit|Subtotal
--------|-----------|-------|-----|----------|--------
1005 | 1-934| Impressora laser| 5 | 1500.00| 7500.00
1006 | 1-956| Impressora matricial| 1 | 190.00 |190.00

Neste caso, tanto o Produto, quanto o Valor_Unit dependem do código do produto e dependem dele. Seria necessário criar outra tabela a parte:

Cod_Produto|Produto|Valor_Unit
-----------|-------|----------
 1-934| Impressora laser| 1500.00
 1-956| Impressora matricial| 190.00

----
<br>

### 4.2.3. Terceira Forma Normal (3FN)
<br>

Uma tabela estará na 3FN se estiver na 2FN e se nenhuma coluna ***NÃO*** chave depender de outra coluna ***NÃO*** chave.

Ex.:

N_pedido|Cod_Produto|Quant|Valor_Unit|Subtotal
--------|-----------|-----|----------|--------
1005 | 1-934|  5 | 1500.00| 7500.00
1006 | 1-956|  1 | 190.00 |190.00

- A Coluna Subtotal depende dos valores Quant e Valor_Unit. Como já foi feito no exemplo anterior, Valor_Unit deveria estar junto ao produto e ser removido desta tabela;
- A coluna Subtotal também deve ser removida, visto que através dos dados na tabela cód_produto e Quant ainda é possível obter o valor de Subtotal

N_pedido|Cod_Produto|Quant
--------|-----------|-----
1005 | 1-934|  5 
1006 | 1-956|  1 

----
<br>

### 4.2.4. Outras Formas Normais
<br>

Dependendo da complexidade do projeto, apesar de raro, é possível que seja necessário aplicar a 4FN ou 5FN.

- **4FN** - precisa estar na 3FN, a tabela não conter múltiplas entradas multivaloradas (valores repetidos em diferentes colunas):

paciente|plano|exame
-------|-------|----
Murilo | São Camilo| Endoscopia
Murilo | Unimed | Endoscopia
Murilo | São Camilo| Hemograma
Murilo | Unimed| Hemograma

Se realizar uma busca nessa tabela, com as colunas Exame e Plano juntas, retornaria 4 resultados para Murilo, sendo que ele possui apenas 2 planos de saúde. 

Nesse caso seria necessário criar 2 tabelas:

paciente|plano
---|---

e 

paciente|exame
----|---

- **5FN** - Precisa estar na 4FN, e quando um atributo está em outra tabela sem a necessidade de estar na tabela pesquisada, e **pode ser removido sem a perda de nenhuma informação.**

<center>

![5fn](src/5FN.png)

</center>

Veja que não é necessária a coluna idProduto(FK) na última tabela. A coluna idFornecedor(FK) já interliga as 3 tabelas, permitindo alcançar a primeira tabela de Produto

----

## 
<br>