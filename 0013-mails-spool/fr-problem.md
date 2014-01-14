L’utilisation dans Symfony2 de SwiftmailerBundle permet d’envoyer des emails, par défaut celui-ci le fait de façon immédiate.
Cependant, l’utilisateur aura donc à attendre l’envoi de son email pour afficher la page suivante ; afin d’éviter cette attente il faudrait sauvegarder cet email dans un fichier et non l’envoyer directement, ce procédé s’appelle le “spool”.
Ensuite on lirait le contenu de ce fichier et on enverrait les emails correspondant.

Afin de vérifier si le système de “spooling” est déjà en place il faut vous rendre sur le fichier `config.yml` dans `app/config` et regarder le paramétrage de swiftmailer afin de voir si l’attribut “spool” est paramétré.