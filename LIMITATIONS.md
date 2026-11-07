# Межі перевірки

- Skill дає інструкції; він не гарантує відсутності дефектів. **Q04 NOT MET**: експеримент не довів скорочення їхньої кількості.
- Native candidate0.1.0 прийнятий автором у CLI/headless scope з обмеженнями. Native N4 PARTIALLY VERIFIED, disabled hidden context NOT VERIFIED, F11 SCOPED_PASS_D20 мають власні історичні межі.
- Standalone редакція має перевірені source/link/inventory та deterministic ZIP. Офіційний quick_validate був BLOCKED через відсутній PyYAML; незалежні strict scalar checks виконані окремо, це не повна YAML/schema перевірка.
- Після пакування користувач показав вибраний Skill і змістовну відповідь на `$codex-indie-game-studio`. Це ручний smoke observation. Воно не доводить actual source reads, виконання всіх правил або якості створеного UI; окрему контрольовану перевірку Desktop та VS Code не заявлено.
- Project discovery не є security sandbox. Інструкції AGENTS та дозволи автора залишаються чинними.
- Remote/WSL/multi-root, інші ОС та автоматичне оновлення не перевірені. Немає MCP/hooks, логінів, CA/CDB workaround або зміни глобальних config.
- Історичні `metadata/` описують native source, а не поточне root layout. Актуальний [checksum manifest](checksums.sha256) описує цю публікацію, виключаючи себе; hash не є цифровим підписом.
- Публічний репозиторій не містить ігор, private profiles, credentials, скриншотів, сирих model logs або приватних проєктних документів.
