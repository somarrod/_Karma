# Sprints del projecte Karma Cli

Aquest projecte es divideix en cinc sprints. El projecte es desenvolupa progressivament, ampliant i millorant en cadascun dels sprints la funcionalitat de l’aplicació.

Distribuïts de la següent manera:

1ª avaluació:

Sprint 1

Sprint 2

2ª avaluació:

Sprint 3

Sprint 4

Sprint 5



# Resum









# Sprint 1

## Objectiu general del sprint 1

Aquest sprint és el primer, pel que principalment és una presa de contacte amb els requisits del projecte Karma en sí mateix, i amb Angular.

L’sprint estarà centrat en dissenyar l’aspecte de l’aplicació, descriure les navegacions entre els diferents escenaris, i dissenyar els escenaris més rellevants de l’aplicació. 

Així mateix, haureu de crear la primera versió del projecte KarmaCli i el primer formulari corresponent a la pàgina principal amb un disseny atractiu i fàcil d’utilitzar. Aquesta pàgina principal tindrà un accés per a fer login (integrat o en un altra pàgina, com decidiu). De moment no s’espera que realitzen cap comunicació amb el servidor KarmaWebApi. 

## Descripció de l’sprint 1

Contingut:

Unitat 1: Introducció al desenvolupament i entorn de Treball

Introducció a l'assignatura i al projecte Karma. Explicació dels models de programació en entorns client/servidor. Capacitats i limitacions d'execució en navegadors web.

Característiques dels llenguatges script. Llenguatges de programació en entorn client. Integració del codi amb etiquetes HTML.

Unitat 2: Fonaments de TypeScript i Angular

Maneig de la sintaxi del llenguatge: etiquetes, variables, tipus de dades, conversions, literals, assignacions, operadors, expressions, comentaris.

Estructures de control de flux: blocs de codi, decisions, bucles. Convencions de format i codificació.

Utilització de ferramentes i entorns per facilitar la programació, la prova i la depuració del codi.

## Producte a lliurar 

Cada grup lliurarà els següents productes a la data de l’sprint: 

Un arxiu pdf que inclourà:

Nom del equip de treball

Disseny dels esbossos de l’aplicació

Una explicació dels problemes principals que han trobat fins ara i com els han solucionat.

Un link de github amb la branca : sprint1 que continga el projecte de angular funcional, i que incloga: 

L’estructura de l’aplicació, 

La pàgina de principal amb HTML, CSS i TypeScript

# Sprint 2

## Objectiu general del sprint

Durant aquest sprint, aprofundireu en l’ús dels objectes predefinits del llenguatge i les funcions definides per l’usuari, aplicant aquests coneixements en el projecte Karma mitjançant la creació de funcionalitats com la generació de text dinàmic o la interacció amb el navegador. També es treballarà la creació i manipulació d’arrays en Angular per gestionar col·leccions de dades, i s’introduirà la comunicació asíncrona amb el servidor mitjançant el servei HttpClient, realitzant peticions HTTP per obtenir i mostrar dades de l’API de Karma. A més, es posarà en pràctica la modificació dinàmica del document, la integració de llibreries d’actualització dinàmica i la revisió del codi per garantir-ne el bon funcionament. Finalment, es farà ús d’eines com Docker per posar en marxa el servidor i Postman o Swagger per explorar i provar les rutes de l’API, consolidant així una visió completa del desenvolupament d’aplicacions web dinàmiques.

## Descripció de l’sprint 2

Continguts:

Unitat 3: Objectes Predefinits d’Angular i Funcions  

Utilització d'objectes predefinits del llenguatge: interacció amb el navegador, generació de text i elements HTML, gestió de finestres i marcs.

Referència: https://xxjcaxx.github.io/libro_dwec/intro.html#objetos-predefinidos

Creació i utilització de funcions definides per l'usuari. Arrays: inicialització, recorregut, creació d'objectes, definició de mètodes i propietats.

Referència: https://xxjcaxx.github.io/libro_dwec/intro.html#funciones



Unitat 4: Comunicació asíncrona i aplicacions dinàmiques

Introducció a la comunicació asíncrona amb el servidor.

Referència: https://xxjcaxx.github.io/libro_dwec/intro.html#comunicacion-asincrona

Utilització de mecanismes de comunicació asíncrona: objectes, propietats i mètodes, recuperació remota d'informació, modificació dinàmica del document.

Desenvolupament d'aplicacions web dinàmiques: llibreries d'actualització dinàmica, avantatges i inconvenients de la comunicació asíncrona. 

Referència: https://xxjcaxx.github.io/libro_dwec/intro.html#aplicaciones-dinamicas

## Producte final del sprint 2

Es parteix del projecte desenvolupat en l’sprint anterior, mantenint l’estructura i funcionalitats ja implementades. 

És important haver introduït els comentaris fets per la professora en l’entrega anterior. I haver acabat possibles punts pendents de l’sprint 1.

S’entregarà: link a github amb la branca sprint2 del projecte en Angular, que incloga aquesta funcionalitat:

1. Menú principal

Creació d’un menú de navegació que apareix una vegada l’usuari ha accedit a l’aplicació (encara que de moment no es valide el login).

El menú ha d’adaptar-se al rol de l’usuari (administrador, professor o alumne), mostrant només les opcions corresponents a cada perfil.

2. Gestió d’usuaris i grups

Gestió bàsica

Consultes de dades d’alumnes, professors i grups

Creació de grups per a un curs escolar.

Alta d’alumnes i professors mitjançant formularis.

Edició de dades de grups, alumnes i professors.

Eliminació d’elements (grups, alumnes i professors) amb confirmació prèvia.

Gestió avançada

Assignació d’un professor com a tutor d’un grup.

Assignació d’alumnes a un grup concret.

Assignació de professors a grups per impartir assignatures.

 Funcionalitats avançades (opcional)

Implementació de la càrrega massiva d’alumnes i professors a través d’un fitxer o formulari múltiple, per facilitar la gestió de grans volums de dades.

3. Altres funcionalitats

Connexió amb KarmaWebApi

Generació dinàmica de contingut HTML (com taules o llistes) a partir de les dades obtingudes.

Interacció amb el navegador (per exemple, mostrar alertes, redireccionaments o accions sobre finestres).



Addicionalment s’entregarà el link a un vídeo de 10 minuts on s’explique la funcionalitat desenvolupada amb l’aplicació en funcionalment. El vídeo ha d’indicar específicament amb quin perfil d’usuari s’està logant (si és que és necessari). 



# Sprint 3

## Objectiu general de l’sprint 3

Durant aquest sprint, aprofundireu en la seguretat i la gestió d’usuaris dins d’una aplicació Angular, implementant sistemes d’autenticació i autorització que permeten controlar l’accés segons el rol de l’usuari (alumne, professor o administrador). També es treballarà la validació de formularis mitjançant Reactive Forms per garantir la integritat de les dades introduïdes. A més, es posarà en pràctica la verificació d’accés amb el servidor, incloent-hi la gestió de permisos, la creació i eliminació d’administradors, i la gestió d’accés dels usuaris. Aquest sprint permetrà consolidar coneixements clau per al desenvolupament d’aplicacions web segures i robustes.

## Descripció de l’sprint

Continguts:



Unitat 5: Autenticació i autorització en Angular

Explicació dels conceptes d’autenticació i autorització.

Implementació d’un sistema de login per a diferents rols d’usuari.

Control d’accés a funcionalitats segons el rol.

Revisió i depuració del codi d’autenticació.
Referència: https://xxjcaxx.github.io/libro_dwec/intro.html#autenticacion

Unitat 6: Validació de formularis en Angular

Introducció a la validació de formularis amb Reactive Forms.

Creació de formularis amb validació de camps (nom, cognoms, email, etc.).

Integració de la validació en el projecte Karma.

Revisió i depuració del codi de formularis.
Referència: https://xxjcaxx.github.io/libro_dwec/intro.html#formularios

## Producte final de l’sprint 3

Haureu d’entregar una nova branca del projecte (sprint3) que incloga les següents funcionalitats:

Autenticació i autorització

Sistema de login funcional per a alumnes, professors i administradors.

Control d’accés a les diferents seccions de l’aplicació segons el rol de l’usuari.

Validació de l’accés amb el servidor mitjançant peticions HTTP.

Configuració de permisos i restriccions d’accés.

Gestió d’usuaris i permisos

Donar accés a alumnes i professors.

Bloquejar o restablir l’accés a usuaris.

Crear nous administradors i eliminar-ne d’existents.



Validació de formularis

Formularis amb validació de camps obligatoris, formats i longituds.

Formulari de registre d’alumnes amb comprovació de dades abans d’enviar-les al servidor.

# Sprint 4

## Objectiu general de l’sprint 4

Durant aquest sprint, es treballarà amb més detall en la interacció amb l’usuari mitjançant la gestió d’esdeveniments, la manipulació del DOM i la validació de formularis, tant amb Angular com amb expressions regulars. També es treballarà la configuració de l’aplicació, incloent-hi la gestió de matèries, anys escolars i puntuacions. A més, es començarà a introduir la gestió d’estat i el testing en aplicacions Angular, amb l’objectiu de millorar la qualitat, mantenibilitat i robustesa del projecte Karma. Aquest sprint permetrà consolidar la interacció dinàmica amb l’usuari i preparar el projecte per a escenaris més avançats de desenvolupament.



## Descripció de l’sprint

Continguts:

Unitat 7: Interacció amb l’usuari i manipulació del DOM

Gestió d’esdeveniments i formularis.

Validació de formularis amb expressions regulars.

Accés i manipulació del DOM: creació i modificació d’elements HTML.

Referència: https://xxjcaxx.github.io/libro_dwec/intro.html#eventos

Manipulació del DOM amb Angular.

Esdeveniments

DOM, DOM amb Angular

Referència: https://xxjcaxx.github.io/libro_dwec/intro.html#dom

Referència: https://xxjcaxx.github.io/libro_dwec/intro.html#dom-angular

Unitat 8: Millorant el meu codi: Gestió d’Estats i Testing

Introducció al concepte de gestió d’estat.

Ús de serveis i patrons com Redux per mantenir l’estat de l’aplicació.
Referència: https://xxjcaxx.github.io/libro_dwec/intro.html#gestion-estado

Importància del testing en el desenvolupament web.

Eines com Jasmine i Karma per escriure i executar tests.

Referència: https://xxjcaxx.github.io/libro_dwec/intro.html#testing

## Producte final de l’sprint 4

Haureu d’entregar una nova branca del projecte (sprint4) que incloga les següents funcionalitats:

 1. Configuració general

Configuració de matèries o mòduls.

Definició de nivells màxims i mínims de Karma.

Configuració de privilegis i categories.

2. Configuració de l’any escolar

Alta d’un nou any escolar.

Desactivació d’un any escolar actiu.

Eliminació d’un any escolar existent.

3. Gestió de puntuacions

Afegir puntuació a un alumne concret.

Afegir puntuació a tot un grup.



S’ha de tenir en compte:

Formularis amb validació mitjançant expressions regulars.

Manipulació del DOM per afegir, editar i eliminar elements HTML.

Implementació d’un servei per gestionar l’estat global de l’aplicació (usuari autenticat, dades carregades, idioma per defecte, etc.).

Creació de tests unitaris per a components i serveis.

Fitxers creats per a fer testing (*spec.ts)

Documentació del projecte



També s’ha d’entregar un vídeo explicatiu de 10 minuts on s’expliquen els test realitzats i es puguen vore en execució.

# Sprint 5

## Objectiu general de l’sprint 5

Aquest sprint representa la fase final del projecte Karma. L’objectiu principal és optimitzar i completar l’aplicació, millorant-ne el rendiment, afegint suport multilingüe i implementant la gestió de privilegis per part dels usuaris. L’alumnat aplicarà tècniques d’optimització com el lazy loading i l’estratègia de detecció de canvis, i aprendrà a internacionalitzar l’aplicació per adaptar-la a diferents idiomes. A més, es prepararà l’aplicació per a la presentació final, assegurant que totes les funcionalitats estiguen implementades, revisades i funcionals.

## Descripció de l’sprint 6

Continguts

Unitat 9 – Millorant el meu codi:  Optimització i rendiment en Angular i Internacionalització i localització

Tècniques d’optimització: lazy loading, change detection strategy, divisió de mòduls, etc.

Referència: https://xxjcaxx.github.io/libro_dwec/intro.html#optimizacion

Ús del mòdul @angular/localize per adaptar l’aplicació a diversos idiomes.
Referència: https://xxjcaxx.github.io/libro_dwec/intro.html#internacionalizacion

## Producte final de l’sprint

L’alumnat haurà d’entregar una branca final del projecte (sprint5) que incloga l’aplicació funcional completa, optimitzada i preparada per a ser presentada. Aquesta branca ha d’incloure:

1. Gestió de privilegis

Consultar privilegis disponibles segons la puntuació de l’usuari.

Concedir privilegis a alumnes o professors.

Permetre que els usuaris gaudisquen dels privilegis obtinguts.

2. Consulta del Karma d’un alumne i d’un grup

2. Internacionalització

Implementació del suport multilingüe (valencià i castellà).

Traducció de textos estàtics i dinàmics de la interfície.

 3. Optimització del rendiment

Aplicació de tècniques com lazy loading de mòduls.

Optimització de la detecció de canvis i càrrega de components.

Millora de la velocitat de càrrega i fluïdesa de la navegació.



També hauran de: 

Fer una Presentació final

Cada grup (3 alumnes) presentarà el seu projecte davant la classe.

Les presentacions es realitzaran durant la setmana final (dilluns, dimarts, dijous i divendres).

Es valorarà la claredat, la funcionalitat i la qualitat del projecte presentat, així com l’atractiva que és.



Entregar un document en PDF individual on reflexionen sobre com ha segut la experiència, què els ha agradat i què no. Tenen la sensació d’haver aprés molt? O pensen que haveren aprés més d’un altra manera? Com ha funcionat el seu grup?