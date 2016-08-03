## **<center>Aprendiendo a usar GIT**


#### *<center>Antes de incursionar en el mundo del GIT, debes crear una cuenta en algun servidor de GIT, te recomiendo [GITHUB](https://github.com).*

Una vez creada la cuenta en github, deben hacer clic en *create new*  (o "+" que se puede observar en la parte superior derecha) y darle a la opcion *new repository* para crear el nuevo repositorio.

![](Images/img1.png)

En la siguiente ventana se deben rellenar los datos.

![](Images/img2.png)

Los repositorios siempre deben ser **Public**, inicializar con un archivo **README** y el tipo de licencia que se usara es la **MIT**. Y luego hacer clic en **Create repository**.

![](Images/img3.png)

Luego de haber creado el repositorio, el sistema nos mostrara el nuevo repositorio, para trabajar con nuestro sistema de manera remota es necesario clonar el repositorio a nuestro entorno local, para ello debemos copiar la URL en **Clone o download** haciendo clic en la opcion **copy to clipboard**.

![](Images/img4.png)

Abrimos nuestro terminal y nos preparamos para clonar nuestro repositorio (no olvides desplazarte a la carpeta donde quieres que este).

    git clone (URL copiada)
![](Images/img5.png)

Se mostrara la descripcion de los objetos creados.

![](Images/img6.png)

Ejecutamos

    ls
![](Images/img7.png)

y nos mostrara los archivos README y LICENSE.

![](Images/img8.png)

Hacemos.

    git branch
y nos mostrara las ramas de nuestro repositorio (en este punto deberia estar solo **Master**), es por ello que debemos crear otra rama (la rama develop).

    git branch develop

![](Images/img9.png)

Hacemos.

    ls
y confirmamos que este la rama develop creada.

![](Images/img10.png)

Nos movemos a la rama develop.

    git checkout develop
![](Images/img11.png)

Hacemos.

    git branch

Para confirmar

![](Images/img12.png)

La rama sobre la cual vamos a trabajar es develop (nunca debemos tocar la rama **Master**).
Creamos una nueva rama.

    git branch add-prueba
![](Images/img13.png)

Confirmamos que haya sido creada.

    git branch

![](Images/img14.png)

Nos vamos a la nueva rama creada.

    git checkout add-prueba
![](Images/img15.png)

Confirmamos que nos cambiamos de rama.

    git branch
![](Images/img16.png)

Listamos los archivos.

    ls
![](Images/img17.png)

Abrimos el editor de texto (en nuestro caso **ATOM**)

    atom .
![](Images/img18.png)

y nos mostrara el README de nuestro repositorio

![](Images/img19.png)

Hacemos los cambios pertinentes al archivo, guardamos y cerramos.

![](Images/img20.png)

Revisamos el estatus de nuestro repositorio.

    git status
![](Images/img21.png)

y a;adimos el README.

    git add README.md
![](Images/img22.png)

hacemos commit para revisar los cambios.

     git commit README.md
![imagen 1][1] ![imagen 2][2]

[1]: Images/img23.png
[2]: Images/img24.png

Ejecutamos.

    git commit -m "modificacion de README"
Indicara los cambios que se han agregado en el documento.
![](Images/img25.png)

Agregamos nuestro nombre de usuario en github y contrase;a.

![](Images/img26.png)

Abrimos el navegador y nos dirijimos a github.

Damos click en la opcion que dice Compare y pull

![](Images/img27.png)

Abrira una ventana que dice **Open a pull request** comparamos los cambios en la parte inferior de la pantalla.

Debemos colocar en la base **develop** y en compare **add-prueba**.  Hacer clic en **Create pull request**

![](Images/img28.png)

En la ventana siguiente hacemos clic en **Merge pull request** (siempre y cuando la base sea **develop** y compare con **add-prueba**)

![](Images/img29.png)

Hacemos clic en **Confirm merge**

![](Images/img30.png)

Borramos la rama add-prueba en **Delete branch**

![](Images/img31.png)

Y listo, ya se hicieron los cambios en el servidor.

![](Images/img32.png)

Volvemos al terminal y nos dirigimos a la rama develop, para sincronizar lo que tenemos en el servidor con nuestro equipo.

    git checkout develop

    git pull origin develop

![](Images/img33.png)

corroboramos que estamos en la rama develop

    git branch develop
![](Images/img34.png)

Borramos la rama add-prueba.

    git branch -D add-prueba

![](Images/img35.png)

Revisamos que se haya borrado la rama.

    git branch

![](Images/img36.png)

Y listo!! bienvenido al mundo de GIT.
