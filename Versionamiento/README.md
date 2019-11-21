
# Versionamiento con git

Hola este sería un buen comienzo para todos, lo principal es entender lo que es un sistema de versionamiento, por lo que les invito a leer al respecto antes de empezar.

Si ya estan acostumbrados al versionamiento pueden omitir esta parte sin ningun problema.

## Git y Github

Lo primero que debemos entender es que **Git** y **Github**, no son lo mismo, *git* es la herramienta de versionamiento, mientras que *Github* es la plataforma en la que versionamos, podriamos decir que *git* es la interfaz, y *Github* es el repositorio que hospeda nuestro código.

Nosostros podemos no depender de *Github*, usando una plataforma llamada *Gitlab* sobre todo para aquel código que no queremos que los demas vean, *Github* tiene unos repositorios privados y otros públicos, pero en sus normas esta el que pagues por tus repositorios privados.

*Github* se ha convertido en el mejor CV de un desarrollador, ya que como tiene mucho código público, es ideal para cuando una empresa busca desarrolladores, con habilidades "especificas" github es un lugar donde pueden ellos buscar ese personal, sin mensionar que si en tu CV apuntas tu usuario de *Github* ellos pueden ver tus intereses y habilidades previo a contratarte.

## Basta de charla!!!

Lo primero que vamos a hacer es usar *Github* vamos a hacer es editar este archivo y poner nuestro usuario y ruta.
Este archivo esta hecho en md Syntax por lo que lo vas a hacer de este modo.

```
- [Usuario](ruta_perfil)
```

- [Lli-li](https://github.com/Lli-li)

Cuando hayas colocado tu usuario veras que puedes proponer el cambio y tienes que colocar un comentario para solicitar este cambio.

## Ahora viene lo bueno!!!

Deberas instalar git para hacer la siguiente practica, todo sería tan bonito editando desde el navegador y haciendo solicitudes de cambio al código, pero que pasa cuando tienes que hacer varios cambios, que tienes que probar esos cambios antes de hacer la solicitud del cambio, quizas requieres un VoBo. de QA. o quizas tu oficina impide hacer las solicitudes al desarrollador y la tiene que hacer el QA.

Para esto nos adueñamos del código haciendo un *clone* o un *branch* en este caso clonaremos el código tan funcional que tenemos para hacer un cambio grande a este magnifico proyecto.

```
git clone https://github.com/Lli-li/Pininos-GTI
```

Este comando nos hara una copia del código que esta en *Github*, por lo que ahora podemos hacer uso del código del repositorio para construir algo nuevo.

En este caso como solo es una prueba puedes hacer un archivo **html**, que se llame como tu usuario con un *"hola mundo"*.

Ahora debemos agregar este código a nuestro proyecto, ya que no esta siendo versionado, el archivo no existia cuando clonaste el proyecto, por lo que no lo tiene contemplado el git para versionarlo, antes de hacer un commit debemos agregar los cambios, esto se hace con el comando **add**.

```
git add *
```

En vista que tenemos vastos y largos cambios por hacer le decimos que agregue todos los archivos al repositorio con el comodin favorito **"*"**.
Ahora antes de hacer commit podemos asegurarnos de que los cambios que se van a aplicar sean de los archivos que modificamos con el comando *status*.

```
git status
```

Nos arrojara un resultado similar a este.

```
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   Versionamiento/Lli-li.html
```

Viendo que no nos va a modificar ningún archivo que no hayamos creado o editado podemos hacer *commit*.
Si intentamos hacer un comit git nos va a advertir que no puede hacer commits anonimos, por lo que debemos decirle quien esta haciendo el cambio, si este fuese un repositorio local, no importaria el correo que pongamos en el git, pero como lo tenemos que compartir, usaremos los correos de *Github*.

```
git config --global user.email "you@example.com"
git config --global user.name "Gilberto Lara"
```

Ahora si ya podemos hacer el poderoso commit.

```
git commit -m "Agrego el saludo del Gil Obezo"
```
Antes de hacer cualquier *commit* se recomienda hacer un comentario que de pistas al Gestor de versiones que estabas haciendo un cambio con que prioridad, para que si hay varios trabajando en el mismo proyecto el puede evaluar su impacto y hacer los merges de las ramas en orden de prioridad.

Ahora ya tienes tu código versionado en tu maquina, solo falta subirlo al repositorio, para eso hace falta hacer un **push**.

```
git push [remote] [branch]
```

La sintaxis es primero el remoto y luego la rama, para ver los remotos usamos el comando **remote**. Con su opción *-v* podemos ver a donde apunta el remoto.

```
git remote -v
```

Para ver la rama usamos el comando *branch*.

```
git branch -v
```

