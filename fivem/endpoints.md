---
title: Ustawianie endpointów
description: Ustawianie endpointów
authors:
  - name: Wiktor Bukowski
    email: kontakt@buko-dev.pl
    avatar: /static/authors/buko.gif
---

# Ustawianie endpointów

Domyślnie endpointy serwera są automatycznie ustawiane na poprawne. Jeśli użyjesz gotowej paczki skryptów z panelu txAdmin, musisz je ustawić samodzielnie.

Przechodzimy do pliku `server.cfg` i ustawiamy dwie linijki:

`endpoint_add_tcp "0.0.0.0:PORT"`

`endpoint_add_udp "0.0.0.0:PORT"`

![Ustawianie endpointów](/static/fivem/endpoints.png)

Zamiast `PORT` wpisujemy port, na którym chcemy, aby nasz serwer działał. Swój port możesz sprawdzić w zakładce `Przegląd` lub `Sieć` w zarządzaniu serwerem.

:::caution
Linijka z ustawieniem endpointów musi znajdować się na samym początku pliku konfiguracyjnego.
:::

![Zakładka Przegląd](/static/fivem/port_console.png)

![Zakładka Sieć](/static/fivem/port_network.png)

Po ustawieniu konfiguracji, należy uruchomić serwer ponownie.

Gotowe! Twój serwer powinien być teraz widoczny w liście serwerów.
