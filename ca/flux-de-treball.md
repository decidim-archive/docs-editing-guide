# Flux de treball

## Format i estructura del document

Abans de poder publicar un document cal que aquest tingui el format i l'estructura adequats.

Sigui quin sigui el seu format original el document només podrà ser publicat si disposem d'una còpia en format [Markdown](https://www.markdownguide.org/), per tant, caldrà convertir el document de treball a aquest format.

Un cop feta la conversió caldrà fragmentar el document, generant un document nou per cada capítol o secció de que consti l'original. Preneu aquesta mateixa guia com a exemple i observeu com es dona estructura al document en el fitxer [SUMMARY](https://raw.githubusercontent.com/decidim/docs-editing-guide/master/ca/SUMMARY.md).

Finalment, podreu publicar el document seguint les indicacions de la secció *Flux de treball* corresponent al vostre rol.


## Conversió del format del document

L'eina recomanada per convertir el document original i per donar-li l'estructura desitjada és [Typora](https://typora.io/). *Typora* és un editor que permet importar fitxers en format *MS Word* per editar-los com a documents *Markdown*. Tot i que el procediment per fer-ho surt de l'abast d'aquesta guia podeu [llegir la seva documentació](http://support.typora.io/Install-and-Use-Pandoc/) per conèixer els detalls.

A continuació trobareu instruccions de com instal·lar *Typora*
en els operatius [Ubuntu 14.04+](#ubuntu), [macOS 10.10+](#macos) i [Windows 10 64-bits](#windows).

### Ubuntu
Obrim un terminal i instal·lem l'editor executant una a una les comandes següents:

```bash
# 1. Instal·lem Pandoc
sudo apt install pandoc

# 2. Afegim la clau criptogràfica dels desenvolupadors de Typora
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys BA300B7755AFCFAE

# 3. Afegim el repositori de Typora a la llista de fonts de programari de confiança
echo 'deb https://typora.io linux/' | sudo tee /etc/apt/sources.list.d/typora.list

# 4. Instal·lem Typora
sudo apt update
sudo apt install typora
```

### macOS
Obrim un terminal i instal·lem l'editor executant una a una les comandes següents:

```bash
# 1. Instal·lem Pandoc
brew install pandoc

# 2. Instal·lem typora
brew cask install typora
```

### Windows
[Descarreguem](https://github.com/jgm/pandoc/releases/latest) l'instal·lador `.msi` i hi fem doble clic per instal·lar *Pandoc*,
acceptant totes les opcions per defecte que ens apareixen.

A continuació [descarreguem](https://typora.io/#windows) l'instal·lador `.exe` de *Typora* i hi fem doble clic per instal·lar l'editor,
acceptant totes les opcions per defecte que ens apareixen.


## Enllaços

- Markdown Guide https://www.markdownguide.org/
- Mastering Markdown https://masteringmarkdown.com/
- Typora https://typora.io/
- Pandoc https://pandoc.org/
- Install and Use Pandoc http://support.typora.io/Install-and-Use-Pandoc/
- Installing pandoc https://pandoc.org/installing.html