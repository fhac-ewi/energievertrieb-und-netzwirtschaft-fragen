# Welchem Zweck dienen Lastprognosen? Diskutieren Sie die Wirkung/Bedeutung der Prognosen im Rahmen des Bilanzkreismanagements. Rekapitulieren Sie hierbei den Bilanzkreis und das Netzzugangsmodell.
**Prognosen** sind Vorhersagen für die Zukunft, die mit einer gewissen Wahrscheinlichkeit eintreten. Je besser die Prognosen sind, desto weniger Abweichungen sind zwischen Prognose und tatsächlichem Lastgang. Die Güte einer Prognose kann nur ex post (im Nachhinein) mit dem tatsächlichen Lastgang bestimmt werden.

Eine **aktive Bewirtschaftung eines Bilanzkreises** meint die Vorhersage der anfallenden Erzeugung und Verbrauch mittels Prognosen und dem Ausgleich der Differenz durch Handel am Energiemarkt. Der Bilanzkreis muss immer ausgeglichen sein. Ist der Bilanzkreis nicht ausgeglichen, oder weichen die tatsächlichen Erzeugungen/Verbräuche von den Prognosen ab, wird (teure) Ausgleichsenergie benötigt.

**Lastprognosen** dienen der aktiven Bewirtschaftung von Bilanzkreisen und **der Vermeidung von Ausgleichsenergie**. Sie werden also auch zur Bestimmung der notwendigen Energiemengen auf dem Handelsmarkt genutzt und der Intradayoptimierung.

TODO Netzzugangsmodell?

# Beschreiben Sie beispielhaft Einflussfaktoren auf das konkrete Lastverhalten von Endkunden. 

Die wesentlichen Einflussfaktoren sind **Technik, Zeit und Umwelt**. Bei Haushaltskunden zusätzlich noch Benutzer (soziales Verhalten).

**Haushaltskunden**
- Soziales Verhalten
- Innen- und Außentemperatur
- Urlaub, Feiertage
- eingesetze Technik (z.B. Kühlschrank)

**Gewerbekunden**
- Innen- und Außentemperatur
- Arbeitszeiten, Feiertage, Betriebsferien
- eingesetze Technik (z.B. Maschinen)
- Produktionsabläufe
- Konjunktur
- Streik

F 8 - 13f.

# Beschreiben Sie die verschiedenen Formen eines Lastmanagements. Diskutieren Sie den Nutzen sowie die Folgen für die Prognose eines markt- bzw. netzdienlichem Lastmanagements.
Es gibt
- Lastverzicht
- Lastverschiebung
- Lasterhöhung
- Sektorenkopplung

Mithilfe dieser Aktionen kann die Last beeinflusst werden. Die Lastveränderungen sind nur in einem gewissen Rahmen möglich. 

Ein **marktdienliches Lastmanagement** wäre es die Last nach dem Strompreis anzupassen. (Niedriger Preis = Hohe Last) 

Ein **netzdienliches Lastmanagement** dient zur Sicherung der Netzfrequenz von 50 Hz.

F 8 - 46

# Angenommen, Sie sind Berater:in für die Energiewirtschaft und sollen bei einem Kunden ein Lastprognoseverfahren einführen. Welchem Kunden empfehlen Sie welche Methodik?
Es gibt verschiedene Lastprognoseverfahren:
- Vergleichstageverfahren
- SLP
- Regression
- Zeitreihenverfahren (statistische Verfahren)
- neuronale Netze

Die Verfahren sind unterschiedlich Komplex und weisen eine unterschiedliche Güte der Prognose auf. Während die einfacheren Verfahren (Vergleichsverfahren, SLP) wenig Daten benötigen und mit relativ geringem Aufwand umgesetzt werden können, benötigen die komplexeren Verfahren eine große Datenbasis und aufwändige Brechnungen. 

Kleinere Unternehmen mit wenig Kunden werden aus Kostengründen eher die einfacheren Verfahren nehmen und höhere Prognosefehler in Kauf nehmen.

Größere Unternehmen mit vielen Kunden können sich hohe Prognosefehler nicht leisten. (Die benötigte Ausgleichsenergie würde viel Geld kosten.) Deshalb sollten diese Unternehmen mehr Geld in die Prognosen investieren und genauere Prognosen erstellen. Aufgrund der Vielzahl an Kunden haben größere Unternehmen auch ausreichend Daten für solche Verfahren vorliegen.

F 8 - 26-39

# Nehmen Sie an, ein Kunde wünscht von Ihnen eine Fahrplanlieferung. Hierzu sollen Sie ein Angebot ausarbeiten. Überlegen Sie sich eine Methodik, um einen „fairen“ Preis (quasi aus Ihrer Sicht Ihr Mindestpreis) für die Lieferung zu finden. 
Annahme: Wir sind Lieferant und der Kunde könnte ein größerer Gewerbekunde sein.

Mit einer mengenneutralen oder wertneutralen Zerlegung würde man die Standardprodukte für den Kunden beschaffen. Diese würden über den heuten bekannten Preis abgerechnet. (Absicherung am Terminmarkt / Kauf eines Forwards)
Die Kosten wären der faire Preis. 

Hinweis: Als Lieferrant könnte man dem Kunden auch einen günstigeren Preis anbieten, sofern dieser risikolos erreicht werden kann. (z.B. Delta Hedging)

# Beschreiben Sie das Konzept einer PreisForwardCurve (PFC). Wie würden Sie herangehen, um eine PFC zu entwickeln. Beschreiben Sie schrittweise und präzise die Vorgehensweise.
Für eine **PreisForwardCurve** wird 
1. Historischen Spotpreisdaten bereinigt (3 Sigma Band, 99.7%) und normiert (auf Intervall 0 bis 1 gebracht)
2. Zusammenhänge/Muster erkennen (z.B. Wochentag zu Stunde im Jahr)
3. Suche nach Zusammenhängen in der FutureCurve
4. Zusammentragen der gefunden Zusammenhänge von historischen Spotpreisen und FutureCurve

Das Ergebnis ist eine Vorhersage für Spotmarktpreise.

> Ziel der PFC wird zum Pricing genutzt und zur Bewertung von Strukturen und Lastgängen.

# Beschreiben Sie alternative andere Vorgehensweisen. Existiert ein objektives Bewertungsmaß? Existiert ein eindeutiger „fairer“ Marktpreis des Fahrplans? Beschreiben Sie weitere Strategien zur Objektivierung.
Es kann kein **fairer Marktpreis** existieren, da die tatsächlichen Preise in Zukunft nicht vorhersagbar sind. Die Preise können höher oder niedriger als in der Prognose vorhergesagt ausfallen.

Bewertungsmaße sind entweder quanititativ, qualitativ oder heuristisch. Nur die quanititativen Bewertungsmaße sind objektiv.

Beispiele für quantitative z.B.
- Mittlerer Fehler
- Quadratische Fehler
- Relativer Fehler
- Relvativer absoluter Fehler



F 8 - 41

# Angenommen, Sie haben den oben skizzierten Fahrplan verkauft. Wie können Sie nun herausfinden, welche Standardprodukte zur Absicherung Ihrer Verkaufsposition sinnvoll wären?
Delta Hedging ist die Antwort auf alles. Die 42 der Energiewirtschaft.

Mittels PFC und Lastgang kann nun der Preis und die Menge der verschiedenen Standardprodukte bestimmt werden. Dadurch kann dann ermittelt werden, welche Produkte in den jeweiligen Zeiträumen benötigt wird. Man versucht die am Spotmarkt beschaffbaren Positionen zu minimieren, entweder Mengenneutral, Wertneutral oder Risikoarm.

- **Mengenneutrale Zerlegung**: zerlege so, dass die Summe aller am Spotmarkt zu beschaffenden Mengen null ist.
- **Wertneutrale Zerlegung**: zerlege so, dass die Summe der Werte der am Spotmarkt zu beschaffenden Mengen null ist. Hierbei ergibt sich der Wert aus dem Produkt aus PFC und Lastgang.
- **Risikominimierende Zerlegung**: zerlege so, dass das Risiko aus der Spotmarktposition minimal wird.

F 8 - 52 und 59
