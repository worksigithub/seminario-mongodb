### [Volver al indice](readme.md)

## Actividad #1

#### 1 - Instalar MongoDB en ambiente local.
* Ok

#### 2 - Conectarse a MongoDB vía CLI.
* Ok

#### 3 - Crear una nueva base de datos llamada futbolfifa.
* use futbolfifa
* show dbs

#### 4 - Crear una nueva collection llamada players.
* db.createCollection("players")
* show collections

#### 5 - Insertar 5 documentos en la collection players con datos básicos (nombre, apellido, posición, fecha de nacimiento, etc).
* db.players.insert({nombre: "Nom1", apellido: "Ape1", posicion: "Arquero", fechaNacimiento: "2000-01-01", altura: 185})
* db.players.insert({nombre: "Nom2", apellido: "Ape2", posicion: "Defensor", fechaNacimiento: "2000-02-01", altura: 175})
* db.players.insert({nombre: "Nom3", apellido: "Ape3", posicion: "Defensor", fechaNacimiento: "2000-03-01", altura: 180})
* db.players.insert({nombre: "Nom4", apellido: "Ape4", posicion: "Mediocampo", fechaNacimiento: "2000-04-01", altura: 165})
* db.players.insert({nombre: "Nom5", apellido: "Ape5", posicion: "Delantero", fechaNacimiento: "2000-05-01", altura: 165})

#### 6 - Listar todos los documentos de la collection players.
* db.players.find()
   * { "_id" : ObjectId("5f84bb2939c813d2af177080"), "nombre" : "Nom1", "apellido" : "Ape1", "posicion" : "Arquero", "fechaNacimiento" : "2000-01-01", "altura" : 185 }
   * { "_id" : ObjectId("5f84bb8139c813d2af177081"), "nombre" : "Nom2", "apellido" : "Ape2", "posicion" : "Defensor", "fechaNacimiento" : "2000-02-01", "altura" : 175 }
   * { "_id" : ObjectId("5f84bb8939c813d2af177082"), "nombre" : "Nom3", "apellido" : "Ape3", "posicion" : "Defensor", "fechaNacimiento" : "2000-03-01", "altura" : 180 }
   * { "_id" : ObjectId("5f84bb9239c813d2af177083"), "nombre" : "Nom4", "apellido" : "Ape4", "posicion" : "Mediocampo", "fechaNacimiento" : "2000-04-01", "altura" : 165 }
   * { "_id" : ObjectId("5f84bb9a39c813d2af177084"), "nombre" : "Nom5", "apellido" : "Ape5", "posicion" : "Delantero", "fechaNacimiento" : "2000-05-01", "altura" : 165 }

#### 7 - Crear otras collections con documentos (ej. teams, games, etc).
* db.createCollection("teams")
* db.createCollection("games")
* db.createCollection("stadiums")
* show collections
 * games
 * players
 * stadiums
 * teams

* db.teams.insert({nombre: "Team1"})
* db.teams.insert({nombre: "Team2"})
* db.teams.insert({nombre: "Team3"})
* db.games.insert({nombre: "Copa America",pais: "Argentina", fechaInicio: "2020-11-01"})
* db.stadiums.insert({nombre: "Stadium1",pais: "Argentina", localidad: "Buenos Aires"})
    


