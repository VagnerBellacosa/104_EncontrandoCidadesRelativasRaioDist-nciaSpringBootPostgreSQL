#Explore os recursos do PostGIS

Por MundoGEO

30/09/07 00h00 - Atualizado: 27/01/12 14h26

publicidade

<iframe id="google_ads_iframe_/3221002/Home_Fixas_2" title="3rd party ad content" name="google_ads_iframe_/3221002/Home_Fixas_2" width="300" height="250" scrolling="no" marginwidth="0" marginheight="0" frameborder="0" role="region" aria-label="Advertisement" tabindex="0" allow="attribution-reporting" srcdoc="" data-google-container-id="3" data-load-complete="true" style="box-sizing: border-box; border: 0px; vertical-align: bottom;"></iframe>

No primeiro artigo desta série foi visto como instalar e configurar o software PostgreSQL junto com a extensão PostGIS. Um banco de dados com suporte a dados espaciais foi criado e algumas geometrias foram importadas.

Neste artigo será visto como realizar algumas operações com a utilização das funcionalidades disponíveis no PostGIS.

**Conversão de coordenadas**

O PostGIS utiliza a excelente biblioteca Proj.4 como suporte para realizar operações de conversão de coordenadas internamente. Os leitores que trabalham com a versão do PostGIS para Windows já possuem esta biblioteca instalada automaticamente. Usuários que desejam compilar o código fonte devem lembrar de informar que desejam o suporte ao Proj.4.

O PostGIS utiliza os códigos de identificação da tabela EPSG para informar qual o sistema de referência que se está utilizando, ou para o qual deve-se converter os dados.
Veja o exemplo abaixo:

**SELECT TRANFORM(coluna_geo, 4269) FROM tabela_teste**

A consulta acima solicita ao banco de dados para transformar as geometrias, que estão na coluna COLUNA_GEO da tabela TABELA_TESTE do seu sistema de referência original (aquele definido na criação da tabela), para o sistema de referência de código 4269, ou seja, para coordenadas geográficas com datum WGS84.

Importante reforçar que o uso da função TRANSFORM implica que o sistema de referência da coluna esteja definido. Caso o código seja -1 (não definido), então as operações que utilizam conversão não serão possíveis.
Veja agora um outro exemplo para a conversão de uma coordenada que não está armazenada em nenhuma tabela específica.

**SELECT ASTEXT(TRANFORM(GEOMFROMTEXT(‘POINT(741981 7086584)’, 29182), 32722))**

Vamos quebrar a consulta acima em pedaços para entender melhor:

**SELECT ASTEXT(TRANFORM(GEOMFROMTEXT(‘POINT(741981 7086584)’, 29182), 4291))**

A função GeomFromText, destacada em azul na consulta acima, cria uma geometria a partir de um texto fornecido e um sistema de referência.

Este texto deve seguir um sintaxe específica e, neste caso, estamos criando uma geometria do tipo PONTO com localização E:741981 e N: 7086584.

Além disso, informamos que estas coordenadas estão em UTM SAD 69, fuso 22S, cujo código é 29182.
O próximo passo é converter esta geometria para o sistema de referência desejado, então utilizamos o TRANSFORM:

**SELECT ASTEXT(TRANFORM(GEOMFROMTEXT(‘POINT(741981 7086584)’, 29182), 4291))**

No destaque em vermelho vemos que o ponto está sendo convertido para o código 4291, ou seja, para coordenadas geográficas com datum SAD 69.

Por fim, a função AsText nos apresenta as novas coordenadas de forma legível. Faça uma experiência, e retire a função AsText da nossa consulta e veja o resultado. É a mesma informação, mas com uma representação diferente.

Neste ponto o leitor já poderia imaginar a criação de um ferramenta que, dadas as coordenadas e os sistemas de referência, poderia passar para o PostGIS o procedimento de conversão e retornar as informações para os usuários.

Para conhecer os sistemas de referência que estão disponíveis no seu banco, basta visualizar o conteúdo da tabela SPATIAL_REF_SYS. Para isto utilize SELECT * FROM SPATIAL_REF_SYS.

**Como encontrar objetos a uma determinada distância**

O PostGIS permite uma série de operações espaciais devido ao uso da biblioteca GEOS ([**http://geos.refractions.net**](http://geos.refractions.net/)).

A GEOS é uma biblioteca desenvolvida com apoio da mesma empresa que apóia o PostGIS, a Refractions, e tem o objetivo de criar uma biblioteca em C++ que contenha todas as funcionalidades do JTS (Java Topology Suite, ou em português, Conjunto de Topologias em Java). Atualmente a GEOS suporta todos os predicados funcionais e operadores espaciais da especificação “Simple Features for SQL”, da OGC.

Vamos a um exemplo de uma função que retorna todos os registros de uma tabela, cuja geometria esteja a menos de 100 metros de determinado ponto:
**SELECT \*
FROM tabela_teste
WHERE DISTANCE(GEOMFROMTEXT(‘POINT(1000 1000)’, -1), coluna_teste) < 100**

No exemplo acima visualizamos a nossa já conhecida função GeomFromText, que cria uma geometria a partir de um texto. Neste caso, este é o centro do círculo que vamos criar. Logo após vem a função DISTANCE, que calcula a distância entre duas geometrias, ou seja, para cada registro da tabela TABELA_TESTE, estamos calculando a distância da geometria que está na COLUNA_TESTE até o ponto criado. Por fim, o operador < 100 informa que somente os registros cuja distância seja menor que 100 metros serão retornados.

**Outras funções**

Além da TRANSFORM e DISTANCE, existem diversas outras funções dentro do PostGIS que podem e devem ser utilizadas para incrementar os sistemas desenvolvidos. Entre elas podemos citar LENGTH, AREA e ENVELOPE, entre outros. Para uma listagem completa consulte [**http://postgis.refractions.net/docs/ch06.html**](http://postgis.refractions.net/docs/ch06.html) .

Neste artigo tivemos a oportunidade de ter contato com um pequeno pedaço das funções disponíveis dentro do PostGIS. A documentação sobre estas funções é muito bem escrita e está disponível em [**http://postgis.refractions.net/docs**](http://postgis.refractions.net/docs) (inglês) e [**http://www.webgis.com.br/postgis**](http://www.webgis.com.br/postgis) (português). Baseados nesta documentação, os leitores em pouco tempo poderão criar consultas muito úteis dentro do
PostgreSQL/PostGIS.

No nosso próximo artigo iremos desenvolver uma ferramenta de conversão de coordenadas em PHP com os conceitos vistos aqui. Até lá!

+Informações
**Proj.4 – Cartographic Projections Library** é uma biblioteca que suporta a conversão de coordenadas entre os mais diversos sistemas. É utilizada na maior parte das ferramentas de software livre disponíveis atualmente, como MapServer, PostGIS e Grass, entre outros. O link para a página é [**http://proj.maptools.org**](http://proj.maptools.org/) 
(em inglês)

**Roberto Oliveira Santos**
Oracle Certified Professional
Consultor/ desenvolvedor especialista em geotecnologias
[**py5gol@gmail.com**](mailto:py5gol@gmail.com) 