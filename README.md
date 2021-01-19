# Sistema de login / registro con JWT en GraphQL con MongoDB

En este proyecto vamos a aprender como crear un sistema para registro de usuarios haciendo uso de JWT y con ello vamos a conseguir también el inicio de sesión para obtener el token que nos servirá para autenticarnos en GraphQL.

## Requerimientos

* Node v10.16.0 o más.
* NPM v6.0.0 o más
* MongoDB instalado y en marcha.

## Intrucciones de uso

### Instalar las dependencias de NPM
```npm install```

### Crear el fichero de variables de entorno
Creamos el fichero .env dentro del directorio "src"
```
PORT=<numero-puerto>
SECRET=<PALABRA_SECRETA>
DATABASE=mongodb+srv://TomJ92:<tomtom>@ppe-lyarb.gcp.mongodb.net/test?retryWrites=true&w=majority<base-de-datos>
```

### Iniciar en debug
```npm run start:dev```


#### Base de données
2 bases de données sont disponibles:
    - base de données "PPE": base fonctionnelle, c'est la base de production

    - base de données "DEV": base de test de développpement pour effectuer toutes les modifications sans importer la base de données de production

Pour utiliser une base de données il suffit de choisir le nom de la base et d'utiliser le lien associé dans le fichier /src/.env:

    - Pour "PPE": 
        PORT = 4000
        SECRET = PPE
        DATABASE = mongodb://TomJ92:tomtom92@ppe-shard-00-00-lyarb.gcp.mongodb.net:27017,ppe-shard-00-01-lyarb.gcp.mongodb.net:27017,ppe-shard-00-02-lyarb.gcp.mongodb.net:27017/PPE?ssl=true&replicaSet=PPE-shard-0&authSource=admin&retryWrites=true&w=majority
    - Pour "DEV":
        PORT = 4000
        SECRET = DEV
        DATABASE = mongodb://TomJ92:tomtom92@ppe-shard-00-00-lyarb.gcp.mongodb.net:27017,ppe-shard-00-01-lyarb.gcp.mongodb.net:27017,ppe-shard-00-02-lyarb.gcp.mongodb.net:27017/DEV?ssl=true&replicaSet=PPE-shard-0&authSource=admin&retryWrites=true&w=majority

Pour la connexion, les identifiant de connexion actuel sont: (à compléter à chaque création de profil)
    - Côté podologue:
        - (email:"manuel@edu.fr", password:"12345")
        - (email: "jean.papon@gmail.com", password:"password")
        - (email:"podologue@feetback.fr", password:"password")
    - Côté patient:
        - (email:"tom.jouvet@edu.ece.fr", password:"password")
        - (email:"sofia@edu.fr", password:"password")
        - (email:"sbsn", password:"password")
        - (email:"a", password:"password")
        - (email:"test", password:"password")
        - (email:"william.terrien@edu.ece.fr", password:"password")
        - (email:"patient@feetback.fr", password:"password")

### compilation
Pour compiler le projet écrit en TypeScript, il suffit de taper, dans le dossier de travail,la ligne de commande:
tsc

Cela génére les fichiers JavaScript dans le dossier: /build/

### Lancer le serveur
Pour lancer le seveur, il suffit de taper, dans le dossier de travail, la ligne de commande:
node build/server.js

Puis, il faut ouvrir un onglet internet avec le lien:
http://localhost:4000/graphql

Graphql permet de construire les requêtes.

### Lien
Pour créer et utiliser des requêtes:

https://www.youtube.com/watch?v=zatQlSyjW_Q

https://www.youtube.com/watch?v=b8i8hxEQWGg

https://www.youtube.com/watch?v=7I_LcVVyKIk

