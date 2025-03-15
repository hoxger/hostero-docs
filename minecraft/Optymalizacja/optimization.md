---
title: Optymalizacja
description: Optymalizacja serwerów minecraft.
authors:
  
- name: Lakiś
  avatar: /static/authors/lakis.png
---
## Co jest problemem?
Minecraft Java Edition nie jest najlepiej zoptymalizowaną grą, co oznacza, że serwer może mieć problemy z wydajnością, szczególnie gdy gra na nim dużo osób lub gdy świat gry jest rozbudowany.
Do najczęstszych powodów spadków wydajności należą:
- **Generowanie mapy:** Generowanie nowych fragmentów świata (chunków) jest bardzo zasobożerne. Każdy chunk serwer musi wygenerować osobno, co oznacza bardzo duże zużycie CPU, które jest bardzo ważne w przypadku minecrafta.
- **Entity:** Wszystko, co nie jest blokiem (np. zwierzęta, potwory, ramki na przedmiot), nazywa się entity, jako że nie jest to blok minecraft śledzi jego ruch i położenie ciągle, nawet jeśli jest to entity ozdobny typu ramka na przedmiot.
- **Ilość pluginów:** Zbyt wiele pluginów lub ich nieoptymalne działanie mogą znacząco obciążać serwer, prowadząc do opóźnień i problemów z płynnością gry.

## Jaki silnik wybrać na serwer?
Istnieje wiele silników serwerowych do Minecrafta, które różnią się funkcjonalnością i poziomem optymalizacji. 
### Najpopularniejsze/Najlepsze silniki
1. **[Vanilla:](https://www.minecraft.net/en-us/download)** jest to oficjalny silnik serwera Minecraft, oferowany przez Mojang. Nie obsługuje pluginów ani modów, co sprawia, że jest mało wydajny na duże serwery. Jeśli jednak chcesz grać na serwerze ze znajomymi, ten silnik powinen się sprawdzić.
2. **[Spigot:](https://spigotmc.org/)** Spigot to ulepszona wersja Bukkit, z **lepszą wydajnością i większą stabilnością**. Spigot zmniejsza lagi *(ale nie jakoś bardzo)* i oferuje dodatkowe opcje konfiguracyjne, które pomagają lepiej dostosować serwer do większej liczby graczy.
3. **[Paper:](https://papermc.io/downloads/all)** silnik operaty na bazie następnego silnika o nazwie Spigot (dzięki czemu wszystkie pluginy pisane na silnik spigot działają na innych), który dodatkowo poprawia wydajność i pozwala na jeszcze więcej ustawień optymalizacyjnych. Paper oferuje **bardziej zaawansowane opcje zarządzania zużyciem pamięci i mocy procesora**. Wprowadza m.in. zmiany w obsłudze mobów i innych obiektów, co pozwala na **znaczną redukcję lagów**.
4. **[PurPur:](https://purpurmc.org/download/purpur)** jest to kolejne rozwinięcie silnika, tym razem paper. W PurPur można znaleźć dodatkowe ustawienia, które pozwanają np. na **regulowanie fizyki gry czy zachowania mobów**.
5. **[Folia:](https://papermc.io/software/folia)** to najnowszy silnik serwerowy oparty na paper oraz tunity, który został stworzony **z myślą o bardzo dużych serwerach**. Jest zaprojektowany pod kątem rozgrywki z dużą liczbą graczy oraz **poprawia wydajność na maszynach, które obsługują setki lub nawet tysiące osób jednocześnie**.
6. **[Sponge:](https://www.spongepowered.org/)** to silnik serwerowy stworzony z myślą o rozbudowanej obsłudze pluginów oraz modów. Oferuje **wysoką elastyczność i wsparcie dla różnych typów modyfikacji**, co czyni go idealnym rozwiązaniem dla graczy, którzy chcą wprowadzić bardziej złożone zmiany w swoim świecie.
### Bukkit
Istnieje również silnik **[Bukkit](https://bukkit.org/)**, jednak __nie jest on uwzględniony na tej liście jako rekomendowany wybór__. Bukkit to w zasadzie **podstawa** dla silników takich jak Spigot i Paper, dlatego zapewnia tylko podstawowe funkcje, ale bardzo niewiele opcji optymalizacji. Korzystanie z niego na serwerach publicznych jest możliwe, ale ze względu na **niski poziom optymalizacji** może prowadzić do lagów i problemów z wydajnością, szczególnie przy większej liczbie graczy.
### Podsumowanie
Jeśli nadal nie wiesz, jaki silnik wybrać, **[Paper](https://papermc.io/downloads/all)** będzie najbardziej optymalnym wyborem. Jest łatwy w obsłudze i jednocześnie bardzo skutecznie poprawia wydajność serwera. Ale to nie wszystko, aby jeszcze lepiej zoptymalizować serwer, używamy wiele opcji konfiguracyjnych silników.
