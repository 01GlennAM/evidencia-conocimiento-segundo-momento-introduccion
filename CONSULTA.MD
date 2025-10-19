# Cuestionario: Frameworks de CSS y Metodología BEM

*A continuación, responde cada una de las siguientes preguntas. Recuerda hacer un commit por cada pregunta principal que completes.*

### Pregunta 1: Fundamentos de los Frameworks de CSS

* **1.1.** ¿Qué es un **Framework de CSS**? Explícalo con una analogía del mundo real que no sea de programación (por ejemplo, un kit de bloques de construcción, una plantilla para dibujar, etc.) para facilitar su comprensión.
* **1.2.** ¿Qué problemas principales vienen a solucionar los frameworks de CSS en el desarrollo web? Menciona y explica al menos dos ventajas clave de utilizarlos.

**[ESPACIO PARA TU RESPUESTA 1]**
los framework de css son como un caja de erramientas que facilita y agiliza nuestro trabajo en el desarrollo web, ahorrando grandes cantidades de tiempo. para mi in framework en el mundo real mas espesificamente en la construcción seria una retro escabadora la cual agiliza la creación de brechas y huecos que de otra forma al hacerlo de forma manual con un pala seria tedioso y llevaria mucho tiempo.

los problemas que viene a resolver seria mas que todo de tiempo, productividad y diseños mas simetricos
---

### Pregunta 2: Bootstrap CSS - El Ecosistema Basado en Componentes

* **2.1.** Describe la filosofía principal de **Bootstrap**, centrada en **componentes pre-diseñados** (component-based).
* **2.2.** Investiga en la documentación de Bootstrap y crea una lista con **10 clases** fundamentales. Incluye el nombre de la clase y una breve definición de lo que hace. (Ej: `.container` - Centra y ajusta el ancho del contenido). Procura que la lista incluya clases de layout (grid), componentes y utilidades.
* **2.3.** Basado en tu investigación, menciona dos **ventajas** y dos **desventajas** claras de usar Bootstrap en un proyecto.

**[ESPACIO PARA TU RESPUESTA 2]**
Bootstrap propone que la UI se arme como si ensamblas piezas prefabricadas (componentes), aprovechando utilidades y layout flexible, en lugar de partir de estilos personalizados para cada elemento.

algunas clases fundamentales de bootstrap
container: crea un contenedor centralizado con anchos máximos adaptables según el tamano de la pantalla
row: crea filas en forma de rejilla, se usa para columnas
col: define columnas dentro de un row ejemplo: .col-md-6 ocupa 6 de 12 columnas en tamaño mediano.
btn: clase para botones aplicando padin, borde y tipografia.
card: crea un componente de tipo tarjeta con estructura defina como sombras, padding.
navbar: clase para barra de navegación responsiva
modal: define diálogo emergente con estilos y comportamiento: fonde atenuado, centrado, cerrar, entre otros.
mt: se usa para aplicar margen en la parte de arriba.
text-center: se usa para centrar horizontalmente el texto  dentro de un elemento
align-items: centra elementos hijos dentro de un contenedor.

ventajas: me parece que el tema del tiempo es fundamental, también tiene diseños muy buenos y que se adaptan a todo, son responsivos 
desventajas: que cuando se trata de crear algo mas personalizado estos componente no creo q se ajusten a lo q quieres, son mas bien estandar.

---

### Pregunta 3: Tailwind CSS - El Enfoque "Utility-First"

* **3.1.** Describe la filosofía **"Utility-First"** (clases de utilidad) de **Tailwind CSS** y en qué se diferencia fundamentalmente del enfoque de Bootstrap.
* **3.2.** Investiga en la documentación de Tailwind y crea una lista con **10 clases** de utilidad. Incluye el nombre de la clase y el estilo CSS que aplica. (Ej: `.text-center` - Aplica `text-align: center;`). Procura que la lista incluya clases para manejo de colores, espaciado, tipografía y flexbox.
* **3.3.** Basado en tu investigación, menciona dos **ventajas** y dos **desventajas** claras de usar Tailwind CSS en un proyecto.

**[ESPACIO PARA TU RESPUESTA 3]**
la filosofía de tailwind css se basa en clases utilitarias pequeñas, atómicas, que aplican estilos muy específicos (márgenes, colores, tipografía, tamaño, flexbox, etc.). Se combinan en el HTML para construir el diseño. es muy flexible por las clases atómicas tienes control sobre cada parte del estilo 

10 clases de utilidad de tailwind:
text-lg aplica tamano de fuente grande 
font-bold: le da peso a la letra la pone mas gorda y negrita
px-6: le da espaciado en el eje x de los elementos
bg-blue-500: el da color de fuente a la letra un azul medio
flex: es como el display flex
justify-between: alineacion horizontal entre elementos en el espacio permitido
border-blue-900: color en el borde del componente
py-6: crea padding en el eje y del elemento
text-sm: pone la letra muy pequeña, funciona como un breakpoint
uppercase: trasforma la letra toda en mayuscula
ventajas: flexibilidad, control mas centrado en componentes y al instante.
desventajas: se puede ver muy saturado de clases en cada componente, curva de aprendizaje, cuesta al principio entender la filosfía.

---

### Pregunta 4: BEM - Organizando CSS Puro

* **4.1.** ¿Qué es la metodología **BEM** (Block, Element, Modifier)? Explica con tus propias palabras qué representa cada una de sus partes (Bloque, Elemento y Modificador).
* **4.2.** ¿Qué problema clave viene a solucionar BEM en el desarrollo con CSS puro? ¿Cómo ayuda a prevenir colisiones de estilos y a hacer el código más mantenible?
* **4.3.** Muestra un ejemplo de código HTML y CSS para un componente de "tarjeta de producto" (`product-card`) utilizando la sintaxis BEM. El bloque debe tener elementos como un título, una imagen y un botón, y el botón debe tener un modificador para un estado primario (ej. `product-card__button--primary`).

**[ESPACIO PARA TU RESPUESTA 4]**
la metodologia Bem se centra en dividir en partes el elemento para que sea mas entendible y fácil de mantener.
la unidad block crea el componente completo ejemplo un class="card".
el elemento es una parte interna del block, sirve para describir partes internas del componente.
y el modificardor sirve para crear variantes o estados de un elemento.

el problema que viene a solucionar la metodologia BEM: este nació para resolver problemas de escalabilidad y mantenimiento en proyectos grandes con CSS puro como la colisión de estilos, dificultades para mantener el código
para evitar colisiones en la practica cada clase es única y especifica a su bloque, por lo que es casi imposible sobrescribirla por accidente ejemplo .card__title { font-size: 1.5rem; }, .menu__title { font-size: 1rem; } aunque tengan title los dos no hay riesgo.

<div class="product-card">
  <img
    class="product-card__image"
    src="https://via.placeholder.com/200"
    alt="Producto"
  />

  <h2 class="product-card__title">Vela Aromática de Lavanda</h2>

  <button class="product-card__button">Agregar al carrito</button>
  <button class="product-card__button product-card__button--primary">Comprar ahora</button>
</div>



---

### Pregunta 5: Frameworks y CSS Puro - Conflictos y Convivencia

* **5.1.** ¿Es posible usar hojas de estilos personalizadas (CSS puro) junto a un framework? Explica las implicaciones y el orden en que deberían cargarse los archivos CSS en el HTML.
* **5.2.** Investiga sobre la **especificidad de CSS**. ¿Qué es y cómo puede generar conflictos al intentar sobreescribir un estilo de un framework? ¿Qué regla de estilo es más específica: la de una clase del framework (ej. `.btn-primary`) o una regla que tú escribas en tu CSS (ej. `#mi-boton-especial`)?
* **5.3.** ¿Es técnicamente posible y/o recomendable usar Bootstrap, Tailwind CSS y una hoja de estilos propia en un mismo proyecto? Argumenta sobre los posibles conflictos (ej. reseteo de estilos, colisión de nombres de clases) y problemas de rendimiento que esto podría causar.

**[ESPACIO PARA TU RESPUESTA 5]**

---

### Pregunta 6: Comparación y Veredicto Final

* **6.1.** Crea una comparativa simple que resuma las diferencias clave entre Bootstrap, Tailwind CSS y una metodología como BEM para CSS puro. Considera al menos los siguientes criterios: **Curva de Aprendizaje**, **Nivel de Personalización**, **"Limpieza" del HTML** y **Velocidad de prototipado**.
* **6.2.** ¿En qué tipo de proyecto recomendarías usar **Bootstrap**? ¿En cuál **Tailwind CSS**? ¿Y en cuál optarías por **CSS Puro + BEM**? Justifica tu respuesta basándote en las fortalezas y debilidades de cada enfoque.

**[ESPACIO PARA TU RESPUESTA 6]**