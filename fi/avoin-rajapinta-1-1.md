Versio: 1.1 (beta)

Julkaistu: 9.5.2016



# Avoimen ohjelmistorajapinnan määritelmä

Kaikki ohjelmistot siirtävät informaatiota ohjelmiston sisäisten ja ulkoisten ohjelmistorajapintojen läpi. Avoin ohjelmistorajapinta  (engl. Open Application Programming Interface, Open API) on ohjelmistorajapinta, jonka **1) kaikki ominaisuudet ovat julkisia** sekä **2) niitä voi käyttää ilman rajoittavia ehtoja**. Ohjelmistorajapintaa hyödyntävän sovelluksen voi esimerkiksi laatia ilman ohjelmistorajapinnan ohjelmistovalmistajan erillistä hyväksyntää tai pakollisia lisenssimaksuja.<sup>[1]</sup> Tämä edellyttää, että sekä ohjelmistorajapintakuvaus että siihen liittyvä riittävän laaja dokumentaatio ovat avoimesti saatavilla. Sen lisäksi ohjelmistorajapintaa on voitava vapaasti käyttää esimerkiksi omien sovellusten sekä tekemiseksi että niiden testaamiseksi.

Avoimen ohjelmistorajapinnan **käyttö on maksutonta**. **Käyttäjän ei tarvitse kysyä lupaa ohjelmistorajapinnan haltijalta tai ilmoittaa etukäteen, mihin tarkoitukseen ohjelmistorajapintaa aikoo käyttää**. Ohjelmistorajapintapalvelun julkisissa ja avoimissa käyttöehdoissa voidaan määritellä, millä edellytyksillä (esimerkiksi palvelunestohyökkäysten torjumiseksi) ohjelmistorajapinnan käyttöä voidaan rajoittaa erikoistapauksissa.

<i>Kommentti: Ohjelmistorajapinnan dokumentaatiosta ja testiaineistoista ei peritä maksua. Ohjelmistorajapinnan takana olevasta varsinaiseen tietosisältöön (tietokantaan) käsiksi pääsemisestä voidaan periä myös maksu, vaikka ohjelmistorajapinta olisi avoin.</i>

## Ohjelmistorajapinta

Ohjelmistorajapinta määrittelee, miten ohjelmisto tarjoaa tietoja tai palveluita sovelluksille tai muille tietojärjestelmille.

<i>Kommentti: Tämän dokumentin kannalta mielenkiintoiset rajapinnat ovat yleensä Internetin yli käytettäviä Web Service -ohjelmistorajapintoja. Samat periaatteet pätevät kuitenkin muihinkin toteutuksiin. Avoimen ohjelmistorajapinnan määritelmä pyrkii olemaan mahdollisimman riippumaton sen teknologisesta toteuttamistavasta.</i>

**Ohjelmistorajapinta voi olla:** 

**1) informaatiorajapinta**, jonka kautta saa luettua palvelun sisältämän informaation toisiin tietojärjestelmiin. 

**2) toiminnallinen rajapinta**, joka tarjoaa esimerkiksi laskenta-algoritmeja tai mahdollisuuden käsitellä ohjelmiston sisältämiä tietoja eri tavoin ohjelmistorajapinnan kautta. Jos tietojärjestelmässä tai organisaatiolla on useita erilaisia ohjelmistorajapintoja, on syytä täsmentää, mitkä niistä ovat avoimia.

<i>Kommentti: Esimerkki datarajapinnasta on kansalaisaloite.fi:n rajapinta<sup>[2]</sup>, joka kertoo kansalaisalotteiden tietoja. Esimerkkejä toiminnallisista ohjelmistorajapinnoista ovat muun muassa Helsingin seudun liikenteen reittioppaan ohjelmistorajapinta<sup>[3]</sup>, joka tarjoaa reititysalgoritmin tai kansainvälinen Open311-rajapintastandardi<sup>[4]</sup>, jota tukeviin kaupunkien palautejärjestelmiin voi tehdä vikailmoituksia.</i>

## Avoin ohjelmistorajapinta

*suhde: rajapinnan haltija - käyttäjä*

Jotta ohjelmistorajapinnan voi sanoa olevan avoin, sen täytyy täyttää seuraavat ehdot:

**1) Avoimesti dokumentoitu:** Ohjelmistorajapinta on määritelty ja sen dokumentaatio on verkon kautta avoimesti saatavilla ja vapaasti käytettävissä.  **Ohjelmistorajapinnan toiminnan kuvaavan dokumentaation on oltava kattava ja sen on tarjottava toimivia koodiesimerkkejä ohjelmistorajapinnan hyödyntämisestä eri tavoin**. Järjestelmän sisältämät tiedot, niiden rakenne ja ohjelmistorajapinnat on dokumentoitu riittävällä tarkkuudella, jotta ojelmistorajapinnan käyttöönotto ja hyödyntäminen on mahdollisimman vaivatonta. Dokumentaatioon kuuluu myös ohjelmistorajapinnan avoimesti esitetty elinkaarisuunnitelma. Ohjelmistorajapinnan elinkaari voi poiketa sen taustalla toimivan tietojärjestelmän elinkaaresta.

<i>Kommentti: Dokumentaation tulee riittää itsenäiseen kehitykseen ilman, että käyttäjän tarvitsee kysyä toimittajalta lisätietoja. Jos järjestelmä käyttää epästandardeja tietoformaatteja, myös niiden rakenne ja käsittely tulee dokumentoida kattavasti avoimesti. Ylivoimaisesti suurimpia esteitä rajapintojen hyödyntämiselle on niiden hyvin puutteellinen dokumentaatio.</i>

**2) Käyttöönotettava:** Avoin rajapinta on mahdollista ottaa käyttöön ilman ylläpitäjän tai järjestelmätoimittajan toimia myös virka-ajan ulkopuolella. Mahdolliset rekisteröitymiset ovat automaattisia. Käyttäjälle voidaan esimerkiksi luoda automaattisesti api-avain (tilastollinen käytön seuranta ja alustava liikenteen priorisointi). Käyttöönottoa tulee tukea asiakaslähtöisesti niin, että käyttäjän ongelmatilanteista opitaan ja palautteeseen reagoidaan. **Avoimen ohjelmistorajapinnan on toimittava luotettavasti, koska sen ympärille muodostuu verkosto riippuvuussuhteita.** 

<i>Kommentti: Avoimen ohjelmistorajapinnan käyttöönoton ei tarvitse tarkoittaa suoraa pääsyä orgnisaation tuotantojärjestelmään, eikä vaatimus siten estä tuotantojärjestelmän käyttöoikeuksien hallintaa. Ohjelmistorajapinnan luotettava toiminta on erittäin tärkeää, koska esimerkiksi ohjelmistokehittäjät rakentavat sen varassa toimivia sovelluksia, joiden toiminta häiriintyy, mikäli ohjelmistorajapinta ei toimi oikein.</i>

**3) Testattava:** Ohjelmistorajapinnan tulee olla testattavissa. Testausta varten on tarjolla on vähintään testiaineisto. Testattavuuden voi toteuttaa seuraavilla tavoilla:

a. avoin pääsy tuotantojärjestelmään, jota käyttäen palveluun voi integroitua, tai

b. avoin pääsy testijärjestelmään, jossa on realistista tai autenttista dataa, tai

c. testijärjestelmä on ladattavissa vapaasti omaan käyttöön itse asennettavaksi

Avoimen ohjelmistorajapinnan kautta saatavan datan ei tarvitse olla avointa dataa<sup>[5]</sup>. Ohjelmistorajapinta voi olla avoin, vaikka siihen liitetty tuotantojärjestelmä olisi kokonaan irti internetistä ja siihen olisi pääsy vain hyvin rajatulla joukolla. Jos ohjelmistorajapinta on avoin, mutta pääsy sen päässä olevaan datasisältöön on rajoitettu, tarjolla tulee olla avoimesti verkossa käytettävissä oleva testiympäristö.

<i>Kommentti: Jos järjestelmään on tarjolla avoin ohjelmistorajapinta, ei se tarkoita, että tuotantojärjestelmään tai sen sisältämään tietoon pääsisi kuka tahansa käsiksi. Esimerkiksi potilastietojärjestelmään voi olla avoin ohjelmistorajapinta, mutta rajapinnan takana olevat potilastiedot eivät ole avoimia. Avoimen ohjelmistorajapinnan kautta voidaan myös tarjota tiettyä henkilöä koskevia tietoja vain tämän omalla suostumuksella joko hänelle pelkästään tai hänen hyväksymälle taholle (engl. MyData / suom. omadata). Ohjelmistorajapinta voi tarjota myös erilaisia pääsy- ja käyttöoikeuksia eri käyttäjille ja käyttäjä voidaan tunnistaa usealla eri tavalla tai näiden yhdistelmällä.</i>

Ohjelmistorajapinnan avoimuus mahdollistaa myös sen, että kuka tahansa voi tehdä kilpailevan tietojärjestelmän, joka toteuttaa samat ohjelmistorajapinnat ja on näin yhteensopiva kaikkien ohjelmistorajapintaa hyödyntävien sovellusten kanssa.

<i>Kommentti: Esimerkiksi maanmittauslaitoksessa ja tilastokeskuksella on avoimia ohjelmistorajapintoja, joiden määrittelytyö on tehty EU-tasolla. Näin ollen ohjelmistorajapinnat ovat kaikissa EU-maissa samanlaisia.</i>

## Tilaajan hallitsema ohjelmistorajapinta

*suhde: toimittaja - tilaaja*

Tilaajan hallitsema ohjelmistorajapinta tarkoittaa ohjelmistorajapintaa, jota järjestelmän tilaajalla on oikeus käyttää ja levittää haluamallaan tavalla. Tällöin tilaaja voi halutessaan avata ohjelmistorajapinnan järjestelmätoimittajasta riippumatta. Mikäli näin ei tehdä, ei rajapinta ole ulkopuolisille avoin, eli ohjelmistorajapinta ei ole yleisesti ottaen avoin ohjelmistorajapinta.

[1]: http://www.kdk.fi/fi/kokonaisarkkitehtuuri/sanasto
[2]: https://www.kansalaisaloite.fi/api
[3]: http://developer.reittiopas.fi/pages/fi/reittiopas-api
[4]: http://www.open311.org/
[5]: http://opendefinition.org/
