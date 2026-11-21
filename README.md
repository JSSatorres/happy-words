# Happy Words

Juego mínimo de vocabulario en inglés para niños (Android). 20 palabras con emojis, 3 opciones por ronda,
10 rondas, pronunciación con el TextToSpeech del móvil. Sin permisos, sin internet, sin dependencias.

- Código Android: `app/src/main/java/com/satorus/happywords/MainActivity.java` (WebView + TTS)
- Juego: `app/src/main/assets/index.html`
- Material de la ficha: `store/`

## Compilar
```
./gradlew bundleRelease      # -> app/build/outputs/bundle/release/app-release.aab (lo que se sube a Play)
./gradlew assembleRelease    # -> APK para instalar a mano en un móvil (adb install)
```
Para una nueva versión, sube `versionCode` (y `versionName`) en `app/build.gradle`.

## Firma (¡IMPORTANTE!)
`upload-key.jks` + `keystore.properties` son la clave de subida. Haz copia de los dos (p. ej. en KeePassXC).
No se suben a git (.gitignore). En Play usa "Firma de apps de Google Play" (por defecto): si pierdes
la clave de subida se puede resetear desde la consola, pero mejor no perderla.
