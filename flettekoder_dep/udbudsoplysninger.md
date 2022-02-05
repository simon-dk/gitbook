# Udbudsoplysninger

## Brug oplysninger om det aktuelle udbud

Vi indhenter oplysninger om udbuddet som kan bruges i forskellige sammenhænge.&#x20;

```javascript
{{pris}}                  // 4.500.000
{{liggetid}} 		          // 123
{{liggetid_samlet}}       // 345 (eller 123 hvis boligen ikke har skiftet mægler)
{{liggetid_mdr}}          // 4 (Liggetid nedrundet til nærmeste hele måned, 
                          // f.eks. 145 dage/30 = 4,8 mdr. Afrundes til 4.)

{{ejerudgift}}            // 3.456
{{udbudtHos}}             // Edc, Danbolig mv.


{{prisudvikling}}         // -3%
                          // 4% (hvis prisen er steget)
                    
{{prisudvikling_neutral}} // 3% (minustegn er fjernet)
                          // 4%
```

### Udbudt hos

Vælger I at benytte firmanavnet hos den mægler der har boligen udbudt, bliver det formatteret med stort forbogstav og resten småt. Enkelte mindre forretninger o.l. er muligvis ikke katalogiseret korrekt, så der kan opstå situationer hvor navnet skrives forkert.

### Prisudvikling

Vi har to flettekoder for prisudvikling, en normal {{prisudvikling}} og en {{prisudvikling\_neutral}}.&#x20;

Ved {{prisudvikling}} skrives den samlede udvikling afrundet til nærmeste hele procentsats. Er udviklingen negativ skrives et minustegn foran.

```javascript
Boligen er justeret med {{prisudvikling}}. // Boligen er justeret med -3%.
```

I nogle situationer vil man gerne skrive en sætning som.

```javascript
Jeg kan se at {{du}} har sat prisen ned med {{prisudvikling_neutral}}
//Jeg kan se at I har sat prisen ned med 3%.
```

I den situation kan man bruge {{prisudvikling\_neutral}} da der ellers kan komme til at stå "..I har sat prisen ned med -3%" som vil være forkert.

Begge flettekoder kan med fordel bruges i kombination med [avancerede flettefelter](avancerede-flettekoder.md) og koden {{#afslag}}, så teksten kun vises hvis der reelt har været et afslag.
