![Logo O que é o PostgreSQL? Instalando e criando primeiro Banco de Dados](https://storage.googleapis.com/hcode.com.br/blog/posts/133/cover_copy.webp)

# O que é o PostgreSQL? Instalando e criando primeiro Banco de Dados

- [SQL](https://hcode.com.br/search?q=SQL)
- [POSTGRE](https://hcode.com.br/search?q=POSTGRE)
- [POSTGRESQL](https://hcode.com.br/search?q=POSTGRESQL)

- 22 de June de 2020
- [Anthony Rafael](https://hcode.com.br/blog/author/anthony-rafael)

[![Curso PHP 8 - A Linguagem](https://storage.googleapis.com/hcode.com.br/courses/58/logo_svg5fc37f8680ecb.svg)LançamentoCurso de PHP 8 - A LinguagemR$ 22,90R$ 599,90](https://hcode.com.br/cursos/PHP8L)

O PostgreSQL é um gerenciador de Bancos de Dados muito conhecido e usado no mundo do Desenvolvimento Web. Seus Bancos de Dados são relacionais, muito similar ao que vemos no MySQL, por exemplo.

Foi lançado no ano de 1996, mas seu desenvolvimento se iniciou na década de 1980. Ele é um projeto de código aberto e possui muitos recursos avançados, como chaves estrangeiras, triggers e stored procedures. Ele é definido por sua documentação como “O banco de dados relacional de código aberto mais avançado do mundo”. Sua versão estável mais recente é a 12.3.

Neste artigo iremos aprender como fazer sua instalação e criaremos um primeiro exemplo com o Postgres.

## Instalação

## Linux

A instalação no Linux pode ser realizada através do apt-get, com os seguintes comandos:

```routeros
sudo apt-get update
sudo apt-get install postgresql
```

## Mac

O PostgreSQL pode ser instalado no Mac através do Homebrew, com o seguinte comando:

```mipsasm
brew install postgresql
```

## Windows

Podemos instalar o Postgres no Windows por meio da linha de comando, usando o Chocolatey. Nós ensinamos a instalar este Gerenciador de Pacotes no artigo [Conhecendo Chocolatey: o Gerenciador de Pacotes do Windows](https://www.hcode.com.br/blog/conhecendo-chocolatey-o-gerenciador-de-pacotes-do-windows).

Se desejar usar o Chocolatey para a instalação, poderá usar o comando **choco install postgresql**. Contudo, se desejar realizar a instalação pelo site do PostgreSQL, poderá acessar a página de [downloads do site do Postgres](https://www.postgresql.org/download/windows/).

Nesta página, iremos escolher o download da versão 12.3, no Sistema Operacional Windows:

![Página de downloads do PostgreSQL](https://lh5.googleusercontent.com/6Q45cRfgaB95Le4Y0yb3nw00aBS30GdiHYB5m_hhky6tleEKYxDoZwxLryDD-pPtVKfl6Zlhg3-3eqnN_RJfLSXD2TDvAIEnIowOBo0wM7bh6fM943dnC_IYn0zDM12B3m6QEzaT)

Após finalizar o download, iremos executar o arquivo de instalação.

Na primeira janela, iremos pressionar “Next".

![Primeira janela da instalação](https://lh3.googleusercontent.com/D1tITY5bJz9SIb2I6DDDV7cikjSj6nlxKwulM3l0VO1rn4bNcLBDZnBTLy6RhSwVP-ldhWNb1an25YOGzJ0UEIQN2TZOaZq_6Vmg--FAd6b3vqVZMNK9hDW3NXCfgsgdh2alr1vi)

Na próxima janela iremos escolher a pasta onde o PostgreSQL será instalado.

![Segunda janela da instalação](https://lh3.googleusercontent.com/jCwItfo2LCOEqJ4qqjsczuTG6XqMUZmx7b4P93cld2-jgJEykNFo1NNBhPgZ_mYhChBfPofoJSGbfBxElK-2Bg8z_x5lezmQqcihcExM1fBqJquRznHe9LPqha0xvTz5lFmFcMqp)

O próximo passo será escolher quais recursos desejamos instalar com o Postgres. Em nosso caso, iremos deixar todas as opções marcadas.

![Terceira janela da instalação](https://lh6.googleusercontent.com/pLXn0dSVDsnfRKW5WGVwS_nFrBn5dF_-VYIZqGSzC1A9r7neDKP4zgucnV_9pTtsYVXReaiz65uoaVOe7nv0rKP9F7BDxjSCxOX1f1g8v-wJPu_dYrLngrCamhFcvOK3__fbVQZI)

Na próxima janela poderemos escolher a pasta onde os dados do Postgres serão salvos. Podemos clicar em “Next”.

![Quarta janela da instalação](https://lh6.googleusercontent.com/VRZB5qEfAxmcNYs45V7A-RWrPH8wDHR82-O-qzkIV-LWKdbSRN_x8zjSiXTEJnDBBmZRlpl6Q0XmnZ8opQzipfLsl1Z4NZ0UsL99YLrsaDfccn2qrq6lxfF_r2v4J45e27vC7vkt)

A próxima janela pedirá para definirmos a senha do super usuário do PostgreSQL, que neste Banco de Dados se chama **postgres**. Podemos definir a senha que desejarmos.

![Quinta janela da instalação](https://lh3.googleusercontent.com/2FGQGEPogxVrqM0RPfq9yftdmZ9el6SSZp2pV_xevVQgpNp63c0Cp3k9qkMHLhqnrNUJ1qsDMZlttRCCe5eCG52kRa3_IenEHqVKbMW0JvBEcmEqlmziwVWd8DX243aprpljBnYP)

A configuração que iremos definir a seguir será a porta que o Postgres irá rodar. Por padrão, a porta será a 5432 e podemos deixá-la assim. Por isso, basta clicar em “Next”.

![Sexta janela da instalação](https://lh3.googleusercontent.com/bfbzoop7AhSNM4NTnQmDMz4Z36E-0jPpq1MpU0SJ_sH216vmay_iY-aZ_Ffn3NB5Cx66hiEkLUwXFub7fLWxRJzrQJYx0qZBgnn0c44r7cHiBklDrPunp3uo7ZJuNAUy_a_Y4VIn)

A seguir iremos escolher o idioma que veremos no Postgres. Iremos escolher o Português do Brasil.

![Sétima janela de instalação](https://lh3.googleusercontent.com/w4Iu4X0PAo0zHj4dPoMLPLBPoi1cUuJI2TDBSiqCJu3CJN7q8WD3_xROVf44cQjJXBfUMxTLvkC0erEr6ZZDwE74DIawSAn06ancFN3WGfwDAERfb6VmUcCEE1HBdHq3f_M4f1bT)

A próxima janela nos mostrará um resumo dos recursos que serão instaladas em nosso computador.

![Oitava janela da instalação](https://lh3.googleusercontent.com/6PRlMp11kNLEXlx1yg6lv6-1hXqit07oHSI1uYRFLt9unij5UXsqnGrFBr-otl4oempw7waPa4OKoB9v90nW0eaDfpEmZyqAwMYFVO6RV0eUNVjDMrgeysngsG6Ba5gTKxqXUEE7)

Veremos a seguir a opção de iniciar de fato a instalação. Basta clicar em “Next” e a instalação será iniciada.

![Nona janela de instalação](https://lh4.googleusercontent.com/MWiXxpmOG0wptmUhxbjVWFbhL1N9Ogzio2GQNhhuvrjwJwVuBxSCc5hqUomsodJkLRO4Ho9vqo74kG6ajbL9N-KSF_E4hDfKBLTBhgc9rn3o9QJTDeDGHh2PZ2nx8qRTwkozF05C)

Após a instalação ser concluída, será exibida a janela de finalização do processo. Basta clicar em “Finish”.

![Janela final da instalação](https://lh6.googleusercontent.com/rt6D3hCMA37dR1UXPjzxqjTnQZ7du8KELMva-K_aYA60KbmOQOxFOLqgk_5AqczRh6WWv79IOlOZLLJDkZ3HSRdOkL3cDX2zoH60CYtEW-K8RY3tinJ__hrPiyQxNuJzJm071P88)

## Criando primeiro Banco de Dados

Para criar nosso primeiro Banco de Dados, precisamos iniciar a interface gráfica do PostgreSQL. Ela se chama pgAdmin. Diferente do MySQL Workbench, que é um programa instalado em nosso computador, o pgAdmin inicia um servidor Web em nosso localhost. Você pode encontrá-lo no Menu Iniciar:

![pgAdmin em nosso Menu Iniciar](https://lh4.googleusercontent.com/0XAEVOSNdRlpesY8zXxRt6XoOifYR_YjAjuenTMSKX_YNI3xPNyJ-3o7sQcY0HcOGN8dP8S9JQrK5Ic5Y1EFJpEVbLOnpbTEK2yi2cOs-0fum9RxqlozUUYRcV5Q_QA0kvBawCAX)

O servidor será aberto em nosso navegador. Vamos expandir a opção Servers > PostgreSQL 12.

Nesse menu, iremos clicar com o botão direito na opção “Databases” e clicar em Create > Database...

![Opção de criar um Banco de Dados no pgAdmin](https://lh5.googleusercontent.com/Bgqva8NB246HWPB_B08pKHAK3ULhov2f5__yJWL0EAt5lwIEttz78wpO54thNWy5lQqrAkI6WU95jZx2dIS77-mFHWHbKiQgC_7QwHNvlXlAi5q8Hui14K_eC6BYi0ewyaC_HfxH)

Iremos dar o nome “hcodedb” para nosso Banco de Dados e clicar em “Save”.

![Janela para criar o Banco de Dados](https://lh6.googleusercontent.com/kMpB-ztGjfk4pMZTnwtjlXWXgQEg93cm3H4R2HM7WiM9dvJTFcAIj7dXGpxOBplrdLb7baaG0VCmR4QKUMpwIvR1RsBQGOtpVEI7rMMuS8jv_DZ070hFNW2NOxkXnwPXSKeH8i1I)

Após ter nosso Banco de Dados criado, vamos criar nossa primeira tabela. Para isso, vamos clicar em cima do Banco “hcodedb” e então clicar no botão “Query Tool”, que fica ao lado da palavra “Browser”.

![Opção para criar uma nova query no Banco de Dados](https://lh3.googleusercontent.com/YSSxABKUR7MzTaUSg3MhVI3L3ZjItQqj7_PjDcdFWfzDm6tUY0VxiDPnRPev4Uq11YBQcS-lweEMfNdJqy5_OJUnbbul3cMvTTiWT6cRVmV-8Jf8gEfp065Bn6F7GiBrwHQG9PYe)

Será aberta uma janela onde poderemos executar as nossas queries no Banco de Dados.

Para criar nossa primeira tabela, iremos usar o seguinte script:

```pgsql
CREATE TABLE users (
	id SERIAL PRIMARY KEY,
	name VARCHAR(256) NOT NULL,
	email VARCHAR(256) NOT NULL
);
```

Note que a nossa coluna “id” é do tipo **SERIAL**. Esse é um tipo de dado do PostgreSQL que define que aquele campo será do tipo **AUTO_INCREMENT**, que já conhecemos no MySQL.

Para executar este script, iremos selecionar as linhas da query e pressionar o botão F5, igual ao SQL Server.

Após criar a tabela, vamos adicionar os primeiros dados a ela. Usaremos o seguinte script para isso:

```pgsql
INSERT INTO users (name, email) VALUES ('Anthony', 'anthony@hcode.com.br'), ('Glaucio Daniel', 'glaucio@hcode.com.br');
```

É importante selecionar apenas essa linha antes de pressionar o F5, para que o script de criação da tabela não seja executado de novo, o que pode gerar um erro.

Agora que os dados foram inseridos, podemos vê-los em nossa interface por meio do comando abaixo:

```n1ql
SELECT * FROM users;
```

Com este comando, veremos o seguinte resultado:

![Dados de nossa tabela retornados em nossa interface gráfica](https://lh3.googleusercontent.com/uDH3_c7KQjxehTwkgpNrgnyk0SWRjSo2U8ebBDSK7JHy3lWWSIspn-dJGHZ0CsQiy6yEId5X04qnr3esTATxjJ-p84qFA22-49zz8DZDy3nOckKRJXCR4TVCrYt_1_v9W4vOmEaM)

Excelente, a inserção dos dados ocorreu corretamente!!!

Neste artigo tivemos uma introdução ao que é o PostgreSQL e criamos nosso primeiro Banco de Dados. Perceba que, como o Postgres faz uso da linguagem SQL, há muitas semelhanças com o MySQL. Dessa forma, se já temos algum conhecimento de MySQL, não teremos dificuldades em aprender também o Postgres e usá-lo para projetar a estrutura dos dados de nossos sistemas Web.

Se você gostou deste artigo, não esqueça de compartilhar com outras pessoas. Você pode enviar sugestões de temas clicando [aqui](https://www.hcode.com.br/contato).

Obrigado por ter lido e até o próximo artigo :)