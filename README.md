# ai_vibes

# Herausforderung 08: Slash-Befehle

## Beschreibung
In dieser Herausforderung haben Sie die Aufgabe, die bestehende KI-Chatbot-Anwendung zu erweitern, um "Slash-Befehle" zu unterstützen.

## Was sind Slash-Befehle?
Slash-Befehle sind spezielle Befehle, die Benutzer in eine Chat-Schnittstelle eingeben können, typischerweise beginnend mit einem `/` (Schrägstrich), um bestimmte Aktionen oder Funktionen auszulösen.  
Beispielsweise könnte in einer Chat-Anwendung die Eingabe von `/help` eine Liste verfügbarer Befehle anzeigen, oder `/giphy cat` könnte ein zufälliges Katzen-GIF einfügen.

Das Konzept hinter Slash-Befehlen ist es, Benutzern schnellen, tastaturgesteuerten Zugang zu erweiterten Funktionen zu bieten, ohne den Chat-Kontext zu verlassen.  
Wenn ein Benutzer einen Schrägstrich gefolgt von einem Befehl eingibt, fängt die Anwendung diese Eingabe ab, analysiert den Befehl und seine Argumente und führt dann die entsprechende Aktion aus.

## Beispiele aus beliebten Anwendungen
- **Slack:** `/remind me to call John at 3pm` setzt eine Erinnerung.  
- **Discord:** `/ban @user` verbannt einen Benutzer vom Server.  
- **Telegram:** `/start` startet eine Unterhaltung mit einem Bot.  
- **GitHub:** `/assign @username` weist ein Issue oder Pull Request einem Benutzer zu.

Diese Befehle verbessern die Produktivität und optimieren Arbeitsabläufe, indem sie Benutzern ermöglichen, komplexe Aktionen mit einfachen Texteingaben durchzuführen.

## Anwendungskontext
Dieser Abschnitt umreißt die beteiligten Bereiche der Anwendung. Slash-Befehle umfassen mehrere Bereiche wie:
- Chat-Nachrichtenverarbeitung, bevor die Eingabe an ein KI-Modell gesendet wird  
- Verschiedene Tools der Anwendung, z.B. könnte der Slash-Befehl `/weather` auf das bestehende Tool zugreifen und es verwenden  
- Die Chat-Nachricht-Komponente, die die spezialisierte Antwort vom Tool/Slash-Befehl rendert

## Relevante Komponenten
Das Lösen dieser Herausforderung umfasst die folgenden Komponenten:
- `ModelSelection` innerhalb der `chat.tsx`, `multimodal-input.tsx` Komponenten  

---

# Developer Akademie

- `/lib/ai/tools` für die Tool-Implementierungen, die unterstützt werden sollen  
- `toolbar.tsx` für das Rendern aller Tools enthält die Tool-Komponente sowie die Tools-Komponente.

## Slash-Befehl-Ideen
Falls keine Ideen vorhanden sind, könnten die folgenden Slash-Befehle mit dieser Herausforderung implementiert werden:

- `/weather` → gibt das aktuelle Wetter für den Standort des Benutzers unter Verwendung des Wetter-Tools zurück  
  - `/weather <STADT|ORTSNAME>` würde dann die Wetterinformationen für die angegebene STADT oder den ORT zurückgeben  

- `/suggest-project` → ein Slash-Befehl, der Schlüsselwörter als Eingabeargumente erhalten kann und dann Ideen für Projekte vorschlägt, die mit den Schlüsselwörtern verwandt sind  

- `/quiz create <THEMA>` → erstellt ein Quiz mit immer 10 Boolean-Fragen (JA/NEIN-Fragen)  
  - `/quiz -q <ANZAHL DER FRAGEN> create <THEMA>` → erstellt ein Quiz mit der angegebenen Anzahl von Boolean-Fragen für das bereitgestellte Thema  

---
