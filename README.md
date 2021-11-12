# DVD Elektor 2000-2009 (FR)

Correctifs pour accès WWW du DVDROM Elektor 2000-2009. Ce dépôt contient les liens des fichiers ayant un probleme de casse.
Il ne contient aucune donnée présente sur [le DVD de l'éditeur](https://www.elektor.fr/dvd-elektor-2000-2009-fr).

## Installation

Clonez ce dépôt à la racine de votre serveur HTTP (DocumentRoot)
```
  cd ${DocumentRoot}
  git clone https://github.com/lhondareyte/dvd-elektor-2000.git Elektor-2000
```

Copiez le contenu du DVD dans le dossier:

Sous FreeBSD:
```
  mount -t cd9660 /dev/cd0 /mnt ; cd /mnt
  find . -print | cpio -pdvmu ${DocumentRoot}/Elektor-2000
  cd - && umount /mnt
  camcontrol eject cd0
```

Sous Linux:
```
  mount -t iso9660 /dev/scd0 /mnt ; cd /mnt
  find . -print | cpio -pdvmu ${DocumentRoot}/Elektor-2000
  cd - && umount /mnt
  eject /dev/scd0
```
