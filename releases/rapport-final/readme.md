# Rapport SAÉ 2.03 : Installation de services réseaux
Auteurs : [Dewaele Enzo](mailto:enzo.dewaele.etu@univ-lille.fr), [Fernandes Bastien](mailto:bastien.fernandes.etu@univ-lille.fr) et [Hamiti Edi](mailto:edi.hamiti.etu@univ-lille.fr)

Dernières modifications : 23/03/2025

## Comment convertir un fichier .adoc sur Linux ?

### ⤓ Installation de `asciidoctor`
Utilisez la commande suivante pour **installer** le package asciidotor :
```bash
sudo apt install asciidoctor
```
 Pour **vérifier** l'installation, tapez la commande suivante :
```bash
asciidoctor --version
```

### ⇄ Convertir un fichier `.adoc` en fichier `.html`
Utilisez la commande suivante pour **convertir** votre fichier `adoc` en fichier `html`:
```bash
asciidoctor rapport.adoc
```
📄 Un `fichier.html` du meme nom que votre `fichier.adoc` sera automatiquement créé dans le répertoire. 

### ⇄ Convertir un fichier `.adoc` en `.pdf`
Tout d'abord, vous allez devoir installer **ruby** :
```bash
sudo apt install ruby-full
```
Pour **vérifier** l'installation, tapez la commande suivante :
```bash
ruby -v
```
---
Ensuite **installer** le package asciidoctor-pdf :
```bash
sudo gem install asciidoctor-pdf
```
Pour **vérifier** l'installation, tapez la commande suivante :
```bash
asciidoctor-pdf --version
```
---
Utilisez la commande suivante pour **convertir** votre fichier `adoc` en fichier `PDF`:
```bash
asciidoctor-pdf rapport.adoc
```
📄 Un `fichier.pdf` du meme nom que votre `fichier.adoc` sera automatiquement créé dans le répertoire.
