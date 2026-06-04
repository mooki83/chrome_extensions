# 개인정보 처리 방침 — Gmail 메일 캡처

_최종 수정일: 2026-06-04_

본 확장 프로그램("Gmail 메일 캡처")은 **사용자의 데이터를 외부로 전송하지 않으며, 모든 처리는 사용자의 로컬 기기 안에서만 이루어집니다.** 개발자를 포함한 제3자는 어떤 데이터에도 접근할 수 없습니다.

## 1. 수집하는 데이터

본 확장은 개발자나 외부 서버로 **어떤 데이터도 수집·전송하지 않습니다.** 확장이 기기 내에서 다루는 항목은 다음과 같으며, 모두 사용자의 명시적 동작(캡처 버튼 클릭)에 의해서만 처리됩니다.

- 사용자가 캡처를 요청한 메일의 **제목·보낸이·받는이·날짜·본문(HTML/텍스트)** — 사용자의 디스크에 `.json`으로 저장
- 사용자가 캡처를 요청한 메일 영역의 **스크린샷(PNG)** — 사용자의 디스크에 저장하거나, 새 탭 미리보기/클립보드 복사에 사용
- 사용자가 직접 설정한 **확장 설정값**(저장 폴더 경로, 캡처 형식, 캡처 가로폭, 뷰어 보기 모드)

**수집하지 않는 항목**: 개인 식별 정보, 위치 정보, 인증 정보(비밀번호·토큰·쿠키), 분석/텔레메트리, 광고 식별자, 브라우징 기록. 또한 위 메일 데이터를 외부로 보내거나 개발자가 열람하는 일은 일절 없습니다.

## 2. 저장 위치

- **확장 설정값**: `chrome.storage.local` (사용자 브라우저 프로필 내부)
- **새 탭 미리보기용 이미지**: `chrome.storage.session` 에 일시 보관되며, 뷰어 탭에 한 번 표시된 직후 즉시 삭제됩니다(휘발성, 브라우저 종료 시에도 소멸)
- **캡처 결과 파일(JSON/PNG)**: 사용자의 **Chrome 다운로드 폴더** 하위 사용자 지정 경로(기본 `gmail-captures/`)
- 외부 서버로의 전송: **없음**. 개발자의 데이터 접근: **불가능**

## 3. 데이터 공유

제3자에게 데이터를 전송·공유·판매하지 않습니다. 광고 네트워크, 분석 도구, 외부 SDK를 일절 사용하지 않습니다.

## 4. 사용하는 권한

| 권한 | 용도 |
| --- | --- |
| `storage` | 확장 설정값 저장(local) 및 새 탭 미리보기용 이미지 임시 보관(session) |
| `activeTab` | 사용자가 캡처 버튼을 누른 현재 Gmail 탭의 화면을 스크린샷 |
| `downloads` | 캡처한 JSON/PNG 파일을 다운로드 폴더 하위에 저장 |
| `clipboardWrite` | 뷰어에서 선택 영역 또는 전체 이미지를 클립보드로 복사 |
| `host: https://mail.google.com/*` | Gmail 페이지에 캡처 버튼을 주입하고, 메일 내용을 읽어 저장하며, 해당 탭을 스크린샷 |

## 5. 데이터 삭제

- **설정값**: 확장 프로그램을 제거하면 `chrome.storage`의 모든 설정이 함께 삭제됩니다.
- **미리보기용 임시 이미지**: 표시 직후 자동 삭제되며 영구 보관되지 않습니다.
- **캡처한 파일(JSON/PNG)**: 사용자 디스크의 일반 파일이므로 파일 탐색기/Finder에서 직접 삭제하면 됩니다.

## 6. 아동의 개인정보

본 확장은 아동을 대상으로 하지 않으며, 아동으로부터 어떤 정보도 수집하지 않습니다.

## 7. 정책 변경

본 방침이 변경될 경우 이 문서와 게시 URL을 갱신하고 상단의 "최종 수정일"을 함께 갱신합니다.

---

# Privacy Policy — Gmail Mail Capture

_Last updated: 2026-06-04_

This extension ("Gmail Mail Capture") **does not transmit any user data off the device. All processing happens locally on the user's own machine.** Neither the developer nor any third party can access any data.

## 1. Data We Collect

The extension **collects and transmits nothing** to the developer or any external server. The items it handles locally — only upon the user's explicit action (clicking the capture button) — are:

- The **subject, sender, recipients, date, and body (HTML/text)** of an email the user chose to capture, saved as a `.json` file on the user's disk.
- A **screenshot (PNG)** of the captured email area, saved to disk or used for the new-tab preview / clipboard copy.
- **User settings** the user configured (download folder path, capture formats, capture width, viewer view mode).

**Not collected**: personally identifiable information, location, credentials (passwords/tokens/cookies), analytics/telemetry, advertising identifiers, browsing history. The email data above is never sent anywhere and is never accessible to the developer.

## 2. Where Data Is Stored

- **Settings**: `chrome.storage.local` (inside the user's browser profile).
- **New-tab preview image**: held briefly in `chrome.storage.session` and deleted immediately after being shown once in the viewer tab (volatile; gone on browser exit).
- **Captured files (JSON/PNG)**: under the user's **Chrome downloads folder**, in a user-specified subpath (default `gmail-captures/`).
- Transmission to external servers: **none**. Developer access to data: **not possible**.

## 3. Data Sharing

No data is transmitted, shared, or sold to any third party. No ad networks, analytics, or external SDKs are used.

## 4. Permissions Used

| Permission | Purpose |
| --- | --- |
| `storage` | Store settings (local) and temporarily hold the preview image (session) |
| `activeTab` | Screenshot the current Gmail tab when the user clicks the capture button |
| `downloads` | Save captured JSON/PNG files under the downloads folder |
| `clipboardWrite` | Copy a selected region or the full image to the clipboard from the viewer |
| `host: https://mail.google.com/*` | Inject the capture button, read email content to save it, and screenshot the tab |

## 5. Data Deletion

- **Settings**: removing the extension deletes all `chrome.storage` settings.
- **Temporary preview image**: auto-deleted right after display; never retained.
- **Captured files (JSON/PNG)**: ordinary files on the user's disk — delete them directly via the file manager/Finder.

## 6. Children's Privacy

This extension is not directed at children and collects no information from children.

## 7. Changes to This Policy

If this policy changes, this document and its published URL will be updated along with the "Last updated" date above.
