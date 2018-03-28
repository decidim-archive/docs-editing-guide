# Requeriments de programari

1. Gestor de paquets (macOS: https://brew.sh/, https://caskroom.github.io/ | Windows: https://chocolatey.org/)
2. Git (https://git-scm.com/)
3. GitBook Editor (https://www.gitbook.com/editor)

## Instal·lació

A continuació trobareu instruccions de com instal·lar el programari necessari
en els operatius [Ubuntu](#ubuntu), [macOS](#macos) i [Windows](#windows).

### Ubuntu

#### Gestor de paquets apt
Farem servir el gestor de paquets del sistema per a instal·lar el programari necessari.

#### Git
Obrim un terminal i executem la comanda

```bash
$ sudo apt install git
```

#### GitBook Editor
[Descarreguem](https://www.gitbook.com/editor/linux-64-bit/download) el paquet .deb i hi fem doble clic per instal·lar l'editor.

### macOS

#### Gestor de paquets Homebrew
Obrim un terminal i executem les comandes

```bash
# 1. Instal·lem Xcode Command Line Tools
$ xcode-select --install

# 2. Instal·lem Homebrew
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# 3. Instal·lem Homebrew-Cask
$ brew tap caskroom/cask
```

#### Git
Comprovem que el tenim instal·lat en el sistema amb la comanda

```bash
$ git -v
```

Si el terminal no ens mostra la versió instal·lada, procedirem a la instal·lació amb la comanda

```bash
$ brew install git
```

#### GitBook Editor
Instal·lem l'editor amb la comanda

```bash
$ brew cask install gitbook-editor
```

### Windows
TODO
