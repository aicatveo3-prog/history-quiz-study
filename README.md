# 한국사 OX 퀴즈 (history-quiz-study)

한국사를 **시대별 OX 퀴즈**로 학습하는 정적 웹앱입니다. 답을 고르면 즉시 정답·해설이 뜨고, 파트별 **이론 정리**와 **최종 암기 체크리스트**를 함께 제공합니다.

**▶ 바로 풀기: https://aicatveo3-prog.github.io/history-quiz-study/**

## 구성

- 홈(챕터 목록) → 목차(파트) → 퀴즈 → 결과 흐름. 챕터 데이터는 카드 탭 시 지연 로딩.
- 각 문항: 기출·핵심 개념을 옳게 서술한 ⭕ 문항 + 핵심어를 바꾼 ❌ 변형 문항을 짝으로 구성(파트별 O/X 비율 5:5 근접, 같은 정답 4연속 없음).
- 파트별 **이론 정리** 패널(섹션·표·⚠️ 함정 체크 콜아웃) — ON/OFF 토글, 상태는 `localStorage` 저장.
- 파트 목록 상단 ⭐ 카드에서 **최종 암기 체크리스트** — 항목 탭 시 암기 체크(localStorage), 진행률 표시.

## 시대 구성 (계획: 10개 시대)

선사 · 고조선/초기국가 · 삼국/가야 · 남북국 · 고려 · 조선 전기 · 조선 후기 · 개항기 · 일제 강점기 · 현대

현재 수록: **한국사 제1편 (선사 시대) — 90문항**. (지방세기본법 제1장은 데이터 포맷 참고용 견본으로 함께 둠)

## 개발

- 정적 사이트: `app/index.html`, `app.js`, `chapters.js`, `quizdata-<id>.js`.
- 새 시대(장) 추가: `app/quizdata-<id>.js` 생성 → `app/chapters.js`의 `CHAPTER_LIST`에 `{ id, num, title, file, count }` 추가 → `app/index.html`의 `ASSET_VER` 갱신.
- 배포: GitHub Pages가 `main` 브랜치를 자동 배포.
