# Rôle Ansible : Installation et Déploiement de Site Web dans un Conteneur Apache

Ce rôle Ansible installe un conteneur Apache et déploie un site web en copiant le contenu depuis le dossier `templates` du rôle vers le conteneur.

## Prérequis

- Ansible 2.9 ou version ultérieure.
- Docker doit être installé sur la machine cible pour exécuter le conteneur Apache.

## Variables

- `ansible_user` : utilisateur ansible `admin`
- `èansible_password` : mot de passe utilisateur ansible `admin`
- `container_name` : le nom du conteneur apache `webapp`
- `apache_image` : l'image apache associée `httpd`
- `host_volume` : le chemin du volume de l'hôte `"/home/admin/index.html"`
- `container_volume` : le chemin du volume du conteneur `"/usr/local/apache2/htdocs/index.html"`
