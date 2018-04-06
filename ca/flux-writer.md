# Flux de treball

### Preparació de l'entorn de treball

El primer cop que treballem amb *GitBook Editor* cal que preparem l'espai de treball que acollirà els documents
sobre els que farem les nostres contribucions. Obrim un terminal i executem la comanda següent:

```bash
mkdir -p GitBook/Library/Imports
```

A continuació demanarem a l'**Administradora de documentació** que ens afegeixi al grup de redactores de documentació (equip *docs*) a *GitHub*.

### Contribució a un document nou

Si volem afegir un document nou a la documentació del projecte haurem de demanar a l'**Administradora de documentació**
que prepari el repositori que l'allotjarà a *GitHub*.

Un cop l'**Administradora de documentació** ens doni el vist i plau podrem fer les nostres contribucions seguint les indicacions
de la secció següent.

### Contribució a un document ja existent

Si és el primer cop que fem una contribució al document cal que preparem l'entorn de treball seguint les instruccions següents:

1. En un terminal ens situem al directori que ha d'allotjar el document.
```bash
cd && cd GitBook/Library/Imports
```

2. [Clonem el repositori](https://help.github.com/articles/cloning-a-repository/) del document al que volem afegir la nostra contribució.
```bash
git clone https://github.com/decidim/docs-workshop.git
```

Per començar a fer les nostres contribucions al document cal seguir les indicacions següents:

1. Iniciem el *GitBook Editor*.

2. A la finestra d'inici cliquem sobre l'enllaç *Do that later*.

   ![](./img/flux-writer-01.png)

3. Seleccionem el document sobre el que volem treballar.

  ![](./img/flux-writer-02.png)

4. Un cop obert, i **abans de fer la nostra contribució**, creem una branca per guardar els nostres canvis.

   ![](./img/flux-writer-03.png)

5. A continuació seleccionem la branca de treball i fem les nostres contribucions.

   ![](./img/flux-writer-04.png)

6. Cada cop que guardem els canvis fets sobre el document l'editor ens demanarà que escrivim el comentari associat al *commit* que afegirà a l'històric del document.

   ![](./img/flux-writer-05.png)

7. Un cop hàgim enllestit la sessió de treball i ara per ara no haguem de fer cap més canvi publiquem les nostres contribucions.

   ![](./img/flux-writer-06.png)

8. Introduim les nostres credencials a *GitHub* quan l'editor ens ho demani.

   ![](./img/flux-writer-07.png)

9. Comuniquem a l'**Administradora de documentació** que hem fet la nostra contribució per a que pugui integrar els canvis a la branca principal  *master* del document.

10. Un cop l'administradora ens comuniqui que ha integrat els nostres canvis podrem sincronitzar la nostra còpia local. Seleccionem la branca principal com a branca de treball i fem *Sync* al menú *Book*.

    ![](./img/flux-writer-08.png)

11. Un cop els canvis s'hagin sincronitzat sense conflictes podrem esborrar la branca de treball que hem fet servir per a fer les nostres contribucions.

    ![](./img/flux-writer-09.png)


## Enllaços

- GitHub https://github.com/
- Cloning a repository https://help.github.com/articles/cloning-a-repository/
