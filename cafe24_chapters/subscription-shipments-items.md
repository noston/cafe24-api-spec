# SUBSCRIPTION SHIPMENTS ITEMS


## Subscription shipments items

```json
Endpoints    PUT /api/v2/admin/subscription/shipments/{subscription_id}/items
```

```json
PUT /api/v2/admin/subscription/shipments/{subscription_id}/items
```

### Subscription shipments items property list

| Attribute | Description |
| --- | --- |
| subscription_item_id | 정기배송 아이템 번호 |
| subscription_state | 정기배송 상태 U:이용중 B:일시정지(구매자신청) Q:일시정지(관리자신청) M:고객해지 A:자동해지 O:관리자해지 |
| quantity | 주문 수량 |
| expected_delivery_date | 배송예정일 |
| subscription_shipments_cycle | 배송주기 1W : 1주 2W : 2주 3W : 3주 4W : 4주 1M : 1개월 2M : 2개월 3M : 3개월 4M : 4개월 5M : 5개월 6M : 6개월 1Y : 1년 |
| changed_variant_code형식 : [A-Z0-9]글자수 최소: [12자]~최대: [12자] | 변경된 옵션 품목코드 |
| max_delivery_limit최소값: [0]최대값: [12] | 정기배송 횟수 0 : 제한없음 2 : 2회 3 : 3회 4 : 4회 6 : 6회 10 : 10회 12 : 12회 |

### Update product variants in subscription   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| subscription_idRequired | 정기배송 신청번호 |
| subscription_item_idRequired최소값: [1] | 정기배송 아이템 번호 |
| subscription_state | 정기배송 상태   U:이용중 Q:일시정지(관리자신청) O:관리자해지 |
| quantity최소값: [1] | 주문 수량 |
| expected_delivery_date날짜 | 배송예정일 |
| subscription_shipments_cycle | 배송주기   1W : 1주 2W : 2주 3W : 3주 4W : 4주 1M : 1개월 2M : 2개월 3M : 3개월 4M : 4개월 5M : 5개월 6M : 6개월 1Y : 1년 |
| changed_variant_code형식 : [A-Z0-9]글자수 최소: [12자]~최대: [12자] | 변경된 옵션 품목코드 |
| max_delivery_limit최소값: [0]최대값: [12] | 정기배송 횟수   0 : 제한없음 2 : 2회 3 : 3회 4 : 4회 6 : 6회 10 : 10회 12 : 12회 |

```bash
Update product variants in subscription        Update product variants in subscription       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
