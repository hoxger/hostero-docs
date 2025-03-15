---
title: Podłączanie domeny
description: Jak podłączyć domenę na serwer FiveM w OVH.
authors:
  
- name: Buko
  email: kontakt@buko-dev.pl
  avatar: /static/authors/buko.gif
---
## Podłączanie domeny (OVH)
Do podłączenia domeny potrzebujesz mieć zarejestrowaną lub dodaną domenę na OVH. Jeśli nie masz domeny na OVH, możesz ją dodać w panelu zarządzania OVH.

1. **Wybieramy naszą domenę w panelu OVH i przechodzimy do zakładki DNS.**

    <br>

    ![Wybór DNS w panelu](/static/fivem/domain-step1.png)

2. **Klikamy przycisk „Dodaj rekord” w sekcji zarządzania strefą DNS.**
  
    <br>

  ![Dodawanie rekordu](/static/fivem/domain-step2.png)

3. **Wybieramy rekord A jako typ rekordu DNS.**
 
    <br>

   ![Wybór rekordu A](/static/fivem/domain-step3.png)

4. **Uzupełniamy dane dla rekordu A:**
   - W polu __Subdomena__ wpisujemy „serwer”
   - W polu __Adres docelowy__ wpisujemy adres IP serwera (bez portu)
   - Klikamy __Dalej__ i zapisujemy zmiany.
 
    <br>

   ![Konfiguracja rekordu A](/static/fivem/domain-step4.png)

5. **Dodajemy kolejny rekord – tym razem wybieramy typ SRV.**

    <br>

    ![Wybór rekordu SRV](/static/fivem/domain-step5.png)

6. **Konfigurujemy rekord SRV zgodnie z poniższymi wartościami:**
   - W polu __Subdomena__ wpisujemy `_cfx._udp`
   - W polu __Port__ wpisujemy port serwera FiveM
   - W polu __Adres docelowy__ wpisujemy nazwę rekordu A, czyli `serwer.mojserwer.pl`
   - Pola __Priorytet__ oraz __Waga__ ustawiamy na `10`
   - Klikamy __Dalej__ i zapisujemy zmiany.

    <br>

   ![Konfiguracja rekordu SRV](/static/fivem/domain-step6.png)

## Finalizacja
Domena powinna działać po aktualizacji DNS, co może zająć od kilku minut do kilku godzin. Po zakończeniu możesz połączyć się z serwerem FiveM za pomocą skonfigurowanej domeny.
