# qa.poc-maestro-mobile-test.YAML

POC do framework de testes mobile [MAESTRO](https://maestro.mobile.dev/)

Framework desenvolvido em kotlin e shell

## Instalação

1. Execute `brew tap mobile-dev-inc/tap`
2. Execute `brew install maestro`

## Connecting to Your Device

### Android

O `maestro test` detectará e usará automaticamente qualquer emulador local ou dispositivo físico conectado por USB.

### IOS

Antes de executar o Flows no IOS, instale a ferramenta [FACEBOOK IDB](https://fbidb.io/)

```
brew tap facebook/fb
brew install facebook/fb/idb-companion
```

E lança-lo

```
idb_companion --udid {id of the iOS device}
```

**Exemplo:** idb_companion --udid 64988326-2838-4AB9-96CC-4F767A26E394

**Dica:** você pode encontrar o ID do seu dispositivo usando `xcrun simctl list` [link](https://medium.com/xcblog/simctl-control-ios-simulators-from-command-line-78b9006a20dc)

**Nota:** No momento, o Maestro não suporta dispositivos iOS reais.

## Extrair apps exemplo

**Download:** https://storage.googleapis.com/mobile.dev/samples/samples.zip 

### IOS

```
cd ./samples
unzip samples.zip
xcrun simctl install Booted Wikipedia.app
maestro test ios-flow.yaml
```

### Android

```
cd ./samples
adb install sample.apk
maestro test android-flow.yaml
```

## Executar testes

**Obs.:** Instalar o yarn antes de rodar os comandos abaixo.

`yarn test-ios` or `yarn test-android`

POC em construção a medida que o maestro vai evoluindo.