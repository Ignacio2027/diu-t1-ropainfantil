# Documentación de la interfaz — T-Children

## 1. Justificación del diseño

### 1.1 Importancia del diseño centrado en el usuario
El diseño de la aplicación está pensado principalmente para madres, padres, abuelos y personas que compran ropa infantil como regalo. Son personas que normalmente tienen poco tiempo y pueden tener dudas a la hora de elegir una talla.

Por eso, la aplicación debe ser intuitiva y fácil de usar desde el móvil. La idea es que el usuario pueda encontrar la ropa que busca rápidamente, consultar las tallas y realizar una compra sin complicaciones.
### 1.2 Objetivos y metas del proyecto
Los principales objetivos de la aplicación son:

1. Conseguir que el usuario pueda completar una compra en menos de minutos.

2. Conseguir que el usuario pueda encontrar un producto utilizando los filtros en menos de  segundos.

3. Conseguir que al menos 9 de cada 10 usuarios puedan encontrar y utilizar correctamente la guía de tallas.
### 1.3 Beneficios esperados
Para el usuario, la aplicación permitirá encontrar ropa infantil de una forma más rápida y sencilla. También tendrá más facilidad para elegir la talla gracias a la guía de tallas.

Para la tienda, la aplicación puede facilitar las compras desde el móvil y hacer que el proceso de compra sea más cómodo para los clientes.
## 2. Investigación y análisis de usuarios

### 2.1 Datos demográficos y segmentación
El público principal de la aplicación son personas que compran ropa y calzado infantil para niños de 0 a 14 años.

Dentro de este grupo encontramos principalmente madres, padres, abuelos y personas que compran regalos. Son usuarios que pueden utilizar la aplicación desde el móvil y que buscan realizar la compra de forma rápida.

También se tiene en cuenta que algunos usuarios pueden tener dudas con las tallas, por lo que la aplicación debe facilitar esta información.
### 2.2 Personas
#### Persona 1: Jose Miguel, 35 años

Josemi es un padre de dos niños y compra ropa infantil habitualmente. Tiene poco tiempo libre y suele hacer las compras desde el móvil.

**Objetivos:**

* Encontrar un regalo fácilmente.
* Saber qué talla debe comprar.
* Tener un proceso de compra sencillo.

**Frustraciones:**

* No saber qué talla elegir.
* Encontrar demasiadas opciones y no saber cuál escoger.
* Tener dificultades para encontrar algunas funciones.

#### Persona 2: Mari Carmen, 75 años

Mari Carmen es una abuela y utiliza la aplicación para comprar regalos de ropa para sus nietos. No compra ropa infantil habitualmente y puede tener más dudas a la hora de elegir una talla.
**Objetivos:**

* Encontrar ropa rápidamente.
* Saber qué tallas hay disponibles.
* Poder comprar sin perder mucho tiempo.

**Frustraciones:**

* Tardar mucho en encontrar una prenda.
* No saber qué talla elegir.
* Tener que pasar por demasiados pasos para comprar.
### 2.3 Análisis de la competencia
**Zara**
Que hace bien: Tiene muchas categorías y permite filtrar los productos.
Que hace mal: Utilizar categorías y filtros claros.
Que me llevo: Utilizar categorías y filtros claros.
**HyM**
Que cosas hace bien: Tiene una navegación sencilla y diferentes categorías de ropa infantil.
Que cosas hace mal: Organizar bien los productos y facilitar la búsqueda.
Que me llevo: Organizar bien los productos y facilitar la búsqueda.
**Primark**
Que cosas hace bien:Está muy centrada en ropa para toda la familia y permite buscar por categorías.
Que cosas hace mal:Puede resultar algo cargada por la cantidad de productos y opciones.
Que llevo: Mostrar la información importante de forma clara y sencilla.
### 2.4 Insights y hallazgos clave
1. Los usuarios tienen dudas con las tallas → añadir una guía de tallas dentro del detalle del producto.
2. Los usuarios tienen poco tiempo para comprar  hacer que la navegación y el proceso de compra sean rápidos y sencillos.
3. Los usuarios compran principalmente desde el móvil utilizar botones grandes y fáciles de pulsar.
4. Los usuarios pueden tener problemas para encontrar un producto añadir un buscador y filtros por edad, talla, color y precio.
## 3. Diseño de la interfaz

### 3.1 Mapa de navegación

La aplicación MiniStyle permite acceder desde la pantalla de inicio a las categorías de ropa infantil. Después, el usuario puede seleccionar un producto, elegir una talla, añadirlo al carrito y continuar con la compra hasta llegar a la confirmación.

```mermaid
flowchart TD
    A[Inicio] --> B[Categoría niño o niña]
    B --> C[Selección de producto]
    C -->|Añadir al carrito| D[Carrito]
    C -->|Comprar ahora| E[Página de compra]
    D --> E
    E -->|Confirmar| F[Confirmación]
```

### 3.2 Wireframes

Se han realizado wireframes de las pantallas principales de MiniStyle para organizar los elementos antes de crear el diseño definitivo.

- **Inicio:** muestra las categorías infantiles y una selección de productos.
- **Página de niño o niña:** permite consultar las prendas de la categoría elegida.
- **Selección de producto:** muestra la prenda, las tallas disponibles y las opciones para añadirla al carrito o comprarla.
- **Carrito:** presenta los productos seleccionados, permite eliminarlos y muestra el importe total.
- **Página de compra:** contiene los campos para introducir los datos necesarios para continuar con el pedido.
- **Confirmación:** muestra el resultado final del proceso de compra.
git remote -v
Los wireframes sirven como base para desarrollar el prototipo de alta fidelidad utilizando Material Design 3.
![alt text](image.png)

### 3.3 Guía de estilo Material Design 3

La aplicación MiniStyle utiliza Material Design 3 para que todas las pantallas tengan un diseño parecido y fácil de utilizar.

**Colores:** se utiliza el naranja rojizo como color principal, acompañado de rosa apagado, amarillo mostaza y tonos grises. Se han preparado un esquema claro y otro oscuro.

**Tipografía:** se utiliza Roboto, con diferentes tamaños para títulos, subtítulos y textos.

**Rejilla y espaciado:**
- 4 columnas.
- Márgenes de 16 dp.
- Espaciado en múltiplos de 8 dp.
- Áreas táctiles de al menos 48 × 48 dp.
- Tamaño de las pantallas: 360 × 800 px.

**Componentes:** barras de navegación, tarjetas de productos, botones, campos de texto, mensajes de error y una guía de tallas desplegable.

Los colores se guardan en `diseno/estilos.json`. Se comprobará el contraste entre los colores y sus textos para cumplir el mínimo de 4,5:1 de WCAG AA.

### 3.4 Prototipo de alta fidelidad

El prototipo de MiniStyle se desarrollará en Figma a partir de los wireframes existentes. Se mantendrá el recorrido desde la selección de productos hasta la confirmación de compra.

En la versión final se incorporarán componentes de Material Design 3, componentes propios con variantes y Auto Layout, navegación entre pantallas, una ventana inferior superpuesta, animaciones de transición, un estado de error y pantallas en modo oscuro.

El prototipo deberá incluir al menos siete pantallas de 360 × 800 px y la palabra del día indicada en clase.