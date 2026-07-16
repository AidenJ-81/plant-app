# ⚡ Earthing · 변전소 접지망 설계 계산기

IEEE Std 80-2013 기반 변전소 접지망(Grounding Grid) 설계 자동 계산 웹앱입니다.  
단일 HTML 파일로 구성되어 **서버 없이 브라우저에서 바로 실행** 가능합니다.

---

## 앱 소개 및 주요 기능

- **Step 1~10** 순서대로 입력 → GPR · 메시전압 · 보폭전압 PASS/FAIL 자동 산출
- 상단 Summary Bar에서 3개 항목 검토 결과 한눈에 확인
- 접지망 평면도 SVG 자동 생성 (격자 크기·간격 연동)
- 도체 재질 13종 내장 (IEEE 80-2013 Table 1 기준)
- Step 2 고장전류(I)와 Step 6 대칭 고장전류(If) 자동 연동 — User 체크 시 개별 입력 가능
- **도움말** 버튼 — 모달 팝업으로 파라미터 설명 및 주의사항 확인
- 도움말 인라인 편집 기능 — 텍스트·표 셀 직접 수정 후 index.html로 저장·배포 가능
- Reset 버튼으로 IEEE 예제값 즉시 복원

---

## 사용법

1. `index.html`을 브라우저에서 열거나 GitHub Pages URL에 접속합니다.  
   *(별도 서버·설치 없이 바로 실행됩니다)*
2. **01 표준·재질** → **02 설계 조건** 순서대로 입력합니다.
3. 상단 Summary Bar에서 GPR / Mesh / Step 전압 검토 결과를 확인합니다.
4. **Reset · 예제값** 버튼으로 IEEE 예제 데이터를 불러올 수 있습니다.
5. **도움말** 버튼으로 각 파라미터 설명 및 주의사항을 확인합니다.

### 도움말 편집 및 재배포

1. **도움말** → **✏️ 편집** 클릭
2. 텍스트 또는 표 셀을 클릭하여 직접 수정
3. **💾 저장 후 다운로드 (index.html)** 클릭
4. 다운로드된 `index.html`을 GitHub 저장소에 업로드하면 모든 방문자에게 반영됩니다.

---

## 적용 기준 / 코드

| 기준 | 내용 |
|------|------|
| **IEEE Std 80-2013** | Guide for Safety in AC Substation Grounding |
| Para 11.3 | Conductor sizing formula |
| Para 14.2 | Tolerable step & touch voltage |
| Para 15.1 | Grid current calculation |
| Para 16.5 | Ground resistance Rg |
| Para 16.6 | Mesh voltage Em |
| Para 16.7 | Step voltage Es |

---

## GitHub Pages 배포 방법

### 1. GitHub에서 새 Repository 생성

1. [github.com](https://github.com) 로그인 후 우측 상단 **+** → **New repository** 클릭
2. Repository name 입력 (예: `earthing-calculator`)
3. **Public** 선택 → **Create repository** 클릭

### 2. 파일 3개를 Repository 루트에 업로드

1. 생성된 저장소 페이지에서 **Add file → Upload files** 클릭
2. ZIP을 압축 해제한 폴더 안의 파일 3개(`index.html`, `README.md`, `_config.yml`)를  
   **파일만 선택**하여 드래그 업로드  
   ⚠️ 폴더째로 올리지 말고 파일만 올릴 것
3. 하단 **Commit changes** 클릭

### 3. GitHub Pages 설정

1. 저장소 상단 **Settings** 탭 클릭
2. 좌측 메뉴에서 **Pages** 클릭

### 4. 브랜치 선택 및 저장

1. **Source** 항목에서 **Deploy from a branch** 선택
2. Branch를 `main`, 폴더를 `/ (root)` 로 설정
3. **Save** 클릭

### 5. URL 접속

- 저장 후 약 1~2분 후 Pages 페이지 상단에 URL이 표시됩니다.
- 접속 주소: `https://[계정명].github.io/[저장소명]/`

---

## 면책 조항

> ⚠️ 본 앱의 계산 결과는 **예비 검토 목적**으로만 사용하십시오.  
> 실제 변전소 접지 설계는 자격을 갖춘 전력 엔지니어의 검토와 현장 실측 데이터를 바탕으로 수행되어야 합니다.  
> IEEE Std 80-2013 원문 및 관련 국내 기준(KEC 등)과 반드시 대조하시기 바랍니다.  
> 본 도구 사용으로 인한 설계 오류 및 그에 따른 손해에 대해 개발자는 책임을 지지 않습니다.

---

## 버전 정보

| 버전 | 날짜 | 내용 |
|------|------|------|
| v1.1 | 2026-07-16 | 도움말 모달·편집·저장 기능 추가, Step 2↔6 전류 연동, 네이비 테마 적용 |
| v1.0 | 2026-06-22 | 최초 릴리즈 |
