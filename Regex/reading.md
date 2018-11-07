### Začít zlehka

V této lekci je důležité začít zlehka. Níže doporučím několik zdrojů, ale tím nejdůležitějším je v této lekci opět **hraní si**. Přímá zkušenost je nenahraditelná — obdobně jako pro děti, které si hrají s předměty, které najdou na pískovišti (s tím rozdílem, že tam běžně nenajdou regulární výrazy — *zatím*).

> ### Poznámka: Co klasické dokumenty?
> 
> Oproti předchozím letům se tato lekce věnuje pouze běžným regulárním výrazům — vynechány jsou textové procesory, které pracují s jejich různými obdobami. Některé se blíží více, jiné méně: např. v textovém procesoru MS Word se obdobné funkcionalitě říká [*wildcards* a *special characters*](http://www.google.com/search?q=using+ms+word+wildcards) (česky [*speciální a zástupné znaky*](http://www.google.com/search?q=ms+word+speciální+a+zástupné+znaky)). V LibreOffice Writer a Google Documents se naopak blížíme syntaxi `pcre` regulárních výrazů, kterou budeme používat.
> 
> Komplikací je též to, že v různých verzích těchto kancelářských balíků najdete pokročilé hledání a nahrazování textů na různých místech a použitelné speciální a zástupné znaky se mohou lišit. I tak stojí za to vědět, že i zde je možné využít znalost pokročilého nahrazení textu — jen si musíte nastudovat, jaké značky je možné používat a jak pracuje nahrazování.
>
> Další informace najdete hledáním [search and replace in word](http://www.google.com/search?q=search+and+replace+in+word), popř. česky [najít a nahradit ms word](http://www.google.com/search?q=najít+a+nahradit+ms+word). 

### Jdeme na to

Začneme průchodem lekcemi [výukového kurzu a hry v jednom RegexOne](http://regexone.com). Projděte si prvních 15 lekcí a **soustřeďte se při tom na texty, které představují jednotlivé koncepty**. Cvičení se často dají vyřešit bez využití probíraných konceptů, ale ty vám později budou chybět.

**Po průchodu kurzem nahrajte do prvního úkolu screenshot z RegexOne s nápisem „You've finished the tutorial!“**

#### Další materiály

Krom praktického cvičení se může hodit další materiál. Vzhledem k tomu, že jde o poměrně praktickou a dobře živě předveditelnou látku, doporučuji zejména názorná [videa Daniela Shiffmana](https://www.youtube.com/playlist?list=PLRqwX-V7Uu6YEypLuls7iidwHMdCM6o2w). Dají se objevit i videa v češtině, [například od vtipného řečníka Davida Grudla](http://www.youtube.com/watch?v=uzHIXuGzaaY) — ten během prvních pár minut shrnuje všechny základní věci, ale nejsou tak dobře ilustrované.

<iframe width="560" height="315" style="margin-bottom: 1rem;" src="https://www.youtube.com/embed/7DG3kCDx53c" frameborder="0" allowfullscreen></iframe>

Pokud se učíte vizuálně, může vám pomoci nástroj [Regulex](https://jex.im/regulex/), který shluky písmen překládá do přehlednější schematické podoby. Výsledek může vypadat třeba takto ([nebo třeba takto](https://jex.im/regulex/#!flags=&re=%3C%5Ba-z0-9%5D%2B%3E%5B%5E%3C%5D%2B%3C%2F%5Ba-z0-9%5D%2B%3E)):

<iframe frameborder="0" width="600" height="169" style="margin-bottom: 1rem;" src="https://jex.im/regulex/#!embed=true&flags=&re=ve(lr%7Crl)%5Byi%5Dba"></iframe>

Pokud už trochu tušíte, o co jde, přečtěte si nějaký úvodní obecný text pro začátečníky — v angličtině je jich poměrně dost a nejsou těžké, např. [An Introduction to Regular Expressions](http://www.codeproject.com/Articles/939/An-Introduction-to-Regular-Expressions) (další výsledky z Googlu pro [intro regular expressions](http://www.google.com/search?q=regular+expressions+intro)). V češtině něco [najdete také](http://www.google.com/search?q=regulární+výrazy), ale bývají to o něco složitější texty.


#### Jak si vyzkoušet, jak to funguje

Pracovat s reguláry můžete v editoru Sublime Text, kde stačí [zapnout hledání pomocí regulárních výrazů](http://docs.sublimetext.info/en/latest/search_and_replace/search_and_replace_overview.html). Pro přehlednější tvorbu výrazu můžete využít různé webové nástroje, které zvýrazňují jak části výrazu, tak nalezené shody: asi nejlepší z nich je [Regex101](https://regex101.com).

<iframe frameborder="0" width="600" height="600" style="margin-bottom: 1rem;" src="https://regex101.com/r/X128py/3"></iframe>

> Regex101 se na první pohled tváří složitě, ale vystačíte si se dvěma vstupními poli uprostřed stránky. Ostatní pole vám mohou pomoci, ale nejdůležitější je vizuální zpětná vazba, kterou tento nástroj poskytuje. 
>
> **Důležitý tip:** Abyste vyhledávali všechny výskyty hledané fráze v nástroji [Regex101](https://regex101.com), zapněte si v poli pro regulární výraz modifikátor (flag) `global`. Danou volbu najdete po kliknutí na vlaječku napravo.
>
> Pokud vám Regex101 nesedne, vyzkoušejte libovolný [jiný tester](http://www.google.com/search?q=regex+tester).


### Hříčky, hry a interaktivní kurzy

Po patnácti lekcích a nějakém čtení byste měli mít základní představu, co to regulární výrazy jsou — my se budeme bavit o tzv. **Perl-Compatible Regular Expressions** (tento název si nemusíte pamatovat, ale občas se vám může hodit při googlování — a možná jste si všimli položky *„pcre“* v nástroji Regex101, to je zkratka onoho delšího názvu).

Své znalosti si můžete ověřit na [nějaké hře](http://www.google.com/search?q=regexp+game). Doporučuji [Regex Golf](http://regex.alf.nu), který má i hezké nastavení obtížnosti.

>\_**Pozn.:** Při psaní regulárních výrazů si nemusíte vše pamatovat. Důležité je naučit se základním principům a umět se vyznat v [cheatsheetu](http://www.google.com/search?q=regex+cheat+sheet), když jej potřebujete. (Dobrý cheatsheet poznáte klidně si ho vytiskněte).
