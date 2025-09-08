# Gitmoji Commit Message Template

Use emojis with Conventional Commit style to make the intent clear at a glance.

---

## Format

```
<emoji> <type>[optional scope]: <subject>

[optional body]

[optional footer(s)]
```

- **emoji**: Single Gitmoji character representing the change type
- **type**: Conventional Commit type (feat, fix, docs, etc.)
- **scope**: Optional scope in parentheses (module, folder, etc.)  
- **subject**: ≤50 chars, imperative present tense, lowercase first letter, no period

---

## Emoji ↔︎ Type 매핑

* ✨ **feat** — 새로운 기능 (SemVer *minor*)
* 🐛 **fix** — 버그 수정 (SemVer *patch*)
* 📝 **docs** — 문서만의 변경
* 🎨 **style** — 포맷·세미콜론 등 논리적 변경 없는 코드 스타일 수정
* ♻️ **refactor** — 리팩터링 (기능 추가·버그 수정 아님)
* ⚡️ **perf** — 성능 개선
* ✅ **test** — 테스트 추가·수정
* 🏗 **build** — 빌드 시스템·외부 의존성 변경
* 👷 **ci** — CI 설정·스크립트 변경
* 🔧 **chore** — 잡무(빌드 설정, 의존성 업데이트 등)
* ⏪ **revert** — 이전 커밋 되돌리기