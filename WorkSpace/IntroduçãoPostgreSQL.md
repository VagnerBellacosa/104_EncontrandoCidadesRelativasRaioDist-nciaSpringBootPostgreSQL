# Introdução ao PostgreSQL

## Veja um pouco da história do PostgreSQL e Saiba o que é o PostgreSQL.

- [Artigos](https://www.devmedia.com.br/artigos/)[Banco de Dados](https://www.devmedia.com.br/artigos/banco-de-dados)Introdução ao PostgreSQL

É o que chamamos de SGBDRe (alguns o chamam de objeto-relacional), ou seja, é um Sistema de Gerência de Bancos de dados Relacional estendido e livre. "R" porque ele adota uma abordagem relacional. A abordagem em um SGBD é caracterizada pela forma como os dados estão organizados nesse SGBD. Em um SGBD relacional, os dados estão organizados em forma de tabelas (linhas e colunas) e suas relações (chaves estrangeiras). Notem que essa é uma definição bastante simplista de um banco de dados relacional.

O "e" em SGBDRe é de estendido, e denota que o **PostgreSQL** não está restrito à abordagem relacional. Futuramente veremos algumas dessas funcionalidades.

No meu convívio com profissionais da área de TI, tenho percebido que nem todos gostam muito de história, preferindo artigos mais técnicos, até mesmo pelo pouco tempo que, na maioria das vezes, temos disponível. Entretanto, vivemos um momento onde muitas empresas, inclusive públicas, tem realizado estudos para migração de bases de dados para software livre, seja por motivos políticos ou por redução de custo, o fato é que, conhecer um pouco da história do sistema e verificar a seriedade dos estudos que foram realizados para o seu desenvolvimento, certamente nos fornece mais subsídios para essa tomada de decisão, sem falar que enriquece as apresentações dos profissionais da área.

Curso relacionado: [Curso de PostgreSQL](http://www.devmedia.com.br/curso/curso-de-postgresql/1904)

Com relação à essa história, perceberemos que alguns anos de esforços foram, e continuam sendo, empregados para que o **PostgreSQL** se consolide, a cada dia, como o mais avançado SGBD livre.

O “pontapé” inicial aconteceu na universidade de Berkeley na Califórnia (1973), quando Michael Stonebraker e Eugene Wong, decidem iniciar um projeto de Banco de Dados Relacional e desenvolvem o Ingres. Após isso, Stonebraker sai do projeto para comercializar o Ingres, mas volta logo em seguida iniciando o projeto do post-Ingres, que buscava resolver o que considerava ser limitações do modelo relacional. Dessa forma, o post-Ingres começou a ganhar características de um SGBD estendido ou objeto-relacional. Posteriormente, o nome do sistema passou de post-Ingres (após o Ingres) para postgres. O postgres teve entre os seu financiadores organizações como a DARPA (Agência de Pesquisas em Projetos Avançados), e o ARO (Escritório de Pesquisas do Exército).

A primeira versão funcional (versão 1) foi liberada para um grupo pequeno de usuários em junho de 1989. Após a liberação da versão 4 (1993), quando o sistema já contava com uma boa popularidade, o projeto foi oficialmente abandonado pela Universidade de Berkeley e sua continuação só foi possível porque o mesmo estava sob uma licença BSD [4]. Em 1994, dois estudantes de Berkeley, Andrew Yu e Jolly Chen, adicionaram um interpretador SQL ao postgres, deram ao projeto o nome de Postgres95 e divulgaram seu código pela Internet. Com o código aberto (open source), o Postgres95 estrapolou as fronteiras da universidade permitindo que outros desenvolvedores se integrassem ao projeto. Logo, em 1996, o projeto foi renomeado para **PostgreSQL**, que refletia melhor a nova linguagem de consulta ao banco de dados, o SQL. Desde então, o **PostgreSQL** não parou de crescer, sendo mantido por um grupo de desenvolvedores e de voluntários de todo o mundo.

A partir da versão 6.0, o agora **PostgreSQL**, passou a suportar o MVCC (Multiversion Concurrency Control – Controle de Concorrência Multiversões) [5].

Um outro marco na história do PostgreSQL aconteceu com o lançamento em janeiro de 2005 da versão 8.0, que trouxe, entre outras novidades, o suporte nativo para Microsoft Windows (até então eram utilizados emuladores para executar o PostgreSQL no Windows).

Hoje, muitas empresas, que tem feito estudos sérios sobre a adoção de um SGBD livre, tem encontrado no PostgreSQL uma excelente "ferramenta" para substituição de SGBDs proprietários. O maior obstáculo para sua adoção, entretanto, tem sido a falta de mão de obra qualificada e o “lobby” das empresas detentoras de sistemas proprietários.

Tecnologias:

- [Banco de Dados](https://www.devmedia.com.br/banco-de-dados/)
-  

- [PostgreSQL](https://www.devmedia.com.br/postgresql/)
-  

- SGBD
-  

- [SQL](https://www.devmedia.com.br/sql/)