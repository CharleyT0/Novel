# NovelaVoz (Android nativo)

Proyecto Kotlin/Android (minSdk 26). **No se ha compilado ni probado en un dispositivo en este entorno.**

## Funciones
- Navegador HTTPS integrado y extracción heurística de capítulos.
- Traducción al español mediante MyMemory, con límites del servicio gratuito.
- Narración con Android TextToSpeech mediante servicio foreground de tipo mediaPlayback; controles en notificación.
- Velocidad de narración, pausa y continuación aproximada por fragmentos.
- Biblioteca privada con originales y traducciones guardadas para escuchar sin conexión.
- Detección heurística de enlace «siguiente capítulo» y avance automático experimental tras terminar la narración.

## Limitaciones importantes
- Algunas páginas bloquean extracción, requieren sesión o cargan texto de forma incompatible. No se eluden bloqueos de acceso ni DRM.
- La traducción necesita internet; MyMemory puede limitar o rechazar capítulos largos. No garantiza calidad literaria ni idioma automático.
- La detección del siguiente capítulo depende de los enlaces y la carga de cada sitio. No garantiza avance automático.
- La reproducción puede interrumpirse por las restricciones de batería del fabricante o si falta la voz TTS española.
- La biblioteca guarda texto en almacenamiento privado de la aplicación, no genera archivos MP3.
- No se ha verificado compilación ni ejecución; pueden necesitarse ajustes de SDK/Gradle.

## Compilar
1. Instalar Android Studio y Android SDK 35 con JDK 17.
2. Abrir la carpeta `NovelaVoz` como proyecto Android.
3. Sincronizar Gradle y ejecutar `Build > Build APK(s)`.
4. El APK de depuración estará en `app/build/outputs/apk/debug/`.

## Compilación en GitHub Actions
Se incluye `.github/workflows/android.yml`. Subir el proyecto a un repositorio de GitHub, ir a Actions y ejecutar `Android APK`; descargar el artefacto `NovelaVoz-debug-apk`.
