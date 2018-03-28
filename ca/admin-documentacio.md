# Flux de treball (Doc Admin)

### Preparació d'un nou repositori de documentació

Per tal de poder publicar un nou document, cal obrir un terminal i seguir les passes que describim a continuació:

1. Create a brand new document repo in GitHub. Follow the pattern **docs-slug** to name it

2. Clone **decidim/docs-template** repo
```bash
$ git clone git@github.com:decidim/docs-template.git docs-slug
```

3. Change to document directory and install dependencies
```bash
$ cd docs-slug
$ npm install
```

4. Change remotes
```bash
$ git remote set-url origin git@github.com:decidim/docs-slug.git
```

5. Update the repo README file and commit changes
```bash
$ git ci -am "Update README file"
```

6. Update *package.json* file and commit changes
```bash
$ sed -i s/SLUG/slug/g ./package.json
$ git ci -am "Update document slug in package.json file"
```

7. Update *book.json* file and commit changes
```bash
$ sed -i s/SLUG/slug/g ./book.json
$ git ci -am "Update document slug in book.json file"
```

8. Update *_redirects* file and commit changes
```bash
$ sed -i s/SLUG/slug/g ./_redirects
$ git ci -am "Update document slug in _redirects file"
```

9. Push changes to the document repo master branch
```bash
$ git push -u origin master
```

10. Update document metadata in `/{ca,en,es}/book.json` files and commit changes from GitHub

11. Add *decidim* and *decidim-docs* topics to the GitHub document repo

12. Configure settings of the document repo in GitHub (take *docs-template* repo settings as example)

13. Deploy the document site in Netlify

  1. New Site from Git
  2. Connect to GitHub provider
  3. Pick the document repo from the list
  4. Set build options and deploy
      * Branch to deploy: `master`
      * Build command: `npm run build`
      * Publish directory: `_book`

14. Customize the document site settings in Netlify

  1. Change site name to decidim-slug
  2. Enable asset optimization
  3. Visit the brand new document site in https://decidim-slug.netlify.com/slug/

15. Add a new entry in [docs.yml](https://github.com/decidim/docs.decidim.org/blob/master/_data/docs.yml) file
from *decidim/docs.decidim.org* repo and commit changes

```yaml
- title: slug
  path: /slug
  langs: ["ca", "en", "es"]
  url: "https://decidim-slug.netlify.com"
```

Visit the brand new document site in https://docs.decidim.org/slug/


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
$ ssh-keygen -t rsa -b 4096 -C "jane.doe@mail.com"

# 2. Iniciem el ssh-agent, responsable de gestionar les claus
$ eval "$(ssh-agent -s)"

# 3. Afegim la clau SSH al ssh-agent
$ ssh-add ~/.ssh/id_rsa

# 4. Afegim la clau SSH al nostre compte de GitHub
# https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/

# 5. Verifiquem que podem establir una connexió segura amb GitHub.
# A la pregunta de si confiem en el host de destí respondrem que sí.
$ ssh -T git@github.com
```
