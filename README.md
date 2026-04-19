# Editor Agent — Literary Text Diagnostics v6

## Что это

Полноценная библиотека для редакторского анализа текста как многоуровневой диагностики.

Цель: не генерировать советы, а диагностировать текст по уровням — и отличать
реальные дефекты от осознанных приёмов, жанровых норм, ограничений корпуса и вкусовых предпочтений.

---

## Главное изменение v6 относительно v5

### Добавлен полноценный core/shared-слой
В v5 craft-docs были сильными, но не было системного конституционного слоя.
В v6 добавлены:

- `EVIDENCE_POLICY.md` — когда модуль вправе делать вывод и как сильным
- `PRIORITIZATION.md` (расширен) — порядок правки с добавлением contract/mode fit
- `FALSE_POSITIVE_GUARD.md` (расширен) — защита от гипердиагностики
- `EPISTEMIC_STATUS.md` — разметка статуса утверждений (fact/model/interpretation/etc.)
- `STRENGTHS.md` — обязательный модуль, leverage points, fragile strengths
- `TERMINOLOGY.md` — единый словарь craft terms + system terms
- `NONFICTION_PERSONA.md` — авторитет, situatedness, tone as argument, reader relation
- `TRUTH_CONTRACT.md` — типы правды в нонфикшне, explicitness spectrum
- `SUMMARY_QUOTE_RESPONSE.md` — strawman, steelman, quote function, framing signals

### Расширены тощие жанровые docs
Все заглушки v4/v5 доведены до полноценных операциональных текстов:

- `ESSAY.md` — без догмы про essayistic turn как обязательный критерий
- `MEMOIR.md` — без гиперподозрительности к реконструкции
- `NARRATIVE_NONFICTION.md` — без «должен начинаться со сцены»
- `SCENE.md` — без бинарности «нет изменения = псевдосцена»
- `POV.md` — с psychic distance, time layer, free indirect
- `DIALOGUE.md` — без числовой нормы про beats
- `PLOT_AND_ARCS.md` — с scope/exceptions для anti-plot и episodic prose
- `THESIS_AND_ARGUMENT.md` — с falsifiability и burden of proof
- `SOURCING_AND_EVIDENCE.md` — с source ecology
- `EXPLANATION.md` — с scalar jumps и teleology
- `CHARACTER_AND_RELATIONS.md` — с ensemble и triads
- `DETAIL_AND_EMBODIMENT.md` — с viewpoint-filtered detail и motif recurrence
- `SUBTEXT_AND_MICROTENSION.md` — с non-dialogue subtext и reader-character asymmetry

### Разделён PROPULSION_AND_MACRO на два документа
- `PROPULSION.md` — shared-layer для всех текстов
- `MACRO_ARCHITECTURE.md` — genre-sensitive, с ending types и chapter function

### Смягчён тон по всем docs
Общий дефект v5: docs слишком часто писали как законы жанра.
В v6 во все docs добавлены:
- `Scope and Exceptions` — где документ может переусердствовать
- `false_positive_risks` — в output fields
- Явное разведение: правило / сильная эвристика / риск

---

## Структура

```
Literary-Text-Diagnostics/
  Skill.md                          ← главный merged skill (v5, без изменений)
  resources/
    [44 документа — полный список ниже]

core/
  CORE_SYSTEM.md                    ← роль, hard rules, conflict resolution
  OUTPUT_CONTRACT.md                ← порядок разделов отчёта
  DATA_CONTRACTS.md                 ← объекты finding/caution/strength/etc.
  EVIDENCE_POLICY.md                ← NEW: когда вывод правомерен
  FALSE_POSITIVE_GUARD.md           ← расширен
  PRIORITIZATION.md                 ← расширен: 8 уровней + contract fit
  GENERAL_VERDICT.md                ← обязательный 2-й раздел
  GENRE_ROUTER.md                   ← маршрутизация по типу текста
  ORCHESTRATOR.md                   ← пайплайн запуска модулей
  EXECUTION_GRAPH.md                ← граф выполнения
  MODULE_CONTEXT_POLICY.md          ← что каждый модуль получает
  CONFLICT_PLAYBOOK.md              ← разрешение конфликтов между модулями
  OUTPUT_MODES.md                   ← full / short / debug / API
  QUALITY_GATES.md                  ← gate-проверки перед финальным отчётом
  REPORT_STYLE_GUIDE.md             ← тон и стиль вывода

skills/                             ← legacy skill specs (v5)
schemas/                            ← JSON schemas (v5)
prompt_wrappers/                    ← prompt wrappers (v5)
```

---

## Полный список resources/ (44 файла)

### Core layer (в resources для быстрого доступа)
- `CORE_SYSTEM.md`
- `OUTPUT_CONTRACT.md`
- `GENERAL_VERDICT.md`
- `EVIDENCE_POLICY.md`
- `FALSE_POSITIVE_GUARD.md`
- `PRIORITIZATION.md`
- `WHAT_ON_OUTPUT.md`
- `FULL_REPORT_TEMPLATE.md`
- `SHORT_REPORT_TEMPLATE.md`

### Shared diagnostic layer
- `AI_DETECTION.md` + `AI_LANGUAGE.md`
- `EPISTEMIC_AND_CONTRACT.md`
- `EPISTEMIC_STATUS.md` ← NEW
- `STRENGTHS.md` ← NEW
- `TERMINOLOGY.md` ← NEW

### Fiction branch
- `FICTION_MASTER.md`
- `PLOT_AND_ARCS.md`
- `CHARACTER_AND_RELATIONS.md` ← NEW
- `SCENE.md`
- `POV.md`
- `DIALOGUE.md`
- `DETAIL_AND_EMBODIMENT.md` ← NEW
- `SUBTEXT_AND_MICROTENSION.md` ← NEW

### Nonfiction branch
- `NONFICTION_MASTER.md`
- `THESIS_AND_ARGUMENT.md`
- `EXPLANATION.md`
- `SOURCING_AND_EVIDENCE.md`
- `NONFICTION_PERSONA.md` ← NEW
- `TRUTH_CONTRACT.md` ← NEW
- `SUMMARY_QUOTE_RESPONSE.md` ← NEW

### Hybrid branch
- `HYBRID_MASTER.md`
- `ESSAY.md`
- `MEMOIR.md`
- `NARRATIVE_NONFICTION.md`
- `MODE_BALANCE.md`

### Language layer
- `LANGUAGE_PATHOLOGIES.md`
- `SENTENCE_MECHANICS.md`
- `PARAGRAPH_DYNAMICS.md`
- `COHESION_AND_TRANSITIONS.md`
- `RHYTHM_AND_SOUND.md`
- `METAPHOR_AND_ABSTRACTION.md`
- `REGISTER_AND_TONE.md`

### Propulsion & Architecture (разделены)
- `PROPULSION.md` ← split
- `MACRO_ARCHITECTURE.md` ← split

---

## Базовый пайплайн (без изменений от v5)

1. intake / passport / segmentation
2. ai-detection
3. epistemic + contract
4. propulsion + macro outline
5. **general_verdict** ← строится рано, на тексте и сигналах
6. genre branch (fiction | nonfiction | hybrid)
7. language
8. sentence
9. paragraph + cohesion
10. synthesis_guard / strengths / false_positive_guard
11. prioritization + revision plan

---

## Главный принцип (не изменился)

Ни один модуль не получает весь накопленный анализ.
Каждый модуль получает только:
- raw_text
- corpus_profile
- segment_map
- профильные документы
- строго нужные upstream-объекты (structured, not prose)

---

## Ключевые различия docs v6

| Проблема v5 | Решение v6 |
|------------|-----------|
| Docs как законы жанра | Scope/exceptions + false_positive_risks |
| Нет evidence discipline | EVIDENCE_POLICY.md |
| Нет epistemic layer | EPISTEMIC_STATUS.md |
| Нет strengths module | STRENGTHS.md |
| Нет общего словаря | TERMINOLOGY.md |
| Нет nonfiction persona | NONFICTION_PERSONA.md |
| Truth contract разбросан | TRUTH_CONTRACT.md |
| Нет quote/response module | SUMMARY_QUOTE_RESPONSE.md |
| PROPULSION_AND_MACRO слит | Разделён на 2 документа |
| SCENE слишком бинарна | Смягчена через change types |
| DIALOGUE с числовой нормой | Убрана, заменена functional balance |
| PLOT_AND_ARCS = classic only | Добавлены scope/exceptions |
