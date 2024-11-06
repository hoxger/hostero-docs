---
title: Podłączanie domeny
description: Jak podłączyć domenę na serwer minecraft.
authors:
  
- name: Lakiś
  avatar: /static/authors/lakis.png
---
## Podłączanie domeny (Cloudflare)
Do podłączenia domeny potrzebujesz mieć zarejestrowaną lub dodaną domenę na Cloudflare, co jest zalecaną opcją; jeśli nie masz domeny na Cloudflare, możesz ją dodać klikając przycisk __Add a domian__ w głównym panelu.

1. Wybieramy naszą domenę w panelu i __przechodzimy do zakładki DNS__.
![Wybór DNS w panelu](\static\minecraft\domena-1.png)
2. Klikamy przycisk __Add record__ i najpierw wybieramy rekord A, w polu Name wpisujemy np. "Serwer" a w polu __IPv4 address__ wpisujemy adres IP serwera (Bez portu). Zmieniamy opcję Proxy status na __DNS only__ i klikamy Save.
![Rekord A](\static\minecraft\domena-2.png)
3. Ponownie klikamy przycisk __Add record__, wybieramy typ "SRV"
- W polu Name wpisujemy `minecraft_.tcp`
- W polu Port wpisujemy __port serwera__ z panelu
- W polu Target wpisujemy __nazwe rekordu__ A czyli `serwer.domena.pl` gdzie `serwer` jest nazwą rekordu A.
- Pola Priority oraz Weight wpisujemy `10`
![Rekord A](\static\minecraft\domena-3.png)
Wszystko gotowe! Domena powinna działać po aktualizacji DNS.