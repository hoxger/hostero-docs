---
title: Otymalizacja silników
description: Optymalizacja silników do serwera.
authors:
  
- name: Lakiś
  avatar: /static/authors/lakis.png
---
## Wprowadzenie
Każdy silnik serwerowy wprowadza swoje pliki konfiguracyjne, takie jak `bukkit.yml`, które można edytować w celu jeszcze większej optymalizacji serwera. Dzięki temu możesz zoptymalizować działanie serwera jeszcze bardziej niż w ustawieniach domyślnych.
## Bukkit.yml
### `spawn-limits:`
Określa maksymalną liczbę mobów danego typu, które mogą pojawić się w danym obszarze.
Zalecana wartość:
```
spawn-limits:
  monsters: 35
  animals: 10
  water-animals: 5
  water-ambient: 10
  water-underground-creature: 3
  axolotls: 5
  ambient: 3
```
### `ticks-per:`
Definiuje częstotliwość, z jaką różne mechaniki serwera są aktualizowane, wyrażoną w tickach.
Zalecana wartość:
```
  animal-spawns: 400
  monster-spawns: 10
  water-spawns: 400
  water-ambient-spawns: 400
  water-underground-creature-spawns: 400
  axolotl-spawns: 400
  ambient-spawns: 400
  autosave: 6000
```
## Spigot.yml
### `save-user-cache-on-stop-only`
Określa, czy dane o graczach (cache użytkowników) powinny być zapisywane tylko podczas zatrzymywania serwera, czy ciągle.
Zalecana wartość:
```
true
```
### `entity-activation-range`
Określa maksymalną odległość, w jakiej moby i inne byty mogą aktywować swoje AI.
Zalecana wartość:
```
true
```
### `merge-radius`
Określa maksymalną odległość, w jakiej byty, takie jak przedmioty czy XP, mogą się łączyć w jedną jednostkę.
Zalecana wartość:
```
item: 4.0
exp:6.0
```
### `nerf-spawner-mobs`
Pozwala na ograniczenie AI mobów generowanych przez spawner.
Zalecana wartość:
```
true
```
### `max-tick-time`
Definiuje maksymalny czas w tickach, który serwer może poświęcić na przetwarzanie jednej jednostki (np. świata, gracza lub bytu).
Zalecana wartość:
```
tile: 1000
entity: 1000
```
### `arrow-despawn-rate`
Określa czas, po którym strzały (strzały z łuku) znikają z gry, jeśli nie trafią w nic.
Zalecana wartość:
```
300
```
### `tick-inactive-villagers`
Kontroluje, czy nieaktywni wieśniacy będą przetwarzani przez serwer.
Zalecana wartość:
```
false
```
## paper-global.yml oraz paper-world-defaults.yml
Obydwa pliki znajdziesz w katalogu  `/config` w plikach serwera.
### `max-auto-save-chunks-per-tick`
Określa maksymalną liczbę chunków, które mogą być automatycznie zapisywane w każdym ticku serwera.
Zalecana wartość:
```
8
```
### `optimize-explosions`
Włącza lub wyłącza optymalizację eksplozji na serwerze.
Zalecana wartość:
```
true
```
### `max-entity-collisions`
Definiuje maksymalną liczbę kolizji, które mogą wystąpić jednocześnie między bytami w grze.
Zalecana wartość:
```
2
```
### `despawn-range`
Określa maksymalną odległość, w jakiej byty (takie jak moby i przedmioty) mogą być aktywne i widoczne dla graczy.
Zalecana wartość:
```
soft: 28
hard: 96
```
### `prevent-moving-into-unloaded-chunks`
Decyduje, czy gracze mogą poruszać się w obszary, które nie zostały załadowane.
Zalecana wartość:
```
true
```
### `armor-stands-tick`
Kontroluje, czy stojaki na zbroję (armor stands) mają być aktualizowane w każdym ticku serwera.
Zalecana wartość:
```
false
```
### `anti-xray`
Włącza wbudowaną funkcję przeciwko x-ray.
Zalecana wartość:
```
true
```
### `grass-spread-tick-rate`
Określa częstotliwość, z jaką trawa rozprzestrzenia się w grze, wyrażoną w tickach.
Zalecana wartość:
```
4
```