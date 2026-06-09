# ORDERS EXCHANGE


## Orders exchange

```json
Endpoints    POST /api/v2/admin/orders/{order_id}/exchange
PUT /api/v2/admin/orders/{order_id}/exchange/{claim_code}
```

```json
POST /api/v2/admin/orders/{order_id}/exchange
PUT /api/v2/admin/orders/{order_id}/exchange/{claim_code}
```

### Orders exchange property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| order_id | 주문번호 |
| status | 주문상태 accept : 접수 collected : 수거완료 exchanged : 교환완료 |
| claim_code | 교환번호 |
| items | 품주코드 |
| exchanged_items | 교환상품 |
| pickup_completed | 수거완료 여부 T : 수거완료 F : 수거전 |
| return_invoice_no최대글자수 : [40자] | 반품 송장 번호 |
| return_shipping_company_name최대글자수 : [30자] | 반품 배송업체명 |
| recover_inventory | 재고복구 T : 복구함 F : 복구안함 |
| exchanged_after_collected | 수거완료시 교환완료 여부 T : 사용함 F : 사용안함 |
| request_pickup | 수거신청 여부 T : 사용함 F : 사용안함 |
| pickup | 수거지역 상세 |
| undone | 철회 여부 T : 철회함 F : 철회안함 |
| add_memo_too | 관리자 메모에도 추가 T : 사용함 F : 사용안함 |
| undone_reason_type | 철회 사유 구분 A:고객변심B:배송지연J:배송오류C:배송불가지역L:수출/통관 불가D:포장불량E:상품 불만족F:상품정보상이K:상품불량G:서비스불만족H:품절I:기타 |
| undone_reason | 철회 사유 |
| expose_order_detail | 주문상세내역 노출 여부 T : 노출함 F : 노출안함 |
| exposed_undone_reason | 주문상세내역 노출 철회 사유 |
| carrier_id | 배송사 아이디 |
| return_invoice_success | 반송장 처리 성공 여부 T : 성공 F : 실패 N : 미집하 |
| return_invoice_fail_reason최대글자수 : [100자] | 반송장 처리 실패 사유 |

### Create an order exchange   cafe24 youtube

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
| statusRequired | 주문상태   accepted : 교환접수 exchanged : 교환완료 |
| recover_inventory | 재고복구   T : 복구함 F : 복구안함   DEFAULT F |
| add_memo_too | 관리자 메모에도 추가   T : 사용함 F : 사용안함   DEFAULT F |
| items | 품주코드 |
| items 하위 요소 보기     order_item_codeRequired품주코드 quantityRequired수량 exchange_variant_code(동일상품 다른 옵션 교환시) 교환 상품 품목 코드 |
| same_productRequired | 동일상품교환 여부   T : 동일상품교환 F : 다른상품교환 |

```bash
Create an order exchange        Create an order exchange       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update an order exchange   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired | 주문번호 |
| claim_codeRequired | 교환번호 |
| status | 주문상태   exchanged : 교환완료 |
| pickup_completed | 수거완료 여부   T : 수거완료 F : 수거전 |
| return_invoice_no최대글자수 : [40자] | 반품 송장 번호 |
| return_shipping_company_name최대글자수 : [30자] | 반품 배송업체명 |
| recover_inventory | 재고복구   T : 복구함 F : 복구안함 |
| exchanged_after_collected | 수거완료시 교환완료 여부   T : 사용함 F : 사용안함 |
| items | 품주코드 |
| items 하위 요소 보기     order_item_code품주코드 |
| request_pickup | 수거신청 여부   T : 사용함 F : 사용안함 |
| pickup | 수거지역 상세 |
| pickup 하위 요소 보기     name이름 phone전화번호 cellphone휴대전화 zipcode우편번호 address1기본 주소 address2상세 주소 |
| undone | 철회 여부   T : 철회함 |
| add_memo_too | 관리자 메모에도 추가   T : 사용함 F : 사용안함 |
| undone_reason_type | 철회 사유 구분   A:고객변심B:배송지연J:배송오류C:배송불가지역L:수출/통관 불가D:포장불량E:상품 불만족F:상품정보상이K:상품불량G:서비스불만족H:품절I:기타 |
| undone_reason최대글자수 : [2000자] | 철회 사유 |
| expose_order_detail | 주문상세내역 노출 여부   T : 노출함 F : 노출안함 |
| exposed_undone_reason최대글자수 : [2000자] | 주문상세내역 노출 철회 사유 |
| carrier_id | 배송사 아이디 |
| return_invoice_success | 반송장 처리 성공 여부   T : 성공 F : 실패 N : 미집하 |
| return_invoice_fail_reason최대글자수 : [100자] | 반송장 처리 실패 사유 |

```bash
Update an order exchange        Update an order exchange Update pickup status for exchange Withdraw the exchange       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
