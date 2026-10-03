# Obětovaná sonda A-001 a protokol čerstvé výzvy

**Stav:** kánonická technická obálka pro S02; přesná poslední poloha vozíku E12 a konkrétní obraz změny v hale zůstávají produkčními rozhodnutími  
**Nadřazená pravidla:** [technická pravidla brány](../gate-rules.md), [energetika a ochrana pozemského uzlu](gate-power-and-ingress-safety.md)  
**Lokalita:** [A-001 — Prahová stanice](../worlds/a-001-prahova-stanice.md)  
**Dějová vazba:** [dlouhodobá páteř seriálu](../../production/series-long-arc.md)

## Účel a hranice důkazu

Mise ve druhé sérii má zodpovědět úzkou otázku: **změnil se po incidentu S01E12 stav haly A-001 a získal někdo později přístup k tomu, co na místě zanechá nová sonda?** Nemá získat adresu volajícího, otevřít vnější uzávěr, zachránit starý vozík ani potvrdit identitu Konstruktérů.

Sonda projde ze Země na A-001 jako jeden celý objekt při pozemsky vytáčeném spojení. Obraz a telemetrie se vracejí elektromagneticky stejnou relací. Hmota se vrátit nemůže; po ukončení spojení zůstává sonda na A-001. Nenese polní ovladač ani pozemskou návratovou sekvenci a sama neumí bránu vytočit.

## Referenční sestava

Jde o účelový pozemský robot z dobově dostupných průmyslových, vojenských a planetárních technologií. Není odvozen od mimozemského zařízení.

| Vlastnost | Pracovní obálka | Důvod |
|---|---:|---|
| hmotnost | nominálně 280 kg; nepřekročit 320 kg | dostatečná stabilita a baterie, ale snadná pozemská manipulace bez polního ovladače |
| přepravní rozměry | přibližně 1,35 × 0,85 × 0,65 m | celý robot musí projít horizontem; žádný kabel nezůstává na Zemi |
| podvozek | šest poháněných kol, nízký těžišťový rám, pasivní přední skluznice | hladká hala je pravděpodobná, nikoli garantovaná; skluznice pomáhá opustit přímou osu i po ztrátě části pohonů |
| rychlost | 0,10–0,15 m/s běžně; nejvýše 0,35 m/s | přesnost a teleoperace mají přednost před rychlostí |
| využitelná energie | 2,5–3,5 kWh ze zapečetěné NiCd soustavy | vysoká hmotnost je přijatelná; technologie a její provozní rizika odpovídají konci 90. let |
| elektrický příkon | do 3,5 kW krátkodobě; plánovaný průměr nejvýše 1,2 kW | pohon, topení, osvětlení, kamery, analyzátory a rádio |
| senzory | dvě pevné širokoúhlé kamery, otočná kamera, stereodvojice, lidar krátkého dosahu, teplota, tlak, plyny, radiace a inerciální jednotka | redundance obrazu a měření bez univerzálního „skeneru“ |
| pracovní dosah | hlavní hala a přilehlý úsek již zobrazených servisních chodeb | mise neotevírá vnější uzávěr a neprovádí globální průzkum |
| manipulace | pouze sklopný držák tokenu a jednoduchá značkovací lišta | žádné rameno schopné demontovat modul, otevírat dveře nebo nést zbraň |

Sonda nemá výbušninu, samodestrukci, biologický odběr, aktivní chemický zdroj ani energetický vysílač mimo charakterizovaný rádiový a osvětlovací výkon. Ztracená sonda se činí bezpečnější **nepřítomností citlivých údajů**, nikoli spolehlivým fyzickým zničením.

## Energetická a mechanická kontrola

Při průměru 1,2 kW spotřebuje 35 minut provozu asi:

```text
E_sonda = 1,2 kW × 35/60 h ≈ 0,7 kWh ≈ 2,5 MJ
```

Baterie 2,5–3,5 kWh tedy neposkytuje falešnou přesnost doby jízdy, ale nejméně trojnásobnou rezervu proti chladu, špičkám pohonů, stárnutí článků a zdržení. Celá uložená elektrická energie je přibližně 9–13 MJ.

Třicetičtyřminutové spojení spotřebuje podle pozemské obálky přibližně:

```text
E_brana = E_pulz + P_udržování × t
E_brana ≈ (1,5 až 4) GJ + (3 až 7) MW × 2 040 s
E_brana ≈ 7,6 až 18,3 GJ
```

Bránová relace je tedy energeticky zhruba o tři řády výše než kapacita baterie sondy. Robot není přenosný zdroj pro bránu a jeho baterie nevysvětluje fyziku spojení.

Při 280 kg a 0,86 g tlačí sonda na podlahu silou přibližně 2,4 kN. Pro součet styčných ploch kol 0,06–0,10 m² vychází průměrný měrný tlak asi 20–40 kPa. To omezuje poškození známé podlahy, ale není zárukou pro skrytou dutinu nebo aktivní panel; trasa se nejprve kontroluje stereokamerou a krátkodosahovým lidarem.

## Spojení, řízení a datová hygiena

- Konstrukční cíl odchozího průzkumného kanálu je 64–256 kbit/s v již charakterizovaném pásmu. Při zhoršení spojení se sonda přepne na 9,6 kbit/s pro telemetrii, náhledy a několik prioritních snímků. Jde o provozní profil, ne fyzikální kapacitu brány.
- Data jsou řazena: stav a poloha sondy → časově označené snímky vozíku E12 → panoramata a referenční měřítka → token → ostatní senzory. Ztráta souvislého videa proto nezničí hlavní důkaz.
- Dva pozemské přijímače ukládají nezávislý bitový tok. Operátor pracuje s kopií; původní záznam se po relaci uzavře na oddělené zapisovací médium a podepíše.
- Řízení používá pevný malý slovník povelů, pořadová čísla a ověření zprávy předem vloženým klíčem relace. Sonda nepřijímá spustitelný kód, aktualizaci firmwaru ani obecný síťový paket.
- Letový program je v nepřepisovatelné paměti. Obrazový kruhový buffer je volatilní; po vybití nezůstává úplný archiv.
- Klíč relace po skončení okna nemá hodnotu pro další aktivaci. Na palubě nejsou adresa Země, jiné adresy, katalog sítě, plán základny ani dlouhodobé kryptografické klíče.
- Mise nepoužívá kabel přes horizont. Napájení, řízení i mechanika musí po průchodu existovat na jedné straně.

## Jediný vizuální nonce

Bloky III a IV S02 používají **jeden a tentýž** čerstvý token, nikoli dvě různé výzvy.

1. Krátce před relací vznikne rovnoměrně náhodná hodnota o 160 bitech pod dvoučlennou kontrolou.
2. Hodnota neobsahuje významová pole. Není adresou, heslem brány, programem, povolením ke vstupu ani klíčem k jinému systému.
3. Její otisk spolu s identifikátorem mise se před průchodem zapíše a digitálně podepíše do odděleného auditního záznamu. To omezuje dodatečnou záměnu tokenu; nebrání úniku od zasvěceného člověka.
4. Sonda hodnotu na A-001 nastaví na pasivním bistabilním panelu ve dvou shodných kopiích: jako mřížku 16 × 10 bitů a jako 40 šestnáctkových znaků. Orientační značky a samostatný kontrolní součet slouží pouze k opravě čtecích chyb.
5. Kamera odešle široký záběr spojující panel s referenčními body jeho polohy a poté detail obou kopií. Panel zůstane čitelný bez trvalého napájení.
6. Rada v následujícím bloku pouze schválí použití již položeného nonce jako výzvy pro volajícího; neposílá na A-001 druhý kód.

Při rovnoměrném výběru je náhodná shoda celé 160bitové hodnoty řádu 2⁻¹⁶⁰. To však není důkaz identity. Správná pozdější odpověď dokládá pouze, že volající nebo jeho zdroj token po nasazení sondy pozoroval, získal jeho věrnou kopii nebo jej obdržel od někoho s přístupem. Neprokazuje biologickou přítomnost, vlastnictví stanice, držbu starého modulu ani vztah ke Konstruktérům.

Dobový podpis a otisk chrání pozemský řetězec úschovy, ne fyziku sítě. Nesmějí se zobecnit na univerzálně bezpečnou autentizaci ani na současnou kryptografickou praxi.

## Časový plán jediné relace

Cílové ukončení je nejpozději ve 34. minutě; přibližně čtyři minuty zůstávají jako rezerva před běžnou mezí 38 minut.

| Čas od ustavení | Úkol | Bod ukončení |
|---|---|---|
| 0–4 min | průchod, odjezd z přímé osy, základní telemetrie a kontrola atmosféry | bez potvrzené polohy nebo při neznámém nebezpečném toku se relace ukončí |
| 4–18 min | prioritní snímky vozíku E12, starých stop a referenčních bodů haly | mobilita se neobětuje za úplnou mapu |
| 18–25 min | umístění panelu, široký záběr a dva nezávislé detaily nonce | bez čitelného dvojího záznamu se výzva nepovažuje za založenou |
| 25–31 min | redundantní panoramata a vybraná měření | žádné otevírání uzávěru ani demontáž |
| 31–34 min | parkování mimo osu, vymazání klíče relace a řízené ukončení | ztracená sonda se nezachraňuje člověkem ani druhou okamžitou relací |

Časy jsou provozní rozpočet, nikoli tvrzení, že brána selže přesně v 38:00.

## Poruchové stavy

| Porucha | Reakce | Co se nesmí tvrdit |
|---|---|---|
| po průchodu nepřijde telemetrie | krátké opakování výzvy, poté ukončení podle předem daného času | že sonda přežila nebo že ji někdo zajal |
| podvozek zůstane v přímé ose | jeden pevný pokus vpřed a šikmo; jinak ztráta stroje a nový bezpečnostní rozbor | že příští aktivace sondu bezpečně vrátí; iniciační jev ji může poškodit nebo zničit |
| selže hlavní datový tok | nízkorychlostní telemetrie, náhledy a prioritní snímky | že neúplné video dokládá nepřítomnost aktéra mimo zorné pole |
| povel neprojde autentizací | povel se zahodí, robot zpomalí a pokračuje v posledním bezpečném stavu | že pevný parser odolá každému neznámému útoku |
| selže panel nebo jedna kopie nonce | token není platnou výzvou, dokud Země nemá dva čitelné záznamy a kontext | že pozdější podobný řetězec je odpověď |
| objeví se neznámý pohyb nebo inteligentní aktér | zastavit přiblížení, vyslat jednoduchý neadresní identifikační vzor, neblokovat průchod | že mlčení znamená souhlas nebo nepřítomnost |
| přijde vysoký výkon či neznámé záření zpět kanálem | odpojit hlavní přijímače a ukončit spojení | že sonda nebo pozemské stínění zaručují bezpečnost |
| klesne energie nebo teplota | dokončit nejvyšší prioritu, zaparkovat mimo osu, odpojit pohony | že robot zůstane později dálkově dostupný |

Na sondě není výbušná autodestrukce. Pokud se jí někdo zmocní, může rozebrat lidskou techniku konce 90. let a zjistit, co kamera viděla po dobu relace; nemá z ní však získat adresu Země nebo schopnost vytáčet.

## Zneužití a zpětné dopady

- **Není to průzkum bez ceny:** jedna relace spotřebuje 7,6–18,3 GJ pozemské energie, blokuje jedinou bránu, vyžádá si dochlazení a odsune diplomatický nebo záchranný slot.
- **Není to opakovatelná kamera:** po zavření nemá sonda cestu pro data. Další obraz vyžaduje novou pozemskou relaci a neví se, zda robot ještě funguje.
- **Není to autentizace osoby:** nonce autentizuje čerstvý přístup k informaci, nikoli tělo, vládu, druh nebo motiv.
- **Není to suverenitní značka:** panel nemá vlajku ani územní prohlášení; nese pouze referenční značky, hodnotu a neutrální identifikátor mise.
- **Není to skrytá zbraň:** hmotnost, zásoba energie, síla manipulace a software jsou před misí evidovány; nejsou přítomny výbušniny, toxické náplně ani prostředek k ovládnutí místní brány.
- **Není to řešení E12:** starý vozík nedostává nové napájení, senzory ani vysílač. Nová sonda jej pouze fotografuje.
- **Není to důkaz modulu E04:** teprve unikátní neveřejná kalibrační data mohou podpořit držbu modulu nebo úplné kopie jeho paměti.

## Reálné opory měřítka

- JPL popisuje rover Sojourner z roku 1997 jako šestikolové vozidlo o hmotnosti 10,5 kg, s jedenácti motory, primárními bateriemi, solárním napájením a UHF spojením. Dokládá dobovou dostupnost malé dálkově řízené planetární robotiky; zde navržených 280 kg je konzervativní pozemský stroj bez omezení kosmickým startem: [JPL Robotics — Mars Pathfinder Rover: Sojourner](https://www-robotics.jpl.nasa.gov/what-we-do/flight-projects/pathfinder/).
- Dobový popis mise uvádí, že Sojourner byl řízen operátorem pomocí obrazů, ale kvůli přibližně desetiminutovému zpoždění potřeboval autonomní řízení: [NASA NSSDCA — Mars Pathfinder Project Information](https://nssdc.gsfc.nasa.gov/planetary/mesur.html).
- NASA/JPL v roce 1997 vydala pokyny pro pořizování vysoce spolehlivých letecko-kosmických NiCd článků. Zdroj dokládá existenci a inženýrská omezení chemie, nikoli přesnou kapacitu fiktivní baterie: [NASA NTRS — Guidelines for the Procurement of Aerospace Nickel Cadmium Cells](https://ntrs.nasa.gov/citations/19970037681).
- SHA-1 byl v dubnu 1995 vydán jako FIPS 180-1 a DSA v roce 1994 jako FIPS 186; digitální otisk a podpis jsou tedy dobově dostupné pro auditní řetězec: [NIST FIPS 180-1](https://csrc.nist.gov/pubs/fips/180-1/final) a [NIST FIPS 186](https://csrc.nist.gov/pubs/fips/186/final).

Tyto zdroje dokládají dosažitelnost pozemské robotiky, napájení a auditní kryptografie konce 90. let. Nedokládají červí díru, průchod signálu bránou ani bezpečnost A-001.
