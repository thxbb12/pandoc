---
title       : Virtualisation
solutions   : false
author      :
     - "Professeur : Florent Gluck"
     - "Assistant : Sebastien Chassot"
date        : Octobre 2019
papersize   : A4
geometry    : margin=2.5cm
colorlinks  : urlcolor
fontsize    : 12pt
---

# TP Docker basics

## Introduction

Le but de ce travail pratique est de se familiariser avec les manipulations de base des containers Docker et d'en comprendre le fonctionnement.

## Préparation

Sur la même machine hôte que celle utilisée lors des travaux pratiques précédents, installez le package nécessaire à l'utilisation des containers Docker. Pour rappel `apt-cache search` permet de réaliser une recherche par mot-clés dans la repository Ubuntu/Debian.
Il est très fortement recommandé d'utiliser Docker avec votre utilisateur normal (pas root/sudo). Pour cela assurez-vous que votre utilisateur appartient au groupe docker. La commande `groups` permet d'afficher les groupes auquel appartient l'utilisateur courant. Pour ajouter un utilisateur à un ou plusieurs groupes, utilisez la commande `usermod`. Ensuite, reconnectez-vous pour que l'appartenance au groupe soit effective.
Enfin, assurez-vous que le service docker soit démarré au démarrage de la machine avec `systemctl enable docker` (en tant que root). Le service docker peut aussi être démarré/arrêté avec `systemctl start/stop docker`.

\begin{comment}
\begin{lstlisting}[language=bash,style=solutions]
sudo apt install docker.io
sudo usermod -a -G docker student
su student
groups -> permet de vérifier l'appartenance au groupe docker
sudo systemctl enable docker
sudo systemctl start docker
\end{lstlisting}
\end{comment}

Comme Docker nécessite potentiellement plusieurs GB de libre dans `/var/lib/docker`, assurez-vous que vous avez suffisamment d'espace à cet endroit (d'où la nécessité d'avoir réservé la moitié de votre volume groupe avec LVM lors du dernier TP QEMU/LVM).

Docker télécharge les images sur un registry via le protocole https. Sur la machine qui vous est fournie, le traffic https passe par un proxy de l'école. Voici les étapes à effectuer (en root) pour que Docker utilise le proxy de l'école (via systemd) :

```
# Créez le répertoire suivant :
$ sudo mkdir -p /etc/systemd/system/docker.service.d

# Dedans, créez le fichier `http-proxy.conf` avec le contenu :
[Service]
...
```

## Exercice 1

Une série d'exercices se trouvent sur ...

\begin{comment}
\begin{lstlisting}[language=bash,style=solutions]
blah blah blah
blah blah blah
blah blah blah
blah blah blah
\end{lstlisting}
\end{comment}

Déterminez l'image du premier exercice...
