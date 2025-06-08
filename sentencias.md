<!-- 1- Entrar en mogo -->
mongosh

<!-- 2- Crear la BBDD -->
use market

<!-- 2.1 - Ver bbdd -->
show dbs

<!-- 3- Crear la tabla users -->
db.createCollection('users')

<!-- 4- Crear la tabla posts -->
db.createCollection('posts')

<!-- 5- Insertar el primer dato en la tabla posts -->
db.posts.insertOne({
  Title: "Mi primer post",
  TextPost: "Este es el contenido del post.",
  Username: "juan123",
  Comments: [
    {
      Username: "ana456",
      TextComment: "Buen post!"
    },
    {
      Username: "carlos789",
      TextComment: "Gracias por compartir."
    }
  ]
});

<!-- 6- Insertar 15 datos en la tabla posts -->
db.posts.insertMany([
  {
    Title: "Cómo aprendí a programar",
    TextPost: "Empecé con Python y luego seguí con JavaScript. ¡No te rindas!",
    Username: "coderJuan",
    Comments: [
      { Username: "laura_dev", TextComment: "¡Muy inspirador!" }
    ],
    date: new Date()
  },
  {
    Title: "Café favorito",
    TextPost: "Probé un café colombiano que me encantó.",
    Username: "sofiBarista",
    Comments: [
      { Username: "mateoCafe", TextComment: "¿Dónde lo conseguiste?" }
    ],
    date: new Date()
  },
  {
    Title: "Mi primer dibujo digital",
    TextPost: "Usé una tableta gráfica y fue una gran experiencia.",
    Username: "artLeo",
    Comments: [],
    date: new Date()
  },
  {
    Title: "Tips para rendir mejor en los exámenes",
    TextPost: "Dormir bien y estudiar con tiempo es clave.",
    Username: "estudianteTop",
    Comments: [
      { Username: "profesorCarlos", TextComment: "¡Exactamente!" }
    ],
    date: new Date()
  },
  {
    Title: "Reparé mi computadora",
    TextPost: "Cambié el disco duro y ahora funciona perfecto.",
    Username: "tecnicoMiguel",
    Comments: [
      { Username: "pcHelp", TextComment: "Gracias por compartir." }
    ],
    date: new Date()
  },
  {
    Title: "Revisión de iPhone 15",
    TextPost: "Es muy rápido, pero la batería no mejora mucho.",
    Username: "techLaura",
    Comments: [
      { Username: "appleFan", TextComment: "Buen análisis." }
    ],
    date: new Date()
  },
  {
    Title: "Empezando en el gimnasio",
    TextPost: "Hoy fue mi primer día, ¡me siento motivado!",
    Username: "fitMarcos",
    Comments: [
      { Username: "anaFit", TextComment: "¡Ánimo! 💪" }
    ],
    date: new Date()
  },
  {
    Title: "Películas recomendadas",
    TextPost: "¿Qué película no me puedo perder este mes?",
    Username: "movieLover",
    Comments: [
      { Username: "cineFan", TextComment: "Mira Dune 2." }
    ],
    date: new Date()
  },
  {
    Title: "Cocina vegana fácil",
    TextPost: "Aquí tienes 3 recetas deliciosas y rápidas.",
    Username: "veggieSofia",
    Comments: [],
    date: new Date()
  },
  {
    Title: "Decoración de interiores con poco presupuesto",
    TextPost: "Usé plantas y luces LED. ¡Cambió todo el ambiente!",
    Username: "diseñoCasa",
    Comments: [
      { Username: "estiloEco", TextComment: "Me encanta la idea de las plantas." }
    ],
    date: new Date()
  },
  {
    Title: "¿Alguien juega ajedrez?",
    TextPost: "Busco oponentes para practicar.",
    Username: "ajedrecista22",
    Comments: [
      { Username: "mateEn3", TextComment: "Cuenta conmigo." }
    ],
    date: new Date()
  },
  {
    Title: "Error 404 en mi web",
    TextPost: "¿Por qué recibo error 404 si el archivo está en el servidor?",
    Username: "webLuis",
    Comments: [
      { Username: "devHelena", TextComment: "Revisa el path o el archivo .htaccess." }
    ],
    date: new Date()
  },
  {
    Title: "Aprender inglés desde casa",
    TextPost: "Recomiendo usar apps y ver series con subtítulos.",
    Username: "idiomasAna",
    Comments: [],
    date: new Date()
  },
  {
    Title: "¿Vale la pena una impresora 3D?",
    TextPost: "Estoy pensando en comprar una, ¿qué opinan?",
    Username: "makerMario",
    Comments: [
      { Username: "printFan", TextComment: "¡Sí! Pero el mantenimiento es clave." }
    ],
    date: new Date()
  },
  {
    Title: "Rutina de meditación diaria",
    TextPost: "Solo 10 minutos al día cambian mucho tu energía.",
    Username: "zenLuna",
    Comments: [
      { Username: "menteClara", TextComment: "Gracias por recordármelo." }
    ],
    date: new Date()
  }
]);


<!-- 7- Ver tabla posts con los insert hechos -->
db.posts.find()

<!-- 8- Insertar el primer registro de user -->
db.users.insertOne({
  UserName: "leire123",
  Email: "leire@g.com.",
  Age: "23",
});

<!-- 9- Insetar 10 datos en users -->
db.users.insertOne({
  UserName: "leire123",
  Email: "leire@g.com",
  Age: 23
});

db.users.insertOne({
  UserName: "mario_dev",
  Email: "mario.dev@outlook.com",
  Age: 30
});

db.users.insertOne({
  UserName: "ana89",
  Email: "ana89@gmail.com",
  Age: 27
});

db.users.insertOne({
  UserName: "daniCoder",
  Email: "dani@protonmail.com",
  Age: 35
});

db.users.insertOne({
  UserName: "luisa_t",
  Email: "luisa.t@hotmail.com",
  Age: 21
});

db.users.insertOne({
  UserName: "pabloGamer",
  Email: "pablo.gamer@gmail.com",
  Age: 19
});

db.users.insertOne({
  UserName: "noeliaFit",
  Email: "noelia.fit@live.com",
  Age: 26
});

db.users.insertOne({
  UserName: "jorgePhoto",
  Email: "jorge.photo@yahoo.com",
  Age: 32
});

db.users.insertOne({
  UserName: "martinaReads",
  Email: "martina.reads@gmail.com",
  Age: 24
});

db.users.insertOne({
  UserName: "cristianJS",
  Email: "cristian@js.dev",
  Age: 29
});

<!--------------- Actualizar publicaciones:----------->
<!-- 10 - Actualiza todos los campos de una publicación -->
db.posts.updateOne(
  { _id: ObjectId("6844033fc0222f482c50eb7a") }, // Reemplaza con el ID real
  {
    $set: {
      Title: "Update post",
      TextPost: "Este es el contenido del update.",
      Username: "1juan123",
      Comments: [
        { Username: "1ana456", TextComment: "1 Buen post!" },
        { Username: "carlos789", TextComment: "Gracias por compartir." }
      ]
    }
  }
);

<!-- 11- Mirar el cambio de posts -->
db.posts.find({ Title: "Update post" })

<!-- 12- Cambiar el body de una publicación. -->
db.posts.updateOne(
  { Title: "Mi primer día en la universidad" }, // Filtro
  { $set: { TextPost: "Estoy pensando en comprar una, ¿qué opinan?" } }
  // Nuevo contenido
);

<!-- 13- Mirar el cambio de posts -->
db.posts.find({ TextPost: "Estoy pensando en comprar una, ¿qué opinan?" })


<!-------------- Actualizar comentarios: ------------->
<!------ 14 -Actualiza el comentario de una publicación ------>
db.posts.updateOne(
  { _id: ObjectId("6844033fc0222f482c50eb7a") }, // Reemplaza con el ID real
  {
    $set: {
      Comments: [
        { Username: "1ana456", TextComment: "1 Buen post!" },
      ]
    }
  }
);

<!--------------- Actualizar usuarios:----------->
<!-- 15 - Actualiza todos los campos de un usuario -->
db.users.updateOne(
  { UserName: "leire123" },
  {
    $set: {
      UserName: "leire_updated",
      Email: "nuevoemail@g.com",
      Age: 28
    }
  }
);

<!-- 16 - Cambiar el email de dos usuarios es decir hacer la query dos veces. -->
db.users.updateOne(
  { UserName: "ana89" },
  { $set: { Email: "ana89_new@gmail.com" } }
);

db.users.updateOne(
  { UserName: "mario_dev" },
  { $set: { Email: "mario.new@outlook.com" } }
);

<!-- 17 - Aumenta en 5 años la edad de un usuario -->
db.users.updateOne(
  { UserName: "daniCoder" },
  { $inc: { Age: 5 } }
);

<!--------------- Actualizar usuarios:----------->
<!-- 1.2.3 OBTENER DATOS -->
<!-- 18 - Seleccionar todas las publicaciones -->
db.posts.find();

<!-- 19 - Selecciona las publicaciones que coincidan con el username indicado -->
db.posts.find({ Username: "1juan123" });

<!-- 20 - Selecciona todos los usuarios con una edad mayor a 20 -->
db.users.find({ Age: { $gt: 20 } });

<!-- 21 - Selecciona todos los usuarios con una edad inferior a 23 -->
db.users.find({ Age: { $lt: 23 } });

<!-- 22 - Selecciona todos los usuarios que tengan una edad entre 25 y 30 años -->
db.users.find({ Age: { $gte: 25, $lte: 30 } });

<!-- 23 - Muestra los usuarios de edad menor a mayor y viceversa -->
db.users.find().sort({ Age: 1 });
db.users.find().sort({ Age: -1 });

<!-- 24 - Selecciona el número total de usuarios -->
db.users.countDocuments();

<!-- 25 - Selecciona todas las publicaciones y haz que se muestren con la siguiente estructura: Título de la publicación: "title one" -->
db.users.countDocuments();
db.posts.find().forEach(post => print("Título de la publicación: \"" + post.Title + "\""));

<!-- 26 - Selecciona solo 2 usuarios -->
db.users.find().limit(2);

<!-- 27 - Busca por title 2 publicaciones -->
db.posts.find({ Title: /2/i });

<!-- 1.2.4 BORRAR DATOS -->
<!-- 28 - Elimina a todos los usuarios con una edad mayor a 30 -->
db.users.deleteMany({ Age: { $gt: 30 } });

<!-- 1.2.5 SELECCIONAR Y FILTRAR -->
<!-- 29 - Selecciona el número total de publicaciones que tienen más de un comentario -->
db.posts.countDocuments({ "Comments.1": { $exists: true } });

<!-- 30 - Selecciona la última publicación creada -->
db.posts.find().sort({ date: -1 }).limit(1);

<!-- 31 - Selecciona 5 publicaciones y que sean las últimas creadas -->
db.posts.find().sort({ date: -1 }).limit(5);

<!-- 32 - Elimina todas las publicaciones que tengan más de un comentario -->
db.posts.deleteMany({ "Comments.1": { $exists: true } });
