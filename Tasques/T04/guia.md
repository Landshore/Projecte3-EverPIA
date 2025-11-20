GUIA LDAP 
 
Mirem  el status del sldap 
 
 
Comprovem que el directori s’ha creat com hem volgut. 
 
 
Fem la comanda: nano dpkg-reconfigure sldap 
 
 
Cliquem no. 
 
 
Posem aquesta (innovatech28.test) 
 
 
Posem inovatechxx (xx és num llista).


![Image 1: LDAP configuration step or command output](T04/img/01.png)

![Image 2: LDAP configuration step or command output](T04/img/02.png)

![Image 3: LDAP configuration step or command output](T04/img/03.png)

![Image 4: LDAP configuration step or command output](T04/img/04.png)

Posem la contrasenya (usuari) 
 
 
Posem que si 
 
 
Posem que si. 
 
 
Comprovem que el directori s’ha creat com hem volgut.


![Image 5: LDAP configuration step or command output](T04/img/05.png)

![Image 6: LDAP configuration step or command output](T04/img/06.png)

![Image 7: LDAP configuration step or command output](T04/img/07.png)

![Image 8: LDAP configuration step or command output](T04/img/08.png)

Primer creem fitxer: 
 
 
Posem aquestes modificacions: 
 
 
Aquesta commanda permet afegir elements al directori: 
 
 
Posem: 
 
 
Afegim aquest entrada


![Image 9: LDAP configuration step or command output](T04/img/09.png)

![Image 10: LDAP configuration step or command output](T04/img/10.png)

![Image 11: LDAP configuration step or command output](T04/img/11.png)

![Image 12: LDAP configuration step or command output](T04/img/12.png)

![Image 13: LDAP configuration step or command output](T04/img/13.png)

El busquem per assegurar 
 
 
Fem ldap search al atribut 
 
 
Fem aquesta comanda.  
 
Instal·lem account maneger: 
 
 
 
 
Obrim el LDAP account manager; editar perfils de servidor > posar contrasenya (lam)


![Image 14: LDAP configuration step or command output](T04/img/14.png)

![Image 15: LDAP configuration step or command output](T04/img/15.png)

![Image 16: LDAP configuration step or command output](T04/img/16.png)

![Image 17: LDAP configuration step or command output](T04/img/17.png)

![Image 18: LDAP configuration step or command output](T04/img/18.png)

Posem aquestes modificacions en el part de tipus de comptes actius (usuaris/grups). 
 
 
 
Creem un grup.


![Image 19: LDAP configuration step or command output](T04/img/19.png)

![Image 20: LDAP configuration step or command output](T04/img/20.png)

![Image 21: LDAP configuration step or command output](T04/img/21.png)

Guardem i regresem. 
 
 
 
 
 
Ara per tech 
 
 
Això és la llista de grups:


![Image 22: LDAP configuration step or command output](T04/img/22.png)

![Image 23: LDAP configuration step or command output](T04/img/23.png)

![Image 24: LDAP configuration step or command output](T04/img/24.png)

![Image 25: LDAP configuration step or command output](T04/img/25.png)

![Image 26: LDAP configuration step or command output](T04/img/26.png)

![Image 27: LDAP configuration step or command output](T04/img/27.png)

Anem a “nous usuaris” secció personal, i omplim cridencials. 
 
 
 
Aprop de la capaçela  “contrasenya”, i marquem la capçalera Unix i el guardem. 
 
Ara anem a l’apartat Unix i el guardem


![Image 28: LDAP configuration step or command output](T04/img/28.png)

![Image 29: LDAP configuration step or command output](T04/img/29.png)

![Image 30: LDAP configuration step or command output](T04/img/30.png)

![Image 31: LDAP configuration step or command output](T04/img/31.png)

Ara creem manager: 
 
 
 
Al Unix. 
 
 
Establim contrasenya i el guardem


![Image 32: LDAP configuration step or command output](T04/img/32.png)

![Image 33: LDAP configuration step or command output](T04/img/33.png)

![Image 34: LDAP configuration step or command output](T04/img/34.png)

![Image 35: LDAP configuration step or command output](T04/img/35.png)

Aqui podem veure la llista d’usuaris: 
 
 
Ara al part client (ZORIN) editem el fitxer “/etc/hosts”. 
 
 
Fem aquesta comanda per comprovar: 
 
 
Fem aquesta comanda:. 
 
 
Omplim el part que falta amb la nostra nom de server:


![Image 36: LDAP configuration step or command output](T04/img/36.png)

![Image 37: LDAP configuration step or command output](T04/img/37.png)

![Image 38: LDAP configuration step or command output](T04/img/38.png)

![Image 39: LDAP configuration step or command output](T04/img/39.png)

![Image 40: LDAP configuration step or command output](T04/img/40.png)

![Image 41: LDAP configuration step or command output](T04/img/41.png)

Fem més modificacions…


![Image 42: LDAP configuration step or command output](T04/img/42.png)

![Image 43: LDAP configuration step or command output](T04/img/43.png)

![Image 44: LDAP configuration step or command output](T04/img/44.png)

![Image 45: LDAP configuration step or command output](T04/img/45.png)

![Image 46: LDAP configuration step or command output](T04/img/46.png)

![Image 47: LDAP configuration step or command output](T04/img/47.png)

Comprovem 
 
 
Al part de client configurem el arxiu: 
 
 
Editem l’arxiu i elimin la línea use_autho


![Image 48: LDAP configuration step or command output](T04/img/48.png)

![Image 49: LDAP configuration step or command output](T04/img/49.png)

![Image 50: LDAP configuration step or command output](T04/img/50.png)

Perfecte: 
 
 
Fem un restart del servei: 
 
 
El reniciem: 
 
 
Mirem si tenim els clients.


![Image 51: LDAP configuration step or command output](T04/img/51.png)

![Image 52: LDAP configuration step or command output](T04/img/52.png)

![Image 53: LDAP configuration step or command output](T04/img/53.png)

![Image 54: LDAP configuration step or command output](T04/img/54.png)

![Image 55: LDAP configuration step or command output](T04/img/55.png)
