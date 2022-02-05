# Boligejeren

## Herunder er flettekoder vedrørende boligejere

Flettekoderne til at skrive ejernes fulde navne er hhv. {{Ejer1}} og {{Ejer2}}.

```javascript
{{Ejer1}} // Hans Hansen
```

```javascript
{{Ejer2}} // Grete Hansen
```

Typisk vil navnene blive brugt i adressefeltet, så for ikke at få en tom linje kan man sætte {{Ejer2}} øverst som modtager. Hvis der kun er een ejer, vil adresseringen derved se rigtig ud.

```javascript
{{Ejer2}}              // tom eller Grete Hansen
{{Ejer1}}              // Hans Hansen
{{Adresse}}            // Minvej 5 ST TH
{{Postnummer}} {{By}}  // 2800 Kongens Lyngby
```

Man kan også refererer til ejernes fornavne ved blot at skrive {{Fornavn}}. Hvis der er to ejere skrives der automatisk "&" imellem.

```javascript
Kære {{Fornavn}}, // Kære Hans, 
                  // Kære Hans & Grete,
```
