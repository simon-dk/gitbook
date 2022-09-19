# Boligen

{% hint style="danger" %}
#### Disse flettekoder er udgået og bør ikke længere bruges. Vi har beholdt siden indtil alle nuværende kunder er blevet flyttet over på den nye dokumentmotor.
{% endhint %}

## Flettekoder der omhandler selve boligen&#x20;

Vi har en række flettekoder der kan bruges om boligen.

{% hint style="info" %}
Vær opmærksom på at der er flettekoder både med store og små bogstaver for at give mest mulig fleksibilitet.
{% endhint %}

{% code title="Boligen" %}
```java
{{Adresse}}    // Minvej 5 ST TH
{{Postnummer}} // 2800
{{By}}         // Kongens Lyngby   
{{boligareal}} // 120
{{vaerelser}}  // 5

{{Boligtype}}  // Boligtypen med stort
{{boligtype}}  // Boligtypen med småt
{{Boligtyper}} // Boligtypen i flertal, med stort
{{boligtyper}} // Boligtypen i flertal, med småt
{{boligtypen}} // Boligtypen som "villaen", "ejerlejligheden" osv. med småt
```
{% endcode %}

### Boligtype, boligtype, boligtyper...

En boligs _type_ kan skrives på mange måder. "Villa". En "villa", flere "villaer". Vi bruger som udgangspunkt de fulde boligtyper, dvs.:

```java
{{Boligtype}}   // Villa
                // Rækkehus
                // Ejerlejlighed
                // Landejendom
                // Fritidshus
```

```java
{{boligtyper}}  // villaer
                // rækkehuse
                // ejerlejligheder
                // landejendomme
                // fritidshuse
```

Hvis I skal bruge mere fleksibilitet, f.eks. hvis der skal stå "jeg har set at dit _hus",_ så kan dette gøres med avancerede flettefelter som beskrives senere. Vi hjæper gerne med opsætning.

{% hint style="info" %}
Skal du skrive din eller dit før boligtypen, f.eks. "din villa" eller "dit rækkehus", så bruge fletteordet \{{din/dit\}} som du finder under fanen [Du, din, dig...](du-din-dig...md)\
\
Det tager automatisk højde for hvor mange boligsælgere der er, og hvilken boligtype der kommer efter ordet. På den måde skriver den automatisk "din villa", "jeres ejerlejlighed" eller "dit rækkehus" alt efter situationen. Smart!
{% endhint %}

\
