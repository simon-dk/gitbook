# Avancerede flettekoder

{% hint style="danger" %}
#### Disse flettekoder er udgået og bør ikke længere bruges. Vi har beholdt siden indtil alle nuværende kunder er blevet flyttet over på den nye dokumentmotor.
{% endhint %}

## Avancerede flettekoder giver flere muligheder

Disse flettekoder er sværere at bruge da man skal tage højde for flere forskellige udfald. Vi hjælper gerne til med at formulerer budskaberne så der ikke opstår fejl i brevene.

### Struktur

De avancerede flettekoder ser anderledes ud end normale flettekoder. Herunder er et eksempel

```javascript
{{#afslag}}Denne tekst kommer med, hvis der har været prisafslag!{{/afslag}}
// Denne tekst kommer med, hvis der har været prisafslag!
```

Så i stedet for et enkelt ord inden i en tuborg, så har man nu en start tuborg \{{#START\}} og en slut tuborg \{{/SLUT\}}.

Al teksten imellem kommer med, inklusive linjeskift mv.

### Formål

Ideen bag de avancerede flettekoder er, at man kan skrive en særskilt tekst, _hvis et givent forhold er opfyldt._ Det vil sige at sætningen inden imellem flettekoden kun, hvis et bestemt kriterie er opfyldt.

Det kan for eksempel være, at man vil have en særlig tekst med, hvis en bolig har været sat ned i pris. Det kan se således ud:

```javascript
Når boligen har været sat ned i pris, {{#afslag}}kommer denne tekst med!{{/afslag}}
// Når boligen har været sat ned i pris, kommer denne tekst med!
```

{% hint style="info" %}
Avancerede flettekoder kan indeholde enkelte ord, sætninger, hele paragraffer eller endda en hel side.
{% endhint %}

#### De avancerede flettekoder

Der kan i øjeblikket benyttes følgende avancerede flettekoder:

{% code title="Ved prisaflsag" %}
```javascript
{{#afslag}}Denne tekst kommer med, hvis der har været prisafslag{{/afslag}}
```
{% endcode %}

{% code title="Når boligen har haft skiftet mægler" %}
```javascript
{{#skiftetMaegler}}Denne tekst kommer med når boligen
har været udbudt ved mere end 1 mægler.{{/skiftetMaegler}}

// NOTE
// Vi tager udgangspunkt i at hvis en bolig har en samlet liggetid der er mere
// end 30 dage længere end den nuværende liggetid, f.eks. 140/220, så har 
// boligen været udbudt ved mere end 1 mægler. Ved 140/145 aktiveres koden
// f.eks. ikke.
```
{% endcode %}

{% code title="Ved forskellige boligtyper" %}
```javascript
{{#villa}}Tekst vises hvis boligtypen er villa..{{/villa}}
{{#raekkehus}}Tekst vises hvis boligtypen er rækkehus..{{/raekkehus}}
{{#ejerlejlighed}}Tekst vises hvis boligtypen er ejerlejlighed..{{/ejerlejlighed}}
{{#landejendom}}Tekst vises hvis boligtypen er landejendom..{{/landejendom}}
{{#fritidshus}}Tekst vises hvis boligtypen er fritidshus..{{/fritidshus}}fsla
```
{% endcode %}

{% code title="Ved antal sælgere" %}
```javascript
{{#ental}}Denne tekst kommer med hvis der er een sælger.{{/ental}}
{{#flertal}}Denne tekst kommer med hvis der er flere sælgere.{{/flertal}}
```
{% endcode %}

{% code title="Dødsbo / ikke dødsbo" %}
```javascript
{{#doedsbo}} Hvis boligejeren er afdød {{/doedsbo}}
{{ikke_doedsbo}} Hvis boligejeren er nulevende{{/ikke_doedsbo}}
```
{% endcode %}

### Bland normale flettekoder ind i avancerede flettekoder

En af de smarte funktioner ved avancerede flettekoder er, at man kan indsætte _normale_ flettekoder inden i. Så man kan stadig har \{{du\}} osv. i sine tekster som genereres af avancerede flettekoder.

```javascript
Jeg har bemærket at {{din/dit}} {{boligtype}} 
har stået til salg i {{liggetid_samlet}} dage 
{{#afslag}}og er sat ned med {{prisudvikling_neutral}} i alt{{/afslag}}, så 
måske overvejer {{du}} nu hvad der så skal ske..

//RESULTAT hvis boligen IKKE har været sat ned i pris
Jeg har bemærket at dit rækkehus
har stået til salg i 345 dage, så 
måske overvejer du nu hvad der så skal ske..

//RESULTAT hvis boligen har været sat ned i pris
Jeg har bemærket at dit rækkehus
har stået til salg i 345 dage og er sat ned med 3 % i alt, så 
måske overvejer du nu hvad der så skal ske..
```

### Dødsbo / ikke dødsbo

Som udgangspunkt frasorterer vi breve hvis ejeren er afdød, men i situationer hvor man ønsker alligevel at sende et brev, f.eks. til de efterladte, kan det gøres ved at bruge flettekode \{{#doedsbo\}} \{{/doedsbo\}}.&#x20;

Man laver reelt to hele breve i samme skabelon og samler hvert brev med hhv. \{{#doedsbo\}} og \{{#ikke\_doedsbo\}}. På den måde kommer det korrekte brev frem alt efter situationen.

```javascript
{{#ikke_doedsbo}}Heri skrives hele ens normale brev
inklusive nye linier...

Afsender mm.{{/ikke_doedsbo}}

{{#doedsbo}}Heri skrives så brevet der sendes til boets
efterladte. 
inklusive nye linier...

Afsender mm.{{/doedsbo}}

```
