Ich würde den ersten Agenda-Punkt bewusst sehr intensiv behandeln. Aus meiner Sicht ist er sogar der wichtigste Teil des gesamten Workshops: Ihr solltet nicht mit der Frage starten, welches technische Produkt euren Agent Orchestrator bilden soll, sondern zunächst klären, welche Fähigkeiten, Verantwortlichkeiten und Architekturprinzipien ihr unter einem Orchestrator versteht.

Gerade in eurer Situation sehe ich eine interessante Ausgangslage: Ihr habt noch keine große produktive Agentenlandschaft, aber bereits viele Initiativen, unterschiedliche HR-Systeme und eine heterogene Prozess- und Integrationslandschaft. Das ist eigentlich ein guter Zeitpunkt, um ein übergreifendes Architekturkonzept zu entwickeln.

Ich würde dabei eine Gefahr besonders vermeiden: Ihr baut einen zentralen Orchestrator, der irgendwann versucht, sämtliche Agenten, Prozesse, Daten, Berechtigungen und Geschäftslogik selbst zu verwalten. Damit entsteht schnell ein überdimensionierter technischer Monolith.

Stattdessen würde ich ein Zielbild entwickeln, das auf einer klaren Trennung zwischen Agentensteuerung, Prozesssteuerung, Integration, Wissen und Governance basiert.

Im Folgenden würde ich den ersten Agenda-Punkt so aufbauen, dass ihr am Ende des Workshops nicht nur eine Vision habt, sondern konkrete Architekturentscheidungen und Leitplanken für eure zukünftigen Agenteninitiativen.
1. Mein Vorschlag: Was soll im ersten Workshop-Block entstehen?
Ich würde den ersten Punkt in sechs Themenblöcke aufteilen:
1. Architekturverständnis und Mandat
   
   Was verstehen wir unter einem Agent Orchestrator? Welche Verantwortung soll er übernehmen und welche explizit nicht?
2. Orchestrierungsebenen und Verantwortlichkeiten
   
   Auf welchen Ebenen findet Orchestrierung statt? Welche Instanz steuert was?
3. Funktionales Zielbild
   
   Welche Fähigkeiten muss der Orchestrator direkt zum Start haben? Was kommt später?
4. Wissen, Kontext und Ontologie
   
   Wo liegen Informationen, Wissen und Prozesskontext? Wie werden sie Agenten zur Verfügung gestellt?
5. Kommunikation und Interoperabilität
   
   Wie kommunizieren Agenten untereinander und mit Systemen, Datenquellen und Tools?
6. Architekturprinzipien und Orchestrierungsmuster
   
   Welche übergreifenden Prinzipien und Muster sollen für eure HR-Agentenlandschaft gelten?

Ergebnis: Ein fachliches und technisches Zielbild, eine erste Capability Map, eine Einordnung der Orchestrierungsebenen und ein Set verbindlicher Architekturprinzipien.

Wichtig ist mir dabei eine Unterscheidung: Ihr solltet nicht versuchen, alle Detailfragen im ersten Block abschließend zu beantworten. Beispielsweise gehört die konkrete Ausgestaltung des Monitorings in euren zweiten Agenda-Punkt. Im Zielbild muss aber bereits feststehen, dass Monitoring eine zentrale Fähigkeit ist und welche Verantwortung der Orchestrator dafür trägt.

2. Architekturverständnis: Was ist eigentlich euer Orchestrator?
Das wäre für mich der erste Diskussionspunkt.

Der Begriff Agent Orchestrator wird in Unternehmen für ziemlich unterschiedliche Dinge verwendet. Von einer einfachen Routing-Komponente bis hin zu einer zentralen Steuerungsinstanz für eine komplette Agentenlandschaft.

Ich würde deshalb zunächst folgende Arbeitsdefinition vorschlagen:
Vorschlag für euer Zielbild
HR Agent Orchestration Layer
Der HR Agent Orchestration Layer ist die übergreifende Steuerungs- und Koordinationsebene für KI-Agenten innerhalb der HR-Prozess- und Systemlandschaft.

Er ermöglicht die kontrollierte Zusammenarbeit unterschiedlicher Agenten, koordiniert deren Einsatz innerhalb fachlicher Prozesse, stellt benötigten Kontext bereit und gewährleistet die Einhaltung zentraler Governance-, Sicherheits- und Qualitätsanforderungen.

Dabei ist er technologie- und systemübergreifend konzipiert und arbeitet mit bestehenden Prozess-, Integrations- und Anwendungssystemen zusammen.

Ich würde daraus fünf grundsätzliche Verantwortungsbereiche ableiten:
Verantwortungsbereich	Bedeutung
Agent Coordination	Agenten finden, auswählen, aufrufen und ihre Zusammenarbeit koordinieren
Process Coordination	Agenten in übergreifende HR-Prozesse einbetten und Prozessübergänge steuern
Context & Knowledge	Agenten mit dem benötigten fachlichen und situativen Kontext versorgen
Governance & Control	Berechtigungen, Richtlinien, Freigaben und Kontrollmechanismen sicherstellen
Observability & Lifecycle	Agenteneinsätze nachvollziehbar machen und deren Betrieb unterstützen

Ein entscheidender Punkt: Diese Verantwortlichkeiten müssen nicht alle technisch in einer einzigen Plattform liegen. Der Orchestration Layer kann durchaus aus mehreren Komponenten bestehen.
2.1 Was gehört explizit nicht in den Orchestrator?
Diese Frage würde ich unbedingt im Workshop stellen. Sie ist mindestens genauso wichtig wie die Frage nach seinen Fähigkeiten.

Meine Vorschläge:
- Keine zentrale Ablösung aller Prozess-Engines: ServiceNow, Oracle oder andere Systeme dürfen weiterhin ihre eigenen Workflows und Geschäftsprozesse steuern.
- Keine zentrale Ablösung der HR-Systeme: Oracle, Avature und weitere Systeme bleiben führende Systeme für ihre jeweiligen fachlichen Daten.
- Keine zentrale Ablage sämtlicher Unternehmensdaten: Der Orchestrator soll Wissen und Kontext vermitteln, nicht automatisch alle Daten replizieren.
- Keine Implementierung sämtlicher Agentenlogik: Fachliche Entscheidungen und Aufgabenbearbeitung gehören grundsätzlich in die Agenten.
- Keine eigenständige fachliche Entscheidungsinstanz: Der Orchestrator darf nicht unkontrolliert selbst HR-Entscheidungen treffen.
- Keine universelle Integration Engine: Die Integration mit Systemen sollte über eine geeignete Integrationsarchitektur erfolgen.
Das letzte Thema ist besonders wichtig: Ein Agent Orchestrator und ein Integration Layer haben unterschiedliche Aufgaben. Sie sollten eng zusammenspielen, aber nicht miteinander verschmelzen.
3. Orchestrierungsebenen: Die aus meiner Sicht wichtigste Architekturentscheidung
Hier würde ich im Workshop besonders viel Zeit investieren.

Ich glaube nämlich, dass ihr zunächst klären müsst, auf welchen unterschiedlichen Ebenen überhaupt orchestriert wird. Sonst besteht die Gefahr, dass ihr später mehrere Komponenten habt, die sich gegenseitig in der Steuerung behindern.

Ich würde vier Ebenen unterscheiden.
3.1 Die vier Orchestrierungsebenen
Ebene 1 – Business Process Orchestration
Fachliche Ebene

Was soll fachlich passieren?
Steuerung des übergreifenden HR-Prozesses, seiner Zustände, Aktivitäten, Verantwortlichkeiten und Übergänge.

Beispiel: Recruiting, Onboarding, Talent Management

Ebene 2 – Agent Orchestration
Agentenebene

Welcher Agent erledigt was?
Auswahl, Koordination, Delegation und Zusammenarbeit von Agenten zur Erfüllung einer Aufgabe.

Beispiel: Recruiting Agent, Candidate Assessment Agent

Ebene 3 – Tool & Integration Orchestration
Integrationsebene

Wie werden Aktionen ausgeführt?
Bereitstellung und Koordination von APIs, Tools, Datenzugriffen und Systemaktionen.

Beispiel: Oracle API, ServiceNow API, Avature Schnittstelle

Ebene 4 – Agent Execution & Runtime
Ausführungsebene

Wie arbeitet ein einzelner Agent?
Interne Ausführung, Reasoning, Planung, Tool-Auswahl, Zustandsverwaltung und Aufruf von Sprachmodellen.

Beispiel: LangGraph Runtime, ServiceNow Agent Runtime


Vereinfachtes konzeptionelles Modell – die Ebenen müssen nicht zwingend vier getrennte technische Produkte sein.
Warum ist diese Trennung so wichtig?
Nehmen wir ein Beispiel aus eurem HR-Umfeld:

Use Case: Ein Mitarbeiter wechselt intern die Position.
1. Die Business Process Orchestration erkennt, dass ein interner Positionswechsel durchgeführt werden soll, und steuert den fachlichen Prozess.
2. Die Agent Orchestration entscheidet, welche Agenten zur Unterstützung benötigt werden: beispielsweise ein Agent zur Prüfung der Qualifikationen, ein Agent für die Stellenzuordnung und ein Agent für die Erstellung von Kommunikationsentwürfen.
3. Die Tool & Integration Orchestration stellt den Agenten die erforderlichen Funktionen zur Verfügung, beispielsweise das Lesen des Mitarbeiterprofils aus Oracle oder das Aktualisieren eines Vorgangs in ServiceNow.
4. Die Agent Runtime führt die jeweiligen Agenten aus und verwaltet deren internen Arbeitsablauf.
Wichtig: Nicht jeder Prozessschritt muss durch einen Agenten erledigt werden. Manche Schritte sind klassische Workflows, andere sind regelbasiert, und wieder andere benötigen KI-Unterstützung.
Eine zusätzliche Unterscheidung: Zentral oder dezentral?
Ich würde außerdem zwischen zwei Arten der Steuerung unterscheiden:
- Zentrale Orchestrierung: Eine übergreifende Instanz koordiniert Agenten unterschiedlicher Plattformen und Hersteller.
- Lokale Orchestrierung: Eine Plattform wie ServiceNow oder Oracle orchestriert ihre eigenen Agenten und Workflows innerhalb ihres Verantwortungsbereichs.
Mein Vorschlag wäre eine föderierte Architektur:
- ServiceNow darf seine eigenen Agenten und Prozesse intern orchestrieren.
- Oracle darf seine eigenen Agenten und Prozesse intern orchestrieren.
- Ein übergreifender Orchestration Layer koordiniert die Zusammenarbeit über System- und Plattformgrenzen hinweg.
Das bedeutet nicht, dass jeder Agent zwingend über einen zentralen Orchestrator laufen muss.

Meine Empfehlung: Der zentrale Orchestrator sollte vor allem dort eingesetzt werden, wo eine Koordination über mehrere Agenten, Systeme oder fachliche Domänen hinweg erforderlich ist. Lokale Prozesse sollten weiterhin lokal gesteuert werden können.

Das ist insbesondere deshalb sinnvoll, weil ihr perspektivisch nicht nur Agenten von einem Hersteller haben werdet.

4. Funktionales Zielbild: Was muss der Orchestrator können?
Jetzt würde ich die Frage beantworten, welche konkreten Fähigkeiten ihr von eurem Orchestrator erwartet.

Hier empfehle ich, nicht einfach eine Liste von technischen Features zu erstellen. Stattdessen würde ich eine Capability Map entwickeln.

Ich habe dafür acht Capability-Bereiche identifiziert.
4.1 Capability Map des HR Agent Orchestration Layers
HR Agent Orchestration Layer
Übergreifende Steuerungs- und Koordinationsebene
1. Agent Registry & Discovery
Agenten registrieren, finden, beschreiben und ihre Fähigkeiten erkennen.

2. Routing & Coordination
Agenten auswählen, Aufgaben delegieren und Zusammenarbeit steuern.

3. Workflow & State Management
Abläufe, Zustände, Abhängigkeiten und Wiederaufnahme verwalten.

4. Context & Knowledge Management
Fachlichen Kontext, Wissen und relevante Informationen bereitstellen.

5. Governance & Security
Berechtigungen, Richtlinien, Freigaben und Kontrollmechanismen durchsetzen.

6. Observability & Monitoring
Agentenaufrufe, Ergebnisse, Kosten, Qualität und Fehler nachvollziehen.

7. Interoperability & Integration
Plattformübergreifende Kommunikation und standardisierte Schnittstellen ermöglichen.

8. Agent Lifecycle Management
Versionen, Freigaben, Deployment, Deaktivierung und Weiterentwicklung unterstützen.


Vorgeschlagene Capability-Struktur – keine Aussage darüber, welche Funktionen zwingend zentral implementiert werden müssen.
Ich würde diese acht Bereiche im Workshop einzeln diskutieren.
1. Agent Registry & Discovery
Das ist aus meiner Sicht eine absolute Kernfähigkeit.

Wenn ihr perspektivisch Agenten in ServiceNow, Oracle, Azure und möglicherweise weiteren Plattformen habt, benötigt ihr eine übergreifende Sicht darauf, welche Agenten existieren und wofür sie eingesetzt werden können.

Denkbare Informationen pro Agent:
Information	Beispiel
Agent ID	HR-AGENT-001
Name	Recruiting Assistant
Fachliche Domäne	Recruiting
Fähigkeiten	Kandidatenprofile analysieren
Anbieter / Plattform	ServiceNow
Schnittstelle	A2A / API
Verantwortlicher	HR IT
Status	Produktiv
Version	1.2
Berechtigungen	Read Candidate Data
Kritikalität	Hoch

Eine zentrale Registry muss dabei nicht zwingend die technische Laufzeit des Agenten verwalten. Sie kann zunächst ein übergreifender Katalog sein, der auch auf die lokalen Registrierungen der Hersteller verweist.

Eine wichtige Frage für euren Workshop:

Muss der Orchestrator Agenten anhand ihrer Fähigkeiten dynamisch entdecken und auswählen können oder reicht zunächst eine zentral gepflegte, statische Zuordnung?

Meine Empfehlung: Beides vorsehen, aber mit einem einfachen, kontrollierten Einstieg starten.
2. Routing & Coordination
Hier geht es darum, wie Aufgaben an Agenten verteilt werden.

Beispiele:
- Welcher Agent kann eine bestimmte HR-Aufgabe übernehmen?
- Welcher Agent ist für eine bestimmte HR-Domäne zuständig?
- Welcher Agent ist für die jeweilige Aufgabe freigegeben?
- Welcher Agent hat die benötigten Berechtigungen?
- Soll ein Agent eine Aufgabe an einen anderen Agenten übergeben dürfen?
- Wie wird mit Fehlern oder nicht verfügbaren Agenten umgegangen?
Eine wichtige Designentscheidung ist, ob das Routing deterministisch oder KI-basiert erfolgt.

Ich würde beides unterstützen, aber bei HR-Prozessen klare Grenzen setzen.

Beispielsweise sollte die Entscheidung, ob ein Agent eine Gehaltsänderung durchführen darf, nicht allein durch ein LLM getroffen werden.
3. Workflow & State Management
Diese Fähigkeit wird häufig unterschätzt.

Agenteninteraktionen sind nicht immer kurze synchrone Aufrufe. Ein Prozess kann sich über Stunden oder Tage erstrecken.

Beispielsweise:
- Ein Agent analysiert einen Sachverhalt.
- Eine Führungskraft muss eine Entscheidung treffen.
- Der Prozess wartet zwei Tage auf eine Freigabe.
- Anschließend wird ein weiterer Agent aktiviert.
- Ein Ergebnis wird in Oracle gespeichert.
Dafür braucht ihr:
- Persistente Prozess- und Aufgabenzustände
- Korrelation von Agentenaufrufen
- Asynchrone Kommunikation
- Timeouts und Wiederholungslogiken
- Fehlerbehandlung und Kompensation
- Wiederaufnahme unterbrochener Abläufe
- Human-in-the-Loop-Unterstützung
Wichtig ist hier die Abgrenzung: Der Orchestrator sollte übergreifende Agenteninteraktionen verwalten können. Die fachliche Prozessführung kann trotzdem bei ServiceNow, Oracle oder einer anderen Process Engine verbleiben.
4. Context & Knowledge Management
Dazu komme ich in Kapitel 5 noch ausführlicher.
5. Governance & Security
Für eine HR-Agentenlandschaft halte ich diese Capability für besonders wichtig.

Denkbare Anforderungen:
- Authentifizierung und Autorisierung
- Identitätsweitergabe und Delegation
- Rollen- und Berechtigungskonzepte
- Datenzugriff nach Need-to-know
- Richtlinien für sensible HR-Daten
- Freigaben für kritische Aktionen
- Protokollierung und Auditierbarkeit
- Durchsetzung von Datenschutz- und Compliance-Vorgaben
Ein wichtiger Grundsatz: Der Orchestrator sollte nicht einfach mit einem universellen technischen Account auf alle HR-Systeme zugreifen. Die Berechtigungen müssen sich aus dem jeweiligen Nutzer-, Prozess- und Agentenkontext ableiten.
6. Observability & Monitoring
Der Orchestrator sollte einen übergreifenden Überblick über Agenteninteraktionen ermöglichen.

Dazu gehören beispielsweise:
- Welche Agenten wurden aufgerufen?
- In welchem Prozesskontext?
- Welche Eingaben und Ergebnisse wurden ausgetauscht?
- Wo sind Fehler aufgetreten?
- Wie lange hat die Ausführung gedauert?
- Welche Kosten sind entstanden?
- Wo wurden Menschen eingebunden?
- Wurde eine Aufgabe erfolgreich abgeschlossen?
Nicht jedes Detail muss zentral gespeichert werden. Aber eine übergreifende Nachvollziehbarkeit sollte gewährleistet sein.
7. Interoperability & Integration
Das ist die Fähigkeit, die eure heterogene Systemlandschaft adressiert.

Hier geht es um die Kommunikation mit:
- Agenten anderer Plattformen
- Fachsystemen
- APIs und Services
- Datenquellen
- Event-Systemen
- bestehenden Integrationsplattformen
Ich würde den Orchestrator bewusst nicht auf eine bestimmte Agententechnologie ausrichten.
8. Agent Lifecycle Management
Eine Fähigkeit, die ihr wahrscheinlich anfangs noch nicht stark benötigen werdet, die aber perspektivisch wichtig wird:
- Registrierung und Onboarding neuer Agenten
- Test und Freigabe
- Versionsverwaltung
- Deployment und Rollback
- Deaktivierung und Stilllegung
- Überprüfung der Agentenfähigkeiten
- Verwaltung von Verantwortlichkeiten
Gerade bei vielen unterschiedlichen Initiativen ist eine einheitliche Governance des Agentenportfolios wichtig.
4.2 Priorisierung: Was muss direkt vorhanden sein?
Ich würde im Workshop drei Reifegrade definieren.
Capability	Initial	Mittelfristig	Perspektivisch
Agent Registry	Muss		
Agent Routing	Muss		
Workflow-/State-Management	Muss		
Governance & Security	Muss		
Basis-Monitoring	Muss		
Kontextbereitstellung	Muss		
Standardisierte Schnittstellen	Muss		
Dynamische Agent Discovery		Soll	
Fortgeschrittenes Context Management		Soll	
Kosten- und Qualitätsoptimierung		Soll	
Dynamische Multi-Agent-Planung			Kann
Agentenübergreifende Selbstoptimierung			Kann

Das ist meine erste Hypothese, die ihr im Workshop validieren solltet. Insbesondere würde ich dynamische Multi-Agent-Planung nicht als notwendige Startanforderung definieren.

5. Wissen, Kontext und Ontologie: Wo liegt das Wissen des Orchestrators?
Das ist für mich eine der spannendsten und strategisch wichtigsten Fragen.

Ich würde zunächst drei Arten von Informationen unterscheiden, die häufig fälschlicherweise unter dem Begriff Wissen zusammengefasst werden.
5.1 Drei unterschiedliche Informationsarten
A. Fachliches Wissen (Knowledge)

Informationen über HR-Fachlichkeit und Unternehmensregeln.
- HR-Richtlinien
- Betriebsvereinbarungen
- Stellen- und Rollenbeschreibungen
- Prozessdokumentationen
- Fachliche Regeln
- Organisationsstrukturen


B. Operative Daten (Data)

Konkrete Informationen aus den führenden HR-Systemen.
- Mitarbeiterstammdaten aus Oracle
- Bewerberdaten aus Avature
- Prozessinformationen aus ServiceNow
- Organisationsdaten aus weiteren Systemen


C. Laufzeitkontext (Context)

Informationen, die für eine konkrete Agentenausführung benötigt werden.
- Aktueller Prozessschritt
- Aufgabenstellung
- Bisherige Ergebnisse
- Identität und Berechtigungen
- Bereits getroffene Entscheidungen
- Offene Freigaben


Diese drei Informationsarten sollten architektonisch unterschiedlich behandelt werden.

Meine Empfehlung: Der Orchestrator sollte nicht das zentrale Wissenssystem eures HR-Bereichs werden. Er sollte eine zentrale Fähigkeit zur Vermittlung und Bereitstellung von Wissen und Kontext haben.

Das bedeutet:
- Fachliches Wissen bleibt möglichst in geeigneten Wissensquellen.
- Operative Daten bleiben in den jeweiligen führenden Systemen.
- Laufzeitkontext wird dort verwaltet, wo er für die Prozess- und Agentensteuerung benötigt wird.
5.2 Wie sollte der Orchestrator Wissen bereitstellen?
Ich würde ein Konzept aus drei Bausteinen vorschlagen:
1. Knowledge Access: Zugriff auf vorhandene Wissensquellen, beispielsweise über APIs, Suchdienste oder RAG.
2. Context Assembly: Zusammenstellung des für eine konkrete Aufgabe benötigten Kontexts.
3. Context Distribution: Gezielte Bereitstellung dieses Kontexts an die jeweiligen Agenten.
Ein Beispiel:

Ein Recruiting-Agent soll beurteilen, ob ein Kandidat zu einer bestimmten Stelle passt.

Der Orchestrator könnte dafür den Kontext zusammenstellen:
- Stellenbeschreibung aus dem Recruiting-System
- Kompetenzmodell aus einer zentralen Wissensquelle
- Organisationskontext
- Prozessstatus aus ServiceNow
- Berechtigungskontext des aufrufenden Nutzers
Der Agent erhält dann nur den Kontext, den er für seine konkrete Aufgabe benötigt.

Dabei ist wichtig, dass die Zusammenstellung nicht automatisch bedeutet, dass alle Daten in einen zentralen Vektorindex kopiert werden.
5.3 Welche Rolle spielt die Ontologie?
Ich würde das Thema Ontologie ausdrücklich im Zielbild verankern, aber nicht als Voraussetzung dafür definieren, den ersten Orchestrator produktiv zu bringen.

Warum?

Ihr habt unterschiedliche HR-Systeme, die wahrscheinlich teilweise unterschiedliche Begriffe und Datenmodelle verwenden.

Beispiel:
- Oracle kennt einen Mitarbeiter und dessen Position.
- Avature kennt einen Kandidaten und eine Bewerbung.
- ServiceNow kennt einen HR Case.
- Ein weiteres System kennt eine organisatorische Einheit.
Eine gemeinsame fachliche Sprache könnte diese unterschiedlichen Perspektiven miteinander verbinden.

Denkbare Elemente eines HR-Referenzmodells:
- Person
- Employee
- Candidate
- Position
- Job
- Organization
- Department
- Skill
- Competency
- HR Case
- HR Process
- Approval
- Task
Die Ontologie beziehungsweise ein semantisches Modell könnte definieren, wie diese Begriffe zusammenhängen und wie sie in den unterschiedlichen Systemen abgebildet werden.
Beispiel: Fachliche Abstraktion
Person
Gemeinsames fachliches Konzept

Oracle
Employee Record

Avature
Candidate Record

ServiceNow
HR Profile / Case


Illustration eines möglichen semantischen Mappings, keine Behauptung über die konkreten Datenmodelle eurer Installationen.
Die Ontologie kann damit eine wichtige Grundlage für Interoperabilität und Context Assembly bilden.

Ich würde allerdings unterscheiden zwischen:
- Ontologie: Welche fachlichen Konzepte und Beziehungen gibt es?
- Semantisches Datenmodell: Wie werden diese Konzepte strukturiert und beschrieben?
- Mapping: Wie werden die Konzepte den konkreten Datenmodellen der Systeme zugeordnet?
- Knowledge Graph: Wie werden diese Konzepte und ihre Beziehungen technisch repräsentiert und abgefragt?
Ihr müsst nicht sofort einen vollständigen Knowledge Graph bauen, um von einer gemeinsamen fachlichen Semantik zu profitieren.

Meine Empfehlung: Entwickelt mittelfristig ein HR-weites semantisches Referenzmodell. Startet mit wenigen, systemübergreifenden Kernbegriffen, die für eure ersten Agenten relevant sind.

6. Kommunikation und Interoperabilität: Mit welchen Protokollen kommuniziert der Orchestrator?
Das ist ein Punkt, bei dem ich eine sehr klare Architekturentscheidung treffen würde:

Ihr solltet keine einzelne Kommunikationstechnologie als universellen Standard für sämtliche Interaktionen definieren.

Es gibt unterschiedliche Kommunikationsbeziehungen, die unterschiedliche Anforderungen haben.
6.1 Drei Kommunikationsbeziehungen
Kommunikation	Aufgabe	Denkbare Standards
Orchestrator ↔ Agent	Agenten entdecken, Aufgaben übergeben, Ergebnisse empfangen	A2A, REST APIs
Agent ↔ Tools / Datenquellen	Funktionen aufrufen und Kontext abrufen	MCP, REST APIs, SQL, SDKs
Orchestrator ↔ Systeme	Geschäftsprozesse, Daten und Ereignisse koordinieren	REST, Events, Webhooks, Messaging

Daraus würde ich folgende Protokollstrategie ableiten:
A. A2A – Agent-to-Agent
Agent2Agent (A2A) ist aus meiner Sicht ein sehr interessanter Standard für eure Architektur.

Der wesentliche Gedanke: Agenten unterschiedlicher Hersteller und Frameworks sollen miteinander kommunizieren können, ohne dass der aufrufende Agent deren interne Implementierung kennen muss.

A2A adressiert insbesondere:
- Agent Discovery und Beschreibung von Fähigkeiten
- Übergabe von Aufgaben
- Austausch strukturierter Ergebnisse
- Asynchrone Aufgabenbearbeitung
- Status und Lebenszyklus von Aufgaben
Das ist für eure heterogene Landschaft besonders relevant. Ein ServiceNow-Agent sollte perspektivisch mit einem Oracle-Agent kommunizieren können, ohne dass ihr eine proprietäre Punkt-zu-Punkt-Integration für jeden einzelnen Agenten bauen müsst.

A2A wurde ursprünglich von Google entwickelt und wird inzwischen im Rahmen der Linux Foundation als offener Standard weiterentwickelt. 

Agent2Agent (A2A) Protocol+1

B. MCP – Model Context Protocol
Model Context Protocol (MCP) ist dagegen nicht primär ein Agent-zu-Agent-Protokoll.

Es standardisiert, wie KI-Anwendungen auf Tools und Kontextquellen zugreifen können.

MCP unterscheidet unter anderem:
- Tools: ausführbare Funktionen
- Resources: bereitgestellte Kontextinformationen
- Prompts: wiederverwendbare Prompt-Vorlagen
Ein Beispiel:

Ein HR-Agent könnte über einen MCP-Server folgende Funktionen nutzen:
- Mitarbeiterinformationen abrufen
- HR Cases suchen
- Organisationsinformationen abfragen
- Eine Änderung vorbereiten
- Einen Freigabeprozess anstoßen
Der Vorteil wäre, dass unterschiedliche Agenten auf standardisierte Tool-Schnittstellen zugreifen könnten, ohne für jedes Tool eine eigene Integration implementieren zu müssen. 

GitHub+1

C. REST APIs und Events
Ich würde REST APIs und Event-basierte Kommunikation keinesfalls durch A2A oder MCP ersetzen wollen.

Ihr habt bereits eine umfangreiche Systemlandschaft, und viele eurer Systeme werden auch in Zukunft klassische APIs und Events bereitstellen.

Beispiele:
- Ein HR Case wird in ServiceNow angelegt.
- Eine Positionsänderung wird in Oracle durchgeführt.
- Eine Bewerbung wird in Avature aktualisiert.
- Ein Event informiert über den Abschluss eines Prozessschritts.
Gerade bei länger laufenden HR-Prozessen ist eine Event-basierte Architektur interessant.
6.2 Mein Vorschlag für eure Protokollarchitektur
Zentraler HR Agent Orchestrator
Routing · Coordination · Context · Governance
A2A
Agent Communication
Aufgaben und Ergebnisse zwischen Agenten

MCP
Tool & Context Access
Funktionen und Informationen bereitstellen


Integration Layer
REST · Events · Messaging · API Management
ServiceNow
Workflows & Agenten

Oracle
HR-Daten & Agenten

Weitere Systeme
Avature & Eigenentwicklungen


Konzeptionelle Kommunikationsarchitektur. Die tatsächlichen Schnittstellen hängen von den Fähigkeiten der jeweiligen Plattformen ab.
Eine wichtige Einschränkung würde ich direkt in eure Architekturprinzipien aufnehmen:

Ein Protokoll allein löst keine Interoperabilität.

Auch wenn ein Agent A2A unterstützt, müsst ihr beispielsweise weiterhin klären:
- Wie werden Identitäten weitergegeben?
- Wie werden Berechtigungen geprüft?
- Welche Daten dürfen ausgetauscht werden?
- Wie werden fachliche Begriffe interpretiert?
- Wie werden Fehler und Timeouts behandelt?
- Wie wird die Kommunikation nachvollziehbar protokolliert?
Meine Empfehlung für den Workshop: A2A als strategische Richtung für die Kommunikation zwischen unabhängigen Agenten prüfen, MCP für standardisierten Tool- und Kontextzugriff berücksichtigen und REST/Event-basierte Integration als gleichberechtigte Bestandteile der Architektur beibehalten.

7. Orchestrierungsmuster: Welche Muster machen für euch Sinn?
Jetzt kommen wir zur Frage, wie der Orchestrator die Zusammenarbeit von Agenten tatsächlich organisiert.

Ich würde fünf Muster unterscheiden.
7.1 Die fünf wichtigsten Muster









1. Sequential Orchestration

Agenten arbeiten nacheinander in einer definierten Reihenfolge.

Beispiel: Ein Agent analysiert eine Stellenbeschreibung, ein zweiter erstellt ein Anforderungsprofil, ein dritter prüft das Ergebnis.
Hohe Relevanz für HR












2. Concurrent Orchestration

Mehrere Agenten bearbeiten unterschiedliche Teilaufgaben parallel. Die Ergebnisse werden anschließend zusammengeführt.

Beispiel: Ein Agent prüft Qualifikationen, ein anderer Berufserfahrung und ein dritter formale Anforderungen.
Hohe Relevanz für HR












3. Handoff / Delegation

Ein Agent übergibt eine Aufgabe an einen anderen Agenten, wenn dessen Fähigkeiten besser passen.

Beispiel: Ein allgemeiner HR-Agent erkennt eine Frage zum Arbeitszeitmodell und übergibt sie an einen spezialisierten Agenten.
Hohe Relevanz für HR












4. Group Chat / Collaboration

Mehrere Agenten arbeiten gemeinsam an einer Fragestellung und tauschen Ergebnisse aus.

Beispiel: Verschiedene Fachagenten überprüfen gemeinsam einen komplexen HR-Sachverhalt.
Selektiver Einsatz












5. Manager-based / Magentic Orchestration

Ein übergeordneter Agent plant dynamisch die Vorgehensweise und delegiert Teilaufgaben an Spezialagenten.

Beispiel: Ein komplexer HR-Fall wird analysiert und ein Manager-Agent entwickelt eigenständig einen Plan, welche Spezialisten benötigt werden.
Perspektivisch interessant



Diese Muster werden beispielsweise auch im Microsoft Azure Architecture Center beschrieben. Dort werden insbesondere die unterschiedlichen Stärken und Risiken der jeweiligen Ansätze herausgearbeitet. 

Microsoft Learn+1

7.2 Welche Muster würde ich für eure HR-Landschaft bevorzugen?
Ich würde für den Anfang drei Muster priorisieren:
Muster	Priorität	Begründung
Sequential	Hoch	Gut kontrollierbare, nachvollziehbare Prozessketten
Concurrent	Hoch	Unabhängige Teilaufgaben lassen sich parallel bearbeiten
Handoff	Hoch	Ermöglicht die Zusammenarbeit unterschiedlicher Spezialagenten
Group Chat	Mittel	Für bestimmte komplexe Prüf- und Analyseaufgaben
Magentic	Niedriger	Mehr Autonomie, aber schwieriger kontrollierbar

Eine wichtige Ergänzung: Diese Muster sind keine konkurrierenden Architekturentscheidungen. Ein einzelner HR-Prozess kann mehrere Muster kombinieren.

Beispielsweise:
1. Ein Agent analysiert zunächst einen HR-Fall.
2. Anschließend werden drei Spezialagenten parallel aufgerufen.
3. Ein übergeordneter Agent führt die Ergebnisse zusammen.
4. Bei Bedarf erfolgt ein Handoff an einen weiteren Spezialisten.
5. Vor einer kritischen Systemaktion wird ein Mensch eingebunden.
7.3 Noch wichtiger: Deterministische versus dynamische Orchestrierung
Neben den fünf Mustern würde ich eine zweite Dimension betrachten:

Wie viel Entscheidungsfreiheit hat die Orchestrierung?
Deterministische Orchestrierung	Dynamische Orchestrierung
Vorgegebene Prozessschritte	Agent entscheidet über nächste Schritte
Definierte Agenten	Dynamische Agentenauswahl
Vorhersehbare Abläufe	Flexible Aufgabenbearbeitung
Gut kontrollierbar	Höhere Flexibilität
Gut für kritische Prozesse	Gut für offene Aufgabenstellungen

Meine Empfehlung ist ein hybrides Modell:
- Kritische HR-Prozesse werden grundsätzlich deterministisch orchestriert.
- KI-Agenten übernehmen innerhalb dieser Prozesse definierte Aufgaben.
- Dynamische Delegation ist innerhalb klar definierter Grenzen möglich.
- Kritische Aktionen benötigen definierte Kontroll- und Freigabemechanismen.
Ein Beispiel: Ein Agent darf selbst entscheiden, welcher weitere Agent bei der Analyse einer Stellenbeschreibung benötigt wird. Er darf aber nicht selbstständig entscheiden, ob ein Mitarbeiter befördert wird.

Das ist eine wichtige Architekturleitplanke für euren HR-Kontext.

8. Wie sieht das Gesamtzielbild aus?
Wenn ich die bisherigen Überlegungen zusammenführe, würde ich folgendes konzeptionelles Zielbild für euch vorschlagen.
HR Agentic Architecture – Target Vision
HR Users & Business Processes
Führungskräfte · HR Business Partner · HR Operations · Mitarbeiter

HR Agent Orchestration Layer
Agent Registry & Discovery

Routing & Coordination

Workflow & State Management

Context & Knowledge

Governance & Security

Observability & Monitoring

Interoperability

Lifecycle Management



Integration & Communication Layer
A2A · MCP · APIs · Events · Messaging
ServiceNow
Lokale Orchestrierung
Lokale AgentenWorkflows

Oracle
Lokale Orchestrierung
Lokale AgentenWorkflows

Weitere
Lokale Orchestrierung
AvatureEigenentwicklungen


Cross-cutting Services
Identity & Access Management · HR Semantic Model · Knowledge Sources · AI Governance · Enterprise Monitoring

Das ist bewusst ein logisches Zielbild. Es legt noch nicht fest, ob beispielsweise die Registry in ServiceNow, Microsoft oder einer eigenen Komponente implementiert wird.

Eine zentrale Aussage darin ist mir besonders wichtig:

Der Orchestrator ist eine übergreifende Steuerungsebene, keine neue zentrale HR-Plattform, die alle bestehenden Plattformen ersetzt.
9. Welche Fragen würde ich im Workshop konkret stellen?
Ich würde den Workshop nicht als reine Architekturpräsentation aufbauen. Die Teilnehmer sollten gemeinsam Entscheidungen treffen.

Dafür würde ich folgende Fragen vorbereiten.
Themenblock A: Mandat und Verantwortlichkeit
1. Soll es einen zentralen HR Agent Orchestrator geben oder mehrere föderierte Orchestratoren?
2. Welche Aufgaben muss er zwingend übernehmen?
3. Welche Aufgaben sollen weiterhin in ServiceNow, Oracle oder anderen Systemen verbleiben?
4. Muss jeder HR-Agent beim zentralen Orchestrator registriert sein?
5. Welche Agenten dürfen direkt miteinander kommunizieren?
Themenblock B: Orchestrierungsebenen
1. Welche Orchestrierungsebenen unterscheiden wir?
2. Wo endet die Verantwortung der Prozess-Engine und wo beginnt die des Agent Orchestrators?
3. Welche Aufgaben darf ein Agent selbstständig entscheiden?
4. Welche Entscheidungen müssen deterministisch erfolgen?
5. Wie gehen wir mit Prozessen um, die mehrere Systeme und Agenten umfassen?
Themenblock C: Funktionale Fähigkeiten
1. Welche Fähigkeiten benötigen wir zwingend zum Start?
2. Benötigen wir eine zentrale Agent Registry?
3. Wie sollen Agenten ausgewählt und geroutet werden?
4. Wer verwaltet Prozesszustände und Kontext?
5. Welche Governance-Funktionen müssen zentral bereitgestellt werden?
6. Wie viel Autonomie wollen wir den Agenten geben?
Themenblock D: Wissen und Ontologie
1. Wo sollen fachliche HR-Wissensquellen liegen?
2. Benötigen wir einen zentralen Knowledge Layer?
3. Wie wird Kontext systemübergreifend bereitgestellt?
4. Welche Rolle soll ein gemeinsames HR-Datenmodell spielen?
5. Welche fachlichen Begriffe müssen systemübergreifend harmonisiert werden?
6. Benötigen wir perspektivisch eine HR-Ontologie oder einen Knowledge Graph?
Themenblock E: Interoperabilität
1. Welche Standards wollen wir unterstützen?
2. Ist A2A unser strategisches Ziel für Agent-zu-Agent-Kommunikation?
3. Wo setzen wir MCP ein?
4. Wie integrieren wir bestehende APIs und Event-Schnittstellen?
5. Wie stellen wir herstellerübergreifende Identitäten und Berechtigungen sicher?
Themenblock F: Orchestrierungsmuster
1. Welche Aufgaben werden deterministisch orchestriert?
2. Wo erlauben wir dynamische Delegation?
3. Welche Agenten dürfen selbstständig weitere Agenten aufrufen?
4. Wo benötigen wir Human-in-the-Loop?
5. Welche Muster wollen wir als Standard für unsere HR-Agenten etablieren?

10. Wie würde ich den Workshop zeitlich gestalten?
Für diesen ersten Agenda-Punkt würde ich ungefähr 3 bis 3,5 Stunden einplanen.
Zeit	Inhalt	Ergebnis
15 Min.	Ausgangslage und gemeinsames Verständnis	Gemeinsame Definition
35 Min.	Mandat und Orchestrierungsebenen	Verantwortungsmodell
45 Min.	Funktionales Zielbild / Capability Map	Priorisierte Fähigkeiten
30 Min.	Wissen, Kontext und Ontologie	Grundsätzliche Informationsarchitektur
30 Min.	Kommunikation und Protokolle	Interoperabilitätsprinzipien
30 Min.	Orchestrierungsmuster	Bevorzugte Muster
20 Min.	Zusammenführung und Entscheidungen	Konsolidiertes Zielbild

Ich würde insbesondere die Diskussion der Orchestrierungsebenen und der Capability Map nicht zu kurz kommen lassen.
11. Was sollte am Ende des Workshops konkret vorliegen?
Ich würde darauf bestehen, dass ihr fünf konkrete Ergebnisse produziert.
1. Definition und Mandat des Orchestrators

Eine abgestimmte Definition, welche Verantwortung der Orchestrator hat und welche nicht.
2. Logisches Architekturzielbild

Eine Darstellung der Orchestrierungsebenen und ihrer Verantwortlichkeiten.
3. Priorisierte Capability Map

Welche Fähigkeiten zum Start, mittelfristig und langfristig benötigt werden.
4. Interoperabilitäts- und Informationsprinzipien

Grundsätze für A2A, MCP, APIs, Events, Kontext, Wissen und semantische Modelle.
5. Architekturprinzipien

Etwa 8–12 verbindliche Leitplanken für zukünftige HR-Agenteninitiativen.
11.1 Meine vorgeschlagenen Architekturprinzipien
Ich würde mit folgenden zwölf Prinzipien in den Workshop gehen:
Nr.	Architekturprinzip
1	Platform Agnostic: Die Architektur darf nicht von einem einzelnen Agentenhersteller abhängig sein.
2	Federated Orchestration: Lokale Plattformen dürfen weiterhin ihre eigenen Agenten und Prozesse orchestrieren.
3	Central Coordination: Systemübergreifende Agenteninteraktionen müssen zentral koordinierbar sein.
4	Separation of Concerns: Prozess-, Agenten-, Tool- und Runtime-Orchestrierung werden klar getrennt.
5	API & Protocol First: Neue Agenten und Tools sollen standardisierte Schnittstellen anbieten.
6	Knowledge Decoupling: Wissen und operative Daten werden nicht unnötig zentral repliziert.
7	Semantic Consistency: Eine gemeinsame HR-Fachsprache soll systemübergreifende Zusammenarbeit ermöglichen.
8	Security by Design: Identität, Berechtigungen und Datenschutz werden durchgängig berücksichtigt.
9	Human Accountability: Kritische HR-Entscheidungen und Aktionen benötigen angemessene menschliche Kontrolle.
10	Observability by Design: Agenteninteraktionen müssen durchgängig nachvollziehbar sein.
11	Deterministic Where Needed: Kritische Prozessabläufe werden kontrolliert und nachvollziehbar gesteuert.
12	Composable Architecture: Fähigkeiten und Komponenten müssen unabhängig voneinander weiterentwickelt und ausgetauscht werden können.


12. Meine drei wichtigsten strategischen Empfehlungen
Wenn ich eure Ausgangslage betrachte, würde ich drei Dinge besonders stark in den Vordergrund stellen.

1. Den Orchestrator nicht als Produkt, sondern als Architekturkonzept denken.

Ihr werdet wahrscheinlich eine Kombination aus verschiedenen Technologien benötigen. Beispielsweise eine zentrale Agent Registry, einen übergreifenden Koordinationsmechanismus, bestehende Integrationsservices und lokale Orchestrierungsfähigkeiten von ServiceNow und Oracle.

Es ist nicht gesagt, dass eine einzelne Plattform das alles optimal abbilden kann.

2. Prozess- und Agentenorchestrierung sauber voneinander trennen.

Das halte ich für die wichtigste fachlich-technische Unterscheidung.

Ihr habt bereits komplexe HR-Prozesse, die über mehrere Systeme laufen. Ihr solltet nicht versuchen, diese Prozesse künftig vollständig durch Agenten orchestrieren zu lassen.

Vielmehr sollten Agenten gezielt in bestehende Prozesse eingebunden werden. Der Agent Orchestrator koordiniert die Agenten, während die fachliche Prozessverantwortung dort verbleibt, wo sie hingehört.

3. Interoperabilität von Anfang an berücksichtigen.

Ihr habt ServiceNow und Oracle als erste relevante Agentenplattformen. Es wäre aber ein strategischer Fehler, eine Architektur zu bauen, die nur mit diesen beiden Plattformen funktioniert.

Ich würde daher frühzeitig A2A, MCP, REST APIs und Event-basierte Kommunikation als mögliche Bestandteile eurer Zielarchitektur berücksichtigen.

Dabei müsst ihr nicht jeden Standard sofort implementieren. Entscheidend ist, dass ihr euch keine Architekturentscheidungen einhandelt, die euch später einschränken.

13. Eine zusätzliche Überlegung: Wie ihr die Plattformdiskussion vorbereiten solltet
Obwohl dein Fokus zunächst auf Punkt 1 liegt, würde ich bereits eine wichtige Brücke zu eurem dritten Agenda-Punkt schlagen.

Ihr solltet die Anbieter später anhand derselben Architektur-Capabilities vergleichen.

Dafür würde ich folgende Bewertungsdimensionen vorbereiten:
Capability	ServiceNow	Microsoft	Azure + LangGraph	AWS
Agent Registry	Zu bewerten	Zu bewerten	Zu gestalten	Zu bewerten
Cross-Platform Routing	Zu bewerten	Zu bewerten	Zu gestalten	Zu bewerten
Multi-Agent Orchestration	Zu bewerten	Zu bewerten	Zu gestalten	Zu bewerten
State Management	Zu bewerten	Zu bewerten	Zu gestalten	Zu bewerten
A2A / MCP	Zu validieren	Zu validieren	Zu validieren	Zu validieren
Governance	Zu bewerten	Zu bewerten	Zu gestalten	Zu bewerten
Observability	Zu bewerten	Zu bewerten	Zu gestalten	Zu bewerten
HR Context Management	Zu bewerten	Zu bewerten	Zu gestalten	Zu gestalten

Das ist bewusst noch keine Anbieterbewertung. Die konkrete Unterstützung einzelner Funktionen, Standards und Schnittstellen muss anhand der jeweiligen Produktversionen und eurer konkreten Systemkonfiguration geprüft werden.

Damit verhindert ihr, dass ihr euch im Workshop bereits unbewusst auf eine Technologie festlegt, bevor überhaupt klar ist, was sie leisten soll.

14. Weiterführende Grundlagen
Für die fachliche Vorbereitung würde ich insbesondere diese Quellen heranziehen:
1. Microsoft Azure Architecture Center – AI Agent Orchestration Patterns: Gute Übersicht zu den unterschiedlichen Multi-Agent-Mustern und deren Vor- und Nachteilen.
2. Agent2Agent Protocol (A2A): Grundlage für die herstellerübergreifende Agentenkommunikation.
3. Model Context Protocol – Architecture: Verständnis der Trennung von Tools, Resources und Prompts.
4. NIST – Generative AI Risk Management Profile: Gute Grundlage für Governance, Risiken und Kontrollmechanismen.

Mein abschließendes Fazit
Ich würde den ersten Agenda-Punkt tatsächlich als eigenständigen Architektur-Workshop verstehen.

Das Ziel sollte nicht sein, am Ende ein möglichst komplexes Schaubild zu haben. Das Ziel sollte sein, dass ihr euch auf ein gemeinsames Verständnis einigt:
- Was ist unser Agent Orchestrator?
- Welche Verantwortung hat er?
- Welche Fähigkeiten benötigt er?
- Wie interagiert er mit lokalen Agentenplattformen?
- Wie gehen wir mit Wissen, Kontext und Daten um?
- Welche Kommunikationsstandards wollen wir unterstützen?
- Welche Freiheitsgrade geben wir unseren Agenten?
Und eine These würde ich als Diskussionsgrundlage ganz bewusst mitbringen:
Wir brauchen keinen zentralen Super-Agenten, der unsere gesamte HR-Landschaft steuert. Wir brauchen eine föderierte, herstellerunabhängige Orchestrierungsarchitektur, die spezialisierte Agenten und bestehende HR-Prozesse kontrolliert, sicher und nachvollziehbar zusammenarbeiten lässt.

Das wäre für mich das strategische Leitbild, auf das ihr hinarbeiten solltet.