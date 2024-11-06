---
title: Konfiguracja TXAdmin
description: Konfiguracja TXAdmin
authors:
  - name: Wiktor Bukowski
    email: kontakt@buko-dev.pl
    avatar: /static/authors/buko.gif
---
# Konfiguracja TXAdmin

Na początku musimy włączyć TXAdmina w zakładce **Startup**.

![Włączanie TXAdmin](/static/fivem/txadmin-startup.png)

Następnie przechodzimy do zakładki **Console** i uruchamiamy ponownie serwer. Po uruchomieniu serwera, w konsoli powinien pojawić się link wraz z kodem dostępu do panelu TXAdmin.

![Kod dostępu](/static/fivem/txadmin-code.png)

Przechodzimy do strony z panelem TXAdmina i logujemy się za pomocą wcześniej wygenerowanego kodu dostępu.

![Logowanie](/static/fivem/txadmin-codeverify.png)

Autoryzujemy aplikację klikając przycisk **CONTINUE**.

![Autoryzacja](/static/fivem/txadmin-authacc.png)
Opcjonalnie ustawiamy Identyfikator konta Discord oraz ustawiamy hasło zapasowe, akceptujemy regulamin i klikamy przycisk **Register**.

![Autoryzacja](/static/fivem/txadmin-authacc2.png)


W pierwszym punkcie konfiguracji klikamy przycisk **NEXT**.

![Wstęp do konfiguracji](/static/fivem/txadmin-createsrv.png)

W drugim punkcie ustawiamy nazwę swojego serwera i klikamy przycisk **NEXT**.
Nazwa serwera będzie wykorzystywana w txAdmin oraz w powiadomieniach wysyłanych przez txAdmin.

![Nazwa serwera](/static/fivem/txadmin-createsrv2.png)

W trzecim punkcie zalecamy wybrać opcję **Existing Server Data** aby użyć już istniejących danych serwera. W przypadku wyboru opcji **Popular Recipes** będzie możliwość instalacji gotowych paczek serwerowych.

![Existing Server Data](/static/fivem/txadmin-createsrv3.png)

W czwartym punkcie ustawiamy ścieżkę folderu głównego serwera. Domyślnie jest to `/home/container/`.

![Ścieżka folderu](/static/fivem/txadmin-createsrv4.png)

W piątym punkcie ustawiamy ścieżkę pliku `server.cfg`. Domyślnie jest to `/home/container/server.cfg`.

![Ścieżka pliku](/static/fivem/txadmin-createsrv5.png)

Gotowe! TXAdmin został skonfigurowany i jest gotowy do użycia. Naciśnij przycisk **Save & Start Server** aby uruchomić serwer.

![Uruchamianie serwera](/static/fivem/txadmin-createsrv6.png)

Po uruchomieniu serwera, powinien wyświetlić się panel zarządzania TXAdmin.