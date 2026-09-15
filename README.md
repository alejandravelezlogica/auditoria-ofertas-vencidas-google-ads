# Auditoría de Ofertas Vencidas — Google Ads GHL Hotels

Reporte de auditoría que detecta anuncios **activos** de Google Ads (Search, Display, Demand Gen y Performance Max) cuyo texto menciona un mes o fecha que ya pasó respecto a la fecha de referencia — típicamente una oferta de temporada que no se retiró del anuncio a tiempo.

## Cómo verlo

Este repo es privado, así que GitHub no lo renderiza como página pública. Para verlo:

1. Descarga [`index.html`](./index.html) (botón "Download raw file" en GitHub, o clona el repo).
2. Ábrelo con doble clic — es un archivo autocontenido (todo el CSS embebido), se ve igual en cualquier navegador, sin necesidad de servidor ni conexión a internet.

## Qué valida cada hallazgo

- Solo anuncios/recursos con estado **ENABLED** (campaña, grupo y anuncio/recurso).
- Cubre los 4 canales: Search, Display, Demand Gen y Performance Max.
- Clasifica cada fecha detectada como **Booking Window** (fecha límite de reserva) o **Travel Window** (fecha límite de viaje/estadía), porque un mismo anuncio suele mezclar ambas y solo una puede estar vencida.
- Cada hallazgo requiere confirmación manual antes de pausar o editar el anuncio — el texto publicitario es ambiguo y ningún anuncio se modifica automáticamente.

## Reproducir el reporte

El script que genera este reporte corre diariamente como parte del pipeline interno de GHL Hotels y no se incluye en este repositorio (usa credenciales de la API de Google Ads que no se comparten externamente).
