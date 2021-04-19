Déployer Wordpress sous K3S

Cloner le repertoire et dezipper le. Le site est déployer dans le namespace wordpress, il est créer automatique à chaque déploiement. 

Pour lancer la création du site wordpress et de sa base de données, tapez la commande :

kubctl apply -k ./

Pour vérifier les services sont bien lancés, tapez :

kubctl get services --namespace wordpress

Pour vérifier les volumes persistent, tapez :

kubctl get pvc --namespace wordpress

Pour vérifier les pods, tapez :

kubctl get pods --namespace wordpress

Vous pouvez accèder à votre site Wordpress via l'IP ou votre ingressroute si vous configurer un traefik ! 
Déployer Traefik sous K3S : https://github.com/bremib/traefikfork3s
