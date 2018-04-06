# Flux de treball (Doc Admin)

### Preparació d'un nou repositori de documentació

Per tal de poder publicar un nou document, cal obrir un terminal i seguir les passes que describim a continuació:

1. Creem un nou repositori per al document a *GitHub*. Seguim el patró **docs-slug** per donar-li nom.

2. Clonem el repositori **decidim/docs-template**.
```bash
git clone git@github.com:decidim/docs-template.git docs-slug
```

3. Ens situem al directori del document i instal·lem les dependències.
```bash
cd docs-slug
npm install
```

4. Actualitzem els *remots*.
```bash
git remote set-url origin git@github.com:decidim/docs-slug.git
```

5. Actualitzem el fitxer *README* del repositori i fem *commit* dels canvis.
```bash
git commit -am "Update README file"
```

6. Actualitzem el fitxer *package.json* i fem *commit* dels canvis.
```bash
sed -i s/SLUG/slug/g ./package.json
git commit -am "Update document slug in package.json file"
```

7. Actualitzem el fitxer *book.json* i fem *commit* dels canvis.
```bash
sed -i s/SLUG/slug/g ./book.json
git commit -am "Update document slug in book.json file"
```

8. Actualitzem el fitxer *_redirects* i fem *commit* dels canvis.
```bash
sed -i s/SLUG/slug/g ./_redirects
git commit -am "Update document slug in _redirects file"
```

9. Publiquem els canvis a la branca *master* del repositori del document.
```bash
git push -u origin master
```

10. Actualitzem les metadades del document als fitxers `/{ca,en,es}/book.json` i fem *commit* dels canvis directament des de *GitHub*.

11. A *GitHub* afegim els [topics](https://help.github.com/articles/about-topics/) *decidim* i *decidim-docs* al repositori del document.

12. Configurem els *settings* del repositori del document a *GitHub* (prenem la configuració del repositori [decidim/docs-template](https://github.com/decidim/docs-template) com a exemple). En particular, donem permisos d'escriptura al team *docs* sobre el repositori.

13. Despleguem la versió online del document a *Netlify*:

  1. New Site from Git
  2. Connect to GitHub provider
  3. Pick the document repo from the list
  4. Set build options and deploy
      * Branch to deploy: `master`
      * Build command: `npm run build`
      * Publish directory: `_book`

14. Ajustem els *Site settings* del document a *Netlify*:

  1. Change site name to *decidim-slug*
  2. Enable asset optimization
  3. Visit the brand new document site in https://decidim-slug.netlify.com/slug/

15. Afegim una nova entrada al fitxer [docs.yml](https://github.com/decidim/docs.decidim.org/blob/master/_data/docs.yml) del repositori *decidim/docs.decidim.org* i fem *commit* dels canvis:

```yaml
- title: slug
  path: /slug
  langs: ["ca", "en", "es"]
  url: "https://decidim-slug.netlify.com"
```

En aquest punt la nova versió online del document és accessible a l'adreça https://docs.decidim.org/slug/.


### Connexió segura a GitHub

Atès que l'**Administradora de documentació** haurà de treballar amb GitHub de forma habitual
per preparar els repositoris que allotjaran els documents del projecte, convé configurar
la [connexió a GitHub fent ús de certificat SSH](https://help.github.com/articles/connecting-to-github-with-ssh/)
per tal d'evitar haver d'introduir credencials a cada operació.

En un terminal executem les comandes següents:
```bash
# 1. Si no en tenim, generem una nova clau SSH.
# Quan ens ho demani acceptem el nom del fitxer suggerit
# i introduïm la clau de pas de seguretat.
ssh-keygen -t rsa -b 4096 -C "jane.doe@mail.com"

# 2. Iniciem el ssh-agent, responsable de gestionar les claus
eval "$(ssh-agent -s)"

# 3. Afegim la clau SSH al ssh-agent
ssh-add ~/.ssh/id_rsa

# 4. Afegim la clau SSH al nostre compte de GitHub
# https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/

# 5. Verifiquem que podem establir una connexió segura amb GitHub.
# A la pregunta de si confiem en el host de destí respondrem que sí.
ssh -T git@github.com
```


## Enllaços

- Generating eBooks and PDFs https://toolchain.gitbook.com/ebook.html
- GitHub https://github.com/
- About topics https://help.github.com/articles/about-topics/
- Connecting to GitHub with SSH https://help.github.com/articles/connecting-to-github-with-ssh/
- Netlify https://www.netlify.com/
