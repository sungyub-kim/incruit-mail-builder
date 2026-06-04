# 인크루트 메일 빌더

메일 템플릿 11종 + 본문 컴포넌트 라이브러리 + 실시간 미리보기 + 메일 호환성(Outlook 포함) 검수.

🔗 **빌더 열기**: https://sungyub-kim.github.io/incruit-mail-builder/

## 기능 요약

- **형태 옵션**: 공용(700px) / 라운드(640px) / 헤더·푸터 없음 / 공지 텍스트형(noticeTemp) / 공지 이미지형(940px)
- **대상**: 개인 / 기업 (액센트 컬러 자동 전환 — `#ff460a` / `#2772d0`)
- **푸터**: 수신거부 가능 / 발신전용
- **본문 에디터**: WYSIWYG + HTML 모드, 메일 호환 인라인 스타일 자동 보정
  - `<font>`, `<s>`, `<hr>`, `<blockquote>`, deprecated align 등 비호환 태그 자동 변환
  - span 중첩 평탄화 (`flattenSpans`)
  - 표 삽입/편집 (드래그 셀 선택, 병합/분할, 너비 균등)
- **본문 템플릿 라이브러리**: 전체 / 공지사항용 / 부분 탭
- **저장**: HTML 복사 / 선택 1개 다운로드 / 4종 일괄 저장

## 구성

| 파일 | 설명 |
|---|---|
| `builder.html` | 메인 빌더 (단일 HTML, 외부 의존 최소) |
| `index.html` | `builder.html`로 리다이렉트 |
| `01_*.html` ~ `04_*.html` | 공용 700px 메일 템플릿 (개인/기업 × 수신거부/발신전용) |
| `05_*.html` ~ `08_*.html` | 라운드 640px 메일 템플릿 |
| `09_headerfooter_removed.html` | 헤더·푸터 제거 |
| `10_notice_common.html` / `11_notice_corporate.html` | 공지사항 (noticeTemp) |

## 메일 호환성

본 빌더는 Outlook 데스크톱을 포함한 주요 메일 클라이언트 호환을 우선합니다. 출력 HTML은 인라인 스타일 + 시맨틱 태그 위주로 작성되며, `<blockquote>` / `<hr>` 같은 호환성 위험 요소는 자동으로 안전한 형태(table 기반 HR 등)로 변환됩니다.

## 라이선스

내부용 / Incruit Corporation
