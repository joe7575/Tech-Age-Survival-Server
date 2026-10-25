Fingerprint: 01:6A:FA:52:9C:F6:2A:C9:EA:DA:A9:A5:CB:9E:62:DA:3F:3B:BB:15:25:16:89:8B:8C:0E:83:64:F2:DA:10:7A

Lesen Terminal für 3s: 

```
nanoc read --host joesworld.ipv64.net --port 41100 --tls --tls-fingerprint "01:6A:FA:52:9C:F6:2A:C9:EA:DA:A9:A5:CB:9E:62:DA:3F:3B:BB:15:25:16:89:8B:8C:0E:83:64:F2:DA:10:7A" --token <TOKEN> --seconds 3
```

Test, ob Controller errreichbar:

```
nanoc catalog --host joesworld.ipv64.net --port 41100 --tls --tls-fingerprint "01:6A:FA:52:9C:F6:2A:C9:EA:DA:A9:A5:CB:9E:62:DA:3F:3B:BB:15:25:16:89:8B:8C:0E:83:64:F2:DA:10:7A" --token <TOKEN>
```


VS Code ".vscode\launch.json:

```
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "nanoc",
      "request": "attach",
      "name": "NanoC...",
      "host": "joesworld.ipv64.net",
      "port": 41100,
      "token": "<TOKEN>",
      "tls": true,
      "tlsFingerprint": "01:6A:FA:52:9C:F6:2A:C9:EA:DA:A9:A5:CB:9E:62:DA:3F:3B:BB:15:25:16:89:8B:8C:0E:83:64:F2:DA:10:7A",
      "source": "${file}",
      "program": "${file}",
      "upload": false
    }
  ]
}
```
