# Projet3 - Dynamiser un site web avec des animations

## Description

Il s'agit de l'intégration de la maquette du site web de la startup "ohmyfood" incluant des animations pour dynamiser le tout

## Outils

- Visual Studio Code | IDE
- Langage HTML5 | [Docs HTML](https://developer.mozilla.org/fr/docs/Glossaire/HTML)
- Langage CSS3 | [Docs CSS](https://developer.mozilla.org/fr/docs/Glossaire/CSS)
- [Node.js](https://nodejs.org/en/docs/) | Plateforme JavaScript
- Langage [Sass](https://sass-lang.com/) | Préprocesseur CSS
- PostCSS | Autoprefixer CSS
- [Git](https://git-scm.com/) | Gestionnaire de versions

## Pré-requis

Avant de commencer, installez Sass en local sur votre machine.

1. Téléchargez et installez [Node.js](https://nodejs.org/en/download/)
2. Initialisez un fichier package.json, pour y inscrire toutes vos informations et vos scritps. Utilisez la commande :
```bach
npm init
```
Cela donne :
```bach
{
"name": "",
"version": "1.0.0",
"description": "",
"main": "index.js",
"scripts": {
  "test": "echo \"Error: no test specified\" && exit 1"
},
"author": "",
"license": "ISC"
}
```

3. Installez Sass via la commande :
```bach
npm install sass -g
```

4. Vérifiez la version de Sass via :
```bach
sass --version
```

5. Effacez le script "test" et ajoutez le script "sass"
```bach
{
"name": "",
"version": "1.0.0",
"description": "",
"main": "index.js",
"scripts": {
  "sass": "sass --watch ./sass/main.scss:./css/style.css"
},
"author": "",
"license": "ISC",
}
```

6. Lancez Sass via la commande :
```bach
npm run sass
```

7. Intstallez PostCSS via la commande :
```bach
npm install autoprefixer postcss postcss-cli -g
```

8. Ajoutez le script "prefix"
```bach
{
"name": "",
"version": "1.0.0",
"description": "",
"main": "index.js",
"scripts": {
  "sass": "sass --watch ./sass/main.scss:./public/css/style.css",
  "prefix": "postcss ./public/css/style.css --use autoprefixer -d./public/css/prefixed/"
},
"author": "",
"license": "ISC",
"browserslist": "last 4 versions"
}
```

9. Lancez PostCSS via la commande :
```bach
npm run prefix
```

Et voilà vous pouvez compiler votre CSS en toute sécurité !
