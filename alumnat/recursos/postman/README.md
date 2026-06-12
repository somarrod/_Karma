# 🧪 Guia bàsica de Postman

## 📌 Què és Postman?

Postman és una eina molt utilitzada en desenvolupament de programari que permet **provar i treballar amb APIs** (interfícies de programació d'aplicacions).

Amb Postman podem:
- Enviar peticions HTTP (GET, POST, PUT, DELETE…)
- Visualitzar les respostes del servidor
- Comprovar si una API funciona correctament
- Organitzar proves en col·leccions

És especialment útil en el desenvolupament backend i en la integració entre serveis.


## 💻 Descàrrega i instal·lació

Pots obtindre Postman des del seu lloc web oficial:

👉 https://www.postman.com/downloads/

Postman està disponible per als principals sistemes operatius:
- **Windows**
- **macOS**
- **Linux**

També existeix una **versió web**, que pots utilitzar sense instal·lació.

### ✅ Recomanació

Per a treballar en local amb comoditat, es recomana instal·lar la versió d’escriptori, ja que ofereix millor rendiment i accés complet a totes les funcionalitats.

## ⚙️ Conceptes bàsics

Abans de començar a utilitzar Postman, és important conéixer alguns conceptes fonamentals:

- **Request (petició)** → és la crida que fem a una API
- **Response (resposta)** → és la resposta que ens retorna el servidor
- **Endpoint** → és la URL de la API a la qual fem la petició

### 🌐 Mètodes HTTP més habituals

- `GET` → obtindre dades
- `POST` → enviar dades noves
- `PUT` / `PATCH` → actualitzar dades
- `DELETE` → eliminar dades

Estos mètodes defineixen el tipus d’operació que volem realitzar sobre el servidor.

### 🧠 Idea clau

Quan utilitzem Postman, el que fem bàsicament és simular el comportament d’una aplicació client (com un navegador o una app), enviant peticions a una API i analitzant les respostes.


## 🚀 Com utilitzar Postman

### 1. Crear una col·lecció

Les col·leccions permeten organitzar les peticions dins d’un projecte.

- Ves a **New → Collection**
- Assigna un nom (per exemple: `Karma API`)

👉 Les col·leccions funcionen com carpetes on guardar totes les requests relacionades.

---

### 2. Crear una petició

- Fes clic en **New → HTTP Request**
- Selecciona el mètode (GET, POST, etc.)
- Escriu la URL de l’endpoint

Exemples:
```
POST https://localhost:5100//api/alumne/crear
```
o
```
GET {{baseUrl}}/api/categoria/llista
```
---

### 3. Configurar la petició

Una request pot incloure diferents parts:

- **Params** → paràmetres en la URL (no els utilitzem)
- **Headers** → informació addicional (tokens, tipus de contingut…) (no els modifiquem)
- **Body** → dades que s’envien (normalment en format JSON) (aquestos sí que els emprem!)

Exemple de body en JSON:
```
{
    "idTipusCategoria": 100,
    "descripcio": "Excel·lent comportament. Molt col·laborativa.",
    "numpunts": "5",
    "editable": true,
    "comentaris": null
}
```
---

### 4. Enviar la petició

- Fes clic en **Send**
- Observa la resposta en la part inferior de la pantalla

---

### 5. Analitzar la resposta

Després d’enviar la petició, podràs veure:

- **Status** → codi de resposta (200, 404, 500…)
- **Body** → dades retornades (habitualment JSON)
- **Headers** → informació tècnica de la resposta
- **Temps de resposta**

---

### 6. Guardar la petició

- Desa la request dins d’una col·lecció per reutilitzar-la posteriorment
---

## 🌍 Ús d’entorns

Postman permet utilitzar **entorns (environments)** per definir variables reutilitzables.

Per exemple:
```
{{baseUrl}}
```

Açò et permet canviar fàcilment entre diferents entorns:
- Desenvolupament (localhost)
- Producció (servidor real)

👉 Així no has de modificar totes les peticions manualment.

---

## ✅ Flux de treball recomanat

Quan treballes amb Postman, si estàs creant peticions, és recomanable seguir este procés:

1. Crear una col·lecció 
2. Crear les peticions necessàries  
3. Configurar mètode, URL i entorn (enviroment)
4. Afegir headers i/o body  
5. Enviar la petició  
6. Analitzar la resposta  
7. Guardar els resultats  

Si estàs modificant o provant peticions, és recomanable seguir este procés:

1. Obrir una col·lecció existent
2. Seleccionar una petició
3. validar mètode, URL i entorn  (enviroment)
4. Modificar body o Id en l'endpoint
5. Enviar la petició  
6. Analitzar la resposta  
7. Guardar els resultats  

---

## 📚 + Informació

💡 Aquesta guia és una introducció bàsica. Postman també permet automatitzar proves, treballar amb col·leccions avançades i integrar-se amb processos de desenvolupament més complexos.

- https://www.redsauce.net/es/articulo?post=postman-guia-rapida-principiantes  
- https://apidog.com/es/blog/beginners-postman-tutorial-3/  
- https://mundoqa.com/wp-content/uploads/2026/04/guia_postman_api_testing.pdf  

