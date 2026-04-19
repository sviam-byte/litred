# SOURCING_AND_EVIDENCE

## What Evidence Does
Доказательство в nonfiction не служит украшением, знаком эрудиции или чистой страховкой.
Оно должно давать читателю основание принять claim, ограничить claim
или понять, почему автор считает его допустимым.

## Diagnostic Questions

### Necessity
Нужен ли здесь источник?
Что требует ссылки, а что действительно может быть оставлено без неё?
Не перегружен ли текст ссылками там, где они создают видимость доказательности,
а не реальную?

### Integration
Источник встроен в аргумент или приложен декоративно?
Меняется ли логика текста благодаря источнику,
или он просто дублирует уже сказанное?

### Evidence Quality
Что это: anecdote, primary evidence, secondary synthesis, data, expert interpretation?
Соответствует ли тип evidence силе claim?
Достаточна ли репрезентативность?

### Source Ecology
Это особенно важно для длинного нонфикшна и narrative nonfiction.

На скольких типах источников держится текст?
Не зависит ли он слишком сильно от:
- одного автора или одной работы;
- одной исследовательской школы;
- одного интервьюируемого;
- одного типа источника (например, только academic или только journalistic)?

Thin sourcing across long stretches — когда большой участок текста
держится на очень узкой базе — подрывает доверие даже при правильных ссылках.

Repeated dependence on one witness — особенно для narrative nonfiction.

Primary vs. secondary source — первичные источники сильнее вторичных;
важно понять, работает ли текст с оригиналами или только с пересказами.

### Timeliness and Field Volatility
Источник актуален для поля?
Не является ли поле быстро меняющимся, а источник — слишком старым
для силы сделанного вывода?

Date sensitivity: в одних областях источник десятилетней давности нормален,
в других — устарел.

### Unsupported Claims
Есть ли высказывания, которые требуют evidence, но его не имеют?
Не подаётся ли спорное утверждение как общеизвестный факт?
«Все знают, что...», «Давно установлено, что...», «Очевидно, что...»
без источника — это риск, а не риторика.

### Authority Laundering
Не скрывает ли текст слабость собственного рассуждения
за словами «исследования показывают», «эксперты считают» и т.п.?
Не растянут ли вывод источника дальше его реального scope?
Не используется ли авторитет источника для легитимации утверждения,
которое источник не поддерживает?

### Citation Without Function
Делает ли ссылка работу?
Если убрать её, изменится ли аргумент?

### Contested Field as Settled
Не подаёт ли текст спорную область как решённую?

## Common Failures

**Unsupported claim.**
Утверждение сделано уверенно, без материала.

**Absent attribution.**
Информация дана — откуда непонятно.

**Authority laundering.**
«Исследования показывают...» без указания каких именно.

**Decorative citation.**
Ссылка есть, но она не двигает аргумент.

**Contested field as settled.**

**Source monoculture.**
Весь аргумент опирается на слишком узкий круг источников.

**Thin sourcing under confident narration.**
Нарратив звучит уверенно, но под ним мало реальной фактической базы.

## Output Fields
```json
{
  "sourcing_necessity": "high | medium | low",
  "integration_quality": "embedded | appended | absent",
  "evidence_quality": "strong | mixed | weak",
  "source_ecology": "diverse | narrow | thin",
  "source_monoculture_risk": "low | medium | high",
  "timeliness_risk": "low | medium | high",
  "unsupported_claims": ["..."],
  "authority_laundering_risk": "low | medium | high",
  "contested_as_settled": ["..."],
  "issues": ["..."],
  "severity": "low | medium | high"
}
```
