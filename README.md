# Prueba-RA2

## ✅ 1A. Pregunta
### ¿Por qué NO se centra el texto del <h1> en este caso? Explícalo con tus palabras por qué visual y estructuralmente no aparece centrado entre el borde izquierdo y el menú).

* El contenedor .site-header es un flex  en fila, lo que coloca uno pegado a la izquierda y otro pegado a la derecha.​

* text-align: "center" actúa sobre el contenido del h1, no sobre la posición del propio h1 dentro del header, por eso el título no se ve centrado entre el borde izquierdo y el menú.​

## 1B. Ejercicio - Soluciona de dos formas diferentes

Debes indicar dos formas diferentes de conseguir que el h1 si quede centrado visualmente en la cabecera.

### Forma 1 (Flexbox)

.site-header {
  display: flex;
  align-items: center;
}

/* opción 1: que el h1 crezca y se centre */
.site-header h1 {
  flex: 1;
  text-align: center;
}

### Forma 2 (CSS Grid)

.site-header {
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;
}

.site-header h1 {
  grid-column: 2;
  text-align: center;
}

.site-header .main-nav {
  grid-column: 3;
  justify-self: end;
}

## 1C. Ejercicio - Convertir la cabecera en dos filas

.site-header {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto auto;
  row-gap: 30px;
  justify-items: center;
}

.site-header h1 {
  grid-row: 1;
}

.site-header .main-nav {
  grid-row: 2;
}

## 1D. Ejercicio - Dar relieve y separación visual al header

.site-header {
  background-color: #f5f5f5;
  padding: 20px;
  border-bottom: 1px solid #ddd;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

## ✅ Ejercicio 2 - Reorganización del header con tres elementos

## 2A. Ejercicio

### Cambio de HTML

<header class="site-header">
  <button class="menu-btn" aria-label="Abrir menú lateral">☰</button>
  <h1>Mi Sitio Web</h1>
  <nav class="main-nav">
    nav
  </nav>
</header>


## 2B. Ejercicio

## Cambio del CSS

.site-header {
  display: flex;
  align-items: center;
}

.menu-btn {
  margin-right: 1rem;
}

.site-header h1 {
  flex: 1;
  text-align: center;
}

.main-nav {
  margin-left: auto;
}

## Cambio haciendo uso de Grid

.site-header {
  display: grid;
  grid-template-columns: auto 1fr auto;
  align-items: center;
  column-gap: 1rem;
}

.menu-btn {
  grid-column: 1;
  justify-self: start;
}

.site-header h1 {
  grid-column: 2;
  text-align: center;
}

.main-nav {
  grid-column: 3;
  justify-self: end;
}

### Ejercicio 3 - Miniaturas, zoom y enlace a la imagen original.

## 3A. Crear miniaturas

<div class="galleia-grid">
  <a href="img/imagenA.jpg" target="_blank">
    <img src="img/imagenA.jpg" alt="Descripción A" class="thumb">
  </a>
  <a href="img/imagenB.jpg" target="_blank">
    <img src="img/imagenB.jpg" alt="Descripción B" class="thumb">
  </a>
</div>

## 3B. Efecto hover

.gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
}

.gallery .thumb {
  width: 200px;
  height: auto;
  display: block;
  transition: transform 0.3s ease, box-shadow 0.3s ease, border 0.3s ease;
  border: 2px solid transparent;
}

.gallery a:hover .thumb {
  transform: scale(1.1);
  border-color: #333;
  box-shadow: 0 4px 8px rgba(0,0,0,0.3);
}


