# MySQL

Anotações online do MySQL.
Aula 30/07 
Passo a passo base do MySQL e suas utilidades. Paramos na Pag 8 tipos de Dados.

-----

Banco de Dados.
Aula 13/08


```
create database Cogitare_bd;
CREATE database Exerjd_db;
drop database Cogitare_bd;
use Exerjd_db;

show databases;

create table aluno_tb(
Id integer not null, 
NomeAl varchar(50) null,
NotaAl Decimal(6,2) /* Exemplo: 9999.99  sendo necessário usar o ".", afinal se usar o "," ele vai identificar como dois  parâmetros.*/ 
);

show tables;

describe aluno_tb;

create table tbaluno2(
Id int primary key not null,/* nome titulo e restrições*/
Sexo char(1) default 'F', /* Default funciona como o valor padrão, logo quando não colocado, este valor inserido pelo comando vai ser mostrado.*/
datanasc date not null,
Salario float null,
check (Salario > 1000), /* Literalmente uma checagem*/
CPF bigint not null unique
);

describe tbaluno2; /* demonstra a tabela de maneira mais eficaz.*/

-- DDL --´
-- create / drop / alter

alter table tbaluno2 drop datanasc; /* alteração na tabela. Nome da tabela, ação e objeto*/

alter table tbaluno2 add datanasc date null; /* desta vez adicionando e colocando a sua restrição*/

alter table tbaluno2 modify datanasc date not null; /* Modify simplesmente modificando a coluna.*/

truncate table aluno_tb; /* Uma espécie de "delete". A tabela continua existindo mas ele apaga permanentemente os registros de uma tabela. Isso pode ser utilizado quando existem muitos "Gaps" em sua tabela.*/
`
paramos no comandos DDL 
