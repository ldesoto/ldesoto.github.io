# FanUno — descarga y actualizaciones

Esta carpeta es la página pública de descarga de FanUno y el manifiesto de versión que consulta la app.

Archivos:

- `index.html` — página de descarga (la versión se lee en vivo desde `version.json`).
- `version.json` — `versionCode`, `versionName`, `minVersionCode`, URL del APK, `sha256` y notas.
- Los APK se publican aquí con el nombre `fanuno-<versionName>.apk`.

El script `scripts/publish_sideload.sh` del repositorio de FanUno genera `fanuno-<versionName>.apk` y `version.json` en `dist/fanuno/`. Copia el contenido de esa carpeta a esta ruta (`fanuno/`) y publica el cambio para que la app y esta página detecten la nueva versión.

`versionCode: 0` o `apkUrl` vacío significa que todavía no hay una build publicada: la página muestra «Próximamente» y la app no debe tratarlo como una actualización.
