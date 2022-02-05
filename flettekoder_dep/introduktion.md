---
description: >-
  Nedenstående flettekoder benyttes til sælgerbreve. Sælgerbrevene vil i 2021
  overgå til en ny flettemotor, så disse koder vil blive opdateret/udgår på
  sigt.
---

# Introduktion

## Hvad er flettekoder?

Flettekoder er et _felt_ der indsættes i en tekst. Ved at indsætte en flettekode ved programmet, at her skal flettekoden erstattes med en anden værdi, f.eks. et navn.

Flettekoder gør det muligt at lave tekster der er personlige, da man kan indsætte værdier dynamisk.&#x20;

```javascript
Hej, mit navn er {{Navn}}.
```

{% hint style="info" %}
Flettekoder står altid skrevet inden imellem to tuborg tegn: {{her-er-en-flettekode}}.\
\
Tryk Alt + Shift + 8 for "{"\
eller Alt + Shift + 9 for "}"
{% endhint %}

Flettekoder er desuden tegn-sensitive, dvs. man skal skrive korrekt stort/småt for at koderne virker.Hvis man har tastet en flettekode forkert vil der være et "tomt" ord der hvor flettekode skulle have stået.

```javascript
Hej, mit navn er {{navn}}. // Hej, mit navn er .
Hej, mit navn er {{Navn}}. // Hej, mit navn er Simon.
```

Selve koderne, altså det der står imellem tuborg-tegnene, er nogle vi genererer. I oversigten ude til venstre kan du se alle de tilgængelige flettekoder.

Generelt er flettekoderne skrevet på en måde, så man kan skrive sine tekster så normalt som muligt. Der er dog flettekoder der ikke er nemme at huske eller bruge, men vi tilpasser løbende så det bliver så brugervenligt som muligt.

```javascript
Hej {{Fornavn}}, jeg kan se at du har haft din {{boligtype}} på {{Adresse}} 
til salg i {{liggetid}} dage.
```

