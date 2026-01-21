# GUIA DE DUPLICATI A SISTEMES OPERATIUS

## Configuració Inicial - Windows

### Instal·lació del Disc Dur

Instal·lem un disc dur de 10 GB:

![Configuració disc virtual](./img/i0.jpg)
*Diàleg de configuració del disc dur virtual*

![Paràmetres del disc](./img/i1.j)
*Paràmetres de mida del disc*

### Inicialització del Disc

Inicialitzem el disc:

![Gestió de discos](./img/i2)
*Finestra de gestió de discos de Windows*

Amb clic dret creem un nou volum:

![Menú contextual volum](./img/i3)
*Opció per crear nou volum simple*

Utilitzem tot el volum:

![Assignació de mida](./img/i4)
*Selecció de mida màxima del volum*

Assignem la lletra E (pot ser qualsevol):

![Lletra d'unitat](./img/i5)
*Assignació de lletra d'unitat E*

Format NTFS:

![Format NTFS](./img/i6)
*Configuració del sistema de fitxers NTFS*

![Finalització format](./img/i7)
*Confirmació del format del disc*

Ara tenim el nostre disc:

![Disc configurat](./img/i8)
*Disc E: configurat i operatiu*

![Vista de discos](./img/i9)
*Vista general dels discos del sistema*

### Instal·lació de Duplicati

Instal·lem:

![Fitxer instal·lador](./img/i10)
*Fitxer d'instal·lació de Duplicati*

![Procés instal·lació](./img/i11)
*Procés d'instal·lació en curs*

Escrivim això o obrim l'aplicació:

![Comanda localhost](./img/i12)
*Comanda per accedir a la interfície web*

Ens demana una frase de contrasenya:

![Contrasenya inicial](./img/i13)
*Diàleg de configuració de contrasenya*

I estem, ara en el bloc de "backups" fes clic a sobre l'icona "Add+": i cliquem a "afegir una nova còpia de seguretat".

![Pantalla principal Duplicati](./img/i14)
*Interfície principal de Duplicati*

![Menú afegir backup](./img/i15)
*Opció per afegir nova còpia de seguretat*

## Sub-Part: Creant un Backup Local

Posem el nom i la descripció per el nostre còpia de seguretat:

![Nom i descripció local](./img/i16)
*Configuració de nom i descripció del backup local*

Per la destinació seleccionem el sistema de fitxers > segon disc:

![Destinació local](./img/i17)
*Selecció del disc E: com a destinació*

Per l'origen posem C:/Users/Nom_d'usuari:

![Origen del backup](./img/i18)
*Selecció de la carpeta d'usuari com a origen*

Per l'horari posem a true; automàticament fer còpies de seguretat, pròxima hora qualsevol, tornar a fer cada 1 hores i per últim cada dia.

![Configuració horari](./img/i19)
*Programació automàtica del backup cada hora*

Per l'últim pas ho deixem per defecte.

**Nota important:** Les còpies de seguretat estan xifrades amb una contrasenya que s'ha establert a Duplicati, tant per al backup local com per al backup en el núvol, sense requerir configuracions avançades addicionals.

![Opcions finals](./img/i20)
*Configuració final del backup local*

## Sub-Part: Creant un Backup Cloud

Des de l'inici, afegirem una nova còpia de seguretat:

**Nota important:** Tenir una imatge ja pujat a /Documents per fer el pas de restauració.

![Nova còpia cloud](./img/i21)
*Inici de configuració de backup al núvol*

Posem nom i frase de contrasenya per la còpia de seguretat:

![Nom i contrasenya cloud](./img/i22)
*Configuració de credencials per al backup cloud*

Ara a la destinació per la còpia de seguretat busquem "Google Drive", cliquem al enllaç AuthID per deixar Duplicati accedir credencials, genererà un codi perquè pugui autoritzar a la nostra carpeta. Al camí de carpeta podem escriure un nom i el Duplicati ens en creara un de nou per nosaltres.

**Nota important:** Els fitxers de prova s'han creat prèviament a la carpeta Documents de l'usuari. Duplicati s'encarrega automàticament de pujar-los a Google Drive durant l'execució del backup, sense necessitat de copiar-los manualment al núvol.

![Configuració Google Drive](./img/i23)
*Selecció i autenticació amb Google Drive*

![AuthID Google](./img/i24)
*Enllaç d'autorització AuthID*

![Carpeta Google Drive](./img/i25)
*Configuració de la carpeta al Drive*

Per l'origen posem el nostre usuari on hi haurà els documents:

![Origen documents](./img/i26)
*Selecció de carpeta Documents com a origen*

L'horari; el pròxim hora serà a les 18:00h:

![Horari cloud](./img/i27)
*Programació del backup a les 18:00h*

Ara tenim les dues còpies de seguretat:

![Llista de backups](./img/i28)
*Vista amb ambdós backups configurats*

### Part de Local:

![Detalls backup local](./img/i29)
*Informació detallada del backup local*

### Part de Google Drive:

![Detalls Google Drive](./img/i30)
*Estat del backup a Google Drive*

![Carpeta al núvol](./img/i31)
*Carpeta creada automàticament al Drive*

## Prova de Restauració

### Sub-Part: Restauració Local

Per fer la prova de restauració primer pujem imatges a /Documents, executem la còpia de seguretat i els eliminem:

![Fitxers a Documents](./img/i32)
*Imatges de prova a la carpeta Documents*

![Carpeta amb imatges](./img/i33)
*Vista de les imatges abans d'eliminar*

![Execució backup](./img/i34)
*Execució del backup local*

![Icona papelera](./img/i35)
*Icona de la papelera de reciclatge*

Per assegurar que els hem eliminat anem a la papelera per eliminar-ho:

![Buidar papelera](./img/i36)
*Eliminació permanent des de la papelera*

### A RESTAURACIÓ LOCAL:

![Menú restauració local](./img/i37)
*Opció de restauració al backup local*

Fem seleccionem el fitxer que volem eliminar:

![Selecció fitxers](./img/i38)
*Selecció dels fitxers a restaurar*

Posem a sobreescriure el fitxer i a la ubicació original:

![Opcions restauració](./img/i39)
*Configuració per sobreescriure a ubicació original*

Comprovem:

![Verificació restauració](./img/i40)
*Comprovació de fitxers restaurats correctament*

### Sub-Part: Restauració Cloud

Per fer la prova de restauració, les imatges que estan en el document, els hem de eliminar també des de la paperera:

![Eliminació per cloud](./img/i41)
*Eliminació de fitxers per provar restauració cloud*

### A RESTAURACIÓ CLOUD:

![Menú restauració cloud](./img/i42)
*Accés a restauració des de Google Drive*

Seleccionem quines carpetes volem restaurar:

![Selecció carpetes cloud](./img/i43)
*Selecció de carpetes a restaurar del núvol*

Per la pas final podem seleccionar que rastauri en els fitxers previs i si volem sobreescriure o no.

![Opcions finals cloud](./img/i44)
*Configuració final de restauració cloud*

![Procés restauració](./img/i45)
*Procés de restauració en execució*

Verifiquem:

![Verificació cloud](./img/i46)
*Verificació de restauració des del núvol*

---

## PART LINUX

### Configuració del Sistema

L'apartat de Linux:

![Entorn Linux](./img/i47)
*Terminal i entorn de Linux*

![Disc Linux](./img/i48)
*Vista del disc addicional en Linux*

Verifiquem el 2n disc:

![Verificació disc](./img/i49)
*Comanda lsblk per verificar discos*

Creem una nova partició del tot:

![Eina fdisk](./img/i50)
*Creació de partició amb fdisk*

El formatajem en .xfs:

![Format XFS](./img/i51)
*Format del disc amb sistema XFS*

Creem el punt de muntatge:

![Crear directori](./img/i52)
*Creació de /media/backup*

El montem:

![Muntar disc](./img/i53)
*Comanda mount per muntar el disc*

Verifiquem:

![Verificar muntatge](./img/i54)
*Verificació del disc muntat correctament*

Fem muntatge:

![Configuració fstab](./img/i55)
*Edició de /etc/fstab per muntatge permanent*

![Resultat fstab](./img/i56)
*Entrada UUID al fitxer fstab*

Afegim usuaris:

![Crear usuaris](./img/i57)
*Comandes per afegir usuaris*

Creem 4 fitxers, cadascun de 10MB:

![Crear fitxers dd](./img/i58)
*Comanda dd per crear fitxers de prova*

![Fitxers creats](./img/i59)
*Llistat dels 4 fitxers de 10MB*

Verifiquem:

![Verificació fitxers](./img/i60)
*Verificació de mida dels fitxers*

### Backup amb Duplicati en Linux

Generem contrasenya:

![Generació contrasenya](./img/i61)
*Comanda openssl per generar contrasenya*

Fem una còpia de seguretat del /home a media backup:

![Comanda backup tar](./img/i62)
*Comanda tar per crear backup complet*

Part de contrasenya:

![Introducció contrasenya](./img/i63)
*Sol·licitud de contrasenya per xifrar*

Resultat final:

![Backup finalitzat](./img/i64)
*Arxiu de backup creat amb èxit*

Comprovem l'estat de les còpies:

![Llistat backups](./img/i65)
*Comanda ls per veure backups*

![Detalls backup](./img/i66)
*Informació detallada del fitxer de backup*

Esborrem l'arxiu:

![Eliminar fitxer](./img/i67)
*Comanda rm per eliminar fitxer de prova*

Restaurem:

![Comanda restore](./img/i68)
*Restauració amb gpg i tar*

![Verificar restore](./img/i69)
*Verificació de descompressió correcta*

Verifiquem:

![Comprovar fitxers](./img/i70)
*Comprovació de fitxers restaurats*

Creem un nou arxiu:

![Nou fitxer](./img/i71)
*Creació de fitxer5.txt de prova*

Fem una còpia incremental:

![Backup incremental](./img/i72)
*Comanda tar per backup incremental*

Comprovem:

![Llistat incremental](./img/i73)
*Verificació dels dos backups*

### Automatització amb Cron

Ara el desmontem:

![Desmuntar disc](./img/i74)
*Comanda umount per desmuntar*

Creem bashcript:

![Script bash](./img/i75)
*Edició de fullbackup.sh*

Fem això:

![Contingut script](./img/i76)
*Contingut complet del script de backup*

Fem sudo crontab -e i afegim aquesta línea:

![Configuració crontab](./img/i77)
*Entrada crontab per executar cada diumenge*

**Que és bàsicament:** diumenge a les 23h, minut 0, * qualsevol dia al mes, * qualsevol mes, 0 cada diumenge. Al /usr/local/bin/fullbackup.sh executem el script. >> var/log/fullbackup.log 2>&1 es guarda la sortida en aquell log per el final 2>&1 es guarda també els errors de log.

Comprovem:

![Verificació crontab](./img/i78)
*Visualització de tasques programades*

Donem permisos:

![Permisos execució](./img/i79)
*Comanda chmod per donar permisos*

Provem:

![Execució manual](./img/i80)
*Prova manual del script de backup*

Afegim aquesta línea a l'arxiu:

![Cron incremental](./img/i81)
*Línia per backup incremental diari*

Verifiquem:

![Crontab final](./img/i82)
*Configuració final de crontab*

**La part "0 23 * * 1-6"** = De dilluns (1) a dissabte (6) a les 23:00

La resta és igual (no canvia)

---

**Fi**
