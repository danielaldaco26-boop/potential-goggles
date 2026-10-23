# 🔥Musica🔥 — reproductor local Android

Proyecto Kotlin + Jetpack Compose para reproducir archivos de audio locales sin conexión a Internet.

## Funciones incluidas
- Biblioteca local consultada mediante MediaStore.
- Búsqueda por título y artista.
- Carátulas de álbum desde el proveedor multimedia local del teléfono, con icono alternativo si no existe carátula.
- Controles de reproducción, anterior/siguiente, progreso, aleatorio y repetición.
- Listas de reproducción guardadas localmente en SharedPreferences; permiten crear, reproducir y eliminar listas.
- Reproducción en segundo plano mediante Media3 `MediaSessionService`, con integración de controles multimedia del sistema y notificación de reproducción.
- El manifiesto no declara permiso `INTERNET`; no se conectan servicios de streaming.

## Compilar
1. Instala Android Studio desde https://developer.android.com/studio.
2. Descomprime este archivo ZIP.
3. En Android Studio, abre la carpeta raíz que contiene `settings.gradle.kts`.
4. Espera a que termine la sincronización de Gradle (la primera vez puede requerir Internet para descargar dependencias).
5. Selecciona **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. El APK de depuración normalmente se guarda en `app/build/outputs/apk/debug/app-debug.apk`.

## Permisos
La app solicita permiso para leer audio local. En Android 13 o posterior utiliza `READ_MEDIA_AUDIO`; en versiones anteriores utiliza `READ_EXTERNAL_STORAGE`.

## Notas de verificación
El código fuente se ha actualizado, pero en este entorno no está disponible la cadena de herramientas Android/Gradle para compilarlo ni probarlo en un dispositivo. La compilación y la reproducción real deben verificarse en Android Studio. La primera sincronización necesita conexión para descargar las dependencias; la reproducción de archivos locales no requiere Internet.
