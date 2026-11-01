Sehr gerne. Ich würde den zweiten Agenda-Punkt sogar noch etwas erweitern, denn aus meiner Sicht entscheidet sich hier, ob euer Orchestrator später tatsächlich in der HR-Prozesslandschaft funktioniert oder nur eine technische Plattform bleibt, die Agenten aufrufen kann.

Der erste Agenda-Punkt beantwortet im Wesentlichen die Frage:

Wie soll unsere Agenten-Orchestrierungsarchitektur grundsätzlich aussehen?

Der zweite Agenda-Punkt sollte dagegen beantworten:

Was müssen wir organisatorisch, fachlich und technisch tun, damit Agenten zuverlässig in unseren HR-Prozessen arbeiten können?

Dabei würde ich eure vier ursprünglichen Vertiefungsthemen beibehalten:
1. Agenten in HR-Prozesse integrieren
2. Agenten monitoren und steuern
3. Einen geeigneten Integration Layer aufbauen
4. Eine HR-Ontologie und semantische Architektur entwickeln
Ich würde allerdings drei weitere Themen ergänzen, die ich für eine produktive HR-Agentenlandschaft für ausgesprochen wichtig halte:
5. Identity, Security, Datenschutz und Human-in-the-Loop
6. Testing, Qualitätssicherung und Agenten-Evaluation
7. Betrieb, Resilienz und Lifecycle Management
Warum diese Ergänzungen? Weil ihr nicht nur Agenten technisch miteinander verbinden wollt. Ihr wollt ihnen perspektivisch ermöglichen, in teilweise sensiblen HR-Prozessen Aufgaben zu übernehmen und Aktionen in produktiven Systemen auszuführen.

Dafür braucht ihr neben einer guten Orchestrierung vor allem ein belastbares Betriebs- und Kontrollmodell.
1. Überblick: Die sieben Vertiefungsthemen
Deep Dive – HR Agentic Architecture
1. Process Integration & Agentic Process Design
   
   Wie werden Agenten sinnvoll in bestehende und zukünftige HR-Prozesse eingebunden?
2. Agent Observability & Monitoring
   
   Wie überwachen, analysieren und steuern wir die Performance und Qualität unserer Agenten?
3. Integration Layer & Enterprise Connectivity
   
   Wie verbinden wir Agenten, Plattformen, HR-Systeme, APIs und Datenquellen?
4. HR Ontology & Semantic Layer
   
   Wie schaffen wir ein gemeinsames fachliches Verständnis über unsere Systemlandschaft hinweg?
5. Identity, Security & Human-in-the-Loop
   
   Wie stellen wir sicher, dass Agenten nur das dürfen, was sie dürfen, und kritische Aktionen kontrolliert erfolgen?
6. Agent Evaluation & Quality Engineering
   
   Wie testen und bewerten wir Agenten, bevor und nachdem sie produktiv eingesetzt werden?
7. Operations, Resilience & Lifecycle
   
   Wie betreiben, versionieren, aktualisieren und skalieren wir unsere Agentenlandschaft?

Mein Vorschlag: Für jeden Themenblock entwickelt ihr ein Zielbild, konkrete Anforderungen, Architekturentscheidungen und offene Handlungsfelder.

Ich würde die sieben Themen nicht alle gleich stark gewichten. Gerade für eure aktuelle Situation sind die Themen 1, 3, 5 und 6 besonders wichtig. Monitoring und Lifecycle Management müssen allerdings von Anfang an architektonisch mitgedacht werden.

2. Thema 1: Agenten in HR-Prozesse integrieren
Sehr hohe Priorität
Das ist für mich das wichtigste Vertiefungsthema.

Denn ich vermute, dass ihr aktuell viele Initiativen habt, die einzelne Agenten entwickeln oder deren Potenzial untersuchen. Was dabei häufig fehlt, ist die übergreifende Betrachtung:

Wie wird aus einem einzelnen Agenten eigentlich ein sinnvoller Bestandteil eines Ende-zu-Ende-HR-Prozesses?

Ein Agent kann fachlich hervorragend funktionieren und trotzdem keinen wirklichen Mehrwert liefern, wenn er nicht sinnvoll in den Prozess eingebettet ist.
2.1 Grundsätzliches Verständnis: Agentic Process Design
Ich würde zunächst ein gemeinsames Verständnis dafür schaffen, dass nicht jeder Prozessschritt durch einen Agenten automatisiert werden sollte.

Wir haben grundsätzlich vier Arten von Prozessaktivitäten:
A. Klassische Workflow-Aktivität
Deterministisch

Eine klar definierte Aktivität mit festen Regeln und einem vorhersehbaren Ergebnis.

Beispiel: Anlage eines HR Cases oder Aktualisierung eines Mitarbeiterdatensatzes.


B. Regelbasierte Entscheidung
Deterministisch

Eine Entscheidung, die anhand definierter Geschäftsregeln getroffen wird.

Beispiel: Prüfung, ob ein Antrag vollständig ist oder eine bestimmte Genehmigungsstufe benötigt.


C. Agentische Aktivität
KI-basiert

Eine Aufgabe, die Interpretation, Kontextverständnis, Planung oder flexible Problemlösung benötigt.

Beispiel: Analyse einer komplexen Mitarbeiteranfrage oder Zusammenfassung eines Sachverhalts.


D. Menschliche Aktivität
Human-in-the-Loop

Eine Aktivität, die menschliches Urteilsvermögen, Verantwortung oder eine explizite Freigabe benötigt.

Beispiel: Entscheidung über eine Beförderung oder Freigabe einer kritischen Personalmaßnahme.


Diese vier Aktivitätstypen sollten in euren zukünftigen HR-Prozessmodellen explizit unterschieden werden.

Ich würde daraus ein Grundprinzip machen:
Agenten ergänzen und erweitern bestehende HR-Prozesse. Sie ersetzen nicht automatisch klassische Workflows, Geschäftsregeln oder menschliche Entscheidungen.

2.2 Wie werden Agenten in Prozesse eingebunden?
Ich sehe vier grundlegende Integrationsmuster.
Muster A: Agent als Prozessschritt







vidvatta.in


Ein bestehender Prozess ruft einen Agenten an einer definierten Stelle auf.

Beispiel Recruiting:
1. Bewerbung geht ein.
2. Prozess startet in Avature.
3. Ein Agent analysiert die Bewerbungsunterlagen anhand vorgegebener Kriterien.
4. Ergebnis wird an den Prozess zurückgegeben.
5. Ein Mensch prüft und entscheidet über das weitere Vorgehen.
Vorteil: Sehr gut kontrollierbar und einfach in bestehende Prozesse integrierbar.

Meine Einschätzung: Das sollte euer bevorzugtes Einstiegsmuster sein.
Muster B: Agent als Prozessassistent







eesel.ai


Der Agent begleitet einen Prozess und unterstützt einen Menschen bei mehreren Aktivitäten.

Beispiel HR Business Partner:
- Ein HR Case wird geöffnet.
- Der Agent analysiert den bisherigen Sachverhalt.
- Er recherchiert relevante Richtlinien.
- Er schlägt eine Antwort vor.
- Der HR Business Partner entscheidet über die Verwendung.
Vorteil: Hoher Mehrwert, ohne dem Agenten die Prozessverantwortung zu übertragen.
Muster C: Agent als Teilprozess-Orchestrator







github.com


Ein Agent erhält eine klar definierte Teilaufgabe und kann innerhalb dieser Aufgabe weitere Agenten oder Tools koordinieren.

Beispiel:

Ein Agent soll einen komplexen HR-Sachverhalt analysieren und dafür:
- Einen Richtlinien-Agenten aufrufen.
- Einen Organisations-Agenten konsultieren.
- Einen Datenanalyse-Agenten einsetzen.
- Die Ergebnisse zusammenführen.
Der übergeordnete HR-Prozess bleibt dabei weiterhin in der Process Engine.

Vorteil: Flexibilität innerhalb einer begrenzten fachlichen Verantwortung.
Muster D: Agent als End-to-End-Prozessagent







marcohkvanhurne.medium.com


Ein Agent übernimmt die Steuerung eines größeren Prozessabschnitts und entscheidet eigenständig über die nächsten Schritte.

Beispiel:

Ein Agent bearbeitet eine Mitarbeiteranfrage, recherchiert Informationen, ruft Spezialagenten auf und veranlasst definierte Aktionen.

Vorteil: Sehr hohe Automatisierungsmöglichkeiten.

Risiko: Komplexe Kontrolle, eingeschränkte Vorhersehbarkeit und erhöhte Anforderungen an Governance.

Ich würde dieses Muster zunächst nur für klar begrenzte, risikoarme Anwendungsfälle zulassen.
2.3 Wie sieht ein geeignetes Prozessmodell aus?
Ich würde einen HR-Prozess künftig um eine zusätzliche Ebene erweitern: die Agentic Layer.

Nehmen wir einen Mitarbeiter-Onboarding-Prozess.
Beispiel: Onboarding
Business Process – Onboarding
Gesteuert durch eine Process Engine, z. B. ServiceNow oder Oracle

Prozessaktivitäten
Workflow
Mitarbeiter anlegen
Oracle

Agent
Unterlagen prüfen
Onboarding Agent

Mensch
Freigabe erteilen
Führungskraft

Agent
Kommunikation vorbereiten
Communication Agent




HR Agent Orchestration Layer
Koordination der Agenten, Kontext, Status, Governance

HR Systems & Tools
Oracle · ServiceNow · Identity Services · Dokumentenmanagement

Die konkrete Umsetzung kann unterschiedlich sein. Entscheidend ist, dass ihr den Agenten als expliziten Akteur im Prozessmodell behandelt.
2.4 Was passiert bei Fehlern und Unterbrechungen?
Hier wird es besonders interessant.

Ein klassischer Workflow ist relativ einfach zu steuern: Ein Schritt wird ausgeführt oder schlägt fehl.

Bei Agenten ist das nicht so eindeutig.

Ein Agent kann:
- Ein unvollständiges Ergebnis liefern.
- Eine Aufgabe nicht lösen können.
- Ein anderes Ergebnis liefern als erwartet.
- Eine Rückfrage benötigen.
- Ein Tool nicht erreichen.
- Eine Aufgabe an einen anderen Agenten delegieren.
- Einen Prozessschritt starten, aber nicht erfolgreich abschließen.
Dafür braucht ihr definierte Prozess- und Agentenstatus.

Beispielsweise:
Status	Bedeutung
Requested	Aufgabe wurde angefordert
Accepted	Agent hat die Aufgabe übernommen
Running	Aufgabe wird bearbeitet
Awaiting Input	Weitere Informationen erforderlich
Awaiting Approval	Menschliche Freigabe erforderlich
Completed	Aufgabe erfolgreich abgeschlossen
Failed	Aufgabe fehlgeschlagen
Escalated	Aufgabe wurde eskaliert
Cancelled	Aufgabe abgebrochen

Wichtig ist die Unterscheidung zwischen dem Status eines Agentenauftrags und dem Status des übergeordneten HR-Prozesses.

Ein Agent kann beispielsweise Completed sein, während der HR-Prozess weiterhin auf eine menschliche Freigabe wartet.
2.5 Was sollte im Workshop entschieden werden?
Ich würde folgende Fragen mitnehmen:
1. Welche Arten von Prozessaktivitäten unterscheiden wir?
2. Welche Agent-Integrationsmuster wollen wir unterstützen?
3. Wo liegt die Prozessverantwortung?
4. Wann darf ein Agent selbstständig Teilaufgaben orchestrieren?
5. Wie werden Agentenaufgaben in Prozessmodelle integriert?
6. Wie behandeln wir Fehler, Timeouts und Unterbrechungen?
7. Wie unterscheiden wir Agentenstatus und Prozessstatus?
8. Welche Prozessschritte dürfen niemals vollständig autonom erfolgen?
Ergebnis: Ein gemeinsames Agentic Process Design Framework mit definierten Integrationsmustern, Statusmodellen und Verantwortlichkeiten.

3. Thema 2: Agent Observability & Monitoring
Sehr hohe Priorität
Hier würde ich deutlich weiter gehen als bei klassischem IT-Monitoring.

Bei klassischen Anwendungen interessiert uns vor allem, ob ein System funktioniert, wie schnell es antwortet und ob Fehler auftreten.

Bei Agenten reicht das nicht.

Ein Agent kann technisch vollständig verfügbar sein und trotzdem schlechte Ergebnisse produzieren.

Beispielsweise:
- Er gibt eine fachlich falsche Antwort.
- Er verwendet eine veraltete HR-Richtlinie.
- Er interpretiert einen Prozesskontext falsch.
- Er ruft ein falsches Tool auf.
- Er liefert eine überzeugend klingende, aber unzutreffende Begründung.
Daher benötigen wir ein erweitertes Observability-Konzept.
3.1 Fünf Dimensionen des Agenten-Monitorings
1. Technical Observability

Funktioniert die technische Ausführung?
- Verfügbarkeit
- Latenz
- Fehlerraten
- Timeouts
- API-Fehler
- Ressourcenverbrauch


2. Agent Behavior Monitoring

Wie verhält sich der Agent?
- Tool-Aufrufe
- Agentenübergaben
- Anzahl der Reasoning-Schritte
- Schleifen und Wiederholungen
- Abweichungen vom erwarteten Verhalten
- Abbrüche


3. Quality & Outcome Monitoring

Wie gut sind die Ergebnisse?
- Fachliche Korrektheit
- Vollständigkeit
- Relevanz
- Groundedness
- Erfolgsquote
- Nutzerzufriedenheit


4. Risk & Compliance Monitoring

Werden die Sicherheits- und Governance-Anforderungen eingehalten?
- Unzulässige Datenzugriffe
- Policy-Verstöße
- Kritische Aktionen
- Unautorisierte Tool-Aufrufe
- Datenschutzvorfälle
- Human Override


5. Business & Economic Monitoring

Liefert der Agent einen wirtschaftlichen Mehrwert?
- Kosten pro Aufgabe
- Token-Verbrauch
- Durchlaufzeiten
- Automatisierungsgrad
- Entlastung von HR-Mitarbeitern
- Kosten-Nutzen-Verhältnis


Meine Empfehlung: Diese fünf Dimensionen sollten das Grundgerüst eures Monitoring-Konzepts bilden.
3.2 Welche Metriken sollten wir messen?
Ich würde zwischen technischen, agentenspezifischen und fachlichen KPIs unterscheiden.
Kategorie	Beispielmetriken
Verfügbarkeit	Agent Availability, API Availability
Performance	Response Time, Task Duration
Zuverlässigkeit	Success Rate, Failure Rate
Agentenverhalten	Tool Call Count, Handoff Rate
Qualität	Accuracy, Completeness, Groundedness
Governance	Policy Violation Rate, Approval Rate
Wirtschaftlichkeit	Cost per Task, Cost per Successful Task
Prozesswirkung	Process Cycle Time, Automation Rate

Einige Metriken sind dabei nicht einfach automatisch messbar.

Beispielsweise lässt sich die fachliche Richtigkeit eines Agentenergebnisses nicht zuverlässig allein anhand eines zweiten LLM beurteilen. Hier braucht ihr Referenzdaten, fachliche Stichproben und menschliche Bewertungen.
3.3 Der entscheidende Punkt: End-to-End-Observability
Ich würde ein übergreifendes Monitoring aufbauen, das den gesamten Weg einer Agenteninteraktion nachvollziehen kann.

Nehmen wir eine Mitarbeiteranfrage:
1. Mitarbeiter eröffnet einen HR Case in ServiceNow.
2. ServiceNow ruft den zentralen Orchestrator auf.
3. Der Orchestrator ruft einen HR Policy Agent auf.
4. Dieser Agent fragt über MCP eine Wissensquelle ab.
5. Anschließend wird ein weiterer Agent für die Analyse benötigt.
6. Das Ergebnis wird zurückgegeben.
7. Ein HR-Mitarbeiter prüft die Antwort.
Jetzt müsst ihr beantworten können:
- Welcher Prozess hat die Interaktion ausgelöst?
- Welcher Agent wurde wann aufgerufen?
- Welche Version wurde verwendet?
- Welche Tools wurden aufgerufen?
- Welche Datenquellen wurden genutzt?
- Wo ist Zeit verloren gegangen?
- Welche Kosten sind entstanden?
- Wie wurde das Ergebnis bewertet?
Dafür würde ich eine gemeinsame Trace-ID beziehungsweise Correlation-ID verwenden.
Beispiel: End-to-End-Trace
1. ServiceNow HR Case
   Trace ID: HR-2026-00125
2. HR Orchestrator
   Agent Routing – 120 ms
3. HR Policy Agent
   Execution – 2,4 Sekunden
4. MCP Knowledge Service
   Document Retrieval – 450 ms
5. Response & Quality Check
   Ergebnisprüfung – erfolgreich
6. Human Review
   Freigabe durch HR-Mitarbeiter
Illustrative Darstellung einer verteilten Agenteninteraktion, keine realen Messwerte.
Hier bietet sich insbesondere das OpenTelemetry-Konzept an, das mit Traces, Metrics und Logs eine Grundlage für die technische Beobachtbarkeit verteilter Systeme schafft.

Für Agenten muss man das um fachliche und qualitative Evaluationsdaten ergänzen.
3.4 Wer ist für welches Monitoring verantwortlich?
Das ist eine wichtige Architekturfrage.

Ich würde drei Ebenen unterscheiden:
Ebene	Verantwortlichkeit
Lokales Agent Monitoring	Der jeweilige Plattformbetreiber überwacht den Agenten und seine Runtime.
Orchestrator Monitoring	Der Orchestrator überwacht Agentenaufrufe, Delegationen und übergreifende Abläufe.
Enterprise Monitoring	Eine zentrale Instanz bündelt technische, fachliche und Governance-Kennzahlen.

Beispiel:
- ServiceNow überwacht seinen lokalen Agenten.
- Oracle überwacht seinen lokalen Agenten.
- Der HR Orchestrator erkennt, wenn ein Agentenaufruf aus einem übergreifenden Prozess fehlschlägt.
- Ein Enterprise Monitoring liefert eine übergreifende Sicht auf die Agentenlandschaft.
Wichtig: Ihr solltet nicht versuchen, sämtliche Rohdaten und Prompts zentral zu sammeln. Gerade bei sensiblen HR-Informationen müssen Datensparsamkeit, Zugriffsschutz und Aufbewahrungsfristen berücksichtigt werden.
3.5 Wie gehen wir mit Auffälligkeiten um?
Monitoring ohne Konsequenzen ist wenig wertvoll.

Ich würde definierte Reaktionsmechanismen vorsehen:
Auffälligkeit	Mögliche Reaktion
Agent nicht erreichbar	Retry, Fallback oder Eskalation
Hohe Fehlerquote	Agent deaktivieren oder Traffic reduzieren
Schlechte Ergebnisqualität	Menschliche Prüfung erzwingen
Unzulässiger Tool-Aufruf	Blockieren und Sicherheitsalarm
Hohe Kosten	Limits oder Routing-Regeln anpassen
Wiederkehrende Fehlentscheidungen	Agent pausieren und untersuchen

Ein wichtiger Begriff ist dabei der Circuit Breaker: Wenn ein Agent wiederholt fehlschlägt, werden weitere Aufrufe vorübergehend unterbunden, statt einen größeren Prozess zu gefährden.
3.6 Was sollte im Workshop entschieden werden?
1. Welche fünf Monitoring-Dimensionen wollen wir etablieren?
2. Welche Kennzahlen sind für alle Agenten verpflichtend?
3. Wie gewährleisten wir End-to-End-Tracing?
4. Welche Informationen müssen lokal und welche zentral vorliegen?
5. Wer überwacht die Qualität der Agentenergebnisse?
6. Wer darf einen Agenten bei Problemen deaktivieren?
7. Welche Schwellenwerte lösen Eskalationen aus?
8. Wie stellen wir Datenschutz bei Logs und Traces sicher?
Ergebnis: Ein übergreifendes Agent Observability Framework mit Mindestmetriken, Trace-Konzept, Verantwortlichkeiten und Reaktionsmechanismen.

4. Thema 3: Integration Layer & Enterprise Connectivity
Sehr hohe Priorität
Das ist für eure Ausgangslage mit ServiceNow, Oracle, Avature und zahlreichen weiteren Systemen besonders relevant.

Ich würde dieses Thema sehr bewusst von der Agentenorchestrierung trennen.

Denn ihr habt zwei unterschiedliche Herausforderungen:
1. Wie koordinieren wir die Zusammenarbeit von Agenten?
2. Wie ermöglichen wir diesen Agenten einen sicheren und standardisierten Zugriff auf die bestehende HR-Systemlandschaft?
Das sind zwei unterschiedliche Verantwortlichkeiten.

Meine zentrale These: Der Integration Layer sollte eine wiederverwendbare Enterprise-Fähigkeit sein, die sowohl Agenten als auch klassische Anwendungen und Prozesse nutzen können.

Ihr solltet also keine neue, ausschließlich für Agenten entwickelte Integrationslandschaft aufbauen.
4.1 Warum brauchen wir einen Integration Layer?
Schauen wir auf eure Systemlandschaft:
Beispiel einer heterogenen HR-Systemlandschaft
ServiceNow
HR Service Delivery, Cases, Workflows

Oracle
Core HR, Mitarbeiterdaten, Prozesse

Avature
Recruiting, Talent Acquisition

Weitere Systeme
Eigenentwicklungen, Speziallösungen



Integration Layer
API Management · Integration Services · Events · Transformation · Security

Agenten, Orchestratoren und klassische Anwendungen


Ohne eine solche Abstraktionsschicht entstehen schnell direkte Integrationen zwischen Agenten und einzelnen Fachsystemen.

Das kann bei zwei oder drei Agenten noch funktionieren. Bei einer wachsenden Landschaft wird es schwierig.

Typische Probleme:
- Jeder Agent benötigt eigene Schnittstellen.
- Jeder Agent implementiert Authentifizierung und Fehlerbehandlung selbst.
- Datenformate unterscheiden sich.
- Berechtigungen werden unterschiedlich umgesetzt.
- Änderungen in Fachsystemen wirken sich auf viele Agenten aus.
- Monitoring und Auditierung werden uneinheitlich.
4.2 Welche Komponenten sollte der Integration Layer umfassen?
Ich würde sechs Capability-Bereiche unterscheiden.
1. API Management & Gateway
- Einheitliche API-Veröffentlichung
- Authentifizierung und Autorisierung
- Rate Limiting
- API-Versionierung
- Zugriffskontrolle


2. Integration Services & Connectors
- Standardisierte Konnektoren zu HR-Systemen
- Wiederverwendbare Geschäftsoperationen
- Systemübergreifende Service-Aufrufe
- Kapselung proprietärer APIs


3. Event & Messaging Infrastructure
- Event-basierte Kommunikation
- Publish/Subscribe
- Asynchrone Verarbeitung
- Event Routing
- Dead-Letter Queues


4. Data Transformation & Mediation
- Mapping unterschiedlicher Datenmodelle
- Schema-Transformation
- Validierung
- Normalisierung
- Protokollübersetzung


5. Agent Tool Exposure
- Bereitstellung von Business-Funktionen als Tools
- MCP-Server beziehungsweise MCP-Adapter
- Tool-Beschreibungen und Schemas
- Kontrollierte Tool-Ausführung


6. Security & Policy Enforcement
- Token Management
- Identitätsweitergabe
- Zugriffsrichtlinien
- Datenfilterung
- Protokollierung


Ein wichtiger Architekturgedanke ist hier die Unterscheidung zwischen technischen Schnittstellen und fachlichen Services.
4.3 Von technischen APIs zu Business Capabilities
Ich würde Agenten nicht möglichst direkt mit den technischen APIs der HR-Systeme verbinden.

Stattdessen würde ich eine Ebene wiederverwendbarer Business Capabilities aufbauen.

Beispiel:

Ein Agent möchte Informationen über einen Mitarbeiter abrufen.

Technisch könnte er dafür mehrere Oracle-APIs verwenden.

Besser wäre aber eine fachliche Operation:

getEmployeeProfile(employeeId)

Oder:

getOrganizationalContext(employeeId)

Die Integrationsebene kapselt dann:
- Welche Systeme angesprochen werden müssen.
- Wie Daten zusammengeführt werden.
- Wie die Datenformate harmonisiert werden.
- Welche Berechtigungen erforderlich sind.
- Wie Fehler behandelt werden.
Das ist besonders hilfreich, wenn sich eure Systemlandschaft verändert.

Beispielsweise könnte eine fachliche Funktion zunächst aus Oracle gespeist werden und später durch ein anderes HR-System ergänzt werden, ohne dass jeder Agent angepasst werden muss.
Beispiel: Fachliche Service-Abstraktion
Business Capability	Technische Quelle
Mitarbeiterprofil abrufen	Oracle
Bewerberprofil abrufen	Avature
HR Case erstellen	ServiceNow
Organisationsstruktur abfragen	Oracle / weitere Quellen
Freigabestatus prüfen	ServiceNow / Oracle
Stelleninformationen abrufen	Avature / Oracle

Das sind zunächst Beispiele für mögliche Services, keine Festlegung auf eure tatsächlichen Datenverantwortlichkeiten.
4.4 Welche Rolle spielen MCP und APIs im Integration Layer?
Hier würde ich eine klare Abgrenzung vornehmen:
- APIs sind die technische Schnittstelle zu euren Systemen.
- Integration Services kapseln die Geschäftsoperationen.
- MCP kann diese Funktionen für Agenten standardisiert verfügbar machen.
- A2A ermöglicht die Kommunikation zwischen Agenten.
- Der Orchestrator koordiniert, welcher Agent welche Funktion benötigt.
Ein Beispiel:
Beispiel: Ein Agent möchte einen HR Case anlegen
HR Agent


MCP Tool
createHRCase()

Integration Service
Validierung · Berechtigungsprüfung · Mapping

ServiceNow API
HR Case wird angelegt

Ein MCP-Server sollte dabei nicht einfach ungefiltert sämtliche System-APIs veröffentlichen.

Ich würde eine kontrollierte Auswahl fachlich sinnvoller Tools bereitstellen.

Ein Tool wie updateEmployeeSalary() hat beispielsweise ein völlig anderes Risikoprofil als getEmployeeProfile().

Das sollte sich in den Berechtigungen, Freigaben und Kontrollmechanismen widerspiegeln.
4.5 Welche Integrationsmuster benötigen wir?
Neben den Komponenten würde ich vier Integrationsmuster betrachten:
Muster	Wann sinnvoll?	HR-Beispiel
Synchronous API	Sofortige Antwort benötigt	Mitarbeiterinformationen abrufen
Asynchronous Request/Response	Aufgabe dauert länger	Komplexe Datenanalyse
Event-driven	Auf ein Ereignis reagieren	Neue Bewerbung eingegangen
Batch / Bulk	Große Datenmengen verarbeiten	Regelmäßige Datenabgleiche

Gerade das Event-basierte Modell finde ich für eure Agentenlandschaft spannend.

Beispiel:

Ein HR-System veröffentlicht das Event EmployeePositionChanged.

Ein entsprechender Prozess oder Agent kann darauf reagieren, ohne dass ein anderes System ihn direkt aufrufen muss.

Dabei solltet ihr auf idempotente Verarbeitung achten: Ein mehrfach zugestelltes Event darf nicht dazu führen, dass beispielsweise dieselbe Personalmaßnahme mehrfach ausgeführt wird.

Weitere wichtige Konzepte:
- Retries mit kontrollierten Wiederholungsstrategien
- Dead-Letter Queues
- Event Versioning
- Idempotency Keys
- Transactional Outbox, wo fachlich erforderlich
- Kompensationsmechanismen bei verteilten Prozessen
4.6 Zentraler oder dezentraler Integration Layer?
Ich würde keine vollständig zentrale Integrationsplattform erzwingen.

Stattdessen:
- Bestehende Enterprise-Integrationsplattformen weiterverwenden.
- Vorhandene API Gateways nutzen.
- Fachliche Services möglichst wiederverwendbar bereitstellen.
- Neue Agenten-Tools über kontrollierte Schnittstellen veröffentlichen.
- Lokale Plattformintegrationen dort belassen, wo sie sinnvoll sind.
Die Agentenarchitektur sollte die bestehende Integrationsarchitektur ergänzen und nicht duplizieren.
4.7 Was sollte im Workshop entschieden werden?
1. Welche Rolle soll der Integration Layer übernehmen?
2. Gibt es bereits vorhandene Integrationskomponenten, die wir nutzen müssen?
3. Wollen wir fachliche Business Capabilities als wiederverwendbare Services etablieren?
4. Wie werden APIs für Agenten verfügbar gemacht?
5. Welche Rolle spielt MCP?
6. Wann nutzen wir APIs und wann Events?
7. Wie gehen wir mit asynchronen und länger laufenden Aufgaben um?
8. Wo finden Transformation und semantisches Mapping statt?
9. Wie gewährleisten wir einheitliche Berechtigungen?
10. Welche Systeme müssen für die ersten produktiven Agenten angebunden werden?
Ergebnis: Ein logisches Integrationszielbild mit Integrationsmustern, Verantwortlichkeiten, Business-Service-Konzept und einer ersten Schnittstellenstrategie.

5. Thema 4: HR Ontology & Semantic Layer
Strategisch sehr wichtig
Dieses Thema würde ich nicht als rein technische Datenmodellierungsdiskussion behandeln.

Ich sehe darin eine strategische Voraussetzung für eine wirklich systemübergreifende Agentenlandschaft.

Denn eure Agenten werden perspektivisch Informationen aus unterschiedlichen HR-Systemen miteinander kombinieren müssen.

Das funktioniert nur dann zuverlässig, wenn sie nicht nur technisch auf Daten zugreifen können, sondern auch verstehen, was diese Daten fachlich bedeuten.
5.1 Das Problem: Unterschiedliche Systeme sprechen unterschiedliche Sprachen
Nehmen wir das Beispiel einer Person.

In unterschiedlichen Systemen können verschiedene Begriffe und Datenmodelle existieren:
Fachliches Konzept	Mögliche Systemrepräsentation
Person	Person Record
Mitarbeiter	Employee
Bewerber	Candidate
Stelle	Job / Position
Organisation	Department / Business Unit
HR-Anfrage	HR Case
Kompetenz	Skill / Competency

Ein besonders interessantes Beispiel ist die Unterscheidung zwischen Job und Position.

Ein Job beschreibt typischerweise eine Tätigkeits- oder Rollenart. Eine Position ist dagegen eine konkrete organisatorische Stelle, die beispielsweise einer Person zugeordnet werden kann.

Wenn eure Systeme diese Begriffe unterschiedlich verwenden, können Agenten falsche Schlussfolgerungen ziehen, obwohl sie technisch korrekte Daten erhalten.
5.2 Was genau meinen wir mit Ontologie?
Ich würde die Begriffe sauber trennen.
Begriff	Bedeutung
Data Model	Wie sind Daten strukturiert?
Data Dictionary	Welche Felder und Attribute gibt es?
Taxonomy	Wie werden Begriffe hierarchisch klassifiziert?
Business Glossary	Was bedeuten fachliche Begriffe?
Ontology	Welche Konzepte existieren und wie hängen sie fachlich zusammen?
Knowledge Graph	Wie werden Entitäten und Beziehungen als vernetztes Wissen repräsentiert?
Semantic Layer	Wie wird ein gemeinsames fachliches Verständnis technisch verfügbar gemacht?

Eine Ontologie kann beispielsweise ausdrücken:
- Ein Employee ist eine Person.
- Ein Employee ist einer Position zugeordnet.
- Eine Position gehört zu einer Organisationseinheit.
- Eine Position hat ein Anforderungsprofil.
- Ein Candidate kann sich auf eine Position bewerben.
- Eine Bewerbung gehört zu einem Recruiting-Prozess.
Das ist mehr als ein gemeinsames Datenmodell. Es beschreibt die fachliche Bedeutung und die Beziehungen der Konzepte.
5.3 Wie könnte eine HR-Ontologie aussehen?
Ich würde mit einer überschaubaren HR Core Ontology starten.
Beispiel einer HR Core Ontology
Person

Employee
Beschäftigter

Candidate
Bewerber



Position
Organisatorische Stelle

Skills & Competencies
Fähigkeiten

Organization
Organisationseinheit

Job
Rollenprofil


Stark vereinfachtes Beispiel; die tatsächlichen Beziehungen müssen fachlich definiert werden.
Dazu gehören natürlich auch Prozesskonzepte wie:
- HR Process
- HR Case
- Approval
- Task
- Application
- Employment Relationship
- Organizational Assignment
Ich würde dabei nicht versuchen, sofort die komplette HR-Welt zu modellieren.

Viel sinnvoller wäre eine schrittweise Entwicklung entlang konkreter Use Cases.
5.4 Wie wird die Ontologie technisch nutzbar?
Eine Ontologie allein hilft euren Agenten noch nicht.

Ihr benötigt eine technische Architektur, die das semantische Modell mit euren tatsächlichen Systemdaten verbindet.

Ich würde vier Bausteine unterscheiden:

A. Semantic Model

Die fachlichen Konzepte und Beziehungen werden zentral definiert.

B. Mapping Layer

Hier wird festgelegt, wie die fachlichen Konzepte den konkreten Datenmodellen der Systeme entsprechen.

Beispielsweise:

Employee im semantischen Modell wird auf ein bestimmtes Mitarbeiterobjekt in Oracle abgebildet.

C. Semantic Services

Über standardisierte Services können Agenten fachliche Informationen abfragen.

Beispielsweise:
- getEmployeeContext()
- getPositionRequirements()
- getOrganizationalHierarchy()
- getRelevantCompetencies()
D. Knowledge Graph (optional)

Komplexere Beziehungen können als Graph repräsentiert und abgefragt werden.

Das ist insbesondere dann interessant, wenn Agenten Zusammenhänge über mehrere HR-Domänen hinweg erkennen müssen.
5.5 Wie spielt das mit RAG zusammen?
Das würde ich unbedingt diskutieren, denn Ontologie und RAG werden häufig als Alternativen betrachtet, obwohl sie unterschiedliche Probleme lösen.
RAG	Ontologie / Knowledge Graph
Findet relevante Dokumente und Textpassagen	Beschreibt fachliche Konzepte und Beziehungen
Gut für Richtlinien und Dokumentationen	Gut für strukturierte Zusammenhänge
Arbeitet häufig mit semantischer Ähnlichkeit	Arbeitet mit definierten Begriffen und Relationen
Kann unpräzise Treffer liefern	Bietet explizitere semantische Struktur
Liefert Textkontext	Liefert strukturierte Beziehungen

Mein Vorschlag wäre eine Kombination:
- RAG für HR-Richtlinien, Prozessdokumentationen und Wissensartikel.
- Semantisches Modell für fachliche Begriffe und Zusammenhänge.
- APIs für aktuelle operative Daten.
- Knowledge Graph perspektivisch für komplexe Beziehungen.
Ein Agent könnte dann beispielsweise eine Frage beantworten, indem er gleichzeitig eine HR-Richtlinie über RAG findet, die Organisationsstruktur über einen semantischen Service abfragt und aktuelle Mitarbeiterinformationen aus Oracle bezieht.
5.6 Wer sollte die Ontologie verantworten?
Das ist eine wichtige organisatorische Frage.

Ich würde die Verantwortung nicht ausschließlich bei der IT ansiedeln.

Vielmehr braucht ihr:
- HR Domain Owner für die fachliche Definition.
- Data Architects für Datenmodellierung und Mapping.
- Enterprise Architects für die Einbettung in die Gesamtarchitektur.
- Data Governance für Definitionen, Qualität und Verantwortlichkeiten.
Die fachliche Bedeutung eines Begriffs wie Position sollte nicht von einem technischen Systemanbieter vorgegeben werden.
5.7 Was sollte im Workshop entschieden werden?
1. Benötigen wir ein gemeinsames HR-Semantikmodell?
2. Welche HR-Kernbegriffe müssen harmonisiert werden?
3. Welche Systeme sind führend für welche fachlichen Informationen?
4. Wie sollen Agenten auf semantische Informationen zugreifen?
5. Welche Rolle spielen Ontologie, Knowledge Graph und RAG?
6. Wo werden semantische Mappings gepflegt?
7. Wer verantwortet die fachlichen Definitionen?
8. Mit welchen ersten Use Cases beginnen wir?
Ergebnis: Eine Roadmap für ein HR-Semantikmodell, eine erste Liste zentraler HR-Konzepte und ein Verantwortungsmodell für die fachliche Semantik.

6. Thema 5: Identity, Security, Datenschutz & Human-in-the-Loop
Unverzichtbar für produktiven Betrieb
Dieses Thema würde ich unbedingt neu in eure Agenda aufnehmen.

Es ist aus meiner Sicht eine der größten Herausforderungen beim Einsatz von Agenten in HR-Prozessen.

Warum?

Ein Agent ist nicht einfach ein weiterer technischer Nutzer.

Er kann eigenständig Informationen interpretieren, andere Agenten aufrufen und gegebenenfalls Aktionen in produktiven Systemen ausführen.

Damit entstehen neue Fragen:
- In wessen Namen handelt der Agent?
- Welche Daten darf er sehen?
- Welche Aktionen darf er ausführen?
- Darf er seine Berechtigungen weitergeben?
- Wann muss ein Mensch zustimmen?
- Wer trägt die Verantwortung für eine ausgeführte Aktion?
6.1 Identity: Wer ist der Agent?
Ich würde drei Identitäten unterscheiden:
1. User Identity
Die Identität der Person, die einen Prozess oder eine Agenteninteraktion auslöst.Beispiel: Ein HR Business Partner.


2. Agent Identity
Die technische Identität des Agenten, der eine Aufgabe ausführt.Beispiel: Recruiting Agent – ServiceNow.


3. Execution / Delegation Context
Der konkrete Kontext, in dem der Agent handelt.Beispiel: Der Agent arbeitet im Auftrag eines HR Business Partners an einem bestimmten HR Case.


Diese Unterscheidung ist entscheidend.

Ein Agent sollte nicht automatisch sämtliche Berechtigungen erhalten, die sein technischer Service Account besitzt.

Stattdessen muss die Berechtigung aus dem Zusammenspiel von Identität, Aufgabe, Datenkontext und Aktion abgeleitet werden.
6.2 Das Berechtigungsmodell
Ich würde ein mehrstufiges Modell aufbauen:
Kontrollfrage	Beispiel
Wer hat die Interaktion gestartet?	HR Business Partner
Welcher Agent führt sie aus?	HR Case Agent
Welche Aufgabe darf er bearbeiten?	Case analysieren
Auf welche Daten darf er zugreifen?	Zugeordneter HR Case
Welche Tools darf er nutzen?	Case Read, Policy Search
Welche Aktionen darf er ausführen?	Antwortentwurf erstellen
Welche Aktionen sind gesperrt?	Mitarbeiterdaten ändern

Besonders wichtig ist die Trennung zwischen Lesen, Vorbereiten und Ausführen.

Ein Agent kann beispielsweise eine Gehaltsänderung vorbereiten, ohne berechtigt zu sein, sie tatsächlich durchzuführen.
6.3 Risk-based Autonomy: Wie viel Autonomie darf ein Agent haben?
Ich würde hierfür ein einheitliches Risikomodell einführen.
Level 1 – Read
Geringeres Risiko

Agent darf Informationen lesen, zusammenfassen und analysieren.

Beispiel: HR-Richtlinie recherchieren.


Level 2 – Prepare
Begrenztes Risiko

Agent darf Aktionen vorbereiten, aber nicht selbstständig ausführen.

Beispiel: Änderung eines Mitarbeiterdatensatzes vorbereiten.


Level 3 – Execute with Approval
Kontrollbedürftig

Agent darf eine Aktion nach expliziter menschlicher Freigabe ausführen.

Beispiel: Genehmigte Änderung in einem HR-System durchführen.


Level 4 – Autonomous Execution
Hohes Kontrollniveau erforderlich

Agent darf definierte Aktionen innerhalb enger Grenzen selbstständig durchführen.

Beispiel: Standardisierte, risikoarme administrative Aktualisierung.


Das ist ein vorgeschlagenes internes Autonomiemodell, keine regulatorische Risikoklassifizierung.

Die eigentliche Einstufung sollte nicht nur vom Agenten abhängen, sondern von der konkreten Aktion und ihrem Kontext.

Ein Agent kann bei einer Aufgabe autonom arbeiten und bei einer anderen zwingend eine Freigabe benötigen.
6.4 Human-in-the-Loop: Wie wird der Mensch eingebunden?
Ich würde zwischen drei Formen unterscheiden:
- Human-in-the-Loop: Mensch muss aktiv entscheiden oder freigeben.
- Human-on-the-Loop: Mensch überwacht und kann eingreifen.
- Human-in-Command: Mensch definiert die grundsätzlichen Grenzen, Regeln und Verantwortlichkeiten.
Beispiel:

Ein Agent analysiert einen HR Case und erstellt eine Handlungsempfehlung.

Der HR-Mitarbeiter prüft das Ergebnis und gibt eine Aktion frei.

Der Orchestrator stellt sicher, dass die Aktion erst nach der Freigabe ausgeführt werden kann.

Dabei sollte die Freigabe an einen konkreten, unveränderlichen Aktionskontext gebunden sein: Wer hat was, auf welcher Datengrundlage und in welcher Version freigegeben?
6.5 Was bedeutet das für eure HR-Anwendungsfälle?
Ich würde besonders bei diesen Tätigkeiten genau hinschauen:
HR-Aktivität	Grundsätzliche Kontrollanforderung
HR-Richtlinien recherchieren	Lesen und Zusammenfassen meist gut automatisierbar
Mitarbeiteranfrage klassifizieren	Validierung und Qualitätskontrolle
Antwortentwurf erstellen	Menschliche Prüfung je nach Inhalt
Mitarbeiterdaten ändern	Strenge Berechtigungs- und Aktionskontrolle
Gehaltsänderungen vorbereiten	Menschliche Freigabe
Kandidatenprofile analysieren	Besondere Anforderungen an Fairness und Kontrolle
Personalentscheidungen treffen	Keine unkontrollierte autonome Entscheidung

Hier ist auch die regulatorische Einordnung wichtig: Der EU AI Act behandelt bestimmte KI-Systeme im Beschäftigungs- und Personalmanagement, etwa Systeme für Recruiting, Auswahl und Entscheidungen über Beschäftigungsbedingungen, als Hochrisiko-Anwendungen. Die konkrete Einstufung hängt von Zweckbestimmung und Einsatz ab. Die aktuellen Übergangs- und Anwendungsfristen solltet ihr mit Legal und Compliance anhand der geltenden Regelungen prüfen. 

AI Act Service Desk

Gerade für eure Recruiting- und Talent-Management-Agenten ist das kein Thema, das man erst nach der technischen Implementierung betrachten sollte.
6.6 Weitere Sicherheitsrisiken
Ich würde außerdem die spezifischen Risiken agentischer Systeme berücksichtigen:
- Prompt Injection über Dokumente und externe Datenquellen
- Unzulässige Tool-Aufrufe
- Privilegienausweitung
- Manipulation durch Agentenübergaben
- Unsichere Verarbeitung sensibler HR-Daten
- Unkontrollierte Aktionen
- Zu weitreichende technische Service Accounts
Als Referenz für diesen Teil würde ich das OWASP Top 10 for Agentic Applications 2026 verwenden. 

OWASP Gen AI Security Project

6.7 Was sollte im Workshop entschieden werden?
1. Welche Identitäten benötigen wir?
2. Wie werden Berechtigungen an Agenten weitergegeben?
3. Welche Aktionen dürfen Agenten lesen, vorbereiten oder ausführen?
4. Wie klassifizieren wir das Risiko einzelner Aktionen?
5. Welche Freigaben sind erforderlich?
6. Wie werden Freigaben technisch abgesichert?
7. Welche Agentenaktionen müssen besonders protokolliert werden?
8. Wie integrieren wir Datenschutz und AI Governance in die Architektur?
Ergebnis: Ein Agent Identity & Authorization Framework, ein Autonomiemodell und definierte Human-in-the-Loop-Prinzipien.

7. Thema 6: Agent Evaluation & Quality Engineering
Sehr hohe Priorität vor Produktivsetzung
Dieses Thema fehlt in vielen Agentenarchitektur-Diskussionen vollständig.

Ich halte es aber für extrem wichtig.

Denn Agenten sind keine klassischen Softwarekomponenten, deren Verhalten bei gleichen Eingaben immer identisch sein muss.

Sie können bei gleichen Eingaben unterschiedliche Ergebnisse liefern. Sie können durch Änderungen am Modell, Prompt, Tool oder Kontextverhalten beeinflusst werden.

Deshalb reicht ein klassischer Softwaretest nicht aus.

Ihr braucht einen systematischen Ansatz, um Agenten fachlich und technisch zu testen, zu bewerten und für den produktiven Einsatz freizugeben.
7.1 Vier Testdimensionen
1. Functional Testing
- Funktioniert die definierte Aufgabe?
- Werden die richtigen Tools aufgerufen?
- Werden Ergebnisse im erwarteten Format zurückgegeben?
- Werden Fehler korrekt behandelt?


2. Quality Evaluation
- Ist das Ergebnis fachlich korrekt?
- Ist es vollständig?
- Ist es nachvollziehbar?
- Ist es durch die zugrunde liegenden Quellen gedeckt?


3. Safety & Security Testing
- Werden Berechtigungen eingehalten?
- Funktionieren Schutzmechanismen gegen Prompt Injection?
- Werden unzulässige Aktionen verhindert?
- Werden sensible Daten geschützt?


4. Process & Business Testing
- Funktioniert der gesamte Prozess?
- Werden Prozessübergänge korrekt ausgeführt?
- Werden Menschen an den richtigen Stellen eingebunden?
- Wird der erwartete Geschäftsnutzen erreicht?


7.2 Wie testen wir die Qualität eines Agenten?
Ich würde für jeden produktiven Agenten ein eigenes Evaluation Framework etablieren.

Nehmen wir einen HR Policy Agent.

Er beantwortet Fragen zu internen HR-Richtlinien.

Dafür erstellt ihr einen Testdatensatz mit beispielsweise 100 repräsentativen Fragen.

Jede Frage erhält eine fachlich geprüfte Referenzantwort beziehungsweise Bewertungskriterien.

Dann prüft ihr:
Qualitätsdimension	Testfrage
Accuracy	Ist die Antwort fachlich richtig?
Groundedness	Ist sie durch die Quellen gedeckt?
Completeness	Sind alle relevanten Aspekte enthalten?
Relevance	Beantwortet sie tatsächlich die Frage?
Citation Quality	Verweist sie auf die richtige Richtlinie?
Safety	Gibt sie unzulässige Informationen preis?
Consistency	Sind ähnliche Fälle ähnlich behandelt?

Ich würde hier nicht nur auf einen einzelnen Gesamtscore setzen.

Beispielsweise kann ein Agent eine hohe durchschnittliche Qualität erreichen und gleichzeitig bei einer kritischen Kategorie systematisch versagen.

Für HR-Anwendungen sind daher auch kategorisierte Fehleranalysen wichtig.
7.3 Evaluation von Multi-Agent-Systemen
Bei euch wird es besonders interessant, wenn mehrere Agenten zusammenarbeiten.

Hier reicht es nicht, die einzelnen Agenten separat zu testen.

Ihr müsst auch die Interaktion testen:
- Werden Aufgaben korrekt delegiert?
- Werden Ergebnisse korrekt weitergegeben?
- Werden Kontextinformationen vollständig übermittelt?
- Entstehen unnötige Agentenschleifen?
- Werden widersprüchliche Ergebnisse erkannt?
- Werden Aufgaben korrekt abgeschlossen?
- Funktionieren Fehlerbehandlung und Eskalation?
Ich würde daher drei Testebenen etablieren:
Agent Level Testing
Einzelner Agent, Tools und Ergebnisse

Orchestration Testing
Routing, Delegation und Zusammenarbeit mehrerer Agenten

End-to-End Process Testing
Kompletter HR-Prozess inklusive Systeme und Menschen

7.4 Regression Testing und Versionierung
Das ist besonders wichtig, weil sich Agenten kontinuierlich verändern können.

Beispielsweise:
- Neuer Prompt
- Neues Modell
- Neue Systemanweisung
- Neues Tool
- Geänderte Wissensquelle
- Andere Orchestrierungslogik
Jede Änderung kann Auswirkungen auf das Verhalten haben.

Ich würde deshalb einen festen Freigabeprozess etablieren:
1. Änderung am Agenten.
2. Automatisierte Tests.
3. Evaluation anhand eines definierten Testdatensatzes.
4. Security- und Governance-Prüfung.
5. Fachliche Abnahme.
6. Freigabe für die nächste Umgebung.
7. Monitoring nach Produktivsetzung.
Eine wichtige Ergänzung ist das sogenannte Shadow Testing: Neue Agentenversionen werden zunächst parallel zu einer bestehenden Version getestet, ohne ihre Ergebnisse direkt für produktive Entscheidungen zu verwenden.
7.5 Wer bewertet die Ergebnisse?
Das sollte nicht ausschließlich durch IT oder Data Science erfolgen.

Ich würde drei Verantwortlichkeiten unterscheiden:
Rolle	Aufgabe
Agent Developer	Technische Tests und Funktionalität
HR Domain Expert	Fachliche Qualität und Richtigkeit
AI Governance / Risk	Sicherheit, Fairness, Compliance und Freigabe

Bei besonders sensiblen Anwendungsfällen sollte die fachliche Abnahme verbindlich sein.
7.6 Was sollte im Workshop entschieden werden?
1. Welche Testdimensionen sind verpflichtend?
2. Wie werden fachliche Referenzdatensätze erstellt?
3. Wer bewertet Agentenergebnisse?
4. Welche Qualitätskriterien müssen erfüllt sein?
5. Wie testen wir Multi-Agent-Interaktionen?
6. Wie führen wir Regressionstests durch?
7. Wann darf ein Agent produktiv gehen?
8. Wie werden Änderungen und neue Versionen freigegeben?
Ergebnis: Ein HR Agent Evaluation Framework mit Teststufen, Qualitätsmetriken, Freigabekriterien und Verantwortlichkeiten.

8. Thema 7: Operations, Resilience & Lifecycle Management
Für den skalierbaren Betrieb
Dieses Thema würde ich ergänzen, weil sich eine produktive Agentenlandschaft nicht wie eine Sammlung einzelner KI-Projekte betreiben lässt.

Wenn ihr in zwei oder drei Jahren beispielsweise 30, 50 oder mehr Agenten habt, benötigt ihr ein systematisches Betriebsmodell.

Dafür müsst ihr bereits heute einige Grundsatzentscheidungen treffen.
8.1 Wie sieht der Lebenszyklus eines Agenten aus?
Ich würde für jeden Agenten einen standardisierten Lifecycle definieren.
Agent Lifecycle
1. Design & Registration
   
   Fachlicher Zweck, Verantwortlichkeit, Fähigkeiten, Schnittstellen und Risikoklassifizierung definieren.
2. Development & Testing
   
   Agent entwickeln, Tools integrieren, Evaluation und Sicherheitstests durchführen.
3. Approval & Certification
   
   Fachliche, technische und regulatorische Freigabe einholen.
4. Deployment & Release
   
   Agent in einer kontrollierten Umgebung bereitstellen und registrieren.
5. Production Operations
   
   Monitoring, Kostenkontrolle, Incident Management und Qualitätsüberwachung.
6. Optimization & Versioning
   
   Verhalten analysieren, verbessern und neue Versionen kontrolliert veröffentlichen.
7. Retirement
   
   Agent deaktivieren, Berechtigungen entziehen, Abhängigkeiten entfernen und Nachweispflichten erfüllen.

Ich würde diesen Lifecycle unabhängig von der technischen Plattform definieren.

Ein Agent in ServiceNow sollte grundsätzlich denselben Governance- und Freigabeprozess durchlaufen wie ein Agent in Oracle oder Azure.
8.2 Wie gehen wir mit unterschiedlichen Agentenversionen um?
Ein Beispiel:

Ein HR Policy Agent hat die Version 1.0 und wird produktiv eingesetzt.

Anschließend wird eine Version 1.1 mit einem neuen Modell und aktualisierten Wissensquellen entwickelt.

Jetzt braucht ihr Antworten auf folgende Fragen:
- Welche Version ist produktiv?
- Welche Version wird von welchem Prozess aufgerufen?
- Kann ein Prozess während seiner Laufzeit die Version wechseln?
- Können wir auf eine vorherige Version zurückgehen?
- Wie werden Änderungen bewertet?
- Wie lange müssen alte Versionen nachvollziehbar bleiben?
Ich würde ein zentrales Agentenregister mit mindestens folgenden Informationen vorsehen:
Information	Zweck
Agent ID	Eindeutige Identifikation
Version	Versionskontrolle
Platform	Technischer Anbieter
Owner	Verantwortlichkeit
Status	Development / Approved / Production / Retired
Capabilities	Fachliche Fähigkeiten
Risk Classification	Risikoeinordnung
Dependencies	Modelle, Tools, Datenquellen
Evaluation Status	Qualitätsfreigabe
Approval Record	Freigabenachweis

Das ist eine wichtige Voraussetzung für eine herstellerübergreifende Governance.
8.3 Resilience: Was passiert, wenn Agenten ausfallen?
Bei klassischen Anwendungen gibt es etablierte Konzepte für Hochverfügbarkeit und Fehlerbehandlung.

Bei Agenten kommen weitere Herausforderungen hinzu:
- Ein Modellanbieter ist nicht erreichbar.
- Ein Agent liefert ein unvollständiges Ergebnis.
- Ein Tool funktioniert nicht.
- Ein Agent hängt in einer Endlosschleife.
- Eine Delegation schlägt fehl.
- Ein Agent überschreitet sein Kostenbudget.
- Eine Wissensquelle ist nicht verfügbar.
Ich würde folgende Resilience-Fähigkeiten definieren:
Fähigkeit	Zweck
Timeout Management	Verhindert unbegrenzt laufende Aufgaben
Retry Policies	Wiederholt vorübergehend fehlgeschlagene Aufrufe kontrolliert
Circuit Breaker	Unterbindet wiederholte Aufrufe eines fehlerhaften Dienstes
Fallback	Nutzt alternative Agenten oder einen klassischen Prozess
Checkpointing	Ermöglicht die Wiederaufnahme längerer Abläufe
Idempotency	Verhindert doppelte Aktionen
Dead Letter Handling	Behandelt nicht erfolgreich verarbeitete Nachrichten
Graceful Degradation	Ermöglicht einen eingeschränkten Prozessbetrieb

Ein konkretes Beispiel:

Ein Agent soll eine Mitarbeiteranfrage klassifizieren. Der Agent ist nicht verfügbar.

Der Prozess sollte deshalb nicht zwangsläufig komplett stehen bleiben.

Eine mögliche Fallback-Strategie wäre:
1. Ein alternativer Agent wird versucht.
2. Wenn auch dieser ausfällt, erfolgt eine regelbasierte oder manuelle Bearbeitung.
3. Der Prozess wird fortgesetzt.
4. Der Ausfall wird protokolliert.
8.4 Kosten- und Ressourcensteuerung
Das würde ich ebenfalls in den Betriebsbereich aufnehmen.

Agenten können Kosten verursachen durch:
- LLM-Aufrufe
- Embeddings
- Retrieval
- Tool-Aufrufe
- Mehrfache Agentenübergaben
- Lange Ausführungszeiten
- Wiederholte Reasoning-Schleifen
Bei Multi-Agent-Systemen kann sich der Aufwand schnell vervielfachen.

Ich würde deshalb ein Budgetmodell etablieren:
- Kostenbudget pro Agentenaufgabe
- Maximale Anzahl von Agentenübergaben
- Maximale Anzahl von Tool-Aufrufen
- Maximale Ausführungsdauer
- Token-Budgets
- Eskalationsregeln bei Überschreitung
Ein interessanter KPI wäre:

Cost per Successful HR Task

Also nicht nur die Kosten eines Agentenaufrufs, sondern die Kosten für eine tatsächlich erfolgreich abgeschlossene HR-Aufgabe.
8.5 Wer betreibt die Agentenlandschaft?
Ich würde zwischen drei Betriebsverantwortlichkeiten unterscheiden:
Verantwortungsbereich	Aufgabe
Agent Owner	Fachliche Verantwortung und Nutzen des Agenten
Platform / Runtime Owner	Technischer Betrieb der jeweiligen Agentenplattform
Orchestration / Enterprise Operations	Übergreifender Betrieb, Koordination und Governance

Zusätzlich braucht ihr eine übergreifende Instanz, die beispielsweise Agentenstandards, Freigaben und Betriebsanforderungen definiert.

Das könnte organisatorisch in einer HR AI Governance oder einem HR AI Platform Team angesiedelt werden.
8.6 Was sollte im Workshop entschieden werden?
1. Welchen Lifecycle muss jeder Agent durchlaufen?
2. Wie werden Agenten registriert und versioniert?
3. Wer darf Agenten produktiv setzen?
4. Wie organisieren wir den plattformübergreifenden Betrieb?
5. Welche Resilience-Mechanismen sind verpflichtend?
6. Welche Kostenlimits benötigen wir?
7. Wie funktionieren Fallbacks?
8. Wie werden Agenten deaktiviert und stillgelegt?
Ergebnis: Ein standardisierter Agent Lifecycle, ein Betriebsmodell und ein Resilience Framework.

9. Ein Thema, das ich zusätzlich als Querschnitt betrachten würde: HR AI Governance
Die Governance habe ich bewusst nicht als eigenständigen achten Themenblock aufgebaut, sondern in die einzelnen Themen integriert.

Ich würde sie aber im Workshop explizit als Querschnittsthema behandeln.

Warum?

Ihr habt sieben unterschiedliche Themen, aber zahlreiche Anforderungen gelten über alle hinweg:
- Datenschutz
- Informationssicherheit
- Compliance
- Verantwortlichkeiten
- Dokumentation
- Risikomanagement
- Transparenz
- Auditierbarkeit
Gerade in HR ist das entscheidend.
9.1 Ein übergreifendes Governance-Modell
Ich würde vier Governance-Dimensionen definieren:
Dimension	Leitfrage
Business Governance	Wer verantwortet den fachlichen Einsatz des Agenten?
Data Governance	Welche Daten darf der Agent verwenden und wie werden sie geschützt?
AI Governance	Welche Qualitäts-, Risiko- und Transparenzanforderungen gelten?
Technical Governance	Welche technischen Standards und Betriebsanforderungen muss der Agent erfüllen?

Ein wichtiger Punkt: Die Governance muss nicht zentral sämtliche Entscheidungen treffen.

Sie sollte vielmehr verbindliche Mindestanforderungen und Kontrollmechanismen definieren, die in den lokalen Plattformen umgesetzt werden.
9.2 Regulatorische Anforderungen früh berücksichtigen
Ich würde einen Legal-, Compliance- und Datenschutz-Vertreter bereits in die Architekturarbeit einbeziehen.

Insbesondere relevant sind:
- EU AI Act
- DSGVO
- Mitbestimmungsrechte und Betriebsverfassungsrecht
- Interne HR-Richtlinien
- Informationssicherheitsanforderungen
Bei KI-Anwendungen im Beschäftigungskontext ist die konkrete Zweckbestimmung entscheidend für die regulatorische Einstufung.

Gerade bei Recruiting, Bewerberauswahl und Entscheidungen über Beschäftigungsbedingungen muss geprüft werden, ob eine Hochrisiko-Einstufung vorliegt. Auch die konkreten Anforderungen und Übergangsfristen des EU AI Act sollten bei eurer Roadmap aktuell juristisch validiert werden. 

AI Act Service Desk


10. Wie würde ich den zweiten Workshop-Block gestalten?
Ich würde die sieben Vertiefungsthemen nicht einfach nacheinander präsentieren. Stattdessen würde ich mit konkreten HR-Anwendungsfällen arbeiten und daraus die notwendigen Architekturfähigkeiten ableiten.

Mein Vorschlag: Ein Workshop von ungefähr vier Stunden.
10.1 Agenda und Zeitplanung
Zeit	Thema	Arbeitsform
15 Min.	Einführung und Rückblick auf das Zielbild	Gemeinsames Verständnis
40 Min.	1. Agentic Process Design	Prozessbeispiel analysieren
35 Min.	2. Observability & Monitoring	KPI- und Monitoring-Konzept
35 Min.	3. Integration Layer	Integrationsarchitektur skizzieren
35 Min.	4. Ontologie & Semantic Layer	HR-Kernbegriffe und Datenflüsse
40 Min.	5. Identity, Security & HITL	Risikomodell entwickeln
35 Min.	6. Evaluation & Testing	Qualitäts- und Freigabekonzept
25 Min.	7. Operations & Lifecycle	Betriebsmodell definieren
20 Min.	Zusammenführung	Entscheidungen und offene Punkte

Gesamt: 4 Stunden 40 Minuten einschließlich kurzer Übergänge; bei vier Stunden würde ich die einzelnen Arbeitsphasen etwas kürzen oder zwei Themen teilweise parallel bearbeiten.
10.2 Meine Empfehlung für die Workshop-Methode
Ich würde einen konkreten HR-Prozess als roten Faden verwenden.

Dafür eignen sich beispielsweise:
- Recruiting und Bewerbermanagement
- Onboarding
- Mitarbeiteranfragen und HR Case Management
- Interner Positionswechsel
- Talent Management
Ich würde möglichst einen Prozess wählen, der mehrere eurer großen Systeme berührt.

Ein Beispiel könnte ein interner Positionswechsel sein:
Use Case: Interner Positionswechsel
1. Anfrage
   
   Führungskraft initiiert einen Positionswechsel in ServiceNow.
2. Analyse
   
   Ein Agent analysiert die Anfrage und prüft relevante Informationen aus Oracle.
3. Fachliche Prüfung
   
   Ein weiterer Agent recherchiert die relevanten HR-Richtlinien.
4. Freigabe
   
   Eine Führungskraft oder HR-Verantwortliche trifft die erforderliche Entscheidung.
5. Systemaktion
   
   Die Änderung wird kontrolliert in Oracle durchgeführt.
6. Abschluss
   
   ServiceNow erhält den Status und der Prozess wird abgeschlossen.

Anhand dieses einen Prozesses könnt ihr alle sieben Vertiefungsthemen diskutieren:
Thema	Frage am Use Case
Process Design	Wo wird welcher Agent eingebunden?
Monitoring	Wie erkennen wir Fehler und schlechte Ergebnisse?
Integration	Wie greift der Agent auf Oracle und ServiceNow zu?
Ontologie	Wie werden Mitarbeiter, Position und Organisation verstanden?
Security	Wer darf die Änderung vorbereiten und freigeben?
Evaluation	Wie testen wir die fachliche Richtigkeit?
Operations	Was passiert bei einem Ausfall oder einer fehlerhaften Agentenversion?

Das hat einen großen Vorteil: Ihr diskutiert nicht abstrakt über Architekturkomponenten, sondern über einen konkreten Prozess, der eure tatsächliche Systemlandschaft widerspiegelt.

11. Was sollte nach dem zweiten Workshop-Block vorliegen?
Ich würde sieben konkrete Arbeitsergebnisse erwarten.
1. Agentic Process Design Framework

Definierte Integrationsmuster für Agenten in HR-Prozessen sowie Regeln für Prozesszustände, Übergaben und Fehlerfälle.
2. Agent Observability Framework

Einheitliche Monitoring-Dimensionen, KPIs, Trace-Anforderungen und Eskalationsmechanismen.
3. Integration Target Architecture

Zielbild für APIs, Events, Business Services, MCP und die Anbindung der HR-Systeme.
4. HR Semantic Model Roadmap

Erste HR-Kernbegriffe, System-Mappings und Verantwortlichkeiten.
5. Agent Security & Autonomy Framework

Identitätsmodell, Berechtigungen, Autonomiestufen und Freigabeprinzipien.
6. Agent Evaluation Framework

Teststufen, Qualitätsmetriken, Evaluationsverfahren und Produktivfreigaben.
7. Agent Operations Model

Lifecycle, Betrieb, Versionierung, Resilienz und Verantwortlichkeiten.
Diese Ergebnisse bilden später eine sehr gute Grundlage für euren dritten Agenda-Punkt, also den Vergleich und die Auswahl konkreter Plattformen und Technologien.

12. Welche Themen würde ich priorisieren?
Nicht alle sieben Themen müssen sofort vollständig umgesetzt werden.

Ich würde zwischen Architekturvoraussetzungen, produktiven Mindestanforderungen und strategischen Weiterentwicklungen unterscheiden.
Thema	Vor den ersten produktiven Agenten	Mittelfristig	Perspektivisch
Agentic Process Design	Pflicht		
Observability	Pflicht		
Integration Layer	Pflicht		
Ontologie	Grundmodell	Ausbau	
Identity & Security	Pflicht		
Evaluation & Testing	Pflicht		
Operations & Lifecycle	Pflicht		
Knowledge Graph		Prüfen	Ausbau
Fortgeschrittene Agentenoptimierung		Prüfen	Ausbau

Meine Einschätzung: Ihr braucht keine vollständig ausgebaute Ontologie und kein hochkomplexes Agent Operations Center, bevor der erste Agent produktiv geht.

Aber ihr braucht von Anfang an klare Prinzipien und Mindestanforderungen.

Ein Beispiel: Eine zentrale HR-Ontologie kann schrittweise wachsen. Ein Berechtigungskonzept für einen Agenten, der Mitarbeiterdaten ändern darf, muss dagegen vor dem Produktiveinsatz stehen.

13. Meine zusätzlichen Empfehlungen für eure Vorbereitung
Ich würde vor dem Workshop noch drei Dinge vorbereiten.
A. Eine Übersicht eurer bestehenden Agenteninitiativen
Auch wenn noch keine Agenten produktiv sind, würde ich sämtliche geplanten Initiativen zusammentragen.

Für jede Initiative solltet ihr zumindest kennen:
- Fachlicher Use Case
- Betroffener HR-Prozess
- Geplante Agentenfähigkeiten
- Vorgesehene Plattform
- Betroffene HR-Systeme
- Benötigte Daten
- Geplante Autonomie
- Erwarteter Produktivstart
Das hilft enorm, weil ihr eure Zielarchitektur anhand realer Anforderungen validieren könnt.
B. Zwei bis drei repräsentative HR-Prozesse
Ich würde nicht nur einen Prozess betrachten.

Am besten nehmt ihr drei unterschiedliche Prozesscharakteristiken:
Prozess	Was lässt sich damit untersuchen?
Recruiting	Sensible Daten, Entscheidungsunterstützung, Avature, Oracle
HR Case Management	Agentenassistenz, ServiceNow, Wissenszugriff
Interner Positionswechsel	Systemübergreifende Prozesse, Freigaben, Oracle und ServiceNow

Damit stellt ihr sicher, dass euer Architekturkonzept nicht nur für einen einzelnen Agenten funktioniert.
C. Bestehende Integrations- und Governance-Architektur
Ich würde außerdem vorab klären:
- Welche API- und Integrationsplattformen existieren bereits?
- Gibt es einen Enterprise Service Bus oder eine Event-Plattform?
- Wie funktioniert euer Identity- und Access-Management?
- Welche zentralen Monitoring-Lösungen existieren?
- Welche Data-Governance-Standards gibt es?
- Welche AI-Governance-Vorgaben sind bereits definiert?
- Welche Anforderungen stellt der Datenschutz beziehungsweise die Mitbestimmung?
Das verhindert, dass ihr im Workshop Lösungen entwickelt, die es in eurem Unternehmen bereits gibt.

14. Weiterführende technische Grundlagen
Für die fachliche Vorbereitung der Vertiefungsthemen würde ich insbesondere diese Quellen empfehlen:
Themengebiet	Quelle
Prozess- und Multi-Agent-Architektur	Microsoft Azure Architecture Center
Agent Monitoring und Tracing	OpenTelemetry GenAI Agent Semantic Conventions
Verteiltes Monitoring	OpenTelemetry Trace Semantic Conventions
Agent Security	OWASP Top 10 for Agentic Applications 2026
HR AI Compliance	EU AI Act – Implementation Timeline

Besonders interessant finde ich für euren Monitoring-Ansatz die Entwicklung der OpenTelemetry-Semantic-Conventions für generative KI und Agenten. Sie berücksichtigen mittlerweile unter anderem Agent-Aufrufe, Workflow-Ausführungen, Planung, Tool-Ausführung und Retrieval. Das ist eine gute Grundlage, um eine herstellerübergreifende Telemetrie-Strategie zu entwickeln. Die Konventionen befinden sich allerdings teilweise noch in Entwicklung. 

GitHub+2


15. Mein Gesamtfazit: Was ist der entscheidende Gedanke hinter Punkt 2?
Ich würde die sieben Themen auf drei übergeordnete Fragen reduzieren:
Dimension 1
Integration
Wie werden Agenten Bestandteil unserer HR-Prozesse und wie greifen sie auf unsere Systeme und Daten zu?

Dazu gehören:
- Agentic Process Design
- Integration Layer
- Ontologie und Semantic Layer


Dimension 2
Control & Trust
Wie stellen wir sicher, dass Agenten zuverlässig, sicher, nachvollziehbar und in den richtigen Grenzen arbeiten?

Dazu gehören:
- Observability & Monitoring
- Identity, Security & Human-in-the-Loop
- Evaluation & Testing


Dimension 3
Operations & Scale
Wie entwickeln und betreiben wir eine wachsende, heterogene Agentenlandschaft nachhaltig?

Dazu gehören:
- Lifecycle Management
- Resilience
- Kosten- und Betriebssteuerung


Meine wichtigste Empfehlung: Ich würde aus Punkt 2 keinen reinen Technologie-Workshop machen. Es sollte ein gemeinsamer Architektur- und Betriebsmodell-Workshop werden, an dem HR, HR IT, Enterprise Architecture, Integration, Data Architecture, Informationssicherheit, Datenschutz und AI Governance beteiligt sind.

Denn die größte Herausforderung wird vermutlich nicht sein, einen Orchestrator technisch zum Laufen zu bringen. Sie wird sein, eine Vielzahl unterschiedlicher Agenten aus unterschiedlichen Plattformen so in eure HR-Prozesslandschaft einzubetten, dass ihr jederzeit wisst, was sie tun dürfen, was sie tatsächlich tun und ob sie ihre Aufgaben zuverlässig erfüllen.

Genau dafür sollte Punkt 2 die Grundlagen schaffen.

Eine mögliche Ergänzung für eure offizielle Agenda wäre deshalb:
2. Vertiefung der architektonischen und operativen Voraussetzungen
- Agentic Process Design: Integration von Agenten in bestehende HR-End-to-End-Prozesse
- Agent Observability: Monitoring, Qualitätsmessung, Tracing und Steuerung
- Enterprise Connectivity: Integration Layer, APIs, Events und standardisierte Agent-Tools
- HR Semantic Layer: Ontologie, Datenmodelle, Knowledge Graph und Context Management
- Security & Governance: Identity, Berechtigungen, Autonomie, Datenschutz und Human-in-the-Loop
- Agent Quality Engineering: Testing, Evaluation, Validierung und Produktivfreigabe
- Agent Operations: Lifecycle, Versionierung, Resilienz und Kostensteuerung

Damit habt ihr aus meiner Sicht einen sehr runden zweiten Workshop-Block, der direkt auf eurem Zielbild aus Punkt 1 aufbaut und euch gleichzeitig auf die Technologieentscheidung in Punkt 3 vorbereitet.