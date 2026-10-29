---
title: MeshCore riistvara
description: 
published: true
date: 2026-10-28T08:26:45.207Z
tags: 
editor: markdown
dateCreated: 2026-10-26T11:12:53.025Z
---

Navigeeri: [MeshCore](/et/meshcore) | [Riistvara](/et/meshcore/riistvara) | [Tarkvara](/et/meshcore/tarkvara) | [Repiiterid](/et/meshcore/repiiterid)

Kõik MeshCore seadmed koosnevad suuresti samadest komponentitest, sõltumata rollist. Samad kiibid leiab nii lõppkasutajale suunatud raadioseadme *aka **companion***i kui ka [repiiteri](/et/meshcore/repiiterid) seest. Seadme roll defineeritakse kasutaja poolt paigaldatava [tarkvara](/et/meshcore/tarkvara) abil. Natukene suunab valiku suunas ka tootja visioon. Kui teoorias saab *companion*ina kasutada kohmakat päikesepaneeliga karpi, siis praktikas pole see mobiilseks kasutamiseks kõige mugavam lahendus.

Tuntumad nimed on [Elecrow](https://www.elecrow.com), [Heltec](http://heltec.org), [LilyGo](https://lilygo.cc), [RAK](https://store.rakwireless.com) ja [Seeed Studio](https://seeedstudio.com). Valikut tegema asudes märkad ruttu kordumakippuvaid täheühendeid ja koode:
* nRF ja ESP on protsessorid. Nende versioone on mitmeid, aga peamine erinevus on energiatarbes. Esimene on viimasest kuni viis korda säästlikum. Kuid viimasega saab ka WiFi, mis võimaldab *companioni*t või repiiterit üle IP-võrgu näppida.
* SX1262, LR1110 jmt on LoRa raadiokivid. Esimene on odav ja populaarne, LRidel on sisseehitatud GPS/GNSS.

# Valmislahendused

Valik on turul kirju. Suurte akudega, väikeste akudega. Ekraaniga ja ekraanita. Tehases kaasa pandud antennid kipuvad aga kõigil enamasti kehvad olema.

## *Companion*id

**Companion** on raadioseade MeshCore võrgu kasutamiseks. Mõni eelistab ühte seadet, mõni mitut - üks kaasaskandmiseks koos nutitelefoniga, teine kodus arvutis kasutamiseks. Mobiilsel kasutusel on oluline kompaktsus ja aku kestvus, mõnel juhul ka vastupidavus. Kodus laua taga istudes tuleb mõelda kuidas seda arvutis kasutada - USB või WiFi. Näiteks kui USB-C port asub seadme põhjal, siis ei saa kaabliühendusega (ka laadimisel) *companion*i püstiselt hoida (lahendus: tee ise alus).

### Elecrow ThinkNode M1

Kompaktne nRF *companion* sinihambaga kasutamiseks. Väga kerge, korpus tundub käes habras. Vastavalt maitsele võib mõelda vutlarile. Aku kestab sõltuvalt kasutusest paarist päevast nädalani. Antenn võib lahjaks jääda. Uue antenni valimisel pane tähele, et ühendus on RP-SMA.

* [Tootja koduleht](https://www.elecrow.com/thinknode-m1-meshtastic-lora-signal-transceiver-powered-by-nrf52840-with-154-screen-support-gps.html)
* [MeshCore Ninja](https://meshcore.ninja/device/thinknode-m1/)
* [Saksamaa Amazon](https://www.amazon.de/-/en/dp/B0FPLWYB8R/)
* [Vutlarikandidaat](https://www.amazon.de/-/en/dp/B092R5ZCPN) (lõika kääridega sobivad augud lisaks ja põleta narmad)

### RAK WisMesh Pocket V2

Tugeva korpusega (aga mitte veekindel) nRF *companion* sinihambaga kasutamiseks. Aku rekordid 3 nädala kanti, kuid pinge langemisel alla 3,6 voldi võib TX nõrgemaks jääda. Antenn on kehva, aga SMA ühendus teeb asendamise lihtsaks.

* [Tootja koduleht](https://store.rakwireless.com/products/wismesh-pocket)
* [MeshCore Ninja](https://meshcore.ninja/device/rak-wismesh-pocket-v2/)
* [Hollandi Hexaspot](https://hexaspot.com/products/wismesh-pocket-v2-ready-to-use-meshtastic-device)

## Repiiterid

Repiiterite valmislahendused ei ole tegelikult päris valmis, vaid vajavad tihti natukene kohendamist. Kuid põhiline keerukus on sinu eest juba ära tehtud - kõik on ilusasti korpusesse laotud!

### Seeed Studio SenseCAP Solar Node P1

Populaarne kompaktne repiiter. Saadaval ka kallim *pro* versioon, mis tuleb akudega ja GPSiga. GPS aga sööb rohkem akut ja väga täpne kellaaeg pole repiiteril oluline. Akud leiab kohalikust kaubandusvõrgust. Kaasa pandud antenn sobib vaid katsetamiseks. N-tüüpi antenni saab paigaldada vaheklambri avadesse. Kui metallmast, millele paigaldatakse, jääb antenni kõrvalt jooksma, siis sellel on negatiivne mõju antennile. Soovitav leida viis antenni mastist eemale viimiseks, näiteks tippu. Sobiv kaabel tuleb ise teha või panna adapter, sest korpusel on RP-SMA ühendus ja neid valmiskaableid on keeruline leida.

* [Tootja koduleht](https://www.seeedstudio.com/SenseCAP-Solar-Node-P1-for-Meshtastic-LoRa-p-6425.html)

### Heltec MeshTower V2

TODO

* [Tootja koduleht](https://heltec.org/project/meshtower/)

### RAK WisMesh Repeater

TODO

* [Tootja koduleht](https://store.rakwireless.com/products/wismesh-meshtastic-solar-repeater)

# Tee ise

Kui valid lõbusa meisterdamise tee, siis ei ole vahet millist rolli sihid, sest mõnusaks nokitsemiseks sobivad kõik plaadid. Küsimus on ainult nendes paljudes pisidetailides mis sul vastu ööd uinuda ei lase.

## Heltec T114

TODO

## Heltec V4

Ülipopulaarne, mitmekülgne ja kurikuulus ESP plaat, mis väärib eraldi [lehte](/et/meshcore/riistvara/heltecv4).

# Antennid

Järgnevad antennid on VNAga kontrollitud ja kvalifitseeruvad headeks:

* [Hexaspot Whip SMA/RP-SMA](https://hexaspot.com/products/flexible-lora-antenna-868mhz)
* [Hexaspot Tactical SMA](https://hexaspot.com/products/hexaspot-tactical-gooseneck-antenna-868mhz)
* [Alfa 868 5 dBi N-tüüp](https://www.getic.ee/product/alfa-lora-halow-antenna-868mhz-5-dbi)
* [Teadmata päritoluga pooleteisemeetrine N-tüüpi jalutuskepp mis kindlasti ei ole 12 dBi](https://www.photopoint.ee/vorguseadmed/2570888-lora-antenna-868mhz-12dbi-150cm) (tuntud kasutaja: ES5TV-R1)

# Kaablid ja ühendused

TODO

# Filtrid

* [sysmocom 863-870 MHz cavity filter](https://shop.sysmocom.de/868-863..870-MHz-cavity-filter-ISM-LoRa-SigFox-Helium/cf866.5-kt30)

# Akud

TODO

# Päikesepaneelid

TODO