# Boilerplate pour les mémoires

## Nomenclature

Le poids final du dossier est de 3 mo max
Le dossier est nommé avec prenom-nom (sans accents ni caractères spéciaux)
Pas de fichiers de travail dans le dossier (fichiers natifs texte et image)

### Structure
- index.html
    - images/
    - assets/
      - css/
        - reset.css
        - style.css
        - print.css
      - fonts/
        - <font>.woff2


## Traitement des fichiers sources

- Pandoc pour convertir de md à html
`  pandoc -f markdown -t html5 -o index.html input.md -c style.css `

- Pandoc pour convertir de odt à html
`pandoc -t html -s Stiegler.odt -s -o output.html --metadata title="stiegler" `

https://pandoc.org/demos.html

## Compression des images

- Pour compresser les images en webp:
https://developers.google.com/speed/webp/docs/cwebp?hl=fr

`cwebp -q 80 neom-CzwL_vn445k-unsplash.jpg -o neom-CzwL_vn445k-unsplash.webp`

- Pour compresser par lot avec une commande bash:
`for file in *; do
cwebp -q 80 $(file) -o $(file)
done`

## Traitement des fontes

- Pour compresser les fichiers de fontes `otf` et `ttf` en `woff2`:
https://github.com/google/woff2

`woff2_compress myfont.ttf`

## developpement

Serveur de développement local:
- Python > dans le dossier courant `python -m http.server`
- Node.js > live-server
> extension vscode ou cli avec npm
https://www.npmjs.com/package/live-server

### Metadonnées

- Ajouter des metadonnées dans la page `index.html`

## version pdf

https://weasyprint.org/

- Pour générer la version pdf depuis votre page web 

`weasyprint http://127.0.0.1 memoire.pdf` 

# TODO

> videos une image dans pdf
> element qui affiche un autre element au survol (ex: definition)
> btn pour remonter la page 