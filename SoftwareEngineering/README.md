# Software Engineering 정리

## 1. 개발 프로세스 및 방법론

### Agile (애자일)

* 변화에 유연하게 대응하는 반복·점진적 개발 방식
* 고객 피드백 반영, 팀 협업 중심
* **장점:** 요구사항 변경 용이, 빠른 피드백
* **예:** **Scrum**, **Kanban**

- ####  Scrum

   * 가장 널리 쓰이는 Agile 프레임워크
   * **Sprint(1~4주)** 단위 개발
   * 주요 요소

     * Product Backlog
     * Sprint Planning
     * Daily Scrum
     * Sprint Review / Retrospective

### Waterfall (폭포수)

* 순차적 개발 방식 (요구사항 → 설계 → 구현 → 테스트 → 운영)
* 변경에 매우 취약
* 명확한 요구사항에서는 적합

### DevOps

* 개발(Dev) + 운영(Ops)의 통합 문화
* 자동화 기반의 빠른 배포와 안정성
* 핵심:

  * CI(지속적 통합)
  * CD(지속적 배포)
  * IaC(코드 기반 인프라)
  * Docker, Kubernetes

---

## 2. 코드 품질 & 유지보수

### Clean Code

* 읽기 쉽고 유지보수하기 쉬운 코드
* 원칙:

  * 의미 있는 이름
  * 짧고 단일 책임 함수
  * 중복 제거(DRY)
  * 코드로 설명하고 주석 최소화
  * 일관된 포매팅

### Refactoring

* 기능 변화 없이 코드 내부 구조 개선하는 작업
* 주 기법: 메서드 추출, 변수명 개선, 중복 제거, 클래스 분리
* 클린코드를 지향하는 실제 개선 작업

### Code Inspection

* 개발자 간 코드 리뷰
* 버그, 보안 취약점, 스타일 검사

### Secure Coding

* 보안 취약점을 최소화하는 코딩 기법
* 주요 취약점:

  * SQL Injection → Prepared Statement / ORM
  * XSS → 입력값 검증, escape
  * CSRF → CSRF Token, SameSite Cookie
* 핵심: 입력 검증, 최소 권한, 민감정보 암호화

### TDD (Test Driven Development)

* 테스트 작성 → 코드 작성 → 리팩토링
* 사이클: **Red → Green → Refactor**
* 장점: 안정성↑, 버그 조기 발견, 문서화
* 단점: 초기 개발 시간 증가

---

## 3. 프로그래밍 패러다임

### Imperative (명령형)

* 어떻게(How)를 중심으로 명령 실행
* 상태 변화 기반
* 예: 절차지향, OOP

### Declarative (선언형)

* 무엇(What)을 중심으로 목적만 기술
* 내부 구현보다는 결과 강조
* 예: SQL, 함수형 프로그래밍

---

## 4. 객체지향 프로그래밍 (OOP)

###  4대 특징

| 특징      | 설명                               |
| ------- | -------------------------------- |
| **추상화** | 복잡한 개념을 단순화                      |
| **캡슐화** | 데이터+메서드 묶기, 정보 은닉                |
| **상속**  | 코드 재사용성 증가                       |
| **다형성** | 같은 호출, 다른 동작 (Override/Overload) |

###  SOLID 원칙

* SRP: 단일 책임
* OCP: 확장에는 열려 있고 변경에는 닫힘
* LSP: 자식은 부모를 대체할 수 있어야 함
* ISP: 인터페이스 최소 단위 분리
* DIP: 추상에 의존

---

## 5. 함수형 프로그래밍

* 순수 함수 조합, 부수 효과 최소화
* 특징: 불변성, 선언형 스타일, 고차함수
* Java: Lambda, Stream API
* 장점: 테스트 용이, 병렬 처리 적합

---

## 6. 시스템 아키텍처

### Monolithic

* 하나의 애플리케이션에 기능 모두 포함
* 장점: 배포·개발 단순
* 단점: 유지보수 어려움, 확장성 제한

### MSA (Microservices Architecture)

* 서비스별 독립 배포 + 독립 DB
* 장점: 확장성↑, 장애 격리, 서비스별 기술 선택
* 단점: 운영 복잡도↑, 데이터 일관성 문제, 통신 비용 증가

**MSA 핵심 요소**

* API Gateway
* Service Discovery
* 독립 DB
* 통신 방식 (REST/gRPC/Message Queue)

---

## 7. DevOps 구성요소 요약

| 개념            | 설명          | 도구                      |
| ------------- | ----------- | ----------------------- |
| **CI**        | 빌드/테스트 자동화  | GitHub Actions, Jenkins |
| **CD**        | 배포 자동화      | ArgoCD, Spinnaker       |
| **IaC**       | 인프라를 코드로 관리 | Terraform, Ansible      |
| **Container** | 앱 실행 환경 패키징 | Docker, Kubernetes      |

---

## 8. 3rd Party (써드 파티)

* 외부 개발자가 만든 라이브러리/플러그인
* 예:

  * npm 라이브러리
  * Maven dependency
  * OAuth API
  * 결제/지도 API
* 장점: 개발 시간 절약
* 단점: 의존성 증가, 보안 이슈 가능

---

# 전체 요약

* **Agile/Scrum** → 반복 개발
* **DevOps/CI/CD** → 빠르고 안정적인 배포
* **OOP & FP** → 설계 패러다임
* **Clean Code/Refactoring/Secure Coding** → 유지보수 & 품질
* **TDD** → 테스트 중심 개발
* **MSA** → 확장 가능한 아키텍처
* **3rd Party** → 외부 기술 활용
