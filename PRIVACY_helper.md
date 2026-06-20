# 개인정보 처리 방침 — Site 이전글/다음글

_최종 수정일: 2026-06-20_

## 1. 수집하는 데이터
이 확장 프로그램은 **개인을 식별할 수 있는 어떠한 정보도 수집하지 않습니다.**

- 기능 동작을 위해 읽는 항목: Site 글/목록 페이지의 화면 내용(글 목록 링크, 페이지 번호 등 공개된 페이지 구조). 이는 이전글/다음글 위치를 계산하기 위한 용도로만 사용되며, 어디에도 저장·전송되지 않습니다.
- 사용자 환경설정: 네비게이션 메뉴의 접힘/펼침 상태 한 가지(`nav_collapsed`)만 브라우저에 저장합니다.
- **수집하지 않는 항목**: 이름·이메일 등 개인 식별 정보, 위치, 로그인·인증 정보, 결제·금융 정보, 건강 정보, 개인 간 통신 내용, 브라우징 기록, 분석/텔레메트리.

## 2. 저장 위치
- 위 환경설정 값은 사용자의 브라우저 내 `localStorage`(Site 도메인)에만 저장됩니다.
- 외부 서버로 전송되는 데이터는 없습니다. 확장 프로그램은 자체 서버를 운영하지 않습니다.
- 제작자는 사용자의 어떤 데이터에도 접근할 수 없습니다.

## 3. 데이터 공유
- 제3자에게 데이터를 전송·공유·판매하지 않습니다.
- 광고·트래킹·외부 분석 도구를 사용하지 않습니다.

## 4. 사용하는 권한
| 권한 / 접근 | 용도 |
| --- | --- |
| site/* 페이지 접근 (content_scripts) | 글 페이지에 이전글/다음글·페이지 이동 버튼을 추가하고, 인접 글을 찾기 위해 같은 사이트의 목록 페이지를 읽기 위함 |

> 이 확장 프로그램은 별도의 `permissions`·`host_permissions`를 선언하지 않으며, 위 콘텐츠 스크립트 매칭 범위 밖에서는 동작하지 않습니다.

## 5. 데이터 삭제
- 저장되는 값은 환경설정 플래그 하나뿐입니다.
- 브라우저에서 Site의 사이트 데이터를 삭제하거나, 확장 프로그램을 제거하면 관련 값이 함께 제거됩니다.

## 6. 아동의 개인정보
이 확장 프로그램은 아동을 대상으로 하지 않으며, 아동으로부터 어떠한 개인정보도 의도적으로 수집하지 않습니다.

## 7. 정책 변경
본 방침이 변경될 경우 이 문서의 최종 수정일과 내용을 갱신합니다.

## 8. 문의
- 제작자: mooki
---
---

# Privacy Policy — Site Prev/Next

_Last updated: 2026-06-20_

## 1. Data We Collect
This extension does **not collect any personally identifiable information.**

- Read for functionality: the visible content of Site article/list pages (list links, page numbers, and other public page structure). This is used solely to compute the previous/next article position and is never stored or transmitted.
- User preference: a single navigation collapse/expand flag (`nav_collapsed`) is stored in the browser.
- **Not collected**: personal identifiers (name, email), location, login/authentication data, payment/financial data, health data, personal communications, browsing history, analytics/telemetry.

## 2. Where Data Is Stored
- The preference value is stored only in your browser's `localStorage`.
- No data is sent to any external server. The extension operates no backend of its own.
- The developer has no access to any of your data.

## 3. Data Sharing
- No data is transmitted, shared, or sold to third parties.
- No advertising, tracking, or external analytics tools are used.

## 4. Permissions Used
| Permission / Access | Purpose |
| --- | --- |
| Access to Site/* pages (content_scripts) | To add previous/next and page-navigation buttons on article pages, and to read the site's own list pages in order to locate adjacent articles |

> The extension declares no separate `permissions` or `host_permissions`, and does not run outside the content-script match scope above.

## 5. Data Deletion
- The only stored value is the preference flag.
- Clearing site data in your browser, or removing the extension, deletes the value.

## 6. Children's Privacy
This extension is not directed at children and does not knowingly collect personal information from children.

## 7. Changes to This Policy
If this policy changes, the "Last updated" date and content of this document will be revised.

## 8. Contact
- Developer: mooki
