Construire l’image docker:
Créez votre image de conteneur à l'aide de Cloud Build. Pour cela, exécutez la commande suivante à partir du répertoire contenant le fichier Docker
gcloud builds submit --tag gcr.io/PROJECT-ID/PROJET-NAME

Où PROJECT-ID correspond à l'ID de votre projet GCP. Vous pouvez l'obtenir en exécutant gcloud config get-value project. Et le PROJET-NAME correspond au nom de votre projet

Deployer l’image docker:
Pour déployer l'image de conteneur, procédez comme suit.

Utilisez la commande suivante pour effectuer le déploiement :
gcloud run deploy --image gcr.io/PROJECT-ID/PROJET-NAME --platform managed

Remplacez PROJECT-ID par l'ID de votre projet GCP. Vous pouvez afficher votre ID de projet en exécutant la commande gcloud config get-value project. Et le PROJET-NAME correspond au nom de votre projet

Vous serez invité à saisir le nom du service:
Appuyez sur Entrée pour accepter le nom par défaut, helloworld.

Vous serez invité à indiquer la région :
Sélectionnez la région de votre choix, par exemple us-central1.

Vous serez invité à autoriser les appels non authentifiés :
Répondez y.

Patientez quelques instants jusqu'à la fin du déploiement. En cas de réussite, la ligne de commande affiche l'URL du service.

Contenu du repo
DockerFile
Il continent la configuration de l’image Docker dans laquelle le logiciel Aideal sera exécuté

Wrapper/Index.js
Il contient le code source écrit en node js pour executer la library Aideal

Wrapper/*
Il contients les fichier sources du logiciel d’analyse Aideal

Wrapper/Index.js (main)
Le rôle de ce fichier est de recevoir le fichier à analyser + le fichier de configuration depuis le front-end. Ensuite il recuperer ( type de fichier, type de rapport, mail) à partir du fichier de configuration. Ensuite, le programme va exécuter le logiciel d’analyse pour générer le diagnostic. Enfin, il va envoyer le diagnostic au mail extrait depuis le fichier de configuration.

Utilisation du service
Pour accéder au service déployé, il faut ouvrir l'URL du service dans un navigateur Web. L'accès au service sera facturé en heure d’utilisation.
