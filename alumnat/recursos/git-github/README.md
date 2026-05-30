# 🔧 Guia d’ús de Git i GitHub

Aquest document està pensat com una guia pràctica per a l’alumnat que treballarà en el projecte. No només inclou les comandes, sinó també el *per què* i *com utilitzar-les correctament* en un entorn real de treball en equip.

---

## 🧠 Què són Git i GitHub?

Git és un sistema de control de versions que permet guardar l’historial dels canvis d’un projecte. Això significa que podem:

- Recuperar versions anteriors del codi
- Veure qui ha fet cada canvi
- Treballar diverses persones sobre el mateix projecte sense perdre informació

GitHub és una plataforma web on es pugen els repositoris Git. Permet:

- Compartir el codi amb altres persones
- Treballar en equip
- Centralitzar totes les versions del projecte

👉 En aquest projecte, GitHub serà el lloc on es lliuraran els sprints.

---

## ⚙️ Instal·lació i configuració

### Instal·lar Git

👉 https://git-scm.com/

Una vegada instal·lat, comprova que funciona:

```bash
git --version
```

---

### Configuració inicial

```bash
git config --global user.name "Nom cognoms"
git config --global user.email "email@exemple.com"
```

👉 Açò és important perquè cada canvi quedarà registrat amb el teu nom.

---

## 🌐 Crear el repositori del projecte

En aquest projecte, el repositori serà creat inicialment en GitHub i posteriorment cada membre del grup el descarregarà al seu ordinador.

---

### 🌐 1. Crear el repositori en GitHub

1. Accedir a:
   https://github.com/

2. Iniciar sessió amb el compte personal.

3. Fer clic en el botó:

```bash
 New repository
```


4. Configurar el repositori:

- **Nom del repositori**: (per exemple `karma-cli`)
- **Visibilitat**: públic o privat (segons indicacions del professorat)
- Marcar opcionalment:
	- ✅ Add a README file  
	- ✅ Add .gitignore  

5. Fer clic en:

```bash
Create repository
```

  👉 En aquest punt, el repositori ja està creat en GitHub.

---

### 📥 2. Clonar el repositori en local

Una vegada creat el repositori, cal descarregar-lo al vostre ordinador.

1. En la pàgina del repositori, fer clic en el botó verd:

```bash
Code
```

2. Copiar la URL del repositori

3. Executar en terminal:

```bash
git clone URL_DEL_REPOSITORI
```

👉 Aquesta comanda crearà una carpeta amb el projecte en el vostre equip.

### 📂 3. Accedir al projecte

Entrar en la carpeta del projecte:

```bash
cd nom-del-repositori
```

### ✅ 4. Comprovar que tot funciona

```bash
git status
```

👉 Si tot és correcte, Git indicarà que el repositori està inicialitzat i sense canvis pendents.

---

## 🔁 Flux de treball habitual

El treball amb Git sempre segueix aquest esquema:

1. Modifiques el codi
2. Guardes els canvis (add)
3. Confirmes els canvis (commit)
4. Els envies a GitHub (push)

---

### 🧩 Exemple complet

```bash
# Verifica que estàs en la branca correcta
git status  

git add .
git commit -m "descripció dels canvis realitzats"
git push
```

---

## 🌿 Treball amb branques (essencial)

Les branques permeten treballar en diferents parts del projecte sense afectar la versió principal.

👉 En aquest projecte:
- Cada sprint = una branca

---

### Saber en quina branca estàs

```bash
git branch
```

👉 L’asterisc indica la branca activa.

---

### Crear una branca

```bash
git checkout -b sprint1
```

👉 Crea la branca i et canvia automàticament.

---

### Canviar de branca

```bash
git checkout sprint1
```

---

### Crear una branca a partir d’una altra

```bash
git checkout sprint1
git checkout -b sprint2
```

👉 sprint2 hereta tot el treball fet en sprint1.

---

### Pujar branca a GitHub

```bash
git push -u origin sprint1
```

👉 Important: la primera vegada cal usar -u.

---

## 👥 Treball en equip (molt important)

Quan treballen diverses persones:

### Norma principal
👉 Abans de treballar → fer pull

```bash
git pull
```

### Abans de fer push

```bash
git pull
```

👉 Això evita conflictes.

---

## ⚠️ Conflictes

Un conflicte passa quan dues persones modifiquen el mateix lloc del codi.

Git indicarà alguna cosa com:

```text
<<<<<<< HEAD
el teu codi
=======
codi del company
>>>>>>>
```

### Solució:

1. Revisar el codi
2. Decidir què es queda
3. Esborrar les marques
4. Guardar

```bash
git add .
git commit -m "conflicte resolt"
```

---

## ✅ Bones pràctiques

- Fer commits sovint (no tot al final)
- Escriure missatges clars
- No treballar mai en main
- Organitzar el codi
- Comunicar-se amb l’equip

---

## 🔍 On buscar ajuda

- Documentació oficial:
  - https://git-scm.com/doc
  - https://docs.github.com/

- YouTube: "git tutorial principiants"
- IA: ChatGPT / Copilot
- Professor

---

## 🚀 Resum ràpid

```bash
git pull
git checkout -b sprintX
git add .
git commit -m "missatge"
git pull
git push
```

👉 Seguint aquests passos evitaràs la majoria dels errors.

---

## ✅ Conclusió

Git és una eina fonamental en el món professional.

Permet treballar en equip, mantenir versions i evitar pèrdues d’informació. Aprendre a utilitzar-lo correctament és tan important com programar.
