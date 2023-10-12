# 키친포스

## 요구 사항

### 상품
- 상품을 등록할 수 있다.
  - 상품의 가격은 0 원 이상이어야 한다.
- 상품의 모든 목록을 조회할 수 있다.

### 메뉴 그룹
- 메뉴 그룹을 등록할 수 있다.
- 모든 메뉴 그룹 목록을 불러 올 수 있다.

### 메뉴
- 메뉴를 등록할 수 있다.
  - 메뉴의 가격은 0 원 이상이어야 한다.
  - 메뉴를 등록할때는 메뉴그룹에 속해야한다.
  - 메뉴의 가격은 총 메뉴상품의 (가격 *장 수량)의 총합 보다 클 수 없다. 
- 모든 메뉴 목록을 불러 올 수 있다.

### 주문 테이블
- 주문 테이블을 등록할 수 있다.
- 모든 주문 테이블을 불러 올 수 있다.
- 주문 테이블을 빈 테이블로 설정 할 수 있다.
  - 단체 지정이 되어있으면 설정 할 수 없다.
  - 주문 상태가 계산 완료 상태일때만 설정 할 수 있다.
- 주문 테이블의 방문한 손님 수를 변경 할 수 있다.
  - 0명 이상으로만 변경 할 수 있다.
  - 빈 테이블이면 변경 할 수 없다.

### 주문
- 주문을 할 수 있다.
  - 주문 테이블이 존재해야 한다.
  - 빈 테이블에서는 주문 할 수 없다.
  - 1개 이상 메뉴가 존재해야 한다.
  - 주문을 하면 상태는 조리 상태가 된다.
- 모든 주문 목록을 불러 올 수 있다.
- 주문 상태를 변경 할 수 있다.
  - 계산 완료 상태일때는 상태를 변경 할 수 없다.

### 단체 지정
- 단체 지정을 등록 할 수 있다.
  - 주문 테이블이 2개 이상일때 등록 할 수 있다.
  - 주문 테이블이 이미 단체 지정으로 등록 되어있으면 등록 할 수 없다.
  - 주문 테이블이 빈 테이블이면 등록 할 수 없다.
- 단체 지정을 해제 할 수 있다.
  - 주문 테이블이 계산 완료 상태일때만 헤제 할 수 있다.

## 용어 사전

| 한글명 | 영문명 | 설명 |
| --- | --- | --- |
| 상품 | product | 메뉴를 관리하는 기준이 되는 데이터 |
| 메뉴 그룹 | menu group | 메뉴 묶음, 분류 |
| 메뉴 | menu | 메뉴 그룹에 속하는 실제 주문 가능 단위 |
| 메뉴 상품 | menu product | 메뉴에 속하는 수량이 있는 상품 |
| 금액 | amount | 가격 * 수량 |
| 주문 테이블 | order table | 매장에서 주문이 발생하는 영역 |
| 빈 테이블 | empty table | 주문을 등록할 수 없는 주문 테이블 |
| 주문 | order | 매장에서 발생하는 주문 |
| 주문 상태 | order status | 주문은 조리 ➜ 식사 ➜ 계산 완료 순서로 진행된다. |
| 방문한 손님 수 | number of guests | 필수 사항은 아니며 주문은 0명으로 등록할 수 있다. |
| 단체 지정 | table group | 통합 계산을 위해 개별 주문 테이블을 그룹화하는 기능 |
| 주문 항목 | order line item | 주문에 속하는 수량이 있는 메뉴 |
| 매장 식사 | eat in | 포장하지 않고 매장에서 식사하는 것 |
