# NES Player

App Android (Capacitor) para jugar ROMs de NES con EmulatorJS.

## Cargar una ROM automáticamente

Coloca tu archivo en `www/rom/game.nes` antes de compilar. Si existe, la app la carga al abrir.
No subas ROMs con derechos de autor a un repositorio público.

## Compilar el APK

El workflow de GitHub Actions (`.github/workflows/build-apk.yml`) compila el APK.
Descárgalo desde la pestaña Actions > último build > Artifacts.

Local:

    npm install
    npx cap add android
    npx @capacitor/assets generate --android
    npx cap sync android
    cd android && ./gradlew assembleDebug
