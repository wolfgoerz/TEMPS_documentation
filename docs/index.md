# TEMPS Dokumentation

For full documentation visit [TEMPS_documentation.org](https://oekoinstitut.github.io/TEMPS_documentation/).


Das am Öko-Institut entwickelte Modell TEMPS (Transport Emissions and Policy Scenarios) ermöglicht die Quantifizierung von Endenergiebedarf und Treibhausgasemissionen des Verkehrs in Deutschland. Die Szenarien können sich in ihren politischen und techno-ökonomischen Rahmenbedingungen unterscheiden. Darüber hinaus lassen sich mit TEMPS Neuzulassungsstruktur und Fahrzeugbestand von Straßenfahrzeugen sowie Verlagerungen in der Verkehrsnachfrage bestimmen.
Im Zentrum des Modells steht die Markthochlaufmodellierung für Straßenfahrzeuge (Pkw, LNF und Lkw) anhand eines umfangreichen Neuzulassungs- und Bestandsmodells. Dieses simuliert die Kaufentscheidung für repräsentative Nutzungsprofile bottom-up mit Hilfe verschiedener technischer, ökonomischer und regulatorischer Bedingungen. Für alle weiteren Verkehrsträger (Schienenverkehr, Schifffahrt, Luftfahrt, Busse, Motorräder, Fahrräder) werden Annahmen über Antriebe und ihre Effizienzentwicklung hinterlegt. 
Regulatorische Rahmenbedingungen und Entwicklungen des Marktes auf nationaler sowie europäischer Ebene werden in allen Szenarien berücksichtigt. Diese drücken sich beispielsweise durch Steuern, Mautgebühren oder Grenzwerte aus. Ebenso beeinflussen globale Trends die Wirtschaftlichkeit der Fahrzeuge, wie zum Beispiel die Entwicklung von Batterie- und Kraftstoffpreisen. Für die Nutzfahrzeuge spielen spielen insbesondere die CO2-Flottenzielwerte, die Lkw-Maut sowie der Ausbau der Lade- und Tankstelleninfrastruktur für alternative Fahrzeugantriebe eine entscheidende Rolle.
Im Folgenden wird die Kaufentscheidung durch Nutzungsprofile, das Neuzulassungsmodell und das Bestandsmodell für Straßenfahrzeuge beschrieben. Daraufhin wird die Verkehrsnachfrage inklusive Verlagerungswirkungen und Energie- und Treibhausgasbilanz erläutert.

## Methodischer Ansatz

TEMPS ist ein Simulationsmodell, welches die Neuzulassungs- und Bestandsstruktur bottom-up berechnet. Anschließend wird der Bestand top-down anhand einer bestehenden Verkehrsnachfrage und den Auslastungsgraden berechnet und die bottom-up berechnete Gesamtflotte mit dem ermittelten Wert kalibriert.  
TEMPS ist für nationale Verkehre ausgelegt. Internationale Verkehre, welche von- oder nach Deutschland gehen, werden ebenfalls modelliert (Personenflugverkehr, Güterflugverkehr, Güterseeverkehr).
Die Modellrechnung erfolgt jahresscharf. Es können Prognosen bis zum Jahr 2050 abgebildet werden. Bei Bedarf kann der Simulationszeitraum verlängert werden.
Die Flotte und die Verkehrsnachfrage werden auf nationaler Ebene ausgegeben. Räumliche inputs sind beim Personenverkehr unterteilt in die Kategorien urban, suburban und ländlich (EuroStaR-Kategorien).





































## Code Annotation Examples
### Codeblocks

Some `code` goes here.

### Plain codeblock

A plain codeblock:

```
Some code here
def myfunction()
// some comment
```

#### Code for a specific language

Some more code with the `py` at the start:

``` py
import tensorflow as tf
def whatever()
```

#### With a title

``` py title="bubble_sort.py"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

#### With line numbers

``` py linenums="1"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

#### Highlighting lines

``` py hl_lines="2 3"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

## Icons and Emojs

:smile: 

:fontawesome-regular-face-laugh-wink:

:fontawesome-brands-twitter:{ .twitter }

:octicons-heart-fill-24:{ .heart }