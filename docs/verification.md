# 구현·검수 결과

공개 검증 시각: 2026-10-09 18:26 (KST).

## 현재 상태

공개 저장소 생성, 공개 프로젝트 파일 19개 업로드와 GitHub Pages 배포를 완료했습니다. 인증된 GitHub 연결로 소스를 업로드했고, Pages Source는 **GitHub Actions**로 설정했습니다. 첫 배포에 업로드한 19개 파일이 복원한 원본과 바이트 단위로 일치하는 것을 확인했습니다.

| 항목 | 주소 / 상태 |
|---|---|
| 신규 공개 저장소 | https://github.com/bucheoncityboy/yuanta-research-portfolio — 기본 브랜치 main |
| GitHub Pages | https://bucheoncityboy.github.io/yuanta-research-portfolio/ — HTTP 200, 실제 표시 확인 |
| 브리핑 샘플 | https://bucheoncityboy.github.io/yuanta-research-portfolio/samples/2026-10-07.html — HTTP 200, 실제 표시 확인 |
| 첫 배포 Actions | https://github.com/bucheoncityboy/yuanta-research-portfolio/actions/runs/37910707981 — success |
| 배포 구성 | main 변경 → npm 검증 → 허용한 정적 파일만 배포 |
| 기존 LS 저장소 | 쓰기 작업 없음; 작업 시작 시 main은 6f7ae1308c533a6edeeedbac5f77ce0f5f964175 |
| portfolio-index | 참고만 사용, 쓰기 작업 없음 |

Actions의 `deploy` job에서 의존성 설치, 사이트·문서 공개 범위 검사, TypeScript 검사, Pages 설정, 아티팩트 업로드와 실제 배포 단계가 모두 성공했습니다. main 갱신 시 같은 검증과 배포를 다시 실행합니다.

## 주요 변경

- 원본의 밝은 회색·화이트·네이비, Hero 좌우 구성, Featured 카드, 금리 반응 차트, HOW I WORK, Background·Credentials·Contact 유지.
- 유안타 리서치센터 지원 문구와 시장·기업 데이터 분석 중심 Hero 적용. 회사명·메타·OG URL·CSS 캐시 버전·패키지 이름 갱신.
- 대표 경험 순서: 브리핑 자동화 → 기업분석 → 글로벌 매크로·IB 리서치 → 금통위·국고채 연구. 앞의 두 프로젝트를 동등한 Featured 카드로 배치.
- 기업분석 카드에 실제 공개 삼성전자 HTML의 구성 미리보기와 원본 링크 추가. HTML 보고서 파이프라인과 별도 공시 검증 스킬 역할 구분.
- Fama-French·HAQR 카드, K-Skill 5개 기능의 공식 문서·개인 저장소 연결 추가.
- Research Process 5단계와 최신 통계·실험조건 표시. 학력·활동·자격 날짜 유지.

## 자동 검증

| 명령 | 결과 |
|---|---|
| npm ci | 현재 복원 환경과 GitHub Actions에서 통과 |
| npm run check | 현재 복원 환경과 GitHub Actions에서 통과 |
| npm run typecheck | 현재 복원 환경과 GitHub Actions에서 통과 |

검증에는 중복 ID, 내부 앵커, 로컬 샘플·자산 존재, 외부 링크 rel, 대표 프로젝트 순서, 새 지원 문구와 URL, 최신 KTB 수치, AI 구현 구분, 합성 데이터 조건, 문서 비공개와 배포 파일 범위가 포함됩니다.

환경의 tsx CLI IPC 제약을 피하기 위해 스크립트를 `node --import tsx`로 호출하도록 바꿨습니다. TypeScript·tsx 기술 스택은 유지합니다.

## 실제 공개 화면 검수

Codex 브라우저로 GitHub Pages를 직접 열었습니다. 홈페이지의 360·390·768·1280px에서 문서 가로 폭이 각각 뷰포트와 일치했고, 화면 밖으로 나오는 표시 요소와 누락된 내부 앵커가 없었습니다. 공개 환경에서 웹폰트 상태는 loaded였고, 단계 설명은 한글을 지원하는 sans-serif 폰트로 표시됐습니다. Hero·기업분석 카드·오픈소스 목록과 390px 브리핑 샘플을 화면으로 확인했습니다.

모바일에서 `<br>`가 숨겨질 때 `Multi-AssetMorning Briefing`으로 붙어 보이는 오류를 확인해, 줄바꿈 앞에 공백을 넣었습니다. 데스크톱의 기존 줄바꿈은 유지합니다.

| 공개 화면 너비 | 문서 가로 폭 | 요소 수평 넘침 |
|---|---|---|
| 360px | 360px | 없음 |
| 390px | 390px | 없음 |
| 768px | 768px | 없음 |
| 1280px | 1280px | 없음 |
| 샘플 390px | 390px | 없음 |

검수 스크린샷과 브라우저 런타임은 로컬에만 보관하며 저장소·Pages에 포함하지 않습니다.

## 이전 구현 단계의 로컬 검수

로컬 Chromium과 Playwright로 실제 렌더링했습니다. Noto Sans KR·Inter·IBM Plex Mono를 검수용 로컬 fontsource 패키지로 로드했고, 홈페이지의 Google Fonts 링크와 폰트명은 유지했습니다. 검수용 브라우저·폰트·스크린샷은 공개 저장소에 포함하지 않습니다.

| 화면 너비 | 문서 가로 폭 | 텍스트·카드 overflow |
|---|---|---|
| 360px | 360px | 없음 |
| 390px | 390px | 없음 |
| 768px | 768px | 없음 |
| 1280px | 1280px | 없음 |

390px 브리핑 샘플도 가로 넘침이 없었습니다. Hero·대표 프로젝트·오픈소스 영역의 스크린샷을 눈으로 확인했고, Hero 의미 단위 줄바꿈과 flow-detail의 한글 폰트를 수정했습니다. 상세 수치는 `responsive-checks.json`에 있습니다.

## 공개 배포 링크 검수

- 실제 홈페이지·CSS·favicon·브리핑 샘플은 GET HTTP 200이며, 응답 본문이 로컬 원본과 일치했습니다.
- 새 저장소의 `docs/source-notes.md`, 브리핑 원본 저장소, 기업분석 파이프라인, 삼성전자 HTML 보고서 원본, 국고채 연구 저장소를 직접 요청해 모두 HTTP 200을 확인했습니다.
- 문서와 검증 도구는 저장소에서 확인할 수 있지만 Pages 배포 파일에는 포함하지 않습니다. 워크플로는 `index.html`, `styles.css`, `.nojekyll`, `assets/`, `samples/`만 업로드합니다.
- Pages의 `/docs/source-notes.md`, `/package.json`, `/src/harness.ts`는 실제 GET HTTP 404로 배포에서 제외된 것을 확인했습니다.

## 이전 링크 검수와 남은 한계

- 홈페이지의 프로젝트·공식 문서·PR·인덱스 링크 21개가 HTTP 200으로 응답했습니다. 내부 앵커와 로컬 샘플은 자동 검증을 통과했습니다.
- LinkedIn은 HEAD 405, GET 999 접근 제한이 있어 실제 표시를 확인하지 못했습니다. 기존 연락처 링크를 유지했습니다.
- 이전 검수에서 브리핑 샘플 외부 링크 30개 중 26개는 HEAD 200이었습니다. 당시 생성 전이라 404였던 신규 저장소 source-notes 링크는 이번 배포 후 GET 200을 확인했습니다.
- 연합인포맥스 링크는 직접 요청에서 404/403이지만 웹 검색에서 동일 URL의 기사 제목과 해당 채권 수치를 확인했습니다. WSJ 두 링크는 401로 로그인 제한이 있습니다. 접근 제한을 링크의 내용이 없다는 증거로 해석하지 않았고 기존 샘플 수치·출처를 유지했습니다.
- 기업분석 과거 샘플의 모든 수치·뉴스 원문을 재검증하지 않았고, NVIDIA PDF 전 내용을 읽거나 금융 모델을 다시 학습하지 않았습니다. 각 역할과 표현 제한은 `source-notes.md`에 기록했습니다.
- 홈페이지·샘플의 배포와 표시를 확인했으며, 과거 샘플의 금융 수치·뉴스·일정을 이번 배포 작업에서 다시 수집하거나 재계산하지 않았습니다. 접근 제한 링크를 모두 정상 접근 가능하다고 표현하지 않습니다.
