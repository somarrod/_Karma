🚀 Karma Backend — Guia ràpida per a l'alumnat

Aquestes intruccions et permetran obtindre el backend complet (API + Base de Dades) necessari per a treballar en el desenvolupament de la teua client.

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
    └── (altres fitxers generats amb dotnet publish)


✅ Requisits
Només necessites tenir instal·lat: Docker Desktop
	https://www.docker.com/products/docker-desktop/
👉 Instal·lar seguint els passos per defecte.
	
✅ Requisits opcionals
Instal·lar SQL Server Management Studio (SSMS)
   https://learn.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms
   

🚀 Posada en marxa
1. Obrir terminal cmd en la carpeta 'docker'

2. Arrancar el sistema
       docker-compose up -d
⏳ Una vegada ha acabat, espera uns 10–15 segons més

3. Restaurar la base de dades (NOMÉS LA PRIMERA VEGADA)

docker exec sqlserver /opt/mssql-tools18/bin/sqlcmd -S localhost -U sa -P "Password123!" -C -i /var/opt/mssql/backup/init.sql
Has de vore un missatge similar a aquest: RESTORE DATABASE successfully processed 857 pages in 0.262 seconds (25.530 MB/sec).
👉 Açò crea la base de dades i carrega les dades inicials existents

4. Reiniciar el sistema
	docker-compose down
	docker-compose up -d
	
5. Verificar en Docker Desktop que els contenidors sqlserver i karma-api estan iniciats

6. Accedir a l’API
Obri el navegador i valida que tens accés a swagger:
	http://localhost:5000/swagger	

7.  Accés a la base de dades (opcional però recomanat)
	Obrir el SSMS i configurar la connexió amb les dades:
	Server type: Database Engine
	Server name: localhost,1433 (⚠️ Atenció que s'utilitza una coma per a separar)
	Authentication: SQL Server Authentication	
	Login: sa
	Password: Password123!

🔁 A partir d'ara...
Cada vegada que vulgues treballar:
	docker-compose up -d
✅ No s'ha de repetir la restauració de la base de dades

🛑 Parar el sistema
	docker-compose down
👉 Això para el sistema però manté les dades

⚠️ Reiniciar des de zero (opcional)
	docker-compose down -v
👉 Això elimina totes les dades de la base de dades i torna a l’estat inicial
Després hauràs de repetir el pas 3.

