# Карта ассетов: что откуда брать

Главная задача этой таблицы — не генерировать один и тот же объект дважды с разным дизайном.

## Object Sheet 01 — убежище
Источник дизайна для:
- control terminal;
- fuse box;
- emergency lever;
- gauge panel;
- valve;
- fan;
- pipe junction;
- small generator;
- industrial battery;
- intercom;
- locker;
- hydraulic mechanism.

Использовать эти модели внутри:
- modular bunker corridor;
- machinery room;
- blast-door chamber.

Environment prompts задают архитектуру и композицию, но НЕ должны заново придумывать эти props.

## Object Sheet 02 — пустошь / заправка
Источник дизайна для:
- fuel pump;
- roadside sign;
- car battery;
- fuel can;
- barrel;
- tire;
- car door;
- engine block;
- toolbox;
- vending machine;
- road barrier;
- highway sign;
- scrap pile;
- water container.

Использовать внутри:
- gas station;
- garage;
- highway;
- arena dressing.

## Object Sheet 03 — интерактив
Источник дизайна для:
- removable battery;
- electrical fuse / ignition component;
- fuel canister;
- gameplay generator;
- voltage meter;
- power cable;
- breaker;
- hand crank;
- radio;
- antenna control box;
- flashlight;
- melee weapon.

Эти модели должны иметь отдельные части/пивоты там, где требуется взаимодействие.

## Environment prompts — что они создают
01 — модульная архитектура коридоров.
02 — machinery-room architecture.
03 — hero blast-door chamber + сама большая дверь.
04 — внешний вход в убежище.
05 — terrain kit.
06 — rocks/cliffs.
07 — модульная дорога.
08 — архитектура заправки.
09 — архитектура/оборудование гаража вокруг уже определённых props.
10 — escape vehicle.
11 — дальние landmarks.
12 — горизонт.
13 — крупный arena dressing.
14 — decals/material variation.

## Правило конфликта
Если объект уже существует на object sheet — его дизайн берётся с object sheet.
Если речь о здании, крупной конструкции, terrain или distant background — брать environment prompt.
