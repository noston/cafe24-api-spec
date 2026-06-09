# ORDERS EXCHANGEREQUESTS


## Orders exchangerequests

```json
Endpoints    PUT /api/v2/admin/orders/{order_id}/exchangerequests
```

```json
PUT /api/v2/admin/orders/{order_id}/exchangerequests
```

### Orders exchangerequests property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| order_id | 주문번호 |
| undone | 접수거부 여부 |
| order_item_code | 품주코드 |
| additional_payment_gateway_cancel | 추가 PG 취소 |

### Reject an exchange request   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |
| order_item_codeRequired | 품주코드 |
| undoneRequired | 접수거부 여부   T : 접수거부함 |
| reason_type | 사유 구분   A:고객변심B:배송지연J:배송오류C:배송불가지역L:수출/통관 불가D:포장불량E:상품 불만족F:상품정보상이K:상품불량G:서비스불만족H:품절I:기타 |
| reason최대글자수 : [2000자] | 사유 |
| display_reject_reason | 주문상세내역 노출설정   T : 노출함 F : 노출안함   DEFAULT F |
| reject_reason최대글자수 : [2000자] | 거부 사유   고객에게 노출되는 접수 거부 사유 |

```bash
Reject an exchange request        Reject an exchange request       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
