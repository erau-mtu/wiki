---
title: MeshCore 2026 kokkuvõte
description: 
published: true
date: 2026-10-09T13:01:26.065Z
tags: 
editor: markdown
dateCreated: 2026-09-23T08:50:34.393Z
---

# Senine ajalugu ja üldfilosoofia

> **Algne kirjatsura:** Anto ES8LAU\
> **Alustatud:** 2026-09-22
{.is-info}

> (NB! Kõik ERAÜ liikmed on kutsutud end siia Wikisse sisse logima ning fakte ja nimesid õige(ma)ks keerama!)
{.is-success}

Meshcore teadvustati siinkandis ära 2025-nda aasta teises pooles. Veel juunis 2026 esinesid meil MeshCore peal vaid üksikud omavahel sidumata saarekesed. Näiteks Haapsalus oli Meshcore kenasti saadaval (pauhh?), aga sealt viis tee vaid eikusagile. Enamik rahvast sitsisid Meshtasticu lõksus keskpunktiga Tallinna Polütehnikumis. Pole vast väga suur saladus, et lätlased olid selle va MeshCorele üleminekuga meist aastakese ees. Eraldi teema - et itimeestele on MeshCore oluliselt arusaadavam ja loogilisem. Ei ole mingit läbumaja. On nagu Internetis - ruuterid ja lõppseadmed.

Ja siis saabus suvine Balti mere levi. Salvestasin mõned imelised une-eelsed videod sellest, kuidas Poola ja Taani jaamad meiega otse suhtlevad ning paketid Gdanskist otseteed 600km kaugusele Hiitisesse põrutavad. Tänaseks oleme lätlastele PEAAEGU järele jõudnud.

![screenshot_from_2026-06-29_23-17-05.png](/screenshot_from_2026-06-29_23-17-05.png)

Maagilised Zenteki mehed ehitasid nagu pokkerimängus üles terve mastirea Tallinnast Läti lõunapiirini. Umbes juuli keskel tekitasid nad võrgusõlme Virtsu kõrgeima korstna külge ja sealtmaalt tekkis tohutu mahuga transiitliiklus Soomest Lätti. Läks isegi vaidluseks, et mis keeles peab nüüd Public kanalil rääkima.

Tartu ... kui veel ERAÜ suvise kokkutuleku paiku juulis nokitses Lõuna-Eesti mägedel vaid üksik ES5NHC, siis septembri lõpuks on tagatud side Tartust Tõraverre, üle kõigi nende arvukate Vapramägede ja muude mägede, Laeva Hollywood kaasa arvatud. Septembris ehitasid päkapikud sama märkamatult valmis Kose-Imavere trassi.

Septembris tekkis Jõgevamaale ES5TV lühilainekülla ennenägematu ime - **73m kõrgusel paiknev MeshCore jaam**. See sidus omavahel ära Kose ja Tartu ja võib öelda, et ka enamik Tln-Trt maanteest on nüüd kenasti kaetud.

![screenshot_from_2026-09-22_20-59-17.png](/screenshot_from_2026-09-22_20-59-17.png)

Ent pilt meenutab pisut WiFi algusaegu 2001-2002 kandis. Tallinn, Jura Zaitsev. Võimas antenn, mis asus Olümpia hotelli otsas ning mida oli kuulda Laagrist Rohuneemeni. Ainuke mure, et niipea kui Zaitsevile mõni kesklinna klient taha tuli, siis kaugemad üritajad enam löögile ei pääsenud.

Teine sarnane megaruuter asus Seewaldi haigla katusel, aga selle pani AKI kinni (*Pealtnägija*, 11. detsember 2002), sest naabermaja kaabliks kavandatud raadiolingi kaudu sai ühtlasi ka SQL serveris haiguslugusid lugeda. Ent see selleks. Pärast seda megajaamad kadusid, võimsused keerati väiksemaks ja need paigutati tihedamalt. **Tundub, et oleme MeshCorega täna täpselt samas punktis.**

---

Aeg on suvest kokkuvõtted teha ja järgmisele (eelmisest kvaliteetsemale) ringile liikuda. **Mured on järgmised.**

- **"nähtamatu võrgusõlme" (*hidden node*) probleem.** Aktiivne tegija ehitab endale supermasti, see edastab poolt Eesti liiklust ja siis ise istub selle masti all sideta nagu kingsepp paljajalu, sest eeter on küllastunud ja saatelimiit täis.

- **10% piirang.** Euroreeglite järgi, ükski Meshcore saatja ei tohi kiirata rohkem kui 10% ajast. Siis kõik imestavad, et miks lühike sõnum läheb läbi, aga pikk mitte. Aga seepärast, et ruuter arvutab omale eetriaega ette (*sliding window*) ja teab, et hetkel ei tohi ta üle 17-baidiseid sõnumisi läbi lasta. Vt ka eelmine mure. Kriisisidest rääkides, täna piisab kui suurema sõlmjaama alla nimesid rulliv roppsuu-röökur paigutada, see tagab, et 10% eetriaja limiit ongi kogu aeg täis.

  10% piirang pole tegelikult Eesti suhtes aus. Rahvastikutihedus on meil umbes 10x väiksem kui Lääne-Euroopas, sest sealsete olude järgi need reeglid on tehtud. Kuniks mõni matemaatik mudelit ei koosta, et mis küll oleks meil optimaalne soodevaheline saatetihedus, jääb vaid kaks lahendust -- kas reegleid eirav immits ise kokku kompileerida - sellega päris igaüks hakkama ei saa - või siis küüsi närides CoreScope'i jõllata, et no millal ometi transiitliiklusest Lätti küllastunud Virtsu repiiter mu paketi lõpuks Tallinna suunas läbi laseb.

  **Referents:** <https://www.etsi.org/deliver/etsi_tr/102300_102399/102313/01.01.01_60/tr_102313v010101p.pdf> (eriti peatükid 4.1 ja 4.2)

![etsi.png](/etsi.png)

- **Võimsusest.** *Võim on teatavasti ikka selle käes, kellel on pikem.*\
  Ainult et ETSI standard arvab võimsusest omamoodi. **500mW ja 10%** on tegelikult lubatud vaid alambändis "O" - **869.400-869.650 MHz** ja see on siis ERP - aga viisakusest me siin lõigus +12dB antennidest ei räägi. Mainitud ribast üleval- ja allpool on reeglid palju karmimad (0,1-1% ja 25mW ERP).

  **Referents:** <https://www.etsi.org/deliver/etsi_en/300200_300299/30022002/03.03.01_60/en_30022002v030301p.pdf>

- **Eetri paskamisest.** Heltec v4 vigane kood tehti versioonis 1.17 korda, nii et 27dBm väljasaatmiseks pole nüüd enam vaja `set tx 27` kirjutada, vaid piisab `set tx 17`. Sest kui üle pingutada, siis läheb GC1109 lõpukivi küllastusse ja hakkab eetrit essuma - kas teadsid? Muide, Heltec v4 plaatidest on põhjalikult kirjutatud [karu sisemuses](https://karusisemus.wordpress.com/2026/04/05/antennas-sold-with-heltec-v4-boards-can-destroy-your-board/).

- **Puukujuline võrgustruktuur.** Sest "mesh" tähendas ju algselt hoopis midagi muud - kärgvõrku.\
  Et igast võrgusõlmest iga järgmiseni oleks seitse võimalikku teekonda ja küll masinad ise dünaamiliselt valivad sobivaima. Kriisisidet puukujulise struktuuriga teha ei saa, pole üldse keeruline loetleda need paar taburetti Tallinnas, millel jalad alt saagida, et kogu Eesti ühekorraga vait jääks.

- Kõige suuremate lolluste piiramiseks hakkasid mõned adminnid oma ruuterites kasutama **regioonisilte (scope)**. Konkreetselt siis `ee`. Paraku tehti seda ERAKORDSELT valel hetkel, nimelt Meshcore v 1.17 väljatulek [oota pisut, selle kohta tuleb kohe teine artikkel] rikkus oodatava tulemuse täielikult. Aktiivsed lätlased ja soomlased, kes ei taht tropo-tunneli mõnudest ilma jääda, keerasid omalgi sildiks `ee`. Aga oli see siis nii mõeldud?

- **Enamikes seadmetes annab konffida vaid 8 jutukanalit.** `Public`, `#test`, `#kriis` ja `#bot` ning ongi pooled slotid täis. Siit kaks järeldust: absoluutne enamik kanaleid ei saa olla üle-Eestilised ning kanalite nimed on ka vaja omavahel ära koordineerida, et ei juhtuks nii, et alul on `#test` ja siis on selle kõrval veel ka `#testing`.

- **Mitme baidiseks on konfitud jaama räsi (lühend avalikust võtmest)?** Enamik võrgusõlmi Eestis istuvad 2 baidi peal, ent ka 1 ja 3 on tihedalt esindatud. 3 on liiga vähe - meil esineb juba pikemaid ahelaid kui 16 jänkuhüpet. 1 on eksitav, rakendused ei suuda Eesti jaamu Poola omadest eristada. Karjub, et ma pingiks küll, aga keda neist kolmest?

  Ja üldse, kui juba seisusekohane aparaat püsti panna, siis oleks viisakas sellele ka [seisusekohased võtmed genereerida](https://agessaman.github.io/meshcore-web-keygen/?prefix=00000000) ja parem sellised, et [kollisioone ei tekiks](https://corescope.es5nhc.ee/#/analytics?tab=collisions&bytes=1). Harjutage krüptograafiat, keerulises geopoliitilises olukorras läheb seda kindlasti vaja. Kui mitte ajateenistuses, siis metsaonnis juba kindlasti.

- **Kas Sinu aparaat võimaldab meeles pidada 160 korrespondenti või tervelt 350?** Tegelikult vahet pole, sest suvise levi ajal saab see nimekiri niikunii täis. Ja siis algavad mured. Lähim ruuter ei ilmu kuidagi korrespondentide nimekirja. Debug ütleb, et "pole slotti". Kokkuvõttes - pead endale mingi süsteemi leiutama, keda võtta ja keda jätta. Ning piisab ühest läbi-Läti sõidust kui su nimekirjad on taas täis. Ühesõnaga, õpi nimekirju manageerima!

- Koleda jõledusena on avastatud, et **Tele2 moblamastide** üks saatekanalitest ulatub servapidi PEAAEGU meie valitud sageduseni - **869.618 MHz**. Ja siis on veel need hiina raadiomikrofonid sagedusel 863–865 MHz, mis võivad Lora plaadil kõrvad kinni karjuda. See aga tähendab, et võrgusõlme ja antenni vahele tuleb paigutada filter. Kas odav pinnalaine (SAW) hiinakas, mis talub vaid 20dBm võis siis korralik [mahtresonaator](https://shop.sysmocom.de/868-863..870-MHz-cavity-filter-ISM-LoRa-SigFox-Helium/cf866.5-kt30), mis talub mitukümmend vatti, aga maksab 60-70€ tuuris.

  Filtreid on täna vaid vähestel ja sellega seotud kogemusi pole siinkandis laiemalt kirjeldatud, nii et see teema oleks väärt eraldi artiklit [keegi kirjutab filtritest]. Spetsid on avastanud, et Sysmocomi filter tuleb pisut ülespoole ümber häälestada, nii et ta Tele2 signaali maha lõikaks (LTE Band 20 FDD Uplink - 852–862 MHz on kõigest 7.6 MHz kaugusel). Sul ikka on kodus generaatoriga spektrianalüsaator selleks häälestustööks? ;)

---

> Kokkuvõttes - on vaevalt võimalik, et me praeguseks väljakujunenud mõnusa anarhiaga ka järgmise suve samal moel üle elaksime. Et iga maakonna Kulibinid valivad pikima männi, tellivad Aliexpressist pikima antenni ja siis keeravad seadme +27dBm ERP-le antenniga veel +12dB otsa, nii et kokku tuleb kiiratavat võimsust 8W kandis.
{.is-warning}

Ja siitmaalt läheb meie jutt pisut tõsisemaks. **Teha on vaja järgmist.**

1. **Huvilistel, aktivistidel ja katsetajatel omavahel tuttavaks saada.** Kui oled inimest näinud, oskad ta huvidest ja püüdlustest paremini aru saada. Kõige parem on ikka füüsiliselt kätt suruda ja näod-nimed kokku viia. Mõned tegijaist on raadioamatöörid, nendega on lihtsam, kuid on veel palju teisi, kel kõigil on omad huvid - kes tahab kohaliku põllumajandusettevõtte traktorid või lehmad ära radiofitseerida, kes sohust marjuleläinud vanaemasid otsida. Raadioeeter on aga kõigil üks. Seega tuleb koordineerida.

2. **Leppida kokku piirkondlikes märgendites.** Korraga ja kogu tabel, mitte nii, et iga Kulibin omas talus leiutab. Kas `joegeva` või `ee-joegeva`? On teada, et MeshCore tarkvara suudab saksa täpitähed ise ära transkribeerida (`München` -> `muenchen`). Õ-tähte teadaolevalt siiski mitte.

3. **Leppida kokku nimeruumi ja ruuteripidaja atribueerimise heas tavas.** Et kas raadioamatöör paneb oma loomingule kutsungi ka külge või siis vähemasti jaamaomanikuna märgib end vastavas lahtris ära? Sest muidu on varsti terve Eesti Ratsa-Roosisid ja Kollaseid Kanu täis. Iseasi, et mitte-amatööre saab sel teemal üksnes paluda ja veenda, ei enamat. Ja siis veel GDPR oh õudne bulla...

4. **Koos kavandada järgmise soojaperioodi vältel ehitatav taristu.** Selge see, et kõik kavad ei õnnestu ja lambist eksperimenteerida tahaks samuti, aga vähemasti põhisuunad peaksid olema selged ja kusagil avalikult kirjas. Kas just otsusena, aga kogukonnas läbiarutatud teemadena küll. See aga eeldab, et eelnevalt kogutakse ja vahetatakse liikluse statistikat. Kes kellega käib, millist botti enim tülitatakse. Millised regioonid ajavad krüpteeritud era-asja ja millised pigem sõtkuvad avaliku kanali pääl.

   Küsimusi, mida selles punktis arutada, on enam kui küllaga. Kas kasutada suundantenne? Täna meil neid praktiliselt käigus pole, kõik reostavad oma Hiina keradiagrammidega otse kosmost. Milline suund on enamikele osalejatele tähtsam - kas Nuustakult Kapa Kohilasse või Tallinna teletornist otse Riia omasse? Lisaks tuleb asju arutada ja kompromisse leida nii, et keegi südamepõhjani ära ei solvuks, et just tema soovi eirati. Eestlasel on kange iseloom, 10 aastat oma jonni ajavaid vastalisi pole meile praeguses geopoliitilises olukorras üldse vaja. Väga inetu küsimus, aga ka see tuleb paika rääkida - et mil määral me avalikus toas kirillitsat talume?!

5. **Seirejaamad.** Iseenesest on ju tore, kui igamehe bott õhtu jooksul terve Eesti läbi tülitab, ainult et seire osakaal liiklusest ei tohiks üheski võrgus eales ulatuda üle mingi teatud taseme.

6. **Vana, juba 90-ndatest ja CB pealt tuntud probleem**, et kui pidulisi on kümneid ja sadu, siis raudpoltkindel, et keegi ikka hakkab ülbitsema ja kogukonna reegleid rikkuma. Peab tekkima teatav tahe röövkalad välja püüda ja eksinud lambukesed viisakalt ära distsiplineerida... rüütliks pole vaja lüüa, aga raadioamatööri eksamini võiks nad küll nügida.

7. **Välk.** Häälerepiiteritesse lööb välk päris sageli sisse, no miks ei peaks digirepiiteritesse lööma? Otse öeldes, igaüks, kes paneb jaama üles, sel võiks suvel sahvris veel kaks samasugust seadmekomplekti ootel olla. Uskuge, läheb vaja!

8. **Seadmete märgistamisest.** Mõned üksikud ruuterid on puu otsast juba ka ära varastatud. Kuidas me seadmetele omanikumärgi sisse kõrvetame?

9. **Tehnilised KKK'd igasugustel seotud teemadel.** Keegi peab need valmis kirjutama.
   - **a)** seadme valik - [K-space Wiki viited](https://wiki.k-space.ee/projects/radio/MeshCore) (Thnx, Arti!) on asjalikud
   - **b)** installimine - ES1TEM ja K-Space täna küll pakuvad mingit teavet, aga otse öeldes, nende "best before" jääb aasta algusse. Asi areneb edasi meeletult kiiresti...
   - **c)** kogemus antennidega ja filtritega (raadioamatöörid natuke jagavad matsu, aga teised?)
   - **d)** kogemus [Li-Ion akudega (talvel, meie kliimas)](https://yycmesh.com/blog/cold-weather-charging)
   - **e)** kogu see krüptograafia, mis MeshCorega kaasneb. Sest nooremaid adepte võlub eelkõige võimalus riigist ja röövkapitalismist "mööda" suhelda.
   - **f)** igasugused seirelahendused, vt <https://es1tem.uk/> ja <https://corescope.es5nhc.ee/>, aga ka <https://meshcore-analyzer.eu/>