# Informe Tècnic: Comparativa de Gestors de Contrasenyes

## Introducció i Justificació

Les contrasenyes febles o reutilitzades són un risc crític per a l'empresa. Poden ser explotades mitjançant atacs de diccionari, força bruta o credential stuffing.  
L'ús d'un gestor de contrasenyes validat garanteix credencials úniques i robustes, reduint el risc de compromís dels comptes i millorant la seguretat general del projecte.

## Reviews de les Eines

### Bitwarden (Online / Núvol)

**Cita destacada:**  
“Bitwarden és segur, open source, funciona a través de múltiples plataformes i ofereix un flux de treball intuïtiu que facilita la gestió de les teves contrasenyes a tots els teus dispositius.” — Wired

**Descripció:**  
Bitwarden és un gestor de contrasenyes basat en el núvol amb sincronització automàtica entre dispositius, aplicacions natives i extensions per a navegadors.

**Seguretat:**  
- Xifratge AES-256 amb zero-knowledge.  
- Open source i auditats per tercers.

**Usabilitat:**  
- Interfície clara i intuïtiva.  
- Ompliment automàtic de formularis i suport per a passkeys.  
- Funciona en diverses plataformes i dispositius.

**Pros:**  
- Sincronització automàtica entre dispositius.  
- Generador de contrasenyes robust.  
- Open source amb auditories externes.

**Contres:**  
- Depèn d’Internet per sincronitzar.  
- Diferències menors entre app web i desktop poden confondre els usuaris novells.

---

### KeePassXC (Offline / Fitxer Local .kdbx)

**Cita destacada:**  
“KeePassXC és una manera senzilla i segura d'autogestionar les teves contrasenyes. Tot queda local i controlat pel propi usuari.” — PCWorld

**Descripció:**  
Gestor offline que emmagatzema contrasenyes en un fitxer local xifrat (.kdbx), portable i compatible amb múltiples clients.

**Seguretat:**  
- Xifratge AES-256 i SHA-256.  
- Tot es manté local, sense necessitat d’Internet.

**Usabilitat:**  
- Interfície simple però menys intuïtiva.  
- Sincronització manual entre dispositius.  
- Extensions del navegador limitades.

**Pros:**  
- Control total de les dades.  
- Open source i portable.  
- Compatible amb múltiples plataformes.

**Contres:**  
- Sincronització manual, requereix coneixements tècnics.  
- No té sincronització automàtica ni ompliment avançat de formularis.  

---

## Comparativa Ràpida

| Característica         | Bitwarden                           | KeePassXC                          |
|------------------------|------------------------------------|-----------------------------------|
| Tipus                  | Online / Núvol                     | Offline / Fitxer local (.kdbx)    |
| Seguretat              | AES-256, zero-knowledge, sincronització xifrada | AES-256 + SHA-256, tot local      |
| Usabilitat             | Intuïtiu, sincronització automàtica | Manual, més tècnic                 |
| Sincronització         | Automàtica entre dispositius       | Manual, via serveis de fitxers     |
| Extensió navegador     | Completa, ompliment automàtic      | Bàsica, funcionalitat limitada     |
| Control de dades       | Núvol xifrat                        | Totalment local                     |
| Cost                   | Gratuït amb opcions premium        | Totalment gratuït                  |

---

## Recomanació

Per al personal tècnic de l'empresa, **Bitwarden** és la millor opció: combina seguretat robusta amb facilitat d'ús i sincronització automàtica entre dispositius, facilitant la gestió de contrasenyes en entorns empresarials.  
**KeePassXC** és recomanable per a usuaris que prioritzin el control total de les dades i disposin de coneixements tècnics per gestionar sincronització manual.
