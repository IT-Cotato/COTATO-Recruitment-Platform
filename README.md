# COTATO-Recruitment-Platform

> COde Together, Arrive TOgether — IT 연합동아리 코테이토의 통합 지원 플랫폼

## 📁 레포지토리 구조

이 레포지토리는 프론트엔드와 백엔드를 **Git Submodule**로 관리하는 통합 레포입니다.

```
COTATO-Recruitment-Platform/
├── frontend/   → COTATO-FE-v2        (Next.js · TypeScript · Turborepo monorepo)
└── backend/    → COTATO-Recruit-BE   (Spring Boot · Java)
```

| 디렉터리 | 레포지토리 | 브랜치 | 설명 |
|----------|-----------|--------|------|
| `frontend/` | [IT-Cotato/COTATO-FE-v2](https://github.com/IT-Cotato/COTATO-FE-v2) | `develop` | 리크루트 페이지 및 홈페이지 (pnpm monorepo) |
| `backend/`  | [IT-Cotato/COTATO-Recruit-BE](https://github.com/IT-Cotato/COTATO-Recruit-BE) | `develop` | 리크루트 서버 (Spring Boot) |

---

## ⭐ 처음 클론할 때

서브모듈까지 함께 클론하려면 `--recurse-submodules` 옵션을 사용합니다.

```bash
git clone --recurse-submodules https://github.com/IT-Cotato/COTATO-Recruitment-Platform.git
```

이미 클론한 경우 서브모듈을 초기화·다운로드합니다.

```bash
git submodule update --init --recursive
```

---

## 🔄 서브모듈 최신화

각 서브모듈의 `develop` 브랜치 최신 커밋을 통합 레포에 반영합니다.

```bash
# 모든 서브모듈 업데이트
git submodule update --remote --merge

# 변경 사항 커밋
git add frontend backend
git commit -m "chore: 서브모듈 최신화"
git push
```

특정 서브모듈만 업데이트하려면 해당 디렉터리로 이동 후 작업합니다.

```bash
cd frontend
git pull origin develop

cd ../backend
git pull origin develop
```

---

## 🛠️ 개별 실행 방법

### Frontend

```bash
cd frontend
pnpm install
pnpm dev
# Homepage: http://localhost:3001
# Recruit:  http://localhost:3000
```

> Node.js 18 이상, pnpm 필요

### Backend

```bash
cd backend
./gradlew bootRun
```

---

## 🔗 관련 링크

- 홈페이지: [cotato.kr](https://cotato.kr)
- 리크루트: [recruit.cotato.kr](https://recruit.cotato.kr)