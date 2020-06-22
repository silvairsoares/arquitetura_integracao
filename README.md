Repositório contendo os artefatos construidos para o trabalho final da disciplina:

**Arquiteturas de Integração de Aplicações** da **Faculdade Unialfa**


Alunos:

- Adão Joscelin
- Humberto Santana Melo e Silva
- Rafael Borges
- Rafael Gonzaga
- Silvair Leite Soares

**Blueprint com o esquema de funcionamento geral da integração**

![Funcionamento ESB e ETL](https://i.imgur.com/kabP7gY.jpg "Funcionamento ESB e ETL")


**Print do ESB construído com o Mule Anypoint Studio**
![Funcionamento ESB e ETL](https://i.imgur.com/XPPAgr6.jpg "Funcionamento ESB e ETL")


-----------------------------------------------
**ETL Notícias**
Criando o banco de dados!

CREATE TABLE master.dbo.noticias_feed_export (
	id int IDENTITY(0,1) NOT NULL,
	titulo varchar(100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
	conteudo varchar(100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
	autor varchar(100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
	dt_noticia varchar(10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
	CONSTRAINT noticias_feed_export_PK PRIMARY KEY (id)
) GO;

CREATE TABLE master.dbo.noticias (
	id int IDENTITY(0,1) NOT NULL,
	titulo varchar(100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
	autor varchar(100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
	conteudo varchar(100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
	dt_noticia varchar(10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
	CONSTRAINT noticias_PK PRIMARY KEY (id)
) GO;


O arquivo do utilizado no Pentaho Data Integration segue na pasta ETL.