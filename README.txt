# GAER GROUP — web con panel de administración

Esta versión permite editar el contenido y subir fotos desde `/admin/` usando Decap CMS.

## Qué podrás modificar
- Textos en español e inglés
- Imagen principal
- Servicios
- Showroom y puntos destacados
- Galería/proyectos (añadir tantas entradas como quieras)
- Teléfonos, WhatsApp, email, dirección y horario
- Subir fotos nuevas desde el propio panel

## Arquitectura
- Web estática responsive.
- Contenido en `content/site.json`.
- Fotos nuevas en `assets/uploads/`.
- Decap CMS en `/admin/`.
- GitHub guarda los contenidos y el historial.
- Cloudflare Pages publica automáticamente cada cambio.

## Importante
El panel necesita autenticación OAuth de GitHub. La configuración incluida deja marcados:
- `TU_USUARIO/TU_REPOSITORIO`
- `TU-OAUTH-WORKER.workers.dev`

Para el OAuth de GitHub se puede usar un Cloudflare Worker. El proyecto oficial/comunitario de referencia es `sterlingwes/decap-proxy`.

Una vez conectado el repositorio y el OAuth Worker, entrarás en:
`https://TU-WEB.com/admin/`

## Publicación
Conecta este proyecto a GitHub y después conecta el repositorio a Cloudflare Pages. Cada cambio guardado desde el panel crea un commit y Cloudflare vuelve a publicar la web.

## Datos pendientes
Completar desde el panel:
- Dirección exacta del showroom
- Horario
- Email
- Más fotos de obras
- Servicios/materiales concretos
