# LANE4 Claude Code Skills

LANE4 운영에 특화된 Claude Code 커스텀 스킬 모음.

## 스킬 목록

| 스킬 | 호출 | 설명 |
|------|------|------|
| **code-review** | `/code-review` | git diff 기반 코드 리뷰. NestJS 패턴 위반, 보안 취약점, 컨벤션 위반을 심각도별로 피드백 |
| **deploy** | `/deploy` | 배포 전 사이드이펙트 체크. 코드 diff + DB 스키마 + 외부 연동 변경사항 종합 분석 |
| **git-committer** | `/git-committer` | 변경점 분석 후 한국어 커밋 메시지 생성 및 최소 작업 단위로 분할 커밋 |
| **issue** | `/issue` | 이슈 발생 시 관련 로직 조회 및 수정/해결 방안 제안 |
| **lane4-mysql** | `/lane4-mysql` | 자연어 → SQL 변환 및 실행. 배차, 기사, 차량, 법인, 요금 등 LANE4 비즈니스 데이터 조회 |
| **log-search** | `/log-search` | DB(HTTP_LOG)와 Elasticsearch 양쪽에서 로그 검색 및 분석 |

## 설치

```bash
git clone https://github.com/lane4-jiny/claude-lane4-skills.git ~/.claude/skills
```

## 업데이트

```bash
cd ~/.claude/skills && git pull
```
