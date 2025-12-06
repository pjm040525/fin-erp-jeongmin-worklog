# fin-erp-jeongmin-worklog
# Mini ERP - 정민 작업 기록 저장소

이 저장소는 **Mini ERP 프로젝트에서 제가 개발한 기능과 작업 과정**을 기록하기 위해 만들어졌습니다.

---

## 👤 개발자 정보
- 이름: 박정민
- 역할: 조직/예산 담당 (Foundation & Planning)

---

## 📌 수행한 기능 목록

### ✔ 1) Company / Department / Budget 기능 개발
- 회사 자동 세팅 (CP-001)
- 부서 CRUD
- 예산 등록 / 조회 / 수정 / 삭제
- 중복 방지 로직 구현

---

## 🔍 구현 핵심

### 예산 중복 방지 로직
```java
if (budgetDAO.exists(deptId, glAccountId, yearMonth))
    throw new IllegalArgumentException("이미 등록된 예산입니다");
