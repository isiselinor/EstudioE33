# Estudio E33 · Medellín

Landing de reservas del estudio de Entr3t3nimiento: configurador de sesión, agenda, galería, rider y solicitud de reserva. Bilingüe (ES/EN), tema claro y oscuro.

## Estructura

```
index.html              Página completa (HTML + CSS + JS, sin dependencias)
assets/img/             Fotos de la galería
assets/img/thumbs/      Miniaturas de los formatos del inicio
apps-script/Codigo.gs   Script de la hoja "E33 Estudio — Control landing"
netlify.toml            Configuración de Netlify
```

## Previsualizar con el equipo (Netlify)

1. En Netlify: **Add new site → Import an existing project → GitHub** y elige este repositorio.
2. Build command: vacío. Publish directory: `.`
3. En **Site configuration → Build & deploy → Branches and deploy contexts**, activa **Branch deploys** para `develop`.
4. Trabaja en `develop`. Cada push genera un link de vista previa del tipo `develop--<sitio>.netlify.app` para compartir con el equipo.
5. Cuando esté aprobado, haz merge de `develop` a `main` para publicar la versión final.

> El link de vista previa es público para quien lo tenga. No lo compartas fuera del equipo hasta publicar.

## Conexión con la hoja de Google

La landing ya está conectada: `CONFIG.API_URL` apunta al programa «E33 Estudio · Landing» (Drive: E33 · Sistema / Estudio E33). Su código vive en el repositorio `app_e33`, carpeta `apps-script-estudio-landing`. Las solicitudes llegan a la pestaña Solicitudes, crean un evento tentativo en el calendario y avisan por correo con botones para responder.

## Qué se edita desde la hoja

| Pestaña | Qué controla |
| --- | --- |
| Config | TRM (automática), recargo nocturno, WhatsApp, correos de aviso, calendario, carpeta de fotos, capacidad |
| Tarifas | Formatos y precios con y sin ingeniero (ES/EN) |
| Produccion | Mezcla, máster y precio combo |
| Equipos | Canales de la consola (solo estado Nuevo u Operativo) |
| Rider | Rider técnico público |
| Media | Fotos y videos de la galería (se llena con "Sincronizar fotos y videos") |
| Solicitudes | Cada solicitud recibida; el estado actualiza el calendario |

Los cambios aparecen en la página en unos 5 minutos (caché del script). Para verlos al instante: menú **E33 Estudio → Limpiar caché de la landing**.
