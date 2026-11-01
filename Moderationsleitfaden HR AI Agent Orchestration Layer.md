**Moderationsleitfaden: HR AI Agent Orchestration Layer**  
Für deine Rolle als Moderator würde ich die drei inhaltlichen Workshop-Abschnitte nicht als reine Präsentation verstehen, sondern als aufeinander aufbauende Diskussion:  
* Zielbild: Was wollen wir architektonisch und fachlich erreichen?  
* Vertiefungsthemen: Was muss gelöst werden, damit das Zielbild in der HR-Systemlandschaft funktioniert?  
* Umsetzungsoptionen: Mit welcher Plattform und welchem Vorgehen können wir das Zielbild realisieren?  
Deine wichtigste Aufgabe ist, die Diskussion immer wieder von einzelnen Produktfunktionen auf die übergeordnete Architekturfrage zurückzuführen. Es geht nicht darum, möglichst früh einen Anbieter auszuwählen, sondern zunächst zu verstehen, welche Fähigkeiten wir benötigen.  
**1. Abschnitt: Erarbeitung des Zielbilds**  
Höchste Priorität  
Das ist aus meiner Sicht der wichtigste Teil des Workshops. Hier sollte ausreichend Zeit eingeplant werden. Die späteren Plattformdiskussionen sind nur dann sinnvoll, wenn ihr euch vorher auf ein gemeinsames Zielbild und die wesentlichen Architekturprinzipien verständigt habt.  
**1.1 Ausgangslage und Problemstellung**  
Das solltest du als Moderator festhalten:  
* Wir haben aktuell noch keine produktiven HR-Agenten, aber mehrere Initiativen und Aktivitäten.  
* Erste Agenten werden voraussichtlich im ServiceNow- und Oracle-Umfeld entstehen.  
* HR-Prozesse laufen über mehrere Systeme und sind häufig systemübergreifend.  
* Die Systemlandschaft ist heterogen: ServiceNow, Oracle, Avature, ASES, Eigenentwicklungen und weitere Anbieter.  
* Es besteht das Risiko, dass isolierte Agentenlösungen entstehen, die jeweils nur innerhalb ihrer Plattform funktionieren.  
* Wir müssen deshalb frühzeitig überlegen, wie diese Agenten später miteinander interagieren und gemeinsam HR-Prozesse bearbeiten können.  
Worauf du besonders eingehen solltest:  
Das zentrale Problem ist nicht, dass uns ein einzelner besonders intelligenter Agent fehlt. Die Herausforderung ist vielmehr, dass verschiedene Agenten und Systeme zukünftig zusammenarbeiten müssen.  
Ein Beispiel:  
Ein Mitarbeiter stellt eine Anfrage über das HR-Portal. Zur Bearbeitung werden Informationen aus Oracle benötigt, eine HR-Richtlinie muss geprüft werden und anschließend muss gegebenenfalls eine Änderung in einem anderen System erfolgen.  
Ein einzelner Agent kann möglicherweise nur einen Teil dieser Aufgabe übernehmen. Es braucht also eine übergreifende Koordination.  
Diskussionsfrage:  
„Gehen wir davon aus, dass wir zukünftig zahlreiche spezialisierte Agenten in unterschiedlichen HR-Systemen haben: Was muss vorhanden sein, damit diese Agenten gemeinsam einen Ende-zu-Ende-Prozess bearbeiten können?“  
**1.2 Was verstehen wir unter einem HR Orchestration Layer?**  
Hier solltest du zunächst ein gemeinsames Verständnis herstellen.  
Ein Orchestration Layer ist eine übergreifende Koordinationsschicht, die Agenten, Systeme, Tools und Prozesse miteinander verbindet.  
Er soll insbesondere:  
* Aufgaben erkennen und in Teilaufgaben zerlegen.  
* Geeignete Agenten und Services identifizieren.  
* Aufgaben an die richtigen Agenten delegieren.  
* Ergebnisse unterschiedlicher Agenten zusammenführen.  
* Kontext und Informationen kontrolliert weitergeben.  
* Prozesszustände und offene Aufgaben nachhalten.  
* Menschliche Freigaben und Eskalationen ermöglichen.  
* Sicherheit, Berechtigungen und Governance gewährleisten.  
* Die Ausführung und Qualität der Agenten überwachen.  
Wichtige Abgrenzung:  
Der Orchestrator muss nicht selbst alle fachlichen Aufgaben erledigen. Er muss auch nicht alle HR-Prozesse selbst abbilden.  
Er ist primär für die Koordination zuständig.  
Das ist eine wichtige Unterscheidung, weil sonst schnell die Vorstellung eines zentralen „Super-Agenten“ entsteht, der sämtliche HR-Prozesse und Systeme kontrolliert.  
Meine Moderationsempfehlung:  
Stelle bewusst die Frage:  
„Wollen wir einen zentralen Agenten, der alles selbst steuert, oder eine Architektur, in der spezialisierte Agenten eigenständig arbeiten und zentral koordiniert werden?“  
Meine Empfehlung wäre die zweite Variante.  
**1.3 Architekturprinzip: Föderierte Hybridarchitektur**  
Zentrale Arbeitshypothese  
Ich würde dieses Architekturmodell als Ausgangshypothese in den Workshop mitnehmen.  
Grundgedanke:  
Die einzelnen HR-Plattformen behalten ihre fachliche Eigenständigkeit. Eine zentrale Orchestrierung übernimmt nur die Aufgaben, die über System- und Domänengrenzen hinweg koordiniert werden müssen.  

| Ebene | Aufgabe | Beispiel |
| -------------------------- | ------------------------------------------ | ----------------------------------------- |
| Lokale Agentendomäne | Fachliche Aufgaben und lokale Prozesslogik | ServiceNow-Agent, Oracle-Agent |
| Zentraler HR Orchestrator | Systemübergreifende Koordination | Delegation zwischen Oracle und ServiceNow |
| Governance / Control Plane | Einheitliche Regeln und Kontrollen | Registry, Identity, Security, Monitoring |
| Integration Layer | Technische Verbindung | APIs, Events, MCP, A2A |
| HR-Systeme und Daten | Führende Datenhaltung und Transaktionen | Mitarbeiterdaten in Oracle |
  
Leitprinzip:  
„So lokal wie möglich orchestrieren, so zentral wie nötig koordinieren.“  
**Worauf du besonders eingehen solltest**  
Die zentrale Frage ist die Verteilung der Verantwortung.  
* Welche Entscheidungen trifft der lokale Agent?  
* Welche Entscheidungen trifft der zentrale Orchestrator?  
* Wer besitzt den fachlichen Prozesszustand?  
* Wer ist für die Berechtigungen verantwortlich?  
* Wo werden Informationen und Ergebnisse gespeichert?  
Ein wichtiger Punkt: Der zentrale Orchestrator muss nicht zum neuen System of Record werden. Die führenden HR-Systeme sollten weiterhin ihre fachliche Datenverantwortung behalten.  
Diskussionsfragen:  
* Welche Aufgaben sollen zwingend zentral koordiniert werden?  
* Welche Aufgaben sollen in ServiceNow bzw. Oracle verbleiben?  
* Soll der zentrale Orchestrator direkt mit allen Agenten sprechen oder bevorzugt lokale Orchestratoren ansprechen?  
* Wo liegt die Verantwortung für einen systemübergreifenden Prozess?  
**1.4 Welche Kernfähigkeiten muss der Orchestrator haben?**  
Hier würde ich die Diskussion in sechs Fähigkeiten strukturieren.  

| Fähigkeit | Bedeutung | Worauf du achten solltest |
| --------------------- | ------------------------------------- | ------------------------------------------------------ |
| Agent Registry | Agenten und ihre Fähigkeiten kennen | Wie finden wir den richtigen Agenten? |
| Routing & Delegation | Aufgaben verteilen | Wer entscheidet über die Zuständigkeit? |
| Context Management | Kontext weitergeben | Welche Informationen dürfen übertragen werden? |
| State Management | Prozesszustände verwalten | Wie behalten wir den Überblick über laufende Aufgaben? |
| Result Validation | Ergebnisse prüfen | Wie gehen wir mit widersprüchlichen Ergebnissen um? |
| Governance & Security | Regeln und Berechtigungen durchsetzen | Wer darf was ausführen? |
  
**A. Agent Registry und Discovery**  
Die Registry ist ein zentrales Verzeichnis aller verfügbaren Agenten.  
Sie sollte nicht nur Namen und technische Endpunkte enthalten, sondern auch:  
* fachliche Fähigkeiten,  
* unterstützte Aufgaben,  
* Eingabe- und Ausgabeformate,  
* verantwortliche Owner,  
* benötigte Berechtigungen,  
* unterstützte Protokolle,  
* Risikoklasse,  
* Version und Freigabestatus.  
Diskussionsfrage:  
„Woher weiß unser Orchestrator, dass es beispielsweise einen Oracle-Agenten gibt, der Mitarbeiter- und Positionsdaten abfragen kann?“  
**B. Routing und Delegation**  
Der Orchestrator muss entscheiden können, welcher Agent eine Aufgabe am besten erledigt.  
Beispielsweise:  
* Mitarbeiterdaten → Oracle-Agent  
* HR-Richtlinien → HR Policy Agent  
* Employee Case → ServiceNow-Agent  
* Recruiting-Daten → Avature-Service oder -Agent  
Wichtig ist, dass die Auswahl nicht nur anhand der fachlichen Fähigkeit erfolgt. Auch Berechtigungen, Verfügbarkeit, Kosten und Qualität können eine Rolle spielen.  
**C. Context Management**  
Ein Agent benötigt Informationen, um seine Aufgabe zu erfüllen.  
Beispiel:  
Ein Oracle-Agent soll prüfen, ob ein Mitarbeiter eine bestimmte Funktion innehat. Dafür benötigt er die Mitarbeiter-ID und die konkrete Fragestellung, aber nicht zwingend den gesamten Gesprächsverlauf oder alle weiteren HR-Daten.  
Dein Fokus sollte sein:  
* Welche Informationen werden übergeben?  
* Welche Informationen dürfen übergeben werden?  
* Wie werden Herkunft und Aktualität kenntlich gemacht?  
* Wie vermeiden wir unnötige personenbezogene Daten?  
**D. State Management**  
Das ist ein besonders wichtiger Punkt, der häufig unterschätzt wird.  
Ein systemübergreifender HR-Prozess kann mehrere Minuten, Stunden oder Tage dauern. Der Orchestrator muss deshalb wissen:  
* Welche Aufgaben wurden bereits erledigt?  
* Welche Agenten arbeiten noch?  
* Wo wird auf eine menschliche Freigabe gewartet?  
* Welche Ergebnisse liegen bereits vor?  
* Was passiert bei einem Fehler?  
* Wie kann ein Prozess wieder aufgenommen werden?  
Wichtige Abgrenzung: Der zentrale Orchestrator hält den Koordinationszustand. Die fachlichen Zustände und Transaktionen bleiben grundsätzlich in den jeweiligen führenden Systemen.  
**E. Result Validation**  
Ein Agentenergebnis sollte nicht ungeprüft an den nächsten Agenten weitergereicht werden.  
Beispielsweise muss geprüft werden:  
* Ist das Ergebnis vollständig?  
* Ist es strukturiert und technisch verwertbar?  
* Sind Quellen und Aktualität nachvollziehbar?  
* Gibt es Widersprüche?  
* Ist die Antwort ausreichend sicher für die nächste Aktion?  
**F. Governance und Security**  
Das ist insbesondere im HR-Umfeld entscheidend.  
Ein Agent darf nicht automatisch alle Daten und Funktionen nutzen, nur weil er technisch darauf zugreifen könnte.  
Zu diskutieren sind:  
* Identität und Berechtigungen,  
* Datenzugriff,  
* Delegation von Berechtigungen,  
* Freigabeprozesse,  
* Auditierbarkeit,  
* Umgang mit sensiblen Aktionen.  
**1.5 Welche Orchestrierungsmuster benötigen wir?**  
Hier solltest du vermitteln, dass nicht jeder Prozess gleich orchestriert werden muss.  

| Muster | Beschreibung | HR-Beispiel |
| ---------------- | ---------------------------------------------------------- | -------------------------------------------------------- |
| Sequenziell | Agenten arbeiten nacheinander | Mitarbeiterdaten abrufen, anschließend Richtlinie prüfen |
| Parallel | Agenten arbeiten gleichzeitig | Mitarbeiterdaten und HR-Richtlinien parallel abfragen |
| Supervisor | Übergeordnete Instanz koordiniert Agenten | HR Orchestrator verteilt Aufgaben |
| Handoff | Übergabe an anderen Agenten oder Menschen | Sensible Änderung benötigt Freigabe |
| Workflow + Agent | Workflow steuert Prozess, Agent erledigt flexible Aufgaben | Case-Prozess mit agentischer Klassifikation |
  
Meine Empfehlung:  
Ein hybrides Modell sollte der Standard sein.  
* Deterministische Workflows für verbindliche Prozessschritte, Regeln, Fristen und Transaktionen.  
* Agenten für Interpretation, Klassifikation, Informationsbeschaffung und flexible Entscheidungen.  
* Menschliche Freigaben für risikoreiche Aktionen.  
Diskussionsfrage:  
„Welche HR-Prozessschritte müssen immer deterministisch bleiben und an welchen Stellen können Agenten eigenständig agieren?“  
**1.6 Wie gehen wir mit Wissen und Daten um?**  
Hier ist eine klare Unterscheidung wichtig.  

| Informationsart | Beispiele | Grundsätzliche Verantwortung |
| ------------------ | ------------------------------------------ | ------------------------------------- |
| HR-Wissen | Richtlinien, Betriebsvereinbarungen, FAQs | Fachlich verantwortete Wissensquellen |
| Operative HR-Daten | Mitarbeiter, Positionen, Organisationen | Führende HR-Systeme |
| Laufzeitkontext | Aktuelle Anfrage, Teilaufgaben, Ergebnisse | Orchestrator bzw. Prozesslaufzeit |
  
Worauf du eingehen solltest:  
Wir sollten nicht versuchen, alle HR-Daten zentral zu kopieren und in einem großen Agenten-Wissensspeicher abzulegen.  
Stattdessen sollten Agenten auf die jeweils benötigten Daten und Wissensquellen zugreifen. Der Zugriff muss kontrolliert, nachvollziehbar und zweckgebunden erfolgen.  
Ein besonders wichtiger Punkt ist die HR-Semantik: Ein Begriff wie „Position“, „Stelle“, „Job“ oder „Rolle“ kann in verschiedenen Systemen unterschiedlich verwendet werden.  
Eine gemeinsame HR-Ontologie kann helfen, diese Begriffe einheitlich zu interpretieren.  
**1.7 Welche Protokolle brauchen wir?**  
Du solltest hier vor allem die unterschiedlichen Rollen der Protokolle erklären.  

| Technologie | Hauptzweck | Typischer Einsatz |
| ------------------ | ------------------------------------------- | ------------------------------------------ |
| REST / APIs | System- und Serviceintegration | Mitarbeiterdaten abrufen |
| Events / Messaging | Asynchrone Kommunikation | Statusänderung mitteilen |
| MCP | Tools und Kontext für Agenten bereitstellen | Agent nutzt HR-Service |
| A2A | Kommunikation zwischen Agenten | Agent delegiert Aufgabe an anderen Agenten |
  
Wichtige Botschaft:  
MCP und A2A sind keine vollständigen Ersatzlösungen für Enterprise Integration. Sie ergänzen APIs, Events und bestehende Integrationsplattformen.  
Diskussionsfragen:  
* Welche Protokolle wollen wir unternehmensweit unterstützen?  
* Wo verwenden wir APIs und wo MCP?  
* Wann ist eine direkte Agent-zu-Agent-Kommunikation sinnvoll?  
* Brauchen wir einen zentralen Gateway-Ansatz?  
**1.8 Welche Entscheidungen sollten am Ende des Zielbild-Abschnitts stehen?**  
Versuche, die Diskussion auf folgende Ergebnisse zu verdichten:  

| Entscheidung       | Gewünschtes Ergebnis                            |
| ------------------ | ----------------------------------------------- |
| Architekturmodell  | Föderiert, zentral oder hybrid                  |
| Zentrale Aufgaben  | Klare Verantwortlichkeiten des Orchestrators    |
| Lokale Aufgaben    | Abgrenzung zu ServiceNow und Oracle             |
| Kernfähigkeiten    | Priorisierte Fähigkeiten                        |
| Agentenmodell      | Registry und Discovery                          |
| Prozesszustand     | Abgrenzung zwischen zentralem und lokalem State |
| Wissen und Kontext | Grundprinzipien für Daten und Wissenszugriff    |
| Protokolle         | API-, Event-, MCP- und A2A-Strategie            |
| Governance         | Security, Autonomie, Freigaben und Audit        |
  
Mein wichtigster Moderationstipp:  
Versuche nicht, alle technischen Detailfragen abschließend zu beantworten. Ziel ist ein gemeinsames Architekturverständnis und eine Liste von Entscheidungen, offenen Punkten und Hypothesen.  
**2. Abschnitt: Vertiefungsthemen**  
In diesem Abschnitt geht es darum, die zuvor entwickelte Architektur auf konkrete Herausforderungen im HR-Alltag herunterzubrechen.  
Ich würde die vier Themen nacheinander behandeln und jeweils mit einem konkreten HR-Beispiel arbeiten.  
**2.1 Agenten in HR-Prozesse integrieren**  
**Kernaussage**  
Agenten sollten nicht isoliert neben den bestehenden HR-Prozessen betrieben werden. Sie müssen gezielt in bestehende Prozessketten eingebunden werden.  
Ein HR-Prozess sollte weiterhin einen klaren fachlichen Owner und definierte Prozessregeln haben. Agenten übernehmen ausgewählte Aufgaben innerhalb dieses Prozesses.  
**Beispiel: Employee Service Request**  
* Mitarbeiter stellt eine Anfrage in ServiceNow.  
* ServiceNow klassifiziert das Anliegen.  
* Der Orchestrator erkennt, dass Oracle-Daten benötigt werden.  
* Ein Oracle-Agent ruft die erforderlichen Informationen ab.  
* Ein Policy Agent prüft die einschlägige HR-Richtlinie.  
* Der Orchestrator führt die Ergebnisse zusammen.  
* Bei einer sensiblen Aktion wird eine Freigabe eingeholt.  
* Oracle führt die Aktion aus.  
* ServiceNow erhält das Ergebnis und aktualisiert den Case.  
**Worauf du besonders eingehen solltest**  
1. Prozessverantwortung  
Wer ist für den Ende-zu-Ende-Prozess verantwortlich? Der HR-Prozessowner oder der Plattformbetreiber?  
Meine Empfehlung: Die fachliche Prozessverantwortung sollte beim HR-Prozessowner bleiben.  
2. Fehlerbehandlung  
Was passiert, wenn ein Agent nicht antwortet, falsche Daten liefert oder ein System nicht erreichbar ist?  
Du solltest auf folgende Mechanismen eingehen:  
* Timeouts  
* Retries  
* alternative Agenten oder Services  
* Eskalation  
* Abbruch und Wiederaufnahme  
* manuelle Bearbeitung  
3. Human in the Loop  
Welche Prozessschritte benötigen eine menschliche Entscheidung?  
Nicht jede Agentenentscheidung sollte automatisch ausgeführt werden. Besonders bei sensiblen HR-Änderungen sollte die Freigabelogik klar definiert sein.  
4. Schnittstellen und Verantwortlichkeiten  
Jeder Agent sollte klar definierte Aufgaben, Eingaben, Ausgaben und Grenzen besitzen.  
**Gute Diskussionsfragen**  
* Welche HR-Prozesse eignen sich als erste Kandidaten?  
* Wo sehen wir den größten Nutzen durch Agenten?  
* Welche Prozessschritte sollen weiterhin durch klassische Workflows gesteuert werden?  
* Wo benötigen wir menschliche Freigaben?  
* Wer trägt die Verantwortung, wenn mehrere Agenten an einem Prozess beteiligt sind?  
Moderationshinweis: Vermeide es, zu früh in einzelne Use Cases abzutauchen. Zunächst sollten Integrationsprinzipien festgelegt werden. Danach kann ein Pilotprozess ausgewählt werden.  
**2.2 Monitoring, Evaluation und Governance**  
**Kernaussage**  
Ein Agentenökosystem benötigt deutlich mehr Monitoring als eine klassische Schnittstellenlandschaft.  
Bei klassischen Schnittstellen reicht es häufig, technische Verfügbarkeit und Fehlerraten zu überwachen. Bei Agenten muss zusätzlich bewertet werden, ob die Ergebnisse fachlich korrekt, vollständig und regelkonform sind.  
**Was sollte überwacht werden?**  

| Bereich                  | Beispiele für Kennzahlen                       |
| ------------------------ | ---------------------------------------------- |
| Technische Verfügbarkeit | Erreichbarkeit, Fehlerquote                    |
| Performance              | Antwortzeit, Prozessdauer                      |
| Kosten                   | Token-Verbrauch, Kosten pro Prozess            |
| Qualität                 | Korrektheit, Vollständigkeit, Ergebnisqualität |
| Governance               | Policy-Verstöße, unzulässige Zugriffe          |
| Prozess                  | Abbruchquote, Eskalationen, Freigaben          |
| Agentennutzung           | Aufrufhäufigkeit, Erfolgsquote                 |
  
**Besonders wichtig: End-to-End-Tracing**  
Wenn ein Prozess mehrere Agenten und Systeme durchläuft, muss nachvollziehbar sein, was passiert ist.  
Beispiel:  
* ServiceNow hat den Prozess gestartet.  
* Der zentrale Orchestrator hat einen Oracle-Agenten aufgerufen.  
* Der Oracle-Agent hat eine Datenabfrage durchgeführt.  
* Ein Policy Agent hat eine Richtlinie geprüft.  
* Ein Mensch hat eine Aktion freigegeben.  
* Oracle hat die Änderung ausgeführt.  
Jeder Schritt sollte einer gemeinsamen Prozess- bzw. Korrelations-ID zugeordnet werden können.  
**Evaluation**  
Neben technischem Monitoring braucht es regelmäßige Qualitätsprüfungen.  
Dazu gehören:  
* definierte Testfälle,  
* Bewertung der fachlichen Ergebnisqualität,  
* Prüfung von Halluzinationen und falschen Aussagen,  
* Regressionstests bei Änderungen,  
* Überprüfung der Einhaltung von Policies,  
* regelmäßige fachliche Reviews.  
**Governance-Fragen**  
* Wer darf einen neuen Agenten produktiv setzen?  
* Wer ist für die fachliche Qualität verantwortlich?  
* Wie werden Änderungen und neue Versionen freigegeben?  
* Welche Aktionen müssen protokolliert werden?  
* Wie werden Agenten bei Qualitätsproblemen deaktiviert?  
Worauf du besonders eingehen solltest:  
Governance darf nicht erst nach dem Aufbau der Agentenlandschaft entstehen. Sie muss von Anfang an Bestandteil der Architektur sein.  
Ein sinnvoller Ansatz ist eine gemeinsame Control Plane, die Standards vorgibt, während die technischen Laufzeiten weiterhin in den jeweiligen Plattformen liegen können.  
**2.3 Enterprise Integration Layer**  
**Kernaussage**  
Der Integration Layer ist eine der wichtigsten technischen Voraussetzungen für die übergreifende Zusammenarbeit der Agenten.  
Er sorgt dafür, dass Agenten nicht für jedes System eigene, individuelle Integrationen benötigen.  
**Typische Bausteine**  

| Baustein                | Aufgabe                                        |
| ----------------------- | ---------------------------------------------- |
| API Management          | APIs bereitstellen und absichern               |
| Event Bus               | Asynchrone Kommunikation                       |
| MCP Gateway             | Tools für Agenten standardisiert bereitstellen |
| A2A Gateway / Endpunkte | Agentenkommunikation ermöglichen               |
| Adapter                 | Systeme technisch anbinden                     |
| Identity und Security   | Zugriffe kontrollieren                         |
| Monitoring              | Kommunikation nachvollziehen                   |
  
**Wichtige Architekturentscheidung**  
Soll eine neue Integrationsplattform für Agenten entstehen oder wird die bestehende Enterprise Integration Plattform erweitert?  
Meine Empfehlung: Bestehende Integrationsfähigkeiten möglichst nutzen und um agentenspezifische Funktionen ergänzen.  
Es sollte keine parallele Integrationslandschaft entstehen, die später unabhängig betrieben werden muss.  
**Diskussionsfragen**  
* Welche Integrationsplattform ist heute bereits etabliert?  
* Welche Standards existieren bereits für APIs und Events?  
* Wie werden MCP-Server und A2A-Endpunkte bereitgestellt?  
* Wie erfolgt die Authentifizierung zwischen Agenten?  
* Wie werden Zugriffe und Datenflüsse nachvollziehbar gemacht?  
* Wer ist für die Schnittstellen verantwortlich?  
**Worauf du besonders eingehen solltest**  
MCP und A2A sind wichtige neue Bausteine, aber kein Grund, bestehende Integrationsarchitekturen grundsätzlich infrage zu stellen.  
Die entscheidende Frage lautet: Wie integrieren wir Agenten in unsere Enterprise-Architektur, ohne neue Silos aufzubauen?  
**2.4 HR-Ontologie und semantische Ebene**  
**Kernaussage**  
Agenten müssen die fachliche Bedeutung von Informationen verstehen, auch wenn diese in verschiedenen Systemen unterschiedlich bezeichnet oder strukturiert sind.  
Ein Beispiel:  
* In Oracle existiert ein bestimmtes Datenmodell für Mitarbeiter und Positionen.  
* In ServiceNow werden andere Begriffe und Objekte verwendet.  
* Avature arbeitet mit Recruiting- und Kandidatenobjekten.  
* Ein Agent muss trotzdem verstehen können, welche fachlichen Zusammenhänge bestehen.  
**Was ist eine HR-Ontologie?**  
Eine HR-Ontologie ist ein gemeinsames fachliches Begriffs- und Beziehungsmodell.  
Sie beschreibt beispielsweise:  
* Person  
* Mitarbeiter  
* Beschäftigungsverhältnis  
* Position  
* Stelle  
* Organisationseinheit  
* Führungskraft  
* Team  
* Bewerbung  
* Kandidat  
* Recruiting-Prozess  
* Abwesenheit  
* Vergütung  
Sie definiert außerdem die Beziehungen zwischen diesen Begriffen.  
**Warum ist das wichtig?**  
Ohne gemeinsame Semantik besteht das Risiko, dass Agenten:  
* Begriffe unterschiedlich interpretieren,  
* Informationen falsch zuordnen,  
* Daten aus unterschiedlichen Systemen falsch zusammenführen,  
* falsche Schlussfolgerungen ziehen.  
**Was sollte im Workshop geklärt werden?**  
* Gibt es bereits ein HR-Datenmodell oder ein gemeinsames Begriffsmodell?  
* Welche Begriffe sind systemübergreifend besonders relevant?  
* Welche Datenobjekte werden für den ersten Pilot benötigt?  
* Wer verantwortet die fachlichen Definitionen?  
* Wie können bestehende Datenmodelle und Stammdatenstandards genutzt werden?  
Meine Empfehlung:  
Keine große HR-Ontologie als Vorbedingung für den Start aufbauen.  
Stattdessen mit einem kleinen, konkreten semantischen Modell für den ersten Cross-System-Pilot beginnen und dieses schrittweise erweitern.  
**2.5 Was sollte am Ende des Vertiefungsabschnitts stehen?**  

| Thema              | Gewünschtes Ergebnis                                 |
| ------------------ | ---------------------------------------------------- |
| Prozessintegration | Integrationsprinzipien und erste geeignete Use Cases |
| Monitoring         | Anforderungen an Observability und Evaluation        |
| Governance         | Rollen, Freigaben und Kontrollmechanismen            |
| Integration Layer  | Grundsätzliche Integrationsstrategie                 |
| HR-Ontologie       | Vorgehen und erste relevante Begriffe                |
  
Wichtiger Moderationshinweis:  
Die vier Themen hängen eng zusammen. Versuche, sie nicht isoliert zu behandeln.  
Beispiel: Eine Agentenübergabe benötigt nicht nur eine Schnittstelle. Sie benötigt auch eine Identität, Berechtigungen, Kontext, einen Prozesszustand und Monitoring.  
Genau diese Zusammenhänge solltest du sichtbar machen.  
**3. Abschnitt: Konkrete Umsetzungsoptionen**  
Entscheidungsvorbereitung  
In diesem Abschnitt wechselst du von der Architekturperspektive zur konkreten Umsetzung.  
Die zentrale Frage ist nicht: „Welches Produkt hat die meisten Agentenfunktionen?“  
Sondern:  
„Welche Plattform oder Kombination von Plattformen kann unser zuvor definiertes Zielbild am besten unterstützen?“  
**3.1 Die fünf relevanten Optionen**  
A. ServiceNow-zentriert  
ServiceNow übernimmt die zentrale Orchestrierung und nutzt seine nativen Workflow-, Agenten- und Integrationsfähigkeiten.  
B. Microsoft-zentriert  
Microsoft Foundry und Agent Framework bilden die Basis für eine zentrale, flexible Orchestrierung.  
C. Azure mit LangGraph  
Eigene, maßgeschneiderte Orchestrierung auf Basis eines flexiblen Agentenframeworks.  
D. AWS / AgentCore  
Modulare Agentenlaufzeit und Integrationsbausteine auf AWS.  
E. Föderierte Hybridarchitektur  
Lokale Agentenplattformen bleiben bestehen und werden über eine zentrale Orchestrierung verbunden.  
**3.2 Option A: ServiceNow-zentriert**  
**Grundidee**  
ServiceNow wird zur zentralen Plattform für die Orchestrierung von HR-Agenten und Workflows.  
Mögliche Bausteine:  
* AI Agent Orchestrator  
* AI Agent Studio  
* Workflow Studio / Flow Designer  
* HR Service Delivery  
* Integration Hub  
* AI Control Tower bzw. aktuelle Control-Tower-Angebote  
**Vorteile**  
* ServiceNow ist bereits Teil der HR-Systemlandschaft.  
* Gute Nähe zu HR-Service-Prozessen und bestehenden Workflows.  
* Potenziell einfacher Einstieg für erste produktive Use Cases.  
* Integration in die bestehende ServiceNow-Plattform.  
**Nachteile und offene Fragen**  
* Wie gut können externe Agenten aus Oracle oder anderen Plattformen eingebunden werden?  
* Können externe Agenten als eigenständige Akteure orchestriert werden?  
* Wie weit reicht die Governance über die eigene Plattform hinaus?  
* Wie stark entsteht eine Abhängigkeit von ServiceNow?  
* Wie entwickelt sich das Lizenzmodell?  
Worauf du besonders eingehen solltest:  
ServiceNow ist ein sehr naheliegender Kandidat für die Prozessintegration. Das bedeutet aber nicht automatisch, dass ServiceNow auch der beste zentrale Orchestrator für eine heterogene Agentenlandschaft ist.  
Die Cross-Platform-Fähigkeit muss konkret nachgewiesen werden.  
**3.3 Option B: Microsoft-zentriert**  
**Grundidee**  
Microsoft Foundry stellt die Agentenlaufzeit und Plattformfunktionen bereit. Das Microsoft Agent Framework kann die Orchestrierungslogik übernehmen.  
Weitere Bausteine:  
* Azure API Management  
* Logic Apps und Durable Functions  
* Event Grid und Service Bus  
* Entra ID  
* Key Vault  
* Azure Monitor / Application Insights  
* Azure AI Search  
**Vorteile**  
* Gute Kombination aus Managed Services und eigener Orchestrierungslogik.  
* Umfangreiche Enterprise-Integrationsmöglichkeiten.  
* Identity und Security können in die bestehende Microsoft-Welt eingebettet werden.  
* Unterstützung unterschiedlicher Agentenframeworks und Integrationsmuster.  
* Gute Möglichkeit, eine zentrale Orchestrierung unabhängig von einzelnen HR-Systemen aufzubauen.  
**Nachteile und offene Fragen**  
* Relativ komplexe Produktlandschaft.  
* Klärung der Verantwortungsgrenzen zwischen Foundry, Agent Framework und Azure-Diensten.  
* Integration nativer ServiceNow- und Oracle-Agenten muss praktisch geprüft werden.  
* Abhängigkeit von Azure und entsprechendes Kostenmodell.  
Meine Einschätzung:  
Microsoft ist ein sehr interessanter Kandidat für die zentrale Orchestrierung, insbesondere wenn eine flexible, systemübergreifende Architektur gewünscht ist.  
Ich würde Microsoft im Workshop als einen der führenden Kandidaten für einen PoC betrachten, aber noch keine finale Plattformentscheidung treffen.  
**3.4 Option C: Azure mit LangGraph**  
**Grundidee**  
LangGraph wird als Framework für die individuelle Orchestrierung komplexer Agentenabläufe genutzt.  
Es ermöglicht:  
* graphbasierte Workflows,  
* zustandsbehaftete Prozesse,  
* bedingtes Routing,  
* parallele Agentenaufrufe,  
* Checkpointing,  
* Human-in-the-loop,  
* Wiederaufnahme nach Unterbrechungen.  
**Vorteile**  
* Sehr flexibel.  
* Hohe Kontrolle über die Orchestrierungslogik.  
* Gut für komplexe und individuelle HR-Prozesse.  
* Weniger Bindung an einen einzelnen Agentenplattformanbieter.  
**Nachteile**  
LangGraph ist kein vollständiges Enterprise-Plattformprodukt.  
Zusätzlich benötigt werden beispielsweise:  
* Runtime und Deployment,  
* Datenbank und State Persistence,  
* Agent Registry,  
* Identity und Security,  
* Policy Engine,  
* API Management,  
* Monitoring und Evaluation.  
Worauf du besonders eingehen solltest:  
LangGraph bietet viel Flexibilität, aber die Organisation muss deutlich mehr selbst bauen und betreiben.  
Es ist daher wichtig, zwischen technischer Flexibilität und tatsächlichem Betriebsaufwand zu unterscheiden.  
**3.5 Option D: AWS / Amazon Bedrock AgentCore**  
**Grundidee**  
AWS stellt mit AgentCore modulare Bausteine für den Betrieb und die Integration von Agenten bereit.  
Dazu gehören:  
* AgentCore Runtime  
* Gateway  
* Identity  
* Memory  
* Observability  
* Evaluations  
**Vorteile**  
* Framework- und modellübergreifender Ansatz.  
* Gute Bausteine für Agentenlaufzeit und Tool-Integration.  
* MCP-Unterstützung und Möglichkeiten zur Integration anderer Agenten.  
* Modulare Architektur.  
**Nachteile und offene Fragen**  
* Zusätzliche Cloud-Plattform.  
* Integration in die bestehende IT-Landschaft.  
* Betriebs- und Kompetenzaufbau.  
* Strategische Passung zu bestehenden Cloud-Standards.  
Worauf du eingehen solltest:  
AWS ist eine technisch relevante Alternative, wenn AWS bereits strategisch genutzt wird oder entsprechende Kompetenzen vorhanden sind.  
Falls Azure die etablierte Plattform ist, muss der zusätzliche Nutzen einer AWS-basierten Orchestrierung besonders gut begründet werden.  
**3.6 Option E: Föderierte Hybridarchitektur**  
**Grundidee**  
Diese Option ist weniger ein einzelnes Produkt als vielmehr das übergreifende Architekturmodell.  
* ServiceNow bleibt für seine nativen HR-Agenten und Workflows zuständig.  
* Oracle bleibt für seine fachlichen Agenten und Business-Objekte zuständig.  
* Ein zentraler Orchestrator koordiniert systemübergreifende Aufgaben.  
* Eine gemeinsame Governance-Schicht stellt einheitliche Standards sicher.  
* Der Integration Layer verbindet alle Plattformen.  
**Vorteile**  
* Nutzt vorhandene Plattforminvestitionen.  
* Verhindert, dass ein einzelner Anbieter die gesamte Architektur kontrolliert.  
* Ermöglicht lokale Autonomie und zentrale Koordination.  
* Unterstützt eine schrittweise Einführung.  
* Kann mit unterschiedlichen Agentenframeworks erweitert werden.  
**Nachteile**  
* Höhere Anforderungen an Architektur und Governance.  
* Verantwortlichkeiten müssen sauber definiert werden.  
* Integration und Betrieb sind komplexer als in einer vollständig geschlossenen Plattform.  
* Gemeinsame Standards müssen konsequent etabliert werden.  
Meine Empfehlung:  
Die föderierte Hybridarchitektur sollte als Zielbild unabhängig von der konkreten Plattformentscheidung betrachtet werden.  
Microsoft Foundry und Agent Framework wären ein möglicher Kandidat für die zentrale Orchestrierung. ServiceNow und Oracle bleiben dabei wichtige lokale Agentendomänen.  
**3.7 Vergleich der Optionen**  
Die folgende Tabelle ist als erste qualitative Arbeitshypothese gedacht, nicht als abschließende Produktbewertung.  

| Kriterium | ServiceNow | Microsoft | Azure + LangGraph | AWS AgentCore |
| ------------------------ | ------------- | --------------------------- | ----------------------------- | ------------------------ |
| Nähe zu HR-Prozessen | Hoch | Mittel | Abhängig von Eigenentwicklung | Abhängig von Integration |
| Cross-Platform-Fähigkeit | Zu validieren | Hoches Potenzial | Hoch, aber selbst zu bauen | Hohes Potenzial |
| Flexibilität | Mittel | Hoch | Sehr hoch | Hoch |
| Managed Services | Hoch | Hoch | Geringer bis mittel | Hoch |
| Eigenentwicklungsaufwand | Mittel | Mittel | Hoch | Mittel |
| Governance | Plattformnah | Breite Enterprise-Bausteine | Eigenaufbau erforderlich | AgentCore-Bausteine |
| Anbieterabhängigkeit | Hoch | Hoch | Geringer | Hoch |
  
**Worauf du besonders eingehen solltest**  
Die Tabelle sollte nicht dazu führen, dass die Teilnehmer spontan eine Plattform auswählen.  
Vielmehr soll sie die Fragen aufwerfen:  
* Welche Fähigkeiten sind für uns unverzichtbar?  
* Welche Plattform kann diese Fähigkeiten nachweislich bereitstellen?  
* Welche Fähigkeiten müssen wir selbst entwickeln?  
* Welche Plattform passt zu unserer bestehenden IT- und Cloud-Strategie?  
* Welche Kombination ist langfristig am sinnvollsten?  
**3.8 Vorschlag für einen Proof of Concept**  
Ich würde im Workshop einen konkreten Pilotprozess vorschlagen.  
Beispielablauf:  

| Schritt | Komponente      | Aufgabe                                   |
| ------- | --------------- | ----------------------------------------- |
| 1       | ServiceNow      | Employee-Anfrage entgegennehmen           |
| 2       | HR Orchestrator | Aufgabe erkennen und delegieren           |
| 3       | Oracle Agent    | Mitarbeiter- und Positionsdaten ermitteln |
| 4       | HR Policy Agent | Richtlinie prüfen                         |
| 5       | HR Orchestrator | Ergebnisse zusammenführen und validieren  |
| 6       | Mensch          | Sensible Aktion freigeben                 |
| 7       | Oracle          | Freigegebene Aktion ausführen             |
| 8       | ServiceNow      | Case aktualisieren und abschließen        |
  
**Was sollte der PoC beweisen?**  
* Funktioniert die systemübergreifende Agentenkommunikation?  
* Kann der Orchestrator Agenten dynamisch finden und aufrufen?  
* Wie werden Kontext und Prozesszustand verwaltet?  
* Wie funktioniert die Identitäts- und Berechtigungsweitergabe?  
* Können Freigaben integriert werden?  
* Sind Fehler und Unterbrechungen beherrschbar?  
* Können wir den gesamten Prozess nachvollziehen?  
* Wie hoch ist der technische und operative Aufwand?  
**Bewertungskriterien**  

| Kriterium                        | Gewicht |
| -------------------------------- | ------- |
| Cross-platform orchestration     | 20 %    |
| Security und Governance          | 15 %    |
| HR-Systemintegration             | 15 %    |
| Flexibilität und Erweiterbarkeit | 15 %    |
| Observability und Evaluation     | 10 %    |
| Prozess- und State-Management    | 10 %    |
| Betrieb und Wartbarkeit          | 10 %    |
| Kosten und Lizenzierung          | 5 %     |
  
Wichtiger Moderationshinweis:  
Alle Plattformen sollten anhand desselben Use Cases und derselben Erfolgskriterien bewertet werden. Sonst vergleicht ihr unterschiedliche Produktversprechen statt tatsächlicher Fähigkeiten.  
**4. Was du als Moderator unbedingt im Blick behalten solltest**  
Unabhängig vom jeweiligen Abschnitt gibt es einige Themen, auf die du immer wieder zurückkommen solltest.  
**4.1 Nicht in eine reine Produktdiskussion abgleiten**  
Wenn die Diskussion zu früh bei ServiceNow, Microsoft oder Oracle landet, stelle die Frage:  
„Welche konkrete Fähigkeit brauchen wir an dieser Stelle – und kann die jeweilige Plattform sie tatsächlich bereitstellen?“  
Erst die Anforderung, dann das Produkt.  
**4.2 Zentralisierung und Föderation sauber unterscheiden**  
Das ist wahrscheinlich die wichtigste Architekturentscheidung.  
Ein zentraler Orchestrator bedeutet nicht, dass sämtliche Agenten, Prozesse und Daten zentralisiert werden müssen.  
Versuche immer wieder, die Verantwortungsgrenzen zu klären.  
**4.3 Security und Governance nicht als nachgelagertes Thema behandeln**  
Im HR-Umfeld sind personenbezogene Daten und sensible Aktionen besonders relevant.  
Identity, Berechtigungen, Datenminimierung, Freigaben und Audit müssen von Anfang an Bestandteil des Zielbilds sein.  
**4.4 Nicht alles muss ein Agent sein**  
Ein klassischer Workflow, ein API-Aufruf oder eine Business Rule kann die bessere Lösung sein.  
Agenten sollten dort eingesetzt werden, wo Flexibilität, Interpretation und intelligente Aufgabenbearbeitung einen echten Mehrwert bieten.  
**4.5 Immer wieder konkrete Beispiele verwenden**  
Wenn die Diskussion zu abstrakt wird, nutze den Employee-Service-Request als roten Faden.  
Damit kannst du fast alle Architekturfragen konkretisieren:  
* Welche Agenten werden benötigt?  
* Wie finden sie sich?  
* Welche Daten werden übergeben?  
* Wer kontrolliert den Prozess?  
* Wer darf eine Aktion ausführen?  
* Wie wird das Ergebnis dokumentiert?  
**5. Meine Empfehlung für deinen Moderationsablauf**  
Ich würde den Workshop mit folgenden Leitfragen und Ergebnissen strukturieren:  
**Abschnitt 1 – Zielbild**  
Wichtigstes Ergebnis  
Leitfrage: Wie soll unser HR-Agentenökosystem zukünftig grundsätzlich funktionieren?  
Am Ende sollten stehen:  
* Architekturprinzipien  
* Aufgaben des zentralen Orchestrators  
* Abgrenzung zu lokalen Agentendomänen  
* benötigte Kernfähigkeiten  
* erste Entscheidungen zu State, Context, Protokollen und Governance **Abschnitt 2 – Vertiefung **Leitfrage: Was müssen wir organisatorisch und technisch lösen, damit das Zielbild funktioniert?   
Am Ende sollten stehen:  
* Integrationsprinzipien für HR-Prozesse  
* Monitoring- und Governance-Anforderungen  
* Anforderungen an den Integration Layer  
* Vorgehen für eine gemeinsame HR-Semantik **Abschnitt 3 – Umsetzungsoptionen **Leitfrage: Mit welcher Plattform bzw. Kombination können wir das Zielbild realisieren?   
Am Ende sollten stehen:  
* Bewertung der Plattformoptionen  
* bevorzugte Kandidaten für einen PoC  
* ein konkreter Pilotprozess  
* Bewertungskriterien  
* nächste Schritte und Verantwortlichkeiten  
**6. Die zehn wichtigsten Fragen, die du im Workshop stellen solltest**  
Wenn du nur eine kompakte Liste mit den wichtigsten Moderationsfragen mitnehmen möchtest, würde ich diese verwenden:  
* Zielbild: Wollen wir eine zentrale Orchestrierung oder eine föderierte Architektur mit lokalen Agentendomänen?  
* Verantwortung: Welche Aufgaben sollen zentral und welche lokal in ServiceNow bzw. Oracle liegen?  
* Agenten: Wie sollen Agenten gefunden, beschrieben und registriert werden?  
* Prozess: Wer besitzt den systemübergreifenden Prozesszustand?  
* Kontext: Welche Informationen dürfen Agenten untereinander austauschen?  
* Integration: Welche Standards sollen wir für APIs, Events, MCP und A2A etablieren?  
* Governance: Welche Aktionen dürfen Agenten autonom ausführen und wann ist eine menschliche Freigabe notwendig?  
* Monitoring: Wie stellen wir Qualität, Nachvollziehbarkeit und Kontrolle sicher?  
* Plattform: Welche Lösung kann die Anforderungen am besten erfüllen, ohne neue Silos zu erzeugen?  
* Umsetzung: Welchen konkreten HR-Prozess nutzen wir, um das Zielbild in einem PoC zu validieren?  
Mein abschließender Rat: Lass den Workshop nicht mit einer reinen Plattformpräferenz enden. Das wertvollste Ergebnis wäre ein abgestimmtes Architekturzielbild, eine Liste der noch offenen Architekturentscheidungen und ein konkreter Pilotauftrag mit Verantwortlichen. Damit habt ihr eine belastbare Grundlage, um anschließend die Plattformentscheidung fundiert zu treffen.  
