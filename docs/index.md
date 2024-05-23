# TEMPS Dokumentation

For full documentation visit [TEMPS_documentation.org](https://oekoinstitut.github.io/TEMPS_documentation/).

## 1 Kurze Einführung in das Modell TEMPS

Das am Öko-Institut entwickelte Modell TEMPS (Transport Emissions and Policy Scenarios) ermöglicht die Quantifizierung der Entwicklung von Endenergiebedarf und Treibhausgasemissionen des Verkehrs in Deutschland. Die Szenarien berücksichtigen unterschiedliche politische und techno-ökonomischen Rahmenbedingungen und können die Wirkung einzelner Politikinstrumente ermitteln. Darüber hinaus lassen sich mit TEMPS die Entwicklung der Neuzulassungsstruktur und des Fahrzeugbestandes von Straßenfahrzeugen sowie Verlagerungen der Verkehrsnachfrage bestimmen.

Im Zentrum des Modells steht die Markthochlaufmodellierung für Straßenfahrzeuge (Pkw, LNF und Lkw) anhand eines umfangreichen Neuzulassungs- und Bestandsmodells. Dieses simuliert die Kaufentscheidung für repräsentative Nutzungsprofile „bottom-up“ unter Berücksichtigung verschiedener technischer, ökonomischer und regulatorischer Bedingungen. Für alle weiteren Verkehrsträger (Schienenverkehr, Schifffahrt, Luftfahrt, Busse, Motorräder, Fahrräder) werden Annahmen über Antriebe und ihre Effizienzentwicklung hinterlegt. 

Regulatorische Rahmenbedingungen und Entwicklungen des Marktes auf nationaler sowie europäischer Ebene werden in allen Szenarien berücksichtigt. Diese drücken sich beispielsweise durch Steuern, Mautgebühren oder Grenzwerte aus. Ebenso beeinflussen globale Trends die Wirtschaftlichkeit der Fahrzeuge, wie zum Beispiel die Entwicklung von Batterie- und Kraftstoffpreisen. Für die Nutzfahrzeuge spielen insbesondere die CO<sub>2</sub>-Flottenzielwerte, die Lkw-Maut sowie der Ausbau der Lade- und Tankstelleninfrastruktur für alternative Fahrzeugantriebe eine entscheidende Rolle.


## 2 Methodischer Ansatz

TEMPS ist ein Simulationsmodell, das „bottom-up“- und „top-down“-Ansätze miteinander kombiniert. Zunächst wird die Neuzulassungs- und Bestandsstruktur von Pkw und Lkw für rund 2400 Nutzungsprofilen „bottom-up“ basierend auf einem TCO-Modell (Total Costs of Ownership) berechnet. Bei der Antriebswahl für Pkws werden darüber hinaus nicht-ökonomische Verhaltensweise über ein kalibriertes Logit-Modell berücksichtigt. Anschließend werden ermittelte Kennzahlen „top-down“ anhand von u.a. der Verkehrsnachfrage und Energiebilanzdaten sowie weiteren Ist-Daten kalibriert. Die Kalibrierung und das kontinuierliche Nachführen der Ist-Daten stellt eine Kurzfristvalidierung der Modellierung sicher. Das Modell betrachtet die Verkehrsemissionen in Deutschland nach Sektordefinition des Klimaschutzgesetzes. Berücksichtigt wird die Verkehrsleistung nach dem Inlandsprinzip, der Fahrzeugbestand nach dem Inländerprinzip. Internationale Verkehre, welche von- oder nach Deutschland gehen, werden ebenfalls modelliert (Personenflugverkehr, Güterflugverkehr, Güterseeverkehr).

Die Modellrechnung erfolgt jahresscharf. Es können Prognosen bis zum Jahr 2050 abgebildet werden. Bei Bedarf kann der Simulationszeitraum verlängert werden. Die Szenarioergebnisse werden auf nationaler Ebene ausgegeben. Modellintern werden teilweise räumlich differenzierte Daten verarbeitet, z.B. Personenverkehr unterteilt in die Kategorien urban, suburban und ländlich.

TEMPS besitzt Schnittstellen zu den Modellen PowerFlex und der Energiemodellierung ENUSEM des Öko-Instituts wodurch Wechselwirkungen mit dem Strommarkt abgebildet und Flexibilitätspotenziale der E-Mobilität berücksichtigt werden können. Darüber hinaus besteht eine Schnittstelle zu dem Verteilungswirkungsmodell DhoT (Dynamic Household Transport (microsimulation) Model) des Öko-Instituts sowie einer öknomischen Folgenabschätzung.


## 3 Nutzungsprofile und Fahrzeugkonfigurationen

Die Modellierung der Neuzulassungen von Pkw und Lkw basiert auf einem „bottom-up“-Ansatz, indem die Kaufentscheidung von insgesamt rund 2400 Nutzungsprofilen abgebildet wird. Die Gesamtheit der Nutzungsprofile bildet das Fahrverhalten der Bevölkerung im Motorisiertem Individualverkehr (MIV) bzw. der Logistikunternehmen im Güterverkehr repräsentativ ab.

Jedes Nutzungsprofil wird durch fünf Merkmale charakterisiert:
*	Größenklasse des Fahrzeugs 
*	Art des Halters (privat, gewerblich, dienstwagennutzend, carsharing)
*	Regionstyp des Halters (innenstadt, städtisch, ländlich)
*	Jahresfahrleistung
*	Haltedauer

Die Nutzungsprofile im MIV basieren auf dem „Mobilitätspanel“ (MOP) (Ecke et al. 2021) und der Studie „Mobilität in Deutschland 2017“ (Nobis und Kuhnimhof 2018). Für Lkw und LNF beruhen die Profile auf der Studie „Kraftfahrzeugverkehr in Deutschland 2010“ (Bundesministerium für Verkehr und digitale Infrastruktur (BMVI) 2010) und der Fahrleistungserhebung 2014 (Bäumer et al. 2017; Bundesanstalt für Straßenwesen (BASt) 2015).

Jedem Nutzungsprofil stehen – soweit auf dem Markt erhältlich – Fahrzeuge in den jeweiligen Größenklassen mit verschiedenen Antrieben und Effizienzen zur Verfügung. In Tabelle 1 sind die möglichen Antriebe für Pkw und Lkw dargestellt, die sich auf verschiedene Größenklassen verteilen (Tabelle 2).  
  

<table>
  <caption align="left">Tabelle 1: Mögliche Antriebsoptionen in TEMPS</caption>
  <thead>
    <tr>
      <th>Pkw</th>
      <th>Lkw</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Diesel</td>
      <td>Batterieelektrische Oberleitungs-Lkw (O-BEV)</td>
    </tr>
    <tr>
      <td>Plug-In Hybrid (PHEV)</td>
      <td>Batterieelektrischer Antrieb (BEV)</td>
    </tr>
    <tr>
      <td>Batterieelektrischer Antrieb (BEV)</td>
      <td>Erdgasantrieb (LNG)</td>
    </tr>
    <tr>
      <td>Flüssiggasantrieb (LPG)</td>
      <td>Brennstoffzellenantrieb (FCEV)</td>
    </tr>
    <tr>
      <td>Erdgasantrieb (CNG)</td>
      <td></td>
    </tr>
    <tr>
      <td>Brennstoffzellenantrieb (FCEV)</td>
      <td></td>
    </tr>
  </tbody>
</table>


<table>
  <caption align="left">Tabelle 2: Größenklassen für Pkw und Lkw</caption>
  <thead>
    <tr>
      <th>Pkw</th>
      <th>Lkw</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Klein</td>
      <td>Lkw von 3,5 bis 7,49 t</td>
    </tr>
    <tr>
      <td>Mittel</td>
      <td>Lkw von 7,5 bis 11,99 t</td>
    </tr>
    <tr>
      <td>Groß</td>
      <td>Lkw ab 12 t</td>
    </tr>
    <tr>
      <td>Leichte Nutzfahrzeuge (LNF)</td>
      <td>Last- und Sattelzüge</td>
    </tr>
  </tbody>
</table>

Für jedes Fahrzeugmodell (definiert über Größenklasse und Antrieb) stehen jährlich verschiedene Kombinationen aus Antriebseffizienz und entsprechendem Anschaffungspreis zur Auswahl. Die Herleitung dieser Kombinationen basiert auf Kostenkurven (Quelle EU IA?).  Zudem werden laufend aktualisierte Prognosen für Batteriekosten berücksichtigt.


## 4 Neuzulassungsmodell

### 4.1 TCO (Total Costs of Ownership)
Die Bestimmung der Kaufentscheidung eines Nutzungsprofils erfolgt in mehreren Schritten. Anhand einer TCO-Rechnung (Total Cost of Ownership) werden für jedes Nutzungsprofil die Vollkosten aller verfügbaren Fahrzeugmodelle berechnet. Die berücksichtigten Kostenkomponenten sind in Tabelle 3 gezeigt und werden im Folgenden näher beschrieben. 

<table>
  <caption align="left">Tabelle 3: Kostenbestandteile der TCO</caption>
  <thead>
    <tr>
      <th>Investitionskosten</th>
      <th>Laufende Kosten</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Anschaffungspreis</td>
      <td>Kraftstoffkosten (inkl. Energiesteuern)</td>
    </tr>
    <tr>
      <td>Kaufförderung*</td>
      <td>Fixkosten (Kfz-Steuer und Versicherung)</td>
    </tr>
    <tr>
      <td>Steuerersparnis* durch Abschreibung<br>für gewerbliche Nutzungsprofile</td>
      <td>Maut (optional)</td>
    </tr>
    <tr>
      <td>Restwert*</td>
      <td>THG-Prämie*</td>
    </tr>
    <tr>
      <td>Malus (optional)</td>
      <td>Sonstige variable Kosten<br>(Wartung, Reparatur etc.)</td>
    </tr>
  </tbody>
</table>
**Gutschrift* (testen klappt das hier mit italic?!)

Die Literatur zeigt, dass private Fahrzeugkäufer meist nicht die langfristigen Kosten der Fahrzeughaltung und -nutzung berücksichtigen, es findet also eine gedankliche Abzinsung statt (Mock 2010). Es wird angenommen, dass die privaten Pkw-Käufer für ihre Kaufentscheidung nur die ersten drei Jahre zu Grunde legen und für zukünftige Zahlungen eine Diskontrate von 5 % anwenden.
Bei Lkw hingegen spielt die gesamte Haltedauer eine entscheidende Rolle für die Wirtschaftlichkeit eines Fahrzeugs und wird als Grundlage der Kaufentscheidung herangezogen. Aufgrund ihrer hohen Fahrleistung liegen die Haltedauern bei Lkw deutlich niedriger als bei Pkw. Diese liegen nach einer standardisierten Online-Befragung von Transportunternehmen im Frühjahr 2021 (Öko-Institut; Hochschule Heilbronn 2022) zwischen 3-9 Jahren. Zusätzlich wird bei allen gewerblichen Haltern die Abschreibung berücksichtigt, welche mindernd auf die Unternehmenssteuern wirkt. Dabei werden ein Unternehmenssteuersatz von 30 % und eine Abschreibungsdauer von 9 Jahren zu Grunde gelegt.

#### 4.1.1 Anschaffungspreis 
Der Anschaffungspreis ergibt sich, wie in 3 beschrieben, direkt aus den Kostenkurven der Fahrzeuge und berücksichtigt aktuelle Batteriepreisprognosen. Er fällt zum Kaufzeitpunkt an und geht daher nicht diskontiert in die TCO ein.

#### 4.1.2 Restwerte(!! ab hier noch nicht aktuell)
Der Restwert eines Fahrzeugs geht zum Ende der Haltedauer als Erlös in die TCO ein. Basierend auf Daten zur Restwertentwicklung von Fahrzeugen mit Verbrennungsmotoren wurde eine Regressionskurve abgeleitet, die den Restwert eines Fahrzeugs unter Berücksichtigung des Kaufpreises, der Laufleistung und des Fahrzeugalters bestimmt. Für das Modell wurde eine Regressionskurve des Statistischen Bundesamtes verwendet (Dexheimer 2003).  Die Gleichung lautet:



































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
