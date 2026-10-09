# 김재원 | 유안타증권 리서치 포트폴리오

유안타증권 리서치센터 체험형 인턴 지원용 웹 포트폴리오입니다. 국내외 경제·금융시장 분석과 기업·산업 리포트 작성 지원 업무에 맞춰 브리핑 자동화와 기업분석을 앞에 배치했습니다.

- [공개 사이트](https://bucheoncityboy.github.io/yuanta-research-portfolio/)
- [전체 프로젝트 인덱스](https://github.com/bucheoncityboy/portfolio-index)
- [실제 AI 활용 브리핑 샘플](https://bucheoncityboy.github.io/yuanta-research-portfolio/samples/2026-10-07.html)

## 대표 경험

1. **Multi-Asset Morning Briefing**: 시장별 완료 거래일과 관측일·단위·출처 검증, Python 수집 도구와 K-Skill 기여. 약 40분 → 10분 이내는 학회원 피드백 기준입니다.
2. **Corporate Research AI Agent**: 기업자료 수집·대조와 HTML 보고서 생성. v3 에이전트 방식과 이전 v2 Python 파이프라인을 구분합니다. 19종목은 README의 지원 범위이며 분석 완료 건수가 아닙니다.
3. **Global Macro & IB Research**: 해외 IB Rates·FX·Credit 논점 분석과 공개 경제지표·시장가격 대조, 정기 브리핑·발표.
4. **BOK MPC & KTB Curve**: 정책결정 36회, 공통 관측일 1,084개, D+1 확대 19회·축소 17회. 인과효과나 실제 거래 성과가 아닌 이벤트 연구입니다.

추가 연구는 Fama-French 실증과 TensorFlow·LightGBM 기반 분위수 회귀입니다. 스킬 5개는 개인 저장소와 K-Skill 공식 기능 문서로 각각 연결합니다.

## 로컬 검증

```sh
npm ci
npm run check
npm run typecheck
npm run preview
```

미리보기: `http://127.0.0.1:4173`

## 구조

- `index.html`: 대표 경험 4개, 정량 연구, 오픈소스 기여, 작업 방식, 학력·활동·자격·연락처
- `styles.css`: 기존 디자인과 반응형·인쇄 스타일
- `samples/2026-10-07.html`: 기존 공개 AI 스킬 실행 예시
- `assets/favicon.svg`: JK 아이콘
- `src/harness.ts`: 앵커·파일·표현·문서 비공개·배포 범위 검증
- `src/serve.ts`: 공개 파일만 제공하는 미리보기 서버
- `docs/source-notes.md`: 근거와 확인 범위
- `docs/snapshot-2026-10-07.json`: 기존 공개 샘플 실행 기록
- `.github/workflows/deploy-pages.yml`: 검증 후 GitHub Pages 배포

기업분석 HTML은 원본 저장소로 연결하며 내용을 복제하지 않습니다. 첨부 문서·유료 리서치 PDF·변환 이미지·개인 로컬 파일을 포함하지 않습니다. 배포 파일은 `index.html`, `styles.css`, `.nojekyll`, `assets/`, `samples/`로 제한합니다.

## 배포

GitHub Pages 소스를 **GitHub Actions**로 설정합니다. `main` 변경 시 `npm ci`, `npm run check`, `npm run typecheck`를 통과한 공개 파일만 배포합니다.

배포 주소는 저장소 생성과 Pages 활성화 후 사용할 수 있습니다. 실제 상태와 검수 결과는 `docs/verification.md`를 참고합니다.
