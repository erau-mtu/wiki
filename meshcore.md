---
title: MeshCore
description: 
published: true
date: 2026-10-27T21:37:17.204Z
tags: 
editor: markdown
dateCreated: 2026-10-09T08:48:13.457Z
---

Navigeeri: [MeshCore](/et/meshcore) | [Riistvara](/et/meshcore/riistvara) | [Tarkvara](/et/meshcore/tarkvara) | [Repiiterid](/et/meshcore/repiiterid)

[MeshCore](https://meshcore.io) on [LoRa](https://et.wikipedia.org/wiki/LoRa) tehnoloogiale ehitatud litsentsivaba raadiovõrk, mis võimaldab Internetist sõltumatut sõnumisidet. Võrk toetub vabatahtlike paigaldatud autonoomsetele repiiteritele, mis töötavad ka elektri ja internetiühendus puudumisel. MeshCore kasutamiseks on vajalik raadioseade *aka **companion***, mis liidestub nutitelefoniga üle sinihamba. Võrgu arendust ja haldust koordineerib [ERAÜ Raadiosidevõrkude toimkond](/et/erau/rsvt) koostöös [kriisiraadioside töörühmaga](https://www.erau.ee/et/kriisi-raadioside).

# Kohalik vaade

- [MeshMapper levikaart](https://baltic.meshmapper.net/?lat=58.61173&lon=25.70129&zoom=8.00)
- [ES5NHC võrguanalüsaator](https://corescope.es5nhc.ee)
- [ES5KVLT võrguanalüsaator](https://litescope.kvlt.ee) ja [*Tropoparty* agregaator](https://tropoparty.kvlt.ee)

Teiste riikide vaated: [🇱🇻](https://meshlog.anrijs.lv) [🇱🇹](https://meshcore.atvirastinklas.lt) [🇵🇱](https://litescope.riko.dev) [🇫🇮](https://corescope.meshcore.fi) [🇸🇪](https://meshcore.meshat.se) [🇩🇰](http://meshview.dk)

# *Companion*i seadistamine

Eestis kasutame **EU/UK (Narrow)** profiili:
* **Frequency**: 869,618 MHz
* **Bandwidth**: 62,5 kHz
* **Spreading Factor**: 8
* **Coding Rate**: 8

Soovituslikud võrguparameetrid:
* **Default Path Hash Size**: 3-byte (max 21 hops)
* **Default Region Scope**: ee

*Default Region Scope* ehk vaikeskoop ohjeldab pakette millel pole piiri taha asja (kohalik jutt, *advert*id, kontrollsõnumid). Vaikeskoop ei blokeeri skoopimata (**\*** ehk *unscoped*) sõnumite vastuvõttu, vaid juhib sinu sõnumite edasisaatmist. Vaikeskoobi kasutamine ei ole kohustuslik ja sinu sõnumid levivad ka selleta, kuid raadiolained ei tunne riigipiire ja vaikeskoobi kasutamisega säästame naaberriikide eetrit (*dutycycle*).

# Kanalid

| Nimi | Soovituslik skoop | Kasutus |
|-|-|-|
| Public | * | Globaalne kanal, DX ja rahvaste sõprus |
| #estonia | ee | Eestist ja eestlastele |
| #tallinn | tallinn | Pealinna rahvas |
| #tartu | tartu | Head mõtted Emajõe Ateenast |
| #kriis | ee | Kriisiboti teated |
| #bot | ee | Erinevate bottide kräunutamine |
| #test | ee | Levitestid jmt |

# Vaata ka

* [Raadiosidehuvilised Discordis](https://discord.gg/Z9u5QcDTfZ)
* [MeshCore 2026 kokkuvõte](/et/meshcore/2026-kokkuvote)
* [EstMesh MeshCore jutud](https://wiki.estmesh.ee/en/docs/meshcore)
* [K-Space MeshCore jutud](https://wiki.k-space.ee/en/projects/radio/MeshCore)