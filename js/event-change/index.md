---
title: "change"
description: "Работаем со значением, когда пользователь зафиксирует свои изменения"
authors:
  - kejjero
related:
  - js/events
  - html/form
  - js/deal-with-forms
tags:
  - doka
  - placeholder
---

## Кратко

Событие `change` срабатывает, когда пользователь изменяет значение в `<input>`, `<select>` или `<textarea>` и фиксирует свои изменения.

Это событие лучше всего использовать при создании форм, когда не требуется постоянно взаимодействовать с каждым изменённым символом в поле ввода. Так же данное событие пригодится и при создании чекбоксов, полей выбора и т. п.

## Как пишется

```js
const input = document.querySelector('.input')

input.addEventListener('change', function (event) {
  console.log(event.target.value)
})
```

## Пример

💡 В зависимости от указанного типа в HTML элементе, `change` срабатывает по-разному. Лучше всего это становится понятным на примерах.

<iframe title="Демонстрация работы — change() — Дока" src="demos/index"></iframe>

## Как понять

Подробнее о механизме событий читай в статье «[Событийная модель](/js/events)».

Событие change похоже на события `input` и `blur`, но есть важные отличия:

`blur` – срабатывает каждый раз при расфокусировке поля.
`input` – срабатывает сразу же при изменении значения поля.
`change` – срабатывает когда значение поля изменено, но при условии снятия с него фокуса.

<iframe title="Демонстрация в чем различие между событиями blur, input и change? — Дока" src="demos/compare"></iframe>