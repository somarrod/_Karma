## 📘 Guia ràpida per a docents

### 🎯 Objectiu
- Generar una nova versió del paquet Docker destinat a l'alumnat  
- Posar en marxa el sistema  

Per a una informació completa, consulta la *Guia per al desplegament del KarmaWebApi mitjançant Docker* disponible en aquest mateix directori.

---

## 🔧 1. Generar una nova versió del paquet Docker per a l'alumnat

### 🔹 1.1 Actualitzar el backend (Visual Studio)

Després de modificar el codi:

- Fer el *publish* des de Visual Studio  
- O alternativament:

```bash
dotnet publish -c Release
```

👉 Copiar tot el contingut de la carpeta `/publish` en el paquet per a l’alumne dins del directori:

```bash
/api
```

---

### 🔹 1.2 Actualitzar la base de dades

- Generar un nou backup (`.bak`) des de SQL Server  
- Substituir el fitxer:

```bash
backup/KarmaDB.bak
```

👉 (Opcional) Revisar o actualitzar `init.sql` si vols fer modificacions sobre la BD existent mitjançant scripts SQL.  

---

### 🔹 1.3 Preparar el paquet

El paquet ha d’incloure:

- `docker-compose.yml`  
- `Dockerfile`  
- carpeta `api/` (backend compilat)  
- carpeta `backup/` (base de dades + `init.sql`)  

---

## 🚀 2. Posar en marxa el sistema

### 🔹 Primera execució

```bash
docker-compose up -d
```

Esperar uns segons (15-20) i executar:

```bash
docker exec sqlserver /opt/mssql-tools18/bin/sqlcmd -S localhost -U sa -P "Password123!" -C -i /var/opt/mssql/backup/init.sql
```

Accedir a Swagger per validar:

```
http://localhost:5000/swagger
```

---

### 🔹 Execució habitual

```bash
docker-compose up -d
```

---

### 🔹 Parar sistema

```bash
docker-compose down
```

---

### 🔹 Reiniciar Docker completament

```bash
docker-compose down -v
docker-compose up -d
```

---

## 🎯 Resum

- El backend es distribueix ja compilat  
- La base de dades es restaura només la primera vegada o quan hi ha una nova versió  

💥 **Amb aquests passos es pot generar i desplegar una nova versió del backend de forma ràpida i controlada.**
