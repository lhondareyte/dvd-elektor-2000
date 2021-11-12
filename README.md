# Elektor DVD 2000-2009 (FR)

Correctifs pour accès WWW du DVDROM Elektor 2000-2009. Ce dépôt contient les liens des fichiers ayant un probleme de casse.
Il ne contient aucune donnée présente sur [le DVD de l'éditeur](https://www.elektor.fr/dvd-elektor-2000-2009-fr).

## Installation

Copiez le contenu du DVD dans un dossier de votre serveur HTTP:

Sous FreeBSD:
```
  mount -t cd9660 /dev/cd0 /mnt ; cd /mnt
  mkdir ${DocumentRoot}/Elektor-2000
  find . -print | cpio -pdvmu ${DocumentRoot}/Elektor-2000
  cd - && umount /mnt
  camcontrol eject cd0
```

Sous Linux:
```
  mount -t iso9660 /dev/scd0 /mnt ; cd /mnt
  mkdir ${DocumentRoot}/Elektor-2000
  find . -print | cpio -pdvmu ${DocumentRoot}/Elektor-2000
  cd - && umount /mnt
  eject /dev/scd0
```

Puis 
```
  cd ${DocumentRoot}/Elektor-2000
  git clone https://github.com/lhondareyte/dvd-elektor-2000.git
```
