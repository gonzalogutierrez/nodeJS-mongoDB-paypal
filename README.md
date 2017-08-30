"# nodeJS-mongoDB-paypal" 

1)Levante el servidor de mongoDB localmente con el comando

mongod.exe --config mongodb.config


ARCHIVO mongodb.config
            systemLog:
                destination: file
                path: c:\data\log\mongod.log
            storage:
                dbPath: c:\data\db


2) Levante el cliente mongo localmente con el siguiente comando

mongo.exe

3) Inserte en la tabla users y project los datos para el login y mostrar proyectos con el siguiente script:

SCRIPT: 
use dbProgramacionColaborativa
db.users.insert({"name" : "Gonzalo", "lastname" : "Gutierrez", "email" : "gonzaguti85@gmail.com", "password" : "pomelo", "username" : "ggutierrez" })
db.project.insert({"name" : "Aplicacion web en PHP", "price" : 300, "description" : "Es una aplicacion web realizada en php con mysql", "image" : "images/motox.jpg", "createdAt" : ISODate("2017-08-09T01:23:42.201Z")})
db.project.insert({"name" : "Aplicacion de ecommerce", "price" : 600, "description" : "Aplicacion de Ecommerce para ventas al exterior", "image" : "images/sandisk.jpg", "createdAt" : ISODate("2017-02-11T01:04:28.201Z")})
db.project.insert({"name" : "Formulario en Wordpress", "price" : 100, "description" : "Hacer formulario en Wordpress sencillo", "image" : "images/prestige.jpg", "createdAt" : ISODate("2017-04-20T01:09:25.201Z") })


4) Levante node js con el siguiente comando

npm start

5) En el brower poner localhost:81
