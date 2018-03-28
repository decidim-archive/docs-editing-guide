# Requeriments de programari (Doc Admin)

A més dels requeriments de programari que ja hem vist, l'**Administradora de documentació** necessita satisfer
un requeriment addicional: [Node.js](https://nodejs.org/en/).


## Instal·lació

A continuació trobareu instruccions de com instal·lar el gestor de versions de Node.js *[n](https://github.com/mklement0/n-install)*
en els operatius [Ubuntu](#ubuntu) i [macOS](#macos). El procés d'instal·lació de *n* també inclou la instal·lació de la darrera versió
LTS de Node.js.

### Ubuntu
Obrim un terminal i executem les comandes

```bash
# 1. Instal·lem les dependències
$ sudo apt install curl

# 2. Instal·lem n
$ curl -L https://git.io/n-install | N_PREFIX=~/.n bash -s -- -y
$ source ~/.bashrc
```

### macOS
Obrim un terminal i executem les comandes

```bash
$ curl -L https://git.io/n-install | N_PREFIX=~/.n bash -s -- -n
$ echo 'export N_PREFIX="$HOME/.n"; [[ :$PATH: == *":$N_PREFIX/bin:"* ]] || PATH+=":$N_PREFIX/bin"' >> ~/.bash_profile
$ source ~/.bash_profile
```
