# Registr auditu kontinuity

**Poslední úplný audit:** 3. října 2026  
**Auditovaný stav před opravami:** hlavní větev na commitu ec53572dcad5a125222d99d23dfe5cf9c0a547c5  
**Účel:** evidovat skutečné rozpory, minimální opravy, záměrná tajemství a dosud neurčené údaje bez tichých retconů

## Rozsah auditu

Porovnány byly:

- základní premisa a technická pravidla brány,
- registr důkazů o Konstruktérech,
- Veyra a Náar,
- Taal a Oru,
- Project THRESHOLD a první diplomacie,
- tvůrčí omezení, otevřené otázky a formát seriálu,
- Ilyr a jeho planetární i družicové parametry,
- historickou civilizaci Leth a míru nezávislosti jejích pramenů,
- režim původu, úschovy a technologického transferu,
- úplnou pracovní páteř a kontrolní matici S01,
- poslední související změny hlavní větve.

V auditovaném stavu repozitář neobsahoval podrobné osnovy jednotlivých epizod, časovou osu scén ani profily hlavních lidských postav. Pozdější příspěvky doplnily pilot S01E01, základ hlavního pozemského ansámblu a pracovní příčinnou páteř všech 21 dílů. Revize 2. října doplnila dramatické volby a pracovní kontrolní matici času, dopravy a znalostí. Samostatné osnovy epizod 2–21 a scénové časové osy však stále chybějí. Jde o částečně zaplněnou mezeru, ne o uzavřený audit celé série.

## Klasifikace nálezů

- **Rozpor:** dvě kánonická tvrzení nemohou současně platit bez dalšího rozlišení.
- **Mezera s důsledkem:** pravidlo chybí, ale existující scény nebo světy už jeho výsledek předpokládají.
- **Záměrné tajemství:** neúplnost je součástí dlouhodobého příběhu a nemá se nyní řešit.
- **Otevřený údaj:** hodnota ještě není potřebná nebo ji nelze bezpečně uzamknout.
- **Ověřeno:** kontrola nenašla rozpor a změna není nutná.

## Podstatné nálezy

| ID | Typ a závažnost | Dotčené podklady | Nález | Nejméně rušivá oprava | Stav |
|---|---|---|---|---|---|
| K-01 | Rozpor — kritický | canon/gate-rules.md; canon/mysteries/constructors.md | Technická pravidla tvrdila, že síť vytvořila jedna „nyní zmizelá rasa“, zatímco registr zakazuje potvrdit jediný druh, společnou epochu i vyhynutí. | Nahradit tvrzení souhrnným pojmem Konstruktéři a výslovně ponechat počet, biologii i osud neznámé. | Opraveno |
| K-02 | Rozpor — vysoký | canon/gate-rules.md; první kontakt v canon/species/taal.md | „Jednosměrná červí díra“ bez rozlišení by znemožnila, aby Taal odpověděli rádiem přes spojení vytočené Zemí. | Jednosměrnost vztáhnout na makroskopickou hmotu; komunikační elektromagnetické signály povolit oběma směry. | Opraveno |
| K-03 | Mezera — vysoká | Veyra 1,04 baru; Náar 1,68 baru; Ilyr 1,32 baru | Profily předpokládají bezpečné otevření mezi různými atmosférami, ale centrální pravidla nevysvětlovala, proč se tlaky okamžitě nevyrovnají. | Stanovit, že aktivní horizont není volný otvor a potlačuje pasivní tlakový i hydrostatický tok. | Opraveno |
| K-04 | Mezera — vysoká | canon/species/oru.md; obecná pravidla | Pravidlo úplného vstupu fyzicky souvislého objektu bylo uvedeno jen u Oru. Bez zobecnění by kabely, hadice a částečný průchod obcházely logistická omezení. | Přesunout obecné pravidlo celého objektu do canon/gate-rules.md; u Oru ponechat biologický důsledek. | Opraveno |
| K-05 | Mezera — vysoká | canon/species/taal.md; Project THRESHOLD | Taal nedostanou čitelnou adresu Země, zatímco diplomatický protokol používá návratový token. Centrální pravidla neoddělovala token od skutečné adresy. | Zapsat, že příchozí spojení adresu neodhalí a původní ovladač může nabídnout pouze dočasný návrat posledního spojení. | Opraveno |
| K-06 | Mezera — střední | Project THRESHOLD; všechna spojení | Politický dokument správně zachází s časem brány jako s nedostatkovým zdrojem, ale základní pravidla neříkala, že uzel může vést jen jedno spojení. | Uzamknout jedno současné spojení na jednu bránu a stejnou cenu komunikačního i transportního slotu. | Opraveno |
| K-07 | Ověřeno | Veyra; Náar; Ilyr | Hmotnost, poloměr, gravitace, hvězdný příkon a oběžné doby jsou vzájemně konzistentní v deklarované přesnosti. | Bez změny. | Ověřeno |
| K-08 | Ověřeno | Project THRESHOLD | Rozpočet 1,2–2,5 mld. USD odpovídá přibližně 0,48–0,99 % základny 251,6 mld. USD; zaokrouhlení na 0,5–1,0 % je správné. Personální odhad není v rozporu s rozpočtovými kategoriemi. | Bez změny. | Ověřeno |
| K-09 | Možná nechtěná vazba — střední | Veyra; Oru | Veyra má poslední známou aktivaci přibližně před šesti stoletími a Oru začali svou bránu systematicky používat rovněž asi před šesti stoletími. Čtenář může očekávat společnou příčinu. | Zatím neměnit. Buď vazbu později vědomě využít, nebo při přesnější chronologii hodnoty od sebe oddělit. | Otevřeno |
| K-10 | Záměrné tajemství | registr Konstruktérů; Taal | Odstraněná oblast Země, bezpečnostní odmítnutí adres a vrstvy ovladačů mají několik slučitelných vysvětlení. | Nevybírat vysvětlení v raných sériích; evidovat zdroj a míru jistoty každé nové stopy. | Chráněno |
| K-11 | Mezera s důsledkem — vysoká | canon/gate-rules.md; canon/technology/gate-power-and-ingress-safety.md; S01E06; S01E21 | Energetika a příchozí ochrana byly příliš neurčité pro poruchu chlazení a finále. První hrubá hodnota několika GJ by navíc byla rozměrově chybná pro celých 38 minut při megawattovém udržování. | Uzamknout pouze měřenou pozemskou obálku a omezený přijímací režim; skutečnou energii jevu, vysokoenergetické spektrum, kapaliny a buffer ponechat otevřené. | Částečně opraveno |
| K-12 | Mezera projektu — vysoká | production/series-format.md; production/season-01-story-arc.md | Příčinná mapa 21 dílů už sleduje schopnosti, ceny, návraty a postavy, ale epizody 2–21 nemají samostatné osnovy ani scénové časování. | Při rozpracování každého dílu zachovat sezónní příčinu a provést plný epizodní audit. | Pracovně řešeno |
| K-13 | Otevřený údaj — střední | Veyra; Taal; Project THRESHOLD; production/season-01-story-arc.md | Pracovní páteř stanoví první omezenou veyrskou komunikaci v S01E03, začátek Taal v S01E07 a vývoj slovníku přes S01E08–S01E10. Přesná délka jednotlivých relací čeká na osnovy. | Nezkracovat překlad na jedinou scénu a při teleplayích zachovat týdny mezi komunikačními okny. | Pracovně řešeno |
| K-14 | Ověřeno | Taal; Oru; Veyra; Project THRESHOLD | Současné civilizace nemají FTL lodě ani výrobu bran; taalský ovladač, oruská biotechnologie a pozemská pomoc Veyře mají výslovné výrobní, právní a ekologické brzdy. | Mantinely zachovat při každé nové technologii. | Ověřeno |
| K-15 | Rozpor — kritický | dřívější verze production/s01e01-pres-prah.md; canon/gate-rules.md | Pilot nechal tým projít ze Země na Veyru a vrátit se během téhož spojení, přestože makroskopická hmota může jít pouze od vytáčející k přijímající bráně. | Zachovat objev Veyry, ale rozdělit cestu na spojení Země → A-005 a nové spojení A-005 → Země; návrat vyžaduje těžký polní ovladač a výslovně předanou návratovou sekvenci. | Opraveno |
| K-16 | Záměrné tajemství — vysoké budoucí riziko | A-001; production/season-01-story-arc.md; adresa Země | Finále používá kontrolní součet chybějícího modulu A-001. Bez omezení by mohl být zaměněn za důkaz, že modul někdo ukradl, že jde o Konstruktéry nebo že modul byl jediným zdrojem adresy. | Potvrdit pouze přístup volajícího k datům modulu a znalost adresy; identitu, motiv i úplný řetězec získání ponechat otevřené. | Chráněno |
| K-17 | Potenciální rozpor — kritický | A-001; pilot; energetická obálka | Polní prstenec o 2,5–3 t by nemohl z běžných akumulátorů dodat gigajoulový iniciační pulz. Bez rozlišení by návrat pilotní výpravy popřel novou energetiku. | Potvrdit, že souprava napájí jen mechaniku, senzory a řízení a na vzdáleném uzlu spouští dostupnou místní energetickou vazbu. Bez ní návrat nefunguje. | Opraveno |
| K-18 | Mezera s důsledkem — vysoká | S01E21; canon/gate-rules.md; energetická obálka | Zavřená mechanická bariéra sama nezastaví obousměrné elektromagnetické signály. „Stíněný režim“ bez vrstev by byl nezasloužená univerzální obrana. | Vyklidit přímou osu, oddělit hmotovou bariéru od RF, optického a ionizujícího stínění a otevřít jen omezený úzkopásmový kanál. Extrémní zdroje mohou ochranu překonat. | Opraveno |

## Číselná kontrola světů

Použity byly pouze vztahy odpovídající přesnosti vstupů.

### Veyra

- gravitace: 0,94 / 0,98² = 0,979 g, uvedeno 0,98 g;
- hvězdný příkon: 0,46 / 0,70² = 0,939 násobku Země, uvedeno 94 %;
- Keplerova doba: 365,256 × √(0,70³ / 0,82) = 236,2 dne, uvedeno 236 dní.

### Náar

- gravitace: 2,0 / 1,22² = 1,344 g, uvedeno 1,34 g;
- hvězdný příkon: 0,46 / 0,74² = 0,840 násobku Země, uvedeno 84 %;
- Keplerova doba: 365,256 × √(0,74³ / 0,84) = 253,7 dne, uvedeno 254 dní;
- kruhová orbitální rychlost u povrchu je řádově 1,28násobek pozemské, což podporuje uvedenou vysokou cenu kosmických startů bez tvrzení, že jsou nemožné.

Zaokrouhlení jsou přiměřená a nepředstírají přesnost plného klimatického nebo geofyzikálního modelu.

### Ilyr

- gravitace: 0,62 / 0,93² = 0,717 g, uvedeno 0,72 g;
- hustota: 5,51 × 0,62 / 0,93³ = 4,25 g/cm³, uvedeno 4,25 g/cm³;
- hvězdný příkon: 0,30 / 0,56² = 0,957 násobku Země, uvedeno 0,96;
- Keplerova doba: 365,256 × √(0,56³ / 0,74) = 177,9 dne, uvedeno 178 dní;
- úniková rychlost: 11,19 × √(0,62 / 0,93) = 9,14 km/s, uvedeno 9,1 km/s;
- slapové buzení Vary proti Měsíci: (0,008 / 0,0123) × (384 400 / 230 000)³ = 3,04, uvedeno přibližně trojnásobné;
- družicová perioda: 27,32 × √[(230 000 / 384 400)³ / 0,62] = 16,1 dne, uvedeno přibližně 16 dní;
- Hillův poloměr vychází přibližně 790 000 km a dráha Vary na 230 000 km leží na 0,29 této hodnoty. To je pod řádovou mezí prográdní stability v numerických modelech Domingos, Winter a Yokoyama (2006); nejde o úplnou integraci slapového vývoje soustavy.

Hodnoty jsou vnitřně konzistentní. Původ Vary a miliardy let její slapové migrace zůstávají otevřeným údajem, nikoli vyřešenou fyzikou.

## Kontrola dlouhodobých důsledků

### Jediný uzel jako úzké místo

Pravidelné spojení s Taal, obchod s Veyrou, průzkum i záchranná mise soutěží o stejný pozemský uzel. Project THRESHOLD tento důsledek správně převádí do politického přidělování slotů. Budoucí scénáře nesmějí plánovat dvě paralelní pozemská spojení, dokud Země nezíská druhou funkční bránu.

### Adresa Země

Příchozí spojení neprozradí trvalou adresu. Krátkodobý návratový token umožní bezprostřední odpověď, ale ne pozdější samostatné zavolání. Každý protivník nebo partner, který po delší době vytočí Zemi, proto musí mít doložitelný zdroj adresy. Toto pravidlo chrání význam budoucího nečekaného příchozího spojení.

### Atmosféry a karanténa

Potlačení pasivního proudění zabraňuje okamžitému fyzikálnímu kolapsu při spojení s Náarem nebo světem Oru. Nezabraňuje však přenosu patogenů na osobách, předmětech a vzorcích. Technické pravidlo proto neruší biologickou karanténu.

### Technologický transfer

Taalské zařízení může být používáno bez pochopení a oruské živé materiály mimo vlastní mikrobiom degradují. Ani jedna civilizace neposkytuje Zemi reprodukovatelný technologický skok. U každého budoucího zařízení se musí znovu kontrolovat stupně nalezeno, aktivováno, charakterizováno, pochopeno a reprodukováno.

[Režim původu, úschovy a transferu](../canon/politics/extraterrestrial-knowledge-custody-1997-2000.md) nově přidává oddělené kontroly držby, výzkumu, rozmnožení, nasazení a dalšího předání. Bezpečnostní třída a právní či osobnostní status jsou dvě nezávislé osy; bezpečný nález proto nemusí být legitimně použitelný a dobrovolně poskytnutá technologie nemusí být bezpečná.

### Politická kontinuita

Americká kontrola uzlu není mandát za lidstvo. Stejný problém se zrcadlí na Veyře, kde Svaz devíti toků nevládne celé planetě. Taal a Oru mají důvody odmítnout exkluzivitu i neomezené utajení. Tato symetrie je konzistentní a poskytuje dlouhodobý konflikt bez jednoduché záporné frakce.

## Pravidlo pro budoucí epizodní audit

Každá dokončená osnova epizody má uvést:

| Kontrolní pole | Povinná otázka |
|---|---|
| Nová schopnost | Co po epizodě postavy nebo instituce umějí, co dříve neuměly? |
| Cena | Jaké zdroje, čas, zdraví, důvěru nebo politický kapitál řešení spotřebovalo? |
| Přenositelnost | Lze řešení zopakovat jinde, a pokud ne, proč? |
| Zpětný dopad | Který starší problém by tato schopnost mohla vyřešit? |
| Budoucí návrat | Ve které pozdější epizodě se důsledek znovu projeví? |
| Držitel znalosti | Kdo výsledek zná a kdo k němu nemá přístup? |
| Postavy | Jak se změnila odbornost, vztah, trauma, kariéra nebo názor? |
| Kánon | Které soubory musejí být po epizodě aktualizovány? |

Schopnost, která nemá cenu, omezení nebo držitele znalosti, je výchozí podezření na technologickou zkratku.

## Opravy provedené při tomto auditu

- Přepsána základní pravidla původu sítě tak, aby neprozrazovala počet ani osud Konstruktérů.
- Oddělen jednosměrný transport makroskopické hmoty od obousměrné komunikace.
- Uzamčeno potlačení pasivního vyrovnávání atmosfér a kapalin.
- Zobecněno pravidlo úplného vstupu fyzicky souvislého objektu.
- Sjednoceno pravidlo skryté zdrojové adresy a dočasného návratového tokenu.
- Zapsáno omezení jednoho současného spojení a jeho logistický důsledek.
- Výslovně ponechány otevřené energetické, vysokoenergetické a poruchové režimy, které zatím nemají dost podkladů.
- Opraven návrat pilotní výpravy tak, aby použil dvě opačně vytáčená spojení; přenosný ovladač dostal hmotnostní, energetické, kompatibilitní a bezpečnostní limity.


## Doplňkový technický audit — 2. října 2026

Audit energetiky a příchozí ochrany rozlišil iniciační pulz, udržovací příkon a neznámou celkovou energii jevu. Pro plnou relaci platí řádová kontrola `(1,5–4) GJ + (3–7) MW × 2 280 s = přibližně 8–20 GJ`. Tím byl odstraněn rozměrový omyl, aniž by byla odhalena fyzika brány.

Srovnání s motor-generátory TFTR (dva sety po 2,25 GJ) ověřilo, že gigajoulová pulzní infrastruktura byla dobově dosažitelná, ale vyžadovala velkou pevnou strojovnu. To současně vylučuje gigajoulový zdroj v polním prstenci.

Revize S01E21 potvrdila, že mechanická bariéra řeší makroskopickou hmotu, nikoli celé elektromagnetické spektrum. Finále proto smí použít pouze pasivní měření, útlum, úzkopásmový přijímač, optické oddělení, vyklizenou přímou osu a omezený čas. Vysokoenergetické záření, neutrony, aktivně tlačené kapaliny a bezpečné lokální ukončení cizího příchozího spojení zůstávají otevřené.

## Doplňkový produkční audit — 2. října 2026

**Výchozí revize:** `7bdeda9ca64efe9eeabcaddb12fcf439d544c575`. Porovnány pilot, páteř S01, ansámbl, pravidla brány, energetika, A-001, Veyra, Taal, Náar, politická bible a registr Konstruktérů. Nejde o opakovaný výpočet planetárních parametrů ani novou validaci reálných právních či zdravotních tvrzení. Kontrola sleduje soulad produkčního návrhu s těmito podklady.

| ID | Typ | Nález | Oprava a ověřovací podklad | Stav |
|---|---|---|---|---|
| K-19 | Mezera s důsledkem — vysoká | E04 zjistí ztrátu modulu, ale soustavná ochrana byla výslovně popsána až v E19. To by nutilo odborníky ignorovat potenciální kompromitaci. | E04 ihned odvolá staré kódy, předpokládá možný únik adresy a prověří kopie; E19 rozšíří známý rozsah na diagnostické a servisní paměti. Porovnáno s pravidly adresování a charakterem Kimové/Vanceové. | Opraveno v pracovní páteři |
| K-20 | Mezera s důsledkem — vysoká | E06 a nouzové kanály mohly implikovat samostatné volání Veyry, která nemá ovladač. | Oprava a finální oznámení musejí čekat na pozemsky iniciované bezpečné okno; místní právo uzavřít přístup není schopnost vypnout horizont. Porovnáno s profilem Veyry. | Opraveno v pracovní páteři |
| K-21 | Neoprávněný závěr — vysoký | Pilot formuloval Homo sapiens jako potvrzený výsledek, přestože tým nesbírá genetický vzorek místního člověka. | Oddělen autorský fakt od znalosti postav; souhlas k vzorkům se připraví mezi E05–E08, analýza se potvrdí v E11, výsledek se sdělí partnerům. Pomoc není podmíněna vzorky. Porovnáno s veyrským genetickým a kontaktním profilem. | Opraveno v pilotu a pracovní páteři |
| K-22 | Rozpor v míře jistoty — vysoký | E14 tvrdila vazbu odstraněné oblasti na Zemi silněji než registr Konstruktérů K-05, kde je totožnost výslovně nezjištěná. | E14 dokládá existenci historického tvrzení; úmysl, vztah přesně k Zemi a spolehlivost řetězce zůstávají rozlišené. Stejně opraven rozpočet odhalení. | Opraveno v pracovní páteři |
| K-23 | Mezera s důsledkem — vysoká | Návštěva Taal měla token pro příjezd, ale nepopsaný návrat a obnovu pozemské rezervy. | Matice vyžaduje přípravu Země → Náar, nové Náar → Země tokenem a pozdější Země → Náar. Platnost tokenu se ověří; při selhání návratu musí existovat schválený záložní pobyt. | Pořadí řešeno; přesné časy otevřené |
| K-24 | Mezera evidence — střední | Souprava z teaseru a vozík ponechaný v E12 se mohly stát týmž neodlišeným vybavením. | E04 vrátí dohledané části původní soupravy; E12 používá novější zkušební soupravu. E19 porovnává staré pozemské kopie, nemusí magicky vyzvednout ani jednu ztrátu. | Opraveno v pracovní páteři a matici |
| K-25 | Mezera důkazu — vysoká | Starý kontrolní součet mohl působit jako aktuální autentizace nebo důkaz identity. | E21 pouze porovná starou stopu a úsek diagnostického záznamu; bariéra zůstane zavřená. Shoda neprokáže držení modulu ani jediný zdroj adresy. Přijatá data se neprovádějí jako kód. | Opraveno v pracovní páteři; konkrétní blok otevřený |
| K-26 | Mezera příčiny — vysoká | Původ kandidátní adresy Náaru byl pouze označen za nepřímý. | V matici je pracovní návrh starší katalogové položky a výslovný blokér osnovy E07: určit primární nosič podle historie nálezu brány. Opakovaný přepis není nezávislé potvrzení. | Otevřeno s konkrétním dalším úkolem |
| K-27 | Dramaturgické riziko — střední | Šest odborností se mohlo opakovaně rozdělit na ty, kdo chtějí jednat, a ty, kdo proceduru zakazují; cizí partneři zůstávali názvy institucí. | Každý díl má konkrétní volbu a cenu; E03/E08/E17 nesou údiv, místní oprava E11 patří Veyřanům. Matice navrhuje opakující se vedlejší role s vlastním zájmem, nikoli hotové kánonické osoby. | Pracovně řešeno; ověřit v osnovách E02/E03 |

### Přezkoumané průřezy

- Celkem 21 dílů ve správném pořadí; E01 zůstává první lidský průchod na Veyru, E07 první nelidský kontakt a E17 první taalská návštěva Země.
- Časová mapa má zhruba 44 týdnů. E02 zachovává dva týdny, E08–E10 další týdny překladu a E17 několik měsíců přípravy po kontaktu. Jde o pracovní relativní čas, ne uzamčené datum.
- Hmotové návraty vyžadují nové opačné spojení; transport vzorků není umožněn obousměrným rádiem. Relace v matici nejsou paralelní.
- E13 formalizuje zdravotní stop-pravomoc již přítomnou v pilotu; nevytváří ji zpětně. Rada určuje mantinely, Vanceová řídí krizi v hale.
- Omezení lidských misí v E19 přetrvá přes E20. Provozní dohodu lze potvrdit vzdáleně; E21 ji neruší automatickým resetem vztahů.
- Výrobní stupně brány, energetická obálka, absence pozemského FTL, neurčený původ Konstruktérů a uzavřený vnější uzávěr A-001 se nemění.

Tato kontrola potvrzuje soulad zvolené kostry, nikoli proveditelnost všech budoucích scén. Před dokončením konkrétní osnovy se musí vyřešit její blokéry z `production/season-01-continuity-matrix.md` a provést epizodní audit.

## Doplňkový průřezový audit — 3. října 2026

**Výchozí revize:** `ec53572dcad5a125222d99d23dfe5cf9c0a547c5`. Porovnáno všech 22 Markdownových podkladů repozitáře. Kontrola zahrnula odkazy, číselné parametry Ilyru, časovou mapu S01, pravidla adresování, znalosti aktérů, Leth, režim technologického transferu a nejnovější návaznosti mezi kánonem a produkčními dokumenty.

| ID | Typ a závažnost | Dotčené podklady či události | Proč jde o problém | Nejméně rušivá oprava | Stav |
|---|---|---|---|---|---|
| K-28 | Rozpor znalostí — vysoký | S01E07 v `production/season-01-story-arc.md`; `canon/gate-rules.md`; první kontakt Taal | E07 tvrdila, že Taal poznají uživatele „z dlouho tiché oblasti“, ale příchozí relace jim neposkytne čitelnou adresu ani zavedený údaj o oblasti. Předbíhalo to také opatrnější odhalení E14. | V E07 ponechat pouze neznámého nového uživatele. Vazbu na odstraněnou oblast dovolit až po dobrovolném sdílení údajů a archivním porovnání; ani tehdy nepotvrdit totožnost Země s oblastí. | Opraveno |
| K-29 | Rozpor míry jistoty — vysoký | `canon/species/leth.md`; K-11 v registru Konstruktérů | Profil nazýval taalský a oruský řetězec nezávislými, ačkoli oba prošly neznámými prostředníky a společný opisovací předek nebyl vyloučen. Tím se jeden možný pramen počítal dvakrát. | Označit řetězce za nominálně oddělené, výslovně ponechat společného předka otevřeného a oddělit materiálový fragment s nejistým autorstvím. Biologie Leth zůstává silnou inferencí díky shodě různých typů záznamu, nikoli falešnému počtu svědků. | Opraveno |
| K-30 | Ověřeno | `canon/worlds/oru-homeworld-ilyr.md` | Nový svět dosud nebyl součástí číselného registru auditu. | Přepočítat gravitaci, hustotu, tok, rok, únikovou rychlost, periodu Vary, slapové buzení a podíl Hillova poloměru. Vše souhlasí v deklarované přesnosti; doplněn primární zdroj pro řádovou mez stability družice. | Ověřeno |
| K-31 | Mezera s důsledkem — střední | záhlaví a provozní mapa S01; správa THRESHOLD | Série trvá přibližně 44 týdnů a má sahat z roku 1997 do začátku 1998, ale datum pilotu není určeno. Libovolné pozdější datum v roce 1997 už obě tvrzení nesplní. | Zachovat relativní týdny; evidovat pracovní omezení přibližně jarního data pilotu. Přesné datum určit až s historií objevu, případně upravit slovní vymezení konce série. | Otevřeno bez tichého datování |
| K-32 | Ověřeno | režim původu a transferu; rozpočet a personál THRESHOLD | Nová buňka mohla nechtěně zdvojit personál či rozpočet. | Ověřeno: 180–310 specialistů je výslovně uvnitř 1 200–1 800 osob; 80–180 mil. USD je uvnitř 1,2–2,5 mld. USD. Extrémy 3–15 % jsou aritmeticky správné a text zakazuje kombinovat je jako typický plán. | Ověřeno |
| K-33 | Ověřeno | všech 22 Markdownových podkladů | Nové průřezové odkazy mohly po přesunech či přidání souboru mířit na neexistující cestu. | Programová kontrola nenašla žádný neplatný relativní Markdownový odkaz. Páteř obsahuje právě 21 jedinečných epizod ve správném rozsahu E01–E21. | Ověřeno |
| K-34 | Záměrné tajemství — střední | Leth; Konstruktéři K-11; budoucí děj | Oprava provenience nesmí automaticky rozhodnout, zda fragment patří Leth nebo zda dvě kopie mají společný zdroj. | Nechat obě otázky otevřené. Nová stopa může určit bod rozdělení řetězců, ale nesmí tím bez dalšího potvrdit autora bran. | Chráněno |

### Kontrola schopností a zpětných dopadů

- Oprava E07 žádnou schopnost nepřidává; naopak brání Taal v lokalizaci zdroje bez dat.
- Zpřesnění Leth nesnižuje použitelnost civilizace, ale omezuje důkazní váhu archivů. Překlad nadále vyžaduje Taal i Oru, protože jejich kopie zachovaly různé kanály, i kdyby měly společného předka.
- Režim technologického transferu nepovoluje nové zařízení. Rozlišuje držbu, výzkum, reprodukci a nasazení a zachovává dřívější stupně „nalezeno až reprodukováno“.
- Ilyr nevytváří logistickou zkratku: jediný uzel, 83 % oceánů, živé materiály závislé na mikrobiomu a omezená bránová kapacita dál brání hromadnému dovozu.
- Leth nejsou zařazeni do rozpočtu odhalení S01. Jejich vlastní profil dovoluje nanejvýš nepřeložený identifikátor; úplné odhalení v první sérii by porušilo tempo a zůstává zakázané.

### Opravy provedené v této revizi

- Opravena znalost Taal v následku S01E07.
- Snížena falešná jistota o nezávislosti lethských archivních řetězců v profilu i registru Konstruktérů.
- Doplněna číselná kontrola Ilyru a primární studie stability družic.
- Zapsáno kalendářní omezení čtyřiačtyřicetitýdenní první série bez uzamčení data pilotu.
- Aktualizován auditovaný základ kontrolní matice a seznam otevřených otázek.
