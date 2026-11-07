# Адресний QA Godot

Використовуй наявні тести й чинний engine профіль проєкту за його [правилами пошуку канону](project-context.md). Q06 — native SceneTree; новий GUT/GdUnit/addon або runner гри не додається заради перевірки. Визнач фактичний шлях Godot локально; не копіюй machine-local paths у спільні інструкції.

До запуску назви очікувану observable поведінку, доречні assertions/унікальні IDs, counts і timeout з контракту та наявного тесту. Не виводь очікування з поточного успішного stdout. Використовуй новий каталог логів, зберігай невдалі спроби; не повторюй успішний check без зміни або невизначеності.

```text
<GODOT_CONSOLE> --headless --path <PROJECT> --script res://<EXISTING_TEST> --log-file <NEW_ENGINE_LOG>
```

Це форма команди, не готовий тест і не доказ нової функції. Для позитивного запуску потрібні очікувані exit, реальні унікальні assertions і один узгоджений summary; stdout/stderr/engine log перевіряються разом. Missing test/resource/tool, zero/duplicate checks, timeout, parse/runtime/resource errors не стають PASS. Справжня engine error за exit0 теж відхиляє перевірку. `failures=0` не є рядком помилки.

Негативний запуск лишається FAIL; правильне виявлення має окремий detector result. Залежні skipped checks не зараховуються успішними, очікуваний count залежить від реально пройденої гілки. User args Godot передавай після `--`, лише якщо їх підтримує наявний тест. Помилку harness відділяй від дефекту гри; збережений артефакт оцінюється повторно без підміни продукту чи зміни контракту.

Перевір незалежні before/after snapshots, повернення команди й кількість notifications. Відмова/no-op не дає часткового commit або gameplay changed; пакетна зміна повна, callback читає узгоджений стан, повторна mutation не обходить guard. Оголошені load/reset events і діагностика не тотожні gameplay changed. Не додавай epsilon/нові API-межі заради зеленого тесту. Доречна регресія падає на конкретній причині й проходить після виправлення; вже покриті cases не дублюй.

Розділяй **parse/import**, **runtime**, **signal**, **synthetic input**, **physical interaction**, **visual**, **Inspector**. `pressed.emit()` перевіряє реакцію на сигнал; InputEvent — engine input route з потрібним viewport/frame loop; Computer Use або фактична ручна дія — фізичний ввід. Без MCP native/file перевірки залишаються можливими, але непроведений GUI не зараховується.

Для нового UI перевір типове й найбільше заявлене наповнення, довгий допустимий текст, справжню відмову та ріст даних у цільовому viewport. Важливі action controls і повний error/status мають бути доступні; нейтральний порожній status може бути правильним. Scroll-aware geometry враховує clip viewport і досяжність прокруткою, а не вимагає одночасної видимості всього контенту. Geometry не доводить visual; приховування даних чи зміна viewport не виправляють дефект.

Для editor-facing зміни назви власні scene/node/property й очікуваний runtime результат. Inspector roundtrip — фактичні edit → save → reopen → runtime; текстове редагування `.tscn` не називається GUI-редагуванням. Screenshot, реальна interaction, golden comparison і авторське прийняття — різні факти. За відсутнього еталона comparison не проведений.

Звітуй PASS/FAIL лише за проведеною перевіркою; missing prerequisite — BLOCKED/NOT RUN, непроведений огляд — NOT ASSESSED. N/A потребує причини поза заявленим scope. Для ізольованих Windows-запусків за потреби використовуй окремий child-only editor/user/temp profile; не змінюй глобальні settings, security або правила гри для обходу permission/harness failure.
