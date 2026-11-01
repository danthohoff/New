Ich würde den letzten Agendapunkt bewusst entscheidungs- und umsetzungsorientiert gestalten. Ziel ist nicht, am Ende bereits die gesamte Architektur festzulegen, sondern aus den Diskussionen ein gemeinsames Vorgehen mit klaren Verantwortlichkeiten und einem konkreten Startpunkt abzuleiten.

## Letzter Agendapunkt: Next Steps & konkrete Umsetzung

Dauer: ca. 45–60 Minuten

### 1. Ergebnisse und offene Entscheidungen festhalten (10 Min.)

Zunächst die wichtigsten Erkenntnisse aus dem Workshop zusammenführen:

- Welches Zielbild eines HR AI Agent Orchestration Layers verfolgen wir?
- Welche Architekturhypothese wollen wir weiterverfolgen – zentral, föderiert oder hybrid?
- Welche Rolle sollen ServiceNow, Oracle und Microsoft spielen?
- Welche Fähigkeiten müssen zentral bereitgestellt werden?
- Welche Themen sind noch ungeklärt und müssen validiert werden?

Wichtig: Entscheidungen, Arbeitshypothesen und offene Fragen klar voneinander trennen.

### 2. Erste konkrete Use Cases auswählen (10 Min.)

Wir sollten nicht mit dem Bau einer Plattform starten, sondern mit einem konkreten Anwendungsfall, an dem sich die Architektur überprüfen lässt.

Mein Vorschlag: Ein systemübergreifender HR-Prozess mit:

- ServiceNow als Einstiegspunkt,
- Oracle als Daten- bzw. Aktionssystem,
- einem HR-Wissensagenten,
- mindestens zwei miteinander interagierenden Agenten,
- einer menschlichen Freigabe,
- durchgängiger Überwachung und Nachvollziehbarkeit.

Diesen Use Case könnten wir später als Proof of Concept nutzen.

### 3. PoC und Architekturvalidierung definieren (10–15 Min.)

Gemeinsam festlegen, was wir konkret testen wollen:

| Dimension      | Leitfrage                                                        |
| -------------- | ---------------------------------------------------------------- |
| Orchestrierung | Können Agenten verschiedener Plattformen zusammenarbeiten?       |
| Integration    | Wie funktionieren APIs, MCP und A2A?                             |
| Kontext        | Wie werden Kontext und Prozesszustand übergeben?                 |
| Governance     | Wie werden Identitäten, Berechtigungen und Freigaben gehandhabt? |
| Monitoring     | Können wir die gesamte Agenteninteraktion nachvollziehen?        |
| Skalierbarkeit | Lässt sich das Muster auf weitere HR-Prozesse übertragen?        |

Empfehlung: Nicht direkt mehrere vollständige Plattformen bauen. Lieber zwei bis drei Architekturvarianten anhand desselben Use Cases vergleichen, insbesondere Microsoft Foundry/Agent Framework und eine föderierte Variante mit nativen ServiceNow- und Oracle-Agenten. LangGraph kann als technische Vergleichsoption hinzukommen.

### 4. Arbeitspakete und Verantwortlichkeiten festlegen (10–15 Min.)

Ich würde die nächsten Aktivitäten in sechs Arbeitspakete aufteilen:

| Arbeitspaket    | Inhalt                                            | Mögliche Verantwortung        |
| --------------- | ------------------------------------------------- | ----------------------------- |
| Zielarchitektur | Zielbild und Architekturprinzipien konkretisieren | Enterprise Architecture       |
| Plattformen     | ServiceNow, Microsoft, Oracle und AWS bewerten    | IT / Plattformverantwortliche |
| Integration     | APIs, MCP, A2A, Events und Integration Layer      | Integration Architecture      |
| Governance      | Security, Identity, Monitoring, Agent Registry    | Security / Architecture       |
| HR Use Cases    | Prozesse und geeignete Pilotfälle auswählen       | HR / Process Owner            |
| PoC             | Technische Umsetzung und Evaluation               | IT / AI Engineering           |

Dabei sollte für jedes Arbeitspaket ein konkreter Owner benannt werden – nicht nur eine Organisationseinheit.

### 5. Roadmap und nächste Termine vereinbaren (5–10 Min.)

Zum Abschluss einen realistischen Startplan festlegen.

1. Innerhalb von 1–2 Wochen: Ergebnisse konsolidieren

   Architekturhypothese, offene Fragen, Use Case und Verantwortlichkeiten dokumentieren.
2. Innerhalb von 3–4 Wochen: Architektur und Plattformen validieren

   Technische Deep Dives mit ServiceNow, Microsoft und Oracle; Integrations- und Governance-Anforderungen klären.
3. Innerhalb von 4–6 Wochen: PoC vorbereiten

   Use Case, Architekturvariante, technische Komponenten, Ressourcen und Erfolgskriterien festlegen.
4. Anschließend: PoC durchführen und Zielarchitektur schärfen

   Erkenntnisse bewerten und daraus eine belastbare Umsetzungsroadmap ableiten.

## Was am Ende des Workshops vorliegen sollte

Ich würde auf sechs konkrete Ergebnisse bestehen:

1. Gemeinsames Zielbild: Ein abgestimmtes Verständnis des HR AI Agent Orchestration Layers.
2. Architekturhypothese: Eine bevorzugte Richtung, die weiter validiert wird.
3. Priorisierter Pilot-Use-Case: Ein konkreter systemübergreifender HR-Prozess.
4. PoC-Auftrag: Was genau wird getestet und anhand welcher Kriterien?
5. Verantwortlichkeiten: Benannte Owner für die zentralen Arbeitspakete.
6. Roadmap: Konkrete nächste Schritte mit Terminen und einem Folgetermin.

## Meine Empfehlung für die Moderation

Ich würde den Agendapunkt mit einer zentralen Frage eröffnen:

> „Was müssen wir in den nächsten 6–8 Wochen konkret tun, damit aus unserem Zielbild ein erster funktionierender HR Agent Orchestration Layer entstehen kann?“

Und mit einer verbindlichen Abschlussrunde beenden:

- Was ist unser erster konkreter Schritt?
- Wer übernimmt die Verantwortung?
- Bis wann liefern wir ein Ergebnis?
- Welche Entscheidung oder Unterstützung benötigen wir dafür?

Mein wichtigster Hinweis: Der Workshop sollte nicht mit dem Auftrag enden, eine umfassende Orchestrierungsplattform zu bauen. Besser ist ein klar abgegrenzter Auftrag, einen ersten systemübergreifenden HR-Agentenprozess umzusetzen und dabei die wesentlichen Architekturentscheidungen praktisch zu validieren. So entsteht aus der strategischen Diskussion ein belastbarer Einstieg in die Umsetzung.