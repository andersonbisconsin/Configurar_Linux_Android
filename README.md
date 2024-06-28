# Configurar_Linux_Android
Script para configurar ambiente de desenvolvimento Android após instalar o Linux Elementary

Use o comando 'gedit ~/.profile' para alterar o arquivo e após salvar o comando 'source ~/.profile'.

# Android Studio e Flutter SDK
if [ -d "$HOME/Android" ] ; then
    ANDROID_HOME="$HOME/Android/Sdk"
fi

if [ -d "$HOME/flutter" ] ; then
    FLUTTER_ROOT="$HOME/flutter"
fi

if [ -d "$FLUTTER_ROOT/bin/cache/dart-sdk" ] ; then
    DART_SDK="$FLUTTER_ROOT/bin/cache/dart-sdk"
fi

if [ -d "$FLUTTER_ROOT/bin" ] ; then
    FLUTTER_BIN="$FLUTTER_ROOT/bin"
fi

if [ -d "$HOME/.jdks/openjdk-22.0.1" ] ; then
    JAVA_HOME="$HOME/.jdks/openjdk-22.0.1"
fi

if [ -d "$FLUTTER_BIN" ] ; then
    PATH="$FLUTTER_BIN:$PATH"
fi

if [ -d "$JAVA_HOME/bin" ] ; then
    PATH="$JAVA_HOME/bin:$PATH"
fi