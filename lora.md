---
title: LoRa üldinfo
description: 
published: true
date: 2026-10-09T12:55:13.719Z
tags: 
editor: markdown
dateCreated: 2026-09-19T21:53:40.901Z
---

# LoRa mesh-seadmete majutamine ERAÜ asukohtades

> See leht on soovituslik juhend, mitte õigusnõuanne. Seadme nõuetekohase kasutamise eest vastutab seadme omanik. ERAÜ majutab ainult seadmeid, mis vastavad allpool toodud tingimustele.
{.is-info}

## Millest jutt

ERAÜ võib võimaluse korral pakkuda asukohta (mast, katus, ruum, toide) Meshtastic-, MeshCore- , Reticulum/RNode ja teistele sarnastele seadmetele. Need seadmed töötavad **sagedusloast vabastatud lähitoimeseadmetena** (ingl *short range device*, SRD). Nende kasutamiseks ei ole vaja sagedusluba ega raadioamatööri luba, **kuid ainult siis, kui seade peab kinni kõigist sagedusloata kasutamise tingimustest**: sagedusala, kiirgusvõimsus ja töötsükkel.

Tegemist ei ole raadioamatöörjaamadega.

## Õiguslik alus

- **Elektroonilise side seadus** – raadiosageduste kasutamise üldpõhimõtted ja järelevalve.
- **Määrus nr 96** (07.10.2011) „Raadiosageduste kasutamise tingimused ja tehnilised nõuded sagedusloast vabastatud raadioseadmetele“ – konkreetsed sagedusalad, võimsused ja töötsüklid. Määrust muudetakse aeg-ajalt, kontrolli alati kehtivat redaktsiooni Riigi Teatajas.
- **Eesti raadiosagedusplaan** (määrus nr 54, 26.10.2017).
- **Toote nõuetele vastavuse seadus** ja **määrus nr 46** „Nõuded raadioseadmele ja nõuetele vastavuse tõendamise kord“ – raadioseadmete direktiivi 2014/53/EL (RED) rakendamine: CE-märgis ja vastavusdeklaratsioon.
- **Komisjoni otsus 2006/771/EÜ** (muudetud otsustega 2019/1345 ja 2022/180) – EL-is ühtlustatud lähitoimeseadmete sagedusalad.
- Järelevalvet teeb **Tarbijakaitse ja Tehnilise Järelevalve Amet (TTJA)**.

## Lubatud sagedusalad

| Sagedusala | Suurim kiirgusvõimsus | Töötsükkel | Märkus |
|---|---|---|---|
| 869,40–869,65 MHz | 500 mW e.r.p. (27 dBm) | ≤ 10 % | Meshtastic EU_868, MeshCore EU. **Soovitatav.** |
| 868,0–868,6 MHz | 25 mW e.r.p. (14 dBm) | ≤ 1 % | |
| 433,05–434,79 MHz | 10 mW e.r.p. (10 dBm) | ≤ 10 % | Meshtastic EU_433 |
| 2400–2483,5 MHz | 10 mW e.i.r.p. (10 dBm) | vt määrust | 2,4 GHz LoRa |

Muud 863–870 MHz alamribad lubavad ainult 25 mW ja 0,1–1 % töötsüklit ning sobivad mesh-võrgu jaoks halvasti. ERAÜ majutatav 868 MHz sõlm peaks töötama alamribas **869,40–869,65 MHz**.

Määrus lubab mõnel juhul töötsükli asemel kasutada „kuula enne saatmist“ meetodeid (LBT+AFA). ERAÜ eeldab lihtsuse huvides töötsükli piirangu kasutamist.

## Kolm kõige sagedasemat viga

### 1. Võimsuse piir kehtib kiirgusvõimsusele, mitte saatja väljundile

Piir on **e.r.p.** (efektiivne kiirgusvõimsus), mis sisaldab ka antenni võimendust. Mida suurema võimendusega antenn, seda väiksem peab olema saatja võimsus.

```
e.r.p. (dBm) = saatja võimsus (dBm) − kaabli ja pistikute kadu (dB) + antenni võimendus (dBi) − 2,15
```

Näited alamriba 869,40–869,65 MHz jaoks (piir 27 dBm e.r.p.):

| Antenn | Kaabli kadu | Suurim saatja võimsus |
|---|---|---|
| 3 dBi | 1 dB | 27 dBm |
| 6 dBi | 1 dB | 24 dBm |
| 9 dBi | 2 dB | 22 dBm |

Kui kaabli kadu ei ole teada, arvesta see nulliks – nii jääd kindlasti piiridesse.

### 2. Tarkvara võimsusseade ei ole alati tegelik väljundvõimsus

Paljudel plaatidel (nt 1 W moodulid) on LoRa kiibi järel lisavõimendi. Tarkvaras seatud väärtus kehtib kiibile, tegelik väljund võib olla mitu dB suurem. Omanik peab teadma oma seadme **tegelikku** väljundvõimsust (tootja andmed või mõõtmine).

### 3. Töötsükli piirang on välja lülitatud

10 % tähendab kuni 6 minutit saateaega tunnis. Repiiter saadab edasi ka teiste pakette, seega just majutatavas sõlmes on see piirang eriti oluline.

## Kohustuslikud tingimused majutatavale seadmele

1. Seade töötab ainult ülaltoodud sagedusaladel ja **kogu signaali ribalaius** jääb alamriba sisse (nt 869,525 MHz ± 125 kHz = täpselt 869,400–869,650 MHz).
2. Kiirgusvõimsus (e.r.p.) koos antenni ja võimalike võimenditega ei ületa lubatud piiri. Omanik esitab arvutuse.
3. Töötsükli piirang on seadme tarkvaras sisse lülitatud ja vastab sagedusalale.
4. Väliseid lisavõimendeid ei kasutata.
5. Seade ei häiri ERAÜ ega teiste asukohas olevate seadmete tööd (sh ERAÜ repiitrid).
6. Seadmel on silt omaniku nime, kontakti ja seadme andmetega.
7. Omanik on kättesaadav ja reageerib mõistliku aja jooksul.
8. ERAÜ-l on õigus seade igal ajal ette teatamata välja lülitada või eemaldada, kui see rikub neid tingimusi, tekitab häireid või seda nõuab asukoha omanik või TTJA.
9. Toide ja paigaldus on ohutud: CE-märgisega toiteplokk, ilmastikukindel paigaldus, antenni maandus ja piksekaitse vastavalt asukoha reeglitele.
10. Seadistuse muutmisest (sagedus, võimsus, antenn, püsivara) teavitatakse ERAÜ-d.

**Soovitused:**

- Eelistatud on CE-märgise ja EL vastavusdeklaratsiooniga seadmed. Isetehtud või komplektist kokku pandud seadme puhul vastutab omanik ise, et seade vastaks sagedusloata kasutamise tingimustele.
- Seadet peaks saama kaugelt välja lülitada või peaks ERAÜ kontaktisikul olema kaughalduse ligipääs.

## Seadistus tarkvarade kaupa

### Meshtastic

- `Region`: `EU_868` (või `EU_433`). Määramata regiooniga seade ei saada üldse.
- `Override Duty Cycle Limit`: **välja lülitatud**.
- `TX Power`: arvuta antenni järgi. Meshtasticu EU_868 piir 27 dBm ei arvesta sinu välise antenni võimendust ega pruugi arvestada plaadi lisavõimendit.
- Ham-režiim (*licensed mode*): ei kasutata (vt „Mis selle juhendi alla ei kuulu“).
- MQTT-ülesaatmine: vaikimisi välja lülitatud, lubatud ainult kokkuleppel ERAÜ-ga.

### MeshCore

- Sagedus ja ribalaius peavad jääma alamribasse 869,40–869,65 MHz.
- Töötsükkel: `set dutycycle 10` (püsivara v1.15 ja uuem), vanemas püsivaras `set af 9`. **Vaikimisi on piirang 50 %, mis ei vasta EL-i nõuetele.**
- Võimsus: `set tx <dBm>` arvutatud väärtusega. See seade kehtib ainult LoRa kiibile, mitte lisavõimendile.
- Kontrolli: `get radio`, `get tx`, `get dutycycle`.

### Reticulum / RNode

Reticulum ei piira ise sagedust ega võimsust – kõik parameetrid määrab kasutaja ja vastutus on täielikult seadistajal. Näide:

```
[[RNode LoRa]]
  type = RNodeInterface
  interface_enabled = True
  port = /dev/ttyUSB0
  frequency = 869525000
  bandwidth = 125000
  txpower = 14
  spreadingfactor = 8
  codingrate = 5
  airtime_limit_long = 10
```

- `airtime_limit_long` piirab saateaega libiseva 60-minutilise akna jooksul (protsentides). Vaikimisi piirangut ei ole.
- `txpower` arvuta antenni järgi.

## Mis selle juhendi alla ei kuulu

- **Raadioamatöörsagedustel töötav LoRa** (nt Meshtasticu ham-režiim või RNode amatööriribas). See on amatöörraadioside: vaja on raadioamatööri luba ja kutsungit ning sõnumite sisu varjamiseks krüpteerimine ei ole lubatud. Sellisele kasutusele kehtivad raadioamatööride reeglid, mitte see leht.
- Seadmed, mille kasutamiseks on vaja sagedusluba.
- Seadmed, mille parameetreid ei ole võimalik kontrollida.

## Isikuandmed

Mesh-võrgus liiguvad kasutajate sõnumid, seadmete nimed ja sageli ka asukohad. Kui majutatud sõlm saadab andmeid internetti (nt Meshtasticu MQTT), võivad need muutuda avalikult nähtavaks. Soovitame:

- hoida majutatud sõlmes MQTT-ülesaatmine vaikimisi välja lülitatud;
- mitte logida ega salvestada teiste kasutajate sõnumite sisu;
- näidata sõlme asukohta üldistatult, kui asukoha omanik seda soovib.

## Majutuse taotlemine

Omanik esitab ERAÜ-le:

- nimi, telefon, e-post (ja kutsung, kui on);
- seadme mudel, tarkvara ja püsivara versioon;
- sagedus, ribalaius, *spreading factor*;
- saatja võimsuse seadistus ja tegelik väljundvõimsus;
- antenni tüüp ja võimendus (dBi), kaabli tüüp ja pikkus;
- arvutatud e.r.p.;
- töötsükli seadistus;
- toide (pinge, voolutarve);
- kinnitus, et on selle lehega tutvunud ja vastutab seadme nõuetekohase kasutamise eest.

## Häire korral

- Kui majutatud seade tekitab häireid, lülitab ERAÜ selle välja ja teavitab omanikku.
- Muudest raadiohäiretest saab teatada TTJA-le: https://ttja.ee/teade

## Viited

- Määrus nr 96 (kehtiv redaktsioon): https://www.riigiteataja.ee/akt/117052024018?leiaKehtiv
- TTJA, raadioseadmed: https://ttja.ee/ariklient/ohutus/tooted-teenused/raadioseadmed
- EL otsus 2019/1345 (lähitoimeseadmed): https://eur-lex.europa.eu/legal-content/ET/TXT/?uri=CELEX:32019D1345
- Meshtastic LoRa seadistus: https://meshtastic.org/docs/configuration/radio/lora/
- MeshCore CLI: https://docs.meshcore.io/cli_commands/
- Reticulum liidesed: https://reticulum.network/manual/interfaces.html