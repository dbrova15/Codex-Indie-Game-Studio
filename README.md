# Codex Indie Game Studio

Проєктний Skill для роботи з Godot у Codex Desktop та розширенні Codex у VS Code.

Редакція **0.1.0-r1**. Допомагає змінювати GDScript, сцени, ресурси й UI, зберігати Inspector overrides та відділяти parse/runtime перевірки від interaction/visual/Inspector.

## Початок роботи

1. Завантажте цей репозиторій через **Code → Download ZIP** і розпакуйте його.
2. У вибраному локальному проєкті перевірте правила AGENTS та відсутність іншої активної копії `codex-indie-game-studio`.
3. Скопіюйте весь розпакований вміст репозиторію до `.agents/skills/codex-indie-game-studio/` вашого проєкту. Якщо така директорія вже є — не перезаписуйте її автоматично.
4. Відкрийте корінь проєкту у Codex Desktop або VS Code з розширенням Codex і перевірте Skill у списку.

Приклад запиту після перевірки discovery:

```text
Використай $codex-indie-game-studio. Прочитай правила цього Godot-проєкту
та допоможи виправити конкретну помилку, зберігши Inspector-налаштування.
```

[Повна інструкція](INSTALL.md) · [Приклади](EXAMPLES.md) · [Обмеження](LIMITATIONS.md) · [Історія](CHANGELOG.md)

## Що входить

- [SKILL.md](SKILL.md) — правила адресної роботи з Godot.
- [agents/openai.yaml](agents/openai.yaml) — назва та підказка в інтерфейсі.
- [docs/qa.md](docs/qa.md) — перевірки з чесними статусами.
- [docs/project-context.md](docs/project-context.md) — пошук канону саме вашої гри.
- `licenses/` — оригінальні ліцензії та атрибуції.

Це instruction-only Skill: без VSIX, Godot addon, MCP, hooks та інсталятора. Глобальна установка не потрібна. Плагіни та standalone Skills мають різну підтримку клієнтів: [plugins](https://learn.chatgpt.com/docs/plugins), [Skills](https://learn.chatgpt.com/docs/build-skills).

## Статус

Статичне пакування та відтворюваність попередньої standalone редакції перевірені. Користувач надав скриншоти вибору Skill і відповіді на пробний запит; це ручне спостереження, а не контрольована перевірка читання Skill та якості створеного UI. Повна окрема перевірка обох клієнтів ще не підтверджена.

**Q04 NOT MET:** експеримент не довів зменшення дефектів. Цей репозиторій не обіцяє такого результату.

## Походження та ліцензії

Редакція походить із native candidate0.1.0 та project-kit1.0. [Актуальний опис](PROVENANCE.md), [машинний запис](publication.json), [історичний provenance](docs/provenance.md).

Збережено MIT notice для Codex-Game-Studio та LGPL-3.0/NOTICE для godot-game-dev-studio. Див. [LICENSES.md](LICENSES.md); права попередніх авторів не замінюються новою загальною ліцензією. Файли `metadata/` є історичними native inventory; актуальний склад публікації — [checksums.sha256](checksums.sha256).
