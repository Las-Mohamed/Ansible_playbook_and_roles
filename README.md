# Ansible_playbook_and_roles

Injection de apache2/php et mysql sur 2 VM différentes via Ansible

1) Création de l'inventaire qui contiendra les hôtes, les alias et leurs clés SSH
2) Dossier "roles" contenant les arborescences des rôles souhaités obtenus grâce à la commande "ansible-galaxy init <nom_du_role>
3) /roles/(database ou web)/tasks/main.yml, édition des tâches à effectuer pour les applicatifs en question
4) /roles/database/vars/main.yaml, paramétrage des variables de la database
5) Création du playbook.yml qui orchestrera l'injection des applicatifs en fonction des machine cibles (alias)
6) Executer le playbook "ansible-playbook playbook.yml -i inventaire.ini" ((-vvv) pour le mode debug)
