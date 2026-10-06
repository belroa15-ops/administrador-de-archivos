# Administrador De Archivos (Android)

## Lo que necesitas (en tu computadora)
1. Node.js (nodejs.org)
2. Android Studio (developer.android.com/studio)

## Pasos
En una terminal, dentro de esta carpeta:

    npm install
    npx cap add android

1. Abre `PERMISOS_AndroidManifest.txt` y pega lo que dice en `android/app/src/main/AndroidManifest.xml`.
2. Luego ejecuta:

       npx cap sync
       npx cap open android

3. En Android Studio espera a que termine Gradle y pulsa **Build > Build APK(s)**.
4. Instala el APK en tu teléfono (permite "instalar apps de origen desconocido").

## Primer uso
- Al abrir la app aparece la pantalla de bienvenida: **Conceder permisos**.
- Android 11 o superior: si no aparecen todos tus archivos, ve a **Ajustes > Apps > Administrador De Archivos > Permisos > Archivos y multimedia (Acceso a todos los archivos)** y actívalo. Luego pulsa **Escanear dispositivo**.
- Cada persona ve solo sus propios archivos. Nada se envía a internet.

## Cuando cambies el diseño
Edita `www/index.html`, luego `npx cap sync` y vuelve a compilar.

## Importante
- Eliminar para siempre / Vaciar papelera borra el archivo real del teléfono.
- La "Carpeta segura" oculta archivos dentro de la app; no los cifra.
- Google Play restringe el permiso de "todos los archivos". Para uso personal o compartir el APK directo no hay problema.
- Icono de la app: en Android Studio, clic derecho en `res` > New > Image Asset.

## Opción sin instalar nada: crear el APK en la nube (GitHub)
1. Crea una cuenta gratis en github.com y un repositorio nuevo.
2. Sube TODO el contenido de esta carpeta (incluida la carpeta oculta `.github`).
3. Ve a la pestaña **Actions**, abre **Crear APK** y pulsa **Run workflow**.
4. Espera unos 5 a 10 minutos. Entra a la ejecución terminada y descarga **Administrador-De-Archivos-APK** (abajo, en Artifacts).
5. Descomprime ese archivo y te queda `app-debug.apk` para instalar en tu teléfono.
