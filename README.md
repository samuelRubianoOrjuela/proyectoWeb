# Estilos CSS proyectoWeb

Este proyecto consta de 6 archivos HTML, cada uno con su respectiva hoja de estilos.

## index.html 

- Se importan 2 fuentes, entre ellas, una fuente de iconos

    ```css
    @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,300;1,100&display=swap');
    ```

- Quitamos la margen por defecto que tiene el HTML 
- Seleccionamos el color blanco como el color que tendrá la fuente
- Seleccionamos el tipo de fuente que tendra la pagina web

    ```css
    * {
        margin-left: 0;
        color: white;
        font-family: 'Roboto', sans-serif;
    }
    ```

- Usamos 'text-decoration: none;' para quitar las decoraciones que traen por defecto los links

    ```css
    a {
        text-decoration: none;
    }
    ```

- Le damos al cuerpo de la pagina un ancho del 100%

- Quitamos la margen que este elemento trae por defecto

- Utilizamos 'overflow-x: hidden;' para ocultar los desbordamientos en el eje x

- Seleccionamos un color de fondo para nuestra pagina web

    ```css
    body {
        width: 100%;
        margin: 0;
        overflow-x: hidden;
        background-color: #365486;
    }
    ```
    
- Ocultamos todos los elementos <input> que hay en nuestro documento

    ```css
    input {
        display: none;
    }
    ```

- Agregamos 'padding' para añadir un margen interno a nuestro encabezado

- Seleccionamos la altura que utilizaremos

- Utilixamos 'flex' para organizar los elementos contenidos

- Con 'justify-content: center;' y 'align-items: center;' centramos tanto en el eje y como en el eje x nuestros elementos

- Escogemos un color para el encabezado
  
    ```css
    header{
        padding: 20px;
        height: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #363062;
    }
    ```
    
- Centramos los elementos contenidos en el container ´header__section´

    ```css
    .header__section {
        display: flex;
        justify-content: center;
        align-items: center;
    }
    ```

    ------


- Ubicamos el container 'logo'

- Para que este elemento se convierta en una fila utilizaremos los valores por defecto de display: flex;'

    ```css
    .logo {
        margin-right: 25vw;
        display: flex;
    }
    ```

    ------

- Aplicamos margenes a los textos del logo
- Seleccionaos el tamaño de la fuente
- Especificamos el tipo de fuente que queremos utilizar en cada uno de los textos

    ```css
    .p1 {
        margin: 10px 0 10px 20px;
        font-size: 25px;
        font-family: 'Press Start 2P', system-ui;
    }
    .p2{
        margin: 10px 0;
        font-size: 25px;
        font-family: 'Roboto', sans-serif;
    }
    ```

    ------
- Centramos los elementos en el eje y con 'align: items;'

    ```css
    .nav {
        display: flex;
        align-items: center;
    }
    ```

    ------
- Utilizamos 'cursor: pointer;' para los iconos
- Ocultamos los elementos contenidos en los 'label', ya que estos se utilizaran cuando la pagina sea responsiva
- Seleccionamos los tamaños que utilizaremos para nuestros iconos

    ```css
    i {
        cursor: pointer;
    }
    label {
        display: none;
    }
    #hamburguer{
        font-size: 30px;
        height: 30px;
    }
    #x {
        font-size: 40px;
        height: 30px;
    }
    ```

    ------
- Seleccionamos tamaños para nuestros containers y los organizamos con 'flex'
- Utilizamos margenes tanto externas como internas para organizar nuestros elementos
- Redondeamos los bordes y seleccionsmos el tamaño de la fuente
- Agregamos una trancision que se aplicara para crear una sombra cuando el cursor este sobre cada link 

    ```css
    .nav__links {
        height: 100%;
        display: flex;
        align-items: center;
    }
    .nav__link {
        margin: 0 8px;
        padding: 10px;
        border-radius: 10px;
        font-size: 16px;
        transition: 0.1s ease;
        cursor: pointer;
    }
    .nav__link:hover{
        box-shadow: 0 1px 8px 0px black;
    }
    ```

    ------