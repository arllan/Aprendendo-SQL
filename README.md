# Aprendendo-SQL
Diretorio para fins educacionais

use cadastro ;

select * from gafanhotos ;

select * from cursos ; /*seleciona todos os cursos */

select nome, carga, ano from cursos; /*seleciona apenas algumas colunas */

select * from cursos order by carga ; /* seleciona todos os cursos e ordena pela coluna 'carga' de forma do menor para o maior em numero e se for letra de forma alfabetica do 'a' até 'z'*/

select * from cursos order by carga desc ; /* seleciona todos os cursos e ordena pela coluna 'carga de forma numerica e alfabetica com uma pequena diferença, adiconando o desc inverte o sentido para ordenação vai por exemplo do maior para menor em numeros e letras vai do 'z' até 'a'  */

select ano, nome, carga from cursos order by ano, nome ; /* seleciona as colunas definidas e ordena primeiro por a coluna 'ano' e depois por 'nome' essa forma organiza os anos de forma crescente e os nomes do curso por ordem alfabetica*/

select * from cursos where ano = 2015 order by nome ; /* seleciona todas as colunas e buscar pela clasula 'where' apenas '2015' na coluna ano e ordenar tudo pela coluna 'nome'*/

/*select utilizando operadores relacionais*/

select nome, descricao, ano from cursos where ano = 2016 order by ano, nome ; /*Operador igual*/

select nome, descricao, ano from cursos where ano > 2016 order by ano, nome ; /*Operador maior que*/

select nome, descricao, ano from cursos where ano >= 2016 order by ano, nome ; /*Operador maior ou igual a que*/

select nome, descricao, ano from cursos where ano < 2016 order by ano, nome ; /*Operador menor que*/

select nome, descricao, ano from cursos where ano <= 2016 order by ano, nome ; /*Operador menor ou igual*/

select nome, descricao, ano from cursos where ano != 2016 order by ano, nome ; /*Operador 'diferente' que*/

select nome, descricao, ano from cursos where ano <> 2016 order by ano, nome ; /*Operador 'diferente' que 'outra forma de representar'*/

select nome, ano from cursos where ano between 2014 and 2016; /*comando "entre" que retorna todos os elementos da faixa selecionada 2014 até 2016 tudo que estiver nesse intervalo e retornado*/

/* Fazendo buscas por faixas de valores (between e in)*/
select nome, ano from cursos where ano between 2014 and 2016 order by ano desc, nome; /*comando "entre" que retorna todos os elementos da faixa selecionada 2014 até 2016 tudo que estiver nesse intervalo e retornado  e ainda tem a ordenação com o comando desc que inverte do maior para maior*/

select nome, ano from cursos where ano not between 2014 and 2016 order by ano desc, nome;  /*comando "fora da escala" que retorna todos os elementos fora da faixa selecionada 2014 até 2016 tudo que estiver nesse intervalo ele não retorna  e ainda tem a ordenação com o comando desc que inverte do maior para maior*/

select nome, ano from cursos where ano in(2014, 2015, 2020) order by ano desc, nome; /*comando "entre" que retorna todos os elementos da faixa selecionada 2014 até 2016 tudo que estiver nesse intervalo e retornado  e ainda tem a ordenação com o comando desc que inverte do maior para maior*/

select nome, ano from cursos where ano not in(2014, 2015, 2020) order by ano desc, nome; /*comando "fora da escala" que retorna todos os elementos fora da faixa selecionada 2014 até 2016 tudo que estiver nesse intervalo ele não retorna  e ainda tem a ordenação com o comando desc que inverte do maior para maior*/

/*operações logicas */
select nome, carga, totaulas from cursos where carga > 35 and totaulas < 30 ; /* operador 'SE' se elemento 'A' e elemento 'B' forem verdadeiros mostre */

select nome, carga, totaulas from cursos where carga > 35 or totaulas < 30 /*operador 'OU' se o elemento 'A' ou elemento 'B' forem verdadeiros mostre */ ;


/* selecionando partes similares com o comando (like e coringa %) || '%A' vai procurar o elemento 'A' no fim do elemento da string || A% vai procurar o elemento 'A' no inicio da string || '%A%' vai procurar o elemento 'A' em todas as partes da string */

select * from cursos where nome like '%A' ; /*retorna todos os elementos que na coluna 'nome' finalize com a letra A |posição do % vai determinar em qual parte vai buscar a letra*/

select * from cursos where nome like 'A%' ; /*retorna todos os elementos que na coluna 'nome' inicie com a letra A |posição do % vai determinar em qual parte vai buscar a letra*/

select * from cursos where nome like '%A%' ; /*retorna todos os elementos que na coluna 'nome' em qualquer lugar com a letra A |posição do % vai determinar em qual parte vai buscar a letra*/

select * from cursos where nome not like '%A%' ; /*retorna todos os elementos que na coluna 'nome' em que em nenhum lugar tenha a letra A |posição do % vai determinar em qual parte vai buscar a letra*/

/* distinguindo dados - apenas mostrar dados diferentes */

select distinct carga from cursos ; /* apenas mostra os dados diferentes no banco de dados, qu nesse caso mostrar as cargas horarias diferentes do banco e não mostra dados repetidos*/

select distinct nacionalidade from gafanhotos; /*mostra apenas paises diferentes no banco de dados sem repetir os nomes deles*/

/* Contabilizar registros no banco de dados*/

select count(*) from cursos ; /*contabiliza todos os cursos registrados no banco de dados*/

select count(nome) from cursos ; /*contabiliza todos os cursos registrados no banco de dados || contar apenas de um campo especifico*/

select count(*) from cursos where carga >= 30 ; /*contabiliza todos os cursos registrados no banco de dados || mostrando apenas os que estão adequados com a condição*/

/* Verificar valor maximo e minimo de colunas*/

select max(carga) from cursos ; /* Retorna o maior valor que foi cadastrado na coluna carga*/

select min(carga) from cursos ; /* Retorna o menor valor que foi cadastrado na coluna carga*/

select min(carga) from cursos where ano = '2016' ; /* Retorna o menor valor que foi cadastrado na coluna carga e ainda com condição de selecionar o ano*/

/*somar colunas para saber valor da soma total*/

select sum(carga) from cursos where ano = '2016'; /* esse comando soma de todas as tuplas de todos os cursos cadastrados a 'carga' e mostra o valor total que neste caso e: 170*/

/*retirar a media*/

select avg(carga) from cursos where ano = '2016'; /* esse comando retira a media de todas as tuplas de todos os cursos e tira a media de 'carga' e mostra o resultado*/ 


select * from gafanhotos ;


