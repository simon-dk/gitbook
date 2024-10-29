---
description: >-
  Herunder finder du en samlet oversigt over de tilgængelige flettekoder der kan
  benyttes med HelloAgent. Kontakt os gerne hvis du har spørgsmål eller har
  ønsker til tilføjelser.
---

# Samlet oversigt over flettekoder

Herunder findes en samlet oversigt over de flettekoder der kan benyttes i systemet. I tillæg kan alle flette koder benyttes med entent stort forbogstav eller med store bogstaver.&#x20;

{% hint style="info" %}
Alle flettekoder kan skrives som med stort forbogstav eller med caps-lock:

Skriv f.eks. {Din} og systemet ved at der skal stå enten "Din" eller "Jeres" alt efter om der er en eller to ejere.

Ligeledes kan alle flettekoder skrives med STORT.\
Skriv f.eks. {VEJNAVN} for at teksten i brevet skrives som "SKAGENSVEJ"
{% endhint %}

```javascript
/** Modtageroplysninger */
{fornavn}                   // "Hanne" eller "Hanne og Per",
{modtager}                  // Modtagerfelt med navn, adresse og postnummer/by
{modtager_adresse}          // Rådhusvej 5, 1. th
{modtager_vejnavn}          // Rådhusvej
{modtager_husnummer}        // 5
{modtager_etage}            // 1
{modtager_side}             // th
{modtager_supplerende_by}   // Gundsølille
{modtager_postnummer}       // 4000
{modtager_by}               // Roskilde

{#ental}Der er en modtager{/ental} 
//Denne tekst kommer kun med hvis der er en enkelt modtager

{#flertal}Der er flere modtagere{/flertal}   
//Denne tekst kommer kun med hvis der er mere end 1 modtager

/** Adresseoplysninger */
{adresse}               // Skagensvej 4, 1. TH
{vejnavn}               // Skagensvej
{husnummer}             // 4
{etage}                 // 1
{side}                  // TH
{postnummer}            // 9900
{postnr}                // 9900
{by}                    // Skagen
{bynavn}                // Skagen
{postdistrikt}          // Skagen
{supplerendeBynavn}     // Gundsølille

/** Titulering */
{du}                    // "du" eller "I"
{din} 	                // "din" eller "jeres"
{dine} 	                // "dine" eller "jeres"
{dit} 	                // "dit" eller "jeres"
{dig}                   // "dig" eller "jer"

/** Boligen */
{boligtype}             // "ejerlejlighed", "villalejlighed", "villa" osv.
{boligtyper}            // "ejerlejligheder", "villalejligheder", "villaer" osv.
{boligtypen}            // "ejerlejligheden", "villalejligheden", "villaen" osv.
{boligtype_kort}        // "lejlighed", "hus", "sommerhus" osv.
{boligtyper_kort}       // "lejligheder", "huse", "sommerhuse" osv. 
{boligtypen_kort}       // "lejligheden", "huset", "sommerhuset" osv.
{boligareal}            //"174"
{værelser}              //"4"

/** Tid */
{dato}                  //dags dato, f.eks. 14-04-2021      
{"1mdr"}                //dags dato tillagt 1 måned, f.eks. 14-05-2021
{"2mdr"}                //dags dato tillagt 2 måned
{"3mdr"}                //dags dato tillagt 3 måned
{"4mdr"}                //dags dato tillagt 4 måned
{"5mdr"}                //dags dato tillagt 5 måned
{"6mdr"}                //dags dato tillagt 6 måned

/** Afsender */
{forretning_navn}       //Firmaet ApS
{forretning_adresse}    //Kongevejen 123, 2840 Holte
{forretning_email}      //kontakt@firmaet.dk
{forretning_cvr}        //44556677
{forretning_telefon}    //4455 6677

/** Diverse */
Alle ovenstående koder kan skrives med stort forbogstav eller med stort:
{Din}, {Vejnavn} eller {DIN}, {VEJNAVN}, {FORRETNING_NAVN} osv.

Dette giver f.eks.
{Din}                   //"Din" eller "Jeres"
{DIN}                   //"DIN" eller "JERES"
{Vejnavn}               //"Skagensvej" - ingen ændring
{VEJNAVN}               //SKAGENSVEJ

```
