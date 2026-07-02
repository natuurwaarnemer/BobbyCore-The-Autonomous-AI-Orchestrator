Maker Roadmap — BobbyCore Ecosystem
Deze roadmap beschrijft de praktische, maker‑gerichte stappen voor het bouwen van het Bobby‑ecosysteem:

BobbyBuddy — het hoofdapparaat met LCD‑scherm

BobbyCore — het autonome AI‑brein

Home Assistant integratie

Eenvoudige Bobby‑varianten (optioneel later)

De roadmap is opgesplitst in logische fases die je één voor één kunt uitvoeren.

🟦 Fase 1 — BobbyBuddy Hardware Prototype
1.1 Microfoon & Audio‑input
Selecteer omni‑microfoon

Test audio‑kwaliteit

Test ruisonderdrukking

Test audio‑streaming naar BobbyCore

1.2 LCD‑scherm
Kies LCD‑formaat

Test tekstweergave

Test statusweergave (“Luistert…”)

Test animaties (wake‑word)

Bouw basis‑UI‑framework

1.3 Speaker & Audio‑output
Kies speaker

Test TTS‑output

Test volume‑regeling

Test audio‑feedback

1.4 Behuizing
3D‑print ontwerp

Montage microfoon + LCD + speaker

Kabelmanagement

Ventilatie

1.5 Hardware‑controller
Kies CPU (Pi Zero / Pi 5 / ESP32 / Jetson Nano)

Test OS

Test drivers

Test netwerkverbinding

🟧 Fase 2 — Wake‑Word & Input Pipeline
2.1 Wake‑word detectie
“Hello Bobby” model trainen of kiezen

Test latency

Test false positives

Test false negatives

2.2 Audio‑transport
Real‑time audio stream naar BobbyCore

Buffering

Compressie (optioneel)

Foutafhandeling

2.3 LCD‑feedback
“Luistert…”

“Denkt…”

“Voert uit…”

“Klaar.”

🟩 Fase 3 — BobbyCore AI‑Brein
3.1 Speech‑to‑Text
Kies lokaal STT‑model

Test nauwkeurigheid

Test snelheid

Test ruisgevoeligheid

3.2 Intent‑engine
Intent parsing

Command‑routing

Synoniemen

Contextuele interpretatie

3.3 Entity‑finder
Automatische entiteit‑detectie in HA

Mapping van namen

Foutmeldingen bij onbekende entiteiten

3.4 Capability‑mapper
Detecteert wat een entiteit kan

Aan/uit, temperatuur, helderheid, modus

Automatische capability‑detectie

3.5 Action‑executor
Stuurt acties naar HA

Verwerkt resultaten

Stuurt feedback naar BobbyBuddy

🟪 Fase 4 — Home Assistant Integratie
4.1 API‑koppeling
HA WebSocket API

HA REST API

Authenticatie

4.2 Entiteit‑metadata
Namen

Types

Capabilities

Status

4.3 Acties
Aan/uit

Temperatuur instellen

Modus instellen

Scenes activeren

4.4 Foutafhandeling
Entiteit niet gevonden

Capability niet beschikbaar

Actie mislukt

🟫 Fase 5 — LCD‑UI Uitbreiding
5.1 Statusweergave
Luistert

Denkt

Voert uit

Klaar

5.2 Resultaatweergave
“Droger ingesteld op 45°C”

“Lamp keuken is aan”

5.3 Contextvragen
“Welke lamp bedoel je?”

“Welke temperatuur?”

5.4 Mini‑apps (optioneel)
Weer

Kalender

Sensorstatus

🟨 Fase 6 — Ecosysteem Uitbreiding (optioneel)
6.1 BobbyMini
Microfoon + speaker

Geen LCD

Kleine behuizing

6.2 BobbyDot
Alleen microfoon

Geen speaker

Geen LCD

Ultra‑simpel input‑node

6.3 Mesh‑communicatie
Alle Bobby’s praten met BobbyCore

BobbyBuddy geeft antwoorden terug

🟦 Fase 7 — Release v0.1.0
Minimale vereisten:
Werkende BobbyBuddy

Wake‑word detectie

Audio → BobbyCore → intent → HA → actie

LCD‑feedback

Basis‑module structuur

Documentatie in /docs

🟧 Fase 8 — Documentatie & Repo Structuur
8.1 Documenten
README

Roadmap

Architecture

BobbyBuddy hardware

Modules

8.2 Repo‑structuur
/core

/buddy

/docs

/integrations

🟩 Fase 9 — Toekomstige uitbreidingen
Context‑engine

Externe API‑modules

Multi‑room audio

Multi‑wake‑word

Personalisatie

Offline LLM

BobbyCloud (optioneel, later)
