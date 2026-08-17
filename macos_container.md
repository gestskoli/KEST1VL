# Ubuntu á MacOS

## Setja upp `brew`

Keyrðu eftirfarandi línu í **terminal**.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Setja upp `container``

Keyrðu eftirfarandi í **terminal**

```bash
brew install --cask container
```

## Keyra `container`

Keyrðu eftirfarandi í **terminal**

```bash
container system start
```

Þetta getur tekið einhverjar mínútur að keyra. 

Smelltu síðan á `y` þegar `Install the recommended default kernel from ...` birtist.

Hinkraðu svo aftur í nokkrar mínútur.

Ef þú færð villu, prófaðu þá að keyra `container system start` aftur.

## Sækja Ubuntu

Keyrðu eftirfarandi í **terminal**

```bash
container image pull ubuntu
```
