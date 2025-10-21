# Informe Tècnic: Comparativa de Gestors de Contrasenyes

## 🗝 KeePassXC

> “KeePassXC és una manera senzilla i segura d'autogestionar les teves contrasenyes. No replica exactament un gestor de contrasenyes en línia, però aquest és el punt”  
> — PCWorld :contentReference[oaicite:0]{index=0}

**Descripció:** KeePassXC és un gestor de contrasenyes offline que emmagatzema les credencials en un fitxer local xifrat (.kdbx). És una versió més moderna i amigable per a usuaris de l'original KeePass.

**Seguretat:** Utilitza xifratge AES-256 i SHA-256. Tot es manté local, proporcionant un control total sobre les dades. No requereix connexió a Internet per al seu funcionament bàsic.

**Usabilitat:** La interfície és senzilla però potent. La sincronització entre dispositius és manual i requereix coneixements tècnics. La funcionalitat de l'extensió del navegador és bàsica i pot requerir configuracions addicionals per optimitzar l'experiència.

**Pros:**
- Control total de les dades, 100% offline.
- Open source i portable.
- Compatible amb múltiples clients i eines addicionals.

**Contres:**
- Sincronització manual i més tècnica.
- Interfície menys intuïtiva.
- Funcionalitat limitada de l'extensió del navegador.

---

## 🔐 Bitwarden

> “Bitwarden és segur, open source, funciona a través de múltiples plataformes i ofereix un flux de treball intuïtiu que facilita la gestió de les teves contrasenyes a tots els teus dispositius”  
> — Wired :contentReference[oaicite:1]{index=1}

**Descripció:** Bitwarden és un gestor de contrasenyes basat en el núvol que ofereix sincronització automàtica entre dispositius, aplicacions natives per a diverses plataformes i extensions per a navegadors.

**Seguretat:** Utilitza xifratge AES-256 amb arquitectura zero-knowledge. El codi és open source i ha estat auditats per tercers, com Cure53, per garantir la seguretat :contentReference[oaicite:2]{index=2}.

**Usabilitat:** Ofereix una experiència d'usuari fluida amb suport per a passkeys, autenticació biomètrica i ompliment automàtic de formularis. Les aplicacions natives per a Android i iOS han millorat en velocitat i funcionalitat.

**Pros:**
- Open source amb auditories de seguretat.
- Sincronització automàtica entre dispositius.
- Generador de contrasenyes robust i configurable.

**Contres:**
- Depèn d'Internet per sincronitzar.
- Algunes diferències entre l'aplicació web i desktop poden confondre els usuaris novells.

---

## 📊 Comparativa Ràpida: KeePassXC vs Bitwarden

| Característica         | KeePassXC                              | Bitwarden                                 |
|------------------------|----------------------------------------|-------------------------------------------|
| Tipus                  | Offline / Fitxer local (.kdbx)         | Online / Núvol                            |
| Seguretat              | AES-256 + SHA-256, tot local           | AES-256, zero-knowledge, sincronització xifrada |
| Usabilitat             | Manual, tècnic, menys intuïtiu         | Intuïtiu, sincronització automàtica       |
| Sincronització         | Manual, via serveis de fitxers        | Automàtica, entre dispositius             |
| Extensió navegador     | Bàsica, funcionalitat limitada         | Avançada, amb ompliment automàtic         |
| Control de dades       | Total control local                    | Control a través del núvol amb xifratge   |
| Cost                   | Totalment gratuït                      | Gratuït amb opcions premium a $10/any     |

---

## ✅ Recomanació

Per al personal tècnic de l'empresa, **Bitwarden** és la millor opció, ja que combina seguretat robusta amb una usabilitat superior. La seva sincronització automàtica i suport multiplataforma faciliten la gestió de contrasenyes en entorns dinàmics i distribuïts. KeePassXC, tot i ser una opció sòlida per a usuaris que prioritzen el control total de les dades, requereix una gestió manual que pot ser menys eficient en un entorn empresarial.


