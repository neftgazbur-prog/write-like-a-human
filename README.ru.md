# write-like-a-human

[English](README.md) | Русский

Скилл для редактирования англоязычных текстов в Claude Code, Codex, OpenCode и других агентах с поддержкой Agent Skills.

Он ищет шаблонные обороты, предлагает исправления по 21 правилу и помогает убрать преувеличения, расплывчатые ссылки на экспертов и повторяющийся ритм. Совпадение с шаблоном — повод проверить фразу; полезную информацию нужно сохранить.

## Установка

Если установлены Node.js и npm:

```bash
npx skills add neftgazbur-prog/write-like-a-human --skill write-like-a-human
```

Выберите агента в установщике. Для просмотра без установки:

```bash
npx skills add neftgazbur-prog/write-like-a-human --list
```

Без установщика: скачайте [ZIP-архив последнего релиза](https://github.com/neftgazbur-prog/write-like-a-human/releases/latest/download/write-like-a-human.zip) и распакуйте.

Вручную: скопируйте `SKILL.md`, `LICENSE` и `NOTICE.md` в каталог скилла:

| Агент | Каталог |
|---|---|
| Claude Code | `~/.claude/skills/write-like-a-human/` |
| Codex / Copilot CLI / Gemini CLI | `~/.agents/skills/write-like-a-human/` |
| OpenCode, текущий проект | `.opencode/skills/write-like-a-human/` |
| OpenCode, глобально | `~/.config/opencode/skills/write-like-a-human/` |

После ручной установки перезапустите или обновите агента. Сам скилл — Markdown без скриптов и зависимостей; Node.js нужен только для необязательного установщика.

## Использование

```text
Use the write-like-a-human skill to edit this draft.
Preserve facts, names, dates, numbers, quotations, and citations.
Do not add information. Explain any uncertain changes.

<your draft>
```

Пример, вымышленный:

> It's important to note that the team plays a pivotal role in maintaining the archive. The team checks 120 records every Friday.

Вариант редактирования:

> The team maintains the archive and checks 120 records every Friday.

Новых фактов не добавлено; число и периодичность сохранены. Это иллюстрация, а не результат сравнительного тестирования моделей.

## Ограничения и обратная связь

Регулярное выражение и примеры рассчитаны на **английский язык**. Для русского нужна адаптация списка выражений. Результат зависит от модели и требует проверки человеком. Скилл не определяет авторство текста и не гарантирует прохождение детекторов ИИ.

[Сообщить о проблеме или предложить правило](https://github.com/neftgazbur-prog/write-like-a-human/issues/new). Приложите короткий текст, которым вправе поделиться, название агента/модели и объяснение желаемого исправления.

## Источник и лицензия

Переработка [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), авторы — участники Wikipedia. Материал переписан, перегруппирован и дополнен для редактирования обычных текстов. Проект не связан с Wikimedia Foundation.

**CC BY-SA 4.0**: [полный текст лицензии](LICENSE), [уведомление об авторстве](NOTICE.md). Разрешены распространение и переработка, включая коммерческое использование, при соблюдении условий лицензии.