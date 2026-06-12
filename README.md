# Green University 학사관리 시스템 - Frontend

그린대학교(Green University) 학사관리 시스템의 프론트엔드 저장소입니다. 학생, 교수, 관리자 역할에 따라 회원, 학과, 강의, 수강신청, 출결, 성적 관리 화면을 제공합니다.

프로젝트 전체 소개, 팀원 구성, 회고 등은 백엔드 저장소 README를 참고해 주세요.

> Backend: [be-green-uni](https://github.com/green-uni/be-green-uni)

## 기술 스택

| 구분 | 내용 |
|---|---|
| Core | Vue 3, Vite, Vue Router, Pinia (+ pinia-plugin-persistedstate) |
| HTTP | Axios |
| 스타일 | CSS |
| UI/UX | Font Awesome (아이콘), VueUse (디바운스 처리) |
| 코드 품질 | ESLint, Prettier |

## 폴더 구조

```
src/
├── assets/        # 이미지, 공통 CSS (reset, layout 등)
├── components/
│   ├── common/    # 공통 UI 컴포넌트
│   ├── layout/    # 레이아웃 (헤더, 사이드바 등)
│   └── util/      # 유틸리티성 컴포넌트
├── router/        # Vue Router 설정
├── services/      # Axios 기반 API 호출 함수
├── stores/        # Pinia 상태 관리
├── utils/         # 공통 유틸 함수
└── views/         # 화면 단위 컴포넌트
    ├── intro/      # 로그인 등 시작 화면
    ├── member/     # 회원/인증/관리자 (admin 하위 포함)
    ├── major/      # 학과
    ├── lecture/    # 강의
    ├── course/     # 수강신청
    ├── attendance/ # 출결
    └── grade/      # 성적
```

views 하위 폴더는 백엔드 도메인 구분과 동일하게 매칭됩니다.

## 실행 방법

### 1. 사전 요구사항
- Node.js (^20.19.0 또는 >=22.12.0)
- 백엔드 서버가 `localhost:8080`에서 실행 중이어야 합니다 (API 프록시 연동)

### 2. 설치 및 실행
```bash
git clone https://github.com/green-uni/fe-green-uni.git
cd fe-green-uni
npm install
npm run dev
```

### 3. 기타 스크립트

| 명령어 | 설명 |
|---|---|
| `npm run build` | 프로덕션 빌드 |
| `npm run preview` | 빌드 결과 미리보기 |
| `npm run lint` | ESLint 검사 및 자동 수정 |
| `npm run format` | Prettier 포맷팅 |
