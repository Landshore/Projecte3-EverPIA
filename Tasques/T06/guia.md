# Fase Pràctica: Diagnosi de Noms (Auditoria amb CLI)

## Comanda 1: Consulta Bàsica de Registre A

**Comanda executada:**
```bash
dig xtec.cat A
```

![im1](img/im1.png)
*Captura del terminal amb la comanda `dig xtec.cat A`, mostrant la resposta del servidor DNS amb la IP 83.247.151.214, el TTL de 1281 segons i el servidor 127.0.0.53 que ha respost. Es veuen les seccions QUESTION, ANSWER i les estadístiques de la consulta.*

### Anàlisi Comanda 1:

- **IP de resposta:** 83.247.151.214
- **Valor TTL:** 1281 segons (≈ 21 minuts)
- **Servidor que ha respost:** 127.0.0.53 (systemd-resolved local)
- **Status:** NOERROR (consulta resolta correctament)

---

## Comanda 2: Consulta de Servidors de Noms (NS)

**Comanda executada:**
```bash
dig tecnocampus.cat NS
```

![im2](img/im2.png)
*Captura del terminal amb la comanda `dig tecnocampus.cat NS`, mostrant 4 servidors de noms autoritatius d'Amazon AWS (ns-1071.awsdns-05.org, ns-130.awsdns-16.com, ns-1689.awsdns-19.co.uk, ns-535.awsdns-02.net) amb els seus TTL de 10887 segons. La secció ADDITIONAL mostra les IPs IPv4 i IPv6 de cada servidor NS.* ns-130.awsdns-16.com, ns-1689.awsdns-19.co.uk, ns-535.awsdns-02.net) amb els seus TTL de 10887 segons. La secció ADDITIONAL mostra les IPs IPv4 i IPv6 de cada servidor NS.*

### Quins són els servidors de noms autoritatius?

1. ns-1071.awsdns-05.org
2. ns-130.awsdns-16.com
3. ns-1689.awsdns-19.co.uk
4. ns-535.awsdns-02.net

- **Total:** 4 servidors NS (per redundància i alta disponibilitat)
- **Tots són servidors d'Amazon AWS** (awsdns)
- **TTL:** 10887 segons

---

## Comanda 3: Consulta Detallada SOA

**Comanda executada:**
```bash
dig escolapia.cat SOA
```

![im3](img/im3.png)
*Captura del terminal amb la comanda `dig escolapia.cat SOA`, mostrant el registre SOA amb el servidor de noms primari (dns1.nominalia.com), el correu de l'administrador (root.dns1.nominalia.com), el número de sèrie (1761028965) i els paràmetres de sincronització (REFRESH 86400, RETRY 7200, EXPIRE 2592000, MINIMUM 300).*

### Quin és el correu de l'administrador?

- **Correu de l'administrador:** root@dns1.nominalia.com (el punt es converteix en @)
- **Número de sèrie del domini:** 1761028965
- **Servidor de noms primari:** dns1.nominalia.com
- **TTL del registre SOA:** 900 segons (15 minuts)
- **El domini està gestionat per Nominalia** (proveïdor d'hosting)

---

## Comanda 4: Consulta de Resolució Inversa

**Comanda executada:**
```bash
dig -x 147.83.2.135
```

![im4](img/im4.png)
*Captura del terminal amb la comanda `dig -x 147.83.2.135`, mostrant la consulta de resolució inversa PTR amb 8 registres de dominis associats a la IP 147.83.2.135 de la UPC (edicioWeb.produccio.upc.edu, gateens.upc.edu, upc.cat, barcelonatech.upc.edu, upc.edu, barcelonatech-upc.eu, www.upc.es, barcelonatech.es.upc.edu) amb TTL de 3641 segons.*

### Anàlisi Comanda 4:

- **IP consultada:** 147.83.2.135
- **Zona inversa:** 135.2.83.147.in-addr.arpa
- **TTL:** 3641 segons (≈ 1 hora)

**Registres PTR obtinguts (noms de domini associats a aquesta IP):**

1. edicioWeb.produccio.upc.edu.
2. gateens.upc.edu.
3. upc.cat.
4. barcelonatech.upc.edu.
5. upc.edu.
6. barcelonatech-upc.eu.
7. www.upc.es.
8. barcelonatech.es.upc.edu.

**Informació obtinguda:**

- Aquesta IP (147.83.2.135) pertany a la **Universitat Politècnica de Catalunya (UPC)**
- Un sol servidor/IP pot tenir **múltiples noms de domini** (alias)
- Tots els dominis apunten al mateix servidor web de la UPC
- La resolució inversa està correctament configurada
- Útil per verificar l'identitat del servidor i validar configuracions de correu

---

## Comanda 1 nslookup: Consulta Bàsica no Autoritativa

**Comandes executades:**
```bash
$ nslookup
> set type=A
> tecnocampus.cat
```

![im5](img/im5.png)
*Captura del terminal amb nslookup en mode interactiu, mostrant la consulta `set type=A` seguida de `tecnocampus.cat`. El servidor 127.0.0.53 respon amb "Non-authoritative answer" i proporciona 4 adreces IP (18.172.213.97, 18.172.213.8, 18.172.213.110, 18.172.213.22).*

### Anàlisi: Per què indica que la resposta és no autoritativa?

La resposta és **"Non-authoritative answer"** perquè:

1. El servidor DNS que respon (127.0.0.53) **NO és el servidor autoritatiu** del domini tecnocampus.cat

2. Aquest servidor actua com a **"resolver recursiu"**: 
   - Consulta els servidors autoritatius (ns-1071.awsdns-05.org, etc.)
   - Guarda la resposta en **CACHE**
   - Retorna la informació des de la seva cache

3. La informació pot estar lleugerament **desactualitzada** (dins del periode TTL)

4. NO és la **"font oficial"** del domini, sinó una còpia temporal

**Resultat obtingut:**

- **Server:** 127.0.0.53
- **Adreces IP:** 18.172.213.97, 18.172.213.8, 18.172.213.110, 18.172.213.22
- **Missatge:** "Non-authoritative answer"

---

## Comanda 2 nslookup: Consulta Autoritativa

**Comandes executades:**
```bash
$ nslookup
> server 205.251.196.47
> set type=A
> tecnocampus.cat
```

![im6](img/im6.png)

*Captura del terminal amb nslookup consultant directament el servidor autoritatiu 205.251.196.47 (ns-1071.awsdns-05.org). Després de configurar `server 205.251.196.47` i `set type=A`, la consulta de `tecnocampus.cat` retorna les mateixes 4 IPs però sense el missatge "Non-authoritative answer", indicant que és una resposta oficial del servidor autoritatiu.*

### Anàlisi: Quines diferències s'observen amb la Comanda 1?

**Diferències principals:**

1. **NO apareix "Non-authoritative answer":**
   - La resposta ve directament del servidor autoritatiu
   - És la font oficial i actualitzada del domini

2. **Servidor diferent:**
   - **Comanda 1:** 127.0.0.53 (resolver local del sistema)
   - **Comanda 2:** 205.251.196.47 (ns-1071.awsdns-05.org - autoritatiu)

3. **Fiabilitat de la informació:**
   - **Comanda 1:** Depèn de cache intermèdies (pot estar desactualitzada)
   - **Comanda 2:** Informació oficial actualitzada en temps real

4. **Les IPs obtingudes són les mateixes:**
   - 18.172.213.110, 18.172.213.97, 18.172.213.8, 18.172.213.22
   - Això confirma que la cache del resolver local estava actualitzada

5. **Ús pràctic:**
   - Les consultes autoritatives són útils per:
     * Verificar canvis recents en DNS
     * Depurar problemes de propagació DNS
     * Obtenir informació oficial sense dependre de caches
     * Confirmar que els canvis s'han aplicat correctament
