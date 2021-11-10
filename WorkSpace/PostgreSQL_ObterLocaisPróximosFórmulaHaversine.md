# [PostgreSQL] Obter locais próximos (fórmula de Haversine)

[1 comentário](https://bragil.wordpress.com/2011/08/16/postgresql-obter-locais-proximos-formula-de-haversine/#comments)

Sabe aquele recurso que algumas redes sociais têm, de exibir os pontos próximos à sua localização? Sim, é possível e bem simples de fazer. A fórmula matemática que faz tudo funcionar chama-se [Fórmula de Haversine](http://pt.wikipedia.org/wiki/Fórmula_de_Haversine). Sem mais delongas, vamos ao código:

```
-- Cálculo da distância entre dois pontos usando a fórmula de Haversine em PostgreSQL
CREATE OR REPLACE FUNCTION distancia_km(lat1 NUMERIC, lng1 NUMERIC, lat2 NUMERIC, lng2 NUMERIC)
RETURNS DOUBLE PRECISION AS
$BODY$
	SELECT 6371 * acos(
		sin( radians($1) ) * sin( radians( $3 ))
	      + cos( radians($1) ) * cos( radians( $3 )) * cos(radians($4) - radians($2))  )
	as distance;
$BODY$
  LANGUAGE sql IMMUTABLE
  COST 100;
```

Suponhamos que exista uma tabela de usuários onde exista os campos latitude e longitude. É fácil criar uma query usando a função acima para trazer os usuários mais próximos do seu local, em um raio de 10 Km:

```
SELECT * FROM usuarios WHERE distancia_km(minha_latitude, minha_longitude, latitude, longitude) <= 10
AND distancia_km(minha_latitude, minha_longitude, latitude, longitude) > 0
```

Serão listados os usuários que estão a menos de 10 Km de distância de você.

OBS: Se quiser usar milhas ao invés de quilômetros, use a constante 3959 ao invés de 6371 na função:

```
-- Cálculo da distância entre dois pontos usando a fórmula de Haversine em PostgreSQL
CREATE OR REPLACE FUNCTION distancia_milhas(lat1 NUMERIC, lng1 NUMERIC, lat2 NUMERIC, lng2 NUMERIC)
RETURNS DOUBLE PRECISION AS
$BODY$
	SELECT 3959 * acos(
		sin( radians($1) ) * sin( radians( $3 ))
	      + cos( radians($1) ) * cos( radians( $3 )) * cos(radians($4) - radians($2))  )
	as distance;
$BODY$
  LANGUAGE sql IMMUTABLE
  COST 100;
```

Anúncios

DENUNCIAR ESTE ANÚNCIO

### Share this:

- [Twitter](https://bragil.wordpress.com/2011/08/16/postgresql-obter-locais-proximos-formula-de-haversine/?share=twitter&nb=1)
- [Facebook](https://bragil.wordpress.com/2011/08/16/postgresql-obter-locais-proximos-formula-de-haversine/?share=facebook&nb=1)