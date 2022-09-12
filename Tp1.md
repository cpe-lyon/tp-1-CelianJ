# TP 1

## Exercice 2

### Manuel
#### 1
La commande **which** est une commande permettant de trouver l'emplacement d'un fichier en renvoyant son PATH

#### 2
Pour chercher un terme dans le manuel on peut utiliser la commande **/** suivi du terme a chercher

#### 3
Pour quitter le manuel on appuie sur **q**

#### 4
Afin d'afficher la première page de la section 6 du manuel il faut tapper la commande **man -K 6** cette section est la section **dpkg-mainscript-helper** qui est une aide pour le dpkg (debian package)

### Navigation

#### 1
la commande est **cd /var/log** pour accéder au dossier

#### 2
la commande est **cd ..** pour accéder au dossier avec un chemin relatif

#### 3
la commande est **cd /home** pour accéder au dossier personnel

#### 4
la commande est **cd -** pour accéder au dossier précédent

#### 5
Nous n'avons pas les permissions pour accéder au dossier root un **permission denied** apparait apres l'utilisation de la commande cd /root

#### 6
Après l'utilisation de la commande sudo cd /root l'ordinateur nous renvoie un "command not found" car **la commande sudo ne s'applique qu'au programmes et pas aux commandes**

#### 7
```
├── Dossier1
│   └── Fichier1
└── Dossier2
│   ├── Dossier2.1
│   └── Dossier2.2
│   |	├── Fichier2
│   |	└── Fichier3
```
Pour créer les dossiers on utilise la commande ``mkdir`` et pour les fichiers la commande ``touch``.

#### 8
La commande ``rm`` fonctionne pour les fichiers mais pas pour les dossiers.

#### 9
La commande **rmdir** est la commande a utiliser pour supprimer un dossier.

#### 10
Cela ne fonctionne pas car le dossier 2 contient d'autres éléments

#### 11
Afin de supprimer le dossier et le contenu dedans on utilise la commande **rm -r**

### Commandes importantes

#### 1
La commande **date** permet d'afficher la date et l'heure. La commande ``time`` permet d'afficher le temps utiliser pour une commande

#### 2
Les fichiers commençant par un . sont des fichiers **cachés**

#### 3
Le programme ls se trouve a l'emplacement **usr/bin/ls**

#### 4
La commande ``ll`` ne possède pas d'entrée de manuel. En effet il s'agit d'un alias c'est a dire que c'est une contraction de la commande ``ls -alF``.

#### 5
La commande permettant d'afficher les fichiers de /bin est **ls /bin**

#### 6
La commande ``ls ..`` affiche les fichiers non cachés du repository en dessous de l'actuel.

#### 7
La commande permettant d'afficher le chemin complet du dossier courant est la commande **pwd**

#### 8
La commande ``echo 'bib' > plop`` ajoute le mot bib dans un nouveau fichier plop. Exécutée une deuxième fois il écrase le contenu du fichier plop pour le remplacer par bib.

#### 9
La commande ``echo 'bib' >> plop`` ajoute le mot bib a la fin du fichier plop. Exécutée une deuxième fois il rajoute le mot bib a la fin du fichier plop.

#### 10
La commande ``sleep 10 | echo 'toto'`` fait que le pc attend 10 secondes puis renvoie toto dans la commande

#### 11
La commande ``file`` renvoie le type du fichier donné en paramètre

#### 12
Après avoir modifié le contenu de original le lien contient aussi les changements apportés au fichier. Après avoir supprimé le fichier, le lien lui contient encore le contenu du fichier.

#### 13
Après avoir modifié le contenu du lien physique le lien symbolique contient aussi les changements apportés au fichier. Après avoir supprimé le lien physique le lien symbolique est supprimé avec.

#### 14
Afin d'interrompre le défilement du fichier a l'écran il faut appuyer sur **Crtl + s** et pour le reprendre **Crtl + q**

#### 15
pour afficher les 5 premières lignes **head -5 /var/log/syslog**
pour afficher les 15 dernières lignes **tail -15 /var/log/syslog**
pour afficher les lignes entre 10 et 20 **head -n 10 /var/log/syslog | tail -n 20**

#### 16
La commande ``dmesg | less`` permet d'afficher les derniers messages du buffer du kernel.

#### 17
Le fichier ``/etc/passwd`` stocke les informations essentielles des utilisateurs du système.
La commande **man /etc/passwd** permet d'afficher le manuel de ce fichier.

#### 18
La commande pour afficher la première colonne par ordre alphabétique inverse est **cat /etc/passwd | awk '{ print $1 }' | sort -r**

#### 19
La commande qui permet de compter le nombre d'utilisateurs est **wc -l /etc/passwd**

#### 20
**man -k conversion | wc -l**

#### 21
La commande qui permet de trouver tout les fichiers se nommant passwd est **sudo find / -iname passwd**

#### 22
La commande qui permet d'enregistrer tout les fichiers se nommant passwd dans un fichier et les erreurs dans un autre fichier est **sudo find / -iname passwd > -/list_passwd_files.txt 2> /dev/null**

#### 23
La commande qui permet de trouver ou est stocké l'alias ll est **grep -r 'alias ll'**

#### 24
history.log se trouve a l'emplacement **/var/log/apt/history.log**

#### 25

## EXERCICE 3

#### 1
``cp /var/log/syslog log.txt`` puis ``nano log.txt``

#### 2
``Ctrl + \ kernel noyau``

#### 3
``Ctrl + K`` puis ```Ctrl + U``

#### 4
``Alt + U``

#### 5
``Ctrl + S``

## Exercice 4

#### 1
``cp ~/.bashrc .bashrc_bak``

#### 2
``nano .bashrc`` puis ``Ctrl + W force_color``

#### 3
La commande est bien passé en couleur

#### 4
``PS1="[\033[38;5;1m][[$(tput sgr0)][\033[38;5;92m]\t[$(tput sgr0)][\033[38;5;1m]][$(tput sgr0)]-[$(tput sgr0)][\033[38;5;10m]\u@\h[$(tput sgr0)]:[$(tput sgr0)][\033[38;5;51m]\w[$(tput sgr0)]"``
