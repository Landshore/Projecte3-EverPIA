# Guia de Configuració LDAP

Aquesta guia explica el procés complet de configuració d'un servidor LDAP i la configuració del client.

## Configuració del Servidor

### 1. Comprovar l'estat de SLDAP
![Estat SLDAP](./img/01.png)

*Verificar que el servei SLDAP s'està executant correctament*

### 2. Verificar la creació del directori
![Verificació del directori](./img/02.png)

*Confirmar que l'estructura del directori LDAP s'ha creat correctament*

### 3. Reconfigurar SLDAP
![Comanda Dpkg Reconfigure](./img/03.png)

*Executar la comanda de reconfiguració: `dpkg-reconfigure sldap`*

### 4. Assistent de configuració - Pas 1
![Opció No](./img/04.png)

*Seleccionar "No" a la pregunta inicial*

### 5. Establir el nom del domini
![Configuració del domini](./img/05.png)

*Introduir el domini: `innovatech28.test`*

### 6. Nom de l'organització
![Nom de l'organització](./img/06.png)

*Establir el nom de l'organització: `inovatechxx` (on xx és el teu número de llista)*

### 7. Contrasenya de l'administrador
![Contrasenya Admin](./img/07.png)

*Establir la contrasenya de l'administrador (usuari)*

### 8. Confirmacions
![Confirmació Sí](./img/08.png)

*Confirmar amb "Sí" per ambdues preguntes*

### 9. Verificar l'estructura del directori
![Comprovació final del directori](./img/09.png)

*Confirmar que el directori s'ha creat correctament*

## Creació de fitxers LDIF

### 10. Crear el primer fitxer
![Crear fitxer LDIF](./img/10.png)

*Crear el fitxer de configuració LDIF inicial*

### 11. Modificacions del fitxer
![Modificacions LDIF](./img/11.png)

*Afegir les modificacions necessàries al fitxer LDIF*

### 12. Comanda per afegir elements
![Comanda LDAP Add](./img/12.png)

*Utilitzar la comanda ldapadd per inserir elements al directori*

### 13. Afegir entrada
![Afegir dades d'entrada](./img/13.png)

*Afegir la nova entrada al directori LDAP*

### 14. Verificació amb cerca
![Cerca LDAP](./img/14.png)

*Cercar al directori per verificar que l'entrada s'ha afegit*

### 15. Cerca d'atribut
![Cerca d'atribut](./img/15.png)

*Cercar atributs específics a LDAP*

### 16. Executar comanda de cerca
![Execució de comanda de cerca](./img/16.png)

*Executar la comanda de cerca per recuperar dades*

## Configuració de LDAP Account Manager

### 17. Instal·lar Account Manager
![Instal·lar Account Manager](./img/17.png)

*Instal·lar el paquet LDAP Account Manager*

### 18. Obrir la interfície LAM
![Login LAM](./img/18.png)

*Accedir a la interfície web de LDAP Account Manager i editar perfils de servidor*

### 19. Contrasenya del perfil de servidor
![Contrasenya del perfil de servidor](./img/19.png)

*Introduir la contrasenya de configuració de LAM: `lam`*

### 20. Configuració de tipus de comptes
![Configuració de tipus de comptes](./img/20.png)

*Configurar els tipus de comptes actius (usuaris/grups)*

## Creació de Grups

### 21. Crear grup
![Crear nou grup](./img/21.png)

*Crear un nou grup a LDAP*

### 22. Guardar i tornar
![Guardar grup](./img/22.png)

*Guardar la configuració del grup i tornar al menú principal*

### 23. Grup Tech
![Grup Tech](./img/23.png)

*Configurar el grup tech*

### 24. Llista de grups
![Llistat de grups](./img/24.png)

*Veure la llista completa de grups creats*

## Creació d'Usuaris

### 25. Secció de nous usuaris
![Nou usuari personal](./img/25.png)

*Navegar a la secció "Nous usuaris" i omplir les credencials personals*

### 26. Capçalera de contrasenya Unix
![Capçalera contrasenya Unix](./img/26.png)

*Prop de la capçalera de contrasenya, marcar la capçalera Unix i guardar*

### 27. Configuració de la secció Unix
![Secció Unix](./img/27.png)

*Configurar i guardar la configuració de la secció Unix*

### 28. Crear usuari manager
![Crear Manager](./img/28.png)

*Crear un compte d'usuari manager*

### 29. Configuració Unix del manager
![Manager Unix](./img/29.png)

*Configurar les opcions Unix per al compte manager*

### 30. Establir contrasenya del manager
![Contrasenya Manager](./img/30.png)

*Establir la contrasenya per al manager i guardar*

### 31. Llista d'usuaris
![Llistat d'usuaris](./img/31.png)

*Veure la llista completa d'usuaris creats*

## Configuració del Client (Zorin OS)

### 32. Editar fitxer hosts
![Editar Hosts](./img/32.png)

*Al client (ZORIN), editar el fitxer `/etc/hosts`*

### 33. Comanda de verificació
![Verificar connexió](./img/33.png)

*Executar comanda per verificar la connectivitat*

### 34. Comanda addicional
![Comprovació addicional](./img/34.png)

*Executar comanda de verificació addicional*

### 35. Configuració del nom del servidor
![Nom del servidor](./img/35.png)

*Omplir les parts que falten amb el nom del teu servidor*

### 36. Més modificacions
![Més modificacions](./img/36.png)

*Fer modificacions de configuració addicionals*

### 37. Comprovació de verificació
![Verificar configuració](./img/37.png)

*Verificar tota la configuració*

### 38. Configurar fitxer del client
![Configuració fitxer client](./img/38.png)

*Configurar el fitxer de configuració del client*

### 39. Eliminar línia use_autho
![Eliminar línia](./img/39.png)

*Editar el fitxer i eliminar la línia `use_autho`*

### 40. Configuració perfecta
![Configuració perfecta](./img/40.png)

*Configuració completada amb èxit*

### 41. Reiniciar servei
![Reiniciar servei](./img/41.png)

*Reiniciar el servei LDAP*

### 42. Reinicialitzar servei
![Reinicialitzar servei](./img/42.png)

*Reinicialitzar el servei*

### 43. Comprovar clients
![Comprovar clients](./img/43.png)

*Verificar que els clients estan connectats correctament*

## Resum

Aquesta guia cobreix:
- Instal·lació i configuració del servidor LDAP
- Creació de l'estructura de directoris
- Gestió de fitxers LDIF
- Configuració de LDAP Account Manager
- Creació de grups i usuaris
- Configuració del client a Zorin OS
- Verificació del servei i resolució de problemes

Tots els fitxers de configuració i comandes s'executen amb els permisos adequats i es verifiquen a cada pas.
