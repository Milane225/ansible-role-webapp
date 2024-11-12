# Rôle Ansible : Installation et Déploiement de Site Web dans un Conteneur Apache

Ce rôle Ansible installe un conteneur Apache et déploie un site web en copiant le contenu depuis le dossier `templates` du rôle vers le conteneur.

## Prérequis

- Ansible 2.9 ou version ultérieure.
- Docker doit être installé sur la machine cible pour exécuter le conteneur Apache.

## Variables

- `apache_container_name` : Nom du conteneur Apache qui sera créé et utilisé. Par défaut : `apache_container`.
- `apache_web_root` : Chemin du répertoire web dans le conteneur Apache. Par défaut : `/var/www/html`.
- `apache_image` : Image Docker Apache à utiliser. Par défaut : `httpd:latest`.

## Structure du Répertoire

```plaintext
.
├── defaults
│   └── main.yml                # Définit les valeurs par défaut des variables
├── tasks
│   ├── main.yml                # Définit les tâches principales du rôle
│   ├── install_container.yml   # Tâches pour installer et configurer le conteneur Apache
│   └── deploy_site.yml         # Tâches pour copier le site dans le conteneur
├── templates
│   └── index.html.j2           # Exemple de fichier de site web (HTML) à copier
└── README.md                   # Ce fichier
