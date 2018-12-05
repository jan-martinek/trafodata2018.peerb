Do práce s databázemi si můžete přenést návyky z lekcí věnovaných tabulkovým procesorům. Struktura dat je odobná, pouze namísto volné tvorby v dvourozměrném poli políček pracujete s předem definovanými tabulkami, které jsou popsány atributy ve sloupcích (např. *student* může být popsán *jménem*, *oborem*, *datem zápisu* a *seznamem absolvovaných kurzů*, škola zase *názvem*, *adresou*, *stupněm* a *seznamem studentů* — a propojit tyto seznamy je v databázi hračka). Definici databáze se říká *schéma*.

Pokud si vybavujete funkci `VLOOKUP` (česky `SVYHLEDAT`), práce s databází bude něco podobného — ale namísto kryptických souřadnic sloupců a řádků budeme používat **hezké názvy sloupců** a namísto složitých zanořených funkcí **srozumitelný jazyk [SQL](https://en.wikipedia.org/wiki/SQL)**.

### Data neexistují sama o sobě

Data vždy něco popisují. Jedna věc však může být popsána různými způsoby podle toho, čemu popis slouží. Popis domu se bude lišit, pokud jste architekt, hasič nebo nájemník. Vaše finance budete  popisovat finančnímu úřadu jinak než přátelům nad pivem. Stejně tak můžete různě popsat člověka — u doktora si o vás uloží jiné údaje než na univerzitě nebo v obchodě, kde máte zákaznickou kartu.

Při tvorbě databází je kladen důraz na efektivní ukládání dat — a existuje mnoho pravidel, které se vyplatí znát. Nicméně všechna doporučení jsou závislá na správném výběru dat a sledování závislostí mezi nimi.

### SQL dotazy

SQL (Structured Query Language), která se k používá k „dotazování“ se na informace v databázi, připomíná angličtinu. Větu *„Vyber jména studentů z Veselé školky!“* bychom mohli (s trochou cílevědomosti) přeložit jako „*Select names of students from Veselá školka.“*. SQL nejde o mnoho dál:
  
    SELECT name FROM student WHERE school_name = 'Veselá školka';
    
Kdybychom měli větší databázi, kde jsou vedle informacích o studentech a žácích též informace o školách (jak bylo napsáno výše), musíme mezi sebou propojit tabulky. Dotaz by pak mohl vypadat takto:
  
    SELECT name FROM student 
    LEFT JOIN school ON student.school_id = school.id
    WHERE school.name = 'Veselá školka Blansko';

Kdybychom chtěli získat nejen jména, ale všechny dostupné informace o studentech, stačí napsat hvězdičku:

    SELECT * FROM student 
    LEFT JOIN school ON student.school_id = school.id
    WHERE school.name = 'Veselá školka Blansko';        
  
A kdybychom chtěli několik různých konkrétních údajů, mohli bychom je vypsat oddělené čárkami, tedy např.
  
    SELECT name, enrollment_date FROM student 
    LEFT JOIN school ON student.school_id = school.id
    WHERE school.name = 'Veselá školka Blansko';     
  
Stejně snadno si můžete vytáhnout počet studentů všech škol v databázi:

    SELECT COUNT(*) FROM school 
    LEFT JOIN student ON school.id = student.school_id
    GROUP BY school.id;

### Datové typy

S definicí tabulek přichází jedna důležitá věc: tabulkový procesor se z poskytnutých dat snažil určit datový typ (např. číslo poznal a zarovnal jej vpravo), ale mohli jste si jej i sami nastavit (možná se vám stalo, že chybně rozpoznal v nějakém číslu s desetinnou čárkou datum a podobně). 

Při tvorbě databáze musíte datový typ nastavit vždy sami. Dopředu tak určíte, že něco je číslo a něco jiného je text. Většina databázových systémů umožňuje nastavit i typy jako datum, výběr z několika hodnot (`enum`) apod.

### Konvence

Při návrhu databáze existují určité konvence, s nimiž se budeme učit zacházet. Pro začátek stačí tyto dvě věci:

- názvy tabulek a sloupců udržujeme v angličtině,
- pokud názvy musí obsahovat mezeru, vkládáme na její místo podtržítko (`_`),
- tabulky pojmenováváme názvem v jednotném čísle (tabulka se tak jmenuje `student`, nikoli `students`),
- každá tabulka obsahuje číselný sloupec `id`, do kterého se ukládá její jedinečný identifikátor,
- když vytváříme spojení mezi tabulkami (např. „ve škole jsou zapsáni studenti”, „student má zapsané předměty“), dané sloupce pojmenováváme názvem jiné tabulky s příponou `_id` (tedy například `school_id`, `course_id` atp.).

Při odpovídání a hodnocení berte ohled na popsané konvence.
