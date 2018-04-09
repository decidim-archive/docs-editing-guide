# Requeriments de programari

Totes les persones implicades en la producció i publicació de documentació hauran de satisfer els requeriments generals de programari que llistem a continuació. Addicionalment, i segons el rol que exerceixin, caldrà que facin ús de les eines descrites en les seccions corresponents.

1. Gestor de paquets
2. [Git](https://git-scm.com/)

## Instal·lació

A continuació trobareu instruccions de com instal·lar el programari necessari
en els operatius [Ubuntu 14.04+](#ubuntu), [macOS 10.10+](#macos) i [Windows 10 64-bits](#windows).

### Ubuntu

#### Gestor de paquets apt
Farem servir el gestor de paquets del sistema per a instal·lar el programari necessari.

#### Git
Obrim un terminal i executem la comanda

```bash
sudo apt install git
```

### macOS

#### Gestor de paquets Homebrew
Obrim un terminal i executem les comandes

```bash
# 1. Instal·lem Xcode Command Line Tools
xcode-select --install

# 2. Instal·lem Homebrew
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# 3. Instal·lem Homebrew-Cask
brew tap caskroom/cask
```

#### Git
Comprovem que el tenim instal·lat en el sistema amb la comanda

```bash
git --version
```

Si el terminal no ens mostra la versió instal·lada, procedirem a la instal·lació amb la comanda

```bash
brew install git
```

### Windows

#### Gestor de paquets
Enlloc de fer servir un gestor de paquets instal·larem els requeriments de programari de la forma habitual.

#### Git
[Descarreguem](https://git-scm.com/download/win) l'instal·lador `.exe` i hi fem doble clic per procedir a la instal·lació,
acceptant totes les opcions per defecte que ens apareixen. La instal·lació de *Git* inclou *Git Bash* com a interfície de línia de comandes.
En endavant, **quan calgui obrir un terminal obrirem Git Bash** per executar les comandes indicades.


## Enllaços

- Homebrew https://brew.sh/
- Homebrew-Cask https://caskroom.github.io/
- Git https://git-scm.com/
