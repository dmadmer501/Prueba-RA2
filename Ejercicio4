# Informe de Evidencias — Proyecto Página Web F1

## 4.1. Introducción

Esta página web está dedicada a la Fórmula 1 y busca presentar información de forma clara y visual.
Incluye una cabecera fija, un menú superior, un menú lateral tipo hamburguesa, una sección principal con imagen destacada, una galería de pilotos, una tabla de equipos y un formulario de suscripción.
La idea de diseño fue mantener un estilo moderno y ordenado, utilizando tonos rojos y negros relacionados con el mundo del motor, junto con textos grandes y limpios que facilitan la lectura.

---

## 4.2. Evidencias de HTML5

A continuación aparecen fragmentos de la estructura general del sitio, acompañados de una explicación natural de lo que hace cada parte.

### Estructura principal con HTML5
````
<header class="site-header">
  <h1><a href="#hero">La formula de Dan1</a></h1>
  <nav class="main-nav">...</nav>
</header>

<main>
  <section id="hero" class="hero-section">...</section>
  <section id="galeria">...</section>
  <section id="tabla">...</section>
  <section id="formulario">...</section>
  <section id="adicional">...</section>
</main>

<footer class="site-footer">
  <p>&copy; 2025 — Proyecto F1 Simple | 1º DAM.</p>
</footer>
````

El header sirve como parte fija superior y contiene el título y el menú principal.
El main agrupa todas las secciones importantes del contenido.
Cada section separa el contenido en bloques claros: hero, galería, tabla, formulario, etc.
El footer aparece al final para mostrar información complementaria.

### Menú superior
````
<nav class="main-nav">
  <ul>
    <li><a href="#hero">Inicio</a></li>
    <li><a href="#galeria">Pilotos</a></li>
    <li><a href="#tabla">Equipos</a></li>
    <li><a href="#formulario">Suscribirse</a></li>
  </ul>
</nav>
````

Este menú permite moverse rápidamente por la página haciendo clic en los distintos enlaces internos, que llevan a secciones concretas de forma fluida.

### Menú lateral (hamburguesa) 
````
<input type="checkbox" id="menu-toggle" class="menu-toggle" hidden>

<label for="menu-toggle" class="open-menu">☰</label>

<nav id="sideMenu" class="side-menu">
  <ul>
      <li><a href="#hero">Inicio</a></li>
      <li><a href="#galeria">Galería de Pilotos</a></li>
      <li><a href="#tabla">Tabla de Equipos</a></li>
      <li><a href="#formulario">Formulario de Contacto</a></li>
  </ul>
</nav>
````

El checkbox actúa como interruptor invisible. Al pulsar el icono ☰, el menú se desplaza desde la izquierda y aparece en pantalla, evitando el uso de JavaScript.
Esto permite que la navegación en móviles sea sencilla y accesible.

### Sección Hero
````
<section id="hero" class="hero-section">
  <div class="hero-text">
      <h2>Página web Fórmula 1</h2>
      <p>Bienvenido al mi sitio web de formula 1.</p>
      <a href="#galeria" class="button">Ver Pilotos</a>
  </div>

  <div class="hero-image">
      <img src="..." alt="Coche de Fórmula 1">
  </div>
</section>
````

La sección está dividida en dos columnas: una con texto y otra con una imagen.
Su objetivo es presentar la temática desde el principio y guiar al visitante hacia el contenido principal con un botón destacado.

### Galería de pilotos
````
<div class="galeria-grid">
  <figure class="card">
      <img src="..." alt="Max Verstappen">
      <figcaption>Max Verstappen</figcaption>
  </figure>
</div>
````

Cada piloto se muestra dentro de una tarjeta que combina imagen y título.
La galería se adapta automáticamente al tamaño de pantalla, reorganizando las columnas cuando es necesario.

### Tabla de equipos
````
<table>
  <thead>
      <tr>
          <th>Posición</th>
          <th>Equipo</th>
          <th>Sede</th>
          <th>Puntos</th>
      </tr>
  </thead>
  <tbody>
      <tr><td>1</td><td>Red Bull Racing</td><td>Milton Keynes</td><td>750</td></tr>
  </tbody>
</table>
````

La tabla muestra información organizada y comparativa entre los equipos principales, lo que facilita visualizar datos de forma rápida.

### Formulario de suscripción
````
<form action="#" method="POST" class="contact-form">
  <label for="nombre">Tu Nombre:</label>
  <input type="text" id="nombre" name="nombre">

  <label for="email">Tu Email:</label>
  <input type="email" id="email" name="email">

  <select id="favorito" name="favorito">
    <option value="" disabled selected>Elige uno</option>
  </select>

  <textarea id="comentario"></textarea>
</form>
````

El formulario permite que el visitante deje su nombre, correo y preferencias, reforzando la interacción con la web.

---

## 4.3. Evidencias de CSS

Los fragmentos de CSS muestran cómo se ha construido el estilo general del sitio, aplicando selectores útiles, efectos visuales y sistemas de organización como Flexbox y Grid.

### Selectores utilizados
````
body { background-color: #FFFFFF; }
.site-header { background-color: #333; }
#sideMenu { left: -230px; }
.main-nav ul li a { color: white; }
````

Estos selectores permiten aplicar estilos específicos a cada parte de la página según su etiqueta, clase, ID o posición dentro del documento.

### Pseudoclases
````
a:hover { color: #CC0000; }
.card:hover { transform: scale(1.05); }
````

Las pseudoclases se usan para reaccionar cuando el usuario pasa el ratón por encima, dando sensación de interacción.

### Flexbox
````
.site-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
````

Flexbox ayuda a colocar los elementos dentro del encabezado de forma equilibrada, manteniendo su alineación incluso al cambiar de tamaño de pantalla.

### Grid
````
.hero-section {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.galeria-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
}
````

El Grid organiza el contenido de forma modular, permitiendo dividirlo en columnas que se ajustan automáticamente.

### Tarjetas con efecto
````
.card {
  border: 1px solid #ddd;
  border-radius: 4px;
  transition: transform 0.3s;
}
````

Esto da a cada tarjeta un aspecto limpio y uniforme, además de un pequeño efecto al pasar el ratón.

### Estilo de menús
````
.main-nav a:hover { color: #CC0000; }
.side-menu a:hover { background-color: #CC0000; }
````

Los menús cambian de color al interactuar, guiando al usuario mientras navega.

---

## 4.4. Fuentes utilizadas

Las tipografías ayudan a dar carácter y personalidad al diseño.

### Fuente local
````
@font-face {
  font-family: 'Roboto Local';
  src: url('../fonts/Roboto-Regular.woff2') format('woff2');
}
````

Se usa Roboto como base porque es una fuente clara y fácil de leer en cualquier pantalla.

### Fuente online
````
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@400;700&display=swap" rel="stylesheet">
````

Oswald se ha utilizado en títulos porque transmite fuerza y combina bien con el estilo deportivo del proyecto.

---

## 4.5. Funcionamiento del menú lateral

El menú lateral aparece cuando se marca el checkbox vinculado al icono ☰.
Al hacerlo, el CSS cambia la posición del panel:
````
.menu-toggle:checked ~ #sideMenu { left: 0; }
````

De esta forma, el menú se desplaza hacia dentro sin necesidad de JavaScript, haciendo la interfaz más simple y accesible.

---

## 4.6. Conclusión personal

Este proyecto me ha permitido aprender a organizar una página web completa usando etiquetas, menús y técnicas como Grid y Flexbox.
He descubierto formas nuevas de hacer un menú sin JavaScript (buscando en internet) y he mejorado en la separación entre estructura de la página y diseño.
Lo que más me ha costado ha sido ajustar el menú sin uso de JavaScript, además del propio diseño de la página más allá de la estructura, pero he aprendido varias cosas mientras buscaba como hacerlo por mi cuenta y viendo soluciones y diseños de terceros.
La sección que más me gusta es la galería de pilotos, porque combina imagen, interacción y un diseño agradable, además bajo mi punto de vista es de las mejores formas de ver el uso general de html y css, ya que están muy diferenciadas.
