# NanoC-Client unter Windows – Kurzanleitung

> English version: see [English guide](#nanoc-client-on-windows-english) below.

Diese Anleitung beschreibt die Installation und den ersten Test des NanoC-Clients
unter Windows für den Tech-Age-Survival-Server.

## Verbindungsdaten

- Server: `joesworld.ipv64.net`
- Port: `41100`
- TLS-Fingerprint:
  `01:6A:FA:52:9C:F6:2A:C9:EA:DA:A9:A5:CB:9E:62:DA:3F:3B:BB:15:25:16:89:8B:8C:0E:83:64:F2:DA:10:7A`
- Token: pro Controller, siehe Schritt 4

Der Fingerprint kann sich ändern, wenn der Server ein neues Zertifikat bekommt.
Dann den neuen Wert vom Server-Owner verwenden.

## 1. Voraussetzungen

- Luanti
- Python 3 für Windows (bei der Installation **Add Python to PATH** aktivieren)
- Visual Studio Code
- Internetzugang zu GitHub

## 2. Client installieren

1. Auf <https://github.com/joe7575/nanoc_client> den grünen Button **Code** →
   **Download ZIP** wählen und die Datei lokal auspacken.
2. In Windows ein Terminal (PowerShell oder Eingabeaufforderung) im
   entpackten Ordner öffnen.
3. Client installieren:
   ```bat
   py -m pip install .
   ```
   Falls `py` nicht gefunden wird:
   ```bat
   python -m pip install .
   ```
   Bei Rechteproblemen `--user` anhängen.
4. Prüfen:
   ```bat
   nanoc --help
   where nanoc-dap
   ```
   `nanoc-dap` muss gefunden werden; die VS-Code-Extension startet diesen
   Adapter. Wenn `where nanoc-dap` nichts findet, den Python-`Scripts`-Ordner
   in den PATH aufnehmen (oder den Fallback in Schritt 3 verwenden).

## 3. VS Code Extension installieren

1. Im entpackten Client-Ordner die VSIX bauen:
   ```bat
   py vscode\build_vsix.py
   ```
   Die VSIX ist absichtlich nicht im Git-Repository (`.gitignore`); das Skript
   baut sie lokal.
2. Installieren:
   ```bat
   code --install-extension vscode\nanoc-debug.vsix
   ```
   Falls `code` nicht gefunden wird: in VS Code
   `Shell Command: Install 'code' command in PATH` ausführen (oder VS Code
   neu starten).
3. Prüfen:
   ```bat
   code --list-extensions --show-versions
   ```
   Erwartet: `joe7575.nanoc-debug@0.4.1` (oder neuer).
4. VS Code neu laden (Fenster schließen und öffnen oder
   `Developer: Reload Window`).
5. **`nanoc.dapPath` ist normalerweise nicht nötig** – die Extension findet
   `nanoc-dap` über den PATH. Nur falls sie den Adapter nicht findet, in den
   VS-Code-Settings setzen:
   ```json
   "nanoc.dapPath": "C:\\Pfad\\zu\\venv\\Scripts\\nanoc-dap.exe"
   ```
6. Eine Warnung wie `(node:...) [DEP0169] ...` beim Installieren ist eine
   Node.js-Deprecation-Warnung und harmlos, solange die Installation
   erfolgreich war.

## 4. Im Spiel: Controller und Terminal

1. Einen **NanoC-Controller** craften (Rezept im Spiel nachschauen) und
   platzieren.
2. Ein **Terminal** (`termlib:terminal1`) craften.
3. Das Terminal in die Hand nehmen, den Controller **linksklicken**, das
   Terminal daneben platzieren, das Terminal öffnen und `@connect` eingeben.
4. Den Controller **rechtsklicken** → Schaltfläche **Token** → Token mit
   `Ctrl-C` kopieren. Der Token ist persönlich und nur für diesen Controller;
   nicht weitergeben.
5. Optional: dem Controller mit dem Techage Info Tool (sneak + platzieren)
   einen Namen geben.
6. In der Nähe des Controllers bleiben oder den Bereich forceloaden, damit er
   geladen bleibt.

## 5. VS Code: `launch.json`

Den entpackten Client-Ordner (oder einen eigenen Programordner) in VS Code
öffnen und `.vscode\launch.json` anlegen. Der Wrapper mit `version` und
`configurations` ist Pflicht:

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "nanoc",
      "request": "attach",
      "name": "NanoC Tech-Age-Survival",
      "host": "joesworld.ipv64.net",
      "port": 41100,
      "token": "<TOKEN>",
      "tls": true,
      "tlsFingerprint": "01:6A:FA:52:9C:F6:2A:C9:EA:DA:A9:A5:CB:9E:62:DA:3F:3B:BB:15:25:16:89:8B:8C:0E:83:64:F2:DA:10:7A",
      "source": "${file}",
      "program": "${file}",
      "upload": true
    }
  ]
}
```

- `<TOKEN>` durch den Token aus Schritt 4 ersetzen.
- `source` und `program` zeigen auf die aktive Datei; sie muss gespeichert sein.
- Den Token nicht in ein öffentliches Repository committen.

## 6. Mini-Programm anlegen

Im geöffneten Ordner `main.nanoc` anlegen:

```c
// NanoC controller demo
int32 count = 0;

while (1) {
    count = count + 1
    printf("NanoC ready, count=%d\n", count)
    sleep(1000)
}
```

Speichern. Das Programm zählt jede Sekunde hoch und schreibt die Ausgabe auf
das Terminal.

## 7. Starten

1. `main.nanoc` in VS Code aktiv lassen.
2. **F5** drücken. Die Datei wird hochgeladen, kompiliert und gestartet.
3. Falls die VM am Einstieg pausiert: nochmals **F5** (Continue).
4. Im Spiel erscheint im verbundenen Terminal:
   ```text
   NanoC ready, count=1
   NanoC ready, count=2
   ...
   ```
5. Beenden mit **Shift+F5** (Stop) oder über das Controller-Menü.

## 8. Verbindung testen (optional)

Mit dem Token aus Schritt 4 kann die Bridge direkt geprüft werden:

```bat
nanoc catalog --host joesworld.ipv64.net --port 41100 --tls --tls-fingerprint "01:6A:FA:52:9C:F6:2A:C9:EA:DA:A9:A5:CB:9E:62:DA:3F:3B:BB:15:25:16:89:8B:8C:0E:83:64:F2:DA:10:7A" --token <TOKEN>
```

Es kommt JSON mit dem Topic-Katalog zurück; damit sind TLS, Token und Bridge
in Ordnung.

## 9. Fehlersuche

- `connection refused` / `connection reset`: Server/Port falsch, Bridge nicht
  erreichbar, oder TLS-Fingerprint passt nicht.
- `bad token`: Token gehört zu einem anderen Controller oder ist veraltet.
- `NOT_LOADED`: Der Controller-Bereich ist nicht geladen – in der Nähe bleiben
  oder forceloaden.
- Zertifikat/Fingerprint: Der Server hat ein neues Zertifikat; neuen
  Fingerprint verwenden.
- Extension findet den Adapter nicht: `nanoc.dapPath` auf
  `...\Scripts\nanoc-dap.exe` setzen (Schritt 3).
- Keine Terminalausgabe: Terminal mit `@connect` verbunden? Programm
  hochgeladen? Nach dem ersten F5 ggf. ein zweites F5 (Continue)?
- `DEP0169`-Warnung bei der VSIX-Installation: harmlos.

---

# NanoC client on Windows (English)

This is the English translation of the German quick guide above.

## Connection data

- Server: `joesworld.ipv64.net`
- Port: `41100`
- TLS fingerprint:
  `01:6A:FA:52:9C:F6:2A:C9:EA:DA:A9:A5:CB:9E:62:DA:3F:3B:BB:15:25:16:89:8B:8C:0E:83:64:F2:DA:10:7A`
- Token: per controller, see step 4

The fingerprint changes when the server gets a new certificate; use the new
value from the server owner in that case.

## 1. Prerequisites

- Luanti
- Python 3 for Windows (enable **Add Python to PATH** during installation)
- Visual Studio Code
- Internet access to GitHub

## 2. Install the client

1. Open <https://github.com/joe7575/nanoc_client>, use the green **Code** →
   **Download ZIP** button and unpack the file.
2. Open a terminal (PowerShell or Command Prompt) in the unpacked folder.
3. Install the client:
   ```bat
   py -m pip install .
   ```
   If `py` is not found:
   ```bat
   python -m pip install .
   ```
   Add `--user` if you hit permission problems.
4. Verify:
   ```bat
   nanoc --help
   where nanoc-dap
   ```
   `nanoc-dap` must be found; the VS Code extension starts this adapter. If
   `where nanoc-dap` prints nothing, add Python's `Scripts` folder to PATH (or
   use the fallback in step 3).

## 3. Install the VS Code extension

1. In the unpacked client folder, build the VSIX:
   ```bat
   py vscode\build_vsix.py
   ```
   The VSIX is intentionally not in the Git repository (`.gitignore`); the
   script builds it locally.
2. Install it:
   ```bat
   code --install-extension vscode\nanoc-debug.vsix
   ```
   If `code` is not found, run
   `Shell Command: Install 'code' command in PATH` in VS Code (or restart
   VS Code).
3. Verify:
   ```bat
   code --list-extensions --show-versions
   ```
   Expected: `joe7575.nanoc-debug@0.4.1` (or newer).
4. Reload VS Code (close/reopen the window or run
   `Developer: Reload Window`).
5. **`nanoc.dapPath` is normally not needed** – the extension finds
   `nanoc-dap` via PATH. Only if it cannot find the adapter, set it in the
   VS Code settings:
   ```json
   "nanoc.dapPath": "C:\\Path\\to\\venv\\Scripts\\nanoc-dap.exe"
   ```
6. A warning such as `(node:...) [DEP0169] ...` during installation is a
   Node.js deprecation warning and harmless as long as the installation
   succeeds.

## 4. In-game: controller and terminal

1. Craft a **NanoC controller** (see the in-game recipe) and place it.
2. Craft a **terminal** (`termlib:terminal1`).
3. Hold the terminal, **left-click the controller**, place the terminal next
   to it, open the terminal and type `@connect`.
4. **Right-click the controller** → **Token** button → copy the token with
   `Ctrl-C`. The token is personal and only valid for this controller; do not
   share it.
5. Optional: give the controller a name with the Techage Info Tool
   (sneak + place).
6. Stay near the controller or forceload the area so it stays loaded.

## 5. VS Code: `launch.json`

Open the unpacked client folder (or your own program folder) in VS Code and
create `.vscode\launch.json`. The `version`/`configurations` wrapper is
required:

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "nanoc",
      "request": "attach",
      "name": "NanoC Tech-Age-Survival",
      "host": "joesworld.ipv64.net",
      "port": 41100,
      "token": "<TOKEN>",
      "tls": true,
      "tlsFingerprint": "01:6A:FA:52:9C:F6:2A:C9:EA:DA:A9:A5:CB:9E:62:DA:3F:3B:BB:15:25:16:89:8B:8C:0E:83:64:F2:DA:10:7A",
      "source": "${file}",
      "program": "${file}",
      "upload": true
    }
  ]
}
```

- Replace `<TOKEN>` with the token from step 4.
- `source` and `program` point to the active file; it must be saved.
- Do not commit the token to a public repository.

## 6. Create the mini program

Create `main.nanoc` in the opened folder:

```c
// NanoC controller demo
int32 count = 0;

while (1) {
    count = count + 1
    printf("NanoC ready, count=%d\n", count)
    sleep(1000)
}
```

Save it. The program counts up once per second and writes the output to the
terminal.

## 7. Start

1. Keep `main.nanoc` active in VS Code.
2. Press **F5**. The file is uploaded, compiled and started.
3. If the VM pauses at entry, press **F5** again (Continue).
4. The connected in-game terminal shows:
   ```text
   NanoC ready, count=1
   NanoC ready, count=2
   ...
   ```
5. Stop with **Shift+F5** (Stop) or via the controller menu.

## 8. Test the connection (optional)

With the token from step 4 you can check the bridge directly:

```bat
nanoc catalog --host joesworld.ipv64.net --port 41100 --tls --tls-fingerprint "01:6A:FA:52:9C:F6:2A:C9:EA:DA:A9:A5:CB:9E:62:DA:3F:3B:BB:15:25:16:89:8B:8C:0E:83:64:F2:DA:10:7A" --token <TOKEN>
```

It returns JSON with the topic catalog; this confirms TLS, token and bridge.

## 9. Troubleshooting

- `connection refused` / `connection reset`: wrong server/port, bridge not
  reachable, or TLS fingerprint mismatch.
- `bad token`: token belongs to another controller or is outdated.
- `NOT_LOADED`: the controller area is not loaded – stay nearby or forceload.
- Certificate/fingerprint: the server has a new certificate; use the new
  fingerprint.
- Extension cannot find the adapter: set `nanoc.dapPath` to
  `...\Scripts\nanoc-dap.exe` (step 3).
- No terminal output: is the terminal connected with `@connect`? Was the
  program uploaded? After the first F5, press F5 again (Continue) if needed.
- `DEP0169` warning during VSIX installation: harmless.
