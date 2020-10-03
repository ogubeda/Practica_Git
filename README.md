# Qué es GIT y la metodología Git Flow

## Sobre GIT

Git es una herramienta para realizar un control de versiones de nuestro código. Es un proyecto de código abierto y con un mantenimiento activo que desarrolló Linux Torvalds.

Git, que presenta una arquitectura distribuida, es un ejemplo de DVCS. En lugar de tener un único espacio para todo el historial de versiones, en Git, la copia del trabajo del código de cada desarrollador es también un repositorio que puede albergar el historial completo de todos los cambios. 

Además de contar con una arquitectura distribuida, Git se ha diseñado teniendo en cuenta el rendimiento, la seguridad y la flexibilidad.

## Sobre Git Flow

Git Flow es un diseño de flujo de Git que fue publicado por primera vez por Vincent Driessen en nvie. El flujo de trabajo de Git Flow define un modelo estricto de ramificación diseñado alrededor de la publicación del proyecto. 

Este flujo de trabajo no añade ningún concepto ni comando nuevo más allá de lo que se necesita. En su lugar, asigna funciones muy específicas a las diferentes ramas y define cómo y cuándo deben interactuar. Además de las ramas de función utiliza ramas individualmente para preparar, mantener y registrar publicaciones. También te aprovechas de todos los beneficios del flujo de trabajo de cada rama función.

Utilizaremos Git Flow, porque tiene lo mejor de los dos mundos. Está centralizado como SVN y también descentralizado, lo que permite que muchos equipos trabajen de forma independiente entre ellos, siempre pasando por el respositorio central. Esto ayuda a no tener el riesgo de mergear o hacer commit sobre un trunk o repositorio que está utilizado por muchas personas.

## Parte práctica

### Primera parte del usuario 1
El usuario 1 partirá creando el repositorio de Git Hub.
![Creacion del repositorio](/images/image41.png)

Y creando los archivos iniciales arcordados.
![Archivos inciciales](/images/image45.png)

Una vez realizado los primeros pasos inicializaremos el directorio con Git con el comando *git init*.
Y una vez lo tengamos inicializado ejecutaremos el comando  *git flow init* para crear toda las ramas necesarias para realzar el proyecto, una vez lo ejecutemos nos saldrá un submenú para dar nombre a las ramas que Git Flow nos crea por defecto.

Subiremos el archivo inicial.
![Subida archivo inicial git add](/images/image32.png)
![Subida archivo inicial git commit](/images/image16.png)
![Subida archivo inicial git push](/images/image42.png)

Con esto la parte del usuario 1 estaría finalizada, pasemos ahora con la parte del usuario2.

### Parte del usuario 2

Ahora como el usuario 2 realizaremos un *git clone* dek repositorio para obtener los archivos.
![Git clone del usuario2](/images/image29.png)

Y inicializaremos el directorio con *git flow*
![Directorio git flow usuario2](/images/image19.png)

Una vez tengamos el directorio, crearemos la nueva feature **contenidoHTML** con el comando *git flow feature start contenidoHTML*
![Feature contenidoHTML](/images/image21.png)

Craremos el archivo **modifyHTML.html** y le añadiremos el contenido necesario.
![Git flow start contenidoHTML](/images/image8.png)

Una vez tengamos la funcionalidad acabada haremos un *git add* con los ficheros modificados.
![git add contenidoHTML](/images/image2.png)

Y haremos un *commit* con los cambios realizados en la funcionalidad.
![git commit contenidoHTML](/images/image1.png)

Una vez realizado el *commit* realizaremos un *git push* para añadir los cambios en remoto.
![git push contenidoHTML](/images/image43.png)

Para finalizar ejecutaremos el comando *git flow feature finish contenidoHTML* para añadir la nueva funcionalidad a la rama **develop**.
![git flow feature finish contenidoHTML](/images/image21.png)

Cuando hayamos finalizado haremos un *git push* para guardar los cambios en remoto.
![git push contenidoHTML](/images/image34.png)

Una vez lo tengamos listo crearemos la segunda feature llamada **atributosHTML** con el comando *git flow feature start atributosHTML*.
![git flow feature start atributosHTML](/images/image31.png)

Y crearemos el archivo **atributosHTML.html**.
![Creación archivo atributosHTML.html](/images/image7.png)

Como hemos hecho anteriormente ejecutaremos el comando *git add* para confirmar los cambios.
![Git add atributosHTML.html](/images/image27.png)

También haremos *commit* de los cambios.
![git commit atributosHTML.html](/images/image15.png)

Y realizaremos un *git push* para subir los cambios en remoto.
![git push atributosHTML](/images/image13.png)

Para finalizar con esta feature también ejecutaremos el comando *git flow feature finish atributosHTML* para añadirla a la rama de **develop**.
![git flow feature finish atributosHTML](/images/image28.png)

Y ejecutaremos el comando *git push* para guardar los cambios en remoto.
![git push origin develop](/images/image46.png)

Ahora procederemos con el usuario3.

### Parte del usuario 3

El usuario 3 es el encargado de realizar la sección de CSS. Para empezar haremos un *git clone* del repositorio.
![git clone del usuario3](/images/image38.png)

Y ejecutaremos el comando *git flow init* para crear todas las ramas necesarias.
![git flow init del usuario3](/images/image4.png)

Luego ejecutaremos el comando *git flow feature start estilosCSS* para crear la rama de la feature.
![git flow feature start estilosCSS](/images/image40.png)

Crearemos el archivo **estilosCSS.html**
![Creación archivo estilosCSS.html](/images/image39.png)

Cuando hayamos finalizado con los cambios los confirmaremos con el comando *git add*.
![git add estilosCSS](/images/image6.png)

Y subiremos los cambios con el comando *git commit*.
![git commit estilosCSS](/images/image36.png)

Para finalizar realizaremos un *git push* para guardar los cambios en remoto.
![git push estilosCSS](/images/image30.png)

Una vez hayamos acabado con la feature ejecutaremos el comando *git flow feature finish estilosCSS* para añadir los cambios a la rama **develop**.
![git push estilosCSS](/images/image33.png)

Y realizaremos un *git push* para guardar los cambios en remoto.
![git push origin estilosCSS](/images/image24.png)

Una vez hemos añadido todas las funcionalidad crearemos una nueva relesa llamada **v1.0**. Para ello ejecutaremos el comando *git flow release start v1.0*.
![git flow release v1.0](/images/image35.png)

Y realizaremos un *git push* para guardar los cambios en remoto.
![git push release v1.0](/images/image3.png)

Una vez tengamos lista la release ejecutaremos el comando *git flow release finish v1.0* para añadir los cambios a la rama master.
![git flow release finish v1.0](/images/image12.png)

Y realizaremos un *git push* para guardar los cambios en remoto.
![git push origin v1.0](/images/image9.png)

Y con esto es trabajo del usuario 3 estaría acabado.