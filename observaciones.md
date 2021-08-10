# Observaciones

Kari, felicitaciones por tu trabajo. Tu portfolio está muy hermoso, me encanta la abundancia de detalles en el hover, lo lindo que se ve todo, y se nota mucho el esfuerzo por lograr un trabajo con personalidad propia que a la vez cumpla las consignas y el diseño propuesto. 

Como dije en clase, este trabajo no se hace para que constates conocimientos, sino para que aprendas: en ese sentido, mi intencion es que estos comentarios te sirvan para aprender, mejorar tu codigo a futuro e ir apreciando mejor qué se espera de nosotras como desarrolladoras front end.

## Estructura correcta de documento HTML

Tu HTML esta muy bien. Claro, prolijo, muy bien comentado e identado.

Algo que me llama la atención es tu `header`, dado que allí repetís innecesariamente muchísimos links.

```html
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" />
```

Cada uno de esos links hace exactamente lo mismo - traerse el css de google fonts para poder usar los fonts en tu sitio. Quizá estés bajo la impresión de que por cada uno de los fonts de tu web es necesario traerse nuevamente estos css, pero no, no es necesario agregarlo más de una vez. Agregar muchos de estos links innecesarios impacta negativamente en la velocidad de carga de tu web, ya que por cada uno de ellos se hace un llamado a un css externo y se lo carga. Esto para cada uno de los distintos css que te importas. Deberia haber solo uno de cada uno. La excepcion, claro, son las distintas tipografias, que tienen cada una su css. 

Tenés cierta tendencia a tener divs de más. Algunas estructuras de tu web se podrían resolver con menos divs. Dicho esto, yo prefiero que los divs sobren antes de que falten: un div de más se soluciona muy fácil, un div menos puede ser un gran dolor de cabeza cuando estamos recién arrancando. Este sería un comentario que quizá me reservaría para futuros trabajos, pero veo tan bien tu código que me siento confiada en recomendarte que empieces a ver estas cosas desde ya. 

## Respeta la consigna

- El portfolio cuenta con las secciones solicitadas
- Al clickear en los links de navegación, debe llevar a la sección correspondiente

Cumplido. 

- Al clickear en los links de contacto, debe llevar a la página externa correspondiente 

No cumplido. No es necesario que agregues tus propias redes si es algo que preferís no hacer, pero
cualquier link a una web externa hubiera servido para cumplir la consigna.

- El portfolio debe tener un diseño responsivo y verse correctamente en distintos dispositivos 

Cumplido, con la excepcion de un scroll horizontal muy molesto en movil. Quiza ni lo hayas notado, pero eso ocurre cuando hay un elemento que esta rebalsando el ancho del body. En este caso, se trata del div ".centrarwrap", que mide 600px, un tamaño mas grande que el de los celulares. 

- El portfolio debe estar deployado y ser accesible desde una URL 

Cumplido. 

- El repositorio en GitHub debe tener un readme adecuado

Cumplido

### Respeta el diseño dado

Cumplido.

### Buena estructura de proyecto

Cumplido. Cuidado con los archivos que tienen mayúscula en el título, algo que podría traerte problemas en el linkeado.

### Código bien indentado

Tabulas muy bien, lo cual parece un detalle extra cuando una recien comienza pero ayuda un monton a su legibilidad, y que lo hayas logrado en esta etapa es un gran mérito. 

### Comentarios que permiten mejorar la legibilidad del código

Ausentes. Es buena idea comentar cada seccion en HTML y CSS para que quede bien claro donde comienza una cosa y termina otra.

### Uso correcto de etiquetas semánticas

- Me llama la atención que hayas usado `div` para las tarjetas de Mis Conocimientos y Mis Proyectos: yo diría que deberían ser `article`. Pero es el único detalle a comentar aquí (y hay quien podría discutirme que deberían ser divs)

- Usas la etiqueta `section` adentro de `section`, lo que no tiene sentido y puede confundir a un lector de pantalla. 


### Buenos nombres de clases

No usamos mayúsculas en HTML o CSS. Cosas como la clase "CONT" deberian estar siempre en minuscula. Cuando quieras separar palabras, como en "botonformulario", escribilo con guiones: "boton-formulario". 

Cuando decimos que un nombre de clase debe ser descriptivo, lo decimos en un sentido funcional: qué rol cumple este elemento en el código. Los colores de los elementos, su forma, su estilo, su posición, todas esas cosas pueden cambiar y efectivamente cambian todo el tiempo en las webs que hacemos. El botón que hoy es violeta mañana será azul; la sección que estaba primera mañana estará tercera. Por lo tanto esos factores sos no son buenos descriptores, y no deberían ser parte de nuestros nombres de clases.
Otros nombres de clases que usas directamente no tienen sentido. Entiendo que es dificil pensar buenos nombres, y es algo con lo que todos renegamos alguna vez, pero es importante que te vayas acostumbrando a darle más atención a eso. "cards2" no me dice nada. "comillas1", tampoco. "Uno", "Dos", es imposible saber qué son. Son tarjetas de proyectos, son secciones en el form. Clases como "card" y "imagenes" casi que garantizan una confusión, para vos como desarrolladora y para cualquier lector que quiera saber como hiciste tu código. 

### Código CSS bien estructurado

Cumplido a nivel formal. Noto algunos estilos innecesarios o confusos, que te voy indicando en tu archivo de css.

### Reutilización de estilos

Cumplido en general. Hay varios estilos que no necesitas, y te pediria que en algun momento recorras tu CSS viendo todas las cosas que se pueden borrar sin consecuencias. Los divs ya tienen por defecto width de 100%, en la mayoria de los casos eso se puede sacar. No necesitas agregar cosas como flex-direction: row ya que ese es el estilo por defecto de flex. Los menciono como ejemplo pero hay un montooon a lo largo de tu CSS. 

### Cumple con criterios básicos de accesibilidad

- Los colores tienen un contraste adecuado

Cumplido

- Las imágenes tiene el atributo `alt` que corresponde

Incumplido. Tenes solamente dos alt: "fig1" y "fig8". Ponete en la posicion de una persona no vidente a quien el lector de pantalla le lee la descripcion "fig8" de una imagen. Tu web debe ser accesible, y eso incluye tus imagenes: la mujer sentada en un banco que pones en la portada comunica algo a tus usuarios videntes, y debes encontrar la manera de transmitirle esa información a quienes no pueden verla. 

- Los íconos y elementos que no presentan texto agregan la información correspondiente por otros medios (etiquetas aria, texto oculto)

No cumplido, por ejemplo en los links a redes sociales de tu footer. Necesitan un aria.

- Los íconos y elementos que no necesitan ser anunciados por un lector de pantalla tienen la etiqueta aria
  correspondiente

No cumplido. 

- Commits con mensajes adecuados

Cumplido, noto muchos y buenos commits en tu proyecto, lo que siempre se agradece.

- Cuenta con un favicon

No cumplido. 

### Nota: 8
