# helloworld-snapcraft

## Create snap

    snapcraft snap --output codemagic-snapcraft-example.snap

## Clean

    snapcraft clean codemagic-snapcraft-example -s pull

## Install (without codesigning)

    sudo snap install codemagic-snapcraft-example.snap --dangerous

## Login

    snapcraft export-login snapcraft-login-credentials

Will create a file `snapcraft-login-credentials`. To login in CI/CD environment use

    snapcraft login --with snapcraft-login-credentials

## Publish

    snapcraft register codemagic-snapcraft-example # if not already
    snapcraft push codemagic-snapcraft-example.snap
    snapcraft release codemagic-snapcraft-example revision-number channel
    
 
Channels: `stable`, `candidate`, `beta`, and `edge`

## Install from snapcraft

    sudo snap install codemagic-snapcraft-example

## Uninstall

    sudo snap remove codemagic-snapcraft-example

# Install snapcraft on macOS

    brew install --cask multipass
    brew install snapcraft

Doesn't provide ability to download from snapcraft
