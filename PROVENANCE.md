# Походження публікації

Версія standalone **0.1.0-r1**, підготовлена для GitHub 07.11.2026.

Ланцюг: upstream instruction sources → project-kit1.0 → native candidate0.1.0 → standalone0.1.0-r1 → цей репозиторій.

Під час standalone адаптації у SKILL.md змінені лише два посилання `../../docs/` на `docs/`; frontmatter та поведінкові абзаци збережені. Додані лише три UI поля agents/openai.yaml. Для GitHub увесь standalone Skill перенесено в корінь без зміни його десяти файлів.

[publication.json](publication.json) містить source hashes цих десяти файлів і hashes попередніх ZIP. [checksums.sha256](checksums.sha256) — новий склад публікації. Історичні [native provenance](docs/provenance.md) та `metadata/` збережені як source records; їхній старий inventory не описує нову кореневу структуру.

README, INSTALL, EXAMPLES, LIMITATIONS та repository hygiene підготовлені для цієї публікації. Ігри, demo, експериментальні протоколи, credentials, приватні model traces та service specs не включені. Оригінальні [атрибуції й ліцензії](LICENSES.md) збережені.

Прийняття автором native CLI/headless scope не є загальною гарантією поведінки Desktop/IDE. Q04 залишається NOT MET.
