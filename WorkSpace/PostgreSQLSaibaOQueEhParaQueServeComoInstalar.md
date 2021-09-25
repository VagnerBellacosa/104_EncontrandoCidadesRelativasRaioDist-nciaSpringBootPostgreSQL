# PostgreSQL: saiba o que é, para que serve e como instalar

PostgreSQL é um gerenciador de banco de dados relacionados que otimiza muito o trabalho de quem precisa administrar informações nesses níveis. A ferramenta é de fácil instalação e de uso prático, proporcionando uma série de vantagens, especialmente com o uso de extensões.

[Ivan de Souza](https://rockcontent.com/br/blog/author/ivan/)



4 ago, 20 | Leitura: 9min

![PostgreSQL](https://rockcontent.com/br/wp-content/uploads/sites/2/2020/08/PostgreSQL-1024x538.png)

Indiscutivelmente, bancos de dados fazem parte da rotina de quem trabalha com criação, gerenciamento e [hospedagem](https://rockcontent.com/br/blog/hospedagem/) de sites. Diante disso, ferramentas funcionais e que tornem o cotidiano de trabalho mais funcional e descomplicado são essenciais, como é o caso do PostgreSQL. Essa ferramenta pode ser essencial na criação e no gerenciamento de aplicações, como sites e apps.

Quando estão em funcionamento, as estruturas dessas aplicações precisam realizar consultas constantes ao [banco de dados](https://rockcontent.com/br/blog/banco-de-dados/), para então carregar informações importantes. Paralelamente, usuários que fazem manutenções também precisam ter um acesso rápido, seguro e facilitado a esses dados. Com o PostgreSQL, essa rotina se torna mais prática.

Neste post trataremos com mais detalhes o que é essa ferramenta, de que maneira ela pode ser útil e como instalar no seu computador. O conteúdo passará pelos seguintes tópicos:

- [O que é o PostgreSQL?](https://rockcontent.com/br/blog/postgresql/#1)
- [Para que serve o PostgreSQL?](https://rockcontent.com/br/blog/postgresql/#2)
- [Como baixar e instalar o PostgreSQL no Windows?](https://rockcontent.com/br/blog/postgresql/#3)
- [Como baixar, instalar e configurar o PostgreSQL no Ubuntu 18.04?](https://rockcontent.com/br/blog/postgresql/#4)
- [Por que usar o PostgreSQL?](https://rockcontent.com/br/blog/postgresql/#5)

[Continue a leitura e confira!](https://rockcontent.com/br/blog/postgresql/#5)

## O que é o PostgreSQL?

O PostgreSQL é uma ferramenta que atua como sistema de gerenciamento de bancos de dados relacionados. Seu foco é permitir implementação da linguagem SQL em estruturas, garantindo um trabalho com os padrões desse tipo de ordenação dos dados.

Nos últimos anos, o uso desse sistema tem crescido consideravelmente, muito por conta de sua praticidade e pela sua alta compatibilidade com diferentes padrões de linguagem. Seu funcionamento é desenvolvido para ser, na prática de grande suporte para que qualquer trabalho seja feito sem maiores dificuldades.

Um de seus pontos principais é sua adequação em padrões de conformidade, ajudando a construir bancos de dados otimizados. Nesse trabalho, com suas qualidades principais, o PostgreSQL ajuda a armazenar informações de forma segura e, se necessário, restaurá-las sempre que houver solicitação de outras aplicações integradas.

O PostgreSQL é um sistema que lida bem com altos volumes de solicitações e com cargas de trabalho grandes, ou seja, funciona muito bem para sites com intensidade de acesso. [E-commerces](https://rockcontent.com/br/blog/sites-de-e-commerce/) famosos, por exemplo, é um ótimo exemplo de estrutura que precisa desse sistema para ter um desempenho otimizado, devido ao alto número de acessos simultâneos recebidos.



## Para que serve o PostgreSQL?

O PostgreSQL tem o papel de gerenciar os dados desses bancos de maneira organizada e eficaz, rodando e gravando todas as informações que ficam registradas nesses compartimentos. Por meio desse sistema, usuários podem executar consultas de maneira simples, sem precisar acessar diretamente o banco de dados.

Assim, há sempre um processo mais simples, seguro e ágil, fazendo com que apenas o servidor faça essa consulta direta à origem dos conteúdos, ou seja, o banco de dados em si. De modo geral, o PostgreSQL é um verdadeiro organizador de todas as informações, funcionando também como uma plataforma de rápido acesso para consultas e configurações.



## Como baixar e instalar o PostgreSQL no Windows?

Por mais que o PostgreSQL tenha sido desenvolvido para sistemas Linux, há também versões que funcionam perfeitamente em outros ambientes, como no Linux. O processo de instalação não é complicado, começando pelo download diretamente no [site da ferramenta](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads).

Após acessar, basta clicar na opção correta para sistemas Windows (X-86-64). Clique em “Download” e o processo será feito normalmente.

![PostgreSQL](https://rockcontent.com/br/wp-content/uploads/sites/2/2020/08/PostgreSQL1.png)

Com o arquivo no seu computador, clique duas vezes no instalador para que o processo se inicie. São etapas simples que poderão ser seguidas automaticamente.

![PostgreSQL](https://rockcontent.com/br/wp-content/uploads/sites/2/2020/08/PostgreSQL2.png)

Você chegará a uma etapa em que precisará escolher quais componentes serão instalados. Essa precisa de uma atenção maior para garantir que a ferramenta tenha tudo o que será necessário para usá-la. Dessa forma, se atente para marcas os seguintes recursos;

- PostgreSQL Server para instalar o servidor de banco de dados;
- pgAdmin 4 para instalar a ferramenta de gerenciamento de GUI do banco de dados PostgreSQL;
- Command Line Tools para instalar ferramentas de linha de comando tais como psql, pg_restore, entre outras. Essas ferramentas permitem interagir com o servidor de banco de dados PostgreSQL usando a interface de linha de comando.

![PostgreSQL](https://rockcontent.com/br/wp-content/uploads/sites/2/2020/08/PostgreSQL3.png)

Na sequência, selecione o diretório do banco de dados para armazenar os conteúdos ou simplesmente mantenha a configuração padrão de pasta de destino.

![PostgreSQL](https://rockcontent.com/br/wp-content/uploads/sites/2/2020/08/PostgreSQL4.png)

Agora é necessário configurar uma senha para superusuário do banco de dados. O PostgreSQL é executado como um serviço em segundo plano sob uma conta de serviço chamada “postgres”. Se você já criou uma conta de serviço com o nome postgres, você precisa fornecer a senha dessa conta na janela a seguir.

![PostgreSQL](https://rockcontent.com/br/wp-content/uploads/sites/2/2020/08/PostgreSQL5.png)

Após digitar a senha, você precisa digitá-la novamente para confirmar e seguir com a instalação. Na sequência, é hora de configurar um número de porta à qual o servidor irá se conectar. A porta padrão do PostgreSQL é 5432. Você precisa ter certeza de que nenhuma outra aplicação está usando esta porta.

![PostgreSQL](https://rockcontent.com/br/wp-content/uploads/sites/2/2020/08/PostgreSQL6-1.png)

No passo seguinte você precisará definir o local padrão que o PstgreSQL irá utilizar. Se você deixá-lo como padrão (locale), o PostgreSQL utilizará o locale do sistema operacional. Depois disso, siga com a instalação, sempre clicando em “Next”.

![PostgreSQL](data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20554%20436'%3E%3C/svg%3E)

Configurada a porta, o assistente de instalação mostrará o resumo das informações do PostgreSQL. revise tudo e prossiga se tudo estiver correto. Caso contrário, você precisa clicar em “Back” para alterar a configuração de acordo com o que for necessário.

![PostgreSQL](data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20552%20434'%3E%3C/svg%3E)

Com tudo devidamente pronto, agora, enfim, o assistente vai instalar os componentes do PostgreSQL no seu computador. Você verá a mensagem que afirma isso, e então basta clicar em “Next” para prosseguir.

![PostgreSQL](https://rockcontent.com/br/wp-content/uploads/sites/2/2020/08/PostgreSQL9.png)

Esse processo de instalação levará alguns minutos, o que é completamente normal. Quando ele for concluído, a janela de encerramento aparecerá na sua tela. Basta confirmar!

![PostgreSQL](data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20552%20431'%3E%3C/svg%3E)



## Como baixar, instalar e configurar o PostgreSQL no Ubuntu 18.04?

Se você precisa instalar o PostgreSQL em um Ubuntu 18.04, isso não será um problema. O processo é simples, mas há um requisito básico primário: é fundamental ter um servidor devidamente configurado para os padrões dessa ferramenta.

Uma boa dica para conseguir isso é [seguir o tutorial publicado na comunidade da ferramenta Digital Ocean](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-18-04). O conteúdo é didático e ajudará a preparar todo o ambiente para a instalação do PostgreSQL.

Com essa etapa devidamente cumprida, é hora de começar a instalação! Primeiramente, você precisa atualizar os índices de pacotes locais. No Ubuntu, os pacotes Postgres fazem parte dos repositórios padrões do sistema, eles usarão o empacotamento `apt`.

Primeiramente, você precisa instalar o pacote Postgres junto ao pacote `-contrib`. Assim, alguns recursos extras e funcionalidades importantes poderão ser adicionados.

Para realizar a instalação dessa maneira, use o comando:

```
$ sudo apt update
$ sudo apt install postgresql postgresql-contrib
```

### Criando roles

Roles nada mais são do que padrões de autenticação e autorização para flexibilizar o acesso aos bandos de dados pelo PostgreSQL. Depois que a instalação é feita, esses roles ajudam a autenticar o acesso, associando sempre a autorização a usuário Unix/Linux.

Na instalação, uma conta com nome de “postgres” é criada, se tornando padrão e permitindo o login ao usuário, ou seja, sendo uma role. Ainda assim, é possível criar outras à preferência de quem usa o PostgreSQL.

O processo é bem simples, usando principalmente o comando `createrole`. Ao realizar esse procedimento, o usuário vai se deparar com a flag `--interactive`. Ela vai solicitar o nome desse role que está sendo criado e vai questionar sobre permissões de superusuário, o que deve ser devidamente informado e configurado.

Assim, a melhor forma de conduzir o processo é logar com a conta postres citada neste conteúdo e então entrar com o comando:

```
createuser --interactive
```

Você pode também utilizar o `sudo`. Assim, não é preciso sair da sua conta:

```
sudo -u postgres createuser --interactive
```

Com esse comando, você será questionado sobre algumas informações, bastando respondê-las:

```
Output
Enter name of role to add: stage
Shall the new role be a superuser? (y/n) y
```

Com a instalação feita, agora é a hora de configurar um novo banco de dados.

### Adicionando banco de dados

Para cada role é necessário criar um banco de dados. No exemplo deste conteúdo, utilizamos o nome “stage”, como uma referência à plataforma de hospedagem WordPress [Stage](https://rockcontent.com/br/blog/rock-stage/). Você pode utilizar a que quiser, já que isso não interfere no role.

O banco de dados a ser criado precisa ter o mesmo nome, já que o PostgreSQL faz uma associação natural e automática. Dessa forma, você precisa inserir o seguinte comando.

```
createdb stage
```

Você também pode fazer isso pelo `sudo`:

```
sudo -u postgres createdb stage
```

### Abrindo prompt

Com seu novo role é possível abrir um novo prompt. É necessário, no entanto, não estar logado com o postgres. Assim, inicie com o comando:

```
$ sudo adduser stage
```

Com a nova conta ativa, conecte-se ao banco de dados executando:

```
$ sudo -i -u stage
$ psql
```

Se tudo foi configurado anteriormente, você estará agora logado. Se precisar se conectar a um outro banco de dados, especifique-o com este comando:

```
psql -d postgres
```

Se precisar, cheque o status da sua conexão desta maneira:

```
stage=# conninfo
Output
You are connected to database "stage" as user "stage" via socket in "/var/run/postgresq
```

### Criando tabelas

Criar tabelas é uma das mais importantes e úteis funcionalidades do PostgreSQL. Com ela é possível agregar dados de maneira mais organizada e de fácil acesso.

A sintaxe padrão do comando de tabelas é:

```
CREATE TABLE table_name (
    column_name1 col_type (field_length) column_constraints,
    column_name2 col_type (field_length),
    column_name3 col_type (field_length)
);
```

Os comandos acima são feitos para nomear tabelas e definir colunas, ou seja, a estruturação tradicional desse elemento. ele define também o tipo das colunas e o comprimento de cada campo. Assim, a estruturação dos dados fica padrão.

Você pode criar uma tabela de amostragem, apenas para testar o funcionamento do comando e seus resultados, previamente. Dessa forma, use este modelo:

```
CREATE TABLE playground (
    equip_id serial PRIMARY KEY,
    type varchar (50) NOT NULL,
    color varchar (25) NOT NULL,
    location varchar(25) check (location in ('north', 'south', 'west', 'east', 'northeast', 'southeast', 'southwest', 'northwest')),
    install_date date
);
```

Depois de criadas, suas tabelas podem ser visualizadas a partir do seguinte comando:

```
d
Output
                  List of relations
 Schema |          Name           |   Type   | Owner 
--------+-------------------------+----------+-------
 public | playground              | table    | sammy
 public | playground_equip_id_seq | sequence | sammy
(2 rows)
```



## Por que usar o PostgreSQL?

Há motivos claros pelos quais o PostgreSQL tem feito tanto sucesso entre profissionais do setor. A seguir, saiba por que essa ferramenta é tão útil e saiba quais são suas principais vantagens!

### Uso fácil

A facilidade de uso do PostgreSQL começa na instalação, como você pôde ver ao longo deste conteúdo. As interfaces são simples e fluídas, o que se estende também para o seu uso, em uma ferramenta que, no geral, é leve e não implica em processamento mais exigente.

### Extensões

As extensões são importantes para que o PostgreSQL funcione com mais recursos e possibilidades aos usuários. Com elas é possível trabalhar com outras linguagens, mais tipos de dados, funções diferentes e novos tipos de índices. Com uma comunidade ativa e participante, o PostgreSQL recebe novas extensões frequentemente, podendo ser baixadas pore qualquer um.

### Open source

O PostgreSQL é uma ferramenta open source, ou seja, de código aberto. Isso significa que os usuários podem fazer melhorias e mudanças no sistema, sempre projetando otimizações que podem ser aproveitadas por toda a comunidade de desenvolvedores e usuários. Como resultado, há sempre uma ótima versão à disposição de todos!

### Detalhamento nas consultas

Consultar dados mais complexos é uma outra grande vantagem de uso do PostgreSQL! É possível acessar informações mais detalhadas, com tabelas, funções e condições juntas e integradas. Ainda que sejam buscas mais complexas, o alto poder de processamento da ferramenta não torna o processo lento.

O PostgreSQL pode ser um sistema realmente útil para gerenciar bancos de dados de aplicações diversas. Não há dificuldades em saber usá-los, assim como a instalação é também simples, como você viu ao longo deste conteúdo. Há ótimas vantagens que justificam o motivo pelo qual essa é uma ferramenta de destaque.

Que tal agora entender mais sobre MySQL? [Saiba mais](https://rockcontent.com/br/blog/mysql/) sobre esse tradicional banco de dados e veja de que maneira ele pode ser útil ao seu negócio!

Compartilhe









![Ivan de Souza](data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20172%20172'%3E%3C/svg%3E)![Rock author vector](data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20172%20160'%3E%3C/svg%3E)

Author