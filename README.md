# NativeScript-Vue Application
## Attention à l'url dans la balise webview !

> A native application built with NativeScript-Vue

## Usage

``` bash
# Install dependencies
npm install

# Preview on device
tns preview

# Build, watch for changes and run the application
tns run

# Build, watch for changes on emulator
tns run ios
tns run android

# Build, watch for changes and debug the application
tns debug <platform>

# Build for production
tns build <platform> --env.production

```
## État actuel de l'application mobile

Mise en place des notifications push, avec firebase, impossible. Erreurs lors du build avec `tns run ios` :

` Module not found: Error: Can't resolve 'tns-core-modules/... `

![Alt text](error.png?raw=true "Erreur")

## Guide suivi

NativeScript Firebase plugin : 
> https://github.com/EddyVerbruggen/nativescript-plugin-firebase
