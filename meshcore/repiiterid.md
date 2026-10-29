---
title: MeshCore repiiterid
description: 
published: true
date: 2026-10-29T21:00:00.498Z
tags: 
editor: markdown
dateCreated: 2026-10-11T09:38:46.676Z
---

Navigeeri: [MeshCore](/et/meshcore) | [Riistvara](/et/meshcore/riistvara) | [Tarkvara](/et/meshcore/tarkvara) | [Repiiterid](/et/meshcore/repiiterid)

# Seadistamine

Esmane repiiteri seadistus tuleb teha üle USB kasutades ühte järgnevast:
* [config.meshcore.io](https://config.meshcore.io) (vali *Console*)
* [meshcore-cli](https://github.com/meshcore-dev/meshcore-cli)

Repiiterit saab seadistada ka MeshCore rakenduse kaudu. Minimaalselt tuleb selleks repiiteris seadistada administraatori parool või lisada enda võti (*Public Key*) pääsunimekirja (*Access Control*).

Näituseks käsuread mille ükshaaval sisestamisel võiksid saada hästi käituva repiiteri:

```
set name Endla 10A
set lat 59.429584
set lon 24.733158

set radio 869.6179809,62.5,8,5
set tx 22
set dutycycle 10

set path.hash.mode 1
set advert.interval 0
set flood.advert.interval 24
set loop.detect moderate

region default ee
region put harjumaa
region put tallinn
region save

clock sync
```

## Pane tähele

* `radio` parameetri viimane number on *Coding Rate* ehk veaparanduskoodi määr. Hea asukohaga ja hoolega ehitatud repiiterile on `5` õige valik. Kehvemates oludes võib mõelda selle tõstmisele (max `8`). Tõstmine pikendab paketi saatmiseks kuluvat aega kuni 60%.
* `path.hash.mode` on sama mis *companion*il *Default Path Hash Size*. Väärtus `0` ehk `1-byte` on halb, sest võimaldab vaid 254 identifitseeritavat repiiterit ja toob kaasa arusaamatud *trace*id ja valenegatiivid *loop detection*is. Väärtus `1` ehk `2-byte` võimaldab aga juba 65536, mis on mitmetuhande kilomeetri raadiuses piisav maht. Väärtus `2` ehk `3-byte` võimaldaks 16 miljonit identifikaatorit, aga see on meie ja Euroopa oludes juba liiga palju ning paisutab repiiterilt repiiterile leviva paketi mahtu reaalse kasuta.
* Peale igat repiiteri taaskäivitust võiks `clock sync` teha. Vale kellaaeg repiiteri kõhus ei mõjuta põhifunktsionaalsust, kuid võib tekitada segadust kui uurida mida repiiter kuuleb ja kuidas end reklaamib. Loe lähemalt [siit](https://swaits.com/does-repeater-time-matter-in-meshcore/) (inglise keeles).
* Kui repiiteri ümbruses on eeter tihe ja paketid ei liigu hästi, siis katseta *Channel Activity Detection* sisselülitamist (`set cad on`) või saateviite kordaja tõstmist (vaikimisi `set txdelay 0.5`).