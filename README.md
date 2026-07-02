BobbyCore — The Autonomous AI Orchestrator
Hello Bobby is een open‑source AI‑ecosysteem dat bestaat uit drie volledig gescheiden componenten:

BobbyBuddy — het fysieke wake‑word apparaat (microfoon, speaker, LCD display)

BobbyCore — het autonome AI‑brein dat intents begrijpt, entiteiten zoekt en acties uitvoert

Home Assistant — een externe smart‑home backend die alle entiteiten en automations bevat

Samen vormen ze een lokaal, privacy‑vriendelijk alternatief voor Alexa/Google Home — maar volledig modulair, uitbreidbaar en jouw eigendom.

🧩 System Overview
Hello Bobby werkt met drie losse installaties:

🟦 Home Assistant (HA)
Aparte installatie.
Bevat alle smart‑home entiteiten, automations en integraties.
BobbyCore communiceert met HA via de officiële API.

🟧 BobbyCore
Aparte installatie.
Dit is het AI‑brein dat:

spraak omzet naar intent

context begrijpt

entiteiten zoekt binnen HA

capabilities bepaalt

acties uitvoert

externe API’s gebruikt (alleen als toegestaan)

modulair uitbreidbaar is

BobbyCore is niet afhankelijk van HA en kan uitbreiden naar andere systemen.

🟩 BobbyBuddy (Wake‑Word Device)
BobbyBuddy is het fysieke apparaat dat de interactie met de gebruiker verzorgt.
Het bevat:

omni‑microfoon

wake‑word detectie (“Hello Bobby”)

luidsprekers voor audio‑feedback

LCD‑scherm voor visuele feedback

wifi/ethernet

compacte CPU (Pi Zero / Pi 5 / ESP32 / Jetson Nano)

Het LCD‑scherm toont:

status (“Luistert…”)

intent‑resultaten

foutmeldingen

contextvragen

animaties tijdens wake‑word

systeeminformatie

BobbyBuddy stuurt audio naar BobbyCore en toont de resultaten van acties.

we werken meerdere hardware varianten uit 
Bobby Devices (Ecosystem)
BobbyBuddy — full device (LCD + audio)
BobbyMini — small device (audio only)
BobbyDot — micro‑node (input only)

🎯 Doel van het project
Hello Bobby wil een lokaal, open, privacy‑vriendelijk AI‑apparaat zijn dat:

wakker wordt wanneer je hem roept

luistert naar wat je zegt

zelf begrijpt wat je bedoelt

zelf de juiste entiteiten vindt

zelf de juiste actie uitvoert

uitbreidbaar is met modules

werkt zonder cloud‑afhankelijkheid

Dit is zero‑configuration AI automation.

🧠 Architectuur
1. Wake Layer (BobbyBuddy)
Omni‑microfoon

Wake‑word detectie (“Hello Bobby”)

LCD‑feedback

Audio‑transport naar BobbyCore

2. Intent Layer (BobbyCore)
Speech‑to‑text

Intent parsing

Context‑begrip

Command‑routing

3. Execution Layer (BobbyCore + HA)
Entity discovery

Capability mapping

Action execution

Feedback naar BobbyBuddy

🔐 Privacy
BobbyCore zoekt nooit willekeurig API’s op internet.
Alle externe bronnen moeten expliciet door de gebruiker worden gekoppeld.
Alle acties worden uitgevoerd binnen het eigen ecosysteem van de gebruiker.
Alle audio blijft lokaal — geen cloud‑verwerking.

🛣️ Roadmap
[ ] BobbyBuddy hardware prototype

[ ] Wake‑word detectie

[ ] Audio‑transport naar BobbyCore

[ ] Intent‑engine

[ ] Entity‑finder

[ ] Capability‑mapper

[ ] Action‑executor

[ ] Home Assistant integratie

[ ] Externe API‑modules

[ ] Context‑engine

[ ] Public release v0.1.0

📚 Documentatie
Zie /docs voor:

system‑overview

architecture

modules

bobbybuddy hardware

roadmap

🧪 Proof of Concept (coming soon)
De eerste POC zal bestaan uit:

een werkende wake‑word pipeline

audio → BobbyCore → intent → HA → actie

LCD‑feedback

basis‑module structuur

🤝 Contribute
Dit project staat open voor:

hardware‑bouwers

Home Assistant gebruikers

AI‑enthousiastelingen

open‑source makers

Pull requests zijn welkom zodra de basis staat.
