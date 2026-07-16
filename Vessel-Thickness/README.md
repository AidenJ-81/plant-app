# Vessel Thickness Calculator

**ASME Sec.VIII Div.1 압력용기 두께 계산 웹앱**

Live Demo → [GitHub Pages URL]

---

## 기능

- Shell 두께 계산 (UG-27)
- Head 두께 계산 (UG-32) — 2:1 Ellipsoidal / ASME F&D / Hemispherical / Flat
- MAWP (최대 허용 작동 압력) 산정
- 부피 · 표면적 · 중량 계산
- 수평 / 수직 배치 지원
- 보온재(Insulation) 중량 및 표면적
- ASME BPVC 2014 Sec.II Part D 허용응력 DB 내장 (Ferrous 219종 + Non-Ferrous 252종)

## 사용법

별도 설치 없이 `index.html` 파일을 브라우저에서 바로 열면 실행됩니다.  
서버가 필요 없는 단일 HTML 파일(Single Page Application)입니다.

## 적용 Code

| 항목 | 내용 |
|---|---|
| 압력용기 설계 | ASME BPVC Sec.VIII Div.1 |
| 허용응력 DB | ASME BPVC 2014 Sec.II Part D Table 1A / 1B |
| Shell 두께 | UG-27(c)(1) |
| Head 두께 | UG-32(b)(d)(e) |
| 단위계 | kgf/cm², mm |

## 면책 조항

본 앱의 계산 결과는 예비 검토(Preliminary Study) 목적으로만 사용하십시오.  
실제 설계·시공 적용 전에는 반드시 해당 에디션의 ASME Code 원본 및 공인 엔지니어의 검토가 필요합니다.

## 버전

- **v2.6** — 재질 DB 확장 (BPVC 2014 Table 1A/1B 전체 적용), 도움말 추가
- v2.5 — 초기 웹 버전 (Ferrous 8종, Non-Ferrous 2종)

## License

© Xi C&A. All rights reserved.
