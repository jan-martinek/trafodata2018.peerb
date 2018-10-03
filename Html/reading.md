### Zdrojový kód

Jedním z nejdůležitějších konceptů na webu je tzv. zdrojový kód. Zdrojový kód HTML je prostý text, který obsahuje předem definované značky, které umí webové prohlížeče (jako jsou např. Google Chrome, Microsoft Edge, Mozilla Firefox a další) zpracovat.

Mezi tím, co se vám zobrazí v prohlížeči, a zdrojovým kódem je rozdíl: ***zdroják* popisuje to, co prohlížeč *zobrazuje***. Princip je přibližně následující. 

Ve zdrojáku je napsáno něco jako: 

<div class="panel">
 <code>TOHLE JE NADPIS DRUHÉ ÚROVNĚ: Nadpis</code>
</div>

a prohlížeč zobrazí:
    
<div class="panel">
    <h2>Nadpis</h2>
</div>

Protože psát `TOHLE JE NADPIS: ` před každý nadpis by bylo omezující, HTML používá zkrácené značky vymezené lomenými závorkami. Výše uvedený nadpis tak můžete napsat pomocí značky `h2` (z anglického „level 2 heading”): 

<div class="panel">
    <code>&lt;h2&gt;Nadpis&lt;/h2&gt;</code>
</div>

U jakékoli stránky, kterou vidíte na internetu, si můžete zdroják zobrazit. [Jak na to?](https://www.google.cz/search?client=safari&rls=en&q=jak+zobrazit+zdrojov%C3%BD+k%C3%B3d+str%C3%A1nky)

### Sémantika

Asi nejdůležitější, čemu se musíte při práci s HTML naučit, je to, že pracujete s významem částí dokumentu, nikoli s jejich podobou. Výše uvedený příklad ukazuje tvobu *nadpisu*, nikoli *většího tučného textu*.

HTML popisuje význam, nikoli podobu. Tyto dvě věci mezi sebou souvisí, ale první je vždy význam. Podoba může být různá — nadpis v knize bude vypadat odlišně, než nadpis v lifestylovém časopisu. Ale **stále jde o nadpis**. Je to důležité i kvůli tomu, že webový obsah nemusí vždy vypadat stejně: jinak vypadá na mobilu, jinak na počítači, jinak na hlasové čtečce, kterou dnes používají především neslyšící.

Je to tak důležité, že to stojí za zopakování: **HTML popisuje význam prvků dokumentu (sémantiku dokumentu), nikoli jejich podobu.**

### Učíme se psát

Pro psaní HTML nepotřebujete žádné superschopnosti — stačí umět napsat tyto čtyři znaky: `<>"/` (lomené závorky, uvozovky a lomítko). Pak už snadno napíšete i pěkný odkaz `<a href="doma.html">domů</a>`. Jak tyto znaky napsat na české klávesnici? Googlujte třeba „[speciální znaky česká klávesnice](https://www.google.cz/search?q=speci%C3%A1ln%C3%AD+znaky+%C4%8Desk%C3%A1+kl%C3%A1vesnice)“. *Tip: Uživatele MS Windows bude zajímat [pravý Alt (AltGr)](http://dusan.pc-slany.cz/klavesnice/obrazky/pravy-alt.gif).*

### Základní četba

Četbou na tento týden je tentokrát velmi stručný výtah k HTML, který najdete [online](http://jan-martinek.com/etc/html/) (autorem je vyučující, proto se nebojte na nejasnosti ptát ve fóru).

Pokud budete chtít obdobný návod popsaný jinými slovy (opakování je zde skutečně matkou modurosti), doporučuji [googlit](https://www.google.cz/search?q=html+basics) — ale dávejte si pozor, internet je plný nepřesných a neaktuálních článků. *Určitě si ve vyhledávači nastavte časové omezení na poslední rok.* Pěkný článek, který je alternativou zadaného textu, je přímo [od Mozilly](https://developer.mozilla.org/en-US/Learn/Getting_started_with_the_web/HTML_basics), organizace, která vyvíjí prohlížeč Firefox.

Dalším způsobem, jak se HTML snadno naučit, je vyzkoušet si krátký e-learningový kurz na serverech jako je [Coursera](http://coursera.com) nebo [Khan Academy](http://khanacademy.org). V dalších lekcích se s těmito servery ještě setkáte.

> **POZOR: V tomto kurzu je možné používat pouze zdroje, které popisují standard HTML 5**. Pro úplnost dodávám dva zdroje, kterým se v rámci tohoto kurzu **vyhněte**: [jakpsatweb.cz](http://jakpsatweb.cz), [tvorba-webu.cz](http://www.tvorba-webu.cz). Pokud je někde vyžadováno uvedení zdroje, tyto weby nejsou uznatelné.


### Editor

Pro zpracování části domácího úkolu (psaní HTML dokumentu) budete potřebovat textový editor. *Poznámkový blok*, který máte nainstalovaný, pokud používáte operační systém Windows, vám dovolí začít, ale nic vám neusnadní (a leccos ztíží). 

Proto si nainstalujte textový editor [Sublime Text](https://www.sublimetext.com) (pro vyzkoušení je možné jej používat zdarma po neomezenou dobu).


### A píšeme

Jakmile budete mít nainstalovaný editor, můžete se podívat na tento [článek o psaní stránek v HTML](https://developer.mozilla.org/en-US/Learn/HTML/Write_a_simple_page_in_HTML), který hezky vysvětluje, co obnáší psaní HTML stránky. 

Pokud v této fázi narazíte na problémy, obraťte se s prosbou o radu do předmětového fóra. **Je dovoleno — a doporučováno — si vzájemně pomáhat a radit se.** Dejte si na úkolu dobře záležet — na znalosti HTML podstatně závisí úspěch v závěrečném testu.
