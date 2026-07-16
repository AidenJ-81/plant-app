# Pipe Thickness — ASME B31.3 배관 두께 계산기

ASME B31.3 (Process Piping) Para. 304.1.2 기반 직관 압력 설계 두께 및 MAWP 계산 웹 앱

---

## 앱 소개

배관 설계 엔지니어를 위한 브라우저 기반 계산 도구입니다. 별도 설치 없이 `index.html` 파일을 브라우저에서 바로 열어 사용할 수 있습니다.

설계 조건(압력·온도·재질)을 입력하면 NPS 1/2" ~ 36" 전 호칭경에 대해 최소 적정 스케줄과 MAWP를 일괄 산출합니다.

---

## 주요 기능

- **압력 설계 두께 계산** — ASME B31.3 Para. 304.1.2, `t = P·D / [2(S·E·W + P·Y)]`
- **MAWP 계산** — 선정 스케줄 기준 최대 허용 운전 압력 산출
- **전 호칭경 일괄 계산** — NPS 1/2" ~ 36" (ASME B36.10M / B36.19M)
- **383개 규격 지원** — ASME B31.3-2018 Table A-1M (CS / SS / 합금강 / Ni / Cu / Ti / Zr / Al)
- **허용응력 자동 보간** — 온도–허용응력 선형 보간 (MPa, °C 기준)
- **Y·W 계수 자동 산정** — 재질·온도 기준 자동 적용
- **도움말 인라인 편집** — 앱 내에서 도움말 수정 후 index.html 바로 다운로드

---

## 사용법

### 브라우저에서 바로 실행

별도 서버나 설치가 필요 없습니다. `index.html` 파일을 Chrome / Edge / Firefox 등 최신 브라우저로 열면 즉시 실행됩니다.

### 기본 계산 순서

1. **Size Standard** 선택 (B36.10M 또는 B36.19M)
2. **Material** → **Pipe Specification** 선택
3. **Weld Joint Quality Factor (E)** 선택
4. 설계 조건 입력: 압력(P), 온도(T), 기계적 여유(A), 밀 허용오차(M)
5. **검토 실행 →** 버튼 클릭
6. 결과 테이블에서 호칭경별 최소 스케줄·MAWP 확인

### 도움말 편집 및 배포 반영

1. 헤더 우측 **도움말** 버튼 클릭
2. 모달 우측 **✏️ 편집** 버튼 클릭
3. 텍스트 또는 표 셀을 클릭해 직접 수정
4. **💾 저장 후 다운로드 (index.html)** 클릭
5. 다운로드한 파일을 GitHub에 재업로드하면 모든 방문자에게 반영됨

---

## 적용 기준 / 코드

| 항목 | 기준 |
|------|------|
| 두께 계산식 | ASME B31.3-2018 Para. 304.1.2 |
| 허용응력 S | ASME B31.3-2018 Appendix A, Table A-1M (SI 단위) |
| Y 계수 | ASME B31.3-2018 Table 304.1.1 |
| W 계수 | ASME B31.3-2018 Table 302.3.5 |
| E 계수 | ASME B31.3-2018 Table 302.3.4 |
| 배관 치수 | ASME B36.10M, ASME B36.19M |

---

## GitHub Pages 배포 방법

### 사전 준비
- GitHub 계정 (무료)
- 이 ZIP 파일의 압축을 해제한 파일 3개: `index.html`, `README.md`, `_config.yml`

> ⚠️ 압축 해제 후 **폴더째로 올리지 말고 파일 3개만** Repository 루트에 올려야 합니다.

### 배포 순서

**1. GitHub에서 새 Repository 생성**
- GitHub 로그인 → 우측 상단 **＋** → **New repository**
- Repository name 입력 (예: `pipe-thickness`)
- **Public** 선택 → **Create repository** 클릭

**2. 파일 3개를 Repository 루트에 업로드**
- Repository 페이지에서 **Add file** → **Upload files** 클릭
- `index.html`, `README.md`, `_config.yml` 파일을 드래그 앤 드롭
- (폴더째로 올리지 말고 파일만 올릴 것)
- Commit message 입력 후 **Commit changes** 클릭

**3. Repository → Settings → Pages**
- Repository 상단 탭에서 **Settings** 클릭
- 좌측 사이드바에서 **Pages** 클릭

**4. Source: Deploy from branch → main 선택 → Save**
- Branch: **main** (또는 master) 선택
- 폴더: **/ (root)** 선택
- **Save** 클릭

**5. 잠시 후 아래 URL로 접속**
```
https://[계정명].github.io/[저장소명]/
```
- 보통 1~3분 후 접속 가능
- Settings → Pages 페이지에서 배포된 URL 확인 가능

---

## 면책 조항

본 앱의 계산 결과는 **예비 검토 목적**으로만 사용하십시오.

- 허용응력 및 계수 데이터는 ASME B31.3-2018 참고값입니다.
- 실제 설계 적용 시 반드시 해당 코드 에디션, 재질 인증서, 구매 사양으로 재검증하십시오.
- 본 계산기 사용으로 인한 설계 오류 또는 손해에 대해 개발자는 법적 책임을 지지 않습니다.
- 모든 결과는 자격을 갖춘 엔지니어의 검토 후 사용하여야 합니다.

---

## 버전 정보

| 버전 | 주요 변경 사항 |
|------|--------------|
| v3.4 | 스케줄 선정 기준 수정 (tn ≥ tm), B36.10/B36.19 정확값 적용, 도움말 기능 추가 |
| v3.3 | PIPES 배열 B36.10/B36.19 xlsx 실측값으로 전면 교체 |
| v3.2 | run() 함수 버그 수정 (S_ksi 미정의 참조 오류) |
| v3.1 | Pipe Specification 383개 규격으로 확장 (B31.3-2018 Table A-1M) |
| v3.0 | Material 8개 카테고리, 허용응력 MPa/°C 직접 사용으로 전환 |
