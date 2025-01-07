# Boilerplate pour les mémoires

## Nomenclature

Le poids final du dossier est de 3 mo max
Le dossier est nommé avec prenom-nom (sans accents ni caractères spéciaux)
Pas de fichiers de travail dans le dossier (fichiers natifs texte et image)

### Structure
- index.html
    - assets/
      - css/
        - reset.css
        - style.css
        - print.css
      - fonts/
        - <font>.woff2


## Traitement des fichiers sources

Pandoc pour convertir de odt à html

`pandoc -t html -s Stiegler.odt -s -o output.html --metadata title="stiegler" `

https://pandoc.org/demos.html

## Traitement des images

Pour compresser les images en webp:
https://developers.google.com/speed/webp/docs/cwebp?hl=fr

`cwebp -q 80 neom-CzwL_vn445k-unsplash.jpg -o neom-CzwL_vn445k-unsplash.webp`

Pour compresser par lot avec une commande bash:
`for file in *; do
cwebp -q 80 $(file) -o $(file)
done`

## Traitement des fontes

https://github.com/google/woff2

`woff2_compress myfont.ttf`

## developpement

Serveur de développement local:
- Python > dans le dossier courant `python -m http.server`
- Node.js > live-server
> extension vscode ou cli avec npm
https://www.npmjs.com/package/live-server

### Metadonnées

## version pdf
https://weasyprint.org/
