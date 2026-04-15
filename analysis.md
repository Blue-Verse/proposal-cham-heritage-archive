# NFT/DRM/포렌식 워터마크 B2B/B2C 디지털 아카이브 포털 — 제안 분석 로그

> 생성일: 2026-04-15
> 공고 URL: https://www.wishket.com/project/154511/

## 1. 공고 파싱 결과

```yaml
job:
  title: "NFT/DRM/포렌식 워터마크가 적용된 B2B/B2C 디지털 아카이브 포털 구축"
  category: "웹, 안드로이드, iOS, 자사몰 구축"
  budget_range: "100,000,000원"
  duration: "150일"
  tech_stack:
    - Next.js 14 (App Router)
    - Tailwind CSS
    - Node.js + Express
    - Next.js API Routes
    - PostgreSQL + Prisma ORM
    - AWS S3 / MinIO
    - Stripe (단건 + 구독 인보이스)
    - IMATAG (포렌식 워터마크)
    - Pallycon (DRM 스트리밍)
    - Polygon + ethers.js (NFT)
    - web3.storage (IPFS)
    - Docker + Nginx
  description: "한국 전통 예술 콘텐츠(이미지·음원·영상)를 디지털 라이선스로 거래하는 마켓플레이스. B2C + B2B 단일 카탈로그 기반 포털"
  requirements:
    - 콘텐츠 카탈로그 (이미지·음원·영상)
    - B2C 단건 구매 (Stripe)
    - B2B 기관 구독 (Stripe 인보이스)
    - NFT 라이선스 증명 (Polygon ERC-721)
    - 포렌식 워터마크 (IMATAG)
    - DRM 스트리밍 (Pallycon)
    - 관리자 패널
    - IPFS 메타데이터 영구 보관
  client_questions:
    - "첨부된 문서를 검토하셨나요?"
  deadline: "2026-04-17"
  job_post_url: "https://www.wishket.com/project/154511/"
  urls: []
  images: []
```

## 2. URL/이미지 분석

- 참고 URL: 없음
- 첨부 이미지: 없음
- 첨부 PDF: "CHAM Heritage Archive Portal — Development Specification.pdf" (1.81 MB) — 위시켓 로그인 필요하여 분석 불가
- 참고 사항: 클라이언트가 영문 상세 개발 명세서(데이터 모델, API 엔드포인트, 컨트랙트 구조 포함) 보유. 미팅 시 확인 예정.

## 3. 실현 가능성 분석 (내부용)

### 프로젝트 유형
- 메인: 풀스택 웹앱 (CRUD, SaaS) → 가능, +10%
- 서브1: 결제/인증/외부 API 연동 (Stripe, IMATAG, Pallycon) → 조건부 가능, +15%
- 서브2: 스마트 컨트랙트/Web3 (Polygon NFT) → 비추천 (단, 범위 제한적)

### 기본 공수 (AI 보조 없이)

| 작업 영역 | 공수 (M/D) | AI 절감률 | 조정 후 |
|-----------|-----------|----------|--------|
| 기획/설계 | 20 | 35% | 13 |
| Figma 디자인 | 25 | 15% | 21 |
| FE 개발 | 60 | 65% | 21 |
| BE 개발 | 70 | 55% | 31.5 |
| QA/배포 | 20 | 55% | 9 |
| **합계** | **195** | **~51%** | **~96** |

### 버퍼 적용
- 결제/외부 API: +15%
- Web3 리스크: +10%
- 총 버퍼: +25%
- 최종 공수: 96 × 1.25 ≈ 120 M/D

### 달력 일수 변환
- 120 M/D × 7/5 = 168일

### 클라이언트 예상 기간 vs 산정 기간
- 클라이언트 예상: 150일
- 내부 산정: 168일
- 차이: 18일 (12% 초과, 20% 이내)
- 판정: 사용자 요청에 따라 **180일 (6개월)**로 제안

### 리스크 평가
1. Web3 컴포넌트 (Polygon NFT + IPFS): 비추천 카테고리이나 범위가 ERC-721 표준 + web3.storage로 제한적. Life3/NFT-DeFi 경험으로 리스크 관리 가능.
2. 외부 API 3종 (Stripe + IMATAG + Pallycon): 각 API 문서 품질/테스트 환경에 따라 공수 변동 가능.
3. 완화 요소: 클라이언트가 상세 개발 명세서 보유 + 기획자 1명 협업 → 기획 시간 절감.

## 4. 포트폴리오 매칭

| 순위 | 프로젝트 | 매칭 점수 | 핵심 유사점 |
|------|---------|----------|-----------|
| 1 | Life3 | 92% | NFT 마켓플레이스(ethers.js, 스마트 컨트랙트, 온체인 검증), Next.js+Express+PostgreSQL 동일 스택 |
| 2 | NFT-DeFi | 85% | Solidity 스마트 컨트랙트 직접 작성, NFT 민팅/거래/에어드롭, 온체인/오프체인 브릿지 |
| 3 | Series-B | 78% | 대규모 B2B 포탈(50+페이지, 200+API), 관리자 대시보드, 결제 연동, 규제 준수 |

### 매칭 근거
- **기술 스택 일치 (40%)**: Life3의 Next.js+Express+PostgreSQL+ethers.js가 본 프로젝트와 거의 동일
- **도메인 유사성 (30%)**: NFT 마켓플레이스(Life3), Web3 GameFi(NFT-DeFi), B2B 포탈(Series-B) 모두 직접 관련
- **기능 유사성 (20%)**: NFT 민팅, 토큰 거래, 관리자 패널, 결제 연동
- **규모 적합성 (10%)**: Life3(4 마이크로서비스, 700+ 파일), Series-B(1,652 PR, 50+ 페이지)

## 5. 최종 제안 요약

- 지원 금액: 9,000만원 (VAT 별도)
- 지원 기간: 180일 (6개월)
- 핵심 제안 포인트:
  1. NFT 마켓플레이스 직접 구축 경험 (Life3 — ethers.js, 스마트 컨트랙트, 온체인 검증)
  2. 동일 기술 스택 숙련도 (Next.js + Node.js/Express + PostgreSQL)
  3. 대규모 B2B 포탈 구축 경험 (Series-B — 50+ 페이지, 200+ API)
  4. 15+ 외부 API 연동 경험 (Stripe, KYC, AI API 등)
