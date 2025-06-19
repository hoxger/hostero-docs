---
title: Tworzenie bazy danych i logowanie do phpMyAdmin
description: Jak stworzyć bazę danych oraz zalogować się do phpMyAdmin
authors:
  - name: Wiktor Bukowski
    email: kontakt@buko-dev.pl
    avatar: /static/authors/buko.gif
---

# Jak stworzyć bazę danych i zalogować się do phpMyAdmin

## 1. Tworzenie bazy danych

Aby stworzyć nową bazę danych, przejdź do zakładki **Bazy danych** w panelu klienta.

Jeśli nie została jeszcze utworzona żadna baza, zobaczysz przycisk **Nowa baza danych**.

![Nowa baza danych](/static/panel/create_db.png)

### Krok 1: Wybór silnika i nazwy bazy danych

- Wybierz silnik bazy danych: **MariaDB (domyślny)** lub **MySQL**
- Wpisz nazwę bazy danych
- **Pozostaw pole „Dozwolone połączenia z adresu IP” puste**, aby zezwolić na połączenia z dowolnego adresu IP
- **Nazwa bazy danych może składać się z liter, cyfr, myślników, kropek i podkreśleń.**

![Formularz tworzenia](/static/panel/db_create_form.png)

Kliknij **Stwórz**, aby utworzyć bazę danych.

### Krok 2: Podgląd utworzonej bazy danych

Po utworzeniu baza danych pojawi się na liście z informacjami:

- Nazwa bazy
- Adres IP i port
- Użytkownik
- Przycisk do **phpMyAdmin**
- Przycisk **Szczegóły**

![Lista baz danych](/static/panel/db_list.png)

## 2. Szczegóły połączenia

Klikając **Szczegóły**, uzyskasz dostęp do:

- **Adres IP** z portem (np. `37.221.94.187:3306`)
- **Użytkownika**
- **Hasła**
- **Dozwolonych połączeń z IP** (jeśli **%** — dostęp z każdego IP)
- **Ciągu JDBC** – używany np. w botach Discord
- **Ciągu do `cfg`** – używany np. przy serwerze FiveM

![Szczegóły bazy](/static/panel/db_details.png)

## 3. Logowanie do phpMyAdmin

Aby zalogować się do phpMyAdmin, przejdź na stronę:

👉 **[https://phpmyadmin.hostero.pl](https://phpmyadmin.hostero.pl)**

### Dane logowania:

- **Username** – z pola „Użytkownik”
- **Password** – z pola „Hasło”
- **Server choice** – wybierz odpowiedni serwer:

  - Jeśli utworzono bazę **na MySQL**, wybierz **Additional MySQL**
  - Jeśli baza powstała na domyślnym silniku (MariaDB), wybierz **swój node** (np. N01, N02 itd.)

![Logowanie phpMyAdmin](/static/panel/phpmyadmin_login.png)
![Wybór serwera](/static/panel/phpmyadmin_server.png)

---

## 🛑 Uwaga: Nieprawidłowy serwer – błąd logowania

Jeśli podczas logowania zobaczysz poniższy błąd:

> `Access denied for user ... (using password: YES)`

Upewnij się, że dane logowania są poprawne oraz że został wybrany **właściwy serwer** z listy.

![Błąd logowania](/static/panel/phpmyadmin_wrong_server.png)

✅ Upewnij się, że:
- jeśli baza była tworzona jako **MySQL**, wybierasz **Additional MySQL**
- jeśli baza była tworzona jako **MariaDB**, wybierasz swój odpowiedni node (np. N01)
- wpisano poprawną nazwę użytkownika oraz poprawne hasło

---

Po poprawnym zalogowaniu uzyskasz dostęp do swojej bazy danych i możesz nią zarządzać przez interfejs phpMyAdmin.
