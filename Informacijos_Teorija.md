# **Klausimai**
## **I Dalis**
log2(įmanomų pranešimų kiekis) = vidutiniškai, kiek klausimų reikia paklausti vienam pranešimui išsiaiškinti.

Įmanomų pranešimų kiekis. Pvz.: abėcėlė turi 28 raides: a, b, c - įmonomas pranešimas, jų visuma ir yra įmonomų pranešimų kiekis.

Pvz.: Yra 5 kortos, 52 įmanomi pranešimai. Koks vidutinis klausimų kiekis?

log2(52) \* 5 = 28.5 klausimai.

<https://www.khanacademy.org/computing/computer-science/informationtheory/moderninfotheory/v/how-do-we-measure-information-language-of-coins-10-12>

### **Žmogaus kalbos ir alfabeto raidos istorija.  Paskaitos: 1) [Origins of written language](https://www.khanacademy.org/computing/computer-science/informationtheory/info-theory/v/language-of-coins-2-8-proto-writing) , 2) [History of the alphabet](https://www.khanacademy.org/computing/computer-science/informationtheory/info-theory/v/history-of-the-alphabet-language-of-coins-3-9)  .**

### **Šaltinio informacijos kodavimas ir vaizdo telegrafo veikimas. Paskaitos: 1) [Source encoding](https://www.khanacademy.org/computing/computer-science/informationtheory/info-theory/v/source-encoding-language-of-coins-4-9) 2) [Visual telegraphs](https://www.khanacademy.org/computing/computer-science/informationtheory/info-theory/v/history-of-optical-telegraphs-language-of-coins-5-9) .**
### **Elektrostatinio ir elektromagnetinio telegrafo veikimas. Morzės abėcėlė. Paskaitos: 1) [Electrostatic telegraphs](https://www.khanacademy.org/computing/computer-science/informationtheory/info-theory/v/history-of-static-electricity-language-of-coins-6-12) 2) [The battery and electromagnetism](https://www.khanacademy.org/computing/computer-science/informationtheory/info-theory/v/the-battery-electromagnetism) 3) [Morse code**](https://www.khanacademy.org/computing/computer-science/informationtheory/info-theory/v/morse-code-the-information-age-language-of-coins-8-12)**
### **Simbolių perdavimo greitis ir kanalo talpumas. Paskaitos: 1) [Symbol rate](https://www.khanacademy.org/computing/computer-science/informationtheory/moderninfotheory/v/symbol-rate-information-theory)   2) [Channel capacity**](https://www.khanacademy.org/computing/computer-science/informationtheory/moderninfotheory/v/intro-to-channel-capacity-information-theory)**
### **Informacijos kiekio pamatavimas. Markovo grandinės. Paskaitos: 1) [Measuring information](https://www.khanacademy.org/computing/computer-science/informationtheory/moderninfotheory/v/how-do-we-measure-information-language-of-coins-10-12)  2)  [Markov chains](https://www.khanacademy.org/computing/computer-science/informationtheory/moderninfotheory/v/markov_chains)  .**
### **Informacijos entropija Paskaitos: 1) [A mathematical theory of communication](https://www.khanacademy.org/computing/computer-science/informationtheory/moderninfotheory/v/a-mathematical-theory-of-communication) 2)   [Information entropy**](https://www.khanacademy.org/computing/computer-science/informationtheory/moderninfotheory/v/information-entropy)**
### **Kompresijos kodai ir klaidų korekcija. Paskaitos: 1) [Compression codes](https://www.khanacademy.org/computing/computer-science/informationtheory/moderninfotheory/v/compressioncodes)[ ](https://www.khanacademy.org/computing/computer-science/informationtheory/moderninfotheory/v/testtest)2) [Error correction**](https://www.khanacademy.org/computing/computer-science/informationtheory/moderninfotheory/v/testtest)**
### **SETI projektas Paskaitos: 1) [The search for extraterrestrial intelligence**](https://www.khanacademy.org/computing/computer-science/informationtheory/moderninfotheory/v/seti)**

## **
## **II Dalis (Skaityti 1-10 skyrius iš knygos)**
1. ### **Binarinis simetrinis kanalas ir klaidų korekcijos kodai (Žiūrėti skaidres: Information theory Lect3 v1  ).**
Binarinis simetrinis kanalas - komunikacijos kanalo modelis. 

BSC leidžia modeliuoti bitų persiuntimą kanalu, kuris turi bitų perdavimo klaidos tikimybę.

P(0|1) = P(1|0) = Pe - probability of error. P(0|1) - tikimybė, kad išsiuntus 0 gaunamas 1.

P(0|0) = P(1|1)  = 1 - Pe, klaidos nėra.

Kanalas gali būti atvaizduotas tokia diagrama (kairėje siuntėjas, dešinėje gavėjas, f- klaidos tikimybė):

Diagrama simbolizuoja teisingo ir neteisingo perdavimo tikimybes.

Bernoulli Trials

Nesvarbu, kur randasi klaidos.


Klaidų taisymo kodas yra kodavimo schema, kuri pranešimus perduoda dvejetainiais skaičiais taip, kad pranešimą galima atkurti, net jei kai kurie bitai yra klaidingai apversti. 

Tam, kad šaltinis išliktų nesugadintas naudojamas *repetition code*.

Hamming code

Bitas, kuris yra blogų apskritimų ribose ir nėra gero apskirtimo riboje, bus neteisingas. Parity bitas - paskutinis bitas, kuris nusako ar vienetų suma yra lyginis skaičius, tada įrašomas 0, jeigu nelyginis - 1.




Hamming kodas - klaidos atsiradimo aptikimo sistema, leidžianti be perdėto duomenų duplikavimo ir vietos švaistymo užtikrinti, jog įvykusi klaida bus rasta.

Pagrindinė idėja - turėti rezervuotą bitą tam tikram bitų blokui, reprezentuojantį 1-etų lygybę. Tarkim bitas reprezentuoja 8 bitų bloką. Jeigu šiame bloke yra 4 1-etai - bitas lieka 0, jei 5 - bitas virsta į nulį, taip užtikrindamas 1-etų lygybę bloke. Taip žinutę paruoštą žinutę gavęs gavėjas gali iškart pastebėti, jog jei įvyko klaida, t.y. Vienetų kiekis padidėjo arba sumažėjo, pasikeitė 1-etų lygybė, kas reiškia, kad bloke įvyko klaida. Tai ir yra gan silpnas problemos sprendimas, nes gali atsirasti daugiau negu viena klaida, tačiau suskirsčius bitus į blokus, galima lokalizuoti klaidą. Bitai skirstomi į puses, tuomet stulpelius, eilutes, lygines eilutes, nelygines eilutes ir t.t. Taip tikrinant failą didelė tikimybė surasti klaidą. Blokų skirstymo pavyzdys, leidžiantis lokalizuoti klaidą:


Pavyzdys didesne skale:

16 blokų - pakankamas skirstymas 256 bitų informacijai norint rasti klaidą. 

Išplėstas Hammingo kodas - Siekiant aptikti situacijas, kai klaidų yra daugiau negu 1 - 0-inis bitas pradėtas naudoti viso bloko 1-etų lygybei aptikti. Taip įvykus 1 ai klaidai - klaidą gali pastebėti 0-inis bitas, bei lokalizuoti bitų grupės, o įvykus 2 -iems klaidoms - klaidą gali pastebėti bitų grupės, atsižvelgdamos į tai kad viso bloko 1-etų lygybė nepakito.

1. ### **Šaltinio kodavimo teorema . (Žiūrėti skaidres: Information\_theory\_Lect4\_v1).**

1. ### **Simbolių kodai . (Žiūrėti skaidres: Information\_theory\_Lect4\_v1).**
Simbolių kodas - žemėlapis iš kiekvieno simbolio x abecelėje į C(x) (binarinis stringas). C(x) e {0,1} Gali būti bet kokio ilgio.

{0, 1}^2 = { 00, 01, 10, 11}

Simbolių kodas veikia užkoduojant rezultatų stringą x1,x2,x3...xn į C(x1), C(x2), C(x3) … C(xn). Pvz.:

Jeigu a - 1, b - 010, c - 1011, tai stringas, turintis kombinaciją cabb -> 10111010010

Hufmano


Nurodomas kelias iki viršūnės (nuo viršunės iki lapų).

Gaunamas prefix kodas: 00 10 11 010 011.
### Optimalaus simbolių kodo radimas - **Huffmano** algoritmas
Veikimas - binarinio medžio sudarymas pradedant nuo tolimiausių lapų.

Tikimybės: 0.4 , 0.14, 0.13, 0.12, 0.11, 0.10

**Algoritmas** - sujungti du simbolius su mažiausiom tikimybėm ir kartoti

Taip dažniausiai pasikartojantis simbolis gauna trumpiausią kodą, taip sutaupant vietos, nes dažniausiai naudojamas trumpesnis simbolis.




1. ### **Aritmetiniai kodai. (Žiūrėti skaidres:  Information\_theory\_Lect5\_v1 ).**
B
1. ### **LZW kompresijos algoritmas (Žiūrėti skaidres:  Information\_theory\_Lect5\_v1 ).**

1. ### **Kanalo su triukšmu teorema. (Žiūrėti skaidres: Information\_theory\_Lect6\_v1 ).**
**	B
**

## **III Dalis (Skaidrės, Wikipedia, YouTube)**
### **Kvantinio kompiuterio veikimas.**
### **Moderni kriptografija.**
### **Bitcoin veikimo sprendimai.**
### **Ląsteliniai automatai.**
### **Fraktalai.**
### **Chaosas.**
**

**Egzamino klausimai**

1. **Informacijos matavimas, Entropija**

Claude Elwood Shannon amerikiečių matematikas, elektros inžinierius, kriptografas, žinomas kaip „informacijos teorijos tėvas”. Jis parašė mokslinį darbą „[A Mathematical Theory of Communication](https://en.wikipedia.org/wiki/A_Mathematical_Theory_of_Communication)” 1948 metais, kuriuo yra paremta informacijos teorijos mokslo šaka. Informacijos teorijoje vienas iš svarbiausių terminų yra entropija. Entropija - tai matas nusakantis informacijos kiekį. Entropija matuojama bitais. Entropija yra žymima raide ‘H’. 

Pagrindinė informacijos teorijos idėja yra ta, kad perduodamo pranešimo „informacinė vertė“ priklauso nuo to, kiek pranešimo turinys stebina. Jei įvykis yra labai tikėtinas, nenuostabu (ir apskritai neįdomu), kai tas įvykis įvyksta taip, kaip tikėtasi; taigi tokios žinios perdavimas suteikia labai mažai naujos informacijos. Tačiau jei įvykis vargu ar įvyks, daug informatyviau sužinoti, kad įvykis įvyko ar įvyks. Pavyzdžiui, žinojimas, kad tam tikras skaičius nebus loterijos laimėtojas, suteikia labai mažai informacijos, nes bet kuris pasirinktas skaičius beveik nelaimės. Tačiau žinios, kad konkretus skaičius laimės loteriją, turi didelę vertę, nes tai praneša apie labai mažos tikimybės įvykio baigtį.

P - simbolio pasirodymo tikimybė.

Informacijos entropija yra informacijos teorijos sąvoka, kuri nurodo, kiek informacijos yra įvykyje. Apskritai, kuo įvykis yra tikresnis ar determiniškesnis, tuo mažiau informacijos jame bus. Aiškiau pasakius, informacija yra netikrumo ar entropijos padidėjimas. Entropiją galima pritaikyti daugelyje sričių, įskaitant duomenų praradimą be nuostolių, statistines išvadas, kriptografiją ir kartais kitose srityse, tokiose kaip biologija, fizika ar mašininis mokymasis. 

Pavyzdys: Jei kam nors pasakoma kažkas, ką jis jau žino, gaunama informacija yra labai maža. Jiems bus beprasmiška pasakyti, ką jie jau žino. Šios informacijos entropija būtų labai maža. Jei jiems būtų pasakyta apie tai, ką jie mažai žino, jie gautų daug naujos informacijos. Ši informacija jiems būtų labai vertinga. Jie kažko išmoktų, todėl informacija turėtų didelę entropiją.

1. **Informacijos suspaudimas**

**Compresor - > Encoder - > NC -> Decoder - > Uncompressor.**

`	`Kompresija - informacijos kiekio mažinimas be jos praradimo. Kitaip sakant, bandymas suspausti ir sumažinti informaciją tokiu būdu, kad teoriškai būtų įmanoma atgauti visą pradinę informaciją. Perduodant suspaustą informaciją tinklu kaina mažės, kadangi mokama už bitą/baitą, o jų kiekis mažinamas. Kompresija neapsimoka tada, kai dekompresavimo kaštai viršija perdavimo kaštus, kadangi dekompresavimas užima tam tikrą laiką.

Kompresavimas veikia ieškant pasikartojimų ir nuspėjamumų informacijoje. Pavyzdžiui, žodinis failas gali turėti tam tikras pasikartojančias konstrukcijas, kaip frazės, junginiai arba sakiniai, todėl jis bus lengvai kompresuojamas, nes turės pasikartojančius elementus. Nuotraukos yra sudėtingesnės, nes jos yra mažiau nuspėjamos. Pavyzdžiui salos vandenyne nuotrauka. Tokia nuotrauka galėtų turėti didelį kiekį pasikartojančių pikselių, kurie gali būti kompresuoti tokiu pat būdu kaip ir žodinis failas. Tačiau nuotraukos, kaip pavyzdžiui automobilių lenktynių, gali būti daug labiau nenuspėjamos ir pasikartojimų gali nebūti.

Huffman coding naudojamas suspaudžiant duomenis. Huffman coding veikia, nes dažniausiai informacija kartojasi (pvz.: paveiksliuke kartojas mėlyna spalva).


Pagal naujus sukurtus kodus sukuriamas jau suspaustas kodas.

Lentelėje pavaizduoti dvejetainiai kodai, kurie gali būti panaudoti apibrėžti kodinius žodžius. Kiekvieno kodinio žodžio kaina 2^-e (e-dvejetainio kodo ilgis), vaizduojama pagal langelio dydį, kuriame jis yra. Maksimalus biudžetas, kuriant unikaliai  dekoduojamą kodą yra 1. Tai reiškia, kad sudėjus kodinių žodžių kainas, suma negali viršyti 1. Unikaliai koduotame kode negali susidaryti sutaicija, kai kodas gali būti skirtingai interpretuojamas.





1. **Informacijos perdavimas per kanalą su triukšmu**

[kanalas su triuksmu](https://www.youtube.com/watch?v=KtCdq9BbJHw)

Kasdieniame gyvenime mes susiduriame su daugeliu komunikacijos kanalų, pavyzdžiui, internetu, kuriuo naudodamiesi atsisiunčiame duomenis ir žiūrime vaizdo įrašus internete ar net tiesiog kalbame su draugu. Paskutiniu atveju, oras galėtų būti bendravimo kanalas balsui. Tačiau, kartais kanalai turi triukšmą, o tai tiesiog reiškia, kad siuntėjas bandė siųsti nebūtinai tiksliai tai, ką imtuvas gauna. Naudojant tikimybes, galima modeliuoti šiuos bendravimo kanalus ir triukšmą.

Binarinis simetrinis kanalas - komunikacijos kanalo modelis. 

BSC leidžia modeliuoti bitų persiuntimą kanalu, kuris turi bitų perdavimo klaidos tikimybę (triukšmą).

P(0|1) = P(1|0) = Pe - probability of error. P(0|1) - tikimybė, kad išsiuntus 0 gaunamas 1.

P(0|0) = P(1|1)  = 1 - Pe, klaidos nėra.

Kanalas gali būti atvaizduotas tokia diagrama (kairėje siuntėjas, dešinėje gavėjas, f- klaidos tikimybė):

Diagrama simbolizuoja teisingo ir neteisingo perdavimo tikimybes.

Bernoulli Trials

Nesvarbu, kur randasi klaidos.



Triukšmas kanaluose gali iškraipyti informaciją, dėl to svarbu leisti dublikatus.

2 būdai kaip sumažinti triukšmo poveikį: *repetition codes, Hamming code.*

Klaidų taisymo kodas yra kodavimo schema, kuri pranešimus perduoda dvejetainiais skaičiais taip, kad pranešimą galima atkurti, net jei kai kurie bitai yra klaidingai apversti. 

Tam, kad šaltinis išliktų nesugadintas naudojamas *repetition code*.

Hamming code

Bitas, kuris yra blogų apskritimų ribose ir nėra gero apskirtimo riboje, bus neteisingas. Parity bitas - paskutinis bitas, kuris nusako ar vienetų suma yra lyginis skaičius, tada įrašomas 0, jeigu nelyginis - 1.




Hamming kodas - klaidos atsiradimo aptikimo sistema, leidžianti be perdėto duomenų duplikavimo ir vietos švaistymo užtikrinti, jog įvykusi klaida bus rasta.

Pagrindinė idėja - turėti rezervuotą bitą tam tikram bitų blokui, reprezentuojantį 1-etų lygybę. Tarkim bitas reprezentuoja 8 bitų bloką. Jeigu šiame bloke yra 4 1-etai - bitas lieka 0, jei 5 - bitas virsta į nulį, taip užtikrindamas 1-etų lygybę bloke. Taip žinutę paruoštą žinutę gavęs gavėjas gali iškart pastebėti, jog jei įvyko klaida, t.y. Vienetų kiekis padidėjo arba sumažėjo, pasikeitė 1-etų lygybė, kas reiškia, kad bloke įvyko klaida. Tai ir yra gan silpnas problemos sprendimas, nes gali atsirasti daugiau negu viena klaida, tačiau suskirsčius bitus į blokus, galima lokalizuoti klaidą. Bitai skirstomi į puses, tuomet stulpelius, eilutes, lygines eilutes, nelygines eilutes ir t.t. Taip tikrinant failą didelė tikimybė surasti klaidą. Blokų skirstymo pavyzdys, leidžiantis lokalizuoti klaidą:


Pavyzdys didesne skale:

16 blokų - pakankamas skirstymas 256 bitų informacijai norint rasti klaidą. 

Išplėstas Hammingo kodas - Siekiant aptikti situacijas, kai klaidų yra daugiau negu 1 - 0-inis bitas pradėtas naudoti viso bloko 1-etų lygybei aptikti. Taip įvykus 1 ai klaidai - klaidą gali pastebėti 0-inis bitas, bei lokalizuoti bitų grupės, o įvykus 2 -iems klaidoms - klaidą gali pastebėti bitų grupės, atsižvelgdamos į tai kad viso bloko 1-etų lygybė nepakito.




**

