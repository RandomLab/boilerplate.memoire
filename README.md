
Poids final du dossier max : 3mo
Structure :
index.html
assets/
css/
reset.css
style.css
fonts/
<font>.woff2

-----
Avant
-----

Pandoc pour convertir de odt à html

`pandoc -t html -s Stiegler.odt -s -o output.html --metadata title="stiegler" `

https://pandoc.org/demos.html

-----
Après
-----

Serveur de développement local:
- Python > dans le dossier courant `python -m http.server`
- Node.js > live-server
> extension vscode ou cli avec npm
https://www.npmjs.com/package/live-server


------
images
------

Pour compresser les images en webp:
https://developers.google.com/speed/webp/docs/cwebp?hl=fr

`cwebp -q 80 neom-CzwL_vn445k-unsplash.jpg -o neom-CzwL_vn445k-unsplash.webp`

Pour compresser par lot avec une commande bash:
`for file in *; do
cwebp -q 80 $(file) -o $(file)
done`


------
fonts
------
https://github.com/google/woff2

`woff2_compress myfont.ttf`
