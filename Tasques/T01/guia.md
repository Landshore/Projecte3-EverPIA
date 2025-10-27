# Tasca 01: Gestor de Contrasenyes

## Breu Descripció

**⚠️ ALERTA!!** EverPia ha estat atacada per ciberdelinqüents. La consultora on esteu de becaris ha patit una fuita d'informació (data breach) i informació confidencial sobre un projecte que està en fase de desenvolupament està ara en mans de delinqüents que amenacen amb publicar-la si no es paga un rescat.

Òbviament, això ha causat una gran alarma dins la companyia i s'ha creat un comitè de crisi per gestionar la situació.

La investigació interna ha revelat que un dels comptes tècnics va ser compromès a causa de l'ús d'una contrasenya feble o reutilitzada.

## Resposta de la Direcció Tècnica

Com a resposta a aquesta crisi, la Direcció Tècnica ha emès una directriu: tot el personal tècnic ha de començar a utilitzar un gestor de contrasenyes validat per garantir l'ús de credencials úniques i robustes.

**La vostra tasca:** Avaluar les opcions i crear la documentació necessària per a la formació del personal.

---

## Fase 1: Anàlisi i Justificació (Document d'Informe)

Heu de redactar un informe que justifiqui tècnicament la decisió de la Direcció i comparin les opcions. Aquest informe ha d'incloure:

### 1. Introducció i Justificació

- Explicació de per què les contrasenyes febles o reutilitzades són un risc crític per a l'empresa (atac de diccionari, credential stuffing, etc.)
- La funció crucial d'un gestor de contrasenyes per mitigar aquests riscos

### 2. Comparativa Tècnica

Realitzeu una taula comparativa detallada entre:

#### Bitwarden (Alternativa Online / Núvol)
Analitzeu:
- La sincronització
- El model de seguretat (xifratge end-to-end)
- La facilitat d'accés des de múltiples dispositius
- El cost/model freemium

#### KeePassX / KeePassXC (Alternativa Offline / Escriptori)
Analitzeu:
- L'emmagatzematge local de l'arxiu (KDBX)
- La independència del núvol
- El model open source
- La portabilitat de l'arxiu

### 3. Avantatges i Inconvenients

Resumiu els principals pros i contres de cada model (online vs. offline) des del punt de vista de:
- Seguretat
- Usabilitat
- Continuïtat del negoci

### 4. Recomanació

Concloeu l'informe escollint l'eina que considereu més adequada per al personal tècnic de l'empresa i justifiqueu la vostra elecció.

---

## Fase 2: Guia d'Ús Tècnica (Manual Operatiu)

Utilitzant l'eina que heu seleccionat a la Fase 1 (Bitwarden, KeePassX, o similar), heu de crear una Guia d'Ús per a l'Equip Tècnic. Aquesta guia ha de ser clara i basada en captures de pantalla i instruccions pas a pas.

### Punts Obligatoris

#### 1. Instal·lació i Configuració Inicial
- Descàrrega
- Instal·lació
- Creació de la BBDD principal o compte mestre

#### 2. Generació de Contrasenyes Segures
- Explicació de com utilitzar el generador de contrasenyes de l'eina
- Paràmetres: longitud, caràcters especials

#### 3. Exemples d'Ús i Emplenament Automàtic
- Com desar una credencial d'un compte de correu electrònic
- Com desar una credencial d'una aplicació o servei web
- Com fer servir l'extensió del navegador per emplenar automàticament les dades

#### 4. Gestió de Còpies de Seguretat (Backup)
- Explicació detallada de com fer una còpia de seguretat de l'arxiu de contrasenyes (KDBX en KeePass o Exportació en Bitwarden)
- Recomanació de la millor pràctica per emmagatzemar aquesta còpia de seguretat de forma segura (clau USB xifrada o emmagatzematge xifrat al núvol)

---

## Què Caldrà Lliurar?

**⚠️ Es tracta d'una tasca individual**

Dins el repositori del `projecte-3` heu de crear una carpeta anomenada `tasca01`, dins d'ella heu de tenir:

### Estructura de Fitxers
```
tasca01/
├── README.md          # Descripció de la tasca i enllaços als arxius
├── informe.md         # Informe corresponent a la Fase 1
├── guia.md            # Guia d'ús corresponent a la Fase 2
└── img/               # Carpeta amb les imatges de la guia
    ├── imatge01.png
    ├── imatge02.png
    └── ...
```

### Arxius Requerits

- **README.md**: Descripció de la tasca i enllaços als arxius de l'informe i la guia
- **informe.md**: Document d'informe (Fase 1)
- **guia.md**: Manual operatiu (Fase 2)
- **img/**: Carpeta específica amb les imatges que inclogui la guia

> ⚠️ **Important:** Les imatges que inclogui la guia han d'estar a dins una carpeta específica (img, pics, etc.)

---

## Materials i Links de Suport

- [INCIBE: Gestión de contraseñas seguras](https://www.incibe.es/)
- [Pàgina oficial de Bitwarden](https://bitwarden.com/)
- [Pàgina oficial de KeePassXC](https://keepassxc.org/)
- [INCIBE: Gestores de contraseñas: qué son y cómo pueden mejorar la seguridad de las empresas](https://www.incibe.es/)

---

## Resum de les Fases

| Fase | Lliurable | Contingut |
|------|-----------|-----------|
| **Fase 1** | `informe.md` | Anàlisi tècnica, comparativa i recomanació |
| **Fase 2** | `guia.md` | Manual operatiu amb captures de pantalla |
