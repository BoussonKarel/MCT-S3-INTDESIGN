# 4 - Access
## Beveiligen van toegang
**Drie beveiligingsbasissen (BELANGRIJK)**
- **Weten** *bv Wachtwoord*
- **Hebben** *bv Autosleutel*
- **Zijn** *Wie dat je bent*

### Wachtwoorden
- Meest gebruikte vorm van authenticatie
- Moet voldoende "sterk" zijn
  - Voldoende lang (12 tekens)
  - Verschillende soorten tekens
  - Geen bestaande woorden of logische sequenties

**Sterkte = entropie**
![Entropie en tijd om het te kraken](https://i.imgur.com/wNIY6DH.png)
![Voorbeeldwachtwoorden en hun entropie](https://i.imgur.com/HHyQcne.png)

De beste wachtwoorden zijn **voldoende lang**

- Opletten met
  - Woordenlijsten !!!
  - Vaak gebruikte wachtwoorden !!!
  - Hergebruik: wachtwoordlijsten !!!
 - Zorgen voor succesvolle aanval op "complexe" wachtwoorden.
 
 **Tips**
 - Voldoende sterk is
 - Geen logisch patroon
 - Mijd hergebruik
 - Wijzig regelmatig
 - Leen wachtwoorden nooit uit
- Gebruik 2FA voor authenticatie
- Eventueel gebruik van een wachtwoordkluis (door de organisatie goedgekeurd)
- Noteer wachtwoorden NOOIT waar deze door derden kunnen worden achterhaald

## Beveiligen van toegang
### Wachtwoorden (weten)
- Hoofdletters, kleine letters en cijfers
- Speciale tekens
- Minimale lengte
- Geen betekenisvolle begrippen
- Beperkte geldigheidsduur
- Niet opschrijven

**Waarom zijn wachtwoorden nutteloos?**
Manier van aanvallen verschuift
Ze gaan er niet meer vanuit dat het wachtwoord kraakbaar/vindbaar is.

Vaak gaan ze proberen **spear phishing** te doen: fake login, keylogger...

### Beveiligen op hebben-basis
- Smartcards
- Dongles
- Transponder
- Digipass
- Google Authenticator

Gedeeld geheim, gekend bij zowel server als authenticator.
Op basis van tijd, datum en dat geheim wordt telkens een nieuw wachtwoord gegenereerd.

**Grotere investering**
![Authenticator](https://i.imgur.com/X2N4AnL.png)

### Beveiligen op zijn-basis
- Iris scanner
- Vingerafdruk
- Stem

### Combinatie
De combinatie van meerdere authenticatiemethodes verhoogt de veiligheid

Bij combinatie kiezen we bij voorkeur methodes op verschillende werkingsbasis

## Fysieke toegang
- Onvergrendelde schermen
- Toegangscontrole serverroom
- Hardware aanpassingen of diefstal
  - Asset management softare
- Toegang tot het netwerk
- Introductie van vreemde software
- Opstarten vanaf andere media

## Privilege escalation
- Zichzelf een ander gebruikerniveau
- Horizontale escalation
  - Session hijacking van een andere gebruiker
- Vertical escalation
  - Meer machtigingen verwerven
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIyNTc3NzMwOCwxOTYzMzYwNDMwLDIwNj
AxMjQwODgsLTY5OTk2MjYzMSw4OTA1NzYyODcsMTI5OTQyMTQ4
MiwtMzU1NjYxNDAzLC04NDgxNjg2NjEsLTg4OTEzMjE2NCwxOT
YzOTY3MDY2XX0=
-->