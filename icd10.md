### ICD-10 als Wissensquelle

Das digitale Wörterbuch der Augenheilkunde deckt Begriffe einer großen Bandbreite von semantischen Bereichen der Medizin ab. 
Wir konnten während unserer Arbeit am Wörterbuch folgende Kategorien identifizieren:

a) Anatomie (Aufbau des Auges)
b) Pathologie (Erkrankungen des Auges)
c) externe Schädigungen des Auges
d) Behandlungs- und diagnostische Verfahren
e) Instrumente und Apparate in der Augenheilkunde
f) Arzneimittel

Da vor allem Erkrankungen des Auges einen Großteil der Synsets ausmachen lag der Fokus auf potentiellen Wissensdomänen, die diesen Bereich der Augenheilkunde gut abdecken. 
Ausgehend von dieser Überlegung wurde die deutsche Ausgabe der ICD-10 - die internationale Standard-Klassifikation der Krankheiten - in der Version des Jahres 2011 zur Merkmalsextraktion herangezogen. 
Die Tatsache, dass die komplette Klassifikation online in HTML-Form zugänglich ist und Einträge der Klassifikation hierarchisch nach anatomischer Lage geordnet sind, lässt die ICD-10 als ideale Wissensquelle für unsere Zwecke erscheinen, jedoch taten sich Probleme auf, die im Folgenden erläutert werden sollen.

Die automatisierte Merkmalsextraktion setzt am Aufbau der ICD-Notationen an. 
Diese sind nach einem strikten hierarchischen Klassensystem aufgebaut, wie man es von Notationen aus einer Klassifikation kennt. 
So steht z.B. die Klasse H40 für ein Glaukom, während H40.1 konkret für ein primäres Weitwinkelglaukom steht. 
Die Idee besteht nun darin, die Synsets des Wörterbuchs auf die Einträge in der ICD-10 mittels Zeichenkettenvergleich abzubilden (mittels Abgleich von Wörterbuchsynonym und Überschrift des ICD-10-Eintrags), die Klassen der Notation zu identifizieren und diese wiederum auf entsprechende Merkmale abzubilden, wie z.B. Glaukom für H40. 
Identifiziert werden einzelne Einträge der Klassifikation, inklusive Überschrift und Notation, mit regulären Ausdrücken, die einzelne Abschnitte der ICD-10 automatisch erkennen und extrahieren.

Mithilfe der offen gestaltenen Notation soll dann anschließend jedem Synset, dem eine spezifische Notation zugeteilt wurde, zusätzlich alle Merkmale zugewiesen werden, die auch dem Synset der Oberklasse zugeteilt wurden. 
Beispielsweise sollen dem Synset für primäres Weitwinkelglaukom (H40.1) alle Merkmale des Synsets Glaukom (H40), sowie das Merkmal Glaukom selbst zugewiesen werden, ausgehend von der Notation. 
Zusätzlich kann jedem Synset, dem eine Notation als Merkmal zugeordnet wurde, auch das Merkmal Krankheit zugewiesen werden.

In der Praxis scheiterte dieser Ansatz beim Vergleich der Titel der ICD-10-Einträge mit den Benamungen der Wörterbucheinträge. 
Obwohl den Synsets häufig mehrere synonyme Bezeichnungen vergeben wurden, auch z.B. unterschiedliche Schreibweisen, konnten lediglich 43 Synsets aus dem Wörterbuch automatisiert ICD-10-Notationen zugeordnet werden und nur ca. 50 Merkmale (bzw. Notationen) erkannt und vergeben werden, von denen die meisten nur ein einziges Mal vergeben wurden. 
Konkrete Hauptgründe sind die Zusatzinformationen, die bei vielen Krankheiten im Titel standen und ohne manuelles Eingreifen nur schwer zu identifizieren sind, sowie unterschiedliche Wortstellungen bei komplexeren Begriffen. 
Die niedrige Zahl der Merkmalszuweisungen ergibt sich aus der hierarchischen Struktur der ICD-10, da durch die Einteilung in Klassen Überlappungen von Informationen vermieden werden. 
Folglich ist dieses Ergebnis als Grundlage für aussagekräftige formale Verbände in keiner Weise hinreichend und der Ansatz der automatisierten Verarbeitung der ICD-10-Klassifikation wurde nicht weiter verfolgt.
