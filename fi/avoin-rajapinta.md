Versio: 1.0

Julkaistu: 11.10.2014



# Avoimen rajapinnan määritelmä

Avoin rajapinta on rajapinta, jonka kaikki ominaisuudet ovat julkisia ja jota voi käyttää ilman rajoittavia ehtoja (esimerkiksi laatia rajapintaa hyödyntävän ohjelman ilman rajapinnan valmistajan erillistä hyväksyntää tai pakollisia lisenssimaksuja).<sup>[1]</sup> Tämä edellyttää, että rajapintakuvaus ja sen dokumentaatio on avoimesti saatavilla ja että rajapintaa voi vapaasti käyttää esimerkiksi omien sovellusten tekemiseksi ja niiden testaamiseksi. Avoimen rajapinnan käyttö on maksutonta, eikä käyttäjän tarvitse kysyä lupaa rajapinnan haltijalta tai kertoa etukäteen mihin tarkoitukseen aikoo rajapintaa käyttää.

<i>Kommentti: Rajapinnan dokumentaatiosta ja testiaineistoista ei peritä maksua, mutta palvelun varsinaiseen tietosisältöön käsiksi pääsemisestä voidaan periä myös maksu, vaikka rajapinta olisi avoin.</i>

## Rajapinta

Ohjelmointirajapinta (Application programming interface, API) määrittelee, miten ohjelmisto tarjoaa tietoja tai palveluita sovelluksille tai muille tietojärjestelmille.

<i>Kommentti: Tämän dokumentin kannalta mielenkiintoiset rajapinnat ovat yleensä Internetin yli käytettäviä Web Service -rajapintoja. Samat periaatteet pätevät kuitenkin muunkinlaisiin toteutuksiin. Avoimen rajapinnan määritelmä on riippumaton toteutusteknologiasta.</i>

Rajapinta voi olla pelkkä **datarajapinta** jonka kautta saa luettua palvelun sisältämän datan toisiin järjestelmiin, tai se voi olla **toiminnallinen rajapinta**, joka tarjoaa myös laskenta-algoritmeja tai mahdollisuuden muuttaa järjestelmän tietoja rajapinnan kautta. Jos järjestelmässä on useita erilaisia  rajapintoja, on syytä täsmentää, mitkä niistä ovat avoimia.

<i>Kommentti: Esimerkki datarajapinnasta on kansalaisaloite.fi:n rajapinta<sup>[2]</sup>, joka kertoo kansalaisalotteiden tietoja. Esimerkkejä toiminnallisista rajapinnoista ovat muun muassa Helsingin seudun liikenteen reittioppaan rajapinta<sup>[3]</sup>, joka tarjoaa reititysalgoritmin tai kansainvälinen Open311-rajapintastandardi<sup>[4]</sup>, jota tukeviin kaupunkien palautejärjestelmiin voi tehdä vikailmoituksia.</i>

## Avoin rajapinta

*suhde: rajapinnan haltija - käyttäjä*

Jotta rajapinnan voi sanoa olevan avoin, sen täytyy täyttää seuraavat ehdot:

1) **Avoimesti dokumentoitu:** Rajapinta on määritelty ja sen dokumentaatio on verkon kautta avoimesti saatavilla ja vapaasti käytettävissä. Järjestelmän sisältämät tiedot, niiden rakenne ja rajapinnat on dokumentoitu riittävällä tarkkuudella, jotta rajapinnan käyttöönotto ja hyödyntäminen on mahdollisimman vaivatonta.

<i>Kommentti: Dokumentaation tulee riittää itsenäiseen kehitykseen ilman, että käyttäjän tarvitsee kysyä toimittajalta lisätietoja. Jos järjestelmä käyttää epästandardeja tietoformaatteja, myös niiden rakenne ja käsittely tulee dokumentoida avoimesti.</i>

2) **Käyttöönotettava:** Avoin rajapinta on mahdollista ottaa käyttöön ilman ylläpitäjän tai järjestelmätoimittajan toimia myös virka-ajan ulkopuolella. Mahdolliset rekisteröitymiset ovat automaattisia.

<i>Kommentti: Tämän ei tarvitse tarkoittaa pääsyä tuotantojärjestelmään, eikä vaatimus siten estä tuotantojärjestelmän käyttövaltuuksien hallintaa.</i>

3) **Testattava:** Rajapinnan tulee olla testattavissa. Testausta varten on tarjolla on vähintään testiaineisto. Testattavuuden voi toteuttaa seuraavilla tavoilla:

  1. avoin pääsy tuotantojärjestelmään, jota käyttäen palveluun voi integroitua, tai

  2. avoin pääsy testijärjestelmään, jossa on realistista tai autenttista dataa, tai

  3. testijärjestelmä on ladattavissa vapaasti omaan käyttöön itse asennettavaksi

Avoimen rajapinnan kautta saatavan datan ei tarvitse olla avointa dataa<sup>[5]</sup>. Rajapinta voi olla avoin, vaikka tuotantojärjestelmä olisi kokonaan irti Internetistä ja pääsy siihen vain hyvin rajatulla joukolla. Jos rajapinta on avoin, mutta pääsy datasisältöön on rajoitettu, tarjolla tulee olla avoimesti verkossa käytettävissä oleva testiympäristö

<i>Kommentti: Jos järjestelmään on tarjolla avoin rajapinta, se ei tarkoita, että tuotantojärjestelmään tai sen sisältämään tietoon pääsisi kuka vain käsiksi. Esimerkiksi potilastietojärjestelmään voi olla avoin rajapinta, mutta potilastiedot eivät ole avoimia. Avoimen rajapinnan kautta voidaan myös tarjota tiettyä henkilöä koskevia tietoja vain tämän omalla suostumuksella (my data).</i>

Rajapinnan avoimuus mahdollistaa myös sen, että kuka tahansa voi tehdä kilpailevan järjestelmän, joka toteuttaa samat rajapinnat ja on näin yhteensopiva kaikkien rajapintaa hyödyntävien sovellusten kanssa.

## Tilaajan hallitsema rajapinta

*suhde: toimittaja - tilaaja*

Tilaajan hallitsema rajapinta tarkoittaa rajapintaa, jota järjestelmän tilaajalla on oikeus käyttää ja levittää haluamallaan tavalla. Tällöin tilaaja voi halutessaan avata rajapinnan järjestelmäntoimittajasta riippumatta, mutta mikäli näin ei tehdä kyse ei ole avoimesta rajapinnasta. Mikäli tilaaja ei avaa rajapintaa, ei rajapinta ole ulkopuolisille avoin, jolloin kyse ei ole yleisesti ottaen avoimesta rajapinnasta.


[1]: http://www.kdk.fi/fi/kokonaisarkkitehtuuri/sanasto
[2]: https://www.kansalaisaloite.fi/api
[3]: http://developer.reittiopas.fi/pages/fi/reittiopas-api
[4]: http://www.open311.org/
[5]: http://opendefinition.org/
