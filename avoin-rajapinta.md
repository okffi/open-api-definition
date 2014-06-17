Version: 0.8

# Mikä on avoin rajapinta?

Tässä dokumentissa määritellään selkeästi, mikä on avoin rajapinta. Täsmällistä määrittelyä tarvitaan esimerkiksi julkisissa järjestelmähankinnoissa, joissa usein vaaditaan avoimia rajapintoja. Ilman määritelmää lähes mitä tahansa rajapintaa saatetaan kutsua avoimeksi, vaikka käytännössä rajapinnan dokumentaation saisi vain maksullisena tai pääsyä rajapintaan rajoitettaisiin sopimuksilla.

Rajapinta on avoin, jos kuka vain voi kehittää sitä käyttävän sovelluksen. Tähän ei riitä pelkkä dokumentaatio, vaan itse rajapintaan pitää päästä käsiksi, jotta omaa sovellusta voi testata. Avoimen rajapinnan käyttö on maksutonta, eikä käyttäjän tarvitse kysyä lupaa rajapinnan haltijalta tai kertoa etukäteen mitä on tekemässä.


## Rajapinta

Ohjelmointirajapinta (Application programming interface, API) on määritelmä, jonka mukaan eri ohjelmat voivat tehdä pyyntöjä ja vaihtaa tietoja keskenään.

Rajapinta voi olla pelkkä datarajapinta kuten kansalaisaloite.fi:n rajapinta, jonka kautta saa luettua palvelun sisältämän datan toisiin järjestelmiin. Lukuoikeuksien (read) lisäksi rajapinnan kautta voi olla mahdollista myös syöttää (insert), päivittää (update) tai poistaa (delete) dataa.

Järjestelmä voi tarjota myös laskenta-algoritmeja tai muita ohjelmallisia toimintoja rajapinnan kautta palveluna muille järjestelmille. Esimerkkejä tällaisista toiminnallisista rajapinnoista ovat muun muassa Helsingin seudun liikenteen reittioppaan rajapinta, joka tarjoaa reititysalgoritmin tai kansainvälinen Open311-rajapintastandardi, jota tukeviin kaupunkien palautejärjestelmiin voi tehdä vikailmoituksia. Jos järjestelmässä on erikseen datarajapinta ja toiminnallinen rajapinta, on syytä täsmentää, minkä osien on tarkoitus olla avoimia.


## Avoin rajapinta

Jotta rajapinnan voi sanoa olevan avoin, sen täytyy täyttää seuraavat ehdot:

1. Dokumentoitu: Rajapinta on määritelty ja sen dokumentaatio on verkon kautta avoimesti saatavilla. Järjestelmän sisältämät tiedot, niiden rakenne ja rajapinnat tulee  dokumentoida riittävällä tarkkuudella, jotta rajapinnan käyttöönotto ja  hyödyntäminen on vaivatonta.

2. Käyttöönotettava: Avoin rajapinta on mahdollista ottaa käyttöön ilman ylläpitäjän tai järjestelmätoimittajan toimia myös virka-ajan ulkopuolella. Mahdolliset rekisteröitymiset ovat automaattisia.

3. Testattava: Koekäyttöä varten on tarjolla on vähintään testiaineisto. Testattavuuden voi toteuttaa seuraavilla tavoilla:
- avoin pääsy tuotantojärjestelmään, jota käyttäen palveluun voi integroitua, tai
- avoin pääsy testijärjestelmään, API-selaimeen tai konsoliin, jossa on realistista tai autenttista dataa, tai
- testijärjestelmä on ladattavissa vapaasti omaan käyttöön itse asennettavaksi

Avoimen rajapinnan kautta saatava datan ei tarvitse olla avointa dataa. Esimerkiksi potilastietojärjestelmään voi olla avoin rajapinta, mutta potilastiedot eivät ole avoimia. Jos järjestelmään on tarjolla avoin rajapinta, se ei tarkoita, että tuotantojärjestelmään tai sen sisältämään tietoon pääsisi kuka vain käsiksi. Rajapinta voi olla avoin, vaikka tuotantojärjestelmä olisi kokonaan irti internetistä ja pääsy siihen vain hyvin rajatulla joukolla. Tällöin tarjolla pitää kuitenkin olla avoimesti verkossa oleva testiympäristö.







<table>
    <tr>
        <td>ESIMERKKI</td>
        <td>SULJETTU</td>
        <td>TILAAJAN HALLITSEMA</td>
        <td>AVOIN</td>
        <td>KOMMENTTI</td>
    </tr>
    <tr>
        <td>Palveluun on rajapinta tarjolla, ja palvelun toimittaja on sitoutunut tarjoamaan sen asiakkaidensa osoittamille kolmansille osapuolille</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>Palvelun datarajapintaan pääsee vapaasti käsiksi, se on julkisesti netissä ja esimerkkikoodia löytyy googlella, mutta toiminnalliseen rajapintaan ei ole pääsyä.</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>Palveluun on olemassa toiminnallinen rajapinta. Päästäkseen siihen käsiksi täytyy pyytää käyttöavain palvelun tarjoajalta, koska palvelu ei kestäisi vapaan käytön kuormitusta. Käytännössä lupa myönnetään aina.</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>Palveluun on rajapinta, jonka määrittelyt ja dokumentaatio ovat vapasti saatavilla. Itse palveluun ei pääse vapaasti käsiksi, koska se sisältää ihmisten henkilötietoja. Palveluntarjoaja pitää kuitenkin yllä testipalvelinta, jossa on esimerkkidataa, ja testipalvelimeen pääsee käsiksi luomalla itselleen tunnuksen palveluntarjoajan järjestelmään.</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
</table>

# Liite 1: Huomiota ja hyviä käytäntöjä

Avoimen rajapinnan määritelmä ottaa kantaa vain siihen, milloin rajapinta on avoin ja milloin ei. Alle on koottu joitakin avoimista rajapinnoista puhuttaessa yleisesti esiin nousevia huomiota liittyen muun muassa rajapintojen hyötyihin, standardointiin yms.

*Avoimien rajapintojen hyötyjä:* Tärkeä syy avoimien rajapintojen vaatimiseen on halu välttää toimittajalukkoa. Avoimien rajapintojen avulla lisäominaisuudet voi tilata muiltakin toimittajilta, koska järjestelmän sisältämät tiedot on saatavilla rajapintojen kautta. Ilman avoimia rajapintoja usein ainoastaan alkuperäinen järjestelmätoimittaja pystyy  tekemään muutokset. Myös vaihtoehtoisten sovellusten ja käyttöliittymien kehittäminen on helppoa sellaisiin järjestelmiin, joissa on avoimet rajapinnat. Sovellusten kehittäminen voi tapahtua riippumatta rajapinnan ylläpitäjäorganisaatiosta saatika alkuperäisen järjestelmän toimittajasta.

*Tilaajan hallitsema rajapinta:* Tilaajan hallitsema rajapinta tarkoittaa rajapintaa, jota järjestelmän tilaajalla on oikeus käyttää ja levittää haluamallaan tavalla. Tilaaja voi halutessaan avata rajapinnan järjestelmäntoimittajasta tai sovelluksen käyttämästä riippumatta, mutta mikäli näin ei tehdä kyse ei ole avoimesta rajapinnasta. Tekeillä olevat JIT ehdot määrittelevät, että ostajalla pitää olla mahdollisuus halutessaan avata rajapinta (laittaa dokumentaatio ja testiaineisto verkkoon yms.) ilman, että toimittaja puuttuu siihen. JIT-ehdot eivät kuitenkaan vaadi, että kaikissa julkishallinnon ostamissa ohjelmistoissa rajapinnat olisi pakko avata, vaan tämä jää ostajan harkintaan.

*Standardointi:* Rajapintojen toteutuksessa kannattaa suosia yleisesti käytettyjä standardeja, protokollia sekä formaatteja. Käytännössä rajapinta voidaan toteuttaa esimerkiksi REST-arkkitehtuurin mukaisesti siten, että sen kautta järjestelmän tiedot saadaan koneluettavana XML-muodossa sekä selainpohjaisia sovelluksia varten JSON-muodossa. Tässä kiteytyksessä ei oteta kantaa harmonisointiin. Harmonisointi on kuitenkin looginen kehityskulku, jotta kaikki avoimet rajapinnat eivät olisi keskenään erilaisia, vaan syntyisi ainakin toimialakohtaisesti yhteisiä käytänteitä.

*Rajapinnan käyttö ilman rekisteröitymistä:* Rajapinnan avoimuus ei velvoita tarjoamaan pääsyä tuotantojärjestelmään tai tuotantodataan vapaasti, vaan sen osalta voidaan vaatia esim. palvelutasosopimus (Service Level Agreement, SLA). Jos itse tuotantojärjestelmään ei ole pääsyä, tarvitaan testijärjestelmä avoimesti kehittämistä varten.

*Kuormitusrajoitukset:* Avoin rajapinta kannattaa toteuttaa siten, että sitä kuormittamalla ei voi tahattomasti aiheuttaa uhkaa tai haittaa tietojärjestelmän muulle käytölle. Vaikkapa kutsujen määrää per aikayksikkö voi teknisesti rajoittaa. Rajoitustoiminnot saattavat aiheuttaa tarpeita kahdentaa osia tietojärjestelmästä (vrt. Reittiopas)

*Muita vastaavia määritelmiä:* Vastaavaa avoimien rajapintojen määritelmää ei ole, mutta sisältöä voi verrata avoimen lähdekoodin määritelmään ja suomennettuun avoimen datan ja avoimen sisällön määritelmään. Englanniksi on olemassa muun muassa The Open API Principles.
