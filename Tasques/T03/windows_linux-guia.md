# Guia Linux + Windows — Gestió Flexible de Discos  
## T03 – LVM (Linux) i Storage Spaces (Windows)

Aquesta guia explica, pas a pas, com realitzar la gestió flexible d’emmagatzematge en dos sistemes operatius:

- **Linux (LVM – Logical Volume Manager)**
- **Windows (Storage Spaces / Espais d’emmagatzematge)**

Inclou totes les imatges de l’activitat, enumerades del 01 al 61, i amb una breu explicació per a cada captura.

---

# 🐧 PART 1 — LINUX: LVM (Logical Volume Manager)

---

## 1. Configuració inicial de discos

![01](./img/01.png)
> Creació de la màquina virtual i entorn inicial.

![02](./img/02.png)
> Afegim dos discos virtuals nous de 10GB.

![03](./img/03.png)
> Vista dels discos creats en el panell de configuració.

![04](./img/04.png)
![05](./img/05.png)
> Confirmació que els discos extra han estat afegits correctament.

![06](./img/06.png)
> Sortida de `fdisk -l` mostrant *sdb* i *sdc* com a discos nous.

---

## 2. Creació de PV, VG i LV

![07](./img/07.png)
![08](./img/08.png)
![09](./img/09.png)
![10](./img/10.png)
> Creació dels volums físics (`pvcreate`) i del grup de volums (`vgcreate volgrup /dev/sdb /dev/sdc`).

---

## 3. Creació del volum lògic

![11](./img/11.png)
![12](./img/12.png)
> Creació del LV `lvCB01` amb 200MiB dins del grup `volgrup`.

---

## 4. Formatació, muntatge i configuració de fstab

![13](./img/13.png)
![14](./img/14.png)
> Creem la carpeta de muntatge `/mnt/lvm_dades`.

![15](./img/15.png)
![16](./img/16.png)
![17](./img/17.png)
![18](./img/18.png)
> Formatació en ext4, muntatge i afegit al fitxer `/etc/fstab` per muntatge automàtic.

---

## 5. Alta disponibilitat — Mirroring

![19](./img/19.png)
![20](./img/20.png)
![21](./img/21.png)
![22](./img/22.png)
> Eliminem configuració anterior: desmuntar, esborrar LV i VG.

![23](./img/23.png)
> Creació del nou VG `lvm_mirror` i volum amb mirroring:  
> `lvcreate -L 200M -m1 -n mirrorlv lvm_mirror`

---

## 6. Instantànies (Snapshots)

![24](./img/24.png)
![25](./img/25.png)
![26](./img/26.png)
![27](./img/27.png)
> Creació del volum origen (`origin`) i formatació.

![28](./img/28.png)
![29](./img/29.png)
![30](./img/30.png)
![31](./img/31.png)
![32](./img/32.png)
> Creació de la snapshot `lv_snapshot` a partir del volum `origin`.

![33](./img/33.png)
![34](./img/34.png)
![35](./img/35.png)
![36](./img/36.png)
![37](./img/37.png)
![38](./img/38.png)
![39](./img/39.png)
> Restauració de la snapshot i verificació de l’estat original.

---

## 7. Escalabilitat — Ampliació i Reducció de LVs

![40](./img/40.png)
![41](./img/41.png)
![42](./img/42.png)
> Ús de `lvextend`, `lvreduce`, `resize2fs` i `e2fsck` per gestionar l’espai del volum.

---

# 🪟 PART 2 — WINDOWS: Storage Spaces

---

## 8. Creació de discos i Storage Pool

![43](./img/43.png)
![44](./img/44.png)
![45](./img/45.png)
> Afegim tres discos virtuals de 10GB a la màquina Windows.

![46](./img/46.png)
![47](./img/47.png)
![48](./img/48.png)
> Creació del *Storage Pool* inicial.

---

## 9. Mirroring — "Dades_Miralls"

![49](./img/49.png)
![50](./img/50.png)
![51](./img/51.png)
![52](./img/52.png)
> Creació del volum amb resiliència tipus mirall (doble còpia) i prova d'eliminació d’un disc.

---

## 10. Paritat — "Dades_Paritat"

![53](./img/53.png)
![54](./img/54.png)
![55](./img/55.png)
> Creació del volum amb resiliència de paritat: més capacitat útil que el mirall.

---

## 11. Triple Mirall — "Dades_TripleMirall"

![56](./img/56.png)
> Afegim dos discos addicionals i els inicialitzem.

![57](./img/57.png)
![58](./img/58.png)
> Creació del volum amb *triple mirall*, tolerància a fallada de 2 discos.

---

## 12. Consulta d’estat amb PowerShell

![59](./img/59.png)
![60](./img/60.png)
![61](../img/61.png)
> Comandes utilitzades:
> ```powershell
> Get-StoragePool
> Get-VirtualDisk
> ```
> Mostra l’estat del pool i dels discos virtuals.

---

# 🔍 Comparació Final: Linux vs Windows

| Característica           | Linux (LVM) | Windows (Storage Spaces) |
|--------------------------|-------------|---------------------------|
| Snapshots                | ✔ Sí        | ✖ No                      |
| Mirroring                | ✔ Sí        | ✔ Sí                      |
| Paritat                  | ✔ RAID      | ✔ Natiu                   |
| Triple Mirall            | ✖ No        | ✔ Sí                      |
| Ampliació/Reeduccció     | ✔ Potent    | ✔ Però limitada           |
| CLI                      | Molt completa | Moderada (PowerShell)    |
| GUI                      | No integrada | ✔ Sí                      |
| Complexitat              | Alta         | Baixa                     |
| Flexibilitat             | Molt alta    | Mitjana                   |

---

# 📝 Conclusions

Aquesta pràctica ha permès entendre dues aproximacions molt diferents a la gestió flexible d’emmagatzematge:

- **Linux LVM** destaca per potència, flexibilitat i funcionalitats avançades com les snapshots.
- **Windows Storage Spaces** destaca per simplicitat, automatització i les diferents opcions de mirroring (incloent triple mirall).

Ambdós sistemes permeten construir entorns replicats, escalables i tolerants a fallades, cadascun amb les seves fortaleses.

---

**Fi del document.**
