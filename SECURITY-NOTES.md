# Security Notes

## Sesion 2026-03-12

### Cambios realizados hoy
- Se reemplazo el branding visible del template "Arsha" por "Sanelia Software" en las paginas HTML publicas principales.
- Se actualizo el navbar de `index.html` para usar los items `Inicio`, `Soluciones`, `Funcionalidades`, `Precios`, `Contacto` y el boton `Prueba gratis`.
- Se ajusto la paleta global del sitio desde SCSS fuente para reflejar branding de Sanelia Software, incluyendo `heading-color`, `accent-color`, backgrounds claros/oscuros y overrides del header.
- Se hizo una micro-ronda adicional para mover el color interactivo principal a un magenta de marca (`#E93CAC`).
- Se agrego el icono de corazon de Sanelia al branding del header y del footer en `index.html`, manteniendo el nombre de marca como texto HTML real.
- Se actualizo la imagen principal del hero en `index.html` para usar `assets/img/hero-sanelia-booking-v2.png`.
- Se ajusto visualmente el ancho de la imagen del hero desde SCSS local para que ocupe mejor la columna derecha, manteniendo la animacion existente.
- Se oculto temporalmente la seccion `#clients` en `index.html` usando la clase `d-none`, sin eliminar su HTML ni el swiper.
- Se reemplazo el copy del bloque hero textual en `index.html`.
- Se reemplazo el contenido textual de las secciones `About` y `Why Us` en `index.html`, manteniendo estructura, layout, iconos, acordeon e imagenes.
- Se ajusto el branding textual del header y footer para separar `SANELIA` y `SOFTWARE` en spans independientes, usando `Arvo` para `SANELIA` y `Poppins` para `SOFTWARE`.
- Se ajustaron solo los colores del branding textual del footer para dejar `SANELIA` en `#2b23d9` y `SOFTWARE` en `#000000`.

### Archivos creados
- `SECURITY-NOTES.md`

### Archivos modificados
- `index.html`
- `assets/scss/_variables.scss`
- `assets/scss/layouts/_header.scss`
- `assets/scss/layouts/_footer.scss`
- `assets/scss/sections/_hero.scss`
- `assets/css/main.css`

### Archivos/recursos nuevos definidos o previstos
- `assets/img/sanelia-heart-logo.png` fue usado como recurso de branding en header y footer.
- `assets/img/hero-sanelia-booking.png` se uso primero como imagen del hero y luego fue reemplazada por `assets/img/hero-sanelia-booking-v2.png`.

### Verificacion realizada
- Se verificaron los bloques HTML y reglas SCSS/CSS afectados antes y despues de cada micro-ronda.
- Se recompilo `assets/css/main.css` varias veces desde `assets/scss/main.scss` usando `npx sass`.
- Se confirmo por inspeccion que los cambios de branding textual del footer no alteraron el header.
- Se confirmo por inspeccion que la seccion `#clients` sigue presente en `index.html` aunque quedo oculta visualmente.
- Se confirmo que la imagen del hero mantiene `class="img-fluid animated"` y el mismo contenedor con `data-aos`.

### Pendientes recomendados
- Revisar visualmente en navegador el branding tipografico del header y footer para validar balance entre `Arvo` y `Poppins`.
- Validar en navegador la legibilidad final de los textos nuevos con acentos; en consola aparecio mojibake al inspeccionar algunas lineas, por lo que conviene confirmar codificacion UTF-8 real del archivo.
- Traducir y alinear el resto de secciones publicas que aun conservan contenido placeholder o en ingles.
- Sustituir datos de contacto, textos de newsletter, pricing, FAQ adicional y demas contenido de plantilla que todavia no representa el negocio real.

### Como retomar en una nueva sesion
- Indicar: "Revisa `SECURITY-NOTES.md` y continuemos desde la sesion 2026-03-12".

## Sesion 2026-03-16

### Cambios realizados hoy
- Se oculto temporalmente la seccion `#skills` en `index.html` sin eliminar su HTML.
- Se reutilizo la seccion `#services` como bloque de `Funcionalidades clave`, actualizando titulo, descripcion, textos de cards e iconos, manteniendo el layout original.
- Se reutilizo la seccion `#work-process` como flujo comercial de onboarding en 3 pasos, actualizando titulos, textos, bullets, `alt` y luego afinando el copy para no presentar `Sanelia` como nombre de la plataforma.
- Se actualizaron las imagenes de `#work-process` para usar `steps-demo-3d.webp`, `steps-trial-3d.webp` y `steps-plan-3d.webp`.
- Se reutilizo `#call-to-action` como llamada a solicitar una demo, reemplazando titulo, parrafo y texto del boton.
- Se oculto temporalmente la seccion `#portfolio` solo desde la linea de apertura del `<section>`.
- Se adapto la seccion `#team` para mostrar una sola card visible de `Daisy Llivisaca`, con copy de fundadora, LinkedIn real y las otras cards ocultas visualmente.
- Se ajusto la presentacion de la card visible de `#team` para centrarla y mover el icono de LinkedIn primero junto al cargo y despues junto al nombre, manteniendo el resto de la estructura.
- Se reconstruyo la seccion `#pricing` para dejar solo los planes `Basico` y `Profesional`, manteniendo `Profesional` como card destacada con badge `Mas popular`.
- Se agrego un selector visual `Mensual / Anual` en `#pricing` con JavaScript vanilla minimo para alternar precios y sufijos.
- Se restauro el peso visual de los precios en `#pricing` y se agrego un mensaje dinamico de ahorro visible solo en modo anual.
- Se mejoro el badge de ahorro anual en `#pricing` con una presentacion mas promocional y una animacion local sutil.
- Se adapto la seccion `#testimonials` para dejar 3 testimonios realistas alineados con Sanelia, manteniendo el slider existente.

### Archivos creados
- Ninguno.

### Archivos modificados
- `index.html`
- `SECURITY-NOTES.md`

### Archivos/recursos nuevos definidos o previstos
- Se referenciaron en `index.html` los recursos `assets/img/steps/steps-demo-3d.webp`, `assets/img/steps/steps-trial-3d.webp` y `assets/img/steps/steps-plan-3d.webp` para la seccion `#work-process`.

### Verificacion realizada
- Se verifico cada cambio con inspeccion puntual de bloques HTML antes y despues de editar.
- Se reviso repetidamente el `git diff` de `index.html` para confirmar que cada ajuste quedara acotado a la seccion solicitada en cada paso.
- Se confirmo por inspeccion que `#pricing` mantiene el plan `Profesional` como destacado, el toggle funcional y el mensaje de ahorro visible solo en modo anual.
- Se confirmo por inspeccion que `#testimonials` quedo reducido a 3 slides y conserva la estructura del carrusel.

### Pendientes recomendados
- Validar en navegador los textos con acentos, ya que en consola siguio apareciendo mojibake al inspeccionar algunas lineas.
- Probar visualmente en responsive el bloque `#pricing`, sobre todo el toggle, el badge `Mas popular` y el mensaje de ahorro anual.
- Revisar en navegador la nueva presentacion de `#team` y decidir si luego se reemplaza la imagen placeholder de la fundadora.
- Completar la adaptacion de otras secciones que aun conserven copy placeholder, especialmente FAQ y cualquier bloque restante en ingles.

### Como retomar en una nueva sesion
- Indicar: "Revisa `SECURITY-NOTES.md` y continuemos desde la sesion 2026-03-16".
