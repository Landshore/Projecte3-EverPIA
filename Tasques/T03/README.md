# T03: Gestió flexible de discos – Windows Storage Spaces

## Objectiu
Dissenyar i documentar una solució d’emmagatzematge flexible, redundant i escalable per al client **Garriga i Associats** utilitzant **Windows Storage Spaces**.  
L’objectiu és demostrar alta disponibilitat, facilitat de gestió i opcions de resiliència (mirall i paritat) en un entorn virtual.

---

## Descripció del projecte
Aquest projecte simula l’entorn de servidors del client amb **discs virtuals** afegits a una màquina virtual Windows 11.  
S’han creat **Storage Pools** i **Storage Spaces** amb diferents nivells de resiliència per:

- Garantir la protecció de les dades davant fallades de disc.  
- Permetre l’ampliació de l’espai sense interrupcions.  
- Facilitar la gestió centralitzada de l’emmagatzematge.

---

## Contingut de la carpeta tasca03
- [windows-storage.md](windows-storage.md) – Documentació completa del procés Windows Storage Spaces, amb captures, passos i explicacions.
- Captures de pantalla i evidències de la demostració.

---

## Notes importants
- Tots els discos virtuals utilitzats per a Storage Spaces són **simulats** en una VM.  
- Aquest README és l’entrada principal del projecte i conté els enllaços als documents detallats per cada sistema operatiu.  
- La demostració final es realitzarà amb la VM Windows 11 amb els Storage Spaces configurats.

---

## Enllaços
- [Documentació Windows Storage Spaces](windows-storage.md)  
- [Documentació Linux LVM](linux-lvm.md) *(si s’aplica)*
