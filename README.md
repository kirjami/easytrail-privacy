# Privacy Policy for EasyTrail / EasyTrailin Tietosuojaseloste

[In English](#in-english) | [Suomeksi](#suomeksi)

---

<a name="in-english"></a>
## In English

**Last updated:** September 12, 2026

EasyTrail ("we", "our", or "app") is a specialized mountain biking and outdoor navigation application developed to provide real-time route recording, navigation guidance, heart rate monitoring, and weather safety alerts. We are committed to protecting your privacy. This Privacy Policy explains how EasyTrail handles your data.

### 1. Data Collection and Usage

EasyTrail is designed with a privacy-first approach: **we do not operate personal user accounts, and we do not collect, store, or sell your personal data on external servers.** All core activity data stays locally on your device.

#### a. Location Data (Foreground and Background)
* **What we access:** Precise GPS location (`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`) and background location (`ACCESS_BACKGROUND_LOCATION`).
* **Why we need it:**
  * To record your route, distance, speed, and elevation in real time.
  * To provide turn-by-turn and waypoint voice alerts via Text-to-Speech (TTS).
  * To analyze weather hazards along your route, specifically alerting you to approaching rain fronts and nearby lightning strikes.
* **Background usage:** When a workout or navigation session is active, EasyTrail uses an Android Foreground Service to track your location even when your screen is turned off or when you switch to another app. Location tracking stops immediately when you pause or finish your workout.
* **Storage:** Recorded tracks are saved locally on your device as standard GPX/GeoJSON files. No location coordinates are uploaded to our servers.

#### b. Health and Sensor Data (Heart Rate)
* **What we access:** Heart rate data via Bluetooth Low Energy (BLE) sensors (heart rate belts, compatible sports watches) using `BLUETOOTH_SCAN` and `BLUETOOTH_CONNECT`.
* **Why we need it:** To display real-time heart rate zones during your ride and embed heart rate telemetry into your saved GPX tracks.
* **Privacy:** EasyTrail does not use Bluetooth scanning to infer your location (`neverForLocation`). Heart rate data is processed in real time and saved only inside your local GPX file.

#### c. Weather and Environmental Data
* EasyTrail queries open, public weather APIs:
  * **Finnish Meteorological Institute (FMI):** WMS radar images and WFS lightning observation data (CC BY 4.0).
  * **Open-Meteo:** Wind vector forecasts (CC BY 4.0).
* These requests transmit coordinates solely to fetch relevant local weather tiles and observation points. No persistent user identifiers or tracking cookies are attached to these network requests.

### 2. Third-Party Services and Data Sharing

EasyTrail does **not** share, sell, or monetize your personal, location, or health data with advertisers or data brokers.
* **Map Services:** Map tiles and trail data are rendered using open-source MapLibre GL Native and OpenStreetMap/MapAnt open datasets.
* **Local Storage:** You have full ownership and control of your GPX files. You may export, share, or delete them at any time using your device's file manager or the app's route library.

### 3. Permissions Summary
* **Location:** Required for GPS navigation, route tracking, and localized weather hazard calculations.
* **Bluetooth:** Required to pair with external BLE heart rate monitors.
* **Notifications & Foreground Service:** Required to maintain continuous recording and voice prompts when the device is locked in your pocket or pack.
* **Vibration:** Used for haptic alerts indicating waypoints, lightning warnings, or approaching rain.

### 4. Data Retention and Deletion
Since all recorded routes, waypoints, and settings are stored locally on your device's internal storage:
* You can delete individual routes directly from the in-app library.
* Uninstalling EasyTrail or clearing the app storage permanently removes all stored application data.

### 5. Contact Us
If you have any questions or suggestions regarding this Privacy Policy, you may contact the developer at:
* **Email:** easytrail.dev@gmail.com

---

<a name="suomeksi"></a>
## Suomeksi

**Päivitetty viimeksi:** 12. syyskuuta 2026

EasyTrail ("me" tai "sovellus") on maastopyöräilyyn ja ulkoiluun suunniteltu navigointisovellus, joka tarjoaa reaaliaikaisen reitintallennuksen, ääniohjauksen, sykemittauksen ja sääturvallisuusvaroitukset. Olemme sitoutuneet suojelemaan yksityisyyttäsi. Tämä tietosuojaseloste kuvaa, miten EasyTrail käsittelee tietojasi.

### 1. Tietojen kerääminen ja käyttö

EasyTrail noudattaa periaatetta, jossa käyttäjän yksityisyys on etusijalla: **emme ylläpidä käyttäjätilejä emmekä kerää, tallenna tai myy henkilötietojasi ulkoisille palvelimille.** Kaikki lenkki- ja aktiviteettidata säilytetään vain omalla laitteellasi.

#### a. Sijaintitiedot (Etualalla ja taustalla)
* **Mitä tietoja käytetään:** Tarkka GPS-sijainti (`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`) ja taustasijainti (`ACCESS_BACKGROUND_LOCATION`).
* **Mihin tietoa käytetään:**
  * Reitin, matkan, nopeuden ja korkeusprofiilin reaaliaikaiseen tallentamiseen.
  * Käännös- ja rastikohtaisiin ääniohjeisiin (puhesynteesi / TTS).
  * Säävaarojen havaitsemiseen reitin varrella (lähestyvät sadealueet ja lähialueen salamaniskut).
* **Käyttö taustalla:** Kun harjoituksen tallennus tai navigointi on käynnissä, EasyTrail käyttää Androidin taustapalvelua (Foreground Service) sijainnin seuraamiseen myös näytön ollessa sammutettuna tai kun käytät toista sovellusta. Paikannus päättyy välittömästi, kun keskeytät tai lopetat tallennuksen.
* **Tallennus:** Tallennetut reitit tallennetaan laitteesi sisäiseen muistiin vakiomuotoisina GPX/GeoJSON-tiedostoina. Koordinaatteja ei lähetetä omille tai kolmannen osapuolen palvelimille.

#### b. Terveys- ja sensoritiedot (Syke)
* **Mitä tietoja käytetään:** Sykelukemat Bluetooth Low Energy (BLE) -antureista (sykevyöt, urheilukellot) käyttäen lupia `BLUETOOTH_SCAN` ja `BLUETOOTH_CONNECT`.
* **Mihin tietoa käytetään:** Reaaliaikaisten sykealueiden näyttämiseen suorituksen aikana ja syketiedon tallentamiseen GPX-reittipisteisiin.
* **Yksityisyys:** Bluetooth-skannausta ei käytetä sijainnin määrittämiseen (`neverForLocation`). Syketiedot käsitellään vain laitteessa ja tallennetaan paikalliseen reittitiedostoon.

#### c. Sää- ja ympäristötiedot
* EasyTrail hakee tietoja julkisista avoimen datan rajapinnoista:
  * **Ilmatieteen laitos (FMI):** WMS-sadetutkakuvat ja WFS-salamahavainnot (CC BY 4.0).
  * **Open-Meteo:** Tuuliennustemallit (CC BY 4.0).
* Näihin palveluihin välitetään ainoastaan kyseisen kartta-alueen koordinaatit säätietojen noutamiseksi. Pyynnöissä ei välitetä käyttäjätunnisteita tai seurantatietoja.

### 2. Kolmannen osapuolen palvelut ja tiedonsiirto

EasyTrail **ei** jaa, myy tai luovuta henkilö-, sijainti- tai terveystietojasi mainostajille tai tiedonvälittäjille.
* **Karttapalvelut:** Kartat ja polkuaineistot piirretään avoimen lähdekoodin MapLibre GL Native -moottorilla hyödyntäen OpenStreetMap- ja MapAnt-aineistoja.
* **Tiedostojen hallinta:** Omistat ja hallitset GPX-tiedostojasi täysin itse. Voit viedä, jakaa tai poistaa niitä milloin tahansa sovelluksen reittikirjaston tai laitteen tiedostonhallinnan kautta.

### 3. Sovelluksen käyttöoikeudet
* **Sijainti:** Tarvitaan GPS-navigointiin, reitin tallentamiseen ja paikallisiin säähälytyksiin.
* **Bluetooth:** Tarvitaan yhteyden muodostamiseen langattomiin BLE-sykeantureihin.
* **Ilmoitukset ja taustapalvelu:** Tarvitaan jatkuvaan reitin tallennukseen ja ääniopastukseen puhelimen ollessa taskussa.
* **Värinä:** Käytetään haptisiin hälytyksiin (reittipoikkeamat, lähestyvä sade, salamavaroitukset).

### 4. Tietojen säilytys ja poistaminen
Koska kaikki tallennetut reitit, rastit ja asetukset säilytetään vain laitteesi muistissa:
* Voit poistaa yksittäisiä reittejä milloin tahansa sovelluksen kirjastosta.
* Sovelluksen poistaminen laitteesta tai sovellustietojen tyhjentäminen poistaa kaikki tallennetut tiedot pysyvästi.

### 5. Yhteystiedot
Jos sinulla on kysyttävää tästä tietosuojaselosteesta, voit ottaa yhteyttä kehittäjään:
* **Sähköposti:** easytrail.dev@gmail.com
