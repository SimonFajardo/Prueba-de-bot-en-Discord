# Prueba-de-bot-en-Discord

1- Iniciar sesión en Discord (en caso de no tener una cuenta registrarse).

2- Creamos un servidor en el botón "Añadir un servidor".

3- Seleccionamos el tipo de servidor dependiendo de la opción que más se ajuste a lo que queremos y realizamos su configuración, escogiendo el nombre que deseamos y cargando una foto (opcional). Podemos agregar canales al servidor dependiendo de los tópicos que queremos tratar en él (opcional).

4- Ingresamos al portal web para desarrolladores de Discord (Discord Developer).

5- Seleccionamos el botón "Applications".

6- Creamos una nueva aplicación en el botón "New Applications", escogiendo su nombre respectivo. Podemos subir una foto para el bot, escribir una descripción y tags para describir el contenido y funcionalidad del bot (opcional).

7- Seleccionamos la pestaña bot y damos click al botón "Add Bot". Escribimos el mensaje que queremos que se muestre cuando el bot aparezca en el servidor (opcional).

8- Seleccionar el bot como público.

9- Activamos las opciones "PRESENCE INTENT", "SERVER MEMBERS INTENT" y "MESSAGE CONTENT INTENT" y guardamos los cambios.

10- Seleccionamos la pestaña "OAuth2" y posteriormente "URL Generator".

11- Seleccionamos en "SCOPES": "application.commands" y "bot".

12- Seleccionamos en "BOT PERMISSIONS": "Administrator". 

13- Copiamos el campo URL y pegamos la dirección en una pestaña nueva del navegador. Al cargar la página en la nueva pestaña, seleccionamos el servidor al cual vamos a añadir el bot y confirmamos que le queremos dar permisos como administrador.

14- Abrimos la terminal de Visual Studio Code y ejecutamos estando posicionado dentro de la carpeta del bot (ejemplo: botdiscord) el comando "npm init --yes", al haber previamente instalado en la computadora el entorno Node.js. Una vez ejecutado este comando se genera en la carpeta el archivo package.json. Nota explicativa: todos los comandos en la terminal de Visual Studio Code van sin las comillas.

15- Escribimos en dicha terminal el comando "npm i discord.js axios dotenv" para instalar estas dependencias. Discord.js es un potente módulo Node.js que permite interactuar con la API de Discord muy fácilmente. Toma un enfoque mucho más orientado a objetos que la mayoría de las otras bibliotecas de JS Discord, lo que hace que el código del bot sea significativamente más ordenado y fácil de comprender. Axios es una librería Javascript capaz de ejecutarse tanto en el navegador como en NodeJS, que facilita todo tipo de operaciones como cliente HTTP. Con Axios se puede realizar solicitudes a un servidor, completamente configurables, y recibir la respuesta de una manera sencilla de procesar. Dotenv es una dependencia que permite utilizar las variables de entorno.

16- Creamos un archivo index.js con las líneas de código especificadas en él. Lo enlazamos con la variable de entorno DISCORD_BOT_ID.

17- Creamos un archivo .env que va a contener la variable de entorno DISCORD_BOT_ID que va a estar igualada al token del bot que creamos, el cual se encuentra en el portal web de discord developer en la pestaña "Bot". Lo que haremos será copiar el token del bot creado y pegarlo después del igual en el archivo .env.

18- En la terminal de Visual Studio Code escribimos "node index.js" para ejecutar bajo el entorno Node.js este archivo Javascript. Una vez que se ejecute y el bot se conecte al servidor de Discord aparecerá el mensaje en la terminal "Bot is ready".

19- El bot está configurado para responder a palabras en específico. Si escribimos en el servidor de Discord donde está el bot en cualquiera de los canales de texto la palabra "ping" responderá con la palabra "pong", o si escribimos en inglés la palabra "quote" nos responderá con una frase aleatoria de la página "https://api.quotable.io/random".
