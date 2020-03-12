# Chapter 1. Introduction to open source compliance
본 챕터에서는 오픈소스 컴플라이언스가 무엇인지 간단하게 소개하고, 컴플라이언스를 준수하지 않았을 때 발생할 수 있는 이슈들을 설명합니다.
<br>
<br>


## 비즈니스 환경의 변화

| 구분 | 과거 | 현재 |
|------|------|------|
| 개발환경 | 독점 소프트웨어 또는 상용 소프트웨어를 사용하여 개발 | 오픈소스 소프트웨어를 사용하여 개발 |
| 이점 | - 리스크를 예측할 수 있음 <br> - 벤더들과 협상하여 리스크를 완화시킬 수도 있음 | - 오픈소스는 time-to-market이 짧음 <br> - 소스코드를 커스터마이징할 수 있음 <br> - 별도의 계약 없이 자유롭게 선택 가능 |


**변화의 결과** <br>
개발환경의 변화로 소스코드가 다양한 조합으로 개발
-	회사에서 자체 개발한 독점 코드
-	상용 소프트웨어를 구매하여 개발한 3rd Party 코드
-	오픈소스를 사용하여 만들었지만 다시 기여하지 않는 코드
-	오픈소스를 사용하여 만들고 다시 오픈소스로 공개하는 코드 등

> 이전에는 기업 간 계약을 통해 라이선스 협상을 했으나, 이제는 **컴플라이언스 정책과 개발 방식**으로 라이선스를 관리해야 함
<br>


## 오픈소스 컴플라이언스 준수
### 1. 오픈소스 컴플라이언스란?
- 오픈소스 라이선스 의무사항을 이행하는 것
- 오픈소스를 상용 제품에 효과적으로 사용하도록 권장하는 것
- 3rd Party 소프트웨어 공급자와 계약 의무사항을 준수하는 것
- 지적 재산권을 보호하는 것

### 2. 오픈소스 컴플라이언를 준수한다는 것은?
오픈소스를 개발하는 사람, 사용하는 사람, 통합하는 사람들이 저작권과 라이선스 의무사항을 만족시키는 것임

### 3. 오픈소스 컴플라이언스를 준수함으로써 얻는 이익
- 레퍼런스를 가질 수 있기 때문에 서비스, 테스트, 업데이트, 유지보수 할 때 **기술적 이점**을 얻을 수 있음
- 여러 제품들이 **공통적으로 사용하고 있는 오픈소스를 식별**할 수 있고 **조직에 유익한 오픈소스가 무엇인지** 알 수 있음
- 오픈소스 검토에 필요한 **비용과 시간에 대한 레퍼런스**를 쌓을 수 있음
<br>


## 오픈소스 컴플라이언스를 준수하지 않은 사례
- Attribution Notice 제공하지 않을 때
- License 제공하지 않을 때
- Copyright 제공하지 않을 때
- Modification 고지하지 않을 때 (GPL, LGPL)

  >  Modification 고지 예시
  >  ```
  >  /*
  >  * Date 10/15/2015
  >  * Author Ibrahim Haddad
  >  * Comment Fixed memory leak in nextlst()
  >  */
  >  ```

- 소스코드를 제공하지 않을 때 (GPL, LGPL)
- Written offer를 제공하지 않을 때 (GPL. LGPL)

  > Written Offer 예시
  > ```
  > To obtain a copy of the source code being made publicly available by FooBar, Inc. related
  > to software used in this product, you can visit http://opensource.foobar.com
  > or send your request in writing by email to
  > opensource@foobar.com or by regular postal mail to:
  >
  > FooBar Inc. Open Source Program Office Street Address
  > City, State, Postal Code Country
  > ```

- Build Script를 제공하지 않을 때 (GPL, LGPL)
<br>


## 컴플라이언스를 준수하지 않아서 발생할 수 있는 이슈들

### 1. 지적재산권 이슈
| 문제 유형 | 확인 방법 | 예방법 |
|------|------|------|
| <p align="center"><img src="/image/chapter1/opensource-1.png" width="200" style="float:"></p> <br> 오픈소스를 독점코드에 포함시키는 경우, <br> 개발자가 오픈소스 코드 스니펫만 복사하여 붙여넣기 했을 때 | 소스코드 스캔 | - 오픈소스 컴플라이언스에 대한 심각성 알리기 <br> - 정기적인 소스코드 스캔 <br> - 오픈소스 사전 승인 의무화 |
| <p align="center"><img src="/image/chapter1/opensource-2.png" width="200" style="float:"></p><br> 오픈소스를 독점 코드와 결합하는 경우, <br> 양립할 수 없는 라이선스를 결합시킬 때 | 디펜던시 추적 툴로 확인 | - 기업의 컴플라이언스 정책에 결합 방식을 가이드해야 함 <br> - 주기적으로 디펜던시 추적 툴로 결합방식 검증 |
| <p align="center"><img src="/image/chapter1/opensource-3.png" width="200" style="float:"></p><br> 독점 코드를 오픈소스 코드에 포함시키는 경우, <br> 개발자가 독점 코드를 복사해서 붙여넣기 했을 때 | 소스코드 스캔 | - 사내 교육 <br> - 정기적인 소스코드 검사 <br> - 독점 코드를 포함시킬 때 사전 승인 |

**지적재산권 이슈로 인해 발생하는 결과**
- 제품 출시 금지
- 바이너리 소스코드 제공
- 재개발

### 2. 라이선스 이슈
| 문제 유형 | 예방법 |
|------|------|
| 소스코드를 배포하지 않은 경우 | - 정식 배포 전에 체크리스트를 거쳐야 함 |
| 배포된 버전과 일치하지 않은 소스코드를 배포했을 때 | - 소스코드를 배포할 때 정확하게 일치한 버전인지 검증 절차를 거쳐야 함 |
| 수정된 버전에 대해 오픈소스 라이선스 공지를 하지 않은 경우 | - BOM 관리 툴로 업데이트 버전과 기존 버전과의 차이점을 추적 및 관리해야 함 <br> - 업데이트 버전에 대해 재 검증 <br> - 체크리스트에 소스코드의 diff를 검증하는 단계를 추가해야 함 |
| 수정된 소스코드를 표시하지 않거나 수정 고지를 하지 않은 경우 | - 소스코드 배포 전에 체크리스트로 확인 및 소스코드 검사 <br> - 컴플라이언스 준수 절차에 수정된 소스코드를 확인하는 단계 추가하기 <br> - 개발자들에게 소스코드 change log를 기록하도록 교육하기 |

**라이선스 이슈로 인해 발생하는 결과**
- 소스코드를 공개할 때까지 제품 출시 금지
- 배포된 제품의 바이너리 버전과 소스코드 버전이 다르기 때문에 고객 지원 불가
- 나쁜 평판

### 3. 컴플라이언스 프로세스를 이행하지 않아서 발생하는 이슈
| 문제 유형 | 예방법 |
|------|------|
| 개발자가 오픈소스 사용에 대한 승인 요청을 하지 않거나 적절한 기간 내에 요청하지 못한 경우 | - 직원들에게 정책과 절차 교육 <br> - 정기적인 소스코드 스캔(컴플라이언스에 부합하지 않는 소스코드 사용이 발견되면 자동 티켓 발행) <br> - 성과 평가에 컴플라이언스 준수 항목 추가 <br> - 개발 초기에 오픈소스 사용 승인 의무화 |
| 오픈소스 교육이 되어 있지 않은 경우 | - 개발자의 개발 계획에 오픈소스 교육을 이수했다는 것이 보증되어야 함 <br> - 성과 평가 시 오픈소스 교육 이수 여부가 포함되어 있어야 함 |
| 소스코드 검증이 되지 않은 경우 | - 컴플라이언스 업무를 담당하는 직원의 교육 <br> - 정기적인 소스코드 스캔 <br> - 개발 마일스톤에 소스코드 검증이 포함되어 있어야 함 <br> - 소스코드 감사 부서에 적절한 인력 배치 필요 |
| 검증에서 발견된 이슈를 해결하지 못한 경우 | - 이슈가 완전히 해결되기 전까지 티켓을 resolved 시키지 않기 <br> - 모든 subtask가 해결되어야 종료 처리 |
<br>


## Lessons Learned
### 1. 제품이 배포되기 전에 컴플라이언스를 준수했음이 보장되어야 한다.
- 제품과 서비스 및 내부 개발 시 사용되는 모든 오픈소스 식별
- 라이선스 의무사항이 독점 및 3rd party 소프트웨어 구성 요소로 확장되는지 확인하기 위해 아키텍처 검토 수행
- 법무팀이 검토할 수 있도록 오픈소스 라이선스 취합
- 오픈소스 사용 및 배포 정책 수립
- 아키텍처 설계 및 개발 사례를 제공하여 위험 완화

### 2. 컴플라이언스를 준수하지 않으면 결국 비용이 많이 든다.
- 문제가 되는 것은 보통 GPL 관련 라이선스 이슈이기 때문에 GPL/LGPL과 관련된 컴플라이언스 정책을 명확히 수립하고 준수하는 것이 필요함
  - 컴플라이언스 책임자를 임명하여 공식 컴플라이언스 프로그램을 수립하고 지속적으로 컴플라이언스를 모니터링 및 보장
  - 컴플라이언스를 준수하지 않았던 버전의 제품을 사용하고 있는 고객에게 오픈소스 소프트웨어가 포함되어 있음을 알리고 해당 소프트웨어의 의무사항과 권리를 알려야 함
  - 웹 사이트 및 제품에 라이선스 고지문 게시
  - 모든 수정 사항을 포함하여 소스 코드 제공 (코드 공개 요구 사항이 있는 GPL / LGPL 라이선스 제품군 및 유사 라이선스에만 해당)
  - 완전히 소스코드를 공개할 때까지 해당 오픈소스 소프트웨어의 바이너리 배포 중단
  - 어떤 경우에는 소스코드를 공개하지 않기 위해 원저작자에게 배상금 지불

### 3. 오픈소스 커뮤니티와의 관계도 중요하다.
-  컴플라이언스를 준수하면 오픈소스 커뮤니티에서도 존중을 받는다고 느낌
-  컴플라이언스를 준수한다는 것은 오픈소스 커뮤니티에서 가치 있는 일로 여겨짐

### 4. 교육이 중요하다.
- 컴플라이언스 프로그램에서 중요한 요소는 직원 교육
- 소프트웨어 개발에 관련된 모든 직원들은 회사의 정책과 절차를 이해해야 함