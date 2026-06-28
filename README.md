# PlotScope 공개 포트폴리오 / Case Study

이 repository는 **PlotScope**의 공개용 근거 자료와 case study를 정리한 포트폴리오 repository입니다.

PlotScope의 실제 제품은 비공개 repository에서 개발 중입니다. 이 공개 repository는 제품의 전체 소스코드나 내부 설계를 공개하기 위한 공간이 아니라, 심사자와 외부 검토자가 PlotScope의 문제의식, 제품 방향, AI-assisted workflow, human-in-the-loop 구조를 이해할 수 있도록 공개 가능한 범위만 정리한 자료입니다.

- Public preview: https://plotscope-public-preview.vercel.app/
- Repository: https://github.com/dreamwars99/creative-text-annotation-case-study

## PlotScope란?

PlotScope는 장편소설, 웹소설, 웹툰·게임 원작 IP처럼 긴 서사와 복잡한 세계관을 다루는 창작자를 위한 **AI-native Story OS**입니다.

PlotScope는 AI가 소설을 대신 써주는 앱이 아닙니다. 작가가 자유롭게 적은 아이디어, 원고, 캐릭터, 세계관 설정을 AI가 이해할 수 있는 구조로 정리하고, 그 구조를 바탕으로 작가가 계속 창작할 수 있도록 돕는 도구입니다.

핵심 원칙은 다음과 같습니다.

- AI는 정답 작성자가 아니라 제안자입니다.
- AI가 만든 결과는 곧바로 작품의 기준 정보가 되지 않습니다.
- 사용자는 AI 후보를 검토하고, 수정하고, 적용하거나 거절할 수 있습니다.
- 작가가 확정한 정보와 AI 후보, mock 데이터, template 데이터는 분리되어야 합니다.
- 작품의 최종 통제권은 항상 작가에게 있습니다.

## 이 repository가 보여주는 것

이 공개 repository는 PlotScope 전체 제품이 아니라, 공개 가능한 작은 case study와 포트폴리오 자료입니다.

현재 이 repository는 다음 내용을 보여줍니다.

- 자유로운 창작 입력을 구조화된 후보 데이터로 바꾸는 방식
- 이야기 요소를 factor / subelement로 나누는 간단한 예시
- AI 후보와 사람이 승인한 canonical 값을 분리하는 원칙
- evidence, provenance, review status, lock state를 추적하는 방식
- 애매한 창작 텍스트를 검토 가능한 데이터로 다루는 annotation guideline
- schema 품질과 human review 품질을 검증하는 기본 절차

## 공개 preview와의 관계

Vercel public preview는 PlotScope의 실제 frontend MVP 방향을 보여주기 위한 심사용 공개 페이지입니다.

- Public preview: https://plotscope-public-preview.vercel.app/

해당 preview는 실제 제품의 방향을 보여주기 위한 용도이며, 공개 버전에서는 live AI inference를 비활성화하고 mock/fallback 응답만 사용합니다. 실제 제품 소스코드, API key, local model endpoint, 내부 prompt, 비공개 개발 로그, 미공개 작품 자료는 포함하지 않습니다.

## Portfolio Context

이 case study는 창작 workflow를 다루는 비공개 개인 프로젝트를 바탕으로 만든 공개용 축약 자료입니다.

공개 버전에서는 전체 제품 구조를 노출하지 않고, 다음과 같은 작은 annotation slice만 사용합니다.

- `concept.core_premise`
- `concept.narrative_question`
- `concept.logline`

비공개 프로젝트에는 더 넓은 taxonomy, Story OS 구조, AI runtime 설계, model routing, Workspace, Characters, World Atelier 등 더 많은 기능과 문서가 포함되어 있습니다. 이 repository에서는 그 전체 내용을 공개하지 않습니다.

## Repository Map

- [case_study.md](./case_study.md): 제품 문제와 annotation 문제를 설명하는 case study입니다.
- [annotation_guideline_sample.md](./annotation_guideline_sample.md): reviewer가 AI 후보를 검토할 때 사용할 수 있는 guideline 예시입니다.
- [candidate_schema_sample.json](./candidate_schema_sample.json): 최소한의 candidate JSON 구조 예시입니다.
- [demo_flow.md](./demo_flow.md): 창작 입력이 후보 데이터와 human review로 이어지는 흐름 예시입니다.
- [validation_process.md](./validation_process.md): schema와 review 품질을 확인하는 검증 절차 예시입니다.
- [screenshots/README.md](./screenshots/README.md): 공개 가능한 screenshot 설명 자료입니다.

## Safety Boundary

이 repository에는 다음 내용을 포함하지 않습니다.

- PlotScope 전체 제품 소스코드
- production prompt 전문
- 전체 factor taxonomy
- agent / orchestrator 내부 구조 전문
- provider, API, RunPod, model deployment 세부 설정
- API key 또는 secret
- 실제 user data
- 미공개 원고나 작품 설정
- 비공개 repository 링크
- 원본 work_process 전체 로그

## Rights

Copyright (c) 2026 dreamwars99. All rights reserved.

이 repository는 포트폴리오 및 심사용 공개 자료입니다. 별도 허가 없이 이 자료를 복사, 수정, 재배포하거나 다른 제품에 사용하는 것을 허용하지 않습니다.
