### První kroky s kaskádovými styly

**Práce s CSS**, neboli kaskádovými styly (Cascading Style Sheets) je způsob, 
jak sémantickému HTML dát vizuální podobu. Vracíme se zde k základům, ale 
namísto **obsahu** se teď budeme zabývat **formou**. 

HTML a CSS tvoří (společně s Javascriptem) to, co vidíte na jakékoli webové
stránce – se znalostí obojího již můžete vytvořit velmi pokročilý webový obsah.

**K čemu je to dobré?** Je to podobné, jako byste uměli pracovat v roce 1990 s
textovým editorem a tabulkovým procesorem: umožní vám to jednak lepší
porozumění fungování a potenciálu webu, a též vám to dá základní praktické
dovednosti – ty můžete využít profesionálně, ale i pro vlastní potřebu.

### Jak CSS vypadá?

**CSS popisuje, jak mají vypadat jednotlivé prvky v dokumentu**: odstavce
vypadají takto, nadpisy zase jinak, atp. Prohlédněte si kód v jednotlivých
editorech — vlevo vidíte již známé HTML, následuje CSS a vpravo vidíte výstup.
CSS má jednoduchou strukturu `selektor { vlastnost: hodnota; vlastnost2:
hodnota; … }`. 

Selektor (`p`, `h1`) *vybírá* prvky, na něž chcete aplikovat
pravidlo. Pravidlo se skládá z deklarací, které popisují různé vlastnosti
(např. barvu textu, typ písma anebo šířku obrázku).

Na schématu níže je postupně se konkretizující popis struktury CSS. (Viz též [podobný
popis od W3C](https://www.w3schools.com/css/css_syntax.asp).)

    selektor { sada pravidel }
            ↓
    selektor { deklarace; deklarace; }
            ↓
    selektor { 
      vlastnost: hodnota; 
      vlastnost; hodnota; 
    }
            ↓
    p { 
      color: red;
      font-size: 30px; 
    }
