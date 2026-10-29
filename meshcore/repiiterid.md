---
title: MeshCore repiiterid
description: 
published: true
date: 2026-10-27T21:36:51.460Z
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

* Peale igat repiiteri taaskäivitust võiks `clock sync` teha. Vale kellaaeg repiiteri kõhus ei mõjuta põhifunktsionaalsust, kuid võib tekitada segadust kui uurida mida repiiter kuuleb ja kuidas end reklaamib. Loe lähemalt [siit](https://swaits.com/does-repeater-time-matter-in-meshcore/) (inglise keeles).
* `radio` parameetri viimane number on *Coding Rate* ehk veaparanduskoodi määr. Hea asukohaga ja hoolega ehitatud repiiterile on `5` õige valik. Kehvemates oludes võib mõelda selle tõstmisele (max `8`). Tõstmine pikendab paketi saatmiseks kuluvat aega kuni 60%.
* Kui repiiteri ümbruses on eeter tihe ja paketid ei liigu hästi, siis katseta *Channel Activity Detection* sisselülitamist (`set cad on`) või saateviite kordaja tõstmist (vaikimisi `set txdelay 0.5`).