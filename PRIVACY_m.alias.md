# 개인정보 처리 방침 — m.alias

_최종 수정일: 2026-05-21_

본 문서는 **m.alias** Chrome 익스텐션(이하 "본 익스텐션")이 사용자 데이터를 어떻게 다루는지 설명합니다.

---

## 1. 수집하는 데이터

본 익스텐션은 사용자가 직접 입력한 다음 정보만을 저장합니다.

- **alias 키워드** (단축어로 사용할 짧은 문자열)
- **이동 대상 URL 또는 검색어** (각 alias에 연결된 값)
- **익스텐션 설정값** (예: 기본 검색 엔진 선택)

본 익스텐션은 다음을 **수집하지 않습니다**.

- 이름, 이메일, 전화번호, 주소 등 개인 식별 정보
- 사용자가 alias로 호출하지 않은 일반 브라우징 기록
- 위치 정보
- 인증 정보(아이디·비밀번호 등)
- 분석/텔레메트리 데이터

## 2. 저장 위치

모든 사용자 데이터는 Chrome 브라우저가 제공하는 [`chrome.storage.sync`](https://developer.chrome.com/docs/extensions/reference/api/storage)에만 저장되며, 사용자 본인의 Google 계정에 귀속됩니다.

- 데이터는 Google의 동기화 기능을 통해 사용자가 로그인한 Chrome 브라우저들 사이에서만 동기화됩니다.
- 데이터는 Google 저장소와 사용자의 로컬 브라우저를 벗어나지 않습니다.
- **개발자는 이 데이터에 접근할 수 없습니다.**

## 3. 데이터 공유

본 익스텐션은 사용자 데이터를 외부에 전송·공유·판매하지 않습니다. 외부 서버, 분석 서비스, 광고 네트워크, 트래킹 도구를 일체 사용하지 않습니다.

## 4. 사용하는 권한

| 권한 | 용도 |
|---|---|
| `storage` | `chrome.storage.sync`로 사용자 alias 저장·조회 |
| `activeTab` | 사용자가 "This Page"를 눌렀을 때에 한해 현재 탭의 URL/제목을 읽어 alias로 추가 |
| `tabs` | alias 실행 시 대상 URL을 새 탭 또는 기존 탭에 열기 |

본 익스텐션은 어떤 웹사이트에 대해서도 `host_permissions`를 요청하지 않습니다.

## 5. 데이터 삭제

사용자는 언제든지 다음 방법으로 데이터를 삭제할 수 있습니다.

- 팝업에서 개별 alias 삭제
- 팝업의 **Clear All** 사용
- 익스텐션 제거 (Chrome의 동기화 정책에 따라 `storage.sync` 데이터도 정리됨)

## 6. 아동의 개인정보

본 익스텐션은 13세 미만 아동을 대상으로 하지 않으며, 의도적으로 아동의 데이터를 수집하지 않습니다.

## 7. 정책 변경

본 정책이 변경될 경우, 동일한 URL에서 갱신된 내용과 "최종 수정일"로 다시 게시됩니다.

## 8. 문의

본 정책에 관한 문의는 본 익스텐션과 연결된 GitHub 저장소를 통해 개발자에게 연락해 주세요.

---
---

# Privacy Policy — m.alias

_Last updated: 2026-05-21_

This document describes how the **m.alias** Chrome extension (the "Extension") handles user data.

---

## 1. Data We Collect

The Extension stores only the data that the user explicitly enters into it:

- **Alias keys** (short strings the user types to invoke a shortcut)
- **Destination URLs or search queries** associated with each alias
- **Extension settings** (e.g., default search engine selection)

The Extension does **not** collect:

- Personal identifiers (name, email, phone, address)
- Browsing history outside the alias the user invokes
- Location data
- Authentication credentials
- Analytics or telemetry of any kind

## 2. How Data Is Stored

All user data is stored exclusively in [`chrome.storage.sync`](https://developer.chrome.com/docs/extensions/reference/api/storage), which is provided by the Chrome browser and tied to the user's own Google account.

- Data is synced across the user's Chrome browsers via Google's built-in sync mechanism.
- Data never leaves Google's storage layer and the user's local browser.
- The Extension's developer has **no access** to this data at any time.

## 3. Data Sharing

The Extension does **not** transmit, share, sell, or otherwise disclose user data to any third party. There are no external servers, no analytics services, no advertising networks, and no tracking integrations.

## 4. Permissions Used

| Permission | Purpose |
|---|---|
| `storage` | Save and read the user's aliases via `chrome.storage.sync`. |
| `activeTab` | Read the current tab's URL/title only when the user clicks "This Page" to add it as an alias. |
| `tabs` | Open the destination URL in a new or existing tab when an alias is invoked. |

The Extension does **not** request `host_permissions` for any website.

## 5. Data Removal

Users can delete their data at any time by:

- Removing individual aliases from the Extension popup, or
- Using **Clear All** in the popup, or
- Uninstalling the Extension (Chrome will purge the associated `storage.sync` data per the user's sync settings).

## 6. Children's Privacy

The Extension is not directed at children under 13 and does not knowingly collect any data from them.

## 7. Changes to This Policy

If this policy changes, the updated version will be published at the same URL as the current one, with a revised "Last updated" date.

## 8. Contact

For questions about this policy, contact the developer via the GitHub repository associated with this Extension.
