## Workflow

### Référence

- https://devcenter.heroku.com/articles/how-heroku-works : comprendre le fonctionnement technique de Heroku
- https://devcenter.heroku.com/articles/getting-started-with-nodejs#introduction : Getting started Node
- https://devcenter.heroku.com/articles/architecting-apps : architecture

### installation

- installer le Heroku Toolbelt pour OS X https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up

```sh
heroku login
``

```sh
# on rapatrie sur son poste un repo git de github
git clone https://github.com/heroku/node-js-getting-started.git

cd node-js-getting-started

# permet d'ajouter un remote git nommé heroku
heroku create 

MacBook-Air-de-Pierre-Olivier:node-js-getting-started pom$ git remote -v
heroku	https://git.heroku.com/shrouded-spire-64809.git (fetch)
heroku	https://git.heroku.com/shrouded-spire-64809.git (push)
origin	https://github.com/heroku/node-js-getting-started.git (fetch)
origin	https://github.com/heroku/node-js-getting-started.git (push)


# Procfile définit la commande à lancer
cat > Procfile << EOF
web: npm run start
EOF

# ajout du Procfile au repo git général
git add .
git commit -m "ajout Procfile"
git push origin master

# push sur le remote heroku a pour effet de déployer l'app
git push heroku master 

# pour avoir un dyno web (si compte gratuit, 1 dyno max autorisé)
heroku ps:scale web=1 
# ouvre une page de navigateur
heroku open 



# pour troubleshooting  
heroku logs --tail
heroku ps
```

Pour test en local 

```sh
heroku local web
``

Pour accéder en ligne de commande à la VM de Heroku
```sh
heroku run node
heroku run bash
```

## Troubleshooting : 

Si webpack est en devDependencies, ajouter : 

heroku config:set NPM_CONFIG_PRODUCTION=false. You should remove the webpack.NoErrorsPlugin

## Liens

- http://nicholaspaulsmith.com/spring-boot-on-heroku/
- http://www.christianalfoni.com/articles/2015_04_19_The-ultimate-webpack-setup
- https://medium.com/@rajaraodv/webpack-the-confusing-parts-58712f8fcad9#.w8fdh1shg
- http://www.tuicool.com/articles/AzueuiV
- https://scotch.io/tutorials/how-to-deploy-a-node-js-app-to-heroku
