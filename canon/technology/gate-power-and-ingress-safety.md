# Energetika a ochrana pozemského uzlu

**Stav:** kánonická provozní obálka Project THRESHOLD pro první sérii; číselné intervaly popisují pozemské rozhraní, ne univerzální fyzikální konstanty sítě  
**Platnost:** pozemský uzel konce 90. let; jiné brány a původní ovladače se mohou chovat odlišně  
**Nadřazená pravidla:** [pracovní technická pravidla brány](../gate-rules.md)

## Co čísla znamenají

THRESHOLD umí měřit energii na vlastních sběrnicích, teplo ve vlastní strojovně a časování vlastního ovladače. Neumí uzavřít energetickou bilanci samotné červí díry. Brána může využívat vnitřní zásobu, místní infrastrukturu nebo fyzikální vazbu, kterou Země neumí měřit.

Proto se rozlišují tři veličiny:

1. **iniciační pulz** dodaný z pozemského pulzního systému;
2. **příkon udržování** měřený po ustavení horizontu;
3. **celková energie jevu**, která zůstává neznámá.

Žádná z prvních dvou veličin nedokazuje třetí. Brána není elektrárna a není dovoleno dopočítat „přebytek“ z neznámé bilance.

## Pracovní energetická obálka

Rozsahy jsou záměrně široké. Představují opakovatelné hodnoty pozemského uzlu po prvních provozních úpravách, nikoli přesnost laboratorní konstanty.

| Režim | Pozemská hodnota | Co zahrnuje |
|---|---:|---|
| příprava a nabíjení | 5–20 MW po dobu zhruba 5–20 minut | roztočení zásobníků, nabití pulzních stupňů, chlazení a diagnostiku |
| iniciační pulz | přibližně 0,4–1,0 GW po 3–5 sekund | na sběrnici řádově 1,5–4 GJ |
| ustálené spojení | celkem přibližně 3–7 MW | stabilizaci, výkonovou elektroniku, čerpadla, řízení a chlazení |
| desetiminutové okno | řádově 3–8 GJ (0,8–2,2 MWh) | pulz plus deset minut udržování |
| plných 38 minut | řádově 8–20 GJ (2–6 MWh) | pulz plus 2 280 sekund udržování |

Řádová kontrola pro horní délku spojení:

```text
E = E_pulz + P_udržování × t
E ≈ (1,5 až 4) GJ + (3 až 7) MW × 2 280 s
E ≈ 8 až 20 GJ
```

Hodnota „několik gigajoulů na otevření“ tedy může označovat iniciační pulz, ne celou osmatřicetiminutovou relaci. Zaměnit tyto dvě věci by porušilo rozměrovou správnost.

Skutečné hodnoty kolísají s cílovou adresou, tepelným stavem, přesností mechanického nastavení a tím, kolik bezpečnostních oprav musí pozemský ovladač provést. Pozemský tým zatím neumí spolehlivě určit, která část změny patří trase a která chybě ovladače.

## Pozemská napájecí soustava

THRESHOLD nepřipojuje iniciační pulz přímo na běžnou distribuční síť. Referenční uspořádání obsahuje:

- několik motor-generátorových setrvačníkových soustrojí s využitelnou zásobou dohromady řádově 4–6 GJ;
- pulzní transformátory, usměrňovače a spínací stupně;
- menší kondenzátorové banky pro tvarování hran pulzu, nikoli pro uložení všech gigajoulů;
- samostatné sběrnice, rychlé odpojovače a obětované vybíjecí odpory;
- průmyslové chlazení, akumulační nádrže a nouzové napájení řízení;
- galvanicky a opticky oddělenou instrumentaci.

Toto je rozsáhlá pevná infrastruktura. V 90. letech však není mimo známé strojírenství: dvě motor-generátorová soustrojí TFTR měla po 2,25 GJ a společně mohla dodat 4,5 GJ během pulzu. Tato analogie dokládá měřítko pozemského pulzního zařízení, nikoli funkci brány.

Elektrická energie jedné relace sama o sobě není hlavní finanční položkou programu. Rozpočet zatěžují utajená stavba, výkonové soustrojí, údržba, náhradní díly, chlazení, karanténa, pohotovost a personál. Zpravodajsky nápadná není běžná měsíční spotřeba, ale kombinace vysokého pulzního výkonu, velkých rotujících strojů, chlazení, specializovaných dodavatelů a nepravidelného provozu.

## Tepelná a provozní omezení

Ne všechna energie odebraná ze sběrnice se mění v teplo v hale; část mizí v dosud neuzavřené bilanci brány. Pozemské ztráty jsou přesto dost velké, aby určovaly rozvrh:

- po běžném krátkém spojení následuje nejméně desítky minut diagnostiky a dochlazení;
- po relaci blízké 38 minutám se počítá s řádem hodin do návratu plné provozní rezervy;
- nouzové druhé otevření před dokončením kontrol může být technicky možné, ale spotřebuje redundanci a vyžaduje výslovné přijetí rizika;
- několik bezpečných aktivací týdně je na začátku série realistický plán, ne svévolně nízká kvóta;
- limit přibližně 38 minut není jen účet za elektřinu. Jde o hranici stability spojení; větší pozemský generátor ji automaticky neprodlouží.

To zachovává význam slotů v S01E06 a brání tomu, aby každá záchranná mise dostala okamžitý druhý pokus bez ceny.

## Polní ovladač a energie vzdáleného uzlu

Přenosný ovládací prstenec o hmotnosti 2,5–3 tuny nenese gigajoulový zdroj pro bránu. Jeho akumulátory napájejí pohony, snímače, řídicí elektroniku a krátkodobou diagnostiku.

Úspěšné vytáčení z A-001 nebo A-005 znamená pouze, že polní souprava dokázala vyvolat a časovat energetickou vazbu dostupnou v daném kruhu nebo jeho místním uložení. Neznamená to, že:

- totéž dokáže na vyčerpaném, poškozeném nebo odpojeném uzlu;
- lze místní zdroj vyjmout nebo napodobit;
- baterie soupravy dodaly energii fyzikálního jevu;
- jeden úspěch stanoví energetická pravidla celé sítě.

Před každou lidskou výpravou proto bezpilotní diagnostika hledá známky dostupné místní energie. Neprůkazný výsledek je důvodem misi odložit, protože návrat nelze garantovat.

## Poruchové stavy

### Před ustavením horizontu

- **nedostatečná energie nebo chybný tvar pulzu:** spojení se nevytvoří; energie se odvede do dumpu a zařízení se kontroluje;
- **nesouhlas polohy a proudu:** ovladač přeruší sekvenci, i když by mechanika dokázala pokračovat;
- **oblouk nebo porucha izolace:** vysoké riziko pro strojovnu, ale nikoli automaticky síťová katastrofa;
- **překročení otáček, vibrací nebo teploty:** blokuje další pokus do fyzické kontroly.

### Po ustavení horizontu

- **ztráta chlazení nebo napájecí fáze:** nejprve se odpojí nepodstatné zátěže, poté se žádá řízené ukončení;
- **nestabilní fáze nebo rostoucí odražený výkon:** vyvolá přerušení komunikace a evakuaci přímé osy;
- **výpadek pozemského řízení:** nouzové obvody se pokusí spojení ukončit, ale bezpečnostní plán nesmí předpokládat, že přijímající strana vždy dokáže cizí příchozí spojení okamžitě shodit;
- **objekt v transportním bufferu:** postup zůstává neznámý. Není dovoleno tvrdit, že vypnutí bezpečně rekonstruuje, vrátí nebo uloží člověka.

Po tvrdém přerušení se brána nepovažuje za provozuschopnou jen proto, že vypadá nepoškozeně. Následuje kontrola izolace, geometrie, ložisek, časové základny a zbytkového záření.

## Ochrana příchozího spojení

Mechanická rekonstrukční bariéra chrání proti makroskopické hmotě, ne proti rádiu, světlu ani automaticky proti ionizujícímu záření. Pozemský uzel proto používá více vrstev.

### 1. Geometrie a odstup

- Před horizontem není při neověřeném příchozím spojení personál.
- Přímá optická osa končí v obětované cloně a doglegu; lidé i hlavní přístroje jsou mimo ni.
- Bránová hala a řídicí místnost jsou oddělené tlakem, konstrukcí a samostatnými únikovými cestami.

### 2. Hmota a biologie

- Rekonstrukční bariéra zůstává zavřená, dokud není autentizace, karanténa a přijetí nákladu schváleno.
- Bariéra je snímaná, chlazená a má obětovanou zadní vrstvu; není nezničitelná.
- Potlačení pasivního proudění a zavřená bariéra snižují biologické riziko, ale nedokazují sterilitu. Chování aerosolů, jednotlivých částic a aktivně tlačených kapalin zůstává předmětem zkoušek.

### 3. Rádio a mikrovlny

- Hala má vodivou vložku se svařovanými spoji, filtrované průchodky a ventilaci vedenou prvky typu waveguide-below-cutoff.
- Veškeré kabelové signály procházejí omezovači a tam, kde je to možné, převodem na optické vlákno bez vodivého propojení.
- Štěrbiny, dveře a prostupy jsou slabší místo než samotný kov; každá stavební změna vyžaduje nové měření stínění.
- Ochrana je dimenzována proti charakterizovaným pásmům a výkonům, ne proti libovolnému mimozemskému zdroji.

### 4. Optické a ionizující záření

- Přímou osu uzavírají rychlé obětované clony, difuzní terč a senzory, které lze ztratit bez otevření cesty do řídicí místnosti.
- Beton, voda a podle potřeby vrstvy materiálu s vysokou hustotou poskytují omezenou ochranu proti fotonům; vodíkaté materiály a beton pomáhají s neutrony.
- Návrh konzervativně nepředpokládá, že mikroskopické částice nebo neutrony jsou pravidlem jednosměrné makroskopické hmoty bezpečně vyloučeny.
- Bez znalosti spektra a toku neexistuje univerzální tloušťka stínění. Velmi silný laser, gama záblesk nebo neutronový tok může ochranu překonat, aktivovat materiály nebo učinit halu dlouhodobě nepřístupnou.

## Omezený přijímací režim pro S01E21

Finále první série používá pouze schopnost, kterou lze postavit z dobové pozemské techniky:

1. hala je vyklizena a mechanická bariéra zůstane zavřená;
2. nejprve měří pasivní detektory za pevnými útlumy; hlavní přijímače jsou fyzicky odpojené;
3. po zjištění slabého stabilního nosného signálu se otevře jeden úzký přijímací kanál přes omezovač, útlum a optické oddělení;
4. provozní datová rychlost je řádově jednotky až desítky kilobitů za sekundu; nejde o fyzikální kapacitu brány;
5. čas i absorbovaný výkon mají předem stanovené meze a překročení vyvolá pokus o ukončení, uzavření clony a přechod všech systémů do obětovaného režimu;
6. volající spojení nakonec ukončí sám.

Tento režim umí přijmout krátký kontrolní součet a omezený datový blok. Neumí bezpečně analyzovat libovolné pásmo, zaručit příkon odesílatele, zastavit neznámý kód ani chránit proti útoku mimo charakterizovanou obálku. Finále proto neuděluje Zemi univerzální obranu.

## Jednosměrný průzkum A-001 v S02

Obětovaná sonda používá pozemsky vytáčenou relaci kratší než provozní maximum, vlastní baterii a zpětný elektromagnetický kanál. Nenese energii pro bránu, kabel přes horizont ani návratový ovladač. Její hmotnost, datový profil, časový rozpočet, poruchové stavy a neadresní nonce stanoví [samostatný protokol](a-001-probe-and-challenge-protocol.md). Jeho cílové ukončení do 34. minuty ponechává rezervu před přibližnou mezí 38 minut; nejde o novou fyzikální schopnost.

## Zneužití a zakázané zkratky

| Zkratka | Proč nefunguje |
|---|---|
| těžba energie z otevřené brány | fyzikální bilance není uzavřená, pasivní tok je potlačen a stabilizační proces není bezpečný elektrický výstup |
| kabel nebo hadice mezi světy | fyzicky souvislý objekt se rekonstruuje až po úplném vstupu |
| okamžitý vodní či plynový potrubní obchod | pasivní proudění je potlačeno; chování aktivně čerpané kapaliny není vyřešeno a nesmí se předpokládat |
| přenosný „bránový akumulátor“ | polní souprava dodává řízení a mechanickou práci, nikoli gigajouly jevu |
| energetická zbraň skrz bránu jako jistota | nízkovýkonová komunikace je doložena, přenos vysokých výkonů a ionizujícího spektra není charakterizován |
| neprůstřelná iris | bariéra řeší hmotu, nikoli celé elektromagnetické spektrum, teplo, sekundární záření nebo neznámé mezní režimy |
| prodloužení nad 38 minut větší elektrárnou | provozní maximum je hranice stability spojení, ne jen energetický tarif |
| bezpečné okamžité znovuotevření | nabití může být rychlejší než dochlazení, mechanická kontrola a obnova redundance |
| snadné cestování časem | časové odchylky jsou poruchový stav; žádná energetická procedura z nich nedělá navigační funkci |

Příchozí spojení navíc může obsadit jediný uzel a rušit diplomatické či záchranné sloty. Dokud není prokázáno spolehlivé lokální odmítnutí hovoru, opakované cizí vytáčení se posuzuje jako forma odepření služby.

## Výrobní a materiálové důsledky

Země umí vyrobit napájecí a bezpečnostní obal: ocelové a měděné sběrnice, rotující stroje, výkonovou elektroniku, betonové stínění, senzory, clony a software. Neumí vyrobit transportní kruh, jeho aktivní materiál ani komponenty, které uzavírají červí díru.

Každá pozemská oprava je proto rozdělena na:

- **vyměnitelný lidský díl** — kabel, pohon, snímač, relé, chladič;
- **rozhraní** — připojení, jehož funkci tým empiricky charakterizoval;
- **neopravitelné jádro** — část brány, do níž se bez nové znalosti nezasahuje.

Úspěšná výměna lidského stykače není krokem „reprodukováno“ pro bránu. Je pouze údržbou pozemského obalu.

## Otevřené fyzikální otázky

Záměrně nejsou rozhodnuty:

- skutečná celková energie a zdroj fyzikálního jevu;
- proč se příkon liší mezi adresami;
- přesný spektrální a výkonový přenos elektromagnetického záření;
- chování laseru, gama záření, neutronů, plazmatu a jednotlivých částic na horizontu;
- aktivně tlačené kapaliny a aerosoly;
- buffer a rekonstrukce při přerušení;
- zda přijímací uzel může každé příchozí spojení lokálně odmítnout nebo ukončit;
- přesná vazba času, gravitace a limitu přibližně 38 minut.

První epizoda, která některou otázku použije jako řešení nebo zbraň, musí předem provést audit zpětných důsledků.

## Kritická revize rozhodnutí

### Celková energie pouze 1–3 GJ

Odmítnuto jako popis dlouhé relace. Několik megawattů po 38 minutách samo dává několik až desítky gigajoulů. Rozsah jednotek gigajoulů zůstává použitelný pro iniciační pulz.

### Přímý gigawattový odběr ze sítě

Odmítnuto. Zbytečně by zatěžoval veřejnou síť a ignoroval dobově existující pulzní motor-generátory. Energie se akumuluje pomaleji a uvolní lokálně.

### Úplnou energii dodává Země

Neuzamčeno. Měřený pozemský příkon je skutečný, ale neuzavírá bilanci kruhu a červí díry. Toto rozlišení zachovává tajemství i zákaz volné energie.

### Univerzální elektromagnetická ochrana

Odmítnuta. Faradayova klec je užitečná proti charakterizovanému rádiu a mikrovlnám; mechanická bariéra řeší hmotu; objemové stínění pouze omezuje známé ionizující záření. Kombinace snižuje riziko, neodstraňuje je.

### Polní souprava s vlastním gigajoulovým zdrojem

Odmítnuta kvůli hmotnosti, výrobě i dramatickým důsledkům. Souprava pouze ovládá uzel s dostupnou místní energetickou vazbou, takže návrat zůstává nejistý a závislý na charakterizaci cíle.

## Reálné opory měřítka

- Dvojice motor-generátorů TFTR byla popsána jako dva sety po 475 MVA a 2,25 GJ, společně 4,5 GJ pro několikasekundový pulz: [U.S. Department of Energy, OSTI — TFTR Motor Generator](https://www.osti.gov/biblio/5223268) a [Tokamak Physics Experiment Power Supply Design](https://www.osti.gov/servlets/purl/46714).
- NASA ve svém dobovém handbooku pro elektromagnetickou kompatibilitu upozorňuje, že rozhodující jsou spáry a prostupy, a popisuje ventilaci typu waveguide below cutoff: [NASA Technical Reports Server — MEDIC Handbook](https://ntrs.nasa.gov/citations/19960003032).
- Bezpečnostní materiály IAEA popisují beton a vodu jako objemové materiály pro neutronové stínění a zdůrazňují nutnost výpočtu podle zdroje, vzdálenosti a požadované dávky: [IAEA Safety Standards](https://www-pub.iaea.org/MTCD/Publications/PDF/P1879_web.pdf).

Tyto zdroje dokládají proveditelnost pozemského obalu a omezení stínění. Nedokládají existenci ani fyziku hvězdné brány.
