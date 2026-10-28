# Cambio de sábanas

App web personal para llevar el registro del cambio de sábanas de los miércoles, alternado cada semana entre dos personas.
Se publica con GitHub Pages desde la rama `gh-pages` y se usa en el iPhone agregándola a la pantalla de inicio desde Safari.

## Qué hace

- Muestra los miércoles de cada mes y a quién le toca.
- Permite marcar con un check cada cambio hecho y destaca el próximo o el atrasado.
- Guarda los cambios marcados solo en el dispositivo (`localStorage`).
- Funciona sin conexión después de la primera carga (`sw.js`).

## Archivos

- `index.html`: la app completa (estructura, estilos y lógica).
- `manifest.webmanifest`, `icons/`: nombre e ícono de la app.
- `sw.js`: copia local para abrir sin conexión.
- `fonts/`: tipografías Bricolage Grotesque y Figtree, distribuidas bajo la licencia SIL Open Font License 1.1.

## Panel Casa

Al final de la app está la tarjeta «Panel Casa». Con «Pegar código» (el código se copia en Panel Casa → Conexiones), la app publica en el buzón privado de GitHub los últimos miércoles marcados y el primero que falta, en el hito «Sábanas · panel». Así el panel sabe si el cambio ya se hizo y avisa si uno quedó atrasado. Se publica cada vez que se marca o desmarca un miércoles; «Desconectar» deja de publicar y vacía el hito.

El módulo es el mismo en todas las apps conectadas y se copia desde el repositorio casa con `python3 herramientas/conectar-apps.py`.
