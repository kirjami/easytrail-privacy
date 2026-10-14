# Privacy Policy for EasyTrail / EasyTrailin Tietosuojaseloste

[In English](#in-english) | [Suomeksi](#suomeksi)

---

<a name="in-english"></a>
## In English

**Last updated:** October 14, 2026

EasyTrail ("we", "our", or "app") is a specialized mountain biking and outdoor navigation application developed to provide real-time route recording, navigation guidance, tile hunting exploration, heart rate monitoring, and weather safety alerts. We are committed to protecting your privacy. This Privacy Policy explains how EasyTrail handles your data and outlines the terms regarding safety, data handling, and user responsibility.

### 1. Data Collection and Usage

EasyTrail is designed with an offline-first, privacy-by-design architecture: **we do not operate personal user accounts, and we do not collect, store, transmit, or sell your personal data on external servers.** All activity and navigation data stays locally on your device.

#### a. Location Data (Foreground and Background)
- **What we access:** Precise GPS location (`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`) and background location access (`ACCESS_BACKGROUND_LOCATION`).
- **Why we need it:**
  * To record your route path, distance, speed, and elevation profiles in real time.
  * To register and capture visited map tiles (Tile Hunting / Explorer Tiles) on the OpenStreetMap Zoom 14 grid as you traverse terrain.
  * To provide turn-by-turn navigation and waypoint alerts via Text-to-Speech (TTS).
  * To analyze weather hazards along your active path, alerting you to approaching rain radar fronts and nearby lightning strikes.
- **Background usage:** When a workout, route recording, or tile hunting session is active, EasyTrail operates an Android Foreground Service (`TrackingService`) to track your location continuously even when your screen is locked, turned off, or when you switch to another app. Location polling terminates immediately when you pause or finish the recording session.
- **Storage:** GPS tracks are saved locally on your device as standard GPX/GeoJSON files. Tile hunting progress is stored locally in an on-device Room database. No location coordinates or captured tile histories are ever transmitted to developer or third-party servers.

#### b. Tile Hunting Data (Ruutujen metsästys)
- **What is processed:** Geographic coordinates of visited OpenStreetMap Zoom 14 Slippy Map tiles, tile visit counts, and grid cluster metrics (Max Square, Max Cluster, and Max Connected Area).
- **Processing and imports:** All tile calculations, including batch GPX or KML history parsing, execute entirely on-device within the local database engine. No activity files or personal movement heatmaps are uploaded to external cloud services.
- **Compatibility:** Tile algorithms adhere to open OpenStreetMap standards and public VeloViewer/StatsHunters rule sets for user verification, but EasyTrail operates as an independent offline client and does not synchronize data with those platforms unless you manually export and upload files yourself.

#### c. Health and Sensor Data (Heart Rate)
- **What we access:** Real-time heart rate measurements via Bluetooth Low Energy (BLE) sensors (heart rate straps, sports watches) using `BLUETOOTH_SCAN` and `BLUETOOTH_CONNECT`.
- **Why we need it:** To compute real-time heart rate training zones (Z1–Z5), color-code track segments by cardiovascular intensity, and embed heart rate telemetry into locally saved GPX tracks via standard TrackPointExtension schemas.
- **Privacy:** Bluetooth scanning is explicitly flagged as `neverForLocation`. Sensor readings are processed purely in real time and saved inside your local files. Sensor telemetry is never sent off-device.

#### d. Weather and Environmental Data
- EasyTrail queries public open-data APIs:
  * **Finnish Meteorological Institute (FMI):** WMS radar composite imagery and WFS lightning observation vectors (CC BY 4.0).
  * **Open-Meteo:** Global wind vector models and forecasts (CC BY 4.0).
- These requests submit bounding coordinates strictly to fetch relevant visual map tiles and weather vectors. No persistent user identifiers, advertising IDs, or tracking cookies are attached to these network calls.

#### e. Children and Minors
EasyTrail is suitable for outdoor enthusiasts of various ages, including teenagers aged 13 and older. Because all activity data and location coordinates are stored strictly on a local device and no accounts or cloud profiles are maintained, no personal data from minors is collected on external servers. If you are a parent or guardian and have any questions regarding minors using EasyTrail, please contact us at easytrail.dev@gmail.com.

### 2. Third-Party Services and Data Sharing

EasyTrail does **not** sell, broker, or transmit your personal, location, fitness, or tile exploration data to third parties.
- **Map Rendering:** Offline and cached maps are rendered locally using MapLibre GL Native with open spatial datasets (OpenStreetMap, MapAnt Finland).
- **Application Updates (Google Play):** EasyTrail uses the official Google Play In-App Updates library (`app-update-ktx`) to check for and install application updates directly via Google Play Store services without collecting personal user profiles or telemetry.
- **User-Initiated Export & Privacy Filters:** You maintain exclusive custody of your GPX and KML files. When sharing or exporting routes via the system share sheet, EasyTrail provides privacy tools to strip heart rate telemetry and absolute timestamps, enabling you to share geographic routes without disclosing personal biometric schedules.

### 3. Permissions Summary
- **Location (`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`, `ACCESS_BACKGROUND_LOCATION`):** Required for route recording, tile hunting capture, turn-by-turn guidance, and real-time weather alerts when active or locked.
- **Bluetooth (`BLUETOOTH_SCAN`, `BLUETOOTH_CONNECT`):** Required for pairing and streaming data from external BLE heart rate monitors.
- **Notifications & Foreground Service (`POST_NOTIFICATIONS`, `FOREGROUND_SERVICE`):** Required (especially on Android 13+) to display continuous status notifications during background recording and voice guidance when the device is locked in your pocket or pack.
- **Vibration (`VIBRATE`):** Used for haptic navigation cues, tile discovery notifications, and lightning proximity alerts.

### 4. Data Retention and Deletion
All application states, routes, waypoints, and tile hunting records reside exclusively on local device storage:
- You can clear individual routes or reset tile hunting records directly within application settings and sheet menus.
- Uninstalling EasyTrail or wiping application storage via Android system settings irreversibly purges all local databases, recorded GPX tracks, and cached map tiles.

### 5. Disclaimer and Safety Notice

#### a. Fitness and Heart Rate Tracking (Non-Medical Use)
EasyTrail is strictly a recreational outdoor sports tool. **EasyTrail is not a medical device, and none of its features, metrics, heart rate readings, or training zone estimations (Z1–Z5) are intended for medical diagnosis, health monitoring, treatment, or prevention of any disease or acute health condition.** Always consult a licensed medical professional before beginning strenuous athletic activity or if you experience cardiovascular symptoms.

#### b. Navigation, Route Safety, and Outdoor Risks
Mountain biking, backcountry trail navigation, and tile hunting across unfamiliar terrain carry inherent physical risks, including falls, collisions, exhaustion, severe weather encounters, and disorientation.
- Map datasets, trail classifications, GPS coordinates, elevation figures, and weather feeds originate from open third-party sources and satellite networks. Information may contain inaccuracies, seasonal trail closures, private property changes, or signal loss.
- **Tile hunting caution:** Do not enter dangerous terrain, steep cliffs, restricted private property, nature reserves with restricted access, or hazardous railway/highway corridors in pursuit of map tiles.
- **Assumption of Risk:** You participate in outdoor activities and route navigation entirely at your own risk and discretion. You are responsible for route vetting, physical stamina, safety gear, environmental situational awareness, and respecting local laws, landowners, and access rights (Jokamiehenoikeus).
- **Limitation of Liability:** To the maximum extent permitted under applicable law, the author of EasyTrail disclaims all liability for direct, indirect, incidental, or consequential damages, personal injuries, health emergencies, property damage, or losses resulting from the use or technical unavailability of this software.

### 6. Contact Us
For questions, feedback, or inquiries regarding this Privacy Policy:
- **Email:** easytrail.dev@gmail.com

---

<a name="suomeksi"></a>
## Suomeksi

**Päivitetty viimeksi:** 14. lokakuuta 2026

EasyTrail ("me" tai "sovellus") on maastopyöräilyyn ja ulkoiluun kehitetty navigointisovellus, joka tarjoaa reaaliaikaisen reitintallennuksen, ääniohjauksen, karttaruutujen valloituksen (Tile Hunting), sykemittauksen ja sääturvallisuusvaroitukset. Olemme sitoutuneet suojelemaan yksityisyyttäsi. Tämä tietosuojaseloste kuvaa, miten EasyTrail käsittelee tietojasi sekä määrittelee sovelluksen turvallisuusehdot ja vastuunjaon.

### 1. Tietojen kerääminen ja käyttö

EasyTrail noudattaa periaatetta, jossa käyttäjän yksityisyys ja tietojen paikallisuus ovat ensisijaisia: **emme ylläpidä käyttäjätilejä emmekä kerää, tallenna, siirrä tai myy henkilötietojasi ulkoisille palvelimille.** Kaikki harjoitus-, reitti- ja karttadata säilytetään ainoastaan omalla laitteellasi.

#### a. Sijaintitiedot (Etualalla ja taustalla)
- **Mitä tietoja käytetään:** Tarkka GPS-sijainti (`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`) ja taustasijainti (`ACCESS_BACKGROUND_LOCATION`).
- **Mihin tietoa käytetään:**
  * Reitin, matkan, nopeuden ja korkeusprofiilin reaaliaikaiseen tallentamiseen.
  * Uusien karttaruutujen havaitsemiseen ja valloittamiseen (OpenStreetMap Zoom 14 -ruudukko) maastossa liikuttaessa.
  * Käännös- ja reittipisteopastukseen puhesynteesillä (TTS).
  * Säävaarojen arviointiin reitillä (lähestyvät sadealueet ja lähialueen salamahavainnot).
- **Käyttö taustalla:** Kun harjoituksen tallennus, navigointi tai ruutujen metsästys on aktiivinen, EasyTrail käyttää Androidin taustapalvelua (`TrackingService` / Foreground Service) sijaintisi seuraamiseen ja tiilien valloitukseen myös silloin, kun näyttö on suljettuna, puhelin on taskussa tai käytät toista sovellusta. Paikannus ja taustapalvelu pysähtyvät välittömästi, kun keskeytät tai päätät tallennuksen.
- **Tallennus:** Tallennetut reitit tallennetaan laitteesi sisäiseen muistiin standardeina GPX/GeoJSON-tiedostoina. Valloitetut tiilitiedot tallennetaan laitteen paikalliseen Room-tietokantaan. Sijaintikoordinaatteja tai valloitettuja ruutuja ei lähetetä omille tai ulkopuolisille palvelimille.

#### b. Ruutujen metsästys (Tile Hunting)
- **Käsiteltävät tiedot:** Vierailtujen OpenStreetMap Zoom 14 Slippy Map -tiilien koordinaatit, käyntikerrat sekä klusteritilastot (suurin neliö, suurin klusteri ja suurin yhtenäinen alue).
- **Tietojen käsittely ja tuonti:** Kaikki tilastolaskenta sekä GPX- ja KML-historian tuonti ja läpikäynti suoritetaan 100 % paikallisesti laitteessasi. Sovellus ei lähetä reittihistoriaasi tai valloituskarttojasi pilvipalveluihin.
- **Yhteensopivuus:** Laskentalogiikka noudattaa avointa OpenStreetMap-ruudukkoa sekä yleisiä VeloViewer- ja StatsHunters-sääntöjä, mutta EasyTrail toimii itsenäisenä paikallisena sovelluksena eikä synkronoi tietoja näihin palveluihin ilman käyttäjän manuaalisesti tekemää tiedostovientiä.

#### c. Terveys- ja sensoritiedot (Syke)
- **Mitä tietoja käytetään:** Sykelukemat langattomista Bluetooth Low Energy (BLE) -antureista (sykevyöt, urheilukellot) käyttäen lupia `BLUETOOTH_SCAN` ja `BLUETOOTH_CONNECT`.
- **Mihin tietoa käytetään:** Reaaliaikaisten sykealueiden (Z1–Z5) laskentaan, reittijäljen värikoodaukseen rasitustason mukaan sekä syketiedon tallentamiseen GPX-reittipisteisiin standardinmukaisena TrackPointExtension-laajennuksena.
- **Yksityisyys:** Bluetooth-skannausta ei käytetä sijainnin määrittämiseen (`neverForLocation`). Syketiedot käsitellään ainoastaan laitteessa reaaliaikaisesti ja tallennetaan paikalliseen tiedostoon. Tietoja ei luovuteta ulkoisille tahoille.

#### d. Sää- ja ympäristötiedot
- EasyTrail hakee havainto- ja ennustedataa julkisista avoimen datan rajapinnoista:
  * **Ilmatieteen laitos (FMI):** WMS-sadetutkakuvat ja WFS-salamahavainnot (CC BY 4.0).
  * **Open-Meteo:** Tuuliennustemallit ja -vektorit (CC BY 4.0).
- Rajapintapyyntöjen mukana välitetään ainoastaan tarkasteltavan karttaikkunan rajauskoordinaatit tarvittavan säädatan noutamiseksi. Pyynnöissä ei lähetetä käyttäjätunnisteita tai seurantatietoja.

#### e. Alaikäiset ja nuoret käyttäjät
Sovellus soveltuu kaikenikäisille ulkoilijoille, mukaan lukien yli 13-vuotiaat nuoret. Koska kaikki harjoitustiedot ja sijaintikoordinaatit tallennetaan ainoastaan laitteen paikalliseen muistiin eikä palvelimia tai käyttäjätilejä käytetä, alaikäisten henkilötietoja ei kerätä ulkoisiin järjestelmiin. Mikäli olet huoltaja ja sinulla on kysyttävää alaikäisten tietojen käsittelystä EasyTrailissa, voit ottaa yhteyttä sähköpostitse osoitteeseen easytrail.dev@gmail.com.

### 2. Kolmannen osapuolen palvelut ja tiedonsiirto

EasyTrail **ei** jaa, myy tai luovuta henkilö-, sijainti-, liikunta- tai tiilitietojasi mainostajille tai tiedonvälittäjille.
- **Karttapalvelut:** Kartat ja polkuaineistot piirretään laitteessa MapLibre GL Native -moottorilla käyttäen avoimia aineistoja (OpenStreetMap, MapAnt Suomi).
- **Sovelluspäivitykset (Google Play):** Sovellus käyttää virallista Google Play In-App Updates -kirjastoa (`app-update-ktx`) päivitysten tarkistamiseen ja asentamiseen suoraan Google Play Kaupan kautta ilman henkilökohtaista käyttäjäseurantaa.
- **Tiedostojen hallinta ja yksityisyyssuoja:** Omistat ja hallitset reittitiedostojasi täysin itse. Reittejä jaettaessa EasyTrail tarjoaa mahdollisuuden poistaa syke- ja aikatiedot tiedostosta, jolloin voit jakaa puhtaan maastoreitin ilman henkilökohtaisia biometrisiä tietoja tai aikaleimoja.

### 3. Sovelluksen käyttöoikeudet
- **Sijainti (`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`, `ACCESS_BACKGROUND_LOCATION`):** Tarvitaan GPS-navigointiin, reitin tallentamiseen, karttaruutujen valloitukseen ja paikallisiin säähälytyksiin etualalla ja taustalla.
- **Bluetooth (`BLUETOOTH_SCAN`, `BLUETOOTH_CONNECT`):** Tarvitaan yhteyden muodostamiseen langattomiin BLE-sykeantureihin.
- **Ilmoitukset ja taustapalvelu (`POST_NOTIFICATIONS`, `FOREGROUND_SERVICE`):** Tarvitaan (erityisesti Android 13+ -laitteilla) jatkuvan tilanneilmoituksen näyttämiseen ja ääniopastukseen puhelimen ollessa lukittuna taustatallennuksen aikana.
- **Värinä (`VIBRATE`):** Käytetään haptisiin ilmoituksiin (reittipoikkeamat, uudet karttaruudut, lähestyvä sade, salamavaroitukset).

### 4. Tietojen säilytys ja poistaminen
Kaikki tallennetut reitit, rastit, asetukset ja ruututietokannat säilytetään vain laitteesi paikallisessa muistissa:
- Voit poistaa yksittäisiä reittejä tai tyhjentää ruutuhistorian sovelluksen valikoista.
- Sovelluksen poistaminen laitteesta tai sovellustietojen tyhjentäminen Androidin asetuksista poistaa kaikki tietokannat, reitit ja välimuistitiedot pysyvästi.

### 5. Vastuuvapauslauseke ja turvallisuus

#### a. Kuntoilu- ja syketiedot (Ei lääketieteellistä käyttöä)
EasyTrail on puhtaasti vapaa-ajan liikuntaan ja harrastustoimintaan tarkoitettu apuväline. **EasyTrail ei ole lääkinnällinen laite, eikä mitään sen esittämistä tiedoista, sykelukemista tai harjoitusalueista (Z1–Z5) tule käyttää lääketieteelliseen arviointiin, diagnooseihin tai sairauden hoitoon.** Keskustele aina lääkärin tai terveydenhuollon ammattilaisen kanssa ennen raskaan liikunnan aloittamista.

#### b. Navigointi, maastoturvallisuus ja vastuu
Maastopyöräily, luonnossa liikkuminen ja ruutujen metsästys tuntemattomassa maastossa sisältävät aina loukkaantumis-, eksymis- ja tapaturmariskejä.
- Kartta- ja maastoaineistot, polkuluokitukset, GPS-sijainti sekä säävaroitukset perustuvat avoimiin tietolähteisiin ja satelliittipaikannukseen. Tiedot voivat sisältää puutteita, maastomuutoksia, katvealueita tai tilapäisiä virheitä.
- **Huomio ruutujen metsästyksessä:** Älä koskaan vaaranna turvallisuuttasi tai kulje vaarallisille jyrkänteille, ratapihoille, moottoriteille, viljelyksille, pihapiireihin tai luonnonsuojelualueiden liikkumiskieltoalueille karttaruudun tavoittelemiseksi.
- **Käyttäjän oma vastuu:** Liikut maastossa ja liikenteessä aina täysin omalla vastuullasi. Vastaat itse omasta reittisuunnittelustasi, varusteistasi, voimavarojesi arvioinnista, tilannetajustasi maastossa sekä jokamiehenoikeuksien ja paikallisten sääntöjen noudattamisesta.
- **Vastuunrajoitus:** Sikäli kuin soveltuva lainsäädäntö sen sallii, sovelluksen kehittäjä ei vastaa mistään välittömistä tai välillisistä vahingoista, loukkaantumisista, tapaturmista, eksymisistä, kalustorikoista tai aineellisista haitoista, jotka aiheutuvat tai joiden väitetään aiheutuneen EasyTrailin käytöstä.

### 6. Yhteystiedot
Jos sinulla on kysyttävää tästä tietosuojaselosteesta tai vastuuehdoista, voit ottaa yhteyttä kehittäjään:
- **Sähköposti:** easytrail.dev@gmail.com
