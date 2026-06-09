# ORDERS SHORTAGECANCELLATION


## Orders shortagecancellation

```json
Endpoints    POST /api/v2/admin/orders/{order_id}/shortagecancellation
```

```json
POST /api/v2/admin/orders/{order_id}/shortagecancellation
```

### Orders shortagecancellation property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 |
| order_id | 주문번호 |
| status | 주문상태 canceled : 취소완료 canceling : 취소처리중 |
| claim_code | 취소 번호 |
| items | 품주코드 |

### Create an order cancellation on stock shortage   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 |
| order_idRequired | 주문번호 |
| payment_gateway_cancel | PG 취소 요청 여부   T : 취소함 F : 취소안함   DEFAULT F |
| keep_auto_calculation | 할인금액 자동계산 플래그 보존여부   보존함 : T 제거함 : F   DEFAULT F |
| collect_gift | 사은품 자동 회수   T : 사용함 F : 사용안함   DEFAULT F |
| statusRequired | 주문상태   accepted: 취소접수 canceling : 취소처리중 canceled : 취소완료 |
| recover_inventory | 재고복구   T : 복구함 F : 복구안함   DEFAULT F |
| recover_coupon | 쿠폰 복원   T : 복구함 F : 복구안함   DEFAULT F |
| recover_coupon_no | 복원할 쿠폰 번호 |
| add_memo_too | 관리자 메모에도 추가   T : 사용함 F : 사용안함   DEFAULT F |
| reason최대글자수 : [2000자] | 취소사유 |
| claim_reason_type | 취소사유 구분   A : 고객변심 B : 배송지연 C : 배송불가지역 L : 수출/통관 불가 D : 포장불량 E : 상품불만족 F : 상품정보상이 G : 서비스불만족 H : 품절 I : 기타 |
| naverpay_cancel_reason_type | 네이버페이 취소사유 구분   EC 베트남, 필리핀 버전에서는 사용할 수 없음.   51 : 구매 의사 취소 52 : 색상 및 사이즈 변경 53 : 다른 상품 잘못 주문 54 : 서비스 및 상품 불만족 55 : 배송 지연 56 : 상품 품절 60 : 상품 정보 상이 |
| kakaopay_cancel_reason_type | 카카오페이 취소사유 구분   K1 : 변심에 의한 상품 취소 K2 : 다른 옵션이나 상품을 잘못 주문함 K3 : 배송지연 K4 : 상품 파손 또는 불량 K5 : 다른 상품 오배송 또는 구성품 누락 K6 : 상품정보와 다름 K7 : 품절로 인한 배송 불가 |
| refund_method_code | 환불 방식   T : 현금 F : 신용카드 M : 적립금 G : 계좌이체 C : 휴대폰 D : 예치금 Z : 후불 O : 선불금 V : 편의점 J : 제휴상품권 K : 제휴포인트 I : 기타 |
| refund_bank_code | 환불 은행 코드 |
| refund_bank_name최대글자수 : [250자] | 환불은행명 |
| refund_bank_account_no | 환불 계좌번호 |
| refund_bank_account_holder최대글자수 : [15자] | 환불계좌 예금주 명의 |
| items | 품주코드 |
| items 하위 요소 보기     order_item_codeRequired품주코드 quantityRequired수량 |

```bash
Create an order cancellation on stock shortage        Create an order cancellation on stock shortage Cancel the order by using only required fields Try cancel the order when order status is 'In transit' Try cancel the order by without refund_method_code field       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
