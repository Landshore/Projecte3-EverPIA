# GUIA DE DUPLICATI A SISTEMES OPERATIUS

## Configuració Inicial del Disc

Instal·lem un disc dur de 10 GB:

![Disc dur 10GB](./img/0.png)

![Un segon disc afegida](./img/1.png)


Inicialitzem el disc:

![inicialitzar el disc](./img/2.png)


Amb clic dret creem un nou volum: 

![Utilitzar tot el volum](./img/3.png)


Utilitzem tot el volum: 

![Assignar lletra E](./img/4.png)

Assignem la lletra E (pot ser qualsevol):

![Assignar amb la lletra E.](./img/5.png)

Format NTFS:

![Disc configurat](./img/6.png)

## Instal·lació de Duplicati

Instal·lem:

![Instal·lació Duplicati](./img/7.png)

Escrivim això o obrim l'aplicació:

![Obrir aplicació](./img/8.png)

Ens demana una frase de contrasenya:

![Contrasenya inicial](./img/9.png)

I estem, ara en el block de "backups" fes clic a sobre l'icona "Add+": i cliquem a "afegir una nova còpia de seguretat".

![Afegir nova còpia](./img/10.png)

## Sub-Part: Creant un Backup Local

Posem el nom i la descripció per el nostre còpia de seguretat:

![Nom i descripció backup local](./img/11.png)

Per la destinació seleccionem el sistema de fitxers > segon disc:

![Destinació segon disc](./img/12.png)

Per l'origen posem C:/Users/Nom_d'usuari:

![Origen usuari](./img/13.png)

Per l'horari posem a true; automàticament fer còpies de seguretat, pròxima hora qualsevol, tornar a fer cada 1 hores i per últim cada dia.

![Configuració horari](./img/14.png)

Per l'últim pas ho deixem per defecte.

![Pas final](./img/15.png)

**Nota important:** Les còpies de seguretat estan xifrades amb una contrasenya que s'ha establert a Duplicati, tant per al backup local com per al backup en el núvol, sense requerir configuracions avançades addicionals.

## Sub-Part: Creant un Backup Cloud

Des de l'inici, afegirem una nova còpia de seguretat:

**Nota important:** Tenir una imatge ja pujat a /Documents per fer el pas de restauració.

Posem nom i frase de contrasenya per la còpia de seguretat:

![Nom i contrasenya backup cloud](./img/16.png)

Ara a la destinació per la còpia de seguretat busquem "Google Drive", cliquem al enllaç AuthID per deixar Duplicati accedir credencials, genererà un codi perquè pugui autoritzar a la nostra carpeta. Al camí de carpeta podem escriure un nom i el Duplicati ens en creara un de nou per nosaltres.

![Configuració Google Drive](./img/17.png)

**Nota important:** Els fitxers de prova s'han creat prèviament a la carpeta Documents de l'usuari. Duplicati s'encarrega automàticament de pujar-los a Google Drive durant l'execució del backup, sense necessitat de copiar-los manualment al núvol.

Per l'origen posem el nostre usuari on hi haurà els documents:

![Origen documents](./img/18.png)

L'horari; el pròxim hora serà a les 18:00h:

![Horari 18:00](./img/19.png)

Ara tenim les dues còpies de seguretat:

![Dues còpies creades](./img/20.png)

Part de Local:

![Backup local](./img/21.png)

Part de Google Drive:

![Backup Google Drive](./img/22.png)

## Prova de Restauració

### Sub-Part: Restauració Local

Per fer la prova de restauració primer pujem imatges a /Documents, executem la còpia de seguretat i els eliminem:

![Pujar i eliminar imatges](./img/23.png)

Per assegurar que els hem eliminat anem a la papelera per eliminar-ho:

![Eliminar de paperera](./img/24.png)

A RESTAURACIÓ LOCAL:

![Restauració local](./img/25.png)

Fem seleccionem el fitxer que volem eliminar:

![Seleccionar fitxer](./img/26.png)

Posem a sobreescriure el fitxer i a la ubicació original:

![Sobreescriure ubicació original](./img/27.png)

Comprovem:

![Verificació restauració](./img/28.png)

### Sub-Part: Restauració Cloud

Per fer la prova de restauració, les imatges que estan en el document, els hem de eliminar també des de la paperera:

![Eliminar imatges cloud](./img/29.png)

A RESTAURACIÓ CLOUD:

![Restauració cloud](./img/30.png)

Seleccionem quines carpetes volem restaurar:

![Seleccionar carpetes](./img/31.png)

Per la pas final podem seleccionar que rastauri en els fitxers previs i si volem sobreescriure o no.

![Opcions finals restauració](./img/32.png)

Verifiquem:

![Verificació cloud](./img/33.png)

## PART LINUX

L'apartat de Linux:

![Inici Linux](./img/34.png)

Verifiquem el 2n disc:

![Verificar 2n disc](./img/35.png)

Creem una nova partició del tot:

![Crear partició](./img/36.png)

El formatajem en .xfs:

![Format XFS](./img/37.png)

Creem el punt de muntatge:

![Punt de muntatge](./img/38.png)

El montem:

![Muntar disc](./img/39.png)

Verifiquem:

![Verificar muntatge](./img/40.png)

Fem muntatge:

![Configurar muntatge](./img/41.png)

Afegim usuaris:

![Afegir usuaris](./img/42.png)

Creem 4 fitxers, cadascun de 10MB:

![Crear fitxers 10MB](./img/43.png)

Verifiquem:

![Verificar fitxers](./img/44.png)

Generem contrasenya:

![Generar contrasenya](./img/45.png)

Fem una còpia de seguretat del /home a media backup:

![Backup home](./img/46.png)

Part de contrasenya:

![Part contrasenya](./img/47.png)

Resultat final:

![Resultat final backup](./img/48.png)

Comprovem l'estat de les còpies:

![Estat còpies](./img/49.png)

Esborrem l'arxiu:

![Esborrar arxiu](./img/50.png)

Restaurem:

![Restaurar arxiu](./img/51.png)

Verifiquem:

![Verificar restauració](./img/52.png)

Creem un nou arxiu:

![Crear nou arxiu](./img/53.png)

Fem una còpia incremental:

![Còpia incremental](./img/54.png)

Comprovem:

![Comprovar incremental](./img/55.png)

Ara el desmontem:

![Desmuntar](./img/56.png)

Creem bashcript:

![Crear bashscript](./img/57.png)

Fem això:

![Configurar script](./img/58.png)

Fem `sudo crontab -e` i afegim aquesta línea:

![Crontab configuració](./img/59.png)

Que és bàsicament; diumenge a les 23h, minut 0, * qualsevol dia al mes, * qualsevol mes, 0 cada diumenge. Al /usr/local/bin/fullbackup.sh executem el script. >> var/log/fullbackup.log 2>&1 es guarda la sortida en aquell log per el final 2>&1 es guarda també els errors de log.

Comprovem:

![Comprovar crontab](./img/60.png)

Donem permisos:

![Donar permisos](./img/61.png)

Provem:

![Provar script](./img/62.png)

Afegim aquesta línea a l'arxiu:

![Afegir línia](./img/63.png)

Verifiquem:

![Verificació final](./img/64.png)

La part " 0 23 * * 1-6 " = De dilluns (1) a dissabte (6) a les 23:00

La resta és igual (no canvia)

---

**Fi**
