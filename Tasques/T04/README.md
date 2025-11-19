# T04: Serveis de Directori – LDAP

## Breu Descripció

Innovatech, una start-up tecnològica emergent, està experimentant un ràpid creixement i pateix un caos en la gestió dels seus usuaris i accessos.  
Actualment, cada servei intern (servidor de fitxers, wiki de documentació, etc.) utilitza la seva pròpia base de dades d’usuaris i contrasenyes, i als ordinadors clients s’utilitza autentificació local. Això genera diversos problemes crítics:  

- **Ineficiència Operativa:** Cada cop que un empleat s’incorpora o marxa, l’equip tècnic ha de crear o eliminar el compte en múltiples sistemes.  
- **Risc de Seguretat:** Els usuaris sovint reutilitzen contrasenyes entre serveis per evitar l’oblit.  
- **Manca d’Escalabilitat:** Amb l’addició de nous serveis, la gestió d’usuaris es torna insostenible.  

El CEO d’Innovatech ha contactat amb EverPia per implementar una **solució d’autenticació centralitzada**. La proposta és utilitzar **OpenLDAP (Lightweight Directory Access Protocol)** per ser una solució robusta, de codi obert i compatible amb GNU/Linux, sistema operatiu principal de l’empresa.  

## Objectius de la Tasca

L’objectiu principal és implementar un servei **OpenLDAP** en un servidor Linux i integrar un client per autenticar usuaris des del directori. Les tasques concretes inclouen:

1. **Instal·lació del servei OpenLDAP** en un servidor Linux.  
2. **Configuració del domini base** i la jerarquia d’unitats organitzatives (OU).  
3. **Creació d’usuaris i grups** que es podran utilitzar per donar accés a altres serveis de xarxa.  
4. **Configuració d’un equip client** per autenticar usuaris contra el directori centralitzat.  

## Materials de Classe

Els materials i guies utilitzats per completar la tasca es poden trobar al Moodle de l’assignatura:  

- **UD04.AA1:** Serveis de Directori  
- **UD04.AA2:** Instal·lació OpenLDAP  
- **UD04.AA3:** Configuració del Directori  
- **UD04.AA5:** Afegir Client al Directori  

## Requisits

- Sistema operatiu Linux (servidor i client).  
- Accés d’administrador per instal·lar i configurar OpenLDAP.  
- Coneixements bàsics de línia de comandes i administració de Linux.  

## Resultat Esperat

- Servidor OpenLDAP funcional amb domini base i jerarquia OU.  
- Usuaris i grups creats i disponibles per autenticar serveis de xarxa.  
- Client Linux autenticant-se correctament amb el directori centralitzat.  

## Notes Addicionals

- Seguiu el **plec de condicions tècniques** proporcionat a Moodle per a les instruccions detallades.  
- La tasca té com a objectiu la consolidació de coneixements pràctics en serveis de directori i gestió centralitzada d’usuaris en entorns Linux.

