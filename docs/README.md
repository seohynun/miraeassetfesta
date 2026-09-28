# 문서 목차

`docs/` 폴더의 문서 328개를 주제별로 분류한 목차입니다. 파일은 옮기거나 지우지 않았고, 이 목차만 추가했습니다.

프로젝트 개요는 [README](../README.md), 전체 기록은 [PROJECT.md](../PROJECT.md)를 먼저 보세요.

## 분류 요약

| 분류 | 문서 수 |
|---|---|
| 1. 먼저 읽을 문서 | 5 |
| 2. 배포·인프라 | 14 |
| 3. 데이터 | 14 |
| 4. 도메인 지식 | 4 |
| 5. 탐색적 분석 (EDA) | 24 |
| 6. 온톨로지·지식그래프 | 29 |
| 7. 기술제안서 | 59 |
| 8. 검토·질의응답 기록 | 38 |
| 9. 검증 라운드 기록 (과정) | 53 |
| 10. 인수인계·계획·회의 (과정) | 32 |
| 11. 선행연구·설계 스펙 | 21 |
| 12. 핵심문서모음 (스냅샷) | 35 |

## 파일을 옮길 때 주의할 점

- `tests/test_snapshot_round6.py`가 `recheck_2026-09-02_round5.md`와 `kg_structure_probe_round3_2026-09-02.md`를 직접 읽습니다.
- `scripts/make_submission.py`가 `API_SPEC.md`의 존재를 확인합니다.
- `recheck_loop_2026-09-02.md`와 `funds_test_result_2026-09-04.md`는 `eval/`의 스크립트가 생성하는 파일입니다.
- `data_dictionary/`, `ontology_rules/`, `review_2026-08-26/`, `bench/`, `viz/`, `eda/public_funds_entity_map.md`, `proposal/NUMBERS.md`는 `scripts/`의 생성·조립 스크립트가 경로를 고정해 씁니다.
- 날짜가 붙은 기록 문서끼리 서로 경로로 인용하는 경우가 많습니다.

## 1. 먼저 읽을 문서

시스템이 어떻게 동작하는지, API 규격이 무엇인지 설명하는 문서입니다.

| 문서 | 제목 |
|---|---|
| [API_SPEC.md](<API_SPEC.md>) | API 명세 — `GET /answer` (제출 항목 3 · 제안서 부록 D) |
| [HOW_IT_WORKS.md](<HOW_IT_WORKS.md>) | 🔍 우리 Agent 는 어떻게 답을 만드는가 — 원리 (2026-08-31) |
| [agent_architecture_notes.md](<agent_architecture_notes.md>) | 🧩 Agent 아키텍처 참고 노트 — 그래프 엔지니어링 적용 검토 |
| [sqlite_db_architecture.md](<sqlite_db_architecture.md>) | 🗄️ SQLite 데이터베이스 아키텍처 및 구축 가이드 (`SQLITE_SETUP.md`) |
| [구조도_전체흐름_2026-09-06.md](<구조도_전체흐름_2026-09-06.md>) | 전체 답변 흐름 구조도 — 디자인 전달용 텍스트 명세 (2026-09-06) |

## 2. 배포·인프라

서버 배포 절차, 인프라 구성, 응답 속도 측정 기록입니다.

| 문서 | 제목 |
|---|---|
| [DB_SETUP.md](<DB_SETUP.md>) | 🗄️ DB 구축 가이드 — 로컬 재현 절차 (2026-08-31) |
| [DEPLOY.md](<DEPLOY.md>) | 🚀 배포 절차 — NCP + Docker + Caddy(HTTPS) |
| [DEPLOY_CHECKLIST.md](<DEPLOY_CHECKLIST.md>) | ☀️ 8/16 아침 — 배포 작업 체크리스트 |
| [INFRA.md](<INFRA.md>) | 🏗️ 서버 인프라 구성 설명서 |
| [NCP_CONSOLE.md](<NCP_CONSOLE.md>) | 🖥️ NCP 콘솔 — 서버 개설 클릭 순서 |
| [redeploy_request_2026-08-31.md](<redeploy_request_2026-08-31.md>) | 🚀 재배포 요청 — ETF 브랜치 (2026-08-31 · 병철 → 리드) |
| [redeploy_request_2026-09-01.md](<redeploy_request_2026-09-01.md>) | 🚀 재배포 요청 #2 — 공식 예시 문항 수리분 (2026-09-01 · 병철 → 리드) |
| [배포요청_종목지시자_되묻기전제_2026-09-06.md](<배포요청_종목지시자_되묻기전제_2026-09-06.md>) | 배포 요청 — 종목 지시자·되묻기 전제 (2026-09-06) |
| [배포요청_채권QA라운드1_2026-09-06.md](<배포요청_채권QA라운드1_2026-09-06.md>) | 배포 요청 — 채권 QA 라운드1 수리 (2026-09-06) |

**`bench/`**

| 문서 | 제목 |
|---|---|
| [hcx_latency.md](<bench/hcx_latency.md>) | HCX 레이턴시·처리량 실측 — 지시서 §4.3 ① (워크샵 제출물) |
| [hcx_latency_full3x3.json](<bench/hcx_latency_full3x3.json>) |  |
| [hcx_latency_full3x3.md](<bench/hcx_latency_full3x3.md>) | HCX p95 레이턴시 실측 — 지시서 §4.3 ① |
| [hcx_latency_tail_n40.json](<bench/hcx_latency_tail_n40.json>) |  |
| [hcx_latency_tail_n40.md](<bench/hcx_latency_tail_n40.md>) | HCX p95 레이턴시 실측 — 지시서 §4.3 ① |

## 3. 데이터

제공 데이터 설명, 컬럼별 데이터 사전, 외부 데이터 수집 계획입니다.

| 문서 | 제목 |
|---|---|
| [BONDS_MASTER.md](<BONDS_MASTER.md>) | 📘 국내채권 작업 기록 — 08-10 첫 EDA 부터 09-03 까지 무엇을 했는가 (v4 · 2026-09-03) |
| [DATA_COLLECTION_PLAN.md](<DATA_COLLECTION_PLAN.md>) | 📦 데이터 수집 실행 계획 — 주최 측 문의 없이 가는 경로 |
| [DATA_GUIDE_data폴더.md](<DATA_GUIDE_data폴더.md>) | 📁 `data/` · `1.금융상품/` — 데이터 설명서 |
| [DATA_NEEDS.md](<DATA_NEEDS.md>) | 📥 추가 수집이 필요한 데이터 |
| [DATA_V2_2026-08-24_impact.md](<DATA_V2_2026-08-24_impact.md>) | 📦 2차 배포 데이터(2026-08-24) 분석 — 우리 프로젝트에 미치는 영향 |
| [EXTERNAL_DATA.md](<EXTERNAL_DATA.md>) | 📦 외부 수집 데이터 카탈로그 — 2026-08-20 기준 |
| [additional_bonds.md](<additional_bonds.md>) | 국내채권 추가 검토 — 영구채 미탐 규명 · 특수구조 구체화 |
| [notice_2026-08-24_impact.md](<notice_2026-08-24_impact.md>) | 📢 주최 공지(디스코드) 대조 — 우리 규칙과 맞는가 (2026-08-30 · 병철) |
| [spec_audit_2026-08-24.md](<spec_audit_2026-08-24.md>) | 📋 제출 규격 대조 감사 — 리드 확인 요청 (이병철, 2026-08-24) |
| [web_collection_handoff_2026-08-18.md](<web_collection_handoff_2026-08-18.md>) | 🔁 인수인계 — 미래에셋 웹 수집 · 코드북 완성 · DB 적재 (2026-08-18) |

**`data_dictionary/`**

| 문서 | 제목 |
|---|---|
| [README.md](<data_dictionary/README.md>) | 📖 데이터 사전 — 도메인별 피처·의미·결측 판정 |
| [bonds.md](<data_dictionary/bonds.md>) | 📖 데이터 사전 — 국내채권 |
| [etf.md](<data_dictionary/etf.md>) | 📖 데이터 사전 — ETF (국내·해외) |
| [funds.md](<data_dictionary/funds.md>) | 📖 데이터 사전 — 공모펀드 |

## 4. 도메인 지식

채권·펀드 도메인을 정리한 문서입니다.

**`domain/`**

| 문서 | 제목 |
|---|---|
| [domestic_bonds.md](<domain/domestic_bonds.md>) | 📗 국내채권 도메인 이해 |
| [domestic_bonds_graph.md](<domain/domestic_bonds_graph.md>) | 🕸️ 국내채권 구조도 — 작업 산출물 기준 정리 |
| [domestic_bonds_sample.md](<domain/domestic_bonds_sample.md>) | 🧾 국내채권 실제 예시 데이터 — 40컬럼 한 줄씩 읽기 |
| [public_funds.md](<domain/public_funds.md>) | 📘 공모펀드 도메인 이해 |

## 5. 탐색적 분석 (EDA)

상품군별 데이터 탐색 노트와 검토 기록입니다.

| 문서 | 제목 |
|---|---|
| [EDA_GUIDE.md](<EDA_GUIDE.md>) | 📊 EDA & 온톨로지 설계 준비 가이드 (팀 배포용) |

**`eda/`**

| 문서 | 제목 |
|---|---|
| [.gitkeep](<eda/.gitkeep>) |  |
| [domestic_bonds_audit_2026-08-18.md](<eda/domestic_bonds_audit_2026-08-18.md>) | 국내채권 판정 감사 — 2026-08-18 (2차 검증 단계) |
| [domestic_bonds_notes.md](<eda/domestic_bonds_notes.md>) | 🔍 국내채권 EDA 노트 (T1) |
| [domestic_etfs_axis_mismatch.md](<eda/domestic_etfs_axis_mismatch.md>) | ⚠️ 국내ETF 분류축(axis) 불일치 — 주최측 문의용 근거 |
| [domestic_etfs_entity_map.md](<eda/domestic_etfs_entity_map.md>) | 🧬 국내ETF 엔티티 구조도 — 워크샵 논의용 초안 |
| [domestic_etfs_notes.md](<eda/domestic_etfs_notes.md>) | 국내ETF EDA 노트 (T2) |
| [etf_audit_2026-08-18.md](<eda/etf_audit_2026-08-18.md>) | ETF 판정 감사 — 2026-08-18 (2차 검증 단계 · 국내 + 해외) |
| [etf_fund_unification_handoff.md](<eda/etf_fund_unification_handoff.md>) | 🤝 ETF ↔ 펀드 통일 제안 (펀드팀 전달용) |
| [etf_index_normalization.md](<eda/etf_index_normalization.md>) | 🧭 지수(벤치마크) 정규화 — ETF↔펀드↔해외ETF 교차조인 |
| [etf_track_entity_map.md](<eda/etf_track_entity_map.md>) | 🧬 ETF 트랙 통합 엔티티 구조도 — 국내ETF · ETN · 해외ETF |
| [overseas_etfs_notes.md](<eda/overseas_etfs_notes.md>) | 해외ETF EDA 노트 (T3) |
| [public_funds_audit_2026-08-18.md](<eda/public_funds_audit_2026-08-18.md>) | 공모펀드 판정 감사 — 2026-08-18 (2차 검증 단계) |
| [public_funds_codes_conclusions.md](<eda/public_funds_codes_conclusions.md>) | ✅ 공모펀드 식별 코드 — 확정된 결론 |
| [public_funds_codes_handoff.md](<eda/public_funds_codes_handoff.md>) | 🔁 인수인계 — 공모펀드 식별 코드 매칭 EDA (2차) |
| [public_funds_entity_map.md](<eda/public_funds_entity_map.md>) | 🧬 공모펀드 엔티티 구조도 — 컬럼 단위 배정표 |
| [public_funds_feature_overview.md](<eda/public_funds_feature_overview.md>) | 🗂️ 공모펀드 피처 총람 — 45컬럼 한 장 요약 |
| [public_funds_handoff_2026-08-18.md](<eda/public_funds_handoff_2026-08-18.md>) | 🔁 인수인계 — 공모펀드 값 의미 · 결측 처리 (2026-08-18) |
| [public_funds_notes.md](<eda/public_funds_notes.md>) | 공모펀드 EDA 노트 (T4) |
| [public_funds_value_dictionary.md](<eda/public_funds_value_dictionary.md>) | 📖 공모펀드 값 사전 — 컬럼 45개와 범주형 값의 의미 |
| [공모펀드_검토_결정대기_2026-08-29.md](<eda/공모펀드_검토_결정대기_2026-08-29.md>) | 🕹️ 공모펀드 식별자 계열 — 결정 대기 3건 (리드 판단 필요) — 2026-08-29 |
| [공모펀드_검토기록_2026-08-28.md](<eda/공모펀드_검토기록_2026-08-28.md>) | 📝 공모펀드 검토 작업 기록 — 2026-08-28 (에이전트 동반 검토 · 블록 ①: 식별자 계열) |
| [공모펀드_검토기록_2026-08-30.md](<eda/공모펀드_검토기록_2026-08-30.md>) | 📝 공모펀드 검토 작업 기록 — 2026-08-30 (블록 ①-보론: 결측 규칙 전수 점검) |
| [공모펀드_검토기록_2026-08-30_이름계열.md](<eda/공모펀드_검토기록_2026-08-30_이름계열.md>) | 📝 공모펀드 검토 작업 기록 — 2026-08-30 (블록 ②: 이름 계열 + 종목명 문자열 규약 파생) |

## 6. 온톨로지·지식그래프

온톨로지 규칙, 지식그래프 설계와 수정 기록, 가드(guard) 이관 기록입니다.

| 문서 | 제목 |
|---|---|
| [ONTOLOGY_BUILD_PLAN.md](<ONTOLOGY_BUILD_PLAN.md>) | 🕸️ 온톨로지·KG 구축 지시서 — 워크샵(8/17) → 수렴 완료(8/21) |
| [graph_sources_review_2026-08-25.md](<graph_sources_review_2026-08-25.md>) | 🕸️ 도메인별 그래프 재료 소스 검토 — 2026-08-25 |
| [guard_migration_inventory_2026-09-03.md](<guard_migration_inventory_2026-09-03.md>) | 가드 → 슬롯 인벤토리 (단계 0 · 2026-09-03) |
| [guard_to_yaml_migration_2026-09-03.md](<guard_to_yaml_migration_2026-09-03.md>) | 작업 절차 — 코드 가드에 흩어진 수리를 일반화해 yaml 로 옮기고, 실제로 적용되게 만들기 (2026-09-03) |
| [kg_dom_ticker_11_2026-08-30.md](<kg_dom_ticker_11_2026-08-30.md>) | 🔎 KG 종목 노드 — ㉢ 대상 11종 식별자 조사 (2026-08-30 · 병철) |
| [kg_motherfund_fix_2026-09-04.md](<kg_motherfund_fix_2026-09-04.md>) | 지시서 — KG 접지 불가 노드 정리 (모펀드 · 이름폴백) · 2026-09-04 |
| [kg_security_gap_2026-08-28.md](<kg_security_gap_2026-08-28.md>) | KG 종목 노드 — 국내·해외 미연결 실측 (2026-08-28 · Leebyungchul) |
| [ontology_audit_2026-09-02.md](<ontology_audit_2026-09-02.md>) | 온톨로지 전수조사 — ETF 몫 (2026-09-02 · 병철) |
| [ontology_kg_review_2026-09-04.md](<ontology_kg_review_2026-09-04.md>) | 최종 구현 온톨로지·KG 검토 — 2026-09-04 (1차) |
| [ontology_rule_dedup_2026-09-04.md](<ontology_rule_dedup_2026-09-04.md>) | 공모펀드 온톨로지 — 중복·일반화 검토 · 2026-09-04 |
| [rule_delivery_audit_2026-09-03.md](<rule_delivery_audit_2026-09-03.md>) | 작업 지시서 — yaml 규칙이 HCX에 "어떻게" 전달되는지 감사 (2026-09-03) |
| [rule_delivery_audit_result_2026-09-03.md](<rule_delivery_audit_result_2026-09-03.md>) | 규칙 전달 감사 — 결과 (2026-09-03) |

**`ontology_rules/`**

| 문서 | 제목 |
|---|---|
| [01_naming.md](<ontology_rules/01_naming.md>) | 규칙 1. 지칭 정리 — 같은 것을 같다고 부르기 |
| [02_missing.md](<ontology_rules/02_missing.md>) | 규칙 2. 결측 방어 — 비어 있음의 뜻을 가른다 |
| [03_external.md](<ontology_rules/03_external.md>) | 규칙 3. 외부 데이터 병합 — 마스터를 고치지 않고 옆에 붙인다 |
| [04_grain.md](<ontology_rules/04_grain.md>) | 규칙 4. 행 단위(grain) — `COUNT(*)` 는 종목 수가 아니다 |
| [05_population.md](<ontology_rules/05_population.md>) | 규칙 5. 기본 모수 — 말하지 않은 조건을 고정한다 |
| [06_derivation.md](<ontology_rules/06_derivation.md>) | 규칙 6. 파생·유도 — 없는 축을 규칙으로 만든다 |
| [07_disjoint.md](<ontology_rules/07_disjoint.md>) | 규칙 7. 배타·분리 — 한 축에 놓으면 안 되는 것들 |
| [08_unit.md](<ontology_rules/08_unit.md>) | 규칙 8. 단위·스케일 — 같은 이름, 다른 눈금 |
| [09_forbid.md](<ontology_rules/09_forbid.md>) | 규칙 9. 금지 규칙 — 이 컬럼으로는 답하지 마라 |
| [10_absent.md](<ontology_rules/10_absent.md>) | 규칙 10. 부재 선언 — 컬럼이 없다는 사실도 지식이다 |
| [11_hierarchy.md](<ontology_rules/11_hierarchy.md>) | 규칙 11. 계층 — ‘미국’ 질의가 ‘북미’ 를 포함하는가 |
| [12_asof.md](<ontology_rules/12_asof.md>) | 규칙 12. 기준일·시점 — 언제 기준의 사실인가 |
| [README.md](<ontology_rules/README.md>) | 🧱 온톨로지 규칙 12종 — 규칙별 검토 문서 |

**`rule_audit/`**

| 문서 | 제목 |
|---|---|
| [README.md](<rule_audit/README.md>) | 🔍 문자열 규칙 전수 검토 — ETF (2026-08-31 · 병철) |
| [inverse_domestic_2026-08-31.csv](<rule_audit/inverse_domestic_2026-08-31.csv>) |  |
| [inverse_overseas_2026-08-31.csv](<rule_audit/inverse_overseas_2026-08-31.csv>) |  |

**`viz/`**

| 문서 | 제목 |
|---|---|
| [ontology_graph_ui.html](<viz/ontology_graph_ui.html>) |  |

## 7. 기술제안서

제출한 기술제안서의 절별 원고와 작성 과정입니다.

**`proposal/`**

| 문서 | 제목 |
|---|---|
| [NUMBERS.md](<proposal/NUMBERS.md>) | 📊 제안서 수치 — 단일 출처 (GENERATED) |
| [README.md](<proposal/README.md>) | 📄 기술 제안서 자료실 |
| [STALE_NUMBERS_20260826.md](<proposal/STALE_NUMBERS_20260826.md>) | ⚠️ `proposal_data_pipeline_section.md` 수치 정정 요청 (이병철, 2026-08-26) |
| [ontology_3layers_frame_2026-08-31.md](<proposal/ontology_3layers_frame_2026-08-31.md>) | §02-② 서술 프레임 — 온톨로지 3층 (R-10, 리드 2026-08-31) |
| [ontology_engineering_etf.md](<proposal/ontology_engineering_etf.md>) | 기술 제안서 §02-② 온톨로지 엔지니어링 — ETF 트랙 원고 |

| 문서 | 제목 |
|---|---|
| [proposal_data_pipeline_section.md](<proposal_data_pipeline_section.md>) | 기술 제안서 — §데이터 파이프라인 (초안 2026-08-25) |

**`기술제안서/`**

| 문서 | 제목 |
|---|---|
| [00_README.md](<기술제안서/00_README.md>) | 📄 기술 제안서 원고 폴더 |
| [01_작성방향_분담.md](<기술제안서/01_작성방향_분담.md>) | 기술 제안서 작성 방향 — 6대 목차 × 온톨로지/KG × 3인 도메인 분담 (2026-09-02) |
| [02_목차.md](<기술제안서/02_목차.md>) | 기술 제안서 목차 — 온톨로지·KG 중심 압축판 (2026-09-03 개정) |
| [03_구성도_설계.md](<기술제안서/03_구성도_설계.md>) | 온톨로지 구성도 설계 — 도메인 3장이 공통 1장으로 합쳐지는 그림 (2026-09-02) |
| [04_도메인_채권.md](<기술제안서/04_도메인_채권.md>) | 도메인 원고 — 국내채권 (담당: 채권) — 1차 완료 2026-09-03 |
| [05_도메인_ETF.md](<기술제안서/05_도메인_ETF.md>) | 도메인 원고 템플릿 — ETF 국내·해외 (담당: ETF) |
| [06_도메인_펀드.md](<기술제안서/06_도메인_펀드.md>) | 도메인 원고 템플릿 — 공모펀드 (담당: 리드) |
| [07_리드_공통절.md](<기술제안서/07_리드_공통절.md>) | 리드 공통절 뼈대 — 0 · 01 · 2.2.1 · 2.2.5 · 2.3 · 03 · 4.4 (담당: 리드) |
| [08_설계철학.md](<기술제안서/08_설계철학.md>) | 설계 철학 — 선행연구 반영 확정본 (2026-09-03 저녁) |
| [09_오답유형_구조해법.md](<기술제안서/09_오답유형_구조해법.md>) | 오답 유형 → 구조적 해법 — "축 사전"으로 편입 기준을 한 줄 넓힌다 (2026-09-03) |
| [10_흐름도_취합.md](<기술제안서/10_흐름도_취합.md>) | 04장 주요 기능 흐름도 — 취합본 (담당: 채권 · 1차 2026-09-03) |
| [11_기대효과_확장성.md](<기술제안서/11_기대효과_확장성.md>) | 05장 기대효과 · 확장성 — 초안 (담당: 채권 · 1차 2026-09-03) |
| [12_리드_원고초안.md](<기술제안서/12_리드_원고초안.md>) | 리드 원고 초안 — 0 · 01 · 2.2.1 · 2.2.5 · 2.3 · 03 · 4.4 · 펀드 §B~§D (2026-09-03) |
| [13_데이터절_통합.md](<기술제안서/13_데이터절_통합.md>) | 2.1 특화 데이터 수집·정제 — 통합본 (생성 2026-09-04 · scripts/assemble_proposal.py) |
| [14_부록_취합.md](<기술제안서/14_부록_취합.md>) | 부록 A·B·C — 취합본 (생성 2026-09-04 · scripts/assemble_proposal.py) |
| [15_주최QA_반영점검.md](<기술제안서/15_주최QA_반영점검.md>) | 주최 Q&A ↔ 제안서 반영 점검표 (2026-09-04 · 병철) |
| [16_ETF_본문원고.md](<기술제안서/16_ETF_본문원고.md>) | ETF 파트 본문 원고 — Data → EDA → 온톨로지·KG → SQL → 답변 (2026-09-04 · 병철) |
| [17_구축과정_ETF.md](<기술제안서/17_구축과정_ETF.md>) | 온톨로지·KG 구축 과정 — ETF (2026-09-04 · 병철) |
| [18_구축과정_채권_초안.md](<기술제안서/18_구축과정_채권_초안.md>) | 구축 과정 — 국내채권 (초안 · 2026-09-04) |
| [19_구축과정_ETF_흐름판_초안.md](<기술제안서/19_구축과정_ETF_흐름판_초안.md>) | 구축 과정 — ETF 국내·해외 (흐름판 초안 · 2026-09-04) |
| [20_구축과정_펀드_초안.md](<기술제안서/20_구축과정_펀드_초안.md>) | 구축 과정 — 공모펀드 (초안 · 2026-09-04) |
| [21_테크세션_벤치마크_반영점검.md](<기술제안서/21_테크세션_벤치마크_반영점검.md>) | 🎯 테크세션·수상작 벤치마크 반영 점검 (2026-09-04 · 병철) |
| [22_기대효과_정량화_재료.md](<기술제안서/22_기대효과_정량화_재료.md>) | 📊 §5 기대효과·확장성 — 정량화 재료 (2026-09-04 · 병철 → 11 작성자) |
| [23_설명회_전사_반영점검.md](<기술제안서/23_설명회_전사_반영점검.md>) | 🎙️ 오프라인 설명회 전사 반영 점검 (2026-09-04 · 병철) |
| [24_확장성_구조분석.md](<기술제안서/24_확장성_구조분석.md>) | 🧩 확장성 — 이 구조가 다른 데이터에도 그대로 가는가 (2026-09-04 · 병철) |
| [25_문서_명세서.md](<기술제안서/25_문서_명세서.md>) | 저장소 파일 명세서 — 무엇을 남기고 무엇을 정리하는가 (2026-09-04 작성 · **2026-09-06 16:40 재계수** · 병철) |
| [26_ETF_최종원고.md](<기술제안서/26_ETF_최종원고.md>) | 2.2.3 온톨로지 엔지니어링 — ETF 국내·해외 |
| [27_기술제안서_ETF판_전체원고.md](<기술제안서/27_기술제안서_ETF판_전체원고.md>) | 기술 제안서 — ETF 도메인 (국내·해외) |
| [28_채권_최종원고.html](<기술제안서/28_채권_최종원고.html>) |  |
| [28_채권_최종원고.md](<기술제안서/28_채권_최종원고.md>) | 기술 제안서 — 국내채권 도메인 |
| [28_채권_최종원고.pdf](<기술제안서/28_채권_최종원고.pdf>) |  |
| [29_최종제출_명세서.md](<기술제안서/29_최종제출_명세서.md>) | 최종 제출 명세서 — 주최 저장소(fin-120)에 올릴 것 (2026-09-07 · 트리플에이치) |
| [ETF_오답_마스터기록.md](<기술제안서/ETF_오답_마스터기록.md>) | 🧾 ETF 트랙 — 오답 마스터 기록 (라운드 누적) |
| [ETF_오답기록_2026-09-03.md](<기술제안서/ETF_오답기록_2026-09-03.md>) | 🧾 ETF 트랙 — 테스트 문항·오답 기록 (기계 생성 2026-09-03 · 병철) |
| [ETF_재투입_리스트_2026-09-06.md](<기술제안서/ETF_재투입_리스트_2026-09-06.md>) | ETF 재투입 문항 — 재배포 서버 검증용 (2026-09-06) |
| [ETF_초안완료_전달_2026-09-03.md](<기술제안서/ETF_초안완료_전달_2026-09-03.md>) | 📮 ETF 초안 완료 — 형·서현 전달 (2026-09-03 · 병철) |
| [ETF_튜닝문항_20_2026-09-05.md](<기술제안서/ETF_튜닝문항_20_2026-09-05.md>) | 🎯 ETF 튜닝 문항 20 — 정답표 포함 (2026-09-05) |
| [서버점검_미검증_질문유형.md](<기술제안서/서버점검_미검증_질문유형.md>) | 서버 점검 — 아직 안 던져 본 질문 유형 (ETF 트랙 인계) |
| [예상질문_15문항_2026-09-04.md](<기술제안서/예상질문_15문항_2026-09-04.md>) | 🎯 예상 질문 15문항 (2026-09-04) — 약점 · 미시험 영역 · 채점자 시선 |
| [채권_오답기록_2026-09-03.md](<기술제안서/채권_오답기록_2026-09-03.md>) | 국내채권 테스트문항 오답 기록 — 질문 → 오답 → 원인 → 수정 → 현재 상태 (2026-08-29 ~ 09-04) |
| [채권_점검문항_10_2026-09-05.md](<기술제안서/채권_점검문항_10_2026-09-05.md>) | 채권 — 전수조사 직전 서버 점검 10문항 (2026-09-05) |
| [채권_필요파일.md](<기술제안서/채권_필요파일.md>) | 채권 파트 필요 파일 명세서 — yaml 부터 챗봇까지 (2026-09-04) |
| [채권_회신_2026-09-03.md](<기술제안서/채권_회신_2026-09-03.md>) | 국내채권 도메인 — 기술제안서 (2026-09-04 초안 · 2026-09-05 7차 재실측 = **병합용 최종본** · 채권 담당) |
| [최종점검_30문항_2026-09-04.md](<기술제안서/최종점검_30문항_2026-09-04.md>) | 🎯 최종 성능 점검 30문항 (2026-09-04 · 병철) |
| [최종점검_채점기록_2026-09-04.md](<기술제안서/최종점검_채점기록_2026-09-04.md>) | 최종 점검 채점 기록 — 2026-09-04 (ETF 트랙) |
| [최종제출_체크리스트_2026-09-06.md](<기술제안서/최종제출_체크리스트_2026-09-06.md>) | 최종 제출 체크리스트 (2026-09-06 · 트리플에이치) |
| [펀드_회신_2026-09-03.md](<기술제안서/펀드_회신_2026-09-03.md>) | 📮 펀드 §A·§E 회신 — 병철 앞 (2026-09-03 · 리드) |

**`기술제안서/figures/`**

| 문서 | 제목 |
|---|---|
| [fig1_three_layers.svg](<기술제안서/figures/fig1_three_layers.svg>) |  |
| [fig2_missing_types.svg](<기술제안서/figures/fig2_missing_types.svg>) |  |
| [fig3_bond_entities.svg](<기술제안서/figures/fig3_bond_entities.svg>) |  |
| [fig4_pipeline.svg](<기술제안서/figures/fig4_pipeline.svg>) |  |
| [fig5_timeline.svg](<기술제안서/figures/fig5_timeline.svg>) |  |
| [fig6_defense_layers.svg](<기술제안서/figures/fig6_defense_layers.svg>) |  |

## 8. 검토·질의응답 기록

데이터·규칙 검토표, 주최 측 Q&A 정리, 정답지 검증 기록입니다.

| 문서 | 제목 |
|---|---|
| [QNA_REVIEW_2026-08-25.md](<QNA_REVIEW_2026-08-25.md>) | 📮 주최 Q&A 검토 — 2026-08-25 |
| [answer_quality_by_type_2026-09-03.md](<answer_quality_by_type_2026-09-03.md>) | 공모펀드 챗봇 — 유형별 답변 품질 (15R · 2026-09-03) |
| [etf_domain_check_2026-08-26.md](<etf_domain_check_2026-08-26.md>) | 🔍 ETF 도메인 전수 점검 — 값·결측 의미 → 온톨로지·KG 반영 확인 (이병철, 2026-08-26) |
| [etf_v2_recheck_2026-08-25.md](<etf_v2_recheck_2026-08-25.md>) | 🔁 ETF 검토(E1~E7) 2차 데이터 재점검 + 회의 준비 — 이병철 2026-08-25 |
| [eval_gold_verify_cross_official_2026-08-26.md](<eval_gold_verify_cross_official_2026-08-26.md>) | 🥇 gold 63문항 — 교차/공식예시 17문항 검증 (이병철, 2026-08-26) |
| [eval_gold_verify_etf_2026-08-26.md](<eval_gold_verify_etf_2026-08-26.md>) | 🥇 gold 63문항 검증 — ETF 담당분 46문항 (이병철, 2026-08-26) |
| [gold_defects_2026-09-03.md](<gold_defects_2026-09-03.md>) | gold 결함으로 **판정 보류**하는 문항 — 2026-09-03 |
| [gold_review_2026-09-01.md](<gold_review_2026-09-01.md>) | 🔍 gold 판단 검토 시트 — 사람 눈이 필요한 13건 (2026-09-01 · 병철 작성) |
| [qna_discord_2026-08-31.md](<qna_discord_2026-08-31.md>) | 📮 주최 디스코드 Q&A 대조 — 신규분 (2026-08-31 · 병철) |
| [question_design_public_funds_2026-08-31.md](<question_design_public_funds_2026-08-31.md>) | 공모펀드 질문 설계 — 카테고리 지도와 신규 문항 초안 (2026-08-31) |
| [review_codebook_2026-08-25.md](<review_codebook_2026-08-25.md>) | 🧾 운용사 코드북 웹 검수 — 2026-08-25 |
| [review_index_edges_2026-08-25.md](<review_index_edges_2026-08-25.md>) | 🔎 검수 B — Index→Region / AssetClass 규칙 edge 검수 (2026-08-25) |
| [review_recheck_2026-08-25.md](<review_recheck_2026-08-25.md>) | 🔁 검토지시서 재검증 결과 — 2차 데이터(2026-08-22) 기준 · 2026-08-25 |
| [review_reply_bonds_2026-08-21.md](<review_reply_bonds_2026-08-21.md>) | 🙋 채권 B1~B9 검토 답글 — `review_request_2026-08-20.md` 대응 |
| [review_reply_etf_2026-08-21.md](<review_reply_etf_2026-08-21.md>) | 💬 검토 답글 — ETF E1~E7 (이병철, 2026-08-21) |
| [review_request_2026-08-20.md](<review_request_2026-08-20.md>) | 🙋 팀 검토 요청 — 반영 완료된 규칙 전수 검토 (채권 · ETF · 국내펀드) 2026-08-20 |
| [review_yaml_pending_2026-08-25.md](<review_yaml_pending_2026-08-25.md>) | 검수 C — enums yaml "추정 · 미확정 · 보류 · workshop" 항목 판정 (2026-08-25) |

**`review_2026-08-26/`**

| 문서 | 제목 |
|---|---|
| [A_정합성.md](<review_2026-08-26/A_정합성.md>) | A. 데이터 정합성 |
| [B_피처의미.md](<review_2026-08-26/B_피처의미.md>) | B. 피처 의미 |
| [C_결측의미.md](<review_2026-08-26/C_결측의미.md>) | C. 결측치 의미 |
| [D_온톨로지관계.md](<review_2026-08-26/D_온톨로지관계.md>) | D. 온톨로지 관계 |
| [ETF_검토기록_2026-08-27.md](<review_2026-08-26/ETF_검토기록_2026-08-27.md>) | 📝 ETF 검토 작업 기록 — 2026-08-27 (Leebyungchul · 에이전트 동반 검토) |
| [E_지식그래프.md](<review_2026-08-26/E_지식그래프.md>) | E. 지식그래프 |
| [README.md](<review_2026-08-26/README.md>) | 🔎 온톨로지 · 지식그래프 검토 채움표 |
| [약점프로브_2026-09-01.md](<review_2026-08-26/약점프로브_2026-09-01.md>) | 약점 프로브 16문항 — 가드 없는 영역 탐색 (2026-09-01) |
| [에이전트검토_프롬프트.md](<review_2026-08-26/에이전트검토_프롬프트.md>) | 🤖 에이전트와 함께 검토하기 — 지시서(프롬프트) |
| [작성법.md](<review_2026-08-26/작성법.md>) | ✍️ 검토 채움표 작성법 |
| [재실측_체크리스트_2026-09-01.md](<review_2026-08-26/재실측_체크리스트_2026-09-01.md>) | 재배포 후 재실측 체크리스트 (2026-09-01) |
| [전체데이터_검수_2026-08-31.md](<review_2026-08-26/전체데이터_검수_2026-08-31.md>) | 전체 데이터 검수 — 2026-08-31 (DB 14테이블 전수) |
| [종류분류_전수조사_2026-08-31.md](<review_2026-08-26/종류분류_전수조사_2026-08-31.md>) | 🔍 종류·분류 축 전수조사 — 2026-08-31 ('A등급 이상 회사채' 사고 후속) |
| [채권_검토기록_2026-08-27.md](<review_2026-08-26/채권_검토기록_2026-08-27.md>) | 📝 채권 검토 작업 기록 — 2026-08-27 (seohyun · 에이전트 동반 검토) |
| [채권_규칙_원문_2026-08-30.md](<review_2026-08-26/채권_규칙_원문_2026-08-30.md>) | 채권 query_rules 원문(압축 전) — 2026-08-30 밤 I 작업 |
| [채권_재점검_2026-08-30_밤.md](<review_2026-08-26/채권_재점검_2026-08-30_밤.md>) | 채권 재점검 — 챗봇(HCX) 실측 직전 전수 재현 (2026-08-30 밤) |
| [채권_전수조사_2026-08-30.md](<review_2026-08-26/채권_전수조사_2026-08-30.md>) | 🔍 채권 전수 조사 — 2026-08-30 (챗봇 직접 테스트 전 점검) |
| [채권_프로브10_실측_2026-08-31_밤.md](<review_2026-08-26/채권_프로브10_실측_2026-08-31_밤.md>) | 채권 프로브 10문항 — 서버 실측 기록 (2026-08-31 밤) |
| [채권_프로브15_2026-08-30.md](<review_2026-08-26/채권_프로브15_2026-08-30.md>) | 채권 프로브 15문항 — HCX 실측 1라운드 (2026-08-30) |

**`review_2026-09-02/`**

| 문서 | 제목 |
|---|---|
| [온톨로지_yaml_전수재검증_2026-09-02.md](<review_2026-09-02/온톨로지_yaml_전수재검증_2026-09-02.md>) | 온톨로지·yaml 전수 재검증 — 2026-09-02 (2차 DB 기준일 2026-08-22) |
| [한전_삼성전자_실측_수정계획_2026-09-02.md](<review_2026-09-02/한전_삼성전자_실측_수정계획_2026-09-02.md>) | 한전 수익률 순 · 삼성전자 발행채권 — 답변·SQL 실측 판정과 수정 계획 (2026-09-02) |

## 9. 검증 라운드 기록 (과정)

질의응답 품질을 라운드별로 점검하고 고친 기록입니다. 일부는 테스트 코드가 직접 읽으므로 위치를 옮기면 안 됩니다.

| 문서 | 제목 |
|---|---|
| [bond_hard5_fix_plan_2026-09-05.md](<bond_hard5_fix_plan_2026-09-05.md>) | 채권 난이도 상 5문항 — 서버 실측 판정과 수리 계획 (2026-09-05) |
| [bonds_2026-09-06_round1.md](<bonds_2026-09-06_round1.md>) | 국내채권 QA 라운드 1 — 2026-09-06 (서버 db17e07 · 로컬 98414b3) |
| [bonds_2026-09-06_round1_plan.md](<bonds_2026-09-06_round1_plan.md>) | 채권 QA r1 수리 계획 — 간섭 지도 (에이전트 A · 2026-09-06 · 브랜치 qa/bonds-r1) |
| [bonds_latency_analysis_2026-09-06.md](<bonds_latency_analysis_2026-09-06.md>) | 채권 QA r1 응답 시간 분석 — 원인 확정과 줄이는 방법 (2026-09-06) |
| [exp_port_guards_2026-09-06.md](<exp_port_guards_2026-09-06.md>) | 펀드 결정층 기법의 ETF·채권 이식 실험 — 2026-09-06 |
| [funds_core34_2026-09-06.md](<funds_core34_2026-09-06.md>) | 공모펀드 핵심 34문항 — 프리즈 전 최종 점검 (2026-09-06) |
| [funds_defects_2026-09-04.md](<funds_defects_2026-09-04.md>) | 🔧 결함 분류 — 5차(최종) 기준 |
| [funds_domain_axes_2026-09-04.md](<funds_domain_axes_2026-09-04.md>) | 공모펀드 도메인 축 신설 문항 13건 — 기대 답변 · 2026-09-04 |
| [funds_final_review_2026-09-06.md](<funds_final_review_2026-09-06.md>) | 공모펀드 도메인 — 프리즈 최종 검토 (2026-09-06) |
| [funds_ontology_fix_plan_2026-09-04.md](<funds_ontology_fix_plan_2026-09-04.md>) | 공모펀드 78문항 → 최종 온톨로지 수정 계획 — 2026-09-04 |
| [funds_repairs_2026-09-04.md](<funds_repairs_2026-09-04.md>) | 🔧 수리 기록 — 온톨로지·KG 층 (전수조사 진행분) |
| [funds_structural_causes_2026-09-04.md](<funds_structural_causes_2026-09-04.md>) | 실패 25건의 구조 원인 — 온톨로지·KG 층위 진단 (2026-09-04 2차 기준) |
| [funds_submit_check20_2026-09-06.md](<funds_submit_check20_2026-09-06.md>) | 공모펀드 제출 전 필수 점검 20문항 — 모범 답안·채점표 (2026-09-06) |
| [funds_test_result_2026-09-04.md](<funds_test_result_2026-09-04.md>) (`eval/render_funds_report.py` 생성물) | 공모펀드 78문항 테스트 결과 — 2026-09-04 |
| [gold_probe_2026-09-03_g1.md](<gold_probe_2026-09-03_g1.md>) | G1 라운드 — gold 초회 실측 채점 (2026-09-03) |
| [gold_probe_2026-09-03_g2.md](<gold_probe_2026-09-03_g2.md>) | G2 (9R) — gold·주최샘플·교차 계열 재채점 (2026-09-03) |
| [gold_probe_2026-09-03_g3.md](<gold_probe_2026-09-03_g3.md>) | gold·주최샘플·교차환각 11R 판정 — 2026-09-03 (g3) |
| [gold_probe_2026-09-03_g4.md](<gold_probe_2026-09-03_g4.md>) | gold·주최샘플·교차환각 13R 판정 — 2026-09-03 (g4) |
| [gold_probe_2026-09-03_g5.md](<gold_probe_2026-09-03_g5.md>) | gold·주최샘플·교차환각 15R 판정 — 2026-09-03 (g5) |
| [kg_structure_loop_2026-09-02.md](<kg_structure_loop_2026-09-02.md>) | KG 구조 검증 실측 기록 — 2026-09-02 (35 + 형제 X25) |
| [kg_structure_probe_design_2026-09-02.md](<kg_structure_probe_design_2026-09-02.md>) | 온톨로지·KG 구조 검증 문항 설계 — 2026-09-02 |
| [kg_structure_probe_round1_2026-09-02.md](<kg_structure_probe_round1_2026-09-02.md>) | 온톨로지·KG 구조 검증 35문항 — 서버 기준선(31e72ef) 채점 1R — 2026-09-02 |
| [kg_structure_probe_round2_2026-09-02.md](<kg_structure_probe_round2_2026-09-02.md>) | 온톨로지·KG 구조 검증 35문항 — 2라운드 서버 실측(6bad723) 채점 — 2026-09-02 |
| [kg_structure_probe_round3_2026-09-02.md](<kg_structure_probe_round3_2026-09-02.md>) (테스트가 읽음) | 온톨로지·KG 구조 검증 60문항 — 3라운드 서버 실측(1e0e641) 채점 + 수렴 판정 — 2026-09-02 |
| [kg_structure_probe_round4_2026-09-02.md](<kg_structure_probe_round4_2026-09-02.md>) | 온톨로지·KG 구조 검증 85문항 — 4라운드(6R) 서버 실측(07b2ef6) 채점 + 수렴 판정 — 2026-09-02 |
| [kg_structure_probe_round5_2026-09-03.md](<kg_structure_probe_round5_2026-09-03.md>) | KG 구조 계열 7라운드 채점 — 2026-09-03 |
| [kg_structure_probe_round6_2026-09-03.md](<kg_structure_probe_round6_2026-09-03.md>) | KG 구조 계열 9라운드 채점 (2026-09-03) — 심사관 B |
| [kg_structure_probe_round7_2026-09-03.md](<kg_structure_probe_round7_2026-09-03.md>) | KG 구조 계열 11라운드 판정 — 2026-09-03 |
| [kg_structure_probe_round8_2026-09-03.md](<kg_structure_probe_round8_2026-09-03.md>) | KG 구조 계열 8라운드 판정 (13R probe) — 2026-09-03 |
| [kg_structure_probe_round9_2026-09-03.md](<kg_structure_probe_round9_2026-09-03.md>) | KG 구조 계열 9라운드 판정 (15R probe) — 2026-09-03 |
| [recheck_2026-09-02_round1.md](<recheck_2026-09-02_round1.md>) | 재검 2026-09-02 라운드 1 — HANDOFF §1 P1 7문항 채점 (에이전트 B) |
| [recheck_2026-09-02_round1_review.md](<recheck_2026-09-02_round1_review.md>) | 재검 2026-09-02 라운드 1 — A 수리 코드 리뷰 (에이전트 B · 배포 전) |
| [recheck_2026-09-02_round2.md](<recheck_2026-09-02_round2.md>) | 재검 2026-09-02 라운드 2 — 수리 배포(31e72ef) 후 서버 실측 19문항 채점 (에이전트 B) |
| [recheck_2026-09-02_round3.md](<recheck_2026-09-02_round3.md>) | 재검 2026-09-02 라운드 3 — 수리 배포(e56767d) 후 서버 실측 33문항 채점 (에이전트 B) |
| [recheck_2026-09-02_round4.md](<recheck_2026-09-02_round4.md>) | 재검 2026-09-02 라운드 4 — 수리 배포(6bad723) 후 서버 실측 재검 계열 49문항 채점 (에이전트 B) |
| [recheck_2026-09-02_round5.md](<recheck_2026-09-02_round5.md>) (테스트가 읽음) | 재검 2026-09-02 라운드 5 — 수리 배포(1e0e641) 후 서버 실측 재검 계열 61문항 채점 + 수렴 판정 (에이전트 B) |
| [recheck_2026-09-02_round6.md](<recheck_2026-09-02_round6.md>) | 재검 2026-09-02 라운드 6 — 6R 수리 배포(07b2ef6) 후 재검 계열 77문항 채점 + 프리즈 판정 (에이전트 B) |
| [recheck_2026-09-02_round6_plan.md](<recheck_2026-09-02_round6_plan.md>) | 6라운드 수리 계획 — 간섭 지도 먼저 (에이전트 A · 2026-09-02) |
| [recheck_2026-09-02_round7_plan.md](<recheck_2026-09-02_round7_plan.md>) | 7R 수리 간섭 지도 — 재검 §③(M′·R′·S′·P′·B-4′) + KG §③(G1~G7·F3) |
| [recheck_2026-09-03_round10_plan.md](<recheck_2026-09-03_round10_plan.md>) | 10R 수리 간섭 지도 — 2026-09-03 |
| [recheck_2026-09-03_round11.md](<recheck_2026-09-03_round11.md>) | 재검 계열 11라운드 채점 — 2026-09-03 |
| [recheck_2026-09-03_round12_plan.md](<recheck_2026-09-03_round12_plan.md>) | 12라운드 수리 간섭 지도 — 2026-09-03 |
| [recheck_2026-09-03_round13.md](<recheck_2026-09-03_round13.md>) | 재검 계열 13라운드 채점 — 2026-09-03 |
| [recheck_2026-09-03_round14_plan.md](<recheck_2026-09-03_round14_plan.md>) | 14라운드 수리 간섭 지도 — 2026-09-03 |
| [recheck_2026-09-03_round15.md](<recheck_2026-09-03_round15.md>) | 재검 계열 15라운드 채점 — 2026-09-03 |
| [recheck_2026-09-03_round16_plan.md](<recheck_2026-09-03_round16_plan.md>) | 16R 수리 계획 — 간섭 지도 (2026-09-03) |
| [recheck_2026-09-03_round17.md](<recheck_2026-09-03_round17.md>) | 17R 서버 실측 — enforce 슬롯 P0 3종 전환 후 (2026-09-03) |
| [recheck_2026-09-03_round7.md](<recheck_2026-09-03_round7.md>) | 재검 2026-09-03 라운드 7 — 7R 수리 배포(`aaf7864`) 후 재검 계열 93문항 채점 (에이전트 B) |
| [recheck_2026-09-03_round8_plan.md](<recheck_2026-09-03_round8_plan.md>) | 8라운드 수리 — 간섭 지도 (2026-09-03) |
| [recheck_2026-09-03_round9.md](<recheck_2026-09-03_round9.md>) | 재검 계열 9라운드 채점 — 2026-09-03 |
| [recheck_loop_2026-09-02.md](<recheck_loop_2026-09-02.md>) (`eval/render_probe_md.py` 생성물) | 재검 루프 실측 기록 — 2026-09-02 (원 7 + 형제 12/14/16/12) |
| [채권_수리계획_종목지시자_2026-09-06.md](<채권_수리계획_종목지시자_2026-09-06.md>) | 채권 수리 계획 — 종목 지시자 · 되묻기 전제 (사고 #97~#100) |
| [채권_온톨로지_전수조사_2026-09-05.md](<채권_온톨로지_전수조사_2026-09-05.md>) | 채권 온톨로지·SQL 전수조사 (2026-09-05) |

## 10. 인수인계·계획·회의 (과정)

날짜별 인수인계, 진행 상황, 작업 계획, 회의록입니다.

| 문서 | 제목 |
|---|---|
| [EXPERIMENT_LOOP.md](<EXPERIMENT_LOOP.md>) | 🔁 실험 루프 — 챗봇으로 관찰하고 온톨로지를 고친다 |
| [HANDOFF_2026-08-18.md](<HANDOFF_2026-08-18.md>) | 📦 인수인계 — 2026-08-18 (jeonghyeon 세션) |
| [HANDOFF_2026-08-20.md](<HANDOFF_2026-08-20.md>) | 🤝 세션 인수인계 — 2026-08-20 (외부 수집 완료 · 팀 검토 착수) |
| [HANDOFF_2026-08-25.md](<HANDOFF_2026-08-25.md>) | 🤝 세션 인수인계 — 2026-08-25 (2차 데이터 전환 · KG 구축 · 검수 완료) |
| [HANDOFF_2026-08-27.md](<HANDOFF_2026-08-27.md>) | 🤝 세션 인수인계 — 2026-08-27 (챗봇 가동 · 브랜치 통합 · 서버 실배포) |
| [HANDOFF_2026-08-30.md](<HANDOFF_2026-08-30.md>) | 🤝 세션 인수인계 — 2026-08-30 (펀드 식별자 결측 축 정비 · ETF 브랜치 병합) |
| [HANDOFF_2026-08-31.md](<HANDOFF_2026-08-31.md>) | 🤝 세션 인수인계 — 2026-08-31 (KG 후손 탐색 · 펀드 규칙 정비 · 3도메인 삼각 대조) |
| [HANDOFF_2026-09-01.md](<HANDOFF_2026-09-01.md>) | 🤝 세션 인수인계 — 2026-09-01 (병렬 4세션 통합) |
| [HANDOFF_2026-09-02.md](<HANDOFF_2026-09-02.md>) | 🤝 세션 인수인계 — 2026-09-02 (펀드 채점 루프 완주 + 결정층 수리 18종) |
| [HANDOFF_2026-09-02_pm.md](<HANDOFF_2026-09-02_pm.md>) | 🤝 세션 인수인계 — 2026-09-02 오후 (A↔B 재검 루프 5라운드 + KG 구조 검증 3라운드 + 팀원 전부 merge·배포) |
| [HANDOFF_2026-09-03_proposal.md](<HANDOFF_2026-09-03_proposal.md>) | 🤝 세션 인수인계 — 2026-09-03 제안서 트랙 (제출물 정리 → 목차·분담 → 도메인 템플릿 → 폴더 신설) |
| [HANDOFF_2026-09-03_qa_loop.md](<HANDOFF_2026-09-03_qa_loop.md>) | 🤝 인계 — 공모펀드 QA 루프 (2026-09-03) |
| [HANDOFF_2026-09-03_review_proposal.md](<HANDOFF_2026-09-03_review_proposal.md>) | 🤝 인수인계 — 코드 검토 · 보고서 역할 (2026-09-03 저녁) |
| [HANDOFF_2026-09-04_runtime.md](<HANDOFF_2026-09-04_runtime.md>) | 인수인계 — 런타임 트랙 (규칙 전달 감사 → enforce 슬롯 → 17R) · 2026-09-04 |
| [HANDOFF_2026-09-06_funds.md](<HANDOFF_2026-09-06_funds.md>) | 인수인계 — 공모펀드 트랙 · 2026-09-04 ~ 09-06 (프리즈) |
| [HANDOFF_ETF_2026-08-29.md](<HANDOFF_ETF_2026-08-29.md>) | 📌 ETF 트랙 기준선 — 현재 상태 한 장 요약 (2026-08-29) |
| [NEXT_STEPS.md](<NEXT_STEPS.md>) | 🎯 다음 작업 지시서 — 온톨로지 워크샵까지 (팀 배포용) |
| [OUT_OF_BAND_CONTEXT_2026-08-29.md](<OUT_OF_BAND_CONTEXT_2026-08-29.md>) | 📎 저장소 밖 맥락 — 대화·PDF·디스코드·이미지로만 전달된 정보 |
| [PENDING_DECISIONS_ETF.md](<PENDING_DECISIONS_ETF.md>) | ⏸ 보류된 결정 — ETF 트랙 (상의 대기) |
| [PLAN_2026-08-29.md](<PLAN_2026-08-29.md>) | 🗓️ 잔여 8일 구현 계획 — 2026-08-29 (D-8) |
| [PROGRESS_2026-08-18.md](<PROGRESS_2026-08-18.md>) | 📆 진행상황 — 2026-08-18 미래에셋 웹 수집 사이클 |
| [PROGRESS_2026-08-20.md](<PROGRESS_2026-08-20.md>) | 📓 작업일지 — 2026-08-20 |
| [TEAM_WORKFLOW.md](<TEAM_WORKFLOW.md>) | 👥 팀 실험 → 수정 → 반영 (팀원용) |
| [WORK_PLAN_2026-08-26.md](<WORK_PLAN_2026-08-26.md>) | 🧭 작업 계획서 — 2026-08-26 |
| [ask_lead_2026-08-28.md](<ask_lead_2026-08-28.md>) | 🙋 리드 확인 요청 — ETF 검토 완료 보고 + 확답 필요 4건 (이병철, 2026-08-28) |
| [ask_lead_2026-08-31.md](<ask_lead_2026-08-31.md>) | 🙋 리드 확인 요청 — ETF 미해결 6건 (이병철, 2026-08-31) |
| [ask_lead_2026-08-31_reply.md](<ask_lead_2026-08-31_reply.md>) | ✅ 리드 확답 — ETF 미해결 6건 (2026-08-31 · ask_lead_2026-08-31.md (ask_lead_2026-08-31.md) 답글) |
| [handoff_funds_runtime_2026-09-05.md](<handoff_funds_runtime_2026-09-05.md>) | 인계 — 공모펀드 런타임 트랙 (18R) · 2026-09-05 |
| [meeting_2026-08-29.md](<meeting_2026-08-29.md>) | 🗣 회의 기록 — 2026-08-29 (온라인) |
| [meeting_agenda_2026-08-26.md](<meeting_agenda_2026-08-26.md>) | 🗳️ 회의 안건 — 2026-08-26 (D-11) · HCX 플래너 연결 · 제안서 온톨로지 설계 절 |
| [workshop_agenda_2026-08-18.md](<workshop_agenda_2026-08-18.md>) | 🗳️ 워크샵 안건 통합 — 2026-08-18 기준 |
| [클로드정리_2026-08-30.md](<클로드정리_2026-08-30.md>) | 🔁 클로드 정리 — 2026-08-29 ~ 08-30 (채권 담당 seohyun) |

## 11. 선행연구·설계 스펙

참고한 논문 노트와 초기 설계 스펙입니다.

**`research/`**

| 문서 | 제목 |
|---|---|
| [KG_온톨로지_설계_인사이트_2026-08-30.md](<research/KG_온톨로지_설계_인사이트_2026-08-30.md>) | 온톨로지·KG 구축 인사이트 — 선행연구 10편에서 우리 설계로 (2026-08-30) |
| [TASK_CONTEXT_2026-08-30.md](<research/TASK_CONTEXT_2026-08-30.md>) | 선행연구 카드 작성용 과제 맥락 (2026-08-30) |
| [개선_구현_및_기대효과_2026-08-30.md](<research/개선_구현_및_기대효과_2026-08-30.md>) | 개선 구현 및 기대효과 — 2026-08-30 |
| [선행연구_종합_2026-08-30.md](<research/선행연구_종합_2026-08-30.md>) | 선행연구 종합 — "어떤 관계를 잡아야 답을 잘하나, 관계 외에 무엇을 봐야 하나" (2026-08-30) |
| [온톨로지_개정안_2026-08-30.md](<research/온톨로지_개정안_2026-08-30.md>) | 온톨로지·KG 개정안 — 선행연구 인사이트로 현 구축물·계획을 대조 (2026-08-30) |

**`research/notes/`**

| 문서 | 제목 |
|---|---|
| [2025-winner-benchmark.md](<research/notes/2025-winner-benchmark.md>) | 2025(9회) 대상작 벤치마크 — "기술적 분석 특화 금융 에이전트" |
| [2410.09244_progressive-ontology-reveal.md](<research/notes/2410.09244_progressive-ontology-reveal.md>) |  ONT-1 Using off-the-shelf LLMs to query enterprise data by progressively revealing ontolo |
| [2505.18363_schemagraphsql-fk-pathfinding.md](<research/notes/2505.18363_schemagraphsql-fk-pathfinding.md>) |  SCH-1 SchemaGraphSQL: Efficient Schema Linking with Pathfinding Graph Algorithms for Text |
| [2506.07245_sde-sql-value-retrieval.md](<research/notes/2506.07245_sde-sql-value-retrieval.md>) |  VAL-1 SDE-SQL: Enhancing Text-to-SQL Generation in Large Language Models via Self-Driven  |
| [2507.04127_byokg-rag.md](<research/notes/2507.04127_byokg-rag.md>) |  KGQA-1 BYOKG-RAG: Multi-Strategy Graph Retrieval for Knowledge Graph Question Answering |
| [2510.02394_domain-knowledge-retrieval-text2sql.md](<research/notes/2510.02394_domain-knowledge-retrieval-text2sql.md>) |  DK-1 Retrieval and Augmentation of Domain Knowledge for Text-to-SQL Semantic Parsing |
| [2601.10398_latent-refusal-text2sql.md](<research/notes/2601.10398_latent-refusal-text2sql.md>) |  REF-1 LatentRefusal: Latent-Signal Refusal for Unanswerable Text-to-SQL Queries |
| [2606.03363_entsql-enterprise-grounding.md](<research/notes/2606.03363_entsql-enterprise-grounding.md>) |  ENT-1 EntSQL: A Benchmark for Grounding Text-to-SQL in Long-Context Enterprise Knowledge |
| [2606.22419_kg-grounding-only-out-of-training.md](<research/notes/2606.22419_kg-grounding-only-out-of-training.md>) |  KGG-1 Knowledge-Graph Grounding Helps LLMs Only for Out-of-Training Knowledge: A Controll |
| [FIBO_funds-model.md](<research/notes/FIBO_funds-model.md>) | FIBO — Collective Investment Vehicles (펀드 온톨로지 표준) |
| [INDEX.md](<research/notes/INDEX.md>) | 선행연구 노트 INDEX |
| [jamia2025_pvsql-business-context.md](<research/notes/jamia2025_pvsql-business-context.md>) |  JAMIA-1 Automating pharmacovigilance evidence generation: using LLMs to produce context-a |
| [semantic-layer-benchmark.md](<research/notes/semantic-layer-benchmark.md>) |  SL-1 Semantic Layers for Reliable LLM-Powered Data Analytics: A Paired Benchmark of Accur |

**`superpowers/specs/`**

| 문서 | 제목 |
|---|---|
| [2026-08-12-eda-notebook-missing-and-stats-design.md](<superpowers/specs/2026-08-12-eda-notebook-missing-and-stats-design.md>) | EDA 노트북 — 결측 판정 강화 + 기초 통계 절 신설 |
| [2026-08-12-ontology-design-and-roadmap.md](<superpowers/specs/2026-08-12-ontology-design-and-roadmap.md>) | 🕸️ 온톨로지 설계 & 실행 로드맵 |
| [2026-08-22-public-funds-external-data-design.md](<superpowers/specs/2026-08-22-public-funds-external-data-design.md>) | 공모펀드 외부 데이터 활용 설계 — 검증 후 선별 적재 |

## 12. 핵심문서모음 (스냅샷)

주요 문서를 한 폴더에 모아 둔 스냅샷입니다. 35개 중 8개만 원본과 동일하고 26개는 원본과 내용이 다르므로, 최신 내용은 각 원본 위치의 문서를 기준으로 봅니다.

**`핵심문서모음/`**

| 문서 | 제목 |
|---|---|
| [01_프로젝트총괄_PROJECT.md](<핵심문서모음/01_프로젝트총괄_PROJECT.md>) | 🤖 금융상품 AI Agent 구축 프로젝트 (`PROJECT.md`) |
| [02_최신인수인계_HANDOFF_2026-08-27.md](<핵심문서모음/02_최신인수인계_HANDOFF_2026-08-27.md>) | 🤝 세션 인수인계 — 2026-08-27 (챗봇 가동 · 브랜치 통합 · 서버 실배포) |
| [03_주최QNA확정_QNA_REVIEW_2026-08-25.md](<핵심문서모음/03_주최QNA확정_QNA_REVIEW_2026-08-25.md>) | 📮 주최 Q&A 검토 — 2026-08-25 |
| [04_데이터2차변화_DATA_V2_impact.md](<핵심문서모음/04_데이터2차변화_DATA_V2_impact.md>) | 📦 2차 배포 데이터(2026-08-24) 분석 — 우리 프로젝트에 미치는 영향 |
| [05_데이터가이드_DATA_GUIDE.md](<핵심문서모음/05_데이터가이드_DATA_GUIDE.md>) | 📁 `data/` · `1.금융상품/` — 데이터 설명서 |
| [06_외부데이터카탈로그_EXTERNAL_DATA.md](<핵심문서모음/06_외부데이터카탈로그_EXTERNAL_DATA.md>) | 📦 외부 수집 데이터 카탈로그 — 2026-08-20 기준 |
| [07_팀워크플로우_TEAM_WORKFLOW.md](<핵심문서모음/07_팀워크플로우_TEAM_WORKFLOW.md>) | 👥 팀 실험 → 수정 → 반영 (팀원용) |
| [08_실험루프_EXPERIMENT_LOOP.md](<핵심문서모음/08_실험루프_EXPERIMENT_LOOP.md>) | 🔁 실험 루프 — 챗봇으로 관찰하고 온톨로지를 고친다 |
| [09_배포체크리스트_DEPLOY_CHECKLIST.md](<핵심문서모음/09_배포체크리스트_DEPLOY_CHECKLIST.md>) | ☀️ 8/16 아침 — 배포 작업 체크리스트 |
| [10_공모펀드검토기록_2026-08-28.md](<핵심문서모음/10_공모펀드검토기록_2026-08-28.md>) | 📝 공모펀드 검토 작업 기록 — 2026-08-28 (에이전트 동반 검토 · 블록 ①: 식별자 계열) |
| [README.md](<핵심문서모음/README.md>) | 📚 미래에셋 금융상품 AI Agent 프로젝트 핵심 문서 모음 |

**`핵심문서모음/11_검토채움표_review_2026-08-26/`**

| 문서 | 제목 |
|---|---|
| [A_정합성.md](<핵심문서모음/11_검토채움표_review_2026-08-26/A_정합성.md>) | A. 데이터 정합성 |
| [B_피처의미.md](<핵심문서모음/11_검토채움표_review_2026-08-26/B_피처의미.md>) | B. 피처 의미 |
| [C_결측의미.md](<핵심문서모음/11_검토채움표_review_2026-08-26/C_결측의미.md>) | C. 결측치 의미 |
| [D_온톨로지관계.md](<핵심문서모음/11_검토채움표_review_2026-08-26/D_온톨로지관계.md>) | D. 온톨로지 관계 |
| [E_지식그래프.md](<핵심문서모음/11_검토채움표_review_2026-08-26/E_지식그래프.md>) | E. 지식그래프 |
| [README.md](<핵심문서모음/11_검토채움표_review_2026-08-26/README.md>) | 🔎 온톨로지 · 지식그래프 검토 채움표 |
| [작성법.md](<핵심문서모음/11_검토채움표_review_2026-08-26/작성법.md>) | ✍️ 검토 채움표 작성법 |

**`핵심문서모음/12_데이터사전_data_dictionary/`**

| 문서 | 제목 |
|---|---|
| [README.md](<핵심문서모음/12_데이터사전_data_dictionary/README.md>) | 📖 데이터 사전 — 도메인별 피처·의미·결측 판정 |
| [bonds.md](<핵심문서모음/12_데이터사전_data_dictionary/bonds.md>) | 📖 데이터 사전 — 국내채권 |
| [etf.md](<핵심문서모음/12_데이터사전_data_dictionary/etf.md>) | 📖 데이터 사전 — ETF (국내·해외) |
| [funds.md](<핵심문서모음/12_데이터사전_data_dictionary/funds.md>) | 📖 데이터 사전 — 공모펀드 |

**`핵심문서모음/13_온톨로지규칙_ontology_rules/`**

| 문서 | 제목 |
|---|---|
| [01_naming.md](<핵심문서모음/13_온톨로지규칙_ontology_rules/01_naming.md>) | 규칙 1. 지칭 정리 — 같은 것을 같다고 부르기 |
| [02_missing.md](<핵심문서모음/13_온톨로지규칙_ontology_rules/02_missing.md>) | 규칙 2. 결측 방어 — 비어 있음의 뜻을 가른다 |
| [03_external.md](<핵심문서모음/13_온톨로지규칙_ontology_rules/03_external.md>) | 규칙 3. 외부 데이터 병합 — 마스터를 고치지 않고 옆에 붙인다 |
| [04_grain.md](<핵심문서모음/13_온톨로지규칙_ontology_rules/04_grain.md>) | 규칙 4. 행 단위(grain) — `COUNT(*)` 는 종목 수가 아니다 |
| [05_population.md](<핵심문서모음/13_온톨로지규칙_ontology_rules/05_population.md>) | 규칙 5. 기본 모수 — 말하지 않은 조건을 고정한다 |
| [06_derivation.md](<핵심문서모음/13_온톨로지규칙_ontology_rules/06_derivation.md>) | 규칙 6. 파생·유도 — 없는 축을 규칙으로 만든다 |
| [07_disjoint.md](<핵심문서모음/13_온톨로지규칙_ontology_rules/07_disjoint.md>) | 규칙 7. 배타·분리 — 한 축에 놓으면 안 되는 것들 |
| [08_unit.md](<핵심문서모음/13_온톨로지규칙_ontology_rules/08_unit.md>) | 규칙 8. 단위·스케일 — 같은 이름, 다른 눈금 |
| [09_forbid.md](<핵심문서모음/13_온톨로지규칙_ontology_rules/09_forbid.md>) | 규칙 9. 금지 규칙 — 이 컬럼으로는 답하지 마라 |
| [10_absent.md](<핵심문서모음/13_온톨로지규칙_ontology_rules/10_absent.md>) | 규칙 10. 부재 선언 — 컬럼이 없다는 사실도 지식이다 |
| [11_hierarchy.md](<핵심문서모음/13_온톨로지규칙_ontology_rules/11_hierarchy.md>) | 규칙 11. 계층 — ‘미국’ 질의가 ‘북미’ 를 포함하는가 |
| [12_asof.md](<핵심문서모음/13_온톨로지규칙_ontology_rules/12_asof.md>) | 규칙 12. 기준일·시점 — 언제 기준의 사실인가 |
| [README.md](<핵심문서모음/13_온톨로지규칙_ontology_rules/README.md>) | 🧱 온톨로지 규칙 12종 — 규칙별 검토 문서 |
