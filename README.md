# Librería de 100 botones

Catálogo de 100 botones organizados en 10 categorías, hecho con HTML y CSS.

- Sitio: https://yulianadurangoh.github.io/libreria-100-botones/
- Combinaciones: https://yulianadurangoh.github.io/libreria-100-botones/combinaciones.html

## Cómo se usa

Cada botón lleva la clase base `btn` más una o varias clases:

```html
<button type="button" class="btn btn-primary btn-pill btn-grow">
  Guardar
</button>
```

## Botón 100: diseño original (`btn-original`)

Este botón combina técnicas de categorías diferentes:

1. Degradado (categoría 4): el fondo usa `linear-gradient`.
2. Forma (categoría 2): los extremos son redondeados con `border-radius`.
3. Transformación (categoría 6): se eleva y crece con `translateY` y `scale`.
4. Pseudoelementos (categoría 8): `::before` hace un relleno amarillo y `::after` muestra una flecha.
5. Animación (categoría 9): `@keyframes` mueve el degradado.

## ¿Qué clase prevalece?

Si dos clases modifican la misma propiedad, gana la que está más abajo en `styles.css`. No importa el orden en que se escriban en el atributo `class`.

- `btn-rounded` y `btn-pill`: gana `btn-pill`, porque está definida después.
- `btn-gradient-ocean` y `btn-glow-pulse`: se ve el degradado, porque `background-image` se pinta encima de `background-color`.
- `btn-pulse` y `btn-grow`: gana la animación, porque `animation` prevalece sobre `transform` mientras se ejecuta.
