# Схемы фабрик Endfield

## Куда сохранять

Все JSON файлы схем кладите в эту папку:
```
c:\claud\1c\endfield-bonds-calc\data\layouts\
```

## Как создать схему

1. Открой редактор: https://mokhnatti.github.io/endfield-factory-planner/layout_v2.html
2. Создай схему
3. Нажми "Экспорт" - файл скачается
4. Положи файл в эту папку
5. Добавь запись в `index.json`

## Формат index.json

```json
[
  {
    "name": "Название схемы",
    "file": "имя_файла.json",
    "author": "Автор",
    "description": "Описание"
  }
]
```

## Что должен содержать JSON схемы

```json
{
  "name": "Название",
  "author": "Автор",
  "date": "2026-01-31",
  "facilities": [
    { "type": "hub", "x": 25, "y": 25 },
    { "type": "furnace", "x": 2, "y": 1 }
  ],
  "conveyors": [
    { "x": 1, "y": 1, "dir": "r" }
  ]
}
```

## Типы станков (type)

- `hub` - Хаб 9x9 (обязательный)
- `furnace` - Очистка 3x3
- `grinder` - Перемалывание 3x3
- `shaping` - Формовка 3x3
- `filling` - Наполнение 6x4
- `thickener` - Измельчение 6x4
- `planter` - Посадка 5x5
- `seed_collector` - Семена 5x5
- `pylon` - Пилон 2x2
- `storage` - Хранилище 3x3
- `drill` - Бур 2x2
- `pump` - Насос 2x2

## Направления конвейеров (dir)

- `r` - вправо
- `l` - влево
- `u` - вверх
- `d` - вниз
