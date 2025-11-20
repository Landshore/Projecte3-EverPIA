# Guia de Configuració LDAP

Aquesta guia explica el procés complet de configuració d'un servidor LDAP i la configuració del client.

## Configuració del Servidor

### 1. Mirar l'estat del sldap
![Estat SLDAP](./img/01.png)
*Verificar que el servei SLDAP s'està executant correctament*

### 2. Comprovar que el directori s'ha creat com hem volgut
![Verificació del directori](./img/02.png)
*Confirmar que l'estructura del directori LDAP s'ha creat correctament*

### 3. Fer la comanda: nano dpkg-reconfigure sldap
![Comanda Dpkg Reconfigure](./img/03.png)
*Executar la comanda de reconfiguració: `dpkg-reconfigure sldap`*

### 4. Cliquem no
![Opció No](./img/04.png)
*Seleccionar "No" a la pregunta inicial*

### 5. Posem aquesta (innovatech28.test)
![Configuració del domini](./img/05.png)
*Introduir el domini: `innovatech28.test`*

### 6. Posem inovatechxx (xx és num llista)
![Nom de l'organització](./img/06.png)
*Establir el nom de l'organització: `inovatechxx` (on xx és el teu número de llista)*

### 7. Posem la contrasenya (usuari)
![Contrasenya Admin](./img/07.png)
*Establir la contrasenya de l'administrador (usuari)*

### 8. Posem que si
![Primera confirmació Sí](./img/08.png)
*Confirmar amb "Sí"*

### 9. Posem que si
![Segona confirmació Sí](./img/09.png)
*Confirmar amb "Sí" novament*

### 10. Comprovar que el directori s'ha creat com hem volgut
![Comprovació final del directori](./img/10.png)
*Confirmar que el directori s'ha creat correctament*

## Creació de fitxers LDIF

### 11. Primer creem fitxer
![Crear fitxer LDIF](./img/11.png)
*Crear el fitxer de configuració LDIF inicial*

### 12. Posem aquestes modificacions
![Modificacions LDIF](./img/12.png)
*Afegir les modificacions necessàries al fitxer LDIF*

### 13. Aquesta comanda permet afegir elements al directori
![Comanda LDAP Add](./img/13.png)
*Utilitzar la comanda ldapadd per inserir elements al directori*

### 14. Posem
![Posar dades](./img/14.png)
*Introduir les dades necessàries*

### 15. Afegim aquesta entrada
![Afegir entrada](./img/15.png)
*Afegir la nova entrada al directori LDAP*

### 16. El busquem per assegurar
![Cerca per assegurar](./img/16.png)
*Cercar per assegurar que l'entrada s'ha afegit correctament*

### 17. Fem ldap search al atribut
![Cerca LDAP a l'atribut](./img/17.png)
*Fer una cerca LDAP a l'atribut específic*

### 18. Fem aquesta comanda
![Executar comanda](./img/18.png)
*Executar la comanda de cerca*

## Configuració de LDAP Account Manager

### 19. Instal·lem account manager
![Instal·lar Account Manager](./img/19.png)
*Instal·lar el paquet LDAP Account Manager*

### 20. Obrim el LDAP account manager; editar perfils de servidor > posar contrasenya (lam)
![Obrir LAM i posar contrasenya](./img/20.png)
*Accedir a la interfície web de LDAP Account Manager, editar perfils de servidor i introduir la contrasenya: `lam`*

### 21. Posem aquestes modificacions en el part de tipus de comptes actius (usuaris/grups)
![Configuració de tipus de comptes](./img/21.png)
*Configurar els tipus de comptes actius (usuaris/grups)*

## Creació de Grups

### 22. Creem un grup
![Crear nou grup](./img/22.png)
*Crear un nou grup a LDAP*

### 23. Guardem i regresem
![Guardar grup](./img/23.png)
*Guardar la configuració del grup i tornar al menú principal*

### 24. Ara per tech
![Grup Tech](./img/24.png)
*Configurar el grup tech*

### 25. Això és la llista de grups
![Llista de grups](./img/25.png)
*Veure la llista completa de grups creats*

## Creació d'Usuaris

### 26. Anem a "nous usuaris" secció personal, i omplim credencials
![Nous usuaris - Secció personal](./img/26.png)
*Navegar a la secció "Nous usuaris", apartat personal, i omplir les credencials*

### 27. Apropde la capçalera "contrasenya", i marquem la capçalera Unix i el guardem
![Capçalera Unix contrasenya](./img/27.png)
*Prop de la capçalera "contrasenya", marcar la capçalera Unix i guardar*

### 28. Ara anem a l'apartat Unix i el guardem
![Apartat Unix](./img/28.png)
*Anar a l'apartat Unix i guardar*

### 29. Ara creem manager
![Crear Manager](./img/29.png)
*Crear un compte d'usuari manager*

### 30. Al Unix
![Manager Unix](./img/30.png)
*Configurar les opcions Unix per al manager*

### 31. Establim contrasenya i el guardem
![Contrasenya Manager](./img/31.png)
*Establir la contrasenya per al manager i guardar*

### 32. Aquí podem veure la llista d'usuaris
![Llista d'usuaris](./img/32.png)
*Veure la llista completa d'usuaris creats*

## Configuració del Client (ZORIN)

### 33. Ara al part client (ZORIN) editem el fitxer "/etc/hosts"
![Editar /etc/hosts](./img/33.png)
*Al client (ZORIN), editar el fitxer `/etc/hosts`*

### 34. Fem aquesta comanda per comprovar
![Comanda per comprovar](./img/34.png)
*Executar comanda per comprovar la configuració*

### 35. Fem aquesta comanda
![Fer comanda](./img/35.png)
*Executar aquesta comanda*

### 36. Omplim el part que falta amb la nostra nom de server
![Omplir nom del servidor](./img/36.png)
*Omplir les parts que falten amb el nom del teu servidor*

### 37. Fem més modificacions…
![Més modificacions](./img/37.png)
*Fer modificacions de configuració addicionals*

### 38. Comprovem
![Comprovar](./img/38.png)
*Comprovar la configuració*

### 39. Al part de client configurem el arxiu
![Configurar arxiu del client](./img/39.png)
*Configurar l'arxiu del client*

### 40. Editem l'arxiu i eliminem la línea use_autho
![Eliminar línia use_autho](./img/40.png)
*Editar l'arxiu i eliminar la línia `use_autho`*

### 41. Perfecte
![Perfecte](./img/41.png)
*Configuració completada correctament*

### 42. Fem un restart del servei
![Restart del servei](./img/42.png)
*Fer un restart del servei LDAP*

### 43. El reiniciem
![Reiniciar](./img/43.png)
*Reiniciar el servei*

### 44. Mirem si tenim els clients
![Comprovar clients](./img/44.png)
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
### 45. Configuració PAM per autenticació LDAP
![Configuració PAM per autenticació LDAP](./img/45.png)
*Configuració PAM per autenticació LDAP*

### 46. Edició de fitxer nsswitch.conf
![Edició de fitxer nsswitch.conf](./img/46.png)
*Edició de fitxer nsswitch.conf*

### 47. Configuració del mòdul PAM
![Configuració del mòdul PAM](./img/47.png)
*Configuració del mòdul PAM*

### 48. Afegir línies a pam.d/common-auth
![Afegir línies a pam.d/common-auth](./img/48.png)
*Afegir línies a pam.d/common-auth*

### 49. Afegir línies a pam.d/common-account
![Afegir línies a pam.d/common-account](./img/49.png)
*Afegir línies a pam.d/common-account*

### 50. Afegir línies a pam.d/common-password
![Afegir línies a pam.d/common-password](./img/50.png)
*Afegir línies a pam.d/common-password*

### 51. Afegir línies a pam.d/common-session
![Afegir línies a pam.d/common-session](Projecte3-EverPIA/Tasques/T04/img/51.png)
*Afegir línies a pam.d/common-session*

### 52. Comprovació de configuració PAM
![Comprovació de configuració PAM](./img/52.png)
*Comprovació de configuració PAM*

### 53. Reiniciar serveis LDAP i PAM
![Reiniciar serveis LDAP i PAM](./img/53.png)
*Reiniciar serveis LDAP i PAM*

### 54. Verificació final amb comandes ldapsearch
![Verificació final amb comandes ldapsearch](./img/54.png)
*Verificació final amb comandes ldapsearch*

### 55. Llista final d'usuaris i grups LDAP
![Llista final d'usuaris i grups LDAP](./img/55.png)
*Llista final d'usuaris i grups LDAP*
