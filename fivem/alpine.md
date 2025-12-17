---
title: Aktualizacja Artefaktów FiveM
description: Jak pobrać i zaktualizować artefakty FiveM.
authors:
  - name: Wiktor Bukowski
    email: kontakt@buko-dev.pl
    avatar: /static/authors/buko.gif
---

# Aktualizacja Artefaktów FiveM

#### Najnowsza wersja artefaktu
<div id="latest-artifact" class="artifact-box">Ładowanie...</div>

<script>
async function fetchLatestArtifact() {
    try {
        const response = await fetch("https://changelogs-live.fivem.net/api/changelog/versions/linux/server");
        if (!response.ok) throw new Error("Network response was not ok");
        const data = await response.json();
        
        const latestDownload = data.latest_download;
        const match = latestDownload.match(/master\/(\d+-[a-f0-9]+)\/fx\.tar\.xz/);
        
        if (match) {
            document.getElementById("latest-artifact").innerText = match[1];
        } else {
            document.getElementById("latest-artifact").innerText = "Nie znaleziono wersji";
        }
    } catch (error) {
        document.getElementById("latest-artifact").innerText = "Błąd pobierania wersji";
        console.error("Błąd pobierania najnowszej wersji artefaktu:", error);
    }
}
fetchLatestArtifact();
</script>

<br>
<hr>

#### Aby zmienić artefakty FiveM, przejdź na stronę: [Runtime FiveM Artifacts](https://runtime.fivem.net/artifacts/fivem/build_proot_linux/master/)
Na stronie znajdziesz listę dostępnych wersji. Kliknij w najnowszy link i skopiuj jego adres URL.

**Przykład:**

```
https://runtime.fivem.net/artifacts/fivem/build_proot_linux/master/13383-4e9aa42c700f88735a2b9c2f51738568daf597e4/fx.tar.xz
```

### Wklej link do pola poniżej

Wklej skopiowany link, aby automatycznie uzyskać wersję artefaktu:

<input id="artifact-input" type="text" class="artifact-input" placeholder="Wklej link tutaj" oninput="extractVersion()" />

**Wersja:**
<div id="artifact-version" class="artifact-box">Powyżej wklej link do pobrania artefaktów</div>

<script>
function extractVersion() {
    const input = document.getElementById("artifact-input").value;
    const match = input.match(/master\/(\d+-[a-f0-9]+)\//);
    const version = match ? match[1] : "Niepoprawny link";
    document.getElementById("artifact-version").innerText = version;
}
</script>

<style>
:root {
    --background-color: #ffffff;
    --text-color: #333333;
    --border-color: #cccccc;
    --card-background: #f3f3f3;
}

@media (prefers-color-scheme: dark) {
    :root {
        --background-color: #1e1e1e;
        --text-color: #ffffff;
        --border-color: #555555;
        --card-background: #2c2c2c;
    }
}

.artifact-box {
    font-family: monospace;
    font-weight: bold;
    font-size: 1rem;
    padding: 15px;
    background: var(--card-background);
    color: var(--text-color);
    border-radius: 8px;
    border: 1px solid var(--border-color);
    word-break: break-all;
    margin-top: 10px;
    line-height: 1.5;
}

.artifact-input {
    width: 100%;
    padding: 12px;
    margin: 10px 0;
    border: 1px solid var(--border-color);
    background: var(--background-color);
    color: var(--text-color);
    border-radius: 8px;
    box-sizing: border-box;
    font-size: 1rem;
}
</style>
</br>

### Wprowadzenie wersji artefaktu w ustawieniach

Przejdź do zakładki **Parametry startowe** i wprowadź wygenerowaną wersję w polu **Wersja artefaktu FiveM**.

![Wersja artefaktu](/static/fivem/artifacts.png)

Po ustawieniu nowej wersji usuń folder `alpine` i wykonaj **Reinstall serwera**.

![Reinstall serwera](/static/fivem/reinstall.png)

Gotowe! Twój serwer FiveM został zaktualizowany do najnowszej wersji artefaktów.