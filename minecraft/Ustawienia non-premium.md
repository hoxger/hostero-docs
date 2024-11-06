---
title: Ustawienia non-premium
description: Jak odblokować online-mode na serwerze do gry dla osób z non-premium.
authors:
  
- name: Lakiś
  avatar: /static/authors/lakis.png
---
## Odblokowywanie non-premium
Aby umożliwić graczom non-premium dołączenie do serwera, należy zmienić ustawienia w pliku `server.properties`. Oto kroki, które należy wykonać:
1. W zakładce "Pliki" na panelu klienta poszukaj pliku `server.properties`
2. Otwórz plik i wyszukaj linię `online-mode=true`
![Online-Mode](\static\minecraft\online-mode.png)
3. Zmień tę linię na `online-mode=false`

Następnie zrestartuj serwer. Po uruchomieniu gracze non-premium powinni mieć możliwość dołączenia do twojego serwera.
