Versio: 1.1 (beta)

Julkaistu: 9.5.2016



# Avoimen rajapinnan määritelmä

Kaikki ohjelmistot siirtävät informaatiota ohjelmiston sisäisten ja ulkoisten ohjelmistorajapintojen läpi. Avoin rajapinta (engl. Open Application Programming Interface, Open API) on ohjelmistorajapinta, jonka kaikki ominaisuudet ovat sekä julkisia että niitä voi käyttää ilman rajoittavia ehtoja. Rajapintaa hyödyntävän sovelluksen voi esimerkiksi laatia ilman rajapinnan ohjelmistovalmistajan erillistä hyväksyntää tai pakollisia lisenssimaksuja.<sup>[1]</sup> Tämä edellyttää, että sekä rajapintakuvaus että siihen liittyvä dokumentaatio ovat avoimesti saatavilla. Sen lisäksi rajapintaa on voitava vapaasti käyttää esimerkiksi omien sovellusten sekä tekemiseksi että niiden testaamiseksi.

Avoimen rajapinnan käyttö on maksutonta. Käyttäjän ei tarvitse kysyä lupaa rajapinnan haltijalta tai ilmoittaa etukäteen, mihin tarkoitukseen rajapintaa aikoo käyttää. Rajapintapalvelun julkisissa käyttöehdoissa voidaan määritellä, millä edellytyksillä (esimerkiksi palvelunestohyökkäysten torjumiseksi) rajapinnan käyttöä voidaan rajoittaa erikoistapauksissa. 

<i>Kommentti: Rajapinnan dokumentaatiosta ja testiaineistoista ei peritä maksua. Rajapinnan takana olevasta varsinaiseen tietosisältöön käsiksi pääsemisestä voidaan periä myös maksu, vaikka rajapinta olisi avoin.</i>

## Rajapinta

Ohjelmointirajapinta määrittelee, miten ohjelmisto tarjoaa tietoja tai palveluita sovelluksille tai muille tietojärjestelmille.

<i>Kommentti: Tämän dokumentin kannalta mielenkiintoiset rajapinnat ovat yleensä Internetin yli käytettäviä Web Service -rajapintoja. Samat periaatteet pätevät kuitenkin muihinkin toteutuksiin. Avoimen rajapinnan määritelmä pyrkii olemaan mahdollisimman riippumaton sen teknologisista toteuttamistavasta.</i>

**Rajapinta voi olla:** 

**1) datarajapinta**, jonka kautta saa luettua palvelun sisältämän datan toisiin järjestelmiin. 

**2) toiminnallinen rajapinta**, joka tarjoaa esimerkiksi laskenta-algoritmeja tai mahdollisuuden käsitellä ohjelmiston sisältämiä tietoja eri tavoin rajapinnan kautta. Jos tietojärjestelmässä tai organisaatiolla on useita erilaisia rajapintoja, on syytä täsmentää, mitkä niistä ovat avoimia.

<i>Kommentti: Esimerkki datarajapinnasta on kansalaisaloite.fi:n rajapinta<sup>[2]</sup>, joka kertoo kansalaisalotteiden tietoja. Esimerkkejä toiminnallisista rajapinnoista ovat muun muassa Helsingin seudun liikenteen reittioppaan rajapinta<sup>[3]</sup>, joka tarjoaa reititysalgoritmin tai kansainvälinen Open311-rajapintastandardi<sup>[4]</sup>, jota tukeviin kaupunkien palautejärjestelmiin voi tehdä vikailmoituksia.</i>

## Avoin rajapinta

*suhde: rajapinnan haltija - käyttäjä*

Jotta rajapinnan voi sanoa olevan avoin, sen täytyy täyttää seuraavat ehdot:

**1) Avoimesti dokumentoitu:** Rajapinta on määritelty ja sen dokumentaatio on verkon kautta avoimesti saatavilla ja vapaasti käytettävissä.  Rajapinnan toiminnan kuvaavan dokumentaation on oltava kattava ja sen on tarjottava toimivia koodiesimerkkejä rajapinnan hyödyntämisestä eri tavoin. Järjestelmän sisältämät tiedot, niiden rakenne ja rajapinnat on dokumentoitu riittävällä tarkkuudella, jotta rajapinnan käyttöönotto ja hyödyntäminen on mahdollisimman vaivatonta. Dokumentaatioon kuuluu myös rajapinnan avoimesti esitetty elinkaarisuunnitelma. Rajapinnan elinkaari voi poiketa sen taustalla toimivan tietojärjestelmän elinkaaresta.

<i>Kommentti: Dokumentaation tulee riittää itsenäiseen kehitykseen ilman, että käyttäjän tarvitsee kysyä toimittajalta lisätietoja. Jos järjestelmä käyttää epästandardeja tietoformaatteja, myös niiden rakenne ja käsittely tulee dokumentoida kattavasti avoimesti. Ylivoimaisesti suurimpia esteitä rajapintojen hyödyntämiselle on niiden hyvin puutteellinen dokumentaatio.</i>

**2) Käyttöönotettava:** Avoin rajapinta on mahdollista ottaa käyttöön ilman ylläpitäjän tai järjestelmätoimittajan toimia myös virka-ajan ulkopuolella. Mahdolliset rekisteröitymiset ovat automaattisia. Käyttäjälle voidaan esimerkiksi luoda automaattisesti api-avain (tilastollinen käytön seuranta ja alustava liikenteen priorisointi). Käyttöönottoa tulee tukea asiakaslähtöisesti niin, että käyttäjän ongelmatilanteista opitaan ja palautteeseen reagoidaan. Avoimen rajapinnan on toimittava luotettavasti.

<i>Kommentti: Tämän ei tarvitse tarkoittaa pääsyä tuotantojärjestelmään, eikä vaatimus siten estä tuotantojärjestelmän käyttöoikeuksien hallintaa.</i>

**3) Testattava:** Rajapinnan tulee olla testattavissa. Testausta varten on tarjolla on vähintään testiaineisto. Testattavuuden voi toteuttaa seuraavilla tavoilla:

a. avoin pääsy tuotantojärjestelmään, jota käyttäen palveluun voi integroitua, tai

b. avoin pääsy testijärjestelmään, jossa on realistista tai autenttista dataa, tai

c. testijärjestelmä on ladattavissa vapaasti omaan käyttöön itse asennettavaksi

Avoimen rajapinnan kautta saatavan datan ei tarvitse olla avointa dataa<sup>[5]</sup>. Rajapinta voi olla avoin, vaikka siihen liitetty tuotantojärjestelmä olisi kokonaan irti Internetistä ja siihen olisi pääsy vain hyvin rajatulla joukolla. Jos rajapinta on avoin, mutta pääsy sen päässä olevaan datasisältöön on rajoitettu, tarjolla tulee olla avoimesti verkossa käytettävissä oleva testiympäristö.

<i>Kommentti: Jos järjestelmään on tarjolla avoin rajapinta, ei se tarkoita, että tuotantojärjestelmään tai sen sisältämään tietoon pääsisi kuka vain käsiksi. Esimerkiksi potilastietojärjestelmään voi olla avoin rajapinta, mutta rajapinnan takana olevat potilastiedot eivät ole avoimia. Avoimen rajapinnan kautta voidaan myös tarjota tiettyä henkilöä koskevia tietoja vain tämän omalla suostumuksella joko hänelle pelkästään tai hänen hyväksymälle taholle (engl. my data / suomeksi omadata). Rajapinta voi tarjota myös erilaisia pääsy- ja käyttöoikeuksia eri käyttäjille ja käyttäjä voidaan tunnistaa usealla eri tavalla tai näiden yhdistelmällä.</i>

Rajapinnan avoimuus mahdollistaa myös sen, että kuka tahansa voi tehdä kilpailevan tietojärjestelmän, joka toteuttaa samat rajapinnat ja on näin yhteensopiva kaikkien rajapintaa hyödyntävien sovellusten kanssa.

## Tilaajan hallitsema rajapinta

*suhde: toimittaja - tilaaja*

Tilaajan hallitsema rajapinta tarkoittaa rajapintaa, jota järjestelmän tilaajalla on oikeus käyttää ja levittää haluamallaan tavalla. Tällöin tilaaja voi halutessaan avata rajapinnan järjestelmätoimittajasta riippumatta. Mikäli näin ei tehdä, ei rajapinta ole ulkopuolisille avoin, eli rajapinta ei ole yleisesti ottaen avoin rajapinta.

[1]: http://www.kdk.fi/fi/kokonaisarkkitehtuuri/sanasto
[2]: https://www.kansalaisaloite.fi/api
[3]: http://developer.reittiopas.fi/pages/fi/reittiopas-api
[4]: http://www.open311.org/
[5]: http://opendefinition.org/
