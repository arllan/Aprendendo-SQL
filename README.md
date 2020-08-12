# Aprendendo-SQL
Diretorio para fins educacionais. Neste diretorio vocês vão encontrar todos os comandos utilizados na aula de select do curso em vídeo.


## Aula Select - 01
[![Watch the video](https://raw.githubusercontent.com/arllan/Aprendendo-SQL/master/curso_em_video_aula_select_1_2.PNG)](https://bit.ly/3kdzyBb)



## Aula Select - 02
[![Watch the video](https://raw.githubusercontent.com/arllan/Aprendendo-SQL/master/curso_em_video_aula_select_1_2.PNG)](https://bit.ly/30w3wZv)


| COMANDO  | DESCRIÇÃO DO COMANDO | 
| :------------ |:---------------:|
|use cadastro ;|Seleciona o banco a ser utilizado|
| select * from gafanhotos ;      | seleciona a tabela 'gafanhotos' e mostra todas as tuplas |
| select * from cursos ;  | /*seleciona todos os cursos */ |
| select nome, carga, ano from cursos; |  /*seleciona apenas algumas colunas */| 
|select * from cursos order by carga ;| /* seleciona todos os cursos e ordena pela coluna 'carga' de forma do menor para o maior em numero e se for letra de forma alfabetica do 'a' até 'z'*/|
|select * from cursos order by carga ;| /* seleciona todos os cursos e ordena pela coluna 'carga' de forma do menor para o maior em numero e se for letra de forma alfabetica do 'a' até 'z'*/|
|select * from cursos order by carga desc ;| /* seleciona todos os cursos e ordena pela coluna 'carga de forma numerica e alfabetica com uma pequena diferença, adiconando o desc inverte o sentido para ordenação vai por exemplo do maior para menor em numeros e letras vai do 'z' até 'a'  */|
|select ano, nome, carga from cursos order by ano, nome ;|/* seleciona as colunas definidas e ordena primeiro por a coluna 'ano' e depois por 'nome' essa forma organiza os anos de forma crescente e os nomes do curso por ordem alfabetica*/|
|select * from cursos where ano = 2015 order by nome ;| /* seleciona todas as colunas e buscar pela clasula 'where' apenas '2015' na coluna ano e ordenar tudo pela coluna 'nome'*/|
|select nome, descricao, ano from cursos where ano = 2016 order by ano, nome ; |/*Operador igual*/|
|select nome, descricao, ano from cursos where ano > 2016 order by ano, nome ;|/*Operador maior que*/|
|select nome, descricao, ano from cursos where ano >= 2016 order by ano, nome ; |/*Operador maior ou igual a que*/|
|select nome, descricao, ano from cursos where ano < 2016 order by ano, nome ;| /*Operador menor que*/|
|select nome, descricao, ano from cursos where ano <= 2016 order by ano, nome ; |/*Operador menor ou igual*/|
|select nome, descricao, ano from cursos where ano != 2016 order by ano, nome ;|/*Operador 'diferente' que*/|
|select nome, descricao, ano from cursos where ano <> 2016 order by ano, nome ;| /*Operador 'diferente' que 'outra forma de representar'*/|
|select nome, ano from cursos where ano between 2014 and 2016;| /*comando "entre" que retorna todos os elementos da faixa selecionada 2014 até 2016 tudo que estiver nesse intervalo e retornado*/|
|select nome, ano from cursos where ano between 2014 and 2016 order by ano desc, nome;| /*comando "entre" que retorna todos os elementos da faixa selecionada 2014 até 2016 tudo que estiver nesse intervalo e retornado  e ainda tem a ordenação com o comando desc que inverte do maior para maior*/|
|select nome, ano from cursos where ano not between 2014 and 2016 order by ano desc, nome; | /*comando "fora da escala" que retorna todos os elementos fora da faixa selecionada 2014 até 2016 tudo que estiver nesse intervalo ele não retorna  e ainda tem a ordenação com o comando desc que inverte do maior para maior*/|
|select nome, ano from cursos where ano in(2014, 2015, 2020) order by ano desc, nome;| /*comando "entre" que retorna todos os elementos da faixa selecionada 2014 até 2016 tudo que estiver nesse intervalo e retornado  e ainda tem a ordenação com o comando desc que inverte do maior para maior*/|
|select nome, ano from cursos where ano not in(2014, 2015, 2020) order by ano desc, nome;| /*comando "fora da escala" que retorna todos os elementos fora da faixa selecionada 2014 até 2016 tudo que estiver nesse intervalo ele não retorna  e ainda tem a ordenação com o comando desc que inverte do maior para maior*/|
|select nome, carga, totaulas from cursos where carga > 35 and totaulas < 30 ; |/* operador 'SE' se elemento 'A' e elemento 'B' forem verdadeiros mostre */|
|select nome, carga, totaulas from cursos where carga > 35 or totaulas < 30 ;|/*operador 'OU' se o elemento 'A' ou elemento 'B' forem verdadeiros mostre */ |
|select * from cursos where nome like '%A' ;|/* selecionando partes similares com o comando (like e coringa %) - '%A' vai procurar o elemento 'A' no fim do elemento da string - A% vai procurar o elemento 'A' no inicio da string - '%A%' vai procurar o elemento 'A' em todas as partes da string */|
|select * from cursos where nome like 'A%' ; |/* selecionando partes similares com o comando (like e coringa %) - '%A' vai procurar o elemento 'A' no fim do elemento da string - A% vai procurar o elemento 'A' no inicio da string - '%A%' vai procurar o elemento 'A' em todas as partes da string */|
|select * from cursos where nome like '%A%' ;|/* selecionando partes similares com o comando (like e coringa %) - '%A' vai procurar o elemento 'A' no fim do elemento da string - A% vai procurar o elemento 'A' no inicio da string - '%A%' vai procurar o elemento 'A' em todas as partes da string */|
|select * from cursos where nome not like '%A%' ;| /*retorna todos os elementos que na coluna 'nome' em que em nenhum lugar tenha a letra A |posição do % vai determinar em qual parte vai buscar a letra*/|
|select distinct carga from cursos ;| /* apenas mostra os dados diferentes no banco de dados, qu nesse caso mostrar as cargas horarias diferentes do banco e não mostra dados repetidos*/|
|select distinct nacionalidade from gafanhotos;|/*mostra apenas paises diferentes no banco de dados sem repetir os nomes deles*/|
|select count(*) from cursos ;|/*contabiliza todos os cursos registrados no banco de dados*/|
|select count(nome) from cursos ;| /*contabiliza todos os cursos registrados no banco de dados - contar apenas de um campo especifico*/|
|select count(*) from cursos where carga >= 30 ;| /*contabiliza todos os cursos registrados no banco de dados - mostrando apenas os que estão adequados com a condição*/|
|select max(carga) from cursos ;| /* Retorna o maior valor que foi cadastrado na coluna carga*/|
|select min(carga) from cursos ;| /* Retorna o menor valor que foi cadastrado na coluna carga*/|
|select min(carga) from cursos where ano = '2016' ;| /* Retorna o menor valor que foi cadastrado na coluna carga e ainda com condição de selecionar o ano*/|
|select sum(carga) from cursos where ano = '2016';|/* esse comando soma de todas as tuplas de todos os cursos cadastrados a 'carga' e mostra o valor total que neste caso e: 170*/|
|select avg(carga) from cursos where ano = '2016';|/* esse comando retira a media de todas as tuplas de todos os cursos e tira a media de 'carga' e mostra o resultado*/ |


## Aula 04 - Manipulando e alterando colunas, bancos e tabelas.

| COMANDO  | DESCRIÇÃO DO COMANDO | 
| :------------ |:---------------:|
|create database curso default character set utf8 default collate utf8_general_ci;|estrutura para criar o banco com formulação de caracteres do padrão utf8 "sulamericano de acentuação|
|describe pessoas;|Mostrar a estrutura do banco de dados|
|alter table pessoas add column profissao varchar(10);|adicionar uma coluna na tabela já criada|
|alter table pessoas modify column profissao varchar(50);|Modifica uma 'CONSTRAINTS' de um campo já existente do banco de dados obs: apenas modifica a propriedade de uma coluna|
|alter table pessoas change column profissao novoProfissao varchar(30);| Altera o nome de uma coluna e seus 'CONSTRAINTS' obs: esse comando só deve ser utilizado quando for modificar o nome da coluna. Se for apenas modificar alguma constrains utilize o comando 'column|
|alter table pessoas drop column profissao;| Apagar uma coluna do banco de dados|
|alter table pessoas rename to gafanhotos ;|Altera o nome da tabela. Precisa colocar o nome antigo e o novo como está descrito no comando|

```sql
create database curso default character set utf8 default collate utf8_general_ci;

use curso ;

CREATE TABLE pessoas (
	id int not null auto_increment primary key,
	nome varchar(30) NOT NULL,
    nascimento date,
    sexo enum('M','F'),
    peso decimal(5,2),
    altura decimal(3,2),
    nacionalidade varchar(20) default 'Brasil'
) DEFAULT CHARSET = utf8;
```
 ## Aula 05 - Utilizando 'CONSTRAINTS' - São elementos complementares que sempre tem o papel de completar outro comando.

| COMANDO  | DESCRIÇÃO DO COMANDO | 
| :------------ |:---------------:|
|NOT NULL|informa que o campo não pode ficar sem nenhuma informação e assim obriga adicionar algum conteudo ao ser criado|
|DEFAULT|Se caso nenhum 'informação' for adicionado ao campo ele vai assumir um valor padrão que deve esta em spas|
|ENUM('elementoA','elementoB','elementoC')|Limita receber apenas um dos elementos, que são listados dentro do comando|
|UNIQUE|quando adicionado esse campo em uma coluna limita que esse campo seja unico e que nenhuma outra tupla tenha a mesma informação desse campo|


## Aula 06 - Tipos de variaveis

### Variavel do tipo inteiro
- Inteiro
   * Int
   * BigInt
   * MediumInt
   * SmallInt
- Real
   * Decimal
   * Float
   * Double
   * Real
- Lógico
   * Bit
   * Boolean
   
### Variavel do tipo time/date
- Data/Tempo
		* Date
  * dateTime
  * TimeStamp
  * Time
  * year

### Variavel do tipo Literal

- Caractere
		* Char
  * VarChar
- Texto
		* TinyText
  * Text
  * LongText
- Binário
		* TinyBlob
  * Blob
  * MediumBlob
  * LongBlob
- Coleção
		* Enum
  * Set
