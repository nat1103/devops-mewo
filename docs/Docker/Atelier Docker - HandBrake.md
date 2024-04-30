# Atelier Docker - HandBrake

## Quelle commande utiliseriez-vous pour télécharger l'image Docker de HandBrake?
    docker pull jlesage/handbrake
## Comment lanceriez-vous un conteneur HandBrake pour traiter une vidéo située sur votre machine hôte?
    docker run -d --name=handbrake -p 5800:5800 -v /docker/appdata/handbrake:/config:rw -v /home/user:/storage:ro -v /home/user/HandBrake/watch:/watch:rw -v /home/user/HandBrake/output:/output:rw jlesage/handbrake
## Comment accéderiez-vous à l'interface Web de HandBrake?
    http://localhost:5800
## Quelles commandes permettent d'inspecter les détails et les logs d'un conteneur actif?
    docker inspect handbrake
    docker logs handbrake
## Comment arrêter, redémarrer, et finalement supprimer un conteneur et une image?

### Stop
    docker stop handbrake
### Restart
    docker restart handbrake
### Supprimer un conteneur
    docker rm handbrake
### Supprimer une image
    docker rmi jlesage/handbrake
