# O que é PostgreSQL

PostgreSQL é um sistema gerenciador de banco de dados objeto-relacional baseado no POSTGRES, Versão 4.2, desenvolvido na Universidade da Califórnia no Departamento de Ciências da Computação em Berkeley, o qual foi pioneiro em muitos conceitos que vieram a estar disponíveis em alguns bancos de dados comerciais mais tarde.

O PostgreSQL é um descendente open-source do código original de Berkeley code.

O PostgreSQL é um banco de dados objeto-relacional (sem relação com linguagens de programação orientadas a objetos), em que cada coisa criada é tratada como um objeto, tais como bancos de dados, tabelas, views, triggers, etc.

**Algumas características modernas do PostgreSQL**:

- Consultas complexas;
- Chaves estrangeiras (foreign keys);
- Gatilhos (triggers);
- Visões (views);
- Integridade transacional.

**O PostgreSQL pode ser estendido pelo usuário para muitos propósitos, por exemplo adicionando novos:**

- Tipos de dados;
- Funções;
- Operadores;
- Funções agregadas;
- Métodos de indexação;
- Linguagens procedurais.

## **Open Source e Licenciamento**

O PostgreSQL, é 100% comunitário. Isso não significa que companhias estejam longe do PostgreSQL, muito pelo contrário. Grandes empresas como EnterpriseDB, Fujitsu, Apple, Red Hat e VMWare e, até algum tempo atrás, a Sun, participam ativamente do projeto com contribuições, mas nenhuma delas é “dona” do PostgreSQL. Elas têm contribuído no formato de comunidade de desenvolvedores, por exemplo, empregando programadores que trabalham para a comunidade.

Devido à sua licença liberal (PostgreSQL License) , baseada nas licenças BSD e MIT, o PostgreSQL pode ser usado, modificado, e distribuído por qualquer um gratuitamente para qualquer propósito, seja privado, comercial, ou acadêmico.

## **Sobre instalação do PostgreSQL**

O grupo de desenvolvimento do PostgreSQL (PGDG – Postgresql Development Group) disponibiliza o PostgreSQL como código fonte e como binários. Para alguns sistemas operacionais, como Solaris, essa é a única fonte existente atualmente.

Para outros, como Windows e MacOS, o PGDG redireciona para websites de terceiros, dado que o empacotamento é tão oneroso neles que a comunidade prefere não fazê-lo quando possível. Outros ainda, como FreeBSD, OpenBSD e algumas distribuições de Linux, que têm um ciclo de entregas tão próximo com o ciclo do próprio PostgreSQL, o PGDG recomenda usar os pacotes das próprias distribuições.

Contudo, as distribuições Linux mais populares são também as mais comuns em ambientes produtivos e elas não se encaixam nos casos acima. Assim, o PGDG disponibiliza repositórios próprios contendo os pacotes para elas; e as próprias distribuições também disponibilizam pacotes do PostgreSQL.

## **Política de Versionamento**

Até a versão 9.6, o PostgreSQL adotava o modelo de versão X.Y.Z, sendo que a parte X.Y era a versão majoritária e a Z a versão minoritária. A partir da versão 10, adotou-se o modelo X.Y, sendo X a versão majoritária e Y a versão minoritária.

As versões majoritárias do PostgreSQL incluem novas funcionalidades e ocorrem uma vez por ano. As Major releases normalmente mudam o formato interno do sistema de tabelas e arquivos de dados, de forma que o dump ou o uso do módulo pg_upgrade são necessários para a atualização.

Versões minoritárias (minor releases) são numeradas incrementando a segunda parte do número da versão, e.g. 10.0 para 10.1. Nestas versões, apenas correções de bugs são aplicadas.

## **Mundo Corporativo**

No mundo corporativo, onde o PostgreSQL sempre foi adequado, seu uso vem crescendo sobre as alternativas proprietárias como Oracle Database, DB2 e Microsoft SQL Server. Essas alternativas, além de muito caras, vem perdendo em qualidade de suporte especializado. A equação é simples: enquanto numa solução proprietária o suporte é totalmente dependente de sua empresa (vendor lock-in), com o PostgreSQL existe liberdade total de escolha de suporte, assim como, modificações no código feitas por uma empresa podem beneficiar a todos, portanto, é possível “pressionar” uma empresa que suporta o PostgreSQL com maior facilidade do que a Oracle, por exemplo, pois o contrato de suporte é exclusivo dela. Para pressionar a Oracle, o cliente precisará literalmente sair do Oracle Database e isso pode ser muito mais caro que o investimento feito na compra da solução.

## **PostgreSQL na Cloud**

O PostgreSQL tornou-se o banco de dados relacional de código aberto preferencial de muitas empresas e startups e ganhou muito mercado com o crescimento exponencial da adoção de Cloud Computing.

O Cloud SQL para PostgreSQL é o serviço de banco de dados gerenciado da GCP (Google Cloud Platform) que ajuda a configurar, manter, gerenciar e administrar os bancos de dados relacionais PostgreSQL.

O Amazon RDS (AWS) facilita a configuração, a operação e a escalabilidade de implantações de PostgreSQL na nuvem. O Amazon RDS gerencia tarefas administrativas complexas e demoradas, como instalação e atualização do software PostgreSQL, gerenciamento do armazenamento, replicação para alta disponibilidade e throughput de leitura, e backups para recuperação de desastres.

O Azure Database for PostgreSQL é um banco de dados como serviço totalmente gerenciado com recursos internos, como alta disponibilidade e inteligência.

## **Investimento**

É melhor investir desde o início na solução livre PostgreSQL. O suporte ao PostgreSQL costuma ser muito rápido e ágil, pois a comunidade é muito dinâmica. Dúvidas são respondidas em questão de horas (às vezes minutos) e bugs são corrigidos em várias versões minoritárias anuais, aproximadamente uma por mês. Todos os anos uma nova versão majoritária é lançada com dezenas de novas funcionalidades. As versões têm ciclo de vida de 5 anos.

## **Outras Arquiteturas**

O PostgreSQL talvez seja o banco de dados que, entre todos, suporta a maior quantidade de arquiteturas de hardware e software do mercado. Seu sistema operacional e sua linguagem de programação de escolha provavelmente funcionarão com o PostgreSQL.

Em resumo: PostgreSQL é tendência positiva. Não morrerá por causa de uma empresa sozinha. Cresce em uso e funcionalidades todos os anos. Melhora o desempenho a cada versão. Tem suporte plural e legítimo, comunitário ou proprietário.

## **Cases Nacionais**

Grandes cases de uso público no Brasil: Tribunal de Justiça, Caixa Econômica Federal, Ministério da Saúde (Datasus), Serpro, Banco do Brasil, Celepar, Metrô de São Paulo, projeto SIVAM (Sistema de Vigilância da Amazônia).

## **Você gostou deste artigo?**

**Veja outros que temos:**

[O que é PostGIS](https://4linux.com.br/o-que-e-postgis/)

[Banco de Dados NoSQL vs Relacional](https://4linux.com.br/diferenca-banco-dados-relacional-nosql/)

[O que é PITR](https://4linux.com.br/o-que-e-pitr-banco-dados/)

[Principais Banco de Dados Open Source](https://4linux.com.br/principais-banco-dados-open-source/)



