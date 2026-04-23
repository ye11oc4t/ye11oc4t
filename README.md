<img width="100%" alt="Ye11oc4t" src="https://github.com/user-attachments/assets/256ec48c-cec5-4277-9729-c897a8ee707b" />

<div align="center">

# 🐱 김서연 (ye11oc4t)

[![PORTFOLIO](https://img.shields.io/badge/🌐_PORTFOLIO-ye11oc4t.kr-F5C842?style=for-the-badge&logoColor=white)](https://ye11oc4t.kr)
[![BLOG](https://img.shields.io/badge/📝_BLOG-blog.ye11oc4t.kr-F9A825?style=for-the-badge&logoColor=white)](https://blog.ye11oc4t.kr)
[![LINKEDIN](https://img.shields.io/badge/💼_LINKEDIN-서연_김-A8C5DA?style=for-the-badge&logoColor=white)](https://www.linkedin.com/in/서연-김-a71032245)
[![EMAIL](https://img.shields.io/badge/📧_EMAIL-ye11oc4t@gmail.com-D4C5A9?style=for-the-badge&logoColor=white)](mailto:ye11oc4t@gmail.com)

</div>

---

## 소개

안녕하세요, 김서연입니다.

**기술과 정책의 경계를 넘나드는 보안 엔지니어**를 지향합니다.
클라우드 보안과 보안 운영(SecOps)을 중심으로, 취약점 분석·재현 / SIEM·EDR 구축 / CTI 자동화 / 컴플라이언스 점검까지
end-to-end 보안 파이프라인을 직접 설계하고 운영합니다.

> - Baby Beavers CERT 팀 리드
> - 화이트햇 스쿨 3기 수료
> - S-개발자 1기 수료
> - K-Shield.Jr 10기 수료 (취약점 진단 트랙)
> - 네이버 PER(Privacy Engineering Reward) 2025년 **랭킹 6위** 기록
> - 2023 한국컴퓨터종합학회 학부생 논문경진대회 **장려상**

**Interest** : Cloud Security · Vulnerability Research · SecOps Automation · Privacy Engineering

---

## 역량 기술

| 영역 | 기술 |
|---|---|
| **Cloud** | AWS (EC2, ALB, CloudFront, S3, RDS, WAF, ACM, Lambda, Security Hub) |
| **SecOps** | Wazuh (SIEM) · Velociraptor (EDR) · Fix Inventory (ASM) · MISP (CTI) |
| **DevSecOps** | GitHub Actions · GitLeaks · TruffleHog · Terraform · Ansible |
| **Automation** | n8n · ThreatFox/OTX/AbuseIPDB CTI 파이프라인 · AWS Lambda · Slack 알림 |
| **Compliance** | ISMS-P · 개인정보보호법 · Prowler (CSPM) · Cloud Custodian |
| **Dev** | Python · FastAPI · Docker · Nginx · Cloudflare Tunnel · Tailscale |

---

## 대표 프로젝트

### woowa-beavers-shop — MSA 이커머스 플랫폼 + CERT 환경
> Baby Beavers 팀 프로젝트 | **팀 리드 / 프로젝트 오너**

**Repo**: [woowa-beavers](https://github.com/woowa-beavers) | **기간**: 2025.03 ~

FastAPI 기반 MSA 이커머스 플랫폼을 AWS 위에 구축하고, 실제 CERT 운영 환경으로 활용합니다.

- AWS EC2 5대, ALB + path-based HTTPS, CloudFront, S3, RDS (Auth / Commerce 분리) 구성
- Terraform(flat structure), Ansible(ProxyJump Bastion) 직접 작성
- GitHub Actions CI — GitLeaks + TruffleHog 시크릿 스캐닝 자동화
- Wazuh(SIEM) / Velociraptor(EDR) 에이전트 4대 EC2 연동, Fix Inventory로 ASM 수행
- n8n CTI 파이프라인: ThreatFox / OTX / AbuseIPDB → MISP → AWS WAF IP Set 자동 차단 (Lambda)
- [AWS-Breach_Casebook](https://github.com/woowa-beavers) 레포 운영 — CI 기반 frontmatter 검증 + PR 워크플로우

---

### Prowler MCP 개발 및 AWS 취약점 점검 / 조치 자동화
> 화이트햇 스쿨 3기 팀 프로젝트 | 8명 | **2025.06 ~ 2025.08**

Prowler 점검 결과(JSON/CSV/HTML)를 파싱·분석하는 **RAG 기반 Claude Desktop MCP 서버**를 개발하고,
Cloud Custodian IaC 코드 자동 생성 + Slack 알림까지 연결하는 통합 아키텍처를 구성했습니다.

- 금융권 ISMS-P 기준 RAG 연동 → 점검 결과를 자연어로 설명·보고
- Cloud Custodian YAML 자동 생성 → MCP 내에서 AWS 설정 패치까지 수행
- Slack + AWS Security Hub로 전체 플로우 알림 연동
- **Stack**: Prowler · FastMCP · Python · Cloud Custodian · Ansible · AWS

---

### Prowler를 이용한 AWS ISMS-P 점검
> 화이트햇 스쿨 3기 팀 프로젝트 | 6명 | **2025.05 ~ 2025.07**

은행 실시간 입출금 시스템을 AWS 인프라로 직접 설계·구축한 뒤, Prowler로 ISMS-P 컴플라이언스를 점검했습니다.
인프라 기획부터 구축·보안 설정·컴플라이언스 보고서 작성(32p)까지 전 단계에 참여했습니다.

- VPC Peering 기반 망분리, IAM Role 최소 권한 설계, WAF DDoS 차단 구성
- AWS Security Hub + Prowler 연동 → 고위험 취약 리소스(퍼블릭 S3, 과도한 IAM Role) 즉시 패치
- **Stack**: AWS · Prowler · ISMS-P

---

### Aiscort — LLM 인풋 개인정보 가명처리 필터
> 개인 프로젝트 | **2025.01 ~ 2025.04** | **[aiscort.kr](https://aiscort.kr)**

멀티모달 LLM 사용 시 민감정보 필터링 없이 데이터가 업로드되는 문제를 해결하기 위해 개발했습니다.
텍스트·이미지·파일 3가지 입력 모드를 지원합니다.

- **Prompt**: 이름·전화번호·주소 등 PII + 토큰·API 키 등 인증정보를 Regex 기반 자동 마스킹
- **File**: PDF/PPT/Word/HWP OCR 처리 후 개인정보 마스킹·메타데이터 삭제·다운로드
- **Image**: JPG/PNG OCR + 얼굴 감지 → 인물/배경 선택 블러 처리
- **Stack**: React · Next.js · Tailwind CSS · FastAPI · Flask · Docker · Nginx · Tesseract OCR · Presidio

---

### 모의 ISMS-P
> 화이트햇 스쿨 3기 팀 프로젝트 | 4명 | **2025.05 ~ 2025.06**

가상 회사의 개인정보처리시스템을 대상으로 ISMS-P 접근통제·암호화·로그관리 항목을 모의 점검했습니다.
운영자 인터뷰 및 시스템 설정 검토를 통해 결함을 도출하고 개선방안을 작성했습니다.

---

### Docker 내 취약점 진단 자동화 (K-Shield Jr 10기)
> 팀 프로젝트 | 5명 | **2023.03 ~ 2023.05**

KISA 주통기 + SK쉴더스 가이드라인을 통합한 자체 룰셋 기반의 Docker 보안 점검 도구를 개발했습니다.
D-01 ~ D-41 항목을 쉘 스크립트로 자동 진단하고, 결과를 정리된 리포트로 출력합니다.

- **Repo**: [Docker-Vulncheck](https://github.com/ye11oc4t/Docker-Vulncheck)
- **Stack**: Docker · Linux · Bash shell

---

### 큐싱 탐지 솔루션 (해커톤)
> 팀 프로젝트 | 4명 | **2023.10 (2일 해커톤)**

Puppeteer 기반 클라우드 샌드박스에서 QR코드·단축 URL을 분석해 큐싱(피싱) 여부를 판별하는 솔루션입니다.
URL 리다이렉션 추적, 악성 파일 다운로드 탐지, ClamAV + VirusTotal API 연동으로 탐지 정확도를 높였습니다.

- **Stack**: Kotlin · FastAPI · Flask · Puppeteer · ClamAV · VirusTotal API · AWS · YARA Rules

---

## CTF 및 버그바운티 실적

### CTF (해킹방어대회)

| 대회 | 성적 |
|---|---|
| DownUnderCTF 2024, PoXCTF 등 | 국내외 다수 참가 |

Dreamhack, Webhacking.kr 워게임으로 레드팀 관점의 공격 기법을 꾸준히 학습하고 있습니다.

### 네이버 PER (Privacy Engineering Reward) 버그바운티

네이버쇼핑 및 네이버 블로그를 대상으로 개인정보 보호·컴플라이언스 기반의 취약점 발굴 활동을 진행했습니다.
기술적 오류뿐 아니라 **개인정보 처리방침 및 컴플라이언스 이슈**까지 포괄적으로 점검하여 **전체 랭킹 6위**를 기록했습니다.

---

## 개인정보보호법 모의재판

수능 감독관의 수험생 개인정보 무단 이용 사건 모의재판에 참여해, 1심 판결문 분석·2심 항소 이유·법리 쟁점 정리를 수행했습니다.
원고의 '정당한 이용 목적 없음' 주장을 검토해 피고 무죄를 주장했으며,
실제로 **2025년 7월 8일 대법원 최종심에서 피고 무죄가 선고**되어 분석이 실제 판례와 일치하는 결과를 확인했습니다.
개보법 적용 기준과 한계를 실무적으로 이해하는 계기가 됐습니다.

---

## 경험 및 활동

| 기간 | 내용 |
|---|---|
| 2026.03 ~ | Baby Beavers |
| 2025.07 ~ 2025.12| 2025 오픈소스 컨트리뷰션 아카데미 (장려상 수상) |
| 2025.03 ~ 2025.08| 화이트햇 스쿨 3기 수료 |
| 2025.03 ~ 2025.09 | 개인정보보호 분야 학부연구생 — LLM 개인정보 유출 연구 / 공격 기법 테스트 |
| 2024.09 ~ 2024.12 | (주)소프트랩스 인턴 — 모바일 개발 (PWA, Android) |
| 2023.06 ~ 2023.12 | S-개발자 1기 수료 |
| 2023.03 ~ 2023.05 | K-Shield.Jr 10기 수료 (취약점 진단 트랙) |
| 2022 ~ 2023 | 교내 해킹방어대회소학회 인터루드 임원 · CTF 스터디장 |
| 2022, 2023 | 교내 정보보호소학회 연합 세미나 운영진 (2회) |
| 2020.03 ~ 2026.02 | 서울여자대학교 정보보호학과 (졸업) |

---

## 자격증 / 어학

- OPIC IH
- TOEIC 910

---

<div align="center">

| | |
|:---:|:---:|
| <a href="https://github.com/ye11oc4t"><img src="https://render.gitanimals.org/farms/ye11oc4t" width="100%"/></a> | <a href="https://www.gitanimals.org/"><img src="https://render.gitanimals.org/guilds/834826977655465879/draw" width="100%" alt="gitanimals" /></a> |

</div>
