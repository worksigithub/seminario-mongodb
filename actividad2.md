### [Volver al indice](README.md)

## Actividad #2

#### 1 - Crear una nueva base de datos de un sistema de streaming de video (ej. Netflix, Flow, Amazon Prime) que permita almacenar movies.
* use worksiprime

#### 2 - Para cada movie, se debería guardar información como título (String), year (Number), rating (Number, entre 1.0 y 5.0), genre (String), description (String), actors (Array<String>), country (String), income (Number), duration (Number).
* db.createCollection("movie")
  
#### 3 - Agregar películas usando insert(), insertOne() & insertMany().
* insert()
  * db.movie.insert({titulo: "tit1", year: "1998", rating: 2.0, genre: "Drama", descripcion: "desc.1", actors: ["actor 1","actor 2"], country: "USA", income: 12000, duration: 190})
* insert()
  * db.movie.insert([{titulo: "tit2", year: "2005", rating: 2.5, genre: "Accion", descripcion: "desc.2", actors: ["actor 3","actor 4"], country: "USA", income: 25000, duration: 210},{titulo: "tit3", year: "2015", rating: 3.5, genre: "Accion", descripcion: "desc.3", actors: ["actor 3","actor 4"], country: "USA", income: 35000, duration: 200}])

* insertOne()
  * db.movie.insertOne({titulo: "tit1", year: "1998", rating: 2.0, genre: "Drama", descripcion: "desc.1", actors: ["actor 1","actor 2"], country: "USA", income: 12000, duration: 190})

* insertMany()
  * db.movie.insert([{titulo: "tit2", year: "2005", rating: 2.5, genre: "Accion", descripcion: "desc.2", actors: ["actor 3","actor 4"], country: "USA", income: 25000, duration: 210},{titulo: "tit3", year: "2015", rating: 3.5, genre: "Accion", descripcion: "desc.3", actors: ["actor 3","actor 4"], country: "USA", income: 35000, duration: 200}])
  
#### 4 - Actualizar películas agregando el field highlighted=true a aquellas con rating > 4.5.
* db.movie.updateMany({rating: {$gt: 4.5}},{$set: {highlighted: true}},{ upsert: true })

#### 5 - Actualizar películas cambiando el genre “drama” por “bored”.
* db.movie.updateMany({genre: "Drama"},{$set: {genre: "Bored"})

#### 6 - Borrar todas las películas que tengan más de 30 años.

#### 7 - Buscar todas las películas argentinas.

#### 8 - Buscar todas las películas de acción con un buen rating (ej. > 4.0) que hayan salido los últimos 2 años.
