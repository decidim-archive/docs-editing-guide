# Configuració

### Git

En un terminal executem les comandes següents:

```bash
# 1. Definim quin nom farem servir per identificar les nostres contribucions
git config --global user.name "Jane Doe"

# 2. Definim una adreça de correu associada al nostre nom d'usuària
git config --global user.email "jane.doe@mail.com"
```

### GitHub

Per tal de fer contribucions a la documentació del projecte primer hem de ser usuàries de [GitHub](https://github.com/):

1. [Obrim un compte](https://help.github.com/articles/signing-up-for-a-new-github-account/) a *GitHub*. Fem servir la mateixa adreça d'email que hem definit a la configuració de *Git*.
2. [Verifiquem](https://help.github.com/articles/verifying-your-email-address/) la nostra adreça de correu principal.

Arribats a aquest punt podrem començar a fer contribucions a la documentació del projecte.

### Visual Studio Code

Si hem optat per *Visual Studio Code* per a editar continguts és recomanable instal·lar l'extensió [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one):

1. Obrim *Visual Studio Code*.
2. Obrim el *Quick Open* amb la combinació *Ctrl+P*
3. Escrivim la comanda `ext install yzhang.markdown-all-in-one` i fem `Enter`.

En endavant, quan volguem **previsualitzar el nostre document *markdown*** només caldrà que obrim el previsualitzador seguint les passes següents:

1. Obrim la caixa de comandes amb la combinació *Ctrl+Shift+P*
2. Escrivim la comanda `Markdown: Open Preview to the Side`.

Finalment, **si som usuàries de *Windows 10***, cal que configurem el terminal integrat de l'editor seguint les passes següents:

1. Obrim les preferències de l'editor amb la combinació *Ctrl+,*
2. Afegim a la *Configuració d'usuari* del panell dret la línia
```json
{
    "terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",
}
```

D'aquesta manera, quan calgui accedir a un terminal podrem obrir el terminal integrat amb la combinació *Ctrl+ñ*


## Enllaços

- GitHub https://github.com/
- Signing up for a new GitHub account https://help.github.com/articles/signing-up-for-a-new-github-account/
- Verifying your email address https://help.github.com/articles/verifying-your-email-address/
- Visual Studio Code https://code.visualstudio.com/
- User and Workspace Settings https://code.visualstudio.com/docs/getstarted/settings
- Integrated Terminal https://code.visualstudio.com/docs/editor/integrated-terminal
