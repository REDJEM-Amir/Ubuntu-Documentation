# Documentation de Configuration du Serveur Ubuntu

| **Tâche**                                         | **Commande** |
|---------------------------------------------------|--------------|
| **Effacer l'ancienne empreinte digitale**         | `ssh-keygen -R ipserver` |
| **Vérifier si le ping fonctionne avant SSH**      | `ping ipserver` |
| **Connexion SSH vers le serveur**                 | `ssh -lroot -p22 ipserver` <br> **Mot de passe** : `psswdserver` |
| **Voir qui est connecté sur le serveur**          | `who` |
| **Mises à jour système**                          | |
| *Mettre à jour la liste des paquets disponibles*  | `sudo apt update` |
| *Mettre à jour les paquets installés*             | `sudo apt upgrade` |
| *Mettre à jour le noyau et d'autres paquets*      | `sudo apt dist-upgrade` |
| *Supprimer les paquets inutilisés*                | `sudo apt autoremove` |
| **Ajouter un utilisateur**                        | `adduser nameuser` |
| **Changer le nom d'un utilisateur**               | `sudo usermod -l newname oldname` |
| **Modifier le mot de passe d'un utilisateur**     | `sudo passwd username` |
| **Mise à jour du groupe d'un utilisateur**        | `sudo groupmod -n newname oldname` |
| **Changer le répertoire home de l'utilisateur**   | `sudo usermod -d /home/newname -m newname` |
| **Ajouter l'utilisateur au groupe root**          | `sudo usermod -aG root username` |
| **Vérifier les groupes d'un utilisateur**         | `groups username` |
| **Changer le port de connexion SSH**              | |
| *Ouvrir le fichier de configuration SSH*          | `sudo nano /etc/ssh/sshd_config` |
| *Redémarrer le service SSH*                       | `sudo systemctl restart sshd` |
| *Vérifier que le service SSH est actif*           | `sudo systemctl status sshd` |
| **Désactiver le mot de passe du compte root**     | `sudo passwd -l root` |
| **Désactiver la connexion root via SSH**          | |
| *Ouvrir le fichier de configuration SSH*          | `sudo nano /etc/ssh/sshd_config` |
| *Modifier la ligne `PermitRootLogin`*             | `PermitRootLogin no` |
| *Redémarrer le service SSH*                       | `sudo systemctl restart sshd` |
