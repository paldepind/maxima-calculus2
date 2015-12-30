# Maxima Calculus 2

Maxima funktioner til løsning af eksamensopgaver i kurset Calculus 2 på Aarhus Universitet.

## Introduktion

Indlæs filen `main.mac` i Maxima med følgende kommando.

```
batch("main.mac");
```

Afprøv at det virker:

```
criticalPoints(y^2 + 6*x*y + 6*x^2 - 28*y - 66*x + 200)
```

Du skulle nu se output i stil med følgende:

![criticalPoints output](/criticalpoints.png?raw=true)

## Funktioner

### `criticalPoints`

Til løsning af opgavetyper med teksten:

> Gennemfør en undersøgelse af kritiske punkter og en bestemmelse af
arten af disse ved anden- ordenskriteriet (“second derivatives test”).

Funktionen skulle gerne give _alt_ information nødvendigt for
besvarelse.

```
criticalPoints(y^2 + 6*x*y + 6*x^2 - 28*y - 66*x + 200);
```

## `twoVectors`

Til løsning af opgavetyper hvor to vektorer er givet og hvor teksten
er:

> Afstande og projektioner ønskes beregnet.

```
twoVectors([0,1,1],[1,2,3]);
```

## `maclaurin`

Til løsning af opgavetyper med teksten

> Maclaurinrækker i relation til denne funktion beregnes.

Udover funktionen `f(x)` skal `maclaurin` også gives værdien for `F(0)`.

```
maclaurin(x^2 * sin(x), 9);
```