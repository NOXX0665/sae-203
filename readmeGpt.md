# 📖 Guide : Conversion d'un fichier .adoc sous Linux

---

## 🚀 Installation de Asciidoctor

### 🛠️ 1. Installer Asciidoctor

Exécute la commande suivante pour installer Asciidoctor :

```bash
sudo apt install asciidoctor
```
✅ Vérifier l'installation :

```bash
asciidoctor --version
```

---

## 🌐 Convertir un fichier `.adoc` en `.html`

### 📌 Commande de conversion

```bash
asciidoctor rapport.adoc
```

📄 Un fichier `rapport.html` sera automatiquement généré dans le même répertoire.

---

## 📄 Convertir un fichier `.adoc` en `.pdf`

### 🛠️ 1. Installer Ruby (prérequis)

```bash
sudo apt install ruby-full
```
✅ Vérifier l'installation :

```bash
ruby -v
```

### 📌 2. Installer le package `asciidoctor-pdf`

```bash
sudo gem install asciidoctor-pdf
```

✅ Vérifier l'installation :

```bash
asciidoctor-pdf --version
```
### 📄 3. Convertir le fichier `.adoc` en `.pdf`

```bash
asciidoctor-pdf rapport.adoc
```

📄 Un fichier `rapport.pdf` sera automatiquement généré dans le même répertoire.