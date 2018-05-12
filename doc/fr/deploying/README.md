# Déploiement

Tout au long du workshop, nous utilisons un serveur de développement pour voir les exemples. Ceci est similaire à la configuration que vous utiliserez lors du développement d'une application avec le [package `ol`](https://www.npmjs.com/package/ol). Lorsque vous êtes prêt à déployer votre application, vous voudrez créer un bundle minifié de votre point d'entrée de l'application avec une étape de build.

Nous avons utilisé [webpack](https://webpack.js.org/) pour le bundling de modules pendant le développement. Le `webpack.config.js` à la racine du répertoire de workshop comprend le profil de configuration webpack. Lorsque nous avons démarré le serveur de développement avec `npm start`, nous utilisions le profil` development`. Le profil `production` le build est minifié. Cela constitue un bon point de départ pour votre configuration webpack. Explorez les autres [plugins du site web](https://webpack.js.org/plugins/) pour voir ce que vous pourriez souhaiter apporter.

Pour créer des ressources pour le déploiement, nous exécutons notre script `build` à partir de` package.json`:

    npm run build

Cela exécute `webpack --mode=production`, mais ne nécessite pas que` webpack` soit sur notre chemin.

Une fois le build terminé, vous aurez des artefacts dans le répertoire `build`. Ce sont des assets que vous déployeriez sur votre serveur de production (ou S3, ou n'importe où vous souhaitez héberger votre application). Vous pouvez voir à quoi ressemble l'application en ouvrant le fichier `index.html` dans votre navigateur.

    open build/index.html

C'est tout. Vous avez terminé!

