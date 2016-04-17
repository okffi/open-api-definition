# Usein kysyttyjä kysymyksiä ja vastauksia


### Tarkoittaako määritelmä, että kaikki organisaation digitaalinen tieto on avattava avoimeksi dataksi?

Ei tarkoita. Vaikka rajapinta on avoin, ei se tarkoita, että kaikkien tietojen tulisi olla avoimia. 
Rajapinta kattaa usein pienen osajoukon koko organisaation informaatiosta. Tarpeen mukaisesti. Toisin sanoen rajapinnan kautta on usein pääsy osaan tiedoista, ei kaikkeen tietoon. Alla olevassa kuvassa organisaatiolla on 4 erilaista avointa rajapintaa (Open Application Protocol Interface, OAPI), jotka kattavat eri suuruiset ja eri osat organisaation digitaalisessa muodossa olevaa informaatiota. Vaikka kaikki rajapinnat ovat avoimia jää niiden ulkopuolelle merkittävä osa organisaation digitaalisesta tiedosta. Tässä esimerkissä (kuva 1) avoimet rajapinnat 1-4 käsittelevät eri tietoa, mutta teoriassa osa tiedoista voisi myös olla jollain tavalla päällekkäisiä (käsittelevät osittain samaa tietoa).

![Tietojärjestelmissä oleva tieto vs. rajapinnan tarjoama tieto](/organisaation_tiedot_eri_tietojarjestelmissa.png)

*Kuva 1. Kuvassa pinta-ala havainnollistaa tiedon määrää. OAPIt 1-4 käsittelevät organisaation sähköisen tiedon eri osia. Osa organisaation tiedosta jää avoimien rajapintojen ulkopuolelle. Tyypillisesti tälläistä tietoa on esimerkiksi salassapidettävä tieto julkisella sektorilla tai esimerkiksi Henkilötietolain ja tulevan EU:n henkilötieto-asetuksen (engl. General Data Protection Regulation, GDPR) alla oleva tieto.*

### Tarkoittaako määritelmä, että kenellä tahansa pitää olla oikeus päästä tietoon?

Ei tarkoita. Vaikka rajapinta olisi avoin, ei se tarkoita, että siihen käyttöoikeus pitäisi olla kaikilla. Rajapinnan käyttöä voidaan hallita esimerkiksi API-avaimella (joka ainoastaan tunnistaa käyttäjän tilastointitarkoituksessa, ei varsinaisesti tietoturvamielessä) tai vaikkapa SSL:n yli käyttäjätunnuksella ja salasanalla.


### Mitä hyötyä määritelmästä on?

Suomessa ostetaan ohjelmistoja ja niihin liittyviä palveluita miljardeilla euroilla joka vuosi. Julkinen sektori 
(kunnat ja valtio) ovat Suomessa suurin tietotekniikan hyödyntäjä. Jotta todellinen tietojohtaminen (tiedolla johtaminen ja tiedon johtaminen) voisi tietojärjestelmien kohdalla toteutua, on niiden siiloutuneesta rakenteesta päästävä eroon. Nykytilanteessa samoja tietoja on useissa eri järjestelmissä ja organisaatioiden informaatio arkkitehtuuri on syntynyt sattuminen ja valmiiden ohjelmistojen kautta. Rajapinnat ovat digitaalisten informaatiovirtojen avainkomponetteja. Avoimen rajapinnan määritelmää voi käyttää esimerkiksi tarjouspyyntöjen osana julkisen ja yksityisensektorin tietojärjestelmäkilpailutuksissa. Määritelmällä torjutaan ns. toimittalukkoa ja edistetään alan tervettä kilpailua, josta on pitkällä aikavälillä hyötyä kaikille. Toisaalta avoimuus helpottaa kokeilukulttuuria sekä tukee teknologista organisaation ketteryyttä.


### Miten rajapintoja voi käytännössä rakentaa?

Lähes kaikille ohjelmointikielille (esimerkiksi Node.js, PHP, Python, Ruby, Objective-C, .NET ja Java) on olemassa valmiita toteutuksia rajapinnoista. Niitä vähän muokkaamalla saa nopeasti luotua rajapinnan. Esimerkiksi avoimen lähdekoodin Mulesoftilla (https://www.mulesoft.com/) uuden rajapinnan luominen onnistuu ohjelmiston ammattilaiselta jopa 15 minuutissa. Usein rajapintaa tehdessä kannattaa kuitenkin suunnitella sitä käyttäjälähtöisesti, jolloin suunnittelluun kannattaa käyttää enemmän aikaa. Mulesoft on tarkoitettu eri tietojärjestelmien väliseen tietojen integrointiin. Se tukee sekä kooditason muokkausta että graafista työskentelyä. Myös monet pilvipohjaiset alustat, kuten Amazon Web Services (AWS), tarjoavat valmiita työkaluja rajapintojen rakentamiseen.


### Mitä rajapintojen rakentamisessa pitäisi aivan erityisesti huomioida?

1. *Luotettavuus.* Rajapinnan on oltava huokutteleva, jotta kehittäjät kiinnostuvat siitä. Mikäli rajapinta ei ole luotettava, ei sen päälle rakenneta helposti mitään. Toisaalta myös rajapinnan elinkaari on jollain tasolla näkyvissä. Ohjelmistokehittäjä ei lähtökohtaisesti halua rakentaa sellaisen rajapinnan päälle, joka ei toimi oikein tai jos rajapinnan olemassaolosta lähitulevaisuudessa ei voi olla varma.
2. *Käyttäjät.* Suunnittele ja toteuta rajapinnat todelliseen asiakastarpeeseen ja tue niiden käyttäjiä kaikin mahdollisin keinoin.
3. *Monitoroi käyttöä.* Seuraa käyttöä ja skaalaa tarvittaessa ylös tai alas. Rajapinnan käytön seuranta auttaa jatkuvasti oppimaan lisää ja kehittämään suunnittelua sekä toteutusta. Kannattaa siis kuunnella sekä käyttäjiä että katsoa myös rajapinnan käyttödataa.


### Mitä muuta kannattaisi ottaa huomioon?

Rajapintoihin liittyy muutama käsite, joita kannattaa myös huomioida.

*Dataformaatti.* Sama rajapinta voi tukea useita dataformaatteja. Esimerkiksi JSON, XML tai joku muu. Teknologiat kehittyvät, joten dataformaatteja tulee jatkossa lisää.

*Tietomalli,* joka määrittelee, miten datan sisältämät osat liittyvät toisiinsa. Tietomalli voidaan esittää graafisesti esimerkiksi UML:n avulla.


### Avoin rajapinta vai avoin rakenteellinen tiedosto (CSV, XML)?

Rajapinta on hyvä silloin, jos dataa on paljon ja se päivittyy usein. Niissä tapauksissa tiedostoja pitäisi muistaa ladata jatkuvasti (tietojen vanhentuminen) ja tiedostot ovat suuria kooltaan, jolloin niitä on usein haasteellista käsitellä. Tiedosto on hyvä taas silloin, kun dataa on vähän ja/tai data päivittyy harvoin (esimerkiksi kerran vuodessa tai harvemmin). Digitaalisen tiedon määrän arvioidaan kasvavan jopa 60% vuodessa, joten avoimessa tiedossa ollaan suuressa mittakaavassa siirtymässä avoimista tiedostoista avoimiin rajapintoihin. Toisinaan voi olla järkevää tarjota sekä tiedosto että avoin rajapinta. Rajapinta mahdollistaa kuitenkin resurssitehokkaamman tavan toimia, koska sen ei tarvitse käsitellä "ylimääräistä" tietojoukkoa missään tiedon jalostamistamisen vaiheessa.


### Miksi ei anneta suoraa käyttöoikeuksia tietokantaan?

Usein suorat tietokannan käyttöoikeudet eivät ole tietoturvallisia. Siksi väliin tarvitaan hyvä rajapinta, joka myös suojelee organisaatiota. Toisaalta api mahdollistaa informaation uudelleenmuotoilua ja esimerkiksi kuormituksentasausta.

### Miten avoin rajapinta liittyy kansalliseen palveluväylään eli X-roadiin?
Periaatteessa X-road tarjoaa rajapintoja siihen liittyneille organisaatiolle. X-roadiin liittymistä on kuitenkin rajoitettu ja se on lähinnä tarkoitettu julkisten organisaatioiden käyttöön. Toisaalta X-road on ennenkaikkea eri organisaatioiden välinen teknologia siirtää ja integroida tietoa. Sen lisäksi täytyy toteuttaa erikseen yleensä organisaation sisäinen integraatio eri tietojärjestelmien välillä. Aika näyttää, mihin suuntaan X-road kehittyy.

### Mitä tämä kaikki tarkoittaa rahallisesti?

Esimerkiksi Suomen toiseksi suurimmassa kaupungissa Espoossa (noin 270 000 asukasta) on arvioitu, että oikein tehdyllä integraatioilla voidaan säästää noin 1 000 000 euroa joka vuosi.

Espoossa ja Turussa asiakastietojärjestelmän liittäminen toiminnanohjausjärjestelmään on maksanut noin 150 000 euroa. Liittämisen hintaan ei vaikuttanut, vaikka sama tietojärjestelmä-integraatio on toteutettu jo muissa kunnissa (ohjelmistotoimittajalla se on valmiina yhden toteutuksen jälkeen). Espoossa integraatioihin varattu budjetti on noin 20% koko tietojärjestelmäbudjetista.

Espoo investoi uusiin tietojärjestelmiin vuonna 2016 noin 8,6 miljoonaa euroa. **Integraatioihin tästä kohdistuu 20%, eli noin 1,7 miljoonaa euroa.** Tämä laskenta-arvo on täysin tekninen, eikä se huomioi paljon suurempia kustannuksia, kuten sitä, kuinka paljon maksaa, kun työntekijät tekevät päällekkäistä työtä syöttämällä samoja tietoja useampiin tietojärjestelmiin tai esimerkiksi millaisia vaaratilanteita tai/ja kustannuksiksia syntyy, jos toimintaan virheelliseen / vanhentuneen tiedon perusteella.

Tässä Espoon itse tekemät arviot kustannussäästöistä.


#### Hyötypotentiaaliksi arvioidaan seuraavanlaisesti

|Kokonaiskustannukset|Integraatiokustannukset|Säästöt integraatiosta|
|---|---|---|---|
|Suuret tietojärjestelmät|6 595 008 €|1 319 201 €|197 880 €|
|Keskisuuret tietojärjestelmät| 3 553 075 €| 710 615 €| 142 123 €|
|Pienet tietojärjestelmät |645 824 €| 96 873 €| 19 374 €|
|Yhteensä|10 794 907 €| 2 126 690 €| 359 377 €|


#### Uusien tietojärjestelmien kohdalla

|Investointikustannukset|Integraatiokustannukset|Säästöt integraatiosta|
|---|---|---|
|8 600 000 €|1 720 000 €|602 000 €|

||Säästöt per vuosi|
|---|---|
|Nykyiset tietojärjestelmät|359 377 €|
|Uudet tietojärjestelmät|602 000 €|
|Yhteensä|961 377 €|

Espoon tapauksessa laskelmat ovat suuntaa-antavia. Esimerkiksi näiden asioiden arvoa rahallisesti 
on vaikeaa arvioida:

1.	Päällekkäisen tiedon syöttämiseen (turhaa työtä) ja käsittelyyn kuluva työaika. Tämä on suurin kustannus, jota voidaan arvioida vain hyvin karkealla tasolla. Työntekijöiden aikaa tuhlaantuu tähän joka viikko useita tunteja eri arvioiden mukaan. Esimerkiksi Espoon tapauksessa kaupungin työntekijöitä on 14 000, joiden työaikaa kuluu päällekkäiseen ja turhaa työhön tietojärjestelmien parissa. Lisäksi jokaisen kuntalaisen aikaa menee hukkaan, kun omia tietoja joutuu syöttämään ja päivittämään eri tietojärjestelmiin esimerkiksi paperilomakkeilla (täysin turhaa, koska tiedot eivät siirry järjestelmästä toiseen automaattisesti rajapintojen sulkeutuneisuuden takia).

2.	Organisaation virheellinen toiminta väärän tai vanhentuneen tiedon perusteella ja tämän kerrannaisvaikutukset. Tehdäänkö esimerkiksi kunnassa / kaupungissa viisaita päätöksiä, jos ne perustuvat vain valistuneeseen arvaukseen varsinaisen oikean tiedon sijaan?

3.	Syntymättä jäävät yritykset ja innovaatiot, kun tietoa ei pysty käsittelemään vapaasti. Suomi on korkean osaamisen maa, jossa tulevaisuuden menestys perustuu korkeaan osaamiseen eli tietointesiiviseen liiketoimintaan.

Avoimilla ja hyvin toimivilla rajapinnoilla on siis merkittävä vaikutus organisaatioiden toimintaan ja tehokkuuteen. Siksi niiden määrittely on tärkeää ja tarpeellista työtä.

**Lähde:** Julkisen hallinnon tietohallinnon neuvottelukunta ([JUHTA:n kokousasiakirjat vuonna 2016 / 1. JUHTA:n kokous 17.2.2016 / Liite 3 C, Integraatioalustan rahoitushakemus](https://wiki.julkict.fi/julkict/juhta/juhta-n-kokousasiakirjat-vuonna-2016/1-juhta-n-kokous-17-2.2016/Liite%203%20C-%20Integraatioalustan%20rahoitushakemus.zip/view))
