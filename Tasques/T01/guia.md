# Guia d'Ús Tècnica: Bitwarden
## Manual Operatiu per a l'Equip Tècnic d'EverPia

---

## 1. Instal·lació i Configuració Inicial

### 1.1. Registre i Creació del Compte

**Pas 1:** Entrem a la pàgina oficial de Bitwarden i seleccionem "Registrar".

![Pàgina principal de Bitwarden](img/image_0.png)

**Pas 2:** Introduïm el nostre correu electrònic.

![Introducció del correu electrònic](img/image_1.png)

**Pas 3:** El sistema ens notificarà que hem de verificar el correu electrònic.

![Notificació de verificació](img/image_2.png)

**Pas 4:** Creem el nostre compte seguint les instruccions rebudes al correu.

![Creació del compte](img/image_3.png)

---

## 2. Generació de Contrasenyes Segures

### 2.1. Accés al Generador de Contrasenyes

Bitwarden incorpora un generador de contrasenyes que permet crear credencials segures de forma automàtica.

![Generador de contrasenyes](img/image_4.png)

**Funcions disponibles:**
- Generar contrasenyes
- Generar frases de pas
- Generar noms d'usuari
- Historial de contrasenyes generades

### 2.2. Configuració de Paràmetres de Seguretat

Es recomana configurar les contrasenyes amb els següents paràmetres:

![Configuració de paràmetres](img/image_5.png)

**Opcions recomanades:**
- ✅ Lletres majúscules (A-Z)
- ✅ Lletres minúscules (a-z)
- ✅ Números (0-9)
- ✅ Caràcters especials (!@#$%^&*)
- **Longitud mínima:** 12-16 caràcters

---

## 3. Instal·lació de l'Extensió del Navegador

### 3.1. Descàrrega i Configuració

**Pas 7:** Instal·lem l'extensió de Bitwarden al navegador i l'obrim. Introduïm el correu i la contrasenya que vam utilitzar en crear el compte.

![Instal·lació de l'extensió](img/image_6.png)

---

## 4. Exemples d'Ús i Emplenament Automàtic

### 4.1. Crear un Nou Compte amb Bitwarden

**Pas 8:** Per crear un compte nou utilitzant Bitwarden, accedim al lloc web o aplicació desitjada.

![Creació de compte nou](img/image_7.png)

**Pas 9:** Obrim l'extensió i anem a l'apartat "Generador". Podem copiar la contrasenya o generar-ne una nova tantes vegades com vulguem.

![Ús del generador](img/image_8.png)

**Pas 10:** De manera automàtica, l'aplicació/extensió crearà i omplirà automàticament els credencials de connexió. També podem posar-la en un fitxer si volem. Després cliquem "Guardar".

![Emplenament automàtic](img/image_9.png)

### 4.2. Ajustar la Contrasenya segons Requisits

**Pas 11:** Si la contrasenya no compleix els requisits del servei (per exemple, necessita 8 caràcters sense espais i incloure un número, una lletra majúscula i una minúscula):

![Error de requisits](img/image_10.png)

Anem a "Generador" i marquem almenys aquestes opcions:
- **A-Z** (majúscules)
- **a-z** (minúscules)
- **0-9** (números)
- **Símbols** (opcional)

![Configuració ajustada](img/image_11.png)

### 4.3. Generador de Noms d'Usuari

**Pas 12:** Addicionalment, Bitwarden ofereix un generador de noms d'usuari. Es troba al mateix apartat del generador de contrasenyes (sub-apartat).

![Generador de noms d'usuari](img/image_12.png)

---

## 5. Gestió de Credencials a la Caixa Forta

### 5.1. Editar i Eliminar Credencials

**Pas 13:** A la "Caixa Forta", cliquem sobre la icona del lloc web/aplicació. Estarem a l'espai dels credencials d'aquella aplicació/web. Podem:
- Clicar sobre la icona de la paperera per eliminar de manera ràpida
- Modificar les credencials

![Gestió de credencials](img/image_13.png)

![Opcions de gestió](img/image_14.png)

![Detall de credencials](img/image_15.png)

---

## 6. Funció d'Emplenament Automàtic (Auto-Fill)

### 6.1. Activar Auto-Fill

**Pas 14:** Bitwarden permet utilitzar la funció "Auto-Fill", que omple de forma automàtica les dades de credencials. Cliquem sobre els tres punts i la funció apareixerà.

![Funció Auto-Fill](img/image_16.png)

**Pas 15:** Quan accedim a un lloc web, Bitwarden detectarà automàticament els camps de credencials i ens oferirà emplenar-los.

![Auto-Fill en ús](img/image_17.png)

![Credencials emplenades](img/image_18.png)

---

## 7. Gestió de Còpies de Seguretat (Backup)

### 7.1. Exportar la Caixa Forta

És fonamental realitzar còpies de seguretat periòdiques de les nostres contrasenyes.

**Pas 1:** Anem a "Configuració".

![Menú de configuració](img/image_19.png)

**Pas 2:** Seleccionem "Opcions de la caixa forta".

![Opcions de la caixa forta](img/image_20.png)

**Pas 3:** Cliquem a "Exporta caixa forta". Podem triar exportar en format **.json** o **.csv**.

![Exportar caixa forta](img/image_21.png)

**Pas 4:** El sistema demanarà la contrasenya mestra per confirmar l'operació.

![Confirmació de contrasenya](img/image_22.png)

**Pas 5:** El fitxer quedarà desat al nostre dispositiu.

![Fitxer exportat](img/image_23.png)

---

## 8. Bones Pràctiques per a Còpies de Seguretat

### 8.1. Recomanacions de Seguretat

✅ **Freqüència de còpies:**
- Fes una còpia nova cada 3-6 mesos
- Esborra les còpies antigues després de verificar les noves

✅ **Emmagatzematge segur:**
- **Opció 1:** Clau USB xifrada (recomanat per a màxima seguretat)
- **Opció 2:** Servei de núvol amb xifratge (Nextcloud, Tresorit, etc.)
- **MAI guardar còpies sense xifrar en ubicacions accessibles**

✅ **Verificació:**
- Comprova que el fitxer s'obre correctament abans de tancar la sessió
- Assegura't que les dades exportades són completes i llegibles

⚠️ **IMPORTANT:** Les còpies de seguretat contenen totes les contrasenyes en text xifrat o pla (segons el format). Mantingues-les sempre protegides.

---

## Resum de Funcions Principals

| Funció | Descripció |
|--------|------------|
| **Generador de contrasenyes** | Crea contrasenyes segures i úniques automàticament |
| **Auto-Fill** | Emplena automàticament els camps de credencials |
| **Caixa Forta** | Emmagatzema i organitza totes les credencials |
| **Sincronització** | Manté les contrasenyes actualitzades en tots els dispositius |
| **Exportació** | Permet fer còpies de seguretat en format .json o .csv |

---

## Suport i Recursos Addicionals

- 📚 [Documentació oficial de Bitwarden](https://bitwarden.com/help/)
- 🔐 [Configurar 2FA (Autenticació de Doble Factor)](https://bitwarden.com/help/setup-two-step-login/)
- 💼 Per a suport intern, contacteu amb l'equip tècnic d'EverPia

---

**Data de creació:** Octubre 2025  
**Versió:** 1.0  
**Revisat per:** Equip Tècnic EverPia
