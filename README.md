# Configuration server FreeBSD

## Effacer l'ancienne empreinte digitale
> ssh-keygen -R ipserver

## Vérifier si le ping fonctionne avant ssh
> ping ipserver

## Connexion ssh vers le serveur
> ssh -lroot -p22 ipserver
> psswdserver

## Savoir qui est connecté sur le serveur 
> who

## Ajouter un utilisateur
> adduser nameuser

## Changez le nom d'utilisateur 
> sudo usermod -l newname oldname

## Modifier le mot de passe d'un utilisateur
> sudo passwd username

## Mise à jour du groupe 
> sudo groupmod -n newname oldname

## Changez le nom du répertoire home de l'utilisateur 
> sudo usermod -d /home/newname -m newname

## Ajouter l'utilisateur au groupe root
> sudo usermod -aG root username

## Vérifier le groupe de l'utilisateur
> groups username
