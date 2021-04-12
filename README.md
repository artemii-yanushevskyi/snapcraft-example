# helloworld-snapcraft

## Create snap

    snapcraft snap --output codemagic-example.snap

## Clean

    snapcraft clean codemagic-example -s pull

## Install (without codesigning)

    sudo snap install codemagic-example.snap --dangerous

## Login

    snapcraft export-login snapcraft-login-credentials

Will create a file `snapcraft-login-credentials`. To login in CI/CD environment use

    snapcraft login --with snapcraft-login-credentials

## Publish

    snapcraft register codemagic-example # if not already
    snapcraft upload codemagic-example.snap
    snapcraft release codemagic-example revision-number channel
    
 
Channels: `stable`, `candidate`, `beta`, and `edge`

## Install from snapcraft

    sudo snap install codemagic-example

## Uninstall

    sudo snap remove codemagic-example

# Install snapcraft on macOS

    brew install --cask multipass
    brew install snapcraft

Doesn't provide ability to download from snapcraft
