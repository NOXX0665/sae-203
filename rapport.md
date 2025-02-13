# Rapport SAE 2.03

## __Questions semaine 1__

### **Questions 1 : Configuration matérielle dans VirtualBox**
---

- **Que signifie "64-bit" dans "Debian 64-bit" ?**

    Dans "Debian 64-bit", "64-bit" fait référence à l'architecture du système d'exploitation. Cela signifie que le système d'exploitation est conçu pour fonctionner sur des processeurs 64 bits. Les processeurs 64 bits peuvent traiter plus de données simultanément que les processeurs 32 bits, ce qui permet généralement de meilleures performances.

- **Quelle est la configuration réseau utilisée par défaut ?**

    Par défaut, VirtualBox utilise le mode de connexion réseau "NAT" (Network Address Translation). Dans ce mode, la machine virtuelle partage l'adresse IP de l'hôte et est connectée au réseau via celui-ci. Ce mode permet à la machine virtuelle d'accéder à Internet, mais elle n'est pas directement accessible depuis l'extérieur.

- **Quel est le nom du fichier XML contenant la configuration de votre machine ?**

    Le nom du fichier XML contenant la configuration de la machine virtuelle est ```sae203.vbox```. Ce fichier est dans le dossier de la machine virtuelle. Sur les machines des salles TP, ce fichier se trouve dans le répertoire suivant :

    ```
    /usr/local/virtual_machine/infoetu/{login}/vbox_vms/sae203/
    ```
    où `{login}` est le login de l'utilisateur de la machine.

- **Sauriez-vous modifier directement ce fichier de configuration pour mettre 2 processeurs à votre machine ?**

    > [!WARNING]
    > Avant de modifier ce fichier, il est nécessaire d'éteindre la machine virtuelle. Sinon, toutes modifications seront écrasées lors du prochain redémarrage de la machine virtuelle.

    Il est possible de modifier directement le fichier de configuratio, XML pour attribuer 2 processeurs. Dans la section `<CPU>` du fichier `sae203.vbox`, il faut modifier la valeur de l'attribut `count` à 2.


### **Questions 2.Installation de base**
---

-  **Qu’est-ce qu’un fichier ISO bootable ?**

    Un fichier ISO bootable est une image disque utilisée pour démarrer un ordinateur, installer un système d'exploitation ou bien des logitiel.

- **Qu’est-ce que MATE ? GNOME ?**

    - MATE : Environnement de bureau léger et classique, dérivé de GNOME 2.
    - GNOME : Environnement de bureau moderne, minimaliste, axé sur la simplicité.
    
- **Qu’est-ce qu’un serveur web ?**

    Un serveur web est un logiciel qui héberge des sites et applications web et les rend accessibles via le protocole HTTP.

- **Qu’est-ce qu’un serveur SSH ?**

    Un serveur SSH permet d’accéder à distance à un système de manière sécurisée, en chiffrant les communications.

- **Qu’est-ce qu’un serveur mandataire ?**

    Un serveur mandataire (proxy) est un intermédiaire entre un client et un serveur, utilisé pour filtrer, sécuriser ou cacher les requêtes.

    
### **Question(s) 3 : sudo**
---

- **Comment peux-ton savoir à quels groupes appartient l’utilisateur user ?**

    Pour voir les groupes d'un utilisateur il faut faire la commande `groups "user"`

### **Questions 4.1 : Suppléments invités**
---

- **Quel est la version du noyau Linux utilisé par votre VM ? N’oubliez pas, comme pour toutes les questions, de justifier votre réponse**
    
    Pour connaître la version du noyau LInux utiliser il faut utiliser la commande `uname -r` ce qui nous donne : 
    `6.1.0-31-amd64`

- **À quoi servent les suppléments invités ? Donner 2 principales raisons de les installer.**

    Cela permet d'améliorer les performance graphique le partage de dossiers et de périphériques entre l'hôte et la machine vituelle, pour le redimensionnement dynamique de la fenêtre, une meilleur gestion du clipboard, facilite la gestyion de périphérique.

- **À quoi sert la commande mount (dans notre cas de figure et dans le cas général) ?**

    La commande mount est utilisée pour monter un périphérique de stockage ou un système de fichiers sur un répertoire spécifique dans l'arborescence du système de fichiers. Dans notre cas précis, lorsque l'on insére le CD des suppléments invités, on utilise la commande mount pour monter le CD-ROM sur un répertoire spécifique de notre système.

### **Questions 4.2 : Quelques Questions**
---

- **Qu’est-ce que le Projet Debian ? D’où vient le nom Debian ?**

    Le Projet Debian est une organisation communautaire qui développe le système d'exploitation Debian, composé de logiciels libres et open source. Le nom "Debian" est une combinaison des prénoms de son fondateur, Ian Murdock, et de sa petite amie de l'époque, Debra Lynn.

- **Il existe 3 durées de prise en charge (support) de ces versions : la durée minimale, la durée en support long terme (LTS) et la durée en support long terme étendue (ELTS). Quelle sont les durées de ces prises en charge ?**
**Pendant combien de temps les mises à jour de sécurité seront-elles fournies ?**

    Les durées de prise en charge des versions Debian sont les suivantes :

    - **Durée minimale :** 1 an après la sortie de la version suivante.
    
    - **Support long terme (LTS) :** 5 ans après la date de sortie initiale.
    
    - **Support long terme étendu (ELTS) :** Jusqu'à 5 ans supplémentaires après la fin du support LTS, soit un total de 10 ans après la date de sortie initiale.


- **Combien de versions au minimum sont activement maintenues par Debian ? Donnez leur nom générique (= les types de distribution).**

    Debian maintient activement au minimum trois versions de son système d'exploitation à tout moment. Les noms génériques de ces types de distribution sont :

    - **Stable :** La version stable actuelle, recommandée pour la plupart des utilisateurs.

    - **Testing :** La version en cours de test, qui deviendra la prochaine version stable.

    - **Unstable :** La version de développement, où les nouvelles fonctionnalités et mises à jour sont introduites en premier.

- **Chaque distribution majeure possède un nom de code différent. Par exemple, la version majeure actuelle (Debian 12) se nomme "bookworm". D’où viennent les noms de code donnés aux distributions ?**

    Les noms de code donnés aux distributions Debian proviennent des personnages du film d'animation "Toy Story" de Pixar.

    - **Première version avec un nom de code :**
        - **Quel a été le premier nom de code utilisé ?**
            Buzz
        - **Quand a-t-il été annoncé ?**
            Le 16 juin 1996
        - **Quelle était le numéro de version de cette distribution ?**
            Debian 1.1

    - **Dernier nom de code attribué :**
        - **Quel est le dernier nom de code annoncé à ce jour ?**
            Trixie
        - **Quand a-t-il été annoncé ?**
            Le 12 août 2023
        - **Quelle est la version de cette distribution ?**
            Debian 13
        
### **Question(s) 5.Ajustement de la pré-configuration**
---

- **Ajouter le droit d'utiliser sudo à l'utilisateur standard**

    **Pour ajouter le droit sudo à l'utilisateur standard il faut ajouter dans le fichier `preseed-fr.cfg` qui se situe dans le répertoire de la machine virtuelle la ligne suivante :**

        d-i passwd/user-default-groups string audio cdrom video sudo

- **Installer l’environnement MATE**
    
    Pour installer l'environnement MATE il faut ajouter dans le fichier `preseed-fr.cfg` qui se situe dans le répertoire de la machine virtuelle la ligne suivante :

        tasksel tasksel/first multiselect standard ssh-server mate-desktop

- **Ajouter les paquets suivants :
◦ sudo : sinon la gestion sudo est inutile
◦ git, sqlite3, curl : pour préparer l’installation de la semaine prochaine
◦ bash-completion : va vous simplifier grandement l’écriture des lignes de commande
◦ neofetch : pas très utile mais c’est un classique dans son genre (essayez-le)**

    Pour installer les paquets ci-dessus automatiquement pendant l'installation de la machine virtuelle, il faut ajouter, dans le fichier `preseed-fr.cfg`, la ligne suivante :

        d-i pkgsel/include string sudo git sqlite3 curl bash-completion neofetch