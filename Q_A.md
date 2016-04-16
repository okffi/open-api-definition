# Usein kysyttyjä kysymyksiä ja vastauksia

###Tarkoittaako määritelmä, että kaikki organisaation digitaalinen tieto on avattava avoimeksi dataksi?
Ei tarkoita. Vaikka rajapinta on avoin, ei se tarkoita, että kaikkien tietojen tulisi olla avoimia. 
Rajapinta kattaa usein pienen osajoukon koko organisaation informaatiosta. Tarpeen mukaisesti. Toisin sanoen rajapinnan kautta on 
usein pääsy osaan tiedoista, ei kaikkeen tietoon.

###Tarkoittaako määritelmä, että kenellä tahansa pitää olla oikeus päästä tietoon?
Ei tarkoita. Vaikka rajapinta olisi avoin, ei se tarkoita, että siihen käyttöoikeus pitäisi olla kaikilla. Rajapinnan 
käyttöä voidaan hallita esimerkiksi api-avaimella (joka ainoastaan tunnistaa käyttäjän 
tilastointitarkoituksessa, ei varsinaisesti tietoturvamielessä) tai vaikkapa SSL:n yli käyttäjätunnuksella ja salasanalla.

###Mitä hyötyä määritelmästä on?
Suomessa ostetaan ohjelmistoja ja niihin liittyviä palveluita miljardeilla euroilla joka vuosi. Julkinen sektori 
(kunnat ja valtio) ovat Suomessa suurin tietotekniikan hyödyntäjä. Jotta todellinen tietojohtaminen (tiedolla johtaminen ja 
tiedon johtaminen) voisi tietojärjestelmien kohdalla toteutua, on niiden siiloutuneesta rakenteesta päästävä eroon. Nykytilanteessa samoja tietoja on useissa eri järjestelmissä ja organisaatioiden informaatio arkkitehtuuri on syntynyt sattuminen ja valmiiden ohjelmistojen kautta. Rajapinnat ovat digitaalisten informaatiovirtojen avainkomponetteja. Avoimen rajapinnan määritelmää voi käyttää esimerkiksi tarjouspyyntöjen osana julkisen ja yksityisensektorin tietojärjestelmäkilpailutuksissa. Määritelmällä torjutaan ns. toimittalukkoa ja edistetään alan tervettä kilpailua, josta on pitkällä aikavälillä hyötyä kaikille.

###Miten rajapintoja voi käytännössä rakentaa?
Lähes kaikille ohjelmistokielille (esimerkiksi Node.js, PHP, Python, Rails, Obj-C, .NET ja Java) on olemassa valmiita toteutuksia rajapinnoista. Niitä vähän muokkaamalla saa nopeasti luotua rajapinnan. Esimerkiksi avoimen lähdekoodin Mulesoftilla (https://www.mulesoft.com/) uuden rajapinnan luominen onnistuu ohjelmiston ammattilaiselta jopa 15 minuutissa. Usein rajapintaa tehdessä kannattaa kuitenkin suunnitella sitä käyttäjälähtöisesti, jolloin suunnittelluun kannattaa käyttää enemmän aikaa. Mulesoft on tarkoittettu eri tietojärjestelmien väliseen tietojen integrointiin. Se tukee sekä kooditason muokkausta että graaffista työskentelyä. Myös monet pilvipohjaiset alustat, kuten Amazon Cloud tarjoaa valmiit työkalut rajapintojen rakentamiseen.

###Mitä rajapintojen rakentamisessa pitäisi aivan erityisesti huomioida?
1. Luotettavuus. Kehittäjistä rajapintojen kanssa kovaa kisaa. Mikäli rajapinta ei ole luotettava, ei sen päälle rakenneta helposti mitään.
2. Käyttäjät. Suunnittele ja toteuta rajapinnat todelliseen asiakastarpeeseen ja tue niiden käyttäjiä kaikin mahdollisin keinoin.
3. Monitoroi käyttöä. Seuraa käyttöä ja skaalaa tarvittaessa suuntaan tai toiseen. Rajapinnan käytön seuranta auttaa jatkuvasti oppimaan lisää ja kehittämään suunnittelua ja toteutusta. Kannattaa siis kuunnella sekä käyttäjiä että katsoa rajapinnan käyttödataa.

###Mitä muuta kannattaisi ottaa huomioon?
Rajapintoihin liittyy muutama käsite, joita kannattaa myös huomioida.
Dataformaatti. Sama rajapinta voi tukea useita dataformaatteja. Esimerkiksi JSON, XML tai joku muu. Teknologiat kehittyvät, joten dataformaatteja tulee jatkossa lisää.
Tietomalli, joka määrittelee, miten datan sisältämät osat liittyvät toisiinsa. Tietomalli voidaan esittää graaffisesti esimerkiksi UML:n avulla.

###Avoin rajapinta vai avoin rakenteellinen tiedosto (CSV, XML)?
Rajapinta on hyvä silloin, jos dataa on paljon ja se päivittyy usein. Niissä tapauksissa tiedostoja pitäisi muistaa ladata jatkuvasti (tietojen vanhentuminen) ja tiedostot ovat suuria kooltaan, jolloin niitä on usein haasteellista käsitellä. Tiedosto on hyvä taas silloin, kun dataa on vähän ja / tai se päivittyy harvoin (esimerkiksi kerran vuodessa tai harvemmin). Digitaalisen tiedon määrän arvioidaan kasvavan jopa 60 % vuodessa, joten avoimessa tiedossa ollaan suuressa mittakaavassa siirtymässä avoimista tiedostoista avoimiin rajapintoihin. Toisinaan voi olla järkevää tarjota sekä tiedosto että avoin rajapinta.
