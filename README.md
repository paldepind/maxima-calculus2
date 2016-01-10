# Maxima Calculus 2

Maxima funktioner til løsning af eksamensopgaver i kurset Calculus 2 på Aarhus Universitet.

## Introduktion

### Maxima i CLI eller Emacs

Indlæs filen `main.mac` i Maxima med følgende kommando.

```
batchload("main.mac");
```

Afprøv at det virker:

```
criticalPoints(y^2 + 6*x*y + 6*x^2 - 28*y - 66*x + 200);
```

Du skulle nu se output i stil med følgende:

![criticalPoints output](/criticalpoints.png?raw=true)

### wxMaxima

Indlæs programmet i wxMaxima ved at vælge `File -> Load Package...`,
find `main.mac` filen og indlæs den.

Afprøv at det virker ved at indtaste

```
criticalPoints(y^2 + 6*x*y + 6*x^2 - 28*y - 66*x + 200);
```

og tryk `Shift-Enter`. Du skulle nu se følgende output:

![criticalPoints output](/wxcriticalpoints.png?raw=true)

## Funktioner

### `gradient`

Til løsning af opgavetyper med teksten

> Der beregnes gradient og retningsafledede.

`gradient` skal gives et udtryk af `x` og `y`, et punkt og en
retning i form af en enhedsvektor.

```
gradient(x^4 + 3*x^3*y^3 + 6*y^2, [-1,2], 1/sqrt(2)*[-1,-1]);
```

![gradient output](/gradient.png?raw=true)

### `gradientAngle`

Tilsvarende `gradient` men for opgaver hvor der stedet for en vektor
gives en vinkel.

```
gradientAngle(11*x^3 + 15*y^2, [1,2], 3*%pi/4);
```

Bemærk at π i Maxima skal skrives som `%pi`.

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

Til løsning af opgavetyper hvor _to_ vektorer er givet og hvor teksten
er:

> Afstande og projektioner ønskes beregnet.

```
twoVectors([0,1,1],[1,2,3]);
```

## `threeVectors`

Til løsning af opgavetyper hvor _tre_ vektorer er givet og hvor teksten
er:

> Afstande og projektioner ønskes beregnet.

```
threeVectors([1,-1,1],[2,3,1],[3,3,2]);
```

## `maclaurin`

Til løsning af opgavetyper med teksten

> Maclaurinrækker i relation til denne funktion beregnes.

Udover funktionen `f(x)` skal `maclaurin` også gives værdien for `F(0)`.

```
maclaurin(x^2 * sin(x), 9);
```

## `calcMatrix`

Til løsning af opgavetyper med teksten

> Der ønskes en redegørelse for egenværdier og egenvektorer.

```
calcMatrix(matrix([1,0,0],[1,9,2],[1,2,9]));
```

![calcMatrix output](/calcmatrix.png?raw=true)

## `unitVecRad`

Beregning af enhedsvektor udfra radianer

``` 
unitVecRad(%pi/3)
```
