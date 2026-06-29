# FOTOKOPIA

**Fotokopia, xerox, riso eta CMYK inprimaketa-efektuen sortzailea.** Fitxategi bakarreko HTML/JS tresna, edozein irudiri tinta-isuri organikoa, erditonu-trama, erregistro-akatsa duen CMYK bereizketa eta paper-testurak aplikatzen dizkiona. Prozesu osoa zure nabigatzailean gertatzen da: ezein irudik ez du zure ekipoa uzten.

**B_RR_K_** tresna-ekosistemaren parte (estetika industrial iluna, Bebas Neue + JetBrains Mono, bermiloi/urre).

---

## Zer egiten du

Irudi bat inprimaketa inperfektu eta organiko bihurtzen du: isurtzen den tonerra, lerrokatu gabeko plakak, puntu-tramak, orbanak, paper-zuntza eta bineta. Azalentzat, fanzineentzat, riso kartelentzat, testurentzat eta collagerako pentsatua.

## Ezaugarriak

### Inprimaketaren errealismoa
- **Erditonu erreala plakaz plaka** — AM trama-puntuak angelu klasikoekin (C 15°, M 75°, Y 0°, K 45°), arroseta sortzen dutenak; maiztasun doigarria.
- **Puntu-irabazia** — erdiko tonuak loditzen ditu, paperak xurgatutako tinta bezala.
- **Ertza lau kontrol independenteetan** — *Isuria* (tinta-zabaltzea), *Uhindura* (ertzaren forma organikoa), *Hozkada* (kraskadura fina) eta *Ertz-biguntasuna* (kraskaritik lausora/haloraino).
- **Norabide-isuria** — angelua + kopurua, tinta alde batera korritzeko (grabitatea, metxa).
- **Erregistro-akatsa (misregistration) plakaz plaka** — desplazamendu eta biraketa independenteak, plaka bakoitza aktibatzeko edo desaktibatzeko aukerekin.

### Kolorea eta tintak
- **Mono modua** — tinta eta papera kolore librearekin, riso paleta azkarrarekin.
- **CMYK modua** — benetako RGB→CMYK bereizketa, *CMY aberastasunarekin* (rich black) beltzaren azpian kolorezko ertzak lortzeko.
- **Tinta spot / duotonoa** — plaka bakoitzak kolore editagarria du; itzali plakak duotonoak egiteko (adib. Fluo Pink + beltza). Eredu kenkari berak balio du CMYKrako eta tinta lauetarako.

### Testura
- Bi paper-testura eskaneatu **txertatuta** + zurea igotzeko aukera.
- *multiply / screen / overlay / soft light* nahasketa, opakutasuna eta eskala.
- **Estaldura bidezko maskara**: testura denari, tintari soilik edo paperari soilik aplikatu.

### Pikorra eta papera
- Toner-orbanak eta soilguneak (dropout) mono moduan.
- Maiztasun baxuko zuntz-testura eta bineta.

### Lan-fluxua
- **Bereizmen baxuko aurrebista** doitzen ari zaren bitartean eta **bereizmen osoa askatzean** (renderizazioa Web Worker batean, tirakadarik gabe).
- **Aurretik / ondoren** (eutsi sakatuta **KONPARATU**) eta **zoom / mugitu** (gurpila, arrastatu, klik bikoitza berrabiarazteko).
- **Hazia + dadoa** zarata organikoaren aldaera erreproduzigarrietarako.
- **Norberaren aurrezarpenak** nabigatzailean gordeak.

### Esportazioa
- **PNG** prozesu-bereizmenean (1500 px).
- **PNG 2×** (supersampling, 3000 px-raino).
- **Tinta-soileko PNG** atzealde gardenarekin (overlay gisa erabiltzeko).
- **C / M / Y / K bereizketak** fitxategi banatan.

### Hizkuntzak
- Interfaze eleanitza **Euskara / Gaztelania / Ingelesa** aldatzailearekin.

---

## Nola erabili

1. Ireki `fotokopia.html` nabigatzaile moderno batean (Chrome, Firefox, Edge, Safari).
2. Arrastatu irudi bat oihalaren gainera edo egin klik fitxategi bat aukeratzeko.
3. Aukeratu aurrezarpen bat abiapuntu gisa eta doitu kontrolak.
4. Esportatu emaitza.

> **Aurrezarpenak gordetzeak** funtziona dezan, ireki fitxategia tokian (ez biltegiratzerik gabeko lineako aurrebista batean). Aurrezarpenak nabigatzailearen `localStorage`-n gordetzen dira.

---

## Kontrolen erreferentzia

| Taldea | Kontrola | Tartea | Lehenetsia |
|---|---|---|---|
| **Tonua** | Kontrastea | 0.5 – 3 | 1.40 |
| | Atalasea | 20 – 235 | 128 |
| **Ertza / Isuria** | Isuria | 0 – 8 | 2 |
| | Uhindura | 0 – 120 | 45 |
| | Hozkada | 0 – 120 | 45 |
| | Ertz-biguntasuna | 2 – 60 | 13 |
| | Isuri-norabidea | 0 – 360° | 90° |
| | Norabide-kopurua | 0 – 14 | 0 |
| **Erditonua** | Trama aktibatu | bai/ez | ez |
| | Maiztasuna (px) | 3 – 20 | 6 |
| | Puntu-irabazia | 0 – 1.2 | 0.20 |
| **Pikorra (Mono)** | Toner-orbanak | 0 – 120 | 10 |
| | Soilguneak (dropout) | 0 – 120 | 6 |
| **Papera** | Zuntz-testura | 0 – 60 | 12 |
| | Bineta | 0 – 80 | 22 |
| **Kolorea** | Modua | Mono / CMYK | Mono |
| | Erregistro-akatsa | 0 – 24 | 5 |
| | Plaka-biraketa | 0 – 3° | 0 |
| | CMY aberastasuna | 0 – 1 | 0.55 |
| **Testura** | Opakutasuna | 0 – 100 | 0 |
| | Eskala | 0.4 – 3 | 1.00 |
| **Hazia** | Seed | osokoa | 1234 |

## Aurrezarpenak

- **Xerox Z/B** — kontraste handiko fotokopia, orbanekin eta isuriarekin.
- **Riso** — duotonoa (Fluo Pink + beltza) erregistro desplazatuarekin.
- **Offset CMYK** — kuatrikromia, erditonuarekin eta puntu-irabaziarekin.
- **Prentsa** — egunkaria, erditonu lodia eta hozkada handia.

---

## Arkitektura teknikoa

- **Fitxategi bakarra**, mendekotasunik edo build-ik gabe. Tipografiak Google Fonts bidez (sistemaren letra-tipoarekin offline ere badabil).
- **Pipeline-a Web Worker txertatuan**: motorraren kodea `<script type="text/js-worker">` batean dago, Blob worker gisa exekutatzen da eta interfazea arin mantentzen du. Workerra erabilgarri ez badago, motor bera hari nagusian exekutatzen da *fallback* gisa.
- **`renderCore(params, raw, W, H, tex)`** pipeline-aren funtzio purua da: haziatik fBm zarata-eremuak eraikitzen ditu (`mulberry32` PRNG deterministaz), tonua edo CMYK plakak bereizten ditu, gutxieneko iragazkia (tinta-zabaltzea), lausotzea, norabide-isuria, *domain warp* + hozkada fraktala + atalase biguna edo erditonua aplikatzen ditu, eta paperaren gainean modu kenkarian konposatzen du.
- **Bi bereizmen**: aurrebista (720 px) interakzioan, osoa (1500 px) askatzean; esportazioa 3000 px-raino.
- Prozesu osoa **tokikoa** da; irudiak ez dira inoiz zerbitzarira igotzen.

## Errendimendua

**CMYK modua bereizmen osoan astuna da** (lau plakaraino prozesatzen ditu tinta-isuri organikoarekin banan-banan), horregatik dago aurrebista-sistema. **Mono** modua nabarmen azkarragoa da. **2× esportazioa CMYKn** segundo batzuk har ditzake irudiaren tamainaren eta ekipoaren arabera.

## Bateragarritasuna

Web Worker, Canvas 2D eta `localStorage` onartzen dituzten nabigatzaile modernoak. Chromium eta Firefoxen probatua.

---

## Pribatutasuna

FOTOKOPIAk ez du daturik inora bidaltzen. Ez dago analitikarik, ez sarerik, ez fitxategi-igoerarik. Zure nabigatzailean irekitzen duzuna zure nabigatzailean geratzen da.

## Kredituak

**B_RR_K_** tresna. Paper-testura txertatuak Texturelabs eskaneoetan oinarrituak. Tipografiak: Bebas Neue eta JetBrains Mono.
