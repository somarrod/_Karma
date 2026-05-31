# 🚀 Sprint 3

---

## 🎯 Objectiu del sprint

Durant aquest sprint, l’alumnat farà un pas clau en el projecte: **convertir l’aplicació en segura i controlada**.

Els objectius principals són:

- Implementar autenticació d’usuaris  
- Controlar l’accés segons permisos  
- Validar formularis correctament  
- Consolidar la comunicació amb el backend  

👉 En aquest punt, l’aplicació passa de ser funcional a **ser una aplicació real amb control d’accés**.

---

## 🧠 Continguts a treballar

### 📘 Unitat 5: Autenticació i autorització

- Diferència entre autenticació i autorització  
- Sistemes de login  
- Gestió de rols (alumne, professor, admin, equip directiu)  
- Control d’accés a funcionalitats  
- Validació amb el servidor (_KarmaWebApi_)  

👉 Aquestos continguts permeten protegir l’aplicació.

---

### 📘 Unitat 6: Validació de formularis

- Introducció a Reactive Forms  
- Validació de camps (formats, obligatoris, longituds)  
- Missatges d’error  
- Integració de validació amb formularis existents  

👉 Es treballa la qualitat de les dades i l’experiència d’usuari.

---

## 🛠️ Desenvolupament del sprint

---

### 🔐 1. Implementació del login

- Crear sistema de login funcional  
- Connectar amb el servidor (_KarmaWebApi_)  
- Validar credencials  

👉 <!-- Ací pots indicar com fer la petició HTTP de login -->

---

### 👤 2. Gestió de rols

- Identificar el rol de l’usuari  
- Adaptar el comportament de l’aplicació  
- Mostrar opcions segons permisos  

👉 (ex: admin veu tot, alumne només el seu)

---

### 🚫 3. Control d’accés

- Protegir rutes o funcionalitats  
- Evitar accés sense permisos  
- Redirigir usuaris segons el seu rol  

👉 Aquesta part és clau per a evitar errors greus d’ús.

---

### 🧾 4. Validació de formularis

- Validar camps obligatoris  
- Validar formats (email, números, etc.)  
- Mostrar errors a l’usuari  

👉 La validació evita dades incorrectes en el sistema.

---

### 🔄 5. Integració amb el backend

- Validar usuaris en el servidor  
- Gestionar respostes correctes i errors  
- Mantindre coherència amb l’sprint anterior  

---

### 🧪 6. Revisió i depuració

- Provar login i permisos  
- Detectar errors de seguretat  
- Revisar validacions  

---

## 👥 Organització del treball

- Continuar treballant en grups de 3  
- Mantindre organització en tasques  
- Revisar millores pendents de l’sprint 2  

👉 link: ../../recursos/git-github/README.md

👉 En aquest sprint és important:
- treball coordinat  
- evitar duplicació de funcionalitats  
- revisar el codi dels companys  

---

## 📦 Producte a lliurar

Es parteix del projecte de l’sprint anterior, ampliant funcionalitat.

---

### 💻 1. Repositori GitHub

S’haurà d’entregar:

- Enllaç al repositori  
- Branca: `sprint3`  

El projecte ha d’incloure:

---

#### ✅ Funcionalitats obligatòries

### 🔐 Autenticació i autorització

- Login funcional  
- Validació contra backend  
- Control d’accés segons rol  

---

### 👥 Gestió d’usuaris

- Donar accés a usuaris  
- Bloquejar i desbloquejar usuaris  
- Crear i eliminar administradors  

---

### ✅ Validació de formularis

- Validació de camps obligatoris  
- Validació de formats  
- Formularis revisats abans d’enviar  

---

### 🌐 Comunicació amb servidor

- Peticions HTTP correctes  
- Validació de dades  
- Integració amb funcionalitats  

---

## 📄 2. Document individual

Cada alumne haurà de descriure:

- Treball realitzat  
- Aportació de cada membre  
- Funcionament del grup  

---

## ✅ Criteris de qualitat

En aquest sprint es valorarà especialment:

- Seguretat del projecte  
- Control correcte de rols  
- Validació de dades  
- Integració amb backend  
- Qualitat del codi  

👉 Es treballen especialment RA5 i RA7 【1-2db0cf】

---

## 📊 Rúbrica d’avaluació

Pots consultar la rúbrica completa en:

📥 ./rubriques/rubrica_sprint3.pdf

---

## 💡 Recomanacions

- No implementes el login “de mentida”  
- Prova bé els rols d’usuari  
- No deixes la validació per al final  
- Revisa tots els formularis del projecte  
- Prova casos d’error (usuari incorrecte, dades mal formades, etc.)  

---

## 🔗 Navegació

📄 Document general:
👉 link: ../README.md  

⬅️ Sprint anterior:
👉 link: ./sprint2.md  

➡️ Següent sprint:
👉 link: ./sprint4.md