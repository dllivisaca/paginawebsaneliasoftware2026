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

## Sesion 2026-03-17

### Cambios realizados hoy
- Se ajustaron los precios visibles de la seccion `#pricing` en `index.html` para los planes `Basico` y `Profesional`, manteniendo intacta la logica del toggle mensual/anual.
- Se agrego una leyenda visible `Todos los precios incluyen IVA.` dentro de la seccion `#pricing`.
- Se reemplazo el contenido de la seccion `#faq-2` en `index.html` por preguntas y respuestas orientadas a Sanelia Software, luego se ajusto tambien la cabecera de la seccion a `Preguntas frecuentes`.
- Se agrego un decimo item al final del bloque FAQ de `#faq-2` manteniendo la estructura del acordeon y el patron de `data-aos-delay`.
- Se reutilizo la seccion `#subscribe` como CTA de contacto por WhatsApp, eliminando el formulario/input de newsletter y dejando un unico boton con `href="#"`.
- Se reemplazo el estilo heredado del boton de `#subscribe` por un CTA independiente con estilo inline tipo pill en color magenta.
- Se oculto la seccion `#recent-blog-postst` de `index.html` agregando `hidden` en la apertura del `<section>`, sin eliminar su HTML.
- Se adapto la seccion `#contact` con datos reales de Sanelia Software, incluyendo titulo, descripcion, direccion, telefono placeholder, correo visible y mapa embebido apuntando a Guayaquil.
- Se actualizo `forms/contact.php` para cambiar el correo destinatario del formulario a `daisyllivisaca@gmail.com`.
- Se tradujeron al espanol los labels visibles y el boton submit del formulario de contacto en `index.html`.
- Se oculto el bloque visual `footer-newsletter` del footer de `index.html` usando `hidden`, sin eliminarlo del codigo.
- Se actualizaron los datos visibles del bloque de contacto del footer en `index.html` con direccion, telefono y correo reales de Sanelia.
- Se inspeccionaron las paginas internas `service-details.html`, `portfolio-details.html` y `blog-details.html` para evaluar su reutilizacion como base de paginas internas corporativas.
- Se creo `soluciones.html` a partir de `service-details.html`, reemplazando el contenido principal demo por contenido real de Sanelia Software orientado a una pagina de soluciones.
- Se reemplazaron el `header` y el `footer` de `soluciones.html` para alinearlos visualmente con `index.html`, ajustando los enlaces del header para que funcionen correctamente desde una pagina interna.
- Se actualizo el `head` de `soluciones.html` para cargar tambien la fuente `Arvo`, dejando el branding textual del logo consistente con `index.html`.
- Se agrego un bloque `<style>` local en `soluciones.html` para compensar el `fixed-top` del header y despues se ajusto el breadcrumb del `page-title` con icono de casa, subrayado del item actual y mas espacio superior.
- Se corrigio el copy de dos parrafos del contenido principal de `soluciones.html` para que `Sanelia Software` quede claro como empresa y no como nombre del producto.

### Archivos creados
- `soluciones.html`

### Archivos modificados
- `index.html`
- `forms/contact.php`
- `soluciones.html`
- `SECURITY-NOTES.md`

### Archivos/recursos nuevos definidos o previstos
- `soluciones.html` quedo definido como nueva pagina interna basada en `service-details.html`.
- Se mantuvo temporalmente en `soluciones.html` la imagen `assets/img/services/services-4.webp` como recurso provisional del bloque principal.

### Verificacion realizada
- Se verificaron por inspeccion puntual las lineas exactas modificadas en `index.html`, `forms/contact.php` y `soluciones.html` despues de cada cambio.
- Se confirmo repetidamente que los cambios quedaran acotados a la seccion solicitada en cada paso, especialmente en `#pricing`, `#faq-2`, `#subscribe`, `#contact` y footer.
- Se confirmo por inspeccion que el formulario de contacto sigue apuntando a `forms/contact.php`.
- Se confirmo por inspeccion que `soluciones.html` conserva su `<main>` intacto mientras se reemplazaron solo `header`, `footer`, fuentes y ajustes locales de espaciado/breadcrumb.
- Se comprobo que `soluciones.html` ya carga `Arvo` para `.brand-main` y mantiene `Poppins` para `.brand-sub`.

### Pendientes recomendados
- Validar en navegador `soluciones.html` para confirmar que el `page-title` ya no queda tapado por el `header fixed-top`.
- Revisar visualmente en navegador la consistencia final del branding del header y footer entre `index.html` y `soluciones.html`.
- Definir una imagen final para `soluciones.html` que reemplace el recurso temporal `assets/img/services/services-4.webp`.
- Si mas adelante se enlaza `soluciones.html` desde el menu de `index.html`, actualizar esos enlaces de navegacion de forma consistente en todas las paginas internas.
- Verificar en entorno real/XAMPP si el envio de correo de `forms/contact.php` requiere configuracion adicional de `mail()` o SMTP.

### Como retomar en una nueva sesion
- Indicar: "Revisa `SECURITY-NOTES.md` y continuemos desde la sesion 2026-03-17".
