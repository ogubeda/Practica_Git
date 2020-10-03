Git es una herramienta para realizar un control de versiones de nuestro código. Es un proyecto de código abierto y con un mantenimiento activo que desarrolló Linux Torvalds.

Git, que presenta una arquitectura distribuida, es un ejemplo de DVCS. En lugar de tener un único espacio para todo el historial de versiones, en Git, la copia del trabajo del código de cada desarrollador es también un repositorio que puede albergar el historial completo de todos los cambios. 

Además de contar con una arquitectura distribuida, Git se ha diseñado teniendo en cuenta el rendimiento, la seguridad y la flexibilidad.

Git Flow

Git Flow es un diseño de flujo de Git que fue publicado por primera vez por Vincent Driessen en nvie. El flujo de trabajo de Git Flow define un modelo estricto de ramificación diseñado alrededor de la publicación del proyecto. 

Este flujo de trabajo no añade ningún concepto ni comando nuevo más allá de lo que se necesita. En su lugar, asigna funciones muy específicas a las diferentes ramas y define cómo y cuándo deben interactuar. Además de las ramas de función utiliza ramas individualmente para preparar, mantener y registrar publicaciones. También te aprovechas de todos los beneficios del flujo de trabajo de cada rama función.

Utilizaremos Git Flow, porque tiene lo mejor de los dos mundos. Está centralizado como SVN y también descentralizado, lo que permite que muchos equipos trabajen de forma independiente entre ellos, siempre pasando por el respositorio central. Esto ayuda a no tener el riesgo de mergear o hacer commit sobre un trunk o repositorio que está utilizado por muchas personas.