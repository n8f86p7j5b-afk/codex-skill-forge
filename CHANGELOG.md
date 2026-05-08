# Changelog

## 2026-05-08

### Added

- Added `docs/ORIGIN.zh-CN.md` to explain the origin, purpose, usage, and key design turning points of 刻耳柏洛斯系统.
- Linked the origin document from README.

## 2026-05-05

### Added

- Reworked README positioning to describe Cerberus as a portable agent skill/protocol, not only a Codex skill.
- Added usage guidance for both Codex-compatible skill runtimes and other agent frameworks.

### Changed

- Clarified that `cerberus-system/` is a Codex-compatible package format, while the core protocol is framework-neutral.

## 2026-05-05

### Added

- Added language-following policy: Chinese users get Chinese interaction and the product name `刻耳柏洛斯系统`; English users get `Cerberus System`.
- Added Chinese invocation examples and bilingual UI metadata.

### Changed

- Adjusted product naming guidance to prefer transliteration in Chinese contexts instead of the awkward literal "three-head council" phrasing.

## 2026-05-05

### Added

- Added model and agent compatibility guidance so Cerberus can run across different LLMs and agent frameworks.
- Added compact, standard, and deep modes based on model capability and context.
- Added clearer trigger rules to avoid confusing Cerberus with ordinary pros-and-cons lists.

### Changed

- Simplified skill invocation and OpenAI UI metadata.
- Clarified that Cerberus does not select a model; it adapts to the active host model.

## 2026-05-05

### Added

- Added "living parts" guidance so Alpha, Beta, and Gamma speak from protective impulses, fears, desires, sensitivities, and voice texture instead of sounding like mechanical analysis columns.
- Added `living_signature` to persona card templates.

### Changed

- Updated Round 1 to include what each head protects, fears, and wants before voting.
- Updated council guidance to preserve human conflict before translating it into action.

## 2026-05-05

### Added

- Added mandatory visible cross-questioning requirements for Cerberus councils.
- Added a council validity checklist to prevent LLMs from compressing the process into a generic summary.

### Changed

- Clarified that Round 2 must run even when the three heads initially agree.
- Clarified that a valid Cerberus output must show interaction: directed questions, answers, self-blindspots, revised stances, and synthesis.

## 2026-05-05

### Added

- Added persistent Cerberus Profile support so users do not need to configure the council from scratch every time.
- Added `productization.md` with product experience guidance, returning-user flow, profile storage, quick/standard/deep modes, and update discipline.
- Added identity-neutral Gamma guidance. Gamma is now explicitly user-defined and must not assume gender, family structure, parenthood, marriage, religion, culture, or life path.
- Added reusable `cerberus_profile` template.

### Changed

- Updated onboarding flow to ask what the user wants Cerberus to protect from being traded away too casually.
- Updated adaptive interviewing Gamma choices to avoid family/gender assumptions.
- Updated README to highlight profile reuse and identity-neutral setup.

### Notes

- Existing Cerberus users should keep their current cards and add a profile file around them.
- New users can start in quick mode, standard mode, or deep mode depending on available time and energy.
