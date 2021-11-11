# AngularHerokuTemplate

Este repositorio es un template para crear un projecto de angulas listo para ser publicado en la plataforma HEROKU. Sientete libre de usarlo y modificarlo cuando quieras

## Sass

Por defect este repositorio tiene configurado css como leguaje de estilos, puedes cambiarlo facilmente usando la rama sass y estableciendola colo tu rama principal

Tambien lo puedes hacer modificando en angular.json con: 
```json
{
  "projects": {
    "angular-heroku-template": {
      "schematics":{
        "@schematics/angular:component": {
          "style": "scss"
        }
      },
      "architect": {
        "build": {
          "options": {
            "styles": [
              "src/styles.scss"
            ],
          }
        }
      }
    }
  }
}
```

## Despliege

Una ves logeado con el cli de heroku y configurado el repositorio remoto para este de manera exitosa, solo se tiene que segir los pasos indicados en la [documentacion oficial](https://devcenter.heroku.com/articles/build-docker-images-heroku-yml) para tener un despliege exitoso

```
heroku stack:set container
git push heroku master
```



