# Charte graphique orientée web

Afin d'accélérer la création de charte graphique en éliminant les opérations redondantes.

Exemple live en ligne : [la démo](http://stockage.masamune.fr/divers/charte-graphique-example/).

**Pour les graphistes qui n'aiment pas le code/la console, vous pouvez récupérer directement le contenu du dossier `/dist` (tout compilé) et adapter**. Il suffit de modifier le HTML (les couleurs surtout) et normalement ça s'enchaine pas trop mal, cf. la [doc : /src/README.md](./src/README.md). Faite juste gaffe à la mise en place des polices.

Pour les devs, si vous souhaitez utiliser le projet de manière classique (avec un watch) :

```bash
# Accès au projet depuis la console
# cd Documents\_dev\lapie\200922-charte-graphique-lapie-proposition-1

# Installation
yarn
# ou
npm i

# Dev depuis /src (watch)
gulp watch
```

Note : Ne pas passer par `gulp prod`, qui ne gère pas (encore) correctement les modules JS (pas de transpile ou de concat sur les vendeurs -_-).

Note : Les liens du sommaire, les boutons de navigation (section suivante), les divs de couleurs (et des classes CSS) sont générés automatiquement en JS.

## TODOs

- Arrêter le frenglish FFS >.>
- Fix gulp prod (manque les vendeurs css/js ?)
- Passer css en sass et linter/refacto
- Couleurs primaires > Convertir en table x')
- Passer en templating html (pugjs ?) et générer à la volée les composants web

---

Basée sur [chaos-boilerplate-front](https://github.com/youpiwaza/chaos-boilerplate-front).

## chaos-boilerplate-front

Front-end boilerplate, to suit my needs.

## Gulp heavy

Numerous optimisations are done automattically thanks to gulp.

More details in [/gulp](./gulp/).

Here are the main commands.

> gulp

Copy /src & selected vendors to /watch

> gulp watch

Html, css, js HMR

> gulp prod

Concat, minify & inline inject of css & js

## Before prod Checklist

Various recommandations, you can also directly run online validators

### Online validators

- [w3c](https://validator.w3.org/)
- [Pagespeed insight](https://developers.google.com/speed/pagespeed/insights/)
- [Dareboost](https://www.dareboost.com/fr/) / Limited use per day in free version !
- [Webpage test](https://www.webpagetest.org/)
- [CSP check](https://securityheaders.com/)
- [Test responsive](https://www.lambdatest.com/
- [Test mobile load time](thinkwithgoogle.com/feature/testmysite/)

### Html

- Meta tags
- Open graph tags
- Favicon

- Linted
- Minified
- Remove css & js tags if inline injection

### Css

- Linted
- Concat external librairies
- Minified
- Inline injection
- .htaccess inline security (SHA-256) (XSS prevention)

### JS

- Linted
- Concat external librairies
- Minified
- Inline injection
- .htaccess inline security (SHA-256) (XSS prevention)

### Misc

- **Clean unused files**
- .htaccess configuration
- Images minification (.webp & webm, cf. [/src/assets/images](./src/assets/images/))
- Security loopholes prevention / https://www.hacksplaining.com/lessons
- Add google analytics / https://analytics.google.com/analytics/web/

## TODO

- Add accessibility checks & resources from [this article](https://dev.to/karkranikhil/web-accessibility-by-making-your-site-accessible-you-automatically-increase-the-target-audience-d8d)
- [+1](https://varvy.com/googlebot.html)
- Get back tool box & reimplant with css/js injection
  - and add new html stuff :
  
  https://developer.mozilla.org/fr/docs/Web/HTML/Element
  
  https://developer.mozilla.org/fr/docs/Web/HTML/Attributs_universels/itemid
  
  https://developer.mozilla.org/fr/docs/Web/HTML/Attributs_universels/itemprop
  
  https://developer.mozilla.org/fr/docs/Web/HTML/Attributs_universels/itemref
  
  https://developer.mozilla.org/fr/docs/Web/HTML/Attributs_universels/itemscope
  
  https://developer.mozilla.org/fr/docs/Web/HTML/Element/details
  
    - and add [complex elements can do w html/css only](https://dev.to/adrianbdesigns/you-can-create-these-elements-without-javascript-525a) and it also contains ellipsis and stuff

- [seo stuff](https://totheweb.com/learning_center/tools-search-engine-simulator/)

- Add basic [PWA](https://www.webdesignerdepot.com/2019/03/should-you-be-building-progressive-web-apps/) and add it to end checklist
