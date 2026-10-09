# 콘텐츠 근거와 표현 범위

확인일: 2026-10-09 (KST). 공개 README·구현·결과물과 지원자 경험 설명을 대조했습니다. 과거 데이터 수집·금융 모델 실험을 전부 다시 실행한 검증 보고서는 아닙니다.

## 공고와 회사 자료

- [공고 원문](https://www.kofia.or.kr/brd/m_96/view.do?seq=42447): 국내외 경제·금융시장 분석 보조, 기업·산업 분석 리포트 관련 리서치, 센터 제반 업무. AI Tool·Python AI Library 활용 우대를 확인했습니다.
- [유안타 AI 미국 주식시장 마감 시황](https://m.myasset.com/myasset/research/rs_list/rs_view.cmd?SEQ=207573&cd006=&cd007=RB30&cd008=RB30B): 공식 페이지의 AI 한줄평·핵심 이슈 구성 확인. 내부 제작 도구·검증 절차는 추정하지 않습니다.
- [Quant Playbook 2026년 8월호](https://www.myasset.com/myasset/research/rs_list/rs_view.cmd?SEQ=206896&cd006=&cd007=RB30&cd008=RB30A): 공식 페이지의 이익 성장·추정치·변동성과 낙폭 비교를 확인했습니다. 보고서의 결과·표·차트를 복제하지 않습니다.
- [기업분석 공식 목록](https://www.myasset.com/myasset/research/rs_list/rs_list.cmd?cd007=RE01): 실적 Preview·Review, 컨센서스 비교와 산업별 자료 발간을 확인했습니다.

프로젝트의 직무 관련성과 배치 판단에 참고했으며 지원자가 회사 자료를 작성하거나 내부 업무를 경험한 것으로 표현하지 않습니다.

## 디자인 원본과 분리

디자인·코드 원본은 `bucheoncityboy/ls-investment-strategy-portfolio`, 커밋 `6f7ae1308c533a6edeeedbac5f77ce0f5f964175`입니다. 독립 작업 디렉터리와 새 저장소를 구성하고 원본에는 쓰기 작업을 하지 않았습니다. 타이포그래피·색·카드·금리 차트·Background·Credentials·Contact와 정적 배포 구조를 유지했습니다.

## 브리핑 자동화

- [개인 저장소](https://github.com/bucheoncityboy/multi-asset-morning-briefing): README, Python helper와 공식 기능 문서를 대조했습니다.
- 기본 원천은 ECOS·U.S. Treasury·Cboe·ECB. FRED는 발표 지연을 표시하는 보조 fallback입니다.
- 미국과 한국 완료 세션을 독립 판별하고 관측일·단위·가격 기준을 기록합니다. 불일치·원천 오류는 추정이나 보간 없이 제외합니다.
- [PR #675](https://github.com/NomaDamas/k-skill/pull/675): 작성자 `bucheoncityboy`, 2026-09-19 병합 확인.
- [PR #677](https://github.com/NomaDamas/k-skill/pull/677): 같은 날 dev → main 배포 반영. 지원자가 작성한 별도 PR로 표현하지 않습니다.
- 약 40분 → 10분 이내는 지원자가 제공한 학회원 사용 피드백입니다. 약 75%는 40·10분 기준 단순 계산이며 통제 실험·평균 생산성 벤치마크가 아닙니다.

### 2026.10.07 AI 활용 리서치 샘플

원본 `samples/2026-10-07.html`을 재사용했습니다. 새 브리핑을 생성한 것이 아니며 수치·뉴스·일정을 유지하고 상세 근거 링크와 CSS 버전만 신규 사이트로 변경했습니다. 직접 작성한 학회 브리핑과 구분합니다.

- 기존 원본 실행 기록: K-Skill `9fade13b1066bc58fd820fe659145a9a21974138`; helper SHA-256 `30f2df565561616eab7d634cd96e1ba1b6c2c701e7e18e120e3294f182ae99fb`.
- [기존 snapshot](snapshot-2026-10-07.json): 생성 2026-10-07 19:15:54 KST, 미국·한국 세션 각각 2026-10-06, 10개 item, warnings/failures 없음. 이번 작업에서 재실행하지 않았습니다.
- 07:00 KST는 뉴스·시장 세션 기준시각입니다. 실제 조회는 당일 저녁이므로 오전 7시에 작성한 기록으로 표시하지 않습니다.
- Treasury는 일별 Par Yield, ECB는 reference rate, USD/KRW는 서울시장 15:30 주간 종가. 국내 국고채는 금융투자협회 수익률을 인용한 보도 근거입니다.
- CME `current`와 공식 일정 페이지는 갱신되므로 과거 자료가 계속 표시된다고 보장하지 않습니다.

## 기업분석 파이프라인과 별도 스킬

- [Agentic Research Pipeline](https://github.com/bucheoncityboy/agentic-research-pipeline), 확인 커밋 `fa47627a735816032631ff8f17b6281aadeb5a59`: README, 에이전트 지침, HTML 템플릿, 삼성전자·셀트리온 HTML을 확인했습니다.
- v3 공개 구현은 에이전트 지침과 HTML 템플릿입니다. v2 Python 스크립트 제거·게이트의 체크리스트 이관은 공개 지침에 명시돼 있습니다. v2 전체 Python 구현을 실행 검증하지 않았습니다.
- 19종목은 README의 지원 범위입니다. 모든 종목의 실행·검증 완료 건수로 표현하지 않습니다.
- 삼성전자(2026-07-08)·셀트리온(2026-07-03) HTML의 섹션·출처·수집일을 확인했습니다. 삼성전자 샘플의 기업·산업 개요, 재무·컨센서스, 주요 이슈, Bull/Bear, 위험·일정 구성을 대표 링크로 선정했습니다. 과거 보고서의 모든 숫자와 뉴스 링크를 다시 확인한 것은 아닙니다.
- NVIDIA PDF의 공개 저장소 존재를 확인했습니다. 전 내용을 검증하거나 이 사이트에 복제·임베드하지 않았습니다.
- 미리보기는 삼성전자 HTML의 구성 요약입니다. 차트·표·주가·컨센서스 수치를 복제하지 않습니다.
- [Company Analysis](https://github.com/bucheoncityboy/company-analysis-skill): README, 근거 처리 코드와 공식 기능 문서 확인. 한국·미국 공시와 원문·기간·단위·회사 귀속을 대조합니다. Node.js/TypeScript·JavaScript 도구이며 Python 테스트 runner만으로 모든 분석을 Python이라고 표현하지 않습니다.
- Company Analysis는 채팅형 분석이고 HTML 보고서는 별도 Agentic Research Pipeline의 역할입니다.
- 독립 실적 전망·목표주가 산출이나 전문 애널리스트 대체 성과를 주장하지 않습니다.

## 직접 수행한 글로벌 리서치

정기 브리핑과 해외 IB Rates·FX·Credit 분석·발표는 지원자 경험 설명과 기존 포트폴리오를 따릅니다. 중립금리·Fed 정책경로·연례개정·금리 민감도·교차자산 전달경로는 검토한 주제입니다. 비공개 IB 원문·표·차트와 출처가 확인되지 않은 수치는 공개하지 않습니다.

## 국고채 이벤트 연구

[최신 연구 README](https://github.com/bucheoncityboy/krw-rates-integrated-research): 공통 관측일 1,084개, 정책결정 36회, D+1 확대 19회·축소 17회. D-1은 발표 전일 기준이고 D+1·D+5는 다음·다섯째 관측일입니다. 인과효과·변수별 영향도 분해 연구가 아닙니다. DV01 중립 포지션은 가상 민감도 계산이며 실제 체결·전체 이벤트 전략 백테스트가 아닙니다. 과거 38회·1,151개는 사용하지 않았습니다.

## 정량 연구와 Python AI Library

- [Fama-French](https://github.com/bucheoncityboy/fama-french-integrated-research): 최신 README의 미국 FF(1993) 재현, 한국 1,054종목, HML t=3.89, 미국 양(+)·한국 음(-) SMB 확인. 표본 내 결과입니다.
- [HAQR](https://github.com/bucheoncityboy/deep-quant-risk-haqr): README, `src/models.py`, LightGBM 비교 실험 코드 확인. TensorFlow·5/50/95% non-crossing 분위수와 LightGBM을 사용합니다.
- 약 7.4%는 보고서의 합성 AR(3) 데이터 100회 반복 실험에서 Pinball Loss 0.003501 → 0.003242의 감소율입니다. 모델 학습을 재실행하지 않았습니다. 실제시장 예측 정확도·수익률·승률로 표현하지 않습니다.

## K-Skill 오픈소스 기여

공식 문서 5개를 main `50d7bb30f9e2d6b8b09da1055d497fe616820e30`에서 확인하고 GitHub API PR 메타데이터로 병합을 대조했습니다.

| 기능 | 공식 문서 | 지원자 PR | 병합일 |
|---|---|---|---|
| Multi-Asset Morning Briefing | [문서](https://github.com/NomaDamas/k-skill/blob/main/docs/features/multi-asset-morning-briefing.md) | [#675](https://github.com/NomaDamas/k-skill/pull/675) | 2026-09-19 |
| Company Analysis | [문서](https://github.com/NomaDamas/k-skill/blob/main/docs/features/company-analysis.md) | [#682](https://github.com/NomaDamas/k-skill/pull/682) | 2026-09-30 |
| Market Event Impact | [문서](https://github.com/NomaDamas/k-skill/blob/main/docs/features/market-event-impact.md) | [#684](https://github.com/NomaDamas/k-skill/pull/684) | 2026-09-30 |
| Government Bond Analysis | [문서](https://github.com/NomaDamas/k-skill/blob/main/docs/features/government-bond-analysis.md) | [#683](https://github.com/NomaDamas/k-skill/pull/683) | 2026-09-30 |
| Korean Bond Search | [문서](https://github.com/NomaDamas/k-skill/blob/main/docs/features/korean-bond-search.md) | [#685](https://github.com/NomaDamas/k-skill/pull/685) | 2026-09-30 |

## 학력·활동·자격과 공개 범위

[최신 인덱스](https://github.com/bucheoncityboy/portfolio-index)와 원본 사이트의 날짜를 대조했습니다. Background/Credentials와 연락처 링크는 유지했습니다. 첨부 지시·자소서·비공개 PDF·원본 연구문서·변환 이미지·개인 로컬 파일은 포함하지 않습니다. Pages에는 홈페이지·CSS·favicon·기존 브리핑 샘플만 배포하며 문서·도구·snapshot은 제외합니다.
