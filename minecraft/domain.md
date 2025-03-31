---
title: Podłączanie domeny
description: Jak podłączyć domenę na serwer Minecraft.
authors:
  - name: Buko
    email: kontakt@buko-dev.pl
    avatar: /static/authors/buko.gif
  - name: Lakiś
    avatar: /static/authors/lakis.png
---

## Podłączanie domeny (OVH)

Do podłączenia domeny potrzebujesz mieć zarejestrowaną lub dodaną domenę na OVH. Jeśli nie masz domeny na OVH, możesz ją dodać w panelu zarządzania OVH.

1. **Wybieramy naszą domenę w panelu OVH i przechodzimy do zakładki DNS.**  
   ![Wybór DNS w panelu](/static/minecraft/domain-step1.png)

2. **Klikamy przycisk „Dodaj rekord” w sekcji zarządzania strefą DNS.**  
   ![Dodawanie rekordu](/static/minecraft/domain-step2.png)

3. **Wybieramy rekord A jako typ rekordu DNS.**  
   ![Wybór rekordu A](/static/minecraft/domain-step3.png)

4. **Uzupełniamy dane dla rekordu A:**

   - W polu **Subdomena** wpisujemy „serwer”
   - W polu **Adres docelowy** wpisujemy adres IP serwera (bez portu)
   - Klikamy **Dalej** i zapisujemy zmiany.  
     ![Konfiguracja rekordu A](/static/minecraft/domain-step4.png)

5. **Dodajemy kolejny rekord – tym razem wybieramy typ SRV.**  
   ![Wybór rekordu SRV](/static/minecraft/domain-step5.png)

6. **Konfigurujemy rekord SRV zgodnie z poniższymi wartościami:**
   - W polu **Subdomena** wpisujemy `_minecraft._tcp`
   - W polu **Port** wpisujemy port serwera Minecraft
   - W polu **Adres docelowy** wpisujemy nazwę rekordu A, czyli `serwer.mojserwer.pl`
   - Pola **Priorytet** oraz **Waga** ustawiamy na `10`
   - Klikamy **Dalej** i zapisujemy zmiany.  
     ![Konfiguracja rekordu SRV](/static/minecraft/domain-step6.png)

## Podłączanie domeny (Cloudflare)

Do podłączenia domeny potrzebujesz mieć zarejestrowaną lub dodaną domenę na Cloudflare, co jest zalecaną opcją; jeśli nie masz domeny na Cloudflare, możesz ją dodać klikając przycisk **Add a domain** w głównym panelu.

1. **Wybieramy naszą domenę w panelu i przechodzimy do zakładki DNS.**  
   ![Wybór DNS w panelu](/static/minecraft/domena-1.png)

2. **Klikamy przycisk „Add record” i najpierw wybieramy rekord A:**

   - W polu **Name** wpisujemy np. „Serwer”
   - W polu **IPv4 address** wpisujemy adres IP serwera (bez portu)
   - Zmieniamy opcję Proxy status na **DNS only**
   - Klikamy **Save**.  
     ![Rekord A](/static/minecraft/domena-2.png)

3. **Ponownie klikamy przycisk „Add record”, wybieramy typ "SRV":**
   - W polu **Name** wpisujemy `_minecraft._tcp`
   - W polu **Port** wpisujemy **port serwera** z panelu
   - W polu **Target** wpisujemy **nazwę rekordu** A, czyli `serwer.domena.pl`, gdzie `serwer` to nazwa rekordu A.
   - Pola **Priority** oraz **Weight** wpisujemy `10`.  
     ![Rekord SRV](/static/minecraft/domena-3.png)

Wszystko gotowe! Domena powinna działać po aktualizacji DNS.
