### Spojování řetězců a čísel

Podobně jako při práci v tabulkovém procesoru, potřebujete při psaní skriptů
pracovat s čísly a texty. Často chcete spočítat nějakou hodnotu a pak ji
oznámit ve srozumitelné zprávě.

Řetězce se v javascriptu spojují pomocí operátoru `+`. 

    var text = 'abc' + 'xyz';
    console.log(text); // vypíše do konzole 'abcxyz'
    
Pokud chceme vypsat čísla, funguje to stejně. Pokud začneme řetězcem, čísla se
dále nepřičítají, ale připojují (používá se též slovo „zřetězit“, v angličtině
se užívá termín „concatenation“).

Pokud chceme spočítat nějaký výsledek z více čísel (např. čísla sečíst,
vynásobit atp.), stačí čísla sepnout do závorky. Takto se nejprve provede
obsah závorky a vznikne jediné číslo, které se připojí k řetězci. Tedy např.

    var text = 'abc' + 'xyz' + (24 * 3600);
    console.log(text); // vypíše do konzole 'abcxyz86400'

Většinou nepracujeme přímo s literály, ale spojujeme proměnné. Výsledek pak
může vypadat takto:
  
    var verb = ' uběhlo ';
    var seconds = 3600;
    var text = 'Dnes' + verb + (24 * seconds) + ' sekund.';
    console.log(text); // vypíše do konzole 'Dnes uběhlo 86400 sekund.'
