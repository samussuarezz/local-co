# Local.co

**Planes hechos por quienes viven allí.** App para encontrar y reservar experiencias locales y comunitarias en Colombia.

Proyecto **Kit 8 · Local Experience** · Materia Usabilidad · HumanLab
Samuel Suarez · UX Designer

> Prototipo académico. Los planes, anfitriones y precios son ejemplos y ningún pago es real.

## Cómo abrirla en el teléfono

1. Abre el link de GitHub Pages del repositorio (Settings → Pages).
2. **iPhone:** en Safari, toca Compartir y luego *Agregar a inicio*.
3. **Android:** en Chrome, toca el menú ⋮ y luego *Instalar app*.

La app queda con icono propio, se abre en pantalla completa y funciona sin internet después de la primera visita.

## User flow

| # | Paso | Patrón de referencia |
|---|------|----------------------|
| 0 | Bienvenida animada (ruta sobre el mapa de Colombia) | Splash de Parcel (DailyFlutterUI) |
| 1 | Inicio: destino y fechas, como invitado | "Quick track as guest" de Parcel |
| 2 | Descubrir con categorías y filtro "Solo comunitarios" | Categorías de Pizza Ordering Flow |
| 3 | Detalle del plan y del anfitrión: horario, extras, personas y precio en vivo | Detalle de Pizza + fichas de Civitatis |
| 4 | ¿Reservar o contactar? (chat con respuestas rápidas) | — |
| 5 | Acceso solo al reservar (hoja inferior) | Login de Parcel |
| 6 | Reserva y pago (Nequi, PSE, tarjeta) con desglose para la comunidad | Checkout de Pizza |
| 7 | Confirmación y Mi viaje (código, línea de tiempo) | "Payment Successful" de Pizza |
| 8 | Valorar y recomendar | — |

## Competencia: Civitatis

Fuente: revisión de civitatis.com (home y fichas de actividades en Medellín y Cali), octubre de 2026.

| Aspecto | Civitatis | Local.co |
|---|---|---|
| Quién te guía | La ficha no identifica al operador; los nombres de los guías aparecen solo en reseñas | Anfitrión con nombre, foto, verificación y chat antes de pagar |
| Oferta en Colombia | Tours urbanos en Bogotá, Medellín y Cali | Experiencias comunitarias en regiones |
| Precio y pago | US$ por defecto (se puede cambiar a COP); tarjetas, PayPal, Apple/Google Pay, Klarna | Siempre en COP; Nequi, PSE y tarjeta |
| Dinero a la comunidad | No se indica | Desglose del 85 % que llega a la comunidad |
| Cancelación | Gratis hasta 24 h antes | Igual (adoptado) y visible en tarjetas y pago |
| Confianza | 9,1/10, más de 5 millones de opiniones, atención 24/7 | Reseñas por anfitrión y verificación |
| Cuenta | Registro o consulta de la reserva con email + código | Explorar sin cuenta; se pide solo al reservar |

**Lo que adoptamos de Civitatis:** cancelación gratuita visible, precio final sin cargos extra, ficha con secciones (incluye, punto de encuentro, accesibilidad, reseñas) y código de reserva en el teléfono.

**Oportunidad:** Civitatis vende el tour, pero no muestra a la persona ni a la comunidad que lo hace. Local.co puede ser la app donde conoces a tu anfitrión antes de pagar y sabes cuánto le llega.

## Archivos

- `index.html`: toda la app (HTML, CSS y JavaScript)
- `manifest.webmanifest` e iconos (`icon-192.png`, `icon-512.png`, `apple-touch-icon.png`): permiten instalarla como app
- `sw.js`: hace que funcione sin conexión
