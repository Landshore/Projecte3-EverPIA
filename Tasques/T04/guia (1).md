GUIA LDAP 
 
Mirem  el status del sldap 
 
 
Comprovem que el directori s’ha creat com hem volgut. 
 
 
Fem la comanda: nano dpkg-reconfigure sldap 
 
 
Cliquem no. 
 
 
Posem aquesta (innovatech28.test) 
 
 
Posem inovatechxx (xx és num llista).


(img/01.png)

(img/02.png)

(img/03.png)

(img/04.png)

Posem la contrasenya (usuari) 
 
 
Posem que si 
 
 
Posem que si. 
 
 
Comprovem que el directori s’ha creat com hem volgut.


(img/05.png)

(img/06.png)

(img/07.png)

(img/08.png)

Primer creem fitxer: 
 
 
Posem aquestes modificacions: 
 
 
Aquesta commanda permet afegir elements al directori: 
 
 
Posem: 
 
 
Afegim aquest entrada


(img/09.png)

(img/10.png)

(img/11.png)

(img/12.png)

(img/13.png)

El busquem per assegurar 
 
 
Fem ldap search al atribut 
 
 
Fem aquesta comanda.  
 
Instal·lem account maneger: 
 
 
 
 
Obrim el LDAP account manager; editar perfils de servidor > posar contrasenya (lam)


(img/14.png)

(img/15.png)

(img/16.png)

(img/17.png)

(img/18.png)

Posem aquestes modificacions en el part de tipus de comptes actius (usuaris/grups). 
 
 
 
Creem un grup.


(img/19.png)

(img/20.png)

(img/21.png)

Guardem i regresem. 
 
 
 
 
 
Ara per tech 
 
 
Això és la llista de grups:


(img/22.png)

(img/23.png)

(img/24.png)

(img/25.png)

(img/26.png)

(img/27.png)

Anem a “nous usuaris” secció personal, i omplim cridencials. 
 
 
 
Aprop de la capaçela  “contrasenya”, i marquem la capçalera Unix i el guardem. 
 
Ara anem a l’apartat Unix i el guardem


(img/28.png)

(img/29.png)

(img/30.png)

(img/31.png)

Ara creem manager: 
 
 
 
Al Unix. 
 
 
Establim contrasenya i el guardem


(img/32.png)

(img/33.png)

(img/34.png)

(img/35.png)

Aqui podem veure la llista d’usuaris: 
 
 
Ara al part client (ZORIN) editem el fitxer “/etc/hosts”. 
 
 
Fem aquesta comanda per comprovar: 
 
 
Fem aquesta comanda:. 
 
 
Omplim el part que falta amb la nostra nom de server:


(img/36.png)

(img/37.png)

(img/38.png)

(img/39.png)

(img/40.png)

(img/41.png)

Fem més modificacions…


(img/42.png)

(img/43.png)

(img/44.png)

(img/45.png)

(img/46.png)

(img/47.png)

Comprovem 
 
 
Al part de client configurem el arxiu: 
 
 
Editem l’arxiu i elimin la línea use_autho


(img/48.png)

(img/49.png)

(img/50.png)

Perfecte: 
 
 
Fem un restart del servei: 
 
 
El reniciem: 
 
 
Mirem si tenim els clients.


(img/51.png)

(img/52.png)

(img/53.png)

(img/54.png)

(img/55.png)
