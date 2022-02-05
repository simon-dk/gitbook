# Du, din, dig..

## Brug den korrekte tiltale

For at undgå statiske og upersonlige breve, er det vigtigt at modtageren får en fornemmelse af at det er skrevet lige præcis til dem. Det kan bl.a. gøres ved at tage højde for om der er en eller flere modtagere.

{% hint style="info" %}
Alle flettekoder målrettet modtageren skrives i enkeltform, {{du}} og med stort eller småt alt efter om det er i begyndelsen af en tekst eller ej.
{% endhint %}

```javascript
Skal {{du}} have solgt {{din}} bolig.. // Skal du have solgt din bolig
                                       // Skal I have solgt jeres bolig
                                       
{{Du}} kan få en gratis vurdering af {{din}}..
                                       // Du kan få en gratis vurdering af din..
                                       // I kan få en gratis vurdering af jeres..
```

Husk altid at skrive i _**ental**_. Systemet vælger autoamtisk den korrekte tiltale alt efter om der er en eller flere sælgere.

De tiltaler der kan bruges er:

```javascript
{{du}} 		// "du" eller "I"
{{din}} 	// "din" eller "jeres"
{{dine}} 	// "dine" eller "jeres"
{{dit}} 	// "dit" eller "jeres"
{{dig}} 	// "dig" eller "jer"

{{Du}} 		// "Du" eller "I"
{{Din}} 	// ”Din" eller "Jeres"
{{Dine}} 	// "Dine" eller "Jeres"
{{Dit}} 	// "Dit" eller "Jeres"
{{Dig}} 	// "Dig" eller "Jer"

```

### Din, dit, jer, jeres

Der er situationer hvor tiltalen ændrer sig alt efter boligtypen, f.eks. i en sætning som:

```javascript
Jeg har bemærket at {{din}} {{boligtype}}.. 
                                // Jeg har bemærket at din villa..
                                // Jeg har bemærket at din rækkehus..
                                // Jeg har bemærket at jeres rækkehus..
```

{% hint style="info" %}
I situation nummer 2 skrives teksten forkert fordi {{din}} ikke længere er den rigtige tiltale når der er en enkelt sælger og boligtypen er et rækkehus.&#x20;
{% endhint %}

For at ændre på det kan I bruge flettekoderne {{Din/Dit}} samt {{din/dit}}.

```javascript
Jeg har bemærket at {{din/dit}} {{boligtype}}.. 
                                // Jeg har bemærket at din villa..
                                // Jeg har bemærket at dit rækkehus..
                                // Jeg har bemærket at jeres rækkehus..

{{Din/Dit}} {{boligtype}}..
                                // Din villa..
                                // Dit rækkehus..
                                // Jeres rækkehus..
```

