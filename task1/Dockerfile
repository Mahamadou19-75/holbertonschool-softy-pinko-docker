# Utilisation de la dernière version d'Ubuntu comme base (comme dans votre tâche 0)
FROM ubuntu:latest

# Mise à jour des paquets et installation de python3 et pip3 sans interaction utilisateur
RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y python3 python3-pip

# Astuce demandée pour éviter l'erreur "externally-managed-environment" sur les Ubuntu récents
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Installation de Flask via pip3
RUN pip3 install flask

# Définition du répertoire de travail dans le conteneur
WORKDIR /app

# Copie du script local api.py vers le dossier /app du conteneur
COPY ./api.py /app/api.py

# Commande par défaut pour lancer le serveur Flask au démarrage du conteneur
CMD ["python3", "api.py"]