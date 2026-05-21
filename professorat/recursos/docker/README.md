# 📘 Guia ràpida per a docents — Backend Karma amb Docker

## 🎯 Objectiu

Aquest document descriu de forma resumida com:

- Generar una nova versió per a Docker del paquet destinat a l'alumnat
- Posar en marxa el sistema  

Per a una informació completa, pots consultar la 'Guia per al desplegament del KarmaWebApi mitjançant Docker', que podràs trobar en aquest mateix directori.

---

# 🔧 1. Generar una nova versió per a Docker

## 🔹 1.1 Actualitzar backend (Visual Studio)

Després de modificar el codi:

Fer el publish des de Visual Studio o alternativament:

```bash
dotnet publish -c Release
```

👉 Copiar el contingut de la carpeta `/publish` en el paquet per a l'alumne, dins del directori:

```
/api
```

---

## 🔹 1.2 Actualitzar la base de dades

1. Generar un nou backup (.bak) des de SQL Server  
2. Substituir el fitxer:

```
backup/KarmaDB.bak
```

👉 (Opcional) revisar o actualitzar `init.sql`, si el que vols es realitzar modificacions en la BD existent, mitjançants scripts d'SQL.

---

## 🔹 1.3 Preparar el paquet

El paquet ha d’incloure:

- `docker-compose.yml`  
- `Dockerfile`  
- carpeta `api/` (backend acabat de compilar)  
- carpeta `backup/` (base de dades)  

---

# 🚀 2. Posar en marxa el sistema

## 🔹 Primera execució

```bash
docker-compose up -d
```

Esperar uns segons i executar:

```bash
docker exec sqlserver /opt/mssql-tools18/bin/sqlcmd -S localhost -U sa -P "Password123!" -C -i /var/opt/mssql/backup/init.sql
```

---

## 🔹 Execució habitual

```bash
docker-compose up -d
```

---

## 🔹 Parar sistema

```bash
docker-compose down
```

---

## 🔹 Reiniciar complet

```bash
docker-compose down -v
docker-compose up -d
```

---

# 🎯 Resum

- El backend es distribueix ja compilat  
- Docker gestiona l’execució  
- La base de dades es restaura només la primera vegada  

---

💥 **Amb aquests passos es pot generar i desplegar una nova versió del backend de forma ràpida i controlada.**
