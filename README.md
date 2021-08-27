# javascript-lab21

## Módulo 7: Patrones de Diseño en Javascript
Conocer los principales patrones de diseño aplicables a Javascript en el navegador y en el backend.

### Unidad 4: Patrones de Arquitectura

Selecciona Los Patrones De Diseño Aplicables A Javascript En El Navegador Y En El Backend Con El Propósito De Disminuir La Complejidad.

### Construir una arquitectura MVC con express

Vamos a generar un proyecto completo utilizando la arquitectura MVC.
Para hacer un buen trabajo crearemos un proyecto en Github y sacaremos máximo provecho 

#### Crear un proyecto en Github

Vamos a crear un proyecto en Github en la pestaña "project"
y crearemos un proyecto.
Luego crearemos 3 columnas con nombres `Pendiente`, `Trabajando` y `Terminado`.
El tablero debería quedar como en la siguiente Imagen:

<img src="https://res.cloudinary.com/boolean-spa/image/upload/v1630071335/boolean-fullstack-js/tablero-github_eav6ni.png">

Luego presionaremos en el botón de configuración de cada columna y presionaremos `Manage automation` en cada una. Las configuraciones deben quedar como en las siguientes imagenes:

##### Pendiente
<img src="https://res.cloudinary.com/boolean-spa/image/upload/c_scale,w_256/v1630071161/boolean-fullstack-js/pendiente_ahc4uu.png">

##### Trabajando
<img src="https://res.cloudinary.com/boolean-spa/image/upload/c_scale,w_256/v1630071162/boolean-fullstack-js/trabajando_tevchg.png">


##### Terminado
<img src="https://res.cloudinary.com/boolean-spa/image/upload/c_scale,w_256/v1630071161/boolean-fullstack-js/terminado_ny7lgi.png">

Ya estamos en condiciones de crear nuestra primer "issue".
Vamos a pestaña `Issues` y creamos una nueva con el título `Salida a producción en Heroku`y la siguiente descripción:

```

Se debe salir a producción tempranamente con una página publicada en la URL

  https://lab21-<id_github_student>.herokuapp.com


Utilizar un proyecto de ejemplo y sin contemplar aún la conexión a Base de datos.

Se debe cumplir el siguiente criterio de aceptación
  
  Característica: Aplicación Web en producción 

    Escenario:
      Un usuario accediendo a la aplicación
      
      Dado un usuario en el Navegador Web
      Cuando ingresa a la url de la aplicación
      Entonces la aplicación Web es desplegada correctamente

```

Procura seleccionar el proyecto y las etiquetas adecuadas para el issue.

#### Creación de un proyecto MVC con Express Generator

Para crear un proyecto simplemente ejecutamos el siguiente comando:

`npx express-generator --view hbs`

Más información en este [link](https://expressjs.com/en/starter/generator.html)

Ahora instalamos las dependencias y hacemos una prueba del comando "start"

```
npm install
npm start
```

crear `.gitignore` con el siguiente contenido:

```
  node_modules
```

#### Salida a producción

- Creamos un cuenta en Heroku
- Instalamos la linea de comandos de Heroku `npm i -g heroku`
- Ejecutamos el siguiente comando
```
  heroku login
  heroku git:remote -a lab21-gpincheiraa
```
- Ahora agregamos los cambios a git con nuestro primer commit
- agregaremos en el mensaje `closes #<numero_issue>`

- Salimos a producción con el comando `git push heroku main`
- Una vez corroboramos que todo está OK terminamos esta parte haciendo
`git push origin main`

##### Construcción de una funcionalidad

Todo el equipo del laboratorio se pondrá de acuerdo para resolver 2 issues y montaremos una aplicación que sea capaz de mostrar alguna información utilizando la arquitectura MVC
###### Issue 1: Crear un ambiente de desarrollo

- Crear un nuevo Issue relacionado a configurar el ambiente de desarrollo
- Crear una nueva rama `chore/development-environment`
- Instalar Nodemon y Jest
- Crear un comando `dev` que haga lo mismo que `start` pero con `nodemon`
- Crear un comando `test` que corra el comando `jest --runInBand`
- Instalar `Husky` y configurar el comando `test` como "pre-push"
- Crear una prueba para un controlador llamado `StudentController` que entregue la información de un usuario que entregue datos con un método `getStudent(username)`. 
- Una vez la prueba este fallando creamos un Pull Request. En el mensaje del pull request escribimos 'closes #<numero_issue>'
###### Issue 2: Construir primera pantalla

- Crear un nuevo Issue relacionado a configurar el ambiente de desarrollo
- Crear una nueva rama `feature/student-page`
- Comenzaremos por construir el minimo código posible para pasar la prueba
- Refactorizamos y utilizamos este controlador para dibujar una página con la información del usuario
- Analizaremos como trabajar con HandleBars con este [link](https://handlebarsjs.com/guide/)

- Una vez la prueba este fallando creamos un Pull Request. En el mensaje del pull request escribimos 'closes #<numero_issue>'

###### Issue 3: Crear conexión a una base de datos

- Crear un nuevo Issue relacionado a configurar el ambiente de desarrollo
- Crear una nueva rama `feature/database-info`
- Instalaremos Sequelize
- Vamos a crear un Modelo `Student`
- Adaptamos nuestro controlador para que responda un valor desde Base de datos
- Validamos que nuestra vista muestre la información desde base de datos
- Escribimos una nueva prueba adaptada para el controlador

¡Éxito!

### Otros Patrones de Arquitectura

#### MVVM: Model-View View-Model 

Model–View View-Model (MVVM) is a software architectural pattern that facilitates the separation of the development of the graphical user interface (the view) – be it via a markup language or GUI code – from the development of the business logic or back-end logic (the model) so that the view is not dependent on any specific model platform

**Referencia** https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93viewmodel

Podemos ver parte de su implementación en el framework VueJS
https://012.vuejs.org/guide/#Concepts_Overview
