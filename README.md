# Instalación de React Native CLI en Ubuntu
Este tutorial se debe seguir junto con la documentación oficial, cree este documento con el fin de poder ayudarlos, ya que a mi la documentación no me ayudo al 100% y esta guía junto con la documentación les sera útil, les dejo la [documentación oficial](https://reactnative.dev/docs/next/environment-setup).
## Instalar JDK

```console
sudo apt-get install openjdk-11-jdk
```

## Instalar Android Studio
[Descargamos Android Studio](https://developer.android.com/studio), e [instalamos](https://developer.android.com/studio/install#linux). Una vez hecho esto abrimos Android Studio y vamos a **Projects > More Actions > SDK Manager**.

Seleccione la pestaña "SDK Platforms" dentro del SDK Manager, luego marque la casilla junto a "Show Package Details" en la esquina inferior derecha. Busque y expanda la entrada Android 11 (R), luego asegúrese de que los siguientes elementos estén marcados:

* `Android SDK Platform 30`
* `Intel x86 Atom_64 System Image` o `Google APIs Intel x86 Atom System Image`

## Configuración de las variable de entorno

Las herramientas React Native requieren que se configuren algunas variables de entorno para crear aplicaciones con código nativo.

Agregue las siguientes líneas a su archivo de configuración $HOME/.bash_profile o $HOME/.bashrc (si está usando zsh entonces ~/.zprofile o ~/.zshrc).

```javascript
export ANDROID_SDK_ROOT=$HOME/Library/Android/Sdk
export PATH=$PATH:$ANDROID_SDK_ROOT/emulator
export PATH=$PATH:$ANDROID_SDK_ROOT/platform-tools
```

Si no funciona pruebe con: 

```javascript
export ANDROID_SDK_ROOT=$HOME/Android/Sdk
export PATH=$PATH:$ANDROID_SDK_ROOT/emulator
export PATH=$PATH:$ANDROID_SDK_ROOT/platform-tools
```

## Watchman
https://facebook.github.io/watchman/docs/install.html