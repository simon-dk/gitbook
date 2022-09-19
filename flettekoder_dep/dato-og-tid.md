# Dato og tid

{% hint style="danger" %}
#### Disse flettekoder er udgået og bør ikke længere bruges. Vi har beholdt siden indtil alle nuværende kunder er blevet flyttet over på den nye dokumentmotor.
{% endhint %}

## Der kan flettes informationer om tid ind i brevet

```fsharp
{{By}}, den {{dato}}    //København, den 22.03.2020
```

Datofeltet kan for eksempel bruges i footeren som "dette brev er sendt den..." eller hvis man ønsker et mere formelt brev, ude i højre margin:

```aspnet
SKAL VI SÆLGE JERES BOLIG
                                
                                Lyngby d. 22.03.2020
Kære Hans & Grete,

Skal I...
```

Hvis I ønsker en form for tidsbegrænset tilbud, kan I også bruge koderne:

```fsharp
{{1mdr}}    //22.04.2020
{{2mdr}}    //22.05.2020
{{3mdr}}    //22.06.2020
```

{% hint style="info" %}
Koderne \{{1mdr\}} mfl. tillægger antallet af måneder med den dato brevet genereres fra. På den måde kan I lave et tidsbegrænset tilbud der f.eks. løber to måneder fra den nuværende dato.
{% endhint %}

```aspnet
Få en vurdering af {{din}} bolig inden {{2mdr}} og spar kr. 10.000...
//Få en vurdering af jeres bolig inden 22.05.2020 og spar kr. 10.000...
```

{% hint style="info" %}
Se også oplysninger om boligens liggetid under [Udbudsoplysninger](udbudsoplysninger.md)
{% endhint %}

