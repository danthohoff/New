Sehr gerne. Ich halte den dritten Punkt sogar für einen der spannendsten Teile eures Workshops, weil ihr hier die strategischen Architekturüberlegungen aus Punkt 1 und die fachlichen beziehungsweise technischen Anforderungen aus Punkt 2 auf konkrete Technologieoptionen herunterbrechen könnt.

Ich würde dabei bewusst nicht mit einem Anbieter starten und versuchen, eure Anforderungen in dessen Produktwelt abzubilden. Stattdessen würde ich vier unterschiedliche Architekturvarianten entwickeln und anschließend anhand eurer Anforderungen vergleichen.

Meine zentrale Empfehlung vorweg: Ich würde bei euch eine hybride, föderierte Architektur als ernsthaften Favoriten betrachten. ServiceNow und Oracle sollten ihre jeweiligen nativen Agentenfähigkeiten nutzen können. Darüber liegt eine herstellerübergreifende Orchestrierungsschicht, die systemübergreifende Zusammenarbeit ermöglicht. Die Integration, Sicherheit, Beobachtbarkeit und Governance sollten möglichst plattformübergreifend funktionieren.

Das bedeutet ausdrücklich nicht, dass ihr zwingend einen einzigen zentralen technischen Orchestrator benötigt. Es geht darum, eine gemeinsame Steuerungs- und Kontrollarchitektur zu schaffen.

# 1. Überblick: Welche vier Umsetzungsvarianten sollten wir betrachten?

Ich würde eure vier Optionen folgendermaßen strukturieren:

Variante A: ServiceNow-zentriert

Plattformansatz

[Very exciting news from ServiceNow! It’s time to put AI agents to work in every corner of your business. ✨ That’s why we’re introducing a series of breakthrough agentic AI innovations to help… | Oliver Wheeler](https://images.openai.com/static-rsc-4/lkcZmtiP0R7Hn2T6lNwFiOiRfuCXpUZSsdqY7INRUcY3LiGh84waIIMw7BR0ozFkubhZuT_6k4tzswEB1THwC8nMHWIwJABnU7oUjm2XB2yDlNbbDpfJuvZwhXMRdFSGcck1dTzvkbGh-4YZq5JcbzR9hpghn3DbYV0KlAoN4Mo?purpose=inline)

[linkedin.com](https://www.linkedin.com/posts/oliver-wheeler-servicenow_very-exciting-news-from-servicenow-its-activity-7290506865967255552--7QT?utm_source=chatgpt.com)

ServiceNow übernimmt die zentrale Orchestrierung. Agenten und Workflows anderer Plattformen werden angebunden.

Variante B: Microsoft-zentriert

Cloud-Plattformansatz

[Microsoft Foundry: An End-to-End Platform for Building, Governing, and Scaling AI | Microsoft Community Hub](https://images.openai.com/static-rsc-4/YIZ8ii8nTb57JZc4FCsnjfbFmJJY0JeEJnF9qRdEE_GArAT9use8BmxNTvxaa_NJWjm37Hlc9fVJrQLgwR_JopEsnvBdmTE4-ZPdKWFq98tjfaBRqbCh2jdvmn9cSqqSkxJFBilV5FV3R60tLZhDOpo6KSvYnnkDZUOt6dB-9KY?purpose=inline)

[techcommunity.microsoft.com](https://techcommunity.microsoft.com/blog/azure-ai-foundry-blog/microsoft-foundry-an-end-to-end-platform-for-building-governing-and-scaling-ai/4496736?utm_source=chatgpt.com)

Microsoft Foundry beziehungsweise die Microsoft-Agentenplattform bildet die zentrale Grundlage für Agentenmanagement und Orchestrierung.

Variante C: Azure + LangGraph

Framework-Ansatz

[LangGraph Platform in beta: New deployment options for scalable agent infrastructure](https://images.openai.com/static-rsc-4/aOAbh3JW95yvVn3yMfYf4IFRNmROQk7tUNOLHQgLJGjFBM1D_AOaYoTbUfuOB_2qmdXFBq3Gz7ud9mOerece-bzQDMqTL0IO0XyRzLfnfTxmzE9crUh4mYOOCnT93Oe-1deiCbmNoin75bT0D0Xna5pGZ2Of4PFN3MHFb297TT0?purpose=inline)

[blog.langchain.com](https://blog.langchain.com/langgraph-platform-announce/?utm_source=chatgpt.com)

Ihr baut eine eigene, flexible Orchestrierungsschicht auf Basis von LangGraph und Azure-Services.

Variante D: AWS-zentriert

Cloud-Plattformansatz

[From zero-shot forecast to purchase order with Amazon Bedrock AgentCore | AWS Architecture Blog](https://images.openai.com/static-rsc-4/TDZRtFFNedWrRZM04g3HkYxB8x0ONTOxmZ4HLyJj5mBS0JVF7Ko0qoHJNwETpm1Tfl5NHuDO55UWJOwqRH8AsvFSocZPJ2plp3T9KC6qQXLyLspr3AJfbtV59Gva3pyr8sonD9OBV1twS7xOsjHjmUWaCrFlzR1OhdWs3kuKyqw?purpose=inline)

[aws.amazon.com](https://aws.amazon.com/blogs/architecture/from-zero-shot-forecast-to-purchase-order-with-amazon-bedrock-agentcore/?utm_source=chatgpt.com)

AWS Bedrock und ergänzende AWS-Services übernehmen Agentenruntime, Orchestrierung, Integration und Governance.

Variante E: Föderierte Hybridarchitektur

Mein Favorit zur Prüfung

[What Is Multi-Agent Orchestration? A Complete Guide](https://images.openai.com/static-rsc-4/nXW5qXSz6YER6W3eJheVlhThg8S2xX7bDHaFQn44eP3qGxM8WPrfwci8tgfHbaqhOR9g27pV6IcghKHTF4wszPI-1zcQ-5EQOwflNVKwxcO0CYk5CJ1EFPKvrZ33QrNwJ5jg_6yxESura_SSh0fPFEMNh5PD-znl7jSKfr-NSnw?purpose=inline)

[truefoundry.com](https://www.truefoundry.com/blog/what-is-multi-agent-orchestration?utm_source=chatgpt.com)

Native Agentenplattformen bleiben bestehen. Eine übergreifende Schicht koordiniert die Zusammenarbeit und stellt gemeinsame Standards bereit.

Ich würde Variante E ergänzen, obwohl sie kein eigener Anbieter ist. Denn sie ist aus meiner Sicht die wichtigste Architekturhypothese, die ihr gegen die vier konkreten Anbieteroptionen testen solltet.

Vorab noch eine begriffliche Einordnung: Mit Microsoft würde ich nicht nur Azure AI Foundry betrachten, sondern die heutige Microsoft Foundry-Plattform, den Microsoft Agent Framework-Ansatz und die angrenzenden Copilot-/Power-Platform-Fähigkeiten. Bei ServiceNow würde ich zwischen AI Agent Orchestrator, AI Agent Studio und den übergreifenden Workflow- und Governance-Funktionen unterscheiden.

Die konkreten Produktnamen, Lizenzgrenzen und Funktionsumfänge solltet ihr für die im Unternehmen verfügbare Produktversion verifizieren. Die Architektur sollte nicht an einem Produktnamen hängen.

# 2. Variante A: ServiceNow als zentraler Agent Orchestrator

ServiceNow-zentrierte Architektur

[ServiceNow Launches AI Control Tower for Enterprise Agents](https://images.openai.com/static-rsc-4/43UNwvbZVcdKZwSe1FbV8gBMuMEOpoB0-sCEJnJm4rpJpWZnaM3tor9HaRyQ67lhalNd4yK_9olGWe0UPRZ3LlbVbYHBCDhG2OjDdmN3Ly6OgF1W-rJUswzMO42CDd2sEiNUxTIR666VtyuVSTPsoPTCzqrlLLKQRpVyx-Zd0R8?purpose=inline)

[thelettertwo.com](https://thelettertwo.com/2025/05/06/servicenow-ai-control-tower-enterprise-agents-agent-fabric-protocol/?utm_source=chatgpt.com)

## 2.1 Grundidee

ServiceNow übernimmt die zentrale Steuerung der Agentenlandschaft.

Das ist zunächst naheliegend, weil ServiceNow bereits eine wichtige Rolle in eurer HR-Prozesslandschaft spielt und ihr dort auch die ersten produktiven Agenten erwartet.

Die Idee wäre:

- ServiceNow Agenten werden nativ in ServiceNow entwickelt und betrieben.
- ServiceNow übernimmt die Orchestrierung der eigenen Agenten.
- Externe Agenten aus Oracle, Azure oder anderen Plattformen werden über standardisierte Schnittstellen eingebunden.
- Übergreifende HR-Prozesse können aus ServiceNow heraus gesteuert werden.
- Ein Teil der Governance und des Monitorings wird innerhalb der ServiceNow-Plattform umgesetzt.

Hier würde ich insbesondere den ServiceNow AI Agent Orchestrator als zentrale Komponente prüfen.

Wichtig ist aber: Ihr müsst herausfinden, ob dieser eure Anforderungen an eine plattformübergreifende Orchestrierung tatsächlich erfüllt oder primär auf das Zusammenspiel innerhalb des ServiceNow-Ökosystems ausgelegt ist.

## 2.2 Wie könnte die Architektur aussehen?

## Variante A – ServiceNow als zentrale Steuerung

ServiceNow – Agent Orchestration Layer

AI Agent Orchestrator

Agenten koordinieren

AI Agent Studio

Agenten erstellen und konfigurieren

Workflow Engine

HR-Prozesse steuern

Governance & Monitoring

Kontrolle und Nachvollziehbarkeit

Enterprise Integration Layer

APIs · Events · MCP-Adapter · Identity · Data Mapping

Oracle

Native Agenten und HR-Prozesse

Azure / Microsoft

Externe Agenten und Services

Avature

Recruiting-Daten und Services

Weitere Systeme

Eigenentwicklungen und Speziallösungen

Das ist eine logische Zielarchitektur, keine Darstellung der bereits nachgewiesenen Produktfunktionen.

## 2.3 Welche Komponenten würden wir nutzen?

| Architekturfähigkeit                   | Mögliche ServiceNow-Komponente                              |
| -------------------------------------- | ----------------------------------------------------------- |
| Agentenentwicklung                     | AI Agent Studio                                             |
| Agentenkoordination                    | AI Agent Orchestrator                                       |
| Prozesssteuerung                       | Workflow Studio / Flow Designer                             |
| HR-Prozessintegration                  | HR Service Delivery                                         |
| Tool- und Systemintegration            | Integration Hub                                             |
| Zentrale Daten- und Serviceintegration | ServiceNow APIs und Integration Hub                         |
| Governance                             | AI Control Tower und zugehörige Governance-Funktionen       |
| Monitoring                             | ServiceNow-Plattformfunktionen und ergänzende Observability |

Besonders spannend finde ich hier die Kombination aus Agentenorchestrierung und klassischer Workflow Engine.

Ihr könntet beispielsweise den gesamten HR-Prozess weiterhin in ServiceNow steuern und innerhalb des Prozesses einzelne Agentenaufgaben dynamisch orchestrieren.

## 2.4 Wie würden externe Agenten eingebunden?

Das ist der entscheidende Prüfpunkt.

Nehmen wir an, ein Oracle-Agent soll eine fachliche Teilaufgabe übernehmen.

ServiceNow könnte diesen über eine definierte Schnittstelle aufrufen.

Denkbare Varianten:

- REST API
- A2A-basierte Agentenkommunikation
- MCP-basierte Tool- beziehungsweise Serviceintegration
- Event-basierte Kommunikation

Ich würde hier insbesondere prüfen, wie gut ServiceNow externe Agenten als eigenständige Akteure behandeln kann.

Denn ein Oracle-Agent ist nicht einfach ein API-Endpunkt. Er kann selbst Kontext verwalten, mehrere Schritte durchführen und möglicherweise andere Agenten aufrufen.

## 2.5 Vorteile

- Sehr gute Nähe zu euren ersten ServiceNow-Anwendungsfällen.
- Integration in bestehende HR-Workflows.
- Weniger zusätzliche Plattformkomponenten.
- Native ServiceNow-Agenten können eng eingebunden werden.
- Potenziell schneller Einstieg.

## 2.6 Nachteile und Risiken

- Abhängigkeit von ServiceNow als zentralem Plattformanbieter.
- Mögliche Einschränkungen bei der Orchestrierung externer Agenten.
- Gefahr, dass Oracle-Agenten nur als externe Services behandelt werden.
- Begrenzte Freiheit bei individuellen Orchestrierungsmustern.
- Lizenz- und Plattformabhängigkeiten.

## 2.7 Was würde ich im Workshop prüfen?

1. Kann ServiceNow Agenten anderer Hersteller vollständig orchestrieren?
2. Kann der Orchestrator Agenten dynamisch auswählen und delegieren?
3. Unterstützt er A2A und MCP in der für uns benötigten Form?
4. Kann er externe Agentenzustände und längere Ausführungen verwalten?
5. Können wir externe Agenten in einer zentralen Registry verwalten?
6. Wie funktioniert die übergreifende Observability?
7. Wie werden Berechtigungen an externe Agenten übergeben?
8. Welche Funktionen sind Bestandteil der bestehenden Lizenzierung?

Meine Einschätzung: ServiceNow ist ein sehr ernst zu nehmender Kandidat für die lokale HR-Prozess- und Agentenorchestrierung. Ob es euer zentraler Enterprise Agent Orchestrator werden sollte, hängt aber entscheidend von den plattformübergreifenden Fähigkeiten ab.

# 3. Variante B: Microsoft als zentraler Agent Orchestrator

Microsoft-zentrierte Architektur

[針對整個組織使用 Microsoft 生態系統的 AI 代理人技術方案 - Cloud Adoption Framework | Microsoft Learn](https://images.openai.com/static-rsc-4/_eGOidGfkON9ixd9so6jPsJ00xIqwdtgHzZBPe5jvo3FieqyZxMYRdVafbuCK84JkAuBWyQYElfwhImoO7tl7P3s3LbN3NCRdU1SiboyDxgmyTqSueZJUKyy1s6eoeKEs6QemrSxLaIFgHtOUWI196ng48vbBYifG7FPVj2Id-g?purpose=inline)

[learn.microsoft.com](https://learn.microsoft.com/zh-tw/azure/cloud-adoption-framework/ai-agents/technology-solutions-plan-strategy?utm_source=chatgpt.com)

## 3.1 Grundidee

Microsoft ist aus meiner Sicht einer der interessantesten Kandidaten für eure Anforderungen, weil ihr hier mehrere Bausteine kombinieren könnt:

- Microsoft Foundry Agent Service als Managed Agent Runtime.
- Microsoft Agent Framework für die Entwicklung und Orchestrierung komplexer Agentensysteme.
- Azure Services für Integration, Security, Daten und Betrieb.
- Microsoft Entra ID für Identitäten und Berechtigungen.
- Application Insights und Azure Monitor für Observability.

Eine wichtige Unterscheidung:

Microsoft Foundry ist die Plattform, Microsoft Agent Framework ist das Framework für die Entwicklung und Orchestrierung.

Das sind zwei unterschiedliche Bausteine, die sich ergänzen.

Foundry unterstützt sowohl einfach konfigurierte Agents als auch selbst entwickelte, gehostete Agents. Für Letztere können unter anderem das Microsoft Agent Framework und LangGraph verwendet werden. Außerdem stellt Foundry Funktionen für Runtime, Identität, Tools und Observability bereit.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://learn.microsoft.com\&sz=32)

Microsoft Learn+1



## 3.2 Welche Komponenten würden wir nutzen?

| Architekturfähigkeit       | Microsoft-Komponente                                     |
| -------------------------- | -------------------------------------------------------- |
| Agentenentwicklung         | Microsoft Foundry / Agent Framework                      |
| Agent Runtime              | Foundry Agent Service                                    |
| Multi-Agent-Orchestrierung | Microsoft Agent Framework Workflows                      |
| Prozesssteuerung           | Azure Logic Apps / Durable Functions                     |
| API Management             | Azure API Management                                     |
| Event-Kommunikation        | Azure Event Grid / Service Bus                           |
| Tool Management            | Foundry Toolboxes                                        |
| MCP-Integration            | Foundry Toolboxes / eigene MCP-Server                    |
| Identity                   | Microsoft Entra ID                                       |
| Secrets                    | Azure Key Vault                                          |
| Monitoring                 | Azure Monitor / Application Insights                     |
| Evaluation                 | Foundry Evaluations und eigene Testframeworks            |
| Daten und Wissen           | Azure Storage, Azure AI Search und weitere Datenservices |

Wichtig ist, dass nicht alle diese Komponenten zwingend eingesetzt werden müssen. Ihr würdet sie abhängig von euren bestehenden Enterprise-Standards auswählen.

## 3.3 Wie könnte die Architektur aussehen?

## Variante B – Microsoft Foundry als zentrale Plattform

Microsoft Foundry – Agent Platform

Foundry Agent Service

Agent Runtime und Lifecycle

Agent Framework

Multi-Agent-Orchestrierung

Toolboxes

Tools und MCP

Observability

Tracing und Evaluation

Azure Enterprise Services

API Management

Logic Apps / Functions

Event Grid / Service Bus

Entra ID / Key Vault

ServiceNow

Native Agenten

Oracle

Native Agenten

Avature

APIs und Services

Weitere Systeme

Eigenentwicklungen

Hier übernimmt Microsoft die zentrale Agentenruntime und die übergreifende Orchestrierung. Die Fachsysteme bleiben weiterhin die führenden Systeme für ihre jeweiligen HR-Prozesse und Daten.

## 3.4 Welche Rolle spielt Microsoft Agent Framework?

Das ist für mich der wichtigste Baustein dieser Variante.

Das Framework bietet verschiedene Orchestrierungsmuster:

| Muster     | Bedeutung                        | HR-Beispiel                                                    |
| ---------- | -------------------------------- | -------------------------------------------------------------- |
| Sequential | Agenten arbeiten nacheinander    | Anfrage klassifizieren, Richtlinie prüfen, Antwort erstellen   |
| Concurrent | Agenten arbeiten parallel        | Mitarbeiter- und Organisationsinformationen parallel abrufen   |
| Handoff    | Agenten übergeben die Kontrolle  | HR Service Agent übergibt an Payroll Agent                     |
| Group Chat | Agenten arbeiten gemeinsam       | Mehrere Spezialagenten analysieren einen komplexen Sachverhalt |
| Magentic   | Supervisor koordiniert dynamisch | HR Manager Agent entscheidet über benötigte Spezialagenten     |

Das Framework unterstützt außerdem Human-in-the-Loop, Checkpointing und die Wiederaufnahme von Workflows.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://learn.microsoft.com\&sz=32)

Microsoft Learn+1



Das passt gut zu eurem zuvor entwickelten Orchestrierungsmodell.

## 3.5 Wie würde ein konkreter HR-Prozess aussehen?

Beispiel: Eine Mitarbeiteranfrage soll bearbeitet werden.

1. ServiceNow erhält die Anfrage.
2. Ein ServiceNow-Agent klassifiziert den Sachverhalt.
3. ServiceNow übergibt die Aufgabe an den zentralen Microsoft-Orchestrator.
4. Microsoft Agent Framework entscheidet, welche Spezialagenten benötigt werden.
5. Ein Oracle-Agent liefert die relevanten Mitarbeiterinformationen.
6. Ein HR Policy Agent recherchiert die Richtlinien.
7. Ein weiterer Agent erstellt einen Antwortvorschlag.
8. Ein Human-in-the-Loop-Schritt ermöglicht die Freigabe.
9. Das Ergebnis wird zurück an ServiceNow übergeben.

Dabei würde ich die Prozessverantwortung nicht automatisch an Microsoft übertragen. ServiceNow kann weiterhin den HR Case und seine fachlichen Prozesszustände verwalten.

## 3.6 Welche Rolle spielt Fabric beziehungsweise Fabric IQ?

Das würde ich in eurem Workshop separat betrachten.

Microsoft Fabric beziehungsweise Fabric IQ kann perspektivisch für semantische Datenmodelle, Datenintegration und kontextbezogene Informationsbereitstellung interessant sein.

Ich würde es allerdings nicht als Ersatz für einen HR Orchestrator betrachten.

Eine mögliche Aufteilung:

- Foundry und Agent Framework: Agenten und Orchestrierung.
- Fabric: Daten- und semantische Ebene.
- Azure Integration Services: technische Integration.
- Entra ID: Identitäten und Zugriffssteuerung.

Für eure HR-Ontologie könnte insbesondere die Frage interessant sein, ob ein gemeinsames semantisches HR-Modell in einer Microsoft-Datenarchitektur bereitgestellt werden kann.

## 3.7 Vorteile

- Umfangreiche Enterprise-Cloud-Infrastruktur.
- Gute Kombination aus Managed Runtime und eigener Entwicklung.
- Unterschiedliche Orchestrierungsmuster.
- Gute Anbindung an Microsoft-Identitäten und Sicherheitsmechanismen.
- Integration von MCP und eigenen Tools.
- Gute Möglichkeiten für Observability und Evaluation.
- Auch LangGraph-basierte Agenten können in der Plattform betrieben werden.

## 3.8 Nachteile und Risiken

- Hohe Abhängigkeit von Microsoft Cloud und deren Diensten.
- Komplexität durch die Vielzahl der verfügbaren Komponenten.
- Gefahr, zu viele unterschiedliche Microsoft-Produkte einzusetzen.
- Zusätzlicher Entwicklungsaufwand gegenüber einer reinen SaaS-Lösung.
- Native ServiceNow- und Oracle-Agenten müssen sauber integriert werden.
- Die Trennung zwischen Foundry, Agent Framework und Prozessplattform muss bewusst gestaltet werden.

## 3.9 Was sollte im Workshop geprüft werden?

1. Kann Microsoft die zentrale Orchestrierung aller HR-Agenten übernehmen?
2. Wie werden externe ServiceNow- und Oracle-Agenten integriert?
3. Welche Agenten sollten in Foundry gehostet werden und welche lokal?
4. Wie funktioniert das Zusammenspiel mit A2A und MCP?
5. Wie wird der Kontext über mehrere Agenten hinweg verwaltet?
6. Wie können Langzeitprozesse und Human-in-the-Loop umgesetzt werden?
7. Wie lassen sich Monitoring und Evaluation zentralisieren?
8. Welche Azure-Komponenten benötigen wir tatsächlich?
9. Wie hoch sind die laufenden Betriebs- und Lizenzkosten?

Meine Einschätzung: Microsoft ist für mich einer der stärksten Kandidaten, wenn ihr eine zentrale, flexibel erweiterbare Orchestrierungsplattform aufbauen wollt, die gleichzeitig Managed Services und individuelle Entwicklung ermöglicht.

# 4. Variante C: Azure + LangGraph als eigene Orchestrierungsplattform

Individueller Framework-Ansatz

[LangChain in Production: LangGraph Agents, LangSmith Observability & LCEL Patterns | Ilir Ivezaj](https://images.openai.com/static-rsc-4/N8n-G__vk6IbVvD41e4T6Pblu1LkmDA9CAv2b_T8f818LQ1DeCdti5TWsj6w8P4KL-7y4JDJN_LNqxBeZF8lQOO218j2rjjBmdTQbKfaBqG381OqY20A7JaVWLmgGipYj4xzxzRwKJabwvjrnjktEpDf1CwXwoEVGAh2etNVJYY?purpose=inline)

[ilirivezaj.com](https://ilirivezaj.com/ai/langchain-production?utm_source=chatgpt.com)

## 4.1 Grundidee

Diese Variante unterscheidet sich grundlegend von den vorherigen beiden.

Hier kauft ihr nicht primär eine fertige Orchestrierungsplattform, sondern baut euch eine eigene Orchestrierungsschicht.

Die zentrale Technologie dafür wäre LangGraph.

LangGraph ist ein Framework zur Entwicklung zustandsbehafteter Agenten-Workflows. Ihr beschreibt die Orchestrierung als Graph aus einzelnen Verarbeitungsschritten, Übergängen und Entscheidungslogiken.

Es ist besonders interessant, wenn ihr:

- Komplexe Multi-Agent-Systeme aufbauen wollt.
- Die Kontrolle über den Orchestrierungsprozess behalten möchtet.
- Unterschiedliche Agentenframeworks einbinden wollt.
- Eigene HR-spezifische Orchestrierungsmuster entwickeln wollt.
- Eine möglichst geringe Abhängigkeit von einem einzelnen Agentenplattformanbieter anstrebt.

Wichtig: LangGraph ist nicht automatisch eine vollständige Enterprise Agent Platform.

Ihr müsst weitere Komponenten für Deployment, Skalierung, Monitoring, Identitäten, Governance und Integration ergänzen.

## 4.2 Wie funktioniert LangGraph grundsätzlich?

Die zentrale Idee ist ein Graph.

Dieser besteht aus:

- Nodes: Einzelne Verarbeitungsschritte.
- Edges: Übergänge zwischen den Schritten.
- State: Gemeinsamer Zustand des Workflows.
- Conditional Edges: Dynamische Entscheidungen über den weiteren Ablauf.

Ein Beispiel:

Ein HR Orchestrator erhält eine Anfrage und entscheidet, welche Agenten benötigt werden.

Er kann:

1. Die Anfrage analysieren.
2. Einen HR Policy Agent aufrufen.
3. Einen Oracle-Agent aufrufen.
4. Ergebnisse zusammenführen.
5. Einen Qualitätsschritt ausführen.
6. Bei Bedarf einen Menschen einbeziehen.
7. Das Ergebnis zurückgeben.

Der Vorteil: Ihr habt vollständige Kontrolle darüber, wie der Ablauf gestaltet wird.

## 4.3 Wie könnte die Architektur aussehen?

## Variante C – Eigener HR Orchestrator mit LangGraph

HR Agent Orchestration Service

LangGraph Orchestration Runtime

State Management · Routing · Delegation · Checkpointing · HITL

Agent Registry

Agenten entdecken

Policy Engine

Kontrollmechanismen

Context Service

Kontext verwalten

Execution Manager

Aufgaben verwalten

Azure Platform Services

Azure Container Apps / AKS

PostgreSQL / State Store

Entra ID / Key Vault

Azure Monitor

Enterprise Integration Layer

APIs · MCP · A2A · Events · Business Services

ServiceNow Agents

Oracle Agents

Avature Services

Weitere Agenten

Das ist eine Architektur, bei der ihr den eigentlichen Orchestrator selbst entwickelt und betreibt.

## 4.4 Welche Komponenten benötigen wir?

| Architekturfähigkeit | Mögliche Technologie                      |
| -------------------- | ----------------------------------------- |
| Orchestrierung       | LangGraph                                 |
| Agentenruntime       | Eigene Container / LangGraph Deployment   |
| State Management     | LangGraph Checkpointer                    |
| Persistenz           | Azure Database for PostgreSQL             |
| Agent Registry       | Eigener Registry Service                  |
| API Gateway          | Azure API Management                      |
| Agentenkommunikation | A2A / REST                                |
| Toolintegration      | MCP Server                                |
| Events               | Azure Service Bus / Event Grid            |
| Identity             | Microsoft Entra ID                        |
| Secrets              | Azure Key Vault                           |
| Deployment           | Azure Container Apps oder AKS             |
| Monitoring           | OpenTelemetry / Azure Monitor             |
| Evaluation           | LangSmith und eigene Evaluation Pipelines |

LangGraph unterstützt Checkpointing, Unterbrechungen und die Wiederaufnahme von Workflows. Das ist gerade für HR-Prozesse mit längeren Wartezeiten und menschlichen Freigaben relevant.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.langchain.com\&sz=32)

Docs by LangChain+1



## 4.5 Wie könnte die zentrale Orchestrierung konkret aussehen?

Ich würde einen HR-spezifischen Orchestrator entwickeln.

Dieser wäre nicht zwingend selbst ein autonomer Agent, sondern zunächst eine kontrollierte Workflow- und Koordinationsinstanz.

Das halte ich für einen wichtigen Unterschied.

Ein möglicher Ablauf:

1. Ein HR-Prozess übergibt eine Aufgabe an den Orchestrator.
2. Der Orchestrator analysiert die Aufgabe.
3. Er ermittelt geeignete Agenten über eine Registry.
4. Eine Policy Engine prüft die zulässigen Agenten und Tools.
5. LangGraph steuert die Ausführung.
6. Die Agenten liefern ihre Ergebnisse zurück.
7. Der Orchestrator prüft die Vollständigkeit.
8. Gegebenenfalls wird ein Human-in-the-Loop-Schritt ausgelöst.
9. Der finale Status wird an das aufrufende System zurückgegeben.

Ein besonderes Augenmerk würde ich auf das State Management legen.

Denn bei systemübergreifenden HR-Prozessen kann eine Aufgabe mehrere Stunden oder Tage laufen.

LangGraph kann einen Workflow unterbrechen, seinen Zustand persistieren und später fortsetzen. Das ist eine sehr gute Grundlage, ersetzt aber nicht die Definition eines unternehmensweiten Prozesszustands und dessen fachlicher Verantwortlichkeit.

## 4.6 Welche Rolle spielt LangSmith?

[Debugging Deep Agents with LangSmith](https://images.openai.com/static-rsc-4/u8MAXjYX0y3qy8XKt3eJg6Pko5gSpIn5qIahqQpm7FLnZt91Ye7OFDzh5H9GuUchgouEJGGWrNTDiZIVFAc6N7OomJrRkVji5QBAXqkjBGNvpS0_nxFhrlB18aDX6Jb5SVrldeE3rspIUJYkcZVRT1NAxYHFPzmk0H0IvpwBo5Q?purpose=inline)

[blog.langchain.com](https://www.blog.langchain.com/debugging-deep-agents-with-langsmith/?utm_source=chatgpt.com)

LangSmith ist das ergänzende Produktökosystem für Entwicklung, Evaluation, Tracing und Betrieb von LangChain-/LangGraph-Anwendungen.

Ich würde es insbesondere für folgende Aufgaben prüfen:

- Debugging von Agentenabläufen.
- Visualisierung von Graph-Ausführungen.
- Tracing einzelner Agentenschritte.
- Evaluation von Agentenergebnissen.
- Vergleich verschiedener Prompt- und Modellversionen.

Für euer Unternehmen würde ich aber prüfen, welche Daten tatsächlich an LangSmith übertragen werden dürfen und ob ihr eine geeignete Deployment- und Datenresidenzvariante nutzen könnt.

LangSmith sollte außerdem nicht automatisch euer gesamtes Enterprise Monitoring ersetzen.

## 4.7 Vorteile

- Sehr hohe Flexibilität.
- Volle Kontrolle über die Orchestrierungslogik.
- Plattformübergreifende Agentenintegration.
- Individuelle HR-spezifische Orchestrierungsmuster.
- Geringere Abhängigkeit von einem einzelnen Agentenplattformanbieter.
- Gute Möglichkeiten für deterministische und dynamische Orchestrierung.
- Gute Integration mit unterschiedlichen Modellanbietern.

## 4.8 Nachteile und Risiken

- Ihr müsst einen großen Teil der Plattform selbst entwickeln.
- Höherer Entwicklungs- und Betriebsaufwand.
- Eigene Verantwortung für Registry, Governance und Policy Enforcement.
- Komplexität beim State Management.
- Höhere Anforderungen an Software Engineering und DevOps.
- Gefahr, dass ihr eine eigene Agentenplattform entwickelt, statt euch auf HR-Mehrwert zu konzentrieren.

Ein wichtiger Punkt: LangGraph allein ist kein Ersatz für eine Enterprise Integration Platform und auch kein vollständiges IAM- oder Governance-System.

## 4.9 Was sollte im Workshop geprüft werden?

1. Wie viel Orchestrierungslogik wollen wir selbst entwickeln?
2. Benötigen wir eine eigene HR Agent Registry?
3. Wie werden Agenten unterschiedlicher Anbieter eingebunden?
4. Wie verwalten wir Langzeitprozesse und Zustände?
5. Wie integrieren wir LangGraph in unsere bestehende Azure-Landschaft?
6. Welche Governance-Funktionen müssen wir selbst entwickeln?
7. Wie gewährleisten wir eine zentrale Observability?
8. Welche Kompetenzen benötigen wir für den dauerhaften Betrieb?
9. Wie viel Eigenentwicklung ist wirtschaftlich vertretbar?

Meine Einschätzung: Azure + LangGraph ist eine sehr interessante Option, wenn ihr bewusst eine eigene, herstellerunabhängige Orchestrierungsschicht aufbauen möchtet. Ihr solltet allerdings die zusätzlichen Engineering- und Betriebsverantwortlichkeiten nicht unterschätzen.

# 5. Variante D: AWS als zentrale Agentenplattform

AWS-zentrierte Architektur

[Understanding Bedrock AgentCore | CodeSignal Learn](https://images.openai.com/static-rsc-4/Qcbm5DAnaS8nOG_YFpZ_--UoFuBlQCTNb0A5W6EtVQ2UObuGhpv4o2aGAA2ay4mTIHKz41UsNqdgtLA0wzuT2ppR9F0W6gGpUXIVwsaCg5qKL9RV_t7aJUfrwln-3RAxpHbjFbZE-YIGltnyXXDKPdd6JOCGK-FVcNfwTywSOk4?purpose=inline)

[codesignal.com](https://codesignal.com/learn/courses/deploying-agents-aws-with-bedrock-agentcore/lessons/understanding-bedrock-agentcore-1?utm_source=chatgpt.com)

## 5.1 Grundidee

Bei AWS würde ich heute nicht mehr primär mit der klassischen Amazon-Bedrock-Agentenarchitektur starten.

Ich würde vor allem Amazon Bedrock AgentCore betrachten.

Das ist wichtig, weil AWS die klassischen Bedrock Agents inzwischen als Bedrock Agents Classic bezeichnet und für Neukunden auf AgentCore als neuere Architektur verweist.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

Amazon Bedrock+1



AgentCore ist modular aufgebaut und ermöglicht es, Agenten mit unterschiedlichen Frameworks und Modellanbietern zu betreiben.

Das macht AWS durchaus interessant für eure heterogene Landschaft.

## 5.2 Welche Komponenten würden wir nutzen?

| Architekturfähigkeit  | AWS-Komponente                                           |
| --------------------- | -------------------------------------------------------- |
| Agentenruntime        | Bedrock AgentCore Runtime                                |
| Agentenentwicklung    | Strands Agents / LangGraph / eigene Frameworks           |
| Agentenorchestrierung | Eigene Agentenlogik / AgentCore Harness / Step Functions |
| Tool Management       | AgentCore Gateway                                        |
| Agent Identity        | AgentCore Identity                                       |
| Agent Memory          | AgentCore Memory                                         |
| Monitoring            | AgentCore Observability / CloudWatch                     |
| Evaluation            | AgentCore Evaluations                                    |
| API Management        | Amazon API Gateway                                       |
| Event-Kommunikation   | EventBridge / SQS                                        |
| Workflow-Steuerung    | AWS Step Functions                                       |
| Secrets               | AWS Secrets Manager                                      |
| Datenintegration      | AWS Glue und weitere AWS-Datenservices                   |

Ein großer Vorteil: AgentCore ist nicht auf ein einziges Agentenframework oder Modell beschränkt. Die Dokumentation nennt unter anderem LangGraph, CrewAI, Strands Agents und weitere Frameworks sowie MCP und A2A.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

Amazon Bedrock AgentCore+1



## 5.3 Wie könnte die Architektur aussehen?

## Variante D – AWS Bedrock AgentCore

Amazon Bedrock AgentCore

Runtime

Agentenausführung

Gateway

Tools und Agenten

Identity

Berechtigungen

Memory

Kontext und Gedächtnis

Observability

Monitoring und Tracing

Evaluations

Qualitätsmessung

AWS Integration & Workflow Services

Step Functions · API Gateway · EventBridge · SQS

Enterprise Integration Layer

HR Business Services · MCP · A2A · APIs

ServiceNow

Oracle

Avature

Weitere Systeme

## 5.4 Welche Rolle spielt AgentCore Gateway?

Das finde ich besonders interessant.

AgentCore Gateway ermöglicht es, bestehende APIs, Lambda-Funktionen und Services als MCP-kompatible Tools bereitzustellen.

Darüber hinaus können auch externe Agenten und HTTP-Services eingebunden werden.

Das bedeutet:

Ihr könnt eure bestehenden HR-Systeme hinter einem kontrollierten Gateway verfügbar machen, ohne dass jeder Agent eigene Integrationslogik implementieren muss.

Beispielsweise:

- Oracle Employee Service.
- ServiceNow Case Service.
- Avature Candidate Service.
- HR Policy Retrieval Service.

AgentCore Gateway kann dabei die Authentifizierung und den Zugriff auf die jeweiligen Tools unterstützen.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.aws.amazon.com\&sz=32)

Amazon Bedrock AgentCore+1



## 5.5 Welche Rolle spielt AWS Step Functions?

Ich würde hier bewusst zwischen Agentenorchestrierung und Workflow-Orchestrierung unterscheiden.

Step Functions ist besonders interessant für deterministische Prozessabläufe.

Beispiel:

1. Mitarbeiteranfrage empfangen.
2. Agentenaufgabe starten.
3. Auf das Ergebnis warten.
4. Bei Bedarf menschliche Freigabe anfordern.
5. Eine Systemaktion ausführen.
6. Prozess abschließen.

Der Agent selbst kann über AgentCore betrieben werden.

Step Functions kontrolliert dagegen den übergeordneten Ablauf.

Das ist eine sehr ähnliche Architekturidee wie bei Microsoft mit Logic Apps beziehungsweise Durable Functions.

## 5.6 Vorteile

- Modulare Agentenplattform.
- Unterschiedliche Frameworks und Modelle möglich.
- Umfangreiche Security- und Runtime-Funktionen.
- MCP- und A2A-Unterstützung.
- Gute Möglichkeiten für Tool-Gateway und Agent Identity.
- Kombination mit klassischen Workflow-Services.
- Gute Möglichkeiten für skalierbaren Betrieb.

## 5.7 Nachteile und Risiken

- Aufbau einer zusätzlichen Cloud-Plattform, sofern AWS nicht ohnehin strategisch etabliert ist.
- Zusätzliche Komplexität bei hybriden Cloud-Architekturen.
- Mehrere AWS-Services müssen zusammenspielen.
- Potenziell hohe Anforderungen an das AWS-Betriebswissen.
- Die Integration in Microsoft- und ServiceNow-Umgebungen muss sauber geplant werden.

## 5.8 Was sollte im Workshop geprüft werden?

1. Welche Agentenfähigkeiten benötigen wir tatsächlich aus AgentCore?
2. Kann AgentCore als übergreifender Orchestrator fungieren oder benötigen wir eine zusätzliche Koordinationslogik?
3. Wie werden ServiceNow- und Oracle-Agenten eingebunden?
4. Wie funktionieren MCP und A2A im Zusammenspiel?
5. Welche Rolle übernehmen Step Functions und EventBridge?
6. Wie wird die Agentenidentität systemübergreifend umgesetzt?
7. Wie lässt sich die Observability in unser Enterprise Monitoring integrieren?
8. Welche zusätzlichen Cloud- und Betriebsabhängigkeiten entstehen?

Meine Einschätzung: AWS AgentCore ist eine technisch sehr interessante, modulare Alternative. Für euch würde ich sie insbesondere dann ernsthaft verfolgen, wenn AWS bereits eine strategische Rolle in eurer Unternehmensarchitektur hat oder ihr eine sehr flexible, frameworkunabhängige Agentenruntime aufbauen möchtet.

# 6. Variante E: Föderierte Hybridarchitektur – mein Favorit für eure Ausgangslage

Strategische Zielarchitektur zur Prüfung

[Agentic Orchestration for Automation with Google Cloud and Vertex AI Agent Builder](https://images.openai.com/static-rsc-4/9xL6YhMra2NTDt7QmfZGF3R9z8TmLVGIv1Se1QUQcCSFRxZVJ7aOWCQLm7nSPSXzMHLD_Y34atx7OcZoTiTS5YWbufES72Hfz-kXonEN6P_cA7g127hYGwbQ6npWc6tSQjbKPWyHXEGhck5u3ajtSJk3NorF1yEhwSXE4YFyw7M?purpose=inline)

[linkedin.com](https://www.linkedin.com/pulse/agentic-orchestration-automation-google-cloud-vertex-ai-agent-kkz8c?utm_source=chatgpt.com)

Jetzt kommen wir zu der Variante, die ich persönlich am spannendsten finde.

Ich glaube, dass ihr euch nicht zwingend zwischen ServiceNow, Microsoft, LangGraph und AWS entscheiden müsst.

Vielmehr könntet ihr eine Architektur entwickeln, in der jede Plattform ihre Stärken ausspielt und trotzdem eine gemeinsame Orchestrierung und Governance möglich ist.

## 6.1 Grundidee: Föderierte Orchestrierung

Ich würde drei Grundprinzipien verfolgen:

1\. Lokale Autonomie

ServiceNow und Oracle dürfen ihre eigenen Agenten, Agententeams und Prozessabläufe betreiben.

2\. Zentrale Koordination

Systemübergreifende Aufgaben werden durch eine übergreifende HR-Orchestrierung koordiniert.

3\. Gemeinsame Governance

Unabhängig davon, wo ein Agent läuft, gelten gemeinsame Standards für Identität, Berechtigungen, Monitoring, Evaluation und Lifecycle.

Das bedeutet: Der zentrale Orchestrator muss nicht jede interne Aktion jedes Agenten kennen. Er muss aber wissen, welchen Agenten er aufrufen kann, wofür dieser verantwortlich ist, welche Berechtigungen gelten und wie er den Auftrag überwacht.

## 6.2 Wie könnte die Architektur aussehen?

## Variante E – Föderierte HR Agent Architecture

## Enterprise HR Agent Orchestration

Zentrale Koordination über System- und Plattformgrenzen hinweg

Agent Registry

Agenten entdecken

Routing & Delegation

Agenten auswählen

Context Management

Kontext bereitstellen

Policy Enforcement

Regeln durchsetzen

ServiceNow Domain

AI Agent Orchestrator

AI Agent Studio

HR Workflows

Lokale Agenten und Prozesssteuerung

Oracle Domain

AI Agent Studio

Agent Teams

Fusion Workflows

Lokale Agenten und Prozesssteuerung

Interoperability & Integration Layer

A2A · MCP · APIs · Events · Business Services

Avature · Eigenentwicklungen · weitere HR-Systeme

Fachsysteme, Datenquellen und spezialisierte Agenten

Plattformübergreifende Enterprise Services

Identity · Security · Observability · Evaluation · Agent Registry · HR Semantic Layer · Lifecycle Management

Die letzte Ebene ist dabei bewusst horizontal dargestellt. Diese Fähigkeiten sollten nicht ausschließlich in der zentralen Orchestrierungsruntime liegen.

## 6.3 Welche Plattform übernimmt welche Rolle?

Ich würde zunächst folgende Verantwortlichkeiten prüfen:

| Plattform         | Primäre Rolle                                                               |
| ----------------- | --------------------------------------------------------------------------- |
| ServiceNow        | HR Service Workflows und lokale Agentenorchestrierung                       |
| Oracle            | HCM-nahe Agenten und operative HR-Aktionen                                  |
| Microsoft / Azure | Zentrale Orchestrierung, Integration und Enterprise Services                |
| LangGraph         | Individuelle Orchestrierungslogik für komplexe HR-Anwendungsfälle           |
| AWS               | Alternative Runtime- und Integrationsplattform, falls strategisch gewünscht |
| Avature           | Recruiting-Fachsystem und gegebenenfalls lokale Agentenfähigkeiten          |

Hier würde ich eine wichtige Einschränkung machen:

Ihr solltet nicht automatisch alle Plattformen für alle Aufgaben einsetzen.

Beispielsweise braucht ihr nicht gleichzeitig Microsoft Agent Framework und LangGraph als zentrale Orchestrierungsframeworks. Das würde unnötige Komplexität erzeugen.

Vielmehr könnte Microsoft Foundry die zentrale Runtime bereitstellen und LangGraph nur für besonders komplexe, individuelle Orchestrierungsabläufe eingesetzt werden.

Oder ihr entscheidet euch bewusst für LangGraph als zentrale Orchestrierung und verwendet Foundry primär als Managed Runtime und Modellplattform.

## 6.4 Ein konkretes Beispiel: Ende-zu-Ende-Prozess über mehrere Plattformen

Nehmen wir einen internen Positionswechsel.

## Cross-Platform HR Agent Orchestration

1\. ServiceNow

HR Case wird gestartet

2\. Zentraler HR Orchestrator

Aufgabe analysieren und Agenten auswählen

3a. Oracle Agent

Mitarbeiter- und Positionsdaten prüfen

3b. HR Policy Agent

Richtlinien recherchieren

4\. Zentraler Orchestrator

Ergebnisse zusammenführen und validieren

5\. Menschliche Freigabe

HR-Verantwortlicher entscheidet

6\. Oracle

Freigegebene Aktion ausführen

7\. ServiceNow

HR Case abschließen

Hier ist besonders wichtig, dass der zentrale Orchestrator nicht selbst alle fachlichen Regeln kennen muss.

Er koordiniert die Zusammenarbeit und stellt sicher, dass die Aufgaben korrekt ausgeführt werden.

Die Fachlogik bleibt möglichst nah an den jeweiligen HR-Systemen beziehungsweise fachlichen Services.

## 6.5 Wo liegen die Vorteile?

- Ihr könnt eure bestehenden Plattforminvestitionen nutzen.
- ServiceNow und Oracle müssen nicht durch eine neue zentrale Agentenplattform ersetzt werden.
- Ihr könnt unterschiedliche Agentenframeworks zulassen.
- Die Architektur bleibt erweiterbar.
- Ihr reduziert die Abhängigkeit von einem einzelnen Anbieter.
- Governance und Monitoring können vereinheitlicht werden.
- Neue Systeme und Anbieter lassen sich schrittweise anbinden.

## 6.6 Wo liegen die Nachteile?

Die föderierte Architektur ist nicht automatisch einfacher.

Sie hat auch Herausforderungen:

- Mehrere Orchestrierungsebenen müssen sauber abgegrenzt werden.
- Zustände und Kontext müssen systemübergreifend verwaltet werden.
- Unterschiedliche Plattformen haben unterschiedliche Sicherheitsmodelle.
- Monitoring muss über Plattformgrenzen funktionieren.
- Es braucht klare Regeln, welcher Orchestrator in welchem Fall die Kontrolle hat.
- Es besteht die Gefahr, zu viele technische Komponenten aufzubauen.

Gerade deshalb würde ich die Verantwortlichkeiten sehr präzise definieren.

## 6.7 Welche Grundsatzentscheidungen sind erforderlich?

1. Welche Aufgaben werden zentral und welche lokal orchestriert?
2. Welche Agenten müssen in einer gemeinsamen Registry registriert sein?
3. Welche Protokolle werden verpflichtend unterstützt?
4. Wo liegt der führende Prozesszustand?
5. Wie werden Identitäten und Berechtigungen übergeben?
6. Welche Monitoring-Daten werden zentral aggregiert?
7. Welche Fähigkeiten werden zentral als Services bereitgestellt?
8. Wie verhindern wir doppelte Orchestrierungslogik?

Meine Einschätzung: Diese Variante passt am besten zu eurer heterogenen Ausgangslage. Sie sollte deshalb die Referenzarchitektur sein, gegen die ihr die vier Anbieteroptionen bewertet.

# 7. Eine besondere Betrachtung: Welche Rolle sollte Oracle einnehmen?

Das würde ich im Workshop unbedingt separat behandeln.

Ihr habt Oracle als einen eurer größten Anbieter und erwartet dort erste produktive Agenten. Deshalb würde ich Oracle nicht nur als externes System betrachten, sondern als eigenständige Agentendomäne.

[Bounded Autonomy: The Operating Model Behind Scalable AI Agents](https://images.openai.com/static-rsc-4/C6OfD2D9He2AhrqgSHe5UuVLJVv85BMXevnxjKhRR1GmqQTuOkndUJRGKO4U0hUCocKUTXQMGnECE5XSuS2skctZjjp-oqTp1m15eS8VHef56rNouXj9xvumnBTxC0jgKwm6pcjNKwSe3Dl9B1-bcFrpVfqmTrxByf6WplA6F7U?purpose=inline)

[linkedin.com](https://www.linkedin.com/pulse/bounded-autonomy-operating-model-behind-scalable-ai-agents-john-cloud-diszc?utm_source=chatgpt.com)

Oracle bietet mit AI Agent Studio for Fusion Applications eine native Entwicklungs- und Ausführungsumgebung für Agenten.

Interessant ist dabei insbesondere die Unterscheidung zwischen:

- Supervisor Agent Teams: Ein Supervisor koordiniert Agenten und weitere Artefakte.
- Workflow Agent Teams: Eine vorgegebene Abfolge von Agenten und Verarbeitungsschritten.

Außerdem können Business Objects, Tools, Themen und menschliche Freigaben integriert werden.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://docs.oracle.com\&sz=32)

Oracle Docs+1



Das passt sehr gut zu meiner Empfehlung, die fachliche Orchestrierung innerhalb eines Systems möglichst dort zu belassen, wo die fachlichen Daten und Prozesse liegen.

## 7.1 Meine Empfehlung für Oracle

Ich würde Oracle zunächst drei Verantwortlichkeiten geben:

1\. Native HR-Agenten

Agenten, die eng mit Oracle HCM und dessen Geschäftsobjekten verbunden sind, sollten möglichst nativ in Oracle entwickelt werden.

2\. Lokale Agentenorchestrierung

Wenn mehrere Oracle-Agenten gemeinsam eine HCM-Aufgabe bearbeiten, kann Oracle seine nativen Agent Teams einsetzen.

3\. Standardisierte externe Kommunikation

Oracle-Agenten, die für systemübergreifende Aufgaben benötigt werden, sollten über standardisierte Schnittstellen erreichbar sein.

Beispielsweise könnte ein Oracle-Agent die fachliche Aufgabe `getEmployeeContext()` übernehmen, während ein übergreifender HR Orchestrator ihn als spezialisierten Agenten aufruft.

## 7.2 Was ich vermeiden würde

Ich würde nicht versuchen, sämtliche Oracle-internen HCM-Prozesse durch einen externen zentralen Orchestrator nachzubauen.

Das würde bedeuten, dass ihr Fachlogik aus Oracle herauszieht und an anderer Stelle erneut implementiert.

Das wäre aus meiner Sicht weder wartungsfreundlich noch sinnvoll.

Stattdessen:

- Oracle orchestriert intern.
- Der zentrale HR Orchestrator orchestriert übergreifend.
- Der Integration Layer stellt standardisierte Services bereit.

Diese Aufteilung ist eine wichtige Architekturleitplanke.

# 8. Vergleich der fünf Architekturvarianten

Jetzt würde ich die Varianten anhand eines einheitlichen Kriterienmodells vergleichen.

Wichtig: Die folgende Bewertung ist meine qualitative Architektur-Einschätzung. Sie ist keine gemessene Produktbewertung und ersetzt keinen Proof of Concept.

## 8.1 Funktionaler Vergleich

| Kriterium                  | ServiceNow                    | Microsoft               | Azure + LangGraph                | AWS                    | Föderiert                        |
| -------------------------- | ----------------------------- | ----------------------- | -------------------------------- | ---------------------- | -------------------------------- |
| Native Agentenentwicklung  | Sehr gut                      | Sehr gut                | Eigenentwicklung                 | Sehr gut               | Plattformabhängig                |
| Multi-Agent-Orchestrierung | Sehr gut im eigenen Ökosystem | Sehr gut                | Sehr flexibel                    | Sehr gut               | Kombination                      |
| Cross-Platform-Fähigkeit   | Zu validieren                 | Gut bis sehr gut        | Sehr flexibel                    | Gut bis sehr gut       | Architekturabhängig              |
| Prozessintegration         | Sehr gut                      | Gut                     | Eigenentwicklung                 | Gut                    | Sehr gut bei sauberer Aufteilung |
| Integration Layer          | Integration Hub               | Azure Services          | Azure Services, Eigenentwicklung | AWS Services           | Bestehende Enterprise-Lösung     |
| State Management           | Plattformabhängig             | Managed und Framework   | Eigenverantwortlich              | Managed Services       | Verteilt                         |
| Observability              | AI Control Tower              | Foundry / Azure Monitor | LangSmith / OpenTelemetry        | AgentCore / CloudWatch | Zentral zu gestalten             |
| Security & Identity        | ServiceNow-Ökosystem          | Entra ID                | Eigenverantwortlich auf Azure    | AgentCore Identity     | Föderiertes Modell               |
| Flexibilität               | Mittel bis hoch               | Hoch                    | Sehr hoch                        | Hoch                   | Sehr hoch                        |
| Eigenentwicklungsaufwand   | Eher gering bis mittel        | Mittel                  | Hoch                             | Mittel                 | Mittel bis hoch                  |

Eine wichtige Nuance: ServiceNow hat mit AI Agent Fabric ausdrücklich auch eine plattformübergreifende Kommunikations- und Integrationsstrategie angekündigt. AI Control Tower positioniert sich zudem als herstellerübergreifende Governance- und Monitoring-Lösung. Deshalb würde ich ServiceNow keinesfalls vorschnell als reine Insellösung bewerten. Die tatsächliche Tiefe der Integration mit euren Oracle-Agenten muss praktisch nachgewiesen werden.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://newsroom.servicenow.com\&sz=32)

ServiceNow Newsroom+2



## 8.2 Vergleich der strategischen Eigenschaften

| Kriterium                      | ServiceNow                    | Microsoft       | LangGraph | AWS             | Föderiert |
| ------------------------------ | ----------------------------- | --------------- | --------- | --------------- | --------- |
| Herstellerunabhängigkeit       | Mittel                        | Mittel          | Hoch      | Mittel bis hoch | Hoch      |
| Kontrolle über Architektur     | Mittel                        | Hoch            | Sehr hoch | Hoch            | Sehr hoch |
| Time-to-Value                  | Hoch bei ServiceNow Use Cases | Hoch            | Mittel    | Mittel          | Mittel    |
| Betriebskomplexität            | Mittel                        | Mittel bis hoch | Hoch      | Mittel bis hoch | Hoch      |
| Plattformabhängigkeit          | Hoch                          | Hoch            | Geringer  | Hoch            | Geringer  |
| Eignung für eure Heterogenität | Gut                           | Sehr gut        | Sehr gut  | Gut             | Sehr gut  |

# 9. Meine Empfehlung: Welche Architektur würde ich bei euch verfolgen?

Wenn ich eure Ausgangssituation betrachte, würde ich nicht mit einer vollständigen Festlegung auf einen der vier Anbieter starten.

Ich würde stattdessen eine föderierte Zielarchitektur mit Microsoft als bevorzugtem Kandidaten für die zentrale Orchestrierung untersuchen.

Warum?

Ich sehe bei euch vier wesentliche Anforderungen:

1. Ihr habt mehrere große Plattformen, die eigene Agenten entwickeln werden.
2. Die ersten produktiven Agenten entstehen voraussichtlich in ServiceNow und Oracle.
3. Ihr wollt langfristig nicht von einem einzelnen Anbieter abhängig sein.
4. Ihr braucht trotzdem eine zentrale Steuerungsmöglichkeit für systemübergreifende Prozesse.

Daraus würde ich folgende Zielarchitektur ableiten.

## 9.1 Mein Architekturvorschlag

# HR Agentic Enterprise Architecture

## 1. Central HR Orchestration Layer

Bevorzugte Technologieoption: Microsoft Foundry + Microsoft Agent Framework

Agent Registry

Discovery und Routing

Orchestration Engine

Koordination und Delegation

Context Management

Kontext und State

Policy Enforcement

Kontrollierte Ausführung

2\. Cross-Platform Governance & Control

Agent Inventory · Identity · Security · Evaluation · Monitoring · Lifecycle

3\. Enterprise Integration Layer

Azure API Management · MCP Gateway · A2A · Event Services · HR Business APIs

4a. ServiceNow Domain

AI Agent Studio

AI Agent Orchestrator

HR Workflows

4b. Oracle Domain

AI Agent Studio

Agent Teams

Fusion Workflows

5\. HR Enterprise Systems

Oracle HCM · ServiceNow · Avature · Eigenentwicklungen · Speziallösungen

6\. HR Knowledge & Semantic Layer

HR Ontologie · RAG · Knowledge Sources · HR Core Data Model

Das ist bewusst ein logisches Architekturmodell. Die Governance-Funktionen könnten teilweise durch ServiceNow AI Control Tower, Microsoft Foundry und bestehende Enterprise-Security-Lösungen umgesetzt werden. Ihr müsst nicht sämtliche Funktionen doppelt aufbauen.

## 9.2 Warum Microsoft als zentrale Orchestrierung?

Ich würde Microsoft aus folgenden Gründen bevorzugt untersuchen:

- Ihr könnt eigene Orchestrierungslogik mit dem Microsoft Agent Framework entwickeln.
- Foundry bietet eine Managed Runtime.
- Unterschiedliche Frameworks können gehostet werden, darunter LangGraph.
- Toolboxes ermöglichen eine standardisierte Bereitstellung von Tools und MCP-Endpunkten.
- Entra ID bietet eine gute Grundlage für Identitätsmanagement.
- Ihr könnt eure Azure-Integrationsarchitektur nutzen.
- Die Orchestrierungsmuster sind nicht auf einen einzelnen HR-Prozess zugeschnitten.

Die Kombination aus Foundry und Agent Framework ist für mich besonders interessant, weil ihr euch nicht vollständig auf eine deklarative Plattform festlegen müsst. Ihr könnt bei einfachen Agenten Managed Services nutzen und bei komplexen Szenarien eigene Orchestrierungslogik entwickeln.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://learn.microsoft.com\&sz=32)

Microsoft Learn+2



## 9.3 Warum würde ich trotzdem ServiceNow AI Control Tower berücksichtigen?

Das ist ein wichtiger Punkt.

Ich würde unterscheiden zwischen:

- Orchestrierung von Agenten.
- Governance und Kontrolle von Agenten.

Das sind nicht zwingend dieselben Aufgaben.

ServiceNow AI Control Tower beziehungsweise die inzwischen weiterentwickelte Super Intelligence Control Tower-Produktlinie positioniert sich als übergreifende Kontrollinstanz für Agenten, Modelle, Identitäten und Workflows – auch von Drittanbietern.

Das könnte bei euch sehr interessant sein, selbst wenn Microsoft die zentrale Orchestrierung übernimmt.

Ihr könntet also durchaus eine Architektur haben, bei der:

- Microsoft die Agentenkoordination übernimmt.
- ServiceNow die übergreifende AI Governance unterstützt.
- ServiceNow zusätzlich seine lokalen HR-Agenten orchestriert.
- Oracle seine eigenen HCM-Agenten orchestriert.

Das ist kein Widerspruch, solange ihr die Zuständigkeiten klar trennt. Die tatsächlichen Integrationsmöglichkeiten und Lizenzvoraussetzungen müssen natürlich validiert werden.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.servicenow.com\&sz=32)

ServiceNow+1



# 10. Die wichtigste Architekturentscheidung: Wo liegt die Grenze zwischen den Orchestratoren?

Das wäre für mich eine der zentralen Diskussionen im dritten Workshop-Block.

Denn eine hybride Architektur funktioniert nur, wenn ihr klare Verantwortungsgrenzen definiert.

Ich würde folgende Aufteilung vorschlagen:

| Aufgabe                                   | Verantwortlicher                   |
| ----------------------------------------- | ---------------------------------- |
| HR-End-to-End-Prozess in ServiceNow       | ServiceNow                         |
| Oracle-interne HCM-Prozesse               | Oracle                             |
| Interne ServiceNow-Agenten koordinieren   | ServiceNow                         |
| Interne Oracle-Agenten koordinieren       | Oracle                             |
| Systemübergreifende Agenten auswählen     | Zentraler HR Orchestrator          |
| Agentenplattformen anbinden               | Enterprise Integration Layer       |
| Übergreifende Agentenregistrierung        | Enterprise Agent Registry          |
| Übergreifende Sicherheitsrichtlinien      | Enterprise Security / Policy Layer |
| Zentrale Qualitäts- und Betriebsübersicht | Enterprise Observability           |

Ein Beispiel:

Ein Oracle-Agent benötigt zur Bearbeitung einer Aufgabe einen weiteren Oracle-Agenten.

Dann sollte Oracle die interne Koordination übernehmen.

Wenn ein ServiceNow-Prozess hingegen einen Oracle-Agenten und einen ServiceNow-Agenten benötigt, sollte die übergreifende Koordination über den zentralen HR Orchestrator laufen.

Das Prinzip lautet: So lokal wie möglich orchestrieren, so zentral wie nötig koordinieren.

Ich würde diesen Satz tatsächlich als eines eurer Architekturprinzipien festhalten.

# 11. Wie würde ich die Umsetzung konkret angehen?

Ich würde auf keinen Fall versuchen, die gesamte Zielarchitektur auf einmal zu implementieren.

Stattdessen würde ich einen schrittweisen Aufbau empfehlen.

## Phase 1: Foundation – Die Grundlagen schaffen

Priorität 1

Ziel: Die ersten Agenten sollen produktiv werden können, ohne dass ihr euch architektonisch einschränkt.

Umsetzung:

1. Gemeinsame Agentenstandards definieren.
2. Eine erste Agent Registry aufbauen.
3. Ein einheitliches Agenten-Metadatenmodell etablieren.
4. Identity- und Berechtigungskonzept entwickeln.
5. API- und MCP-Integrationsstandard definieren.
6. End-to-End-Tracing vorbereiten.
7. Anforderungen an Agentenfreigabe und Evaluation festlegen.

Wichtig: Ihr benötigt zu diesem Zeitpunkt noch keinen vollumfänglichen zentralen Orchestrator.

## Phase 2: First Cross-Platform Orchestration

Priorität 2

Ziel: Einen ersten systemübergreifenden HR-Prozess mit mehreren Agenten umsetzen.

Beispiel:

- Ein ServiceNow-Agent übernimmt die Anfrage.
- Ein Oracle-Agent liefert Mitarbeiterinformationen.
- Ein HR Policy Agent recherchiert Richtlinien.
- Ein zentraler Orchestrator koordiniert die Zusammenarbeit.
- Ein Mensch gibt die finale Aktion frei.

Dafür würde ich zunächst einen begrenzten, klar definierten Prozess auswählen.

Die Implementierung sollte möglichst mit den vorhandenen nativen Agenten beginnen, statt neue Agenten ausschließlich für den PoC zu entwickeln.

## Phase 3: Enterprise Orchestration Layer

Priorität 3

Jetzt wird aus dem ersten Cross-Platform-PoC eine wiederverwendbare Architektur.

Ausbau:

- Dynamisches Agent Routing
- Agent Discovery
- Zentrale Kontextverwaltung
- Einheitliche Fehlerbehandlung
- Standardisierte Delegation
- Erweiterte Governance
- Zentrale Monitoring- und Evaluation-Funktionen
- Wiederverwendbare HR Business Services

## Phase 4: Skalierung und Optimierung

Jetzt könnt ihr weitere HR-Domänen integrieren:

- Recruiting
- Onboarding
- Talent Management
- Learning
- Compensation
- Employee Services
- HR Administration

Perspektivisch können dann auch komplexere Multi-Agent-Szenarien umgesetzt werden.

# 12. Der entscheidende Schritt: Ein Proof of Concept mit allen relevanten Anbietern

Ich würde die Technologieentscheidung nicht ausschließlich anhand von Präsentationen und Produktdemonstrationen treffen.

Ich würde einen gezielten PoC aufsetzen.

Und zwar nicht vier völlig unterschiedliche PoCs, sondern möglichst einen gemeinsamen Use Case, der auf den verschiedenen Architekturen umgesetzt wird.

## 12.1 Mein Vorschlag für den PoC

Use Case: Systemübergreifende Bearbeitung einer HR-Mitarbeiteranfrage

Anforderungen:

- Einstieg über ServiceNow.
- Mitarbeiterinformationen aus Oracle.
- HR-Richtlinien aus einer zentralen Wissensquelle.
- Mindestens zwei spezialisierte Agenten.
- Agentenkommunikation über standardisierte Schnittstellen.
- Menschliche Freigabe vor einer kritischen Aktion.
- Rückgabe des Ergebnisses an ServiceNow.
- Durchgängiges Monitoring.

Damit könnt ihr fast sämtliche relevanten Architekturfragen praktisch testen.

## 12.2 Was sollte im PoC verglichen werden?

| Testkriterium       | Was soll nachgewiesen werden?                             |
| ------------------- | --------------------------------------------------------- |
| Agent Discovery     | Kann ein Agent einen anderen Agenten finden?              |
| Routing             | Kann der Orchestrator den richtigen Agenten auswählen?    |
| Interoperabilität   | Funktioniert die Kommunikation über Plattformgrenzen?     |
| Context Propagation | Wird der richtige Kontext weitergegeben?                  |
| State Management    | Kann ein Prozess unterbrochen und fortgesetzt werden?     |
| Security            | Werden Identitäten und Berechtigungen korrekt übertragen? |
| Human-in-the-Loop   | Funktionieren Freigaben zuverlässig?                      |
| Error Handling      | Was passiert bei Ausfall eines Agenten?                   |
| Observability       | Können wir den gesamten Ablauf nachvollziehen?            |
| Performance         | Wie lange dauert der gesamte Prozess?                     |
| Cost                | Was kostet eine erfolgreiche Bearbeitung?                 |
| Maintainability     | Wie aufwendig sind Änderungen und Erweiterungen?          |

## 12.3 Wie würde ich die Anbieter vergleichen?

Ich würde eine Gewichtung einführen:

| Bewertungskriterium                   | Gewicht |
| ------------------------------------- | ------- |
| Plattformübergreifende Orchestrierung | 20 %    |
| Security und Governance               | 15 %    |
| Integration in bestehende HR-Systeme  | 15 %    |
| Flexibilität und Erweiterbarkeit      | 15 %    |
| Observability und Monitoring          | 10 %    |
| Prozess- und State Management         | 10 %    |
| Betriebsaufwand                       | 10 %    |
| Kosten                                | 5 %     |
| Gesamt                                | 100 %   |

Die Anbieter sollten dieselben Szenarien und Abnahmekriterien durchlaufen.

Ich würde außerdem zwei unterschiedliche PoC-Varianten unterscheiden:

- Variante 1: Zentrale Orchestrierung mit Microsoft Foundry / Agent Framework.
- Variante 2: Föderierte Orchestrierung mit lokalen ServiceNow- und Oracle-Agenten und einem zentralen Koordinationslayer.

LangGraph würde ich als dritte technische Vergleichsoption aufnehmen, insbesondere um den Mehrwert einer eigenen Orchestrierungslogik gegenüber dem Managed-Ansatz zu messen.

# 13. Welche konkreten Fragen würde ich für den dritten Workshop-Block vorbereiten?

Hier würde ich die Diskussion bewusst auf Architekturentscheidungen fokussieren.

## Themenblock A: Architekturvarianten

1. Wollen wir eine zentrale oder föderierte Orchestrierungsarchitektur?
2. Welche Orchestrierungsaufgaben sollen lokal bleiben?
3. Welche Aufgaben müssen zentral erfolgen?
4. Benötigen wir eine eigenständige HR Orchestration Runtime?
5. Welche Rolle sollen bestehende Plattformen übernehmen?

## Themenblock B: ServiceNow

1. Wie weit reichen die Fähigkeiten des AI Agent Orchestrators über ServiceNow hinaus?
2. Welche Rolle spielen AI Agent Fabric und AI Control Tower?
3. Kann ServiceNow externe Agenten als vollwertige Agenten integrieren?
4. Welche Funktionen sind bereits durch unsere bestehenden Lizenzen abgedeckt?

## Themenblock C: Microsoft

1. Ist Foundry Agent Service unsere zentrale Runtime?
2. Nutzen wir Microsoft Agent Framework oder LangGraph?
3. Wie viel eigene Orchestrierungslogik müssen wir entwickeln?
4. Welche Azure Services benötigen wir zusätzlich?
5. Welche Rolle übernimmt Microsoft bei Governance und Agentenmanagement?

## Themenblock D: Azure + LangGraph

1. Ist eine eigene Orchestrierungsplattform langfristig sinnvoll?
2. Welche Funktionen müssen wir selbst entwickeln?
3. Welche Kompetenzen benötigen wir?
4. Wie können wir Eigenentwicklung und Managed Services kombinieren?
5. Wie stellen wir den nachhaltigen Betrieb sicher?

## Themenblock E: AWS

1. Ist AgentCore für uns eine realistische Alternative?
2. Welche Vorteile bietet es gegenüber Microsoft Foundry?
3. Wie gut können wir bestehende Agenten integrieren?
4. Welche zusätzlichen Cloud-Abhängigkeiten entstehen?

## Themenblock F: Oracle

1. Welche Agenten sollen nativ in Oracle entstehen?
2. Welche Orchestrierungsfähigkeiten bietet AI Agent Studio?
3. Wie können Oracle-Agenten systemübergreifend genutzt werden?
4. Wie vermeiden wir doppelte fachliche Prozesslogik?

## Themenblock G: Zielarchitektur und Entscheidung

1. Welche Variante erfüllt unsere Anforderungen am besten?
2. Wo benötigen wir zusätzliche Eigenentwicklung?
3. Welche Komponenten können wir wiederverwenden?
4. Welche Abhängigkeiten entstehen?
5. Wie starten wir einen gemeinsamen PoC?

# 14. Was sollte am Ende des dritten Workshop-Blocks vorliegen?

Ich würde sieben konkrete Ergebnisse erwarten:

1\. Architekturentscheidung

Welche Architekturvariante verfolgen wir grundsätzlich: zentral, föderiert oder hybrid?

2\. Technologie- und Komponentenlandkarte

Welche Rolle übernehmen ServiceNow, Microsoft, Oracle und gegebenenfalls AWS beziehungsweise LangGraph?

3\. Logische und technische Referenzarchitektur

Wie sehen die zentralen Komponenten und ihre Schnittstellen aus?

4\. Integrations- und Protokollstrategie

Welche Standards verwenden wir für Agenten, Tools, Daten und Events?

5\. Anbieterbewertung

Vergleich der Plattformen anhand eines einheitlichen Kriterienmodells.

6\. PoC-Konzept

Gemeinsamer Use Case, Testkriterien, technische Umsetzung und Abnahmekriterien.

7\. Technologische Roadmap

Welche Komponenten bauen wir wann auf und welche bestehenden Plattformfähigkeiten nutzen wir?

# 15. Meine abschließende Einschätzung

Wenn ich alle eure Rahmenbedingungen zusammennehme, würde ich folgende strategische Position vertreten:

1\. ServiceNow und Oracle bleiben zunächst die führenden Agentendomänen.

Ihr solltet die dort entstehenden Agenten nicht künstlich aus ihren nativen Plattformen herauslösen.

2\. Eine zentrale Orchestrierung sollte unabhängig von diesen Domänen aufgebaut werden können.

Dafür würde ich Microsoft Foundry und Microsoft Agent Framework als erste Option untersuchen. LangGraph würde ich als ernsthafte Alternative für individuelle Orchestrierungsanforderungen bewerten.

3\. ServiceNow AI Control Tower sollte als übergreifende Governance-Option geprüft werden.

Die Governance- und Orchestrierungsfrage sollte nicht automatisch an dieselbe Plattform gebunden sein.

4\. Ein gemeinsamer Integration Layer ist unverzichtbar.

Ich würde bestehende Enterprise-Integrationslösungen nutzen und diese um standardisierte Agenten- und Tool-Schnittstellen erweitern.

5\. Die Architektur muss bewusst föderiert sein.

Das ist für mich die wichtigste strategische Leitentscheidung.

Ihr solltet nicht versuchen, alle Agenten in eine einzige Plattform zu zwingen.

# 16. Eine wichtige Ergänzung zu eurer Gesamtworkshop-Agenda

Ich würde eure drei Architekturblöcke jetzt folgendermaßen miteinander verknüpfen:

Agenda 1

# Zielbild entwickeln

Was wollen wir bauen?

- Mandat und Rolle des Orchestrators
- Orchestrierungsebenen
- Funktionale Capabilities
- Wissen und Kontext
- Protokolle und Muster

Ergebnis: Logisches Architekturzielbild

Agenda 2

# Vertiefung der Architektur

Was muss unsere Architektur leisten?

- Agentic Process Design
- Observability
- Integration Layer
- Ontologie und Semantik
- Security und Governance
- Evaluation und Testing
- Operations und Lifecycle

Ergebnis: Anforderungen und Architekturprinzipien

Agenda 3

# Technologie und Umsetzung

Wie setzen wir es um?

- ServiceNow
- Microsoft
- Azure + LangGraph
- AWS
- Föderierte Hybridarchitektur
- Anbieterbewertung und PoC

Ergebnis: Technische Referenzarchitektur und Umsetzungsentscheidung

Agenda 4

# Umsetzung starten

Wer macht was bis wann?

- Verantwortlichkeiten
- Betriebsmodell
- Roadmap
- PoC
- Erste produktive Agenten

Ergebnis: Konkreter Umsetzungsplan

## 17. Weiterführende Quellen für die Anbieterbewertung

Für die Vorbereitung würde ich direkt mit den offiziellen Dokumentationen arbeiten:

| Anbieter   | Relevante Dokumentation                                                                                                                                                                                                                                  |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ServiceNow | [AI Agents & AI Agent Orchestrator](https://www.servicenow.com/products/ai-agents.html?utm_source=chatgpt.com)                                                                                                                                           |
| ServiceNow | [Super Intelligence Control Tower](https://www.servicenow.com/products/ai-control-tower.html?utm_source=chatgpt.com)                                                                                                                                     |
| ServiceNow | [AI Agent Fabric](https://newsroom.servicenow.com/press-releases/details/2025/ServiceNow-Launches-AI-Control-Tower-a-Centralized-Command-Center-to-Govern-Manage-Secure-and-Realize-Value-From-Any-AI-Agent-Model-and-Workflow/?utm_source=chatgpt.com)  |
| Microsoft  | [Foundry Agent Service](https://learn.microsoft.com/azure/ai-foundry/agents/overview?trk=article-ssr-frontend-pulse_little-text-block\&utm_source=chatgpt.com)                                                                                           |
| Microsoft  | [Agent Framework – Orchestration Patterns](https://learn.microsoft.com/agent-framework/workflows/orchestrations/?utm_source=chatgpt.com)                                                                                                                 |
| Oracle     | [AI Agent Studio](https://docs.oracle.com/en/cloud/saas/fusion-ai/26d/aiaas/overview-of-ai-agent-studio.html?utm_source=chatgpt.com)                                                                                                                     |
| Oracle     | [Agent Teams und Workflows](https://docs.oracle.com/en/cloud/saas/fusion-ai/26b/aiaas/get-started.html?utm_source=chatgpt.com)                                                                                                                           |
| AWS        | [Amazon Bedrock AgentCore](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/?utm_source=chatgpt.com)                                                                                                                                        |
| AWS        | [AgentCore Gateway](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/gateway.html?sc_channel=ps\&utm_source=chatgpt.com)                                                                                                                    |
| LangGraph  | [Thinking in LangGraph](https://newsroom.servicenow.com/press-releases/details/2025/ServiceNow-announces-new-agentic-AI-innovations-to-autonomously-solve-the-most-complex-enterprise-challenges-01-29-2025-traffic/default.aspx?utm_source=chatgpt.com) |
| LangSmith  | [LangSmith Architecture](https://www.servicenow.com/de/products/ai-control-tower.html?utm_source=chatgpt.com)                                                                                                                                            |

Mein wichtigster Rat für euren Workshop:

Geht nicht mit der Frage hinein, welcher Anbieter den besten Orchestrator hat.

Geht mit der Frage hinein:

Welche Fähigkeiten müssen wir unternehmensweit bereitstellen, welche davon können unsere bestehenden Plattformen bereits übernehmen und welche Technologie-Kombination ermöglicht uns, langfristig eine herstellerunabhängige HR-Agentenlandschaft aufzubauen?

Wenn ihr diese Frage sauber beantwortet, ergibt sich die Technologieentscheidung wesentlich natürlicher.

Und ich würde tatsächlich versuchen, den Workshop mit einer ersten Skizze der föderierten Hybridarchitektur zu eröffnen – ausdrücklich als Hypothese, nicht als bereits getroffene Entscheidung. Das gibt der Diskussion eine konkrete Grundlage, ohne die Teilnehmer zu früh auf einen Anbieter festzulegen.