# Sql_projeto
Um projeto basico de MySql usando join em várias tabelas para concatenar relações "n para n "

Segue abaixo a chamada para concatenar de forma a aparecer o resultado concatenado abaixo:

![1bcd76bc-943a-4163-9b27-d1b8d4e1155d](https://github.com/Luis-Impieri/Sql_projeto/assets/128927595/7c6ee779-a72c-4b89-bda6-e6bfd19e0782)

select j.nome, GROUP_CONCAT(g.generonome SEPARATOR ' e ') as genero
from jogos j
join videojogo v on j.id = v.idjogo
join genero g on g.idgenero = v.idgeneros
group by j.nome
order by j.nome;
