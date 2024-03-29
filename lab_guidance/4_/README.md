# Пояснення до виконання роботи 4
## Тема: _Алгоритми пошуку найкоротших шляхів_
## Мета роботи: _Навчитись застосовувати алгоритми пошуку найкоротших шляхів та застосовувати їх в телекомунікаційних мережах._

# Пояснення до роботи
> дані алгоритми застосовуються лише до зважених графів (ребра мають вагу)

## Алгоритм Беллмана-Форда
- використовуємо принцип хвилі так само як і у пошуку в ширину;
- хвиля доходячи до вершини залишає у вузлі мітку відстані яка сумується із всіх пройдених хвилею ребер;
- якщо у вузлі вже присутня мітка і туди приходить хвиля тоді мітки порівнюються, і в кого мітка більше та хвиля блокується і більше не поширюється; 
---

## Алгоритм Дейкстри
- використовуємо принцип - завжди вибираємо мінімальне ребро;
- на кожному кроці додається нова вершина яка зєднується ребром з мінімальною вагою;
- вершини до яких вже знайдено шлях більше не беруть участі у пошуку і шляхи до них більше не розглядаються;

![alt text](https://github.com/BobasB/lab_example/blob/master/lab_guidance/4_/dejkstra.gif "Приклад алгоритму Дейкстри")

---

## Пропускна здатність шляху
- шлях складається з ребер, і ребро з мінімальною вагою і буде визначати пропускну здатність шляху;
```text
Шлях: 1 -> 2 -> 3 -> 4
Ребра: a:(1,2) b:(2,3) c:(3,4)
Вага ребер: а = 15, b = 10, c = 12
Пропускна здатність: 10 (тому що це ребро з мінімальним ваговим коефіцієнтом)
```

## Хід роботи
У роботі використовується онлайн ресурс для генерування графів [Graph Online](https://graphonline.ru/).
1. За допомогою лабораторного макету побудувати випадковий неорієнтований зважений граф з `V=6` та `E=10` та побудувати дерево шляхів з вершини `N` за алгоритмом Дейкстри;

1. Для того ж графа побудувати дерево шляхів з вершини `N` за алгоритмом Беллмана-Форда;

1. Вказати який з алгоритмів виконується швидше:
    1. порівняти за кількістю кроків для знаходження найкоротшого шляху;
    1. порівняти за кількістю відвіданих вершин на кожному кроці;

1. Чи знайдені маршрути за алгоритмом Дейкстри та Беллмана-Форда однакові?
    1. Якщо ні, вказати які та чому;
    1. Чи існують маршрути з однаковою метрикою? Які?

1. Вважаючи, що коефіцієнти ребер вказують на пропускну здатність в Мбіт/с, знайти пропускну здатність кожного шляху визначеного за алгоритмом Дейкстри та Беллмана-Форда.
	1. Які шляхи мають максимальну пропускну здатність, чому?
	1. Чи є шляхи які на якомусь відрізку мережі використовують менше половини пропускної здатності ребра?
	1. Чи можливе одночасне існування потоків із вершини `N` до всіх інших із розрахованою пропускною здатністю кожного шляху? Чому?

## Здача роботи
1. Оформити звіт лабораторної роботи. Звіт повинен бути у файлі `README.md` та завантажений у репозиторій GitHub.
1. URL посилання на виконану роботу вставити у відповідне завдання у Google Classroom.

---
