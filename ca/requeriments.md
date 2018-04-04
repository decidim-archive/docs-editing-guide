# Requeriments de programari

1. Gestor de paquets
2. [Git](https://git-scm.com/)
3. [GitBook Editor](https://www.gitbook.com/editor)

## Instal·lació

A continuació trobareu instruccions de com instal·lar el programari necessari
en els operatius [Ubuntu 14.04+](#ubuntu), [macOS 10.10+](#macos) i [Windows 10 64-bits](#windows).

### Ubuntu

#### Gestor de paquets apt
Farem servir el gestor de paquets del sistema per a instal·lar el programari necessari.

#### Git
Obrim un terminal i executem la comanda

```bash
$ sudo apt install git
```

#### GitBook Editor
[Descarreguem](https://www.gitbook.com/editor/linux-64-bit/download) el paquet `.deb` i hi fem doble clic per instal·lar l'editor.

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
$ git --version
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

#### Gestor de paquets

Preparem el sistema instal·lant el *Subsistema de Windows per Linux*:

1. Cerquem l'aplicació *PowerShell* en la caixa de cerca del sistema.
2. Fem clic amb el botó dret sobre el resultat *Windows PowerShell (x86)* i *Executem com a administrador*.
3. Permetem que l'aplicació faci canvis en el dispositiu responent afirmativament.
4. En el terminal obert escrivim la comanda següent i fem `Enter`
```
PS C:\WINDOWS\system32> Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```
5. Reiniciem quan el sistema ens ho demani.

A continuació comprovem quin és el *Build number* del nostre *Windows 10* seguint les instruccions
següents:

1. Obrim la *Configuració de Windows*.
2. Seleccionem la opció *Sistema*.
3. Fem clic a la opció *Acerca de*.
4. Ens desplacem a la secció *Especificacions de Windows* i ens fixem en el valor *Compilació del sistema operatiu*.

Si el valor és igual o més gran que 16215 seguim les passes següents:

1. Obrim el *Microsoft Store*.
2. Escrivim *Ubuntu* a la caixa de cerca i seleccionem l'aplicació.
3. L'instal·lem fent clic al botó *Obtenir*.
4. Un cop descarregat, procedim a la instal·lació fent clic al botó *Iniciar*.
5. Un cop instal·lat, crearem un compte d'usuària proporcionant un nom i una contrasenya.

En cas que el valor sigui inferior a 16215, seguim les instruccions de l'enllaç següent: [Install using lxrun](https://docs.microsoft.com/en-us/windows/wsl/install-win10#for-anniversary-update-and-creators-update-install-using-lxrun)

#### Git
[Descarreguem](https://git-scm.com/download/win) l'instal·lador `.exe` i hi fem doble clic per procedir a la instal·lació,
acceptant totes les opcions per defecte que ens apareixen.

#### GitBook Editor
La darrera versió d'aquest editor no és compatible amb *Windows 10*. Alternativament podeu fer servir [Visual Studio Code](https://code.visualstudio.com/) com a editor de text. Llegiu les seccions [3. Requeriments (Power Writer)](requeriments-power-writer.md) i [7. Flux de treball (Power Writer)](flux-power-writer.md) per aprendre a instal·lar-lo i fer-lo servir.


## Enllaços

- Homebrew https://brew.sh/
- Homebrew-Cask https://caskroom.github.io/
- Windows Subsystem for Linux https://docs.microsoft.com/en-us/windows/wsl/about
- Git https://git-scm.com/
- GitBook Editor https://www.gitbook.com/editor
- Visual Studio Code https://code.visualstudio.com/