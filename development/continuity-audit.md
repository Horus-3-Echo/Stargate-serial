# Registr auditu kontinuity

**Poslední úplný audit:** 1. října 2026  
**Auditovaný stav před opravami:** hlavní větev na commitu 12a9821cb17df4e27047e3e60415a09cb322b7c5  
**Účel:** evidovat skutečné rozpory, minimální opravy, záměrná tajemství a dosud neurčené údaje bez tichých retconů

## Rozsah auditu

Porovnány byly:

- základní premisa a technická pravidla brány,
- registr důkazů o Konstruktérech,
- Veyra a Náar,
- Taal a Oru,
- Project THRESHOLD a první diplomacie,
- tvůrčí omezení, otevřené otázky a formát seriálu,
- poslední související změny hlavní větve.

V auditovaném stavu repozitář neobsahoval podrobné osnovy jednotlivých epizod, časovou osu scén ani profily hlavních lidských postav. Pozdější příspěvky doplnily pilot S01E01, základ hlavního pozemského ansámblu a pracovní příčinnou páteř všech 21 dílů. Samostatné osnovy epizod 2–21 a scénové časové osy však stále chybějí. Jde o částečně zaplněnou mezeru, ne o uzavřený audit celé série.

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
| K-03 | Mezera — vysoká | Veyra 1,04 baru; Náar 1,68 baru; svět Oru 1,2–1,4 baru | Profily předpokládají bezpečné otevření mezi různými atmosférami, ale centrální pravidla nevysvětlovala, proč se tlaky okamžitě nevyrovnají. | Stanovit, že aktivní horizont není volný otvor a potlačuje pasivní tlakový i hydrostatický tok. | Opraveno |
| K-04 | Mezera — vysoká | canon/species/oru.md; obecná pravidla | Pravidlo úplného vstupu fyzicky souvislého objektu bylo uvedeno jen u Oru. Bez zobecnění by kabely, hadice a částečný průchod obcházely logistická omezení. | Přesunout obecné pravidlo celého objektu do canon/gate-rules.md; u Oru ponechat biologický důsledek. | Opraveno |
| K-05 | Mezera — vysoká | canon/species/taal.md; Project THRESHOLD | Taal nedostanou čitelnou adresu Země, zatímco diplomatický protokol používá návratový token. Centrální pravidla neoddělovala token od skutečné adresy. | Zapsat, že příchozí spojení adresu neodhalí a původní ovladač může nabídnout pouze dočasný návrat posledního spojení. | Opraveno |
| K-06 | Mezera — střední | Project THRESHOLD; všechna spojení | Politický dokument správně zachází s časem brány jako s nedostatkovým zdrojem, ale základní pravidla neříkala, že uzel může vést jen jedno spojení. | Uzamknout jedno současné spojení na jednu bránu a stejnou cenu komunikačního i transportního slotu. | Opraveno |
| K-07 | Ověřeno | Veyra; Náar | Hmotnost, poloměr, gravitace, hvězdný příkon a oběžné doby jsou vzájemně konzistentní v deklarované přesnosti. | Bez změny. | Ověřeno |
| K-08 | Ověřeno | Project THRESHOLD | Rozpočet 1,2–2,5 mld. USD odpovídá přibližně 0,48–0,99 % základny 251,6 mld. USD; zaokrouhlení na 0,5–1,0 % je správné. Personální odhad není v rozporu s rozpočtovými kategoriemi. | Bez změny. | Ověřeno |
| K-09 | Možná nechtěná vazba — střední | Veyra; Oru | Veyra má poslední známou aktivaci přibližně před šesti stoletími a Oru začali svou bránu systematicky používat rovněž asi před šesti stoletími. Čtenář může očekávat společnou příčinu. | Zatím neměnit. Buď vazbu později vědomě využít, nebo při přesnější chronologii hodnoty od sebe oddělit. | Otevřeno |
| K-10 | Záměrné tajemství | registr Konstruktérů; Taal | Odstraněná oblast Země, bezpečnostní odmítnutí adres a vrstvy ovladačů mají několik slučitelných vysvětlení. | Nevybírat vysvětlení v raných sériích; evidovat zdroj a míru jistoty každé nové stopy. | Chráněno |
| K-11 | Otevřený údaj — vysoké budoucí riziko | canon/gate-rules.md; development/open-questions.md | Přesný příkon, chování vysokoenergetického záření, aktivně tlačených kapalin a selhání bufferu nejsou uzamčeny. Předčasné řešení by mohlo vytvořit zbraň, volnou energii nebo snadnou záchrannou schopnost. | Ponechat otevřené, ale před první epizodou, která je použije, provést samostatný audit zpětných důsledků. | Otevřeno |
| K-12 | Mezera projektu — vysoká | production/series-format.md; production/season-01-story-arc.md | Příčinná mapa 21 dílů už sleduje schopnosti, ceny, návraty a postavy, ale epizody 2–21 nemají samostatné osnovy ani scénové časování. | Při rozpracování každého dílu zachovat sezónní příčinu a provést plný epizodní audit. | Pracovně řešeno |
| K-13 | Otevřený údaj — střední | Veyra; Taal; Project THRESHOLD; production/season-01-story-arc.md | Pracovní páteř stanoví první omezenou veyrskou komunikaci v S01E03, začátek Taal v S01E07 a vývoj slovníku přes S01E08–S01E10. Přesná délka jednotlivých relací čeká na osnovy. | Nezkracovat překlad na jedinou scénu a při teleplayích zachovat týdny mezi komunikačními okny. | Pracovně řešeno |
| K-14 | Ověřeno | Taal; Oru; Veyra; Project THRESHOLD | Současné civilizace nemají FTL lodě ani výrobu bran; taalský ovladač, oruská biotechnologie a pozemská pomoc Veyře mají výslovné výrobní, právní a ekologické brzdy. | Mantinely zachovat při každé nové technologii. | Ověřeno |
| K-15 | Rozpor — kritický | dřívější verze production/s01e01-pres-prah.md; canon/gate-rules.md | Pilot nechal tým projít ze Země na Veyru a vrátit se během téhož spojení, přestože makroskopická hmota může jít pouze od vytáčející k přijímající bráně. | Zachovat objev Veyry, ale rozdělit cestu na spojení Země → A-005 a nové spojení A-005 → Země; návrat vyžaduje těžký polní ovladač a výslovně předanou návratovou sekvenci. | Opraveno |
| K-16 | Záměrné tajemství — vysoké budoucí riziko | A-001; production/season-01-story-arc.md; adresa Země | Finále používá kontrolní součet chybějícího modulu A-001. Bez omezení by mohl být zaměněn za důkaz, že modul někdo ukradl, že jde o Konstruktéry nebo že modul byl jediným zdrojem adresy. | Potvrdit pouze přístup volajícího k datům modulu a znalost adresy; identitu, motiv i úplný řetězec získání ponechat otevřené. | Chráněno |

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

## Kontrola dlouhodobých důsledků

### Jediný uzel jako úzké místo

Pravidelné spojení s Taal, obchod s Veyrou, průzkum i záchranná mise soutěží o stejný pozemský uzel. Project THRESHOLD tento důsledek správně převádí do politického přidělování slotů. Budoucí scénáře nesmějí plánovat dvě paralelní pozemská spojení, dokud Země nezíská druhou funkční bránu.

### Adresa Země

Příchozí spojení neprozradí trvalou adresu. Krátkodobý návratový token umožní bezprostřední odpověď, ale ne pozdější samostatné zavolání. Každý protivník nebo partner, který po delší době vytočí Zemi, proto musí mít doložitelný zdroj adresy. Toto pravidlo chrání význam budoucího nečekaného příchozího spojení.

### Atmosféry a karanténa

Potlačení pasivního proudění zabraňuje okamžitému fyzikálnímu kolapsu při spojení s Náarem nebo světem Oru. Nezabraňuje však přenosu patogenů na osobách, předmětech a vzorcích. Technické pravidlo proto neruší biologickou karanténu.

### Technologický transfer

Taalské zařízení může být používáno bez pochopení a oruské živé materiály mimo vlastní mikrobiom degradují. Ani jedna civilizace neposkytuje Zemi reprodukovatelný technologický skok. U každého budoucího zařízení se musí znovu kontrolovat stupně nalezeno, aktivováno, charakterizováno, pochopeno a reprodukováno.

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
