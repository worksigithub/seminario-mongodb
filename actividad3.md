### [Volver al indice](README.md)

## Actividad #3

#### 1 - Utilizar la misma base de datos de películas e insertar varias películas con distinto contenido.
* db.movie.insert([{titulo: "tit30", year: 2018, rating: 2.5, genre: "Accion", descripcion: "desc.2", actors: ["actor 3","actor 4"], country: "Argentina", income: 25200, duration: 210},{titulo: "tit31", year: 2010, rating: 1.5, genre: "Drama", descripcion: "desc.3", actors: ["actor 3","actor 4"], country: "USA", income: 35000, duration: 200}])

#### 2 - Listar todas las películas del año 2018.
* db.movie.find({year: 2018})

#### 3 - Listar las 10 primeras películas de Hollywood.
* db.movie.find({country: "USA"}).limit(10)

#### 4 - Listar las 5 películas más taquilleras.
* db.movie.find().limit(10).sort({income: -1})

#### 5 - Listar el 2do conjunto de 5 películas más taquilleras.
* db.movie.find().skip(5).limit(10).sort({income: -1})

#### 6 - Repetir query 3 y 4 pero retornando sólo el título y genre.
* db.movie.find({country: "USA"}, {titulo: 1, genre: 1}).limit(10)
* db.movie.find({}, {titulo: 1, genre: 1}).limit(10).sort({income: -1})

#### 7 - Mostrar los distintos países que existen en la base de datos.
* db.movie.distinct("country")
