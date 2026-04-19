# MACRO_ARCHITECTURE

## What Macro Architecture Is
Макроархитектура — это не просто порядок частей,
а маршрут текста как целого: что он обещает, как распределяет вес,
где усиливается, где поворачивает, как распоряжается серединой и финалом.

Это genre-sensitive слой: то, что работает в романе,
отличается от того, что работает в аргументативном эссе.

## Primary Questions
- Есть ли у текста реальная траектория?
- Соответствует ли распределение веса функциям частей?
- Не теряет ли текст свои обещания?

## Diagnostic Questions

### Trajectory
Можно ли описать маршрут текста в нескольких шагах?
Ведёт ли он куда-то кроме самой темы?
Есть ли ощущение movement и необходимости у каждого крупного перехода?

### Weight Distribution
Не front-heavy ли текст (слишком много до того, как началось главное)?
Не back-heavy ли финал?
Не раздуто ли второстепенное?
Не скомкано ли главное?

### Chapter / Section Function
Каждая глава или раздел что-то делает в структуре целого?
Есть ли у каждого чёткий мандат — что он добавляет к тому, что было до?
Что сломается, если убрать эту главу?

### Promise / Payoff Map
Какие элементы маркированы как значимые?
Какие из них получают выплату?
Не появляются ли важные элементы без подготовки?

Важно: payoff не обязан быть «большой сценой» или «ответом на всё».
Открытый финал — честный вариант, если он соответствует жанру и обещанию текста.

### Repetition Patterns
Есть ли повторяющиеся архитектурные жесты?
Это осознанный pattern или mechanical template?
Не повторяет ли текст один и тот же драматургический или аргументативный ход?

### Middle Sag
Есть ли участки длительности без усложнения, нарастания или перестройки?
Ставки стоят на месте, пока события продолжаются?

### Beginning Strategy
Чем именно работает начало:
- сценой;
- рамкой;
- парадоксом;
- фактическим hook;
- exposition;
- смешанным подходом?
Оправдан ли выбор задачей текста?

### Ending Strategy и Ending Types
Чем именно работает финал?

Типы финалов:
- **payoff** — выплата главного обещания;
- **reflective** — момент осмысления без полного закрытия;
- **open** — честный незакрытый конец, если материал требует этого;
- **declarative** — итоговое утверждение;
- **abrupt** — резкое завершение как художественный приём.

Не объясняет ли финал то, что текст должен был уже сделать сам?
Не скомкан ли финал — важнейшая часть получила меньше места, чем требует?

## Common Failures

**No trajectory.**
Текст тематически связен, но не ведёт никуда.

**Bloated opening.**
Слишком много до того, как началось главное.

**Collapsed ending.**
Финал скомкан относительно объёма, который получили второстепенные части.

**Dead middle.**
Средняя часть без нарастания, без перестройки.

**Lost promises.**
Элемент введён, маркирован как значимый — и исчез без выплаты.

**Mechanical chapter pattern.**
Каждая глава устроена одинаково — это не структура, это шаблон.

**Declarative ending for narrative text.**
Финал объясняет то, что нарратив должен был сделать сам.

## Scope Notes

Для fiction ключевые оси: escalation, arc structure, chapter functions, ending preparation.
Для nonfiction ключевые оси: thesis route, argument progression, evidence placement.
Для hybrid: mode balance across macro structure.

## Output Fields
```json
{
  "macro_trajectory": "clear | implied | absent",
  "weight_distribution": "balanced | front_heavy | back_heavy | uneven",
  "promise_payoff_gaps": ["..."],
  "chapter_section_function": "clear | partial | unclear",
  "middle_sag_risk": false,
  "repetition_pattern": "conscious | mechanical | none",
  "beginning_strategy": "scene | frame | paradox | fact_hook | exposition | mixed",
  "ending_strategy": "payoff | reflective | open | declarative | abrupt",
  "ending_prepared": true,
  "issues": ["..."],
  "severity": "low | medium | high"
}
```
