# Походження native adapter 0.1.0

Основа — project-kit 1.0.0, ZIP SHA256 `8B7F56F3D7E21D67920704EABE8C1B53A8A45266693173DEAA09F1428740B5C0`. Окремий demo не входить до пакета. Редакція адаптера 0.1.0 не означає прийняття project-kit або доведену користь.

Походження source kit:

- BoyinGlasses/Codex-Game-Studio, revision `bcdf7199968d1bef6b627ece5adb09fa27e36229`, plugin 0.1.0/framework 1.1.0. [Ліцензія](../licenses/Codex-Game-Studio-LICENSE).
- Фактичний bgrenat/godot-game-dev-studio, revision `cb2e2cb6bedeada7140d73a0f45a93db1964e634`, plugin 0.3.0. Declared powehi-eu збережено в оригінальному [NOTICE](../licenses/godot-game-dev-studio/NOTICE.md); [LICENSE](../licenses/godot-game-dev-studio/LICENSE).

LICENSE/NOTICE перенесено побайтово з перевіреного source ZIP. Згадки ширшого upstream складу в NOTICE не означають включення його addons/ролей/assets. Нові спільні ліцензійні умови не оголошуються.

Адаптації обмежені доставкою:

1. Додано root portable manifest та власний README.
2. У Skill два project-relative bindings замінено package-relative переходами до `docs/project-context.md` і `docs/qa.md`. Frontmatter та Godot-правила збережено.
3. У QA посилання на карту замінено context guide; решта QA збережена.
4. Додано короткий context guide; він не містить канону або поточного стану конкретної гри. Старі шаблони AGENTS/source-map/active не встановлюються плагіном.
5. Source manifest замінено цим provenance, без перенесення історичного E2 pending як актуального статусу.

Точні hashes адаптованого складу — у [CSV](../metadata/file-inventory.csv) та [checksums](../metadata/checksums.sha256). Source-file hashes і повні diff збережено у зовнішніх evidence збірки; ZIP hash міститься у зовнішньому build receipt. Metadata не є цифровим підписом або гарантією резервної копії.

Q05: dialogue/VN виключена; Q06: наявні native SceneTree перевірки; Q07: hooks відкладені. **Q04 NOT MET**: закритий експеримент не довів зменшення дефектів (C/I 0/0). Нове C/I-порівняння цим адаптером не запускається.
