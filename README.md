# NLK LOD × BIBFRAME 2.0 / IFLA LRM Alignment

국립중앙도서관 국가서지 LOD 온톨로지와 BIBFRAME 2.0 및 IFLA LRM의 개념적 정렬 분석 — 보충 데이터 저장소

Supplementary data for the research article: *Conceptual Alignment Analysis of the National Library of Korea LOD Ontology with BIBFRAME 2.0 and IFLA LRM*.

## 개요 (Overview)

본 저장소는 국립중앙도서관 국가서지 LOD 온톨로지에 정의된 **속성 157개(객체 속성 33, 데이터 속성 124) 전체**에 대한 BIBFRAME 2.0 매핑 판정표를 공개합니다. 판정은 온톨로지 매칭 이론(Euzenat & Shvaiko, 2013)에 근거한 3단계 기준 — 동등(equivalent), 부분 정렬(partial alignment), 매핑 불가(no match) — 으로 수행되었으며, 모든 판정에 근거를 병기하여 제3자에 의한 재현과 검증이 가능하도록 하였습니다.

This repository publishes the full property-level mapping table (157 properties) of the National Library of Korea (NLK) LOD ontology aligned to BIBFRAME 2.0, with three-level verdicts (equivalent / partial alignment / no match) and per-property rationale.

**핵심 결과 (Key figures):** 동등 13건(8.3%) · 부분 정렬 113건(72.0%) · 매핑 불가 31건(19.7%)

## 파일 구성 (Contents)

| 파일 | 설명 |
|---|---|
| `data/alignment_table.csv` | 속성 전수 매핑 판정표 (157행, UTF-8 with BOM) |
| `docs/appendix.md` | 논문 부록 형식의 판정표 문서 (범주별 소계 포함) |
| `CITATION.cff` | 인용 정보 |
| `LICENSE` | 라이선스 (CC BY 4.0) |

## 데이터 사전 (Data Dictionary)

`data/alignment_table.csv`의 컬럼:

| 컬럼 | 설명 |
|---|---|
| 연번 | 1–157 일련번호 |
| 속성(nlon:) | 국가서지 LOD 자체 어휘 속성의 로컬명 (네임스페이스: `http://lod.nl.go.kr/ontology/`) |
| 속성 유형 | 객체 속성(owl:ObjectProperty) / 데이터 속성(owl:DatatypeProperty) |
| 범주 | 논의 단위 범주 13종 (자원 간 관계, 연관저록, 표제, 발행·제작·복제, 분류·청구기호, 식별자·부호, 주기, 전거, 소장·기관 서비스, 관리 메타데이터 등) |
| BIBFRAME 2.0 대응(안) | 제안 대응 클래스·속성 (`bf:` = `http://id.loc.gov/ontologies/bibframe/`) |
| 판정 | 동등 / 부분 정렬 / 매핑 불가 |
| 판정 근거 | 판정 사유 (승격 매핑·개체화 수반 여부 등) |

## 판정 기준 요약 (Verdict Criteria)

- **동등(≡):** 내포와 외연이 실질적으로 일치하여 의미 손실 없는 상호 대체가 가능한 경우
- **부분 정렬:** 포섭 또는 중첩 관계로 조건부 매핑만 가능한 경우. 리터럴의 개체 변환(승격 매핑)과 관련 자원 신규 생성(개체화)의 수반 여부를 근거에 명시
- **매핑 불가(⊥):** 대응 개체가 없거나 개념 모델 수준의 전제가 상이하여 의미 보존적 매핑이 성립하지 않는 경우

세부 기준과 방법론은 논문 3장을 참조하십시오.

## 유의사항 (Notes)

1. `itermNumberOfKDC`는 온톨로지 원문의 URI 철자를 그대로 수록한 것입니다(`itemNumberOfKDC`의 오기로 추정).
2. MADS/RDF 대응으로 표기된 전거 속성은 BIBFRAME 코어가 전거 상세 기술을 MADS/RDF에 위임하는 설계에 따른 것입니다.
3. 판정은 단일 판정자에 의한 것으로, 복수 판정자 교차 검증은 후속 연구 과제입니다. 본 표의 전면 공개는 이 한계를 투명성으로 보완하기 위한 것입니다.
4. 분석 대상 온톨로지 파일(`nlk_ontology.rdf`)의 저작권은 국립중앙도서관에 있으므로 본 저장소에는 포함하지 않습니다. 원본은 국립중앙도서관 LOD 서비스(https://lod.nl.go.kr)에서 확인할 수 있습니다.

## 인용 (Citation)

게재 확정 후 아래 형식으로 인용해 주십시오. (서지사항은 게재 확정 시 갱신 예정)

> [저자]. (게재 예정). 국가서지 LOD 온톨로지와 BIBFRAME 2.0 및 IFLA LRM의 개념적 정렬 분석: 한국 서지 환경의 특수성을 중심으로. *[학술지명]*.

데이터 자체의 인용은 `CITATION.cff` 또는 Zenodo DOI를 이용해 주십시오.

## 라이선스 (License)

본 저장소의 데이터와 문서는 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) 라이선스로 배포됩니다.
