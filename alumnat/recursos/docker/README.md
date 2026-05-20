# 🚀 Karma Backend — Guia ràpida per a l'alumnat

Aquestes instruccions et permetran obtindre el backend complet (**API + Base de Dades**) necessari per a treballar en el desenvolupament de la teua client.

---

## 📁 Estructura del projecte

```text
docker/
│
├── docker-compose.yml      # Configuració dels serveis (BD + API)
├── Dockerfile              # Definició del contenidor de l'API
├── README.md               # Guia per a l'alumnat (aquesta guia)
│
├── backup/                 # Carpeta amb la base de dades inicial
│   ├── KarmaDB.bak         # Backup de la base de dades
│   └── init.sql            # Script per restaurar la base de dades
│
└── api/                    # Backend ja compilat (no editable)
    ├── KarmaWebAPI.dll
    ├── KarmaWebAPI.deps.json
    ├── KarmaWebAPI.runtimeconfig.json
    ├── appsettings.json
    └── (altres fitxers generats amb `dotnet publish`)
```

---

## ✅ Requisits

Només necessites instal·lar:

- **Docker Desktop**  
  👉 https://www.docker.com/products/docker-desktop/  
  👉 Instal·la seguint els passos per defecte

---

## ✅ Requisits opcionals

- **SQL Server Management Studio (SSMS)**  
  👉 https://learn.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms  

---

## 🚀 Posada en marxa

### 1. Obrir terminal

Obri una terminal (cmd o PowerShell) en la carpeta:

```bash
docker
```

---

### 2. Arrancar el sistema

```bash
docker-compose up -d
```

⏳ Espera uns **10–15 segons** després d'arrancar.

---

### 3. Restaurar la base de dades *(només la primera vegada)*

```bash
docker exec sqlserver /opt/mssql-tools18/bin/sqlcmd -S localhost -U sa -P "Password123!" -C -i /var/opt/mssql/backup/init.sql
```

✅ Has de vore un missatge similar a:

```text
RESTORE DATABASE successfully processed ...
```

👉 Açò crea la base de dades i carrega les dades inicials.

---

### 4. Reiniciar el sistema

```bash
docker-compose down
docker-compose up -d
```

---

### 5. Verificar contenidors

Comprova en **Docker Desktop** que estan en marxa:

- `sqlserver`
- `karma-api`

---

### 6. Accedir a l’API

Obri el navegador:

👉 http://localhost:5000/swagger

---

### 7. Accés a la base de dades *(opcional però recomanat)*

Configura la connexió en **SSMS**:

- **Server type:** Database Engine  
- **Server name:** `localhost,1433` ⚠️ (amb coma)  
- **Authentication:** SQL Server Authentication  
- **Login:** `sa`  
- **Password:** `Password123!`  

---

## 🔁 Ús habitual

Cada vegada que vulgues treballar:

```bash
docker-compose up -d
```

✅ **No cal tornar a restaurar la base de dades**

---

## 🛑 Parar el sistema

```bash
docker-compose down
```

👉 Para el sistema però **manté les dades**

---

## ⚠️ Reiniciar des de zero

```bash
docker-compose down -v
```

👉 Elimina totes les dades de la base de dades

🔁 Després hauràs de repetir el **pas 3**.

---

## 💡 Notes importants

- Si un contenidor no està actiu, pots iniciar-lo des de Docker Desktop
- L'API necessita que la base de dades estiga en marxa
- La restauració només es fa la primera vegada o després d’un reset

---

✅ Ja pots començar a treballar en el teu client 🚀
