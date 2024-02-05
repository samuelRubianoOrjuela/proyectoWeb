# Estilos CSS proyectoWeb

Este proyecto consta de 6 archivos HTML, cada uno con su respectiva hoja de estilos.

## Estilos genetales del documento 'index.html' 

  - Se importan 2 fuentes, entre ellas, una fuente de iconos

    ```css
    @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,300;1,100&display=swap');
    ```
------

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
------

- Usamos 'text-decoration: none;' para quitar las decoraciones que traen por defecto los links

    ```css
    a {
        text-decoration: none;
    }
    ```
------

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
------
    
- Ocultamos todos los elementos <input> que hay en nuestro documento

    ```css
    input {
        display: none;
    }
    ```
------
## Estilos del encabezdo 'index.html'
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

------

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
- Agregamos una transición que se aplicara para crear una sombra cuando el cursor este sobre cada link 

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
    .nav__link2 {
    width: 129px;
    }
    ```
------
- Centramos el elemento de 'item1' el cual contiene el menu de los catalogos de la pagina web
- Acomodamos los elementos del menu con el catalogo con margenes tanto internas como externas
- Definimos su altura como 0 para ocultar el elemento (este será visible cuando el cursor esté sobre 'nav__link1' ell cual es el link que tiene el texto de catalogo)
- Para ocultar correctamente el objeto, evitamos desbordaciones con 'overflow: hidden;'
- Asignamos al menu del catalogo el mismo color del encabezado
- Enviamos el elemento adelante de otros con 'z-index: 2;'
- agregamos una margen a los elementos encontrados en el menu del catalogo para organizarlos
- Utilizamos la pseudoclase ':hover' para que sea visible el menu del catalogo y para que sus elementos se subrayen cuando el cursor este sobre ellos    
    ```css
    .item1 {
        display: flex;
        justify-content: center;
    }
    .menuCatalogo {
    position: absolute;
    padding: 12px 16px;
    border-radius: 10px;
    height: 0;
    top: 54px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    background-color: #363062;
    transition: 0.2s ease;
    z-index: 2;
    }
    .menuCatalogo a {
        margin: 11px 0;
    }
    .menuCatalogo a:hover {
        text-decoration: underline;
    }
    .menuCatalogo:hover, .nav__link1:hover ~ .menuCatalogo{
        box-shadow: 0 1px 8px 0px black;
        height: 207px;
        top: 67px;
    }
    ```
-------
## Estilos generales de la etiqueta <main> 'index.html'
- Organizamos los elementos en forma de columna y los ubicamos en el centro
    ```css
    main {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    ```
-------
## Estilos de la seccion #1 'index.html'
- Agregamos margenes para ubicar el contenedor
- Le damos un alto y un ancho a nuestro contenedor
- Redondeamos los bordes
- Seleccionamos un color de fondo
- Organizamos los elementos contenidos en esta seccion como una columna y los centramos
- Agregamos una transición para nuestro contenedor
    ```css
    .section1{
        margin: 86px 0 45px;
        width: 653.25px;
        height: 370px;
        border-radius: 20px;
        background-color: #363062;
        display: flex;
        flex-direction: column;
        align-items: center;
        transition: 0.15s ease;
    }
    ```
-------
- Agregamos margenes a nuestro contenedor
- Le damos un alto y un ancho a nuestro contenedor
- Redondeamos los bordes
- Organizamos los elementos contenidos en esta caja centrandolos
    ```css
    .contMainImg {
        margin: 25px 0;
        width: 90%;
        height: 320px;
        background-color: white;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 10px;
        z-index: 1;
    }
    ```
-------
- Este elemento en un link el cual contiene una imagen de fondo
- Le damos un alto y un ancho del 100% a ese elemento para que ocupe la totalidad de su contenedor
- Seleccionamos la imagen que vamos a utilizar
- Acomodamos la imagen de fondo
- Agregamos una transición a este elemento
    ```css
    .contMainImg a {
        width: 100%;
        height: 100%;
        background-image: url(../images/zapatos/stanSmith/stanSmith1.png);
        background-repeat: no-repeat;
        background-size: 90%;
        background-position: center;
        transition: 0.15s ease;
    }
    ```
-------
- Al poner el cursor sobre el container 'section1' la imagen de fondo del elemento anteriormente mencionado aumentara su tamaño un 5%, el container tendra una margen interna para alargar el elemento y la margen exterior se reducira para evidat que los elementos posteriores se desorganicen y por ultimo haremos que el elemento 'info' baje a una distancia de 523 pixeles de la parte superior de la pantalla y haremos que el elemento sea visible
    ```css
    .section1:hover .contMainImg a {
        background-size: 95%;
    }
    .section1:hover{
        padding-bottom: 60px;
        margin-bottom: -15px;
    }
    .section1:hover .info{
        top: 523px;
        visibility: visible;
    }
    ```
-------
- El elemento 'info' contiene el nombre del producto de la imagen contenida en la sección #1 y un boton que nos llevara a la ubicacion de este producto en nuestra pagina web
- Ubicamos el elemento de tal forma que se oculte detras de la imagen de la seccion #1
- Indicamos el ancho y el alto de nuestro elemento
- Organizamos los elementos contenidos en 'info'
- Agregamos una transición y quitamos la visibilidad del elemento
- Quitamos las margenes que tiene el nombre del producto y seleccionamos el tamaño que tendra la fuente
- Agregamos margenes internas a nuestro boton, seleccionamos el tamaño de la fuente y redondeamos los bordes
- Seleccionamos un color de fondo que tendra este elemento
- Al poner el cursor sobre el boton el solor del fondo cambiará a un color más oscuro
    ```css
    .info {
        position: absolute;
        top: 473px;
        margin: 20px 50px;
        width: 546.9px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        visibility: hidden;
        transition: 0.15s ease;
    }
    .nombre{
        margin: 0;
        font-size: 30px;
    }
    .boton  {
        padding: 5px;
        border-radius: 5px;
        font-size: 20px;
        background-color: #71A95A;
        cursor: pointer;
    }
    .boton:hover{
        background-color: #709053;
    }
    ```
-------
## Estilos de la sección #2 'index.html'
- Seleccionamos el ancho que tendra la sección #2
- Agregamos margenes externas al contenedor 
- Organizamos los elementos contenidos centrandolos
    ```css
    .section2 {
        width: 1367.28px;
        margin-top: 61.44px;
        margin-bottom: 92.16px;
        display: flex;
        justify-content: center;
    }
    ```
-------
- Agregamos las margenes que tendran los items de esta sección
- Seleccionamos el alto y el ancho que tendran estos elementos, redondeamos los bordes y ponemos un color de fondo
- Organizamos los elementos contenidos en est contenedor
- Agregamos una transición
    ```css
    .section2__item {
        margin: 0 20px;
        border-radius: 15px;
        width: 276.475px;
        height: 183px;
        background-color: #363062;
        cursor: pointer;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        transition: 0.15s ease;
    }
    ```
-------
- Agregamos ancho y alto a este contenedor
- Organizamos el fondo y agregamos un color blanco 
- Redondeamos los bordes

    ```css
    .miniImg {
        width: 90%;
        height: 85%;
        background-color: white;
        background-repeat: no-repeat;
        background-position: center;
        transition: 0.15s ease;
        border-radius: 5px;
        z-index: 1;
    }
    ```
-------
- Seleccionamos el ancho que se le agregará al elemento
- Posicionamos el elemento
- Agregamos una transición y ocultamos el elemento
    ```css
    .miniBoton {
        width: 112.488px;
        position: absolute;
        top: 787px;
        transition: 0.15s ease;
        visibility: hidden;
    }
    ```
-------
- Agregamos una imagen de fondo y definimos su tamaño
- Al poner el cursor sobre La sección #2 haremos que aumente el tamaño del fondo, agregará una margen interna para aumentar el tamaño del objeto y restaremos margen externa para no desorganizar los elementos posteriores, moveremos el botón Hacia abajo y haremos que el elemento sea visible
    ```css
    .miniImg1 {
        background-image: url(../images/tecnologia/pc/pc1.png);
        background-size: 78%;
    }
    .section2__item:hover .miniImg1 {
        background-size: 83%;
    }
    .section2__item:hover {
        padding-bottom: 40px;
        margin-bottom: -40px;
    }
    .section2__item:hover .miniBoton{
        top: 830px;
        visibility: visible;
    ```
-------
- Agregamos una imagen de fondo al segundo elemento y definimos su tamaño
- Seleccionamos el tamaño que tendrá la imagen cuando el cursor esté sobre el ítem de la sección
- Procedemos a hacer lo mismo con el tercer elemento
    ```css
    .miniImg2 {
        background-image: url(../images/deportes/pelotas/pelotas1.png);
        background-size: 57%;
    }
    .section2__item:hover .miniImg2 {
        background-size: 62%;
    }

    .miniImg3 {
        background-image: url(../images/juguetes/pou/pou1.png);
        background-size: 41%;
    }
    .section2__item:hover .miniImg3 {
        background-size: 46%;
    }
    ```
    -------
## Estilos del pie de página 'index.html'
- Organizamos los elementos que están dentro del contenedor y seleccionamos el tamaño de la fuente
- Seleccionamos el tamaño de la fuente de los títulos del pie de página
- Agregamos altura a los links del pie de página
- Organizamos los links del pie de página de tal forma que haya un espacio entre ellos
- Haremos que al estar el cursor sobre los links estos se subrayen
- Agregamos márgenes a los íconos, seleccionamos tamaño de estos, y les agregamos una transición
- Cuando el cursor esté sobre un ícono este aumentará su tamaño 5 pixeles
    ```css
    footer {
        display: flex;
        justify-content: space-evenly;
        font-size: 14px;
    }
    .footerTitle {
        font-size: 18px;
    }
    .menuLinks{
        height: 50%;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
    }
    .menuLinks a:hover{
        text-decoration: underline;
    }
    .icon {
        margin-right: 5px;
        width: 30px;
        cursor: pointer;
        transition: 0.15s;
    }
    .icon:hover{
        width: 35px;
    }
    ```
-------
## Estilos responsivos del documento index.html
- Cuando El ancho de la pantalla sea menor a 800 pixeles se aplicarán las siguientes reglas de estilo
- Seleccionamos nuevos tamaños para la sección del encabezado Y organizamos los elementos de tal forma que haya espacio entre ellos
- Haremos visibles los elementos 'label' los cual es contienen los iconos anteriormente agregados
- Organizamos la posición de los iconos, agregamos una transición y haremos que al estar el cursor sobre los íconos estos aumenten su tamaño
- Haremos que nuestro menú se esconda en la parte superior de la pantalla y con un input tipo 'checkbox' haremos que este sea visible
- Organizamos los elementos contenidos en el menú, agregamos un color de fondo ,posicionamos el elemento por encima de todos los demás, redondeamos el borde y agregamos una transición
    ```css
    @media screen and (max-width: 800px) {
        .header__section {
            width: 95%;
            justify-content: space-between;
        }
        label {
            display: block;
        }
        #x{
            position: absolute;
            top: 5px;
            right: 5px;
            transition: 0.15s;
        }
        #hamburguer{
            transition: 0.15s;
        }
        #x:hover {
            font-size: 41px;
        }
        #hamburguer:hover{
            font-size: 31px;
        }

        #checkMenu:checked ~ .nav{
            top: 20px;
            right: 20px;
        }
        .logo{
            margin-right: 0;
        }
        .nav {
            position: absolute;
            top: -250px;
            right: 20px;
            height: 250px;
            display: flex;
            justify-content: center;
            align-items: center;
            background: #0F1035;
            z-index: 2;
            border-radius: 10px;
            transition: 0.15s;
        }
        .nav__links{
            height: 60%;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }
        .nav__link:hover{
            background-color: #363062;
        }
        .menuCatalogo{
            left: -112px;
            visibility: hidden;
        }
        .menuCatalogo:hover, .nav__link1:hover ~ .menuCatalogo{
            visibility: visible;
        }
        .section1 {
            margin: 10vw 0 7vw;
            width: 80vw;
            height: 49vw;
        }   
    }
    ```
-------

## Estilos del documento 'tecnologia.html'
Las demás estructuras de los documentos de este proyecto son iguales por lo cual utilizaremos como ejemplo el documento 'tecnologia.html' para explicar los estilos de los demás archivos

-------

## Estilos generales del documento 'tecnologia.html'
- Importamos las fuentes que utilizaremos en el documento, aquí encontraremos la importación de iconos
- Hacemos que la margen del documento sea cero, escogemos como color de letra el color blanco y seleccionaremos la fuente que utilizaremos 
- Quitamos la decoración que se encuentra en los links
- Le damos al cuerpo del documento un ancho del 100% nos aseguramos de quitar todas las márgenes por defecto utilizamos 'overflow-x: hidden;' para que los elementos desbordados se oculten y seleccionamos el color del fondo
- Le damos al contenedor principal de nuestro documento una margen inferior de cien pixeles, organizamos los elementos de tal forma que estén en una columna y nos centramos
- Ocultamos todos los elementos 'input' que se encuentren en nuestro documento
    ```css
    @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,300;1,100&display=swap');
    * {
        margin-left: 0;
        color: white;
        font-family: 'Roboto', sans-serif;
    }
    a {
        text-decoration: none;
    }
    body {
        width: 100%;
        margin: 0;
        overflow-x: hidden;
        background-color: #365486;
    }
    main {
        margin-bottom: 100px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    input {
        display: none;
    }
    ```
    -------
## Estilos de encabezado del documento 'tecnologia.html'
- Agregamos a nuestro encabezado un margen interno, seleccionamos el alto que tendrá nuestro encabezado y organizar los elementos contenidos en el centro y seleccionaremos un color de fondo
- Seleccionamos la margen que utilizaremos en la sección del encabezado y organizaremos su contenido
- Organizaremos el contenido del logo
- Organizamos el menú agregando margenes tanto externas como internas, redondeamos los bordes seleccionamos el tamaño de la fuente y agregamos una transición
    ```css
    header{
        padding: 20px;
        height: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #363062;
    }
    .header__section {
        margin: 0 auto;
        display: flex;
        gap: 15vw;
    }
    .logo {
        display: flex;
    }
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
    .nav {
        display: flex;
        align-items: center;
    }
    .nav a {
        margin: 0 8px;
        padding: 10px;
        border-radius: 10px;
        font-size: 16px;
        transition: 0.1s ease;
    }
    .nav a:hover{
        box-shadow: 0 1px 8px 0px black;
    }
    ```
    -------
## Estilos de la plantilla de secciones
- Organizamos la posición de la sección, agregamos un margen interno y externo, seleccionamos un color de fondo, redondeamos los bordes, agregamos el ancho de la sección y acomodamos los elementos contenidos
- Seleccionamos el tamaño del contenido de la sección, agregamos un color de fondo, organizamos los elementos contenidos de tal forma que haya un espacio entre ellos y redondeamos los bordes
- Seleccionamos el tamaño que tendrán las imágenes, organizamos los elementos del contenedor
- Centramos la imagen contenida con margenes seleccionamos el ancho de la imagen redondeamos los bordes
- Agregamos una margen inferior a la foto contenida redondeamos el borde seleccionamos el color blanco como color de fondo seleccionamos un anxo a la imagen organizamos la posición de la imagen
- Brindamos las medidas que tendrá la imagen principal, seleccionamos el color blanco como el color de fondo, el fondo tendrá un tamaño del 100% con respecto al elemento padre, el fondo no se repetirá acomodamos el fondo de tal forma que quede centrado,redondeamos los bordes y centramos el elemento
- Seleccionamos el color blanco como color del fondo del contenedor de texto, definimos el tamaño del contenedor y redondeamos los bordes
- Aplicamos márgenes al 'h1' de contenedor, seleccionamos el tamaño de la fuente y seleccionamos el color negro como color de la fuente
- 
    ```css
    .section {
        margin-top: 60px;
        padding: 0 40px;
        background-color: #363062;
        border-radius: 10px;
        width: 75%;
        height: 500px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .section__content {
        width: 98%;
        height: 86%;
        background-color: #B9B4C7;
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        border-radius: 8px;
    }
    .imgs{
        width: 44%;
        height: 90%;
        display: flex;
        flex-direction: column;
        flex-wrap:wrap;
        justify-content: center;
        align-items: center;
    }
    .imgs img {
        margin: auto;
        width: 95%;
        border-radius: 8px;
    }
    .foto {
        margin-bottom: 5px;
        border-radius: 8px;
        background-color: white;
        width: 18%;
        min-height: 87px;
        cursor: pointer;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .mainImg {
        width: 76%;
        height: 370px;
        background-color: white;
        background-size: 100%;
        background-repeat: no-repeat;
        background-position: center;
        border-radius: 20px;
        align-self: center;
    }
    .section__text {
        background-color: white;
        width: 46%;
        height: 400px;
        border-radius: 20px;
    }
    .section__text h1 {
        margin: 31px 34px 20px;
        font-size: 40px;
        color: black;
    }
    ```
-------
- Seleccionamos las márgenes de las estrellas agregamos el tamaño de la estrella y organizamos la columna
- Agregamos una margen a la estrella, seleccionamos el tamaño de la estrella y ponemos como fondo la imagen de la estrella tendrá un 100% del tamaño del contenedor
- A continuación el código hará que al estar el cursor sobre la estrella vacia esta cambiará la imagen de fondo por una estrella llena y cuando este elemento Este chequeado en la imagen nueva permanecerá Aquí se busca que al hacer over sobre una estrella todas las estrellas anteriores a esta asimismo cuando el elemento este chequeado
    ```css
    .estrellas {
        margin: 18px;
        width: 39%;
        height: 38px;
        display: flex;
        flex-direction: row-reverse;
        justify-content: flex-end;
    }
    .estrella {
        margin: 0 5px;
        width: 40px;
        height: 100%;
        background-image: url(../../../images/estrellaBorde.png);
        background-size: 100%;
        cursor: pointer;
    }
    #input1:checked ~ .cont1 .label1 .estrella1,
    .cont1:hover .estrella1{
        background-image: url(../../../images/estrella.png);
    }
    #input2:checked ~ .cont2 .label2 .estrella2,
    #input2:checked ~ .cont1 .label1 .estrella1,
    .cont2:hover ~ .cont1 .label1 .estrella1,
    .cont2:hover .estrella2{
        background-image: url(../../../images/estrella.png);
    }
    #input3:checked ~ .cont3 .label3 .estrella3,
    #input3:checked ~ .cont2 .label2 .estrella2,
    #input3:checked ~ .cont1 .label1 .estrella1,
    .cont3:hover ~ .cont2 .label2 .estrella2,
    .cont3:hover ~ .cont1 .label1 .estrella1,
    .cont3:hover .estrella3{
        background-image: url(../../../images/estrella.png);
    }
    #input4:checked ~ .cont4 .label4 .estrella4,
    #input4:checked ~ .cont3 .label3 .estrella3,
    #input4:checked ~ .cont2 .label2 .estrella2,
    #input4:checked ~ .cont1 .label1 .estrella1,
    .cont4:hover ~ .cont3 .label3 .estrella3,
    .cont4:hover ~ .cont2 .label2 .estrella2,
    .cont4:hover ~ .cont1 .label1 .estrella1,
    .cont4:hover .estrella4{
        background-image: url(../../../images/estrella.png);
    }
    #input5:checked ~ .cont5 .label5 .estrella5,
    #input5:checked ~ .cont4 .label4 .estrella4,
    #input5:checked ~ .cont3 .label3 .estrella3,
    #input5:checked ~ .cont2 .label2 .estrella2,
    #input5:checked ~ .cont1 .label1 .estrella1,
    .cont5:hover ~ .cont4 .label4 .estrella4,
    .cont5:hover ~ .cont3 .label3 .estrella3,
    .cont5:hover ~ .cont2 .label2 .estrella2,
    .cont5:hover ~ .cont1 .label1 .estrella1,
    .cont5:hover .estrella5{
        background-image: url(../../../images/estrella.png);
    }
    ```
    -------
- Agregamos márgenes a los elementos que se encuentran debajo de las estrellas y seleccionamos el negro como el color de la fuente
- Seleccionamos el ancho que va a tener el botón, agregamos márgenes tanto externas como internas, redondeamos los bordes seleccionamos un color de fondo
- Cuando el cursor esté sobre el botón el color cambiará por uno más oscuro
    ```css
    .section__text h2 {
        margin: 20px 40px 15px;
        color: black;
    }
    .info {
        margin: 0 30px;
        margin-bottom: 0;
        color: black;
    }

    .buy {
        width: 77px;
        margin: 16px 34px;
        padding: 5px;
        border-radius: 3px;
        background-color: #71A95A;
        cursor: pointer;
    }
    .buy:hover {
        background-color: #709053;
    }
    ```
-------
- Ahora crearemos un elemento que saldrá en la pantalla cuando el botón de comprar sea activado
- El contenedor principal se llamará fondo producto, acomodamos el elemento de tal forma que ocupe toda la pantalla y escogemos un color que opaque los elementos que queden detrás
- Ubicamos el ícono el cual cerrará esta ventana y seleccionamos su tamaño
- Le damos algo contenedor de la imagen alto y ancho redondeamos los bordes y acomodamos el fondo
- Le damos un ancho al contenedor del texto
- Agregamos márgenes al título de esta ventana y le brindamos un tamaño
- Agregamos márgenes tanto externas como internas al botón de compra, redondeamos sus bordes escogemos un color de fondo y lo ubicamos
- Agregamos una margen para el contenido del texto
    ```css
    .fondoProducto{
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.3);
        z-index: 100;
        pointer-events: all;
        transition: 0.1s linear;
        opacity: 0;
        visibility: hidden;
    }
    .producto {
        position: fixed;
        top: 2%;
        right: 30%;
        width: 40%;
        height: 700px;
        background-color: #363062;
        border-radius: 10px;
        display: flex;
        flex-direction: column;
        align-items: center;
        z-index: 100;
    }

    .bx{
        position: absolute;
        font-size: 40px;
        top: 1.5%;
        right: 2%;
        cursor: pointer;
    }
    .content__imagen {
        margin-top: 60px;
        width: 83%;
        height: 47%;
        border-radius: 10px;
        background-size: 62%;
        background-repeat: no-repeat;
        background-color: white;
        background-position: center;
    }
    .content__texto{
        width: 83%;
    }
    .content__texto h1{
        margin: 15px;
        margin-bottom: 10px;
        font-size: 40px;
        color: white;
    }
    .content__texto h2 {
        margin: 15px 15px;
        color: white;
    }
    .buy_ {
        position: absolute;
        margin: 16px 34px;
        padding: 5px;
        width: 115px;
        font-size: 24px;
        top: 407px;
        right: 60px;
        border-radius: 3px;
        background-color: #71A95A;
        cursor: pointer;
    }
    .content__texto p {
        margin: 6px 12px;
    }
    ```
-------
- De nuevo organizamos las estrellas para que estas también se apliquen en nuestra nueva ventana
    ```css
    .estrellas_ {
        margin: 0;
        width: 39%;
        height: 38px;
        display: flex;
        flex-direction: row-reverse;
        justify-content: flex-end;
    }
    .estrella_ {
        margin: 0 5px;
        width: 40px;
        height: 100%;
        background-image: url(../../../images/estrellaBorde.png);
        background-size: 100%;
        cursor: pointer;
    }
    #input_1:checked ~ .cont1 .label_1 .estrella_1,
    .cont1:hover .estrella_1{
        background-image: url(../../../images/estrella.png);
    }
    #input_2:checked ~ .cont2 .label_2 .estrella_2,
    #input_2:checked ~ .cont1 .label_1 .estrella_1,
    .cont2:hover ~ .cont1 .label_1 .estrella_1,
    .cont2:hover .estrella_2{
        background-image: url(../../../images/estrella.png);
    }
    #input_3:checked ~ .cont3 .label_3 .estrella_3,
    #input_3:checked ~ .cont2 .label_2 .estrella_2,
    #input_3:checked ~ .cont1 .label_1 .estrella_1,
    .cont3:hover ~ .cont2 .label_2 .estrella_2,
    .cont3:hover ~ .cont1 .label_1 .estrella_1,
    .cont3:hover .estrella_3{
        background-image: url(../../../images/estrella.png);
    }
    #input_4:checked ~ .cont4 .label_4 .estrella_4,
    #input_4:checked ~ .cont3 .label_3 .estrella_3,
    #input_4:checked ~ .cont2 .label_2 .estrella_2,
    #input_4:checked ~ .cont1 .label_1 .estrella_1,
    .cont4:hover ~ .cont3 .label_3 .estrella_3,
    .cont4:hover ~ .cont2 .label_2 .estrella_2,
    .cont4:hover ~ .cont1 .label_1 .estrella_1,
    .cont4:hover .estrella_4{
        background-image: url(../../../images/estrella.png);
    }
    #input_5:checked ~ .cont5 .label_5 .estrella_5,
    #input_5:checked ~ .cont4 .label_4 .estrella_4,
    #input_5:checked ~ .cont3 .label_3 .estrella_3,
    #input_5:checked ~ .cont2 .label_2 .estrella_2,
    #input_5:checked ~ .cont1 .label_1 .estrella_1,
    .cont5:hover ~ .cont4 .label_4 .estrella_4,
    .cont5:hover ~ .cont3 .label_3 .estrella_3,
    .cont5:hover ~ .cont2 .label_2 .estrella_2,
    .cont5:hover ~ .cont1 .label_1 .estrella_1,
    .cont5:hover .estrella_5{
        background-image: url(../../../images/estrella.png);
    }
    ```
-------
## Estilo de seccion específica
- Ahora agregaremos los estilos específicos de cada sección
- Escogemos las fotos las cual es aparecerán como fondo de la imagen principal cuando el cursor esté sobre ellas
- Escogeremos la imagen principal de cada sección y le brindaremos un tamaño específico
- Especificaremos cuál será el botón que activará la nueva ventana de dicha sección
- Agregamos la imagen que tendrá de fondo la nueva ventana
- Organizamos la posición del botón de la nueva ventana
    ```css
    .foto1_2:hover ~ .mainImg1{
        background-image: url(../../../images/tecnologia/pc/pc2.png);

    }
    .foto1_3:hover ~ .mainImg1{
        background-image: url(../../../images/tecnologia/pc/pc3.png);
    }

    .mainImg1 {
        background-image: url(../../../images/tecnologia/pc/pc1.png);
        background-size: 95%;
    }
    #check__buy1:checked ~ .fondo1{
        opacity: 1;
        visibility: visible;
    }
    .content__imagen1{
        background-image: url(../../../images/tecnologia/pc/pc1.png);
    }
    .buy_1 {
        position: absolute;
        top: 460px;
        right: 90px;
    }
    ```
-------
Estos últimos fueron los estilos que se le deberán aplicar a cada una de las secciones especificando la imagen que se utilizará y especificando los tamaños. Todas las secciones incluyendo las de las otras categorías son basadas en esta plantilla, solo se cambiarán estilos específicos.