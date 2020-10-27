# TRAINSET

> TRAINSET is a graphical tool for labeling time series data

![TRAINSET GIF](TRAINSET-GIF.gif?raw=true "Title")

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# testing script for serving prod build locally
npm run start

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).




## Pour le lancement du programe:

``` 
Ouvrir le dossier trainset (2) dans votre bureau 

Ouvrir cmd .puis taper  "cd ".

"drag and drop" le dossier  trainset vers cmd, puis clickez sur "Entrée".

Saisir  " npm run dev" , Ensuite cliquez sur "Entrée".

Le programme accepte en input tous les fichiers .csv utilisé pour Aideal. 

à la fin de l'annotation, le programme enregistrera l'annotation dans un nouveau fichier.
```


## guide d'utilisateur:

``` 
**Menu principe**

Selectionnez le type de fichier à annoter ( saccade ou vergence). 

Si le type choisit est saccade alors le signal qui sera affiché pour l'annotation est le signal conjugué. 
Dans le cas echeant, le signal qui sera affiché est le signal déconjugué.


**Annotation**

Selectioner une partie du signal : labeliser en class 0 ( noir).

Selectionner une partie du signal tout en appuiant sur la touche "shift" : labeliser en class 1 ( bleu).

Selectionner une partie du signal tout en ap  "cltr" : labeliser en class 2 ( rouge).
```
 

## guide developeur:
``` 
**Labeler.vue**

Ce fichier source contient le code qui implemente la labelisation.
Les blocs modifiés sont : 245-246, 275-276, 414-427, 598-618, 776-787.  (format: premiere ligne - derniere ligne)

**Index.vue**

Ce fichier source contient le code qui implemente la page principale. Cette page permet à l'utilisateur de selectionnez le type de fichier à annoter ( saccade ou vergence) afin d'afficher dans la page du labelisateur le signal conjugué ou bien le signal déconjugué.
Les blocs modifiés sont : 12-13, 39-66,113-115.

** 
``` 

