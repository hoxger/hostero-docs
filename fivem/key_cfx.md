---
title: Generowanie klucza licencyjnego
description: Generowanie klucza licencyjnego
authors:
  - name: Wiktor Bukowski
    email: kontakt@buko-dev.pl
    avatar: /static/authors/buko.gif
---

# Generowanie klucza licencyjnego

W pierwszej kolejności należy wejść na stronę [keymaster.fivem.net](https://keymaster.fivem.net/) i zalogować się za pomocą konta FiveM.

![Logowanie](/static/fivem/keymaster-login.png)

Po zalogowaniu się, należy kliknąć przycisk **New server**.

![Nowy serwer](/static/fivem/keymaster-new.png)

Uzupełniamy wszystkie pola w poniższy sposób:

- **Display name** - Nazwa serwera wyświetlana w systemie KeyMaster - Nie jest to nazwa serwera widoczna dla graczy

Następnie zaznaczamy pole **Captcha** i klikamy przycisk **Generate**.

![Generowanie](/static/fivem/keymaster-data.png)

Po wygenerowaniu klucza, należy go skopiować i ustawić go w zakładce **Parametry startowe** oraz wkleić do pliku `server.cfg` w linijce `sv_licenseKey`.

![Kopiowanie](/static/fivem/keymaster-copy.png)
![Ustawianie w zakładce Parametry startowe](/static/fivem/keymaster-paste.png)
![Wklejanie do server.cfg](/static/fivem/keymaster-paste1.png)
