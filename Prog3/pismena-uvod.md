V několika následujících úkolech budete pracovat se stejným zadáním: budete
kreslit konkrétní latinkové písmeno, a to buď v jeho verzálkové nebo minuskové
podobě. Písmeno můžete nakreslit jednoduše i detailně, v libovolném stylu, ale 
mělo by být zcela jasně rozpoznatelné. 

### Podmínky

Písmeno nakreslete tak, 

- **aby se vešlo do vyznačeného rámečku** (200x150px), přičemž dolní hrana
rámečku je [účaří](https://www.google.cz/search?q=%C3%BA%C4%8Da%C5%99%C3%AD) a
horní hrana je horní dotažnice (střední dotažnici si můžete umístit dle
libosti),
- **aby želva skončila na účaří, otočená směrem nahoru** (jako
pomůcka je na konci skriptu příkaz, který vykreslí žlutou čáru, která by měla
být rovnoběžná nebo totožná s pravou hranou rámečku),
- **celý postup vepište do funkce `letterUpperA`**, kterou pak přejmenujte tak,
aby seděla k vašemu písmenu (`Upper` = verzálka, `Lower` = minuska, `[A-Z]` =
písmeno).

### Tipy

- Postupujte po kouscích: zkuste nakreslit první část písmena, spusťte kód a
pokud to bude fungovat správně, pokračujte dál. Když se netrefíte, trochu
upravte kód a opakujte postup.
- Pokud potřebujete, kreslete si na papír nebo klidně „choďte jako želva“ po
místnosti.
- Nemusíte začít vlevo dole — propisku můžete vypnout nastavením
`turtle.penDown = false;` a odjet se želvou tam, kam potřebujete. Začněte
jednodušší částí písmene a pokračujte ke složitějším (úlohy jsou tři, vyberte
si jednoduché písmeno do začátku).
- Algoritmus můžete vytvářet od konce — pokud máte hotové celé písmeno, ale
nepasuje do rámečku, stačí přidat příkazy před první kreslicí příkazy, aby se
želva na začátku přesunula jinam.
- Pkud chcete nějakou sekvenci příkazů zopakovat vícekrát, můžete využít cykly
[while](https://www.w3schools.com/js/js_if_else.asp) nebo [for](https://www.w3schools.com/js/js_loop_for.asp)
anebo využít funkci `repeat(n)`. (Zkopírujte si její užití klidně z funkce `frame()` 
v původním kódu).
- Pokud chcete, kreslete písmena klidně barevná.
- Dolní dotahy (jako např. u písmen *y* nebo *g*) zakreslete mimo rámeček, ale
do plátna.
- Mrkněte na parametry hodnocení úkolu, abyste věděli, podle čeho budou
písmena hodnocena.

Pro inspiraci je v předvyplněném kódu nakreslena verzálka **A**. Upravujte
obsah funkce `letterUpperA` (můžete upravit i jinou část skriptu, ale písmeno
musí vykreslit tato funkce), nicméně můžete si upravit i zbytek kódu (např.
písmeno vykreslit už v metodě `p.setup()` pomocí `run.print()`).