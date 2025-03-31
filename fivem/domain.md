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

3.  **Wybieramy rekord A jako typ rekordu DNS.**

     <br>

    ![Wybór rekordu A](/static/fivem/domain-step3.png)

4.  **Uzupełniamy dane dla rekordu A:**

    - W polu **Subdomena** wpisujemy „serwer”
    - W polu **Adres docelowy** wpisujemy adres IP serwera (bez portu)
    - Klikamy **Dalej** i zapisujemy zmiany.

     <br>

    ![Konfiguracja rekordu A](/static/fivem/domain-step4.png)

5.  **Dodajemy kolejny rekord – tym razem wybieramy typ SRV.**

    <br>

    ![Wybór rekordu SRV](/static/fivem/domain-step5.png)

6.  **Konfigurujemy rekord SRV zgodnie z poniższymi wartościami:**

    - W polu **Subdomena** wpisujemy `_cfx._udp`
    - W polu **Port** wpisujemy port serwera FiveM
    - W polu **Adres docelowy** wpisujemy nazwę rekordu A, czyli `serwer.mojserwer.pl`
    - Pola **Priorytet** oraz **Waga** ustawiamy na `10`
    - Klikamy **Dalej** i zapisujemy zmiany.

        <br>

    ![Konfiguracja rekordu SRV](/static/fivem/domain-step6.png)

## Podłączanie domeny (Cloudflare)

Do podłączenia domeny potrzebujesz mieć zarejestrowaną lub dodaną domenę na Cloudflare, co jest zalecaną opcją; jeśli nie masz domeny na Cloudflare, możesz ją dodać klikając przycisk **Add a domain** w głównym panelu.

7.  **Wybieramy naszą domenę w panelu i przechodzimy do zakładki DNS.**  
    ![Wybór DNS w panelu](/static/fivem/domain-cf-1.png)

8.  **Klikamy przycisk „Add record” i najpierw wybieramy rekord A:**

    - W polu **Name** wpisujemy np. „Serwer”
    - W polu **IPv4 address** wpisujemy adres IP serwera (bez portu)
    - Zmieniamy opcję Proxy status na **DNS only**
    - Klikamy **Save**.  
      ![Rekord A](/static/fivem/domain-cf-2.png)

9.  **Ponownie klikamy przycisk „Add record”, wybieramy typ "SRV":**
    - W polu **Name** wpisujemy `_cfx._udp`
    - W polu **Port** wpisujemy **port serwera** z panelu
    - W polu **Target** wpisujemy **nazwę rekordu** A, czyli `serwer.domena.pl`, gdzie `serwer` to nazwa rekordu A.
    - Pola **Priority** oraz **Weight** wpisujemy `10`.  
      ![Rekord SRV](/static/fivem/domain-cf-3.png)

## Finalizacja

Domena powinna działać po aktualizacji DNS, co może zająć od kilku minut do kilku godzin. Po zakończeniu możesz połączyć się z serwerem FiveM za pomocą skonfigurowanej domeny.
