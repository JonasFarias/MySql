# MySql
BANDO DE DADOS MYSQL

O MySQL suporta vários tipos de dados, agrupados em quatro categorias principais: numéricos, data/hora, literais e espaciais.

Tipos de dados numéricos: incluem inteiros (como INT, TINYINT, SMALLINT, MEDIUMINT e BIGINT) e decimais (como DECIMAL e NUMERIC). Esses tipos são usados para armazenar valores numéricos exatos e de ponto flutuante.

Tipos de dados de data/hora: incluem DATE, TIME, YEAR, DATETIME e TIMESTAMP. Esses tipos são usados para armazenar valores de data e hora.

Tipos de dados literais: incluem CHAR, VARCHAR, TEXT, ENUM e SET. Esses tipos são usados para armazenar valores de texto ou de cadeias de caracteres.

Tipos de dados espaciais: incluem POINT, LINESTRING, POLYGON, MULTIPOINT, MULTILINESTRING e MULTIPOLYGON. Esses tipos são usados para armazenar valores de geometria e dados espaciais.

Em geral, é importante escolher o tipo de dados correto para cada coluna de uma tabela no MySQL, de modo a garantir a precisão dos dados e a otimização do desempenho. Por exemplo, se você está trabalhando com valores monetários, é importante usar um tipo de dados decimal preciso em vez de um tipo de dados de ponto flutuante impreciso.


numerico - inteiro(INT, TINYINT, SMALLINT, MEDIUMINT e BIGINT) - real(DECIMAL, FLOAT, DOUBLE, REAL) - logico(BIT, BOLEAN)
data/tempo - (DATE, DATATIME, TIMESTAMP, TIME, YEAR)
literal - texto (TINYTEXT, TEXT, MEDIUMTEXT, LONGTEXT) - caracteres (CHAR, VARCHAR) - binário (TINYBLOB, BLOB, MEDIUMBLOB, LONGBLOB)- coleção(ENUM, SET) 
espacial - (GEOMITRY, POINT, POLYGON, MULTIPOLYGON)



LINGUAGEM DE DEFINIÇÃO DDL
Criação de banco de dados, definições de tabelas...


		MYSQL
		 |
		 |_______________DDL Definição
		 |
		 |
		 |_______________DML Manipulação
		 |		 
		 |
		 |_______________DQL Solicitações
		 |
		 |
		 |_______________DCL Controle
		 |
		 |
		 |_______________DTL Transações



DDL
	Linguagem de Definição de Dados: comandos DDL são responsáveis pela criação, alteração e exclusão dos objetos no banco de dados.
São eles: CREATE TABLE, CREATE INDEX, ALTER TABLE, DROP
TABLE, DROP VIEW e DROP INDEX;

DML
	Linguagem de Manipulação de Dados: esses comandos indicam uma ação para o SGBD executar. Utilizados para recuperar, inserir e modificar um registro no banco de dados. Seus comandos são:
INSERT, DELETE, UPDATE, SELECT e LOCK;
DQL

DCL
	Linguagem de Controle de Dados: responsável pelo controle de
acesso dos usuários, controlando as sessões e transações do SGBD. Alguns de seus comandos são: COMMIT, ROLLBACK, GRANT e REV


DTL
	D
	I
	C
	A






Para criar um banco de dados no MySql é bem simples utilizamos o comando `CREATE DATABASE` 

Ex: `CREATE DATABSE cadastro;`

Para criar uma tabela utilizamos o comando `CREATE TABLE`
Ex: 
`CREATE TABLE aluno(
nome varchar(60);
`


 utilizando a instrução de criação, temos
o nosso primeiro código para a montagem de uma:

```
mysql> create table comclien(
n_numeclien int not null auto_increment,
c_codiclien varchar(10),
c_nomeclien varchar(100),
c_razaclien varchar(100),
d_dataclien date,
c_cnpjclien varchar(20),
c_foneclien varchar(20),
primary key (n_numeclien));
```



### Introdução à chave primária
A chave primária é o que torna a linha ou o registro de uma tabela únicos.
Geralmente, é utilizada uma sequência automática para a geração dessa chave
para que ela não venha a se repetir. Em nosso caso, o n_numeclien será
único, isto é, nenhum par de linhas possuirá o mesmo valor na mesma coluna.
Será uma sequência de preferência numérica que identificará um registro.


"""Dica: procure usar um campo para chave primária que não seja mostrado na tela de seu sistema. Crie um campo específico para ela e um
outro para você poder manipular e mostrar na tela, como o código do
cliente, por exemplo. Isso ajudará na flexibilidade do seu sistema, na manutenibilidade e na performance."""

