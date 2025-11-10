# 📹 P06: Vídeo + Auditoria DNS — Fonaments i Diagnosi del Sistema de Noms de Domini

## 🧩 Descripció breu
Aquesta activitat forma part del projecte de formació i auditoria encarregat per **DigiCore** a **EverPia**, amb l’objectiu d’explicar i analitzar els **fonaments del sistema de noms de domini (DNS)** i de demostrar, a la pràctica, com es pot diagnosticar el seu funcionament.

El projecte es divideix en dues fases:
1. **Vídeo formatiu (fase teòrica):** Explicació visual dels conceptes bàsics del DNS.
2. **Auditoria CLI (fase pràctica):** Diagnosi tècnica utilitzant eines com `dig` i `nslookup`.

---

## 🎯 Objectius específics
- Comprendre i explicar els **conceptes fonamentals del DNS**.  
- Saber **diagnosticar i analitzar problemes de resolució de noms** amb eines CLI.  
- Desenvolupar **competències tècniques i comunicatives** en l’àmbit de les xarxes.  
- Crear **materials formatius i tècnics de qualitat professional**, útils per a entorns corporatius.

---

## 🧠 Continguts tractats al vídeo (fase teòrica)
- Què és el **DNS** i per què és essencial per al funcionament d’internet.  
- Estructura jeràrquica del sistema de noms (Root → TLD → Segon nivell).  
- Tipus de **servidors DNS** (recursiu, autoritatiu, primari i secundari).  
- Tipus de **zones** (directa, inversa, primària i secundària).  
- Principals **registres DNS** (A, AAAA, CNAME, MX, NS, SRV).  
- Procés de **resolució iterativa i recursiva**.  
- Conceptes essencials: **Resposta autoritativa, TTL, SOA, Reenviadors, mDNS**.

---

🎬 Activitats

📂 Enllaç al vídeo (Google Drive):
[🔗 https://drive.google.com/drive/folders/1VR-PIk7s3nmpXX5_eFc4a9dDM6ubm5KL?usp=drive_link
]

📁 Enllaç a la tasca
[🔗 https://drive.google.com/drive/folders/13TcxvGVCROX_xjcKyqAzBBkk0Bpcqnp1?usp=drive_link
]
---

## 🧰 Fase Pràctica: Auditoria DNS amb Eines CLI

### 🔧 Entorn de proves
- **Sistema operatiu:** Zorin OS (Linux)
- **Configuració de xarxa:**  
  - Interfície 1: NAT  
  - Interfície 2: Adaptador pont (IP configurada segons indicacions dels responsables)

---

### 🧩 Eines utilitzades
- `dig` (Linux / macOS)
- `nslookup` (Windows / Linux / macOS)

---

### 🔹 Comanda 1: Consulta bàsica de registre A
```bash
dig xtec.cat A
