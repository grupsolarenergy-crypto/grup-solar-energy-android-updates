# Actualizaciones Android de GRUP SOLAR ENERGY EIRL

La aplicación de PC publica una APK firmada y su `android.json` en un lanzamiento estable de este repositorio. Al publicarse el lanzamiento, GitHub Actions actualiza automáticamente el manifiesto de GitHub Pages; no hay que editar versiones en Netlify.

- Manifiesto permanente: https://grupsolarenergy-crypto.github.io/grup-solar-energy-android-updates/android.json
- Dirección que siguen consultando los teléfonos: https://grup-solar-energy-peru.netlify.app/updates/android/android.json
- Automatización: `.github/workflows/publicar-android-json.yml`.
- Validación de versión, ruta y SHA-256: `.github/scripts/build-android-manifest.mjs`.

GitHub Pages debe usar **GitHub Actions** como fuente. Para volver a publicar el último manifiesto, abre Actions → Publicar actualizaciones Android → Run workflow en `main`.

Solo se publica el manifiesto en Pages. Las APK siguen alojadas en GitHub Releases y descargándose por la ruta de Netlify. Los borradores y las versiones de prueba no actualizan el manifiesto. Cada APK nueva debe tener una versión y un versionCode mayores, tal como ya valida el centro de actualizaciones de PC.

La web necesita este ajuste una sola vez:

```
/updates/android/android.json  https://grupsolarenergy-crypto.github.io/grup-solar-energy-android-updates/android.json  200!
/updates/android/*  https://github.com/grupsolarenergy-crypto/grup-solar-energy-android-updates/releases/latest/download/:splat  302!
```

Se mantienen las reglas de Windows y el sistema de actualizaciones de PC.
