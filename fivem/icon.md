---
title: Zmiana ikony serwera
description: Zmiana ikony serwera
authors:
  - name: Wiktor Bukowski
    email: kontakt@buko-dev.pl
    avatar: /static/authors/buko.gif
---

# Zmiana ikony serwera

## Przygotowanie ikony

Ikona serwera musi spełniać dwa podstawowe wymagania aby została poprawnie wyświetlona w liście serwerów:

- Mieć rozmiar 96x96 piksele
- Być w formacie PNG

## Wgranie ikony

Przechodzimy do zakładki **Pliki** na panelu klienta serwera. Klikamy przycisk **Wgraj plik** i wybieramy ikonę serwera.
Tą czynność możemy wykonać również poprzez SFTP.

![Wgrywanie ikony](/static/fivem/fivemicon.png)

:::caution
Pamiętaj, aby ikona znajdowała się w głównym katalogu serwera.
:::

## Ustawienie ikony

W pliku `server.cfg` należy dodać linijkę `load_server_icon nazwa_pliku`.
Plik konfiguracyjny możemy edytować przez SFTP lub przez panel klienta serwera.
Po ustawieniu konfiguracji, należy uruchomić serwer ponownie.

Gotowe! Ikona serwera powinna być teraz widoczna w liście serwerów.
