# 4 - Access
## Beveiligen van toegang
**Drie beveiligingsbasissen (BELANGRIJK)**
- **Weten**
*bv Wachtwoord*
- **Hebben**
*bv Autosleutel*
- **Zijn**
*Wie dat je bent*

### Wachtwoorden
- Meest gebruikte vorm van authenticatie
- Moet voldoende "sterk" zijn
  - Voldoende lang (12 tekens)
  - Verschillende soorten tekens
  - Geen bestaande woorden of logische sequenties

**Sterkte = entropie**
![Entropie en tijd om het te kraken](https://i.imgur.com/wNIY6DH.png)
![Voorbeeldwachtwoorden en hun entropia](https://i.imgur.com/HHyQcne.png)

De beste wachtwoorden zijn **voldoende lang**

 - Opgelet voor wachtwoorden in woordenlijsten
 - Vaak gebruikte wachtwoorden zijn gekend
 - Enorme lijsten met wachtwoorden zijn beschikbaar
 - Vak succesvolle aanval op anders toch complexe wachtwoorden
 
 **Tips**
 - Let erop dat het wachtwoord voldoende sterk is
 - Gebruik geen logisch patroon
 - Mijd hergebruik
 - Wijzig je wachtwoorden regelmatig
 - Leen nooit een wachtwoord uit
- Gebruik 2FA voor authenticatie
- Mijd eventueel gebruik van een wachtwoordkluis (gebruik door de organisatie goedgekeurde software)
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
  - d
- Verticale escalation
  - d
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA2MDEyNDA4OCwtNjk5OTYyNjMxLDg5MD
U3NjI4NywxMjk5NDIxNDgyLC0zNTU2NjE0MDMsLTg0ODE2ODY2
MSwtODg5MTMyMTY0LDE5NjM5NjcwNjZdfQ==
-->