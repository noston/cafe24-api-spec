# ORDERS BUYER HISTORY


## Orders buyer history

```json
Endpoints    GET /api/v2/admin/orders/{order_id}/buyer/history
```

```json
GET /api/v2/admin/orders/{order_id}/buyer/history
```

### Orders buyer history property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 |
| name | 주문자명 |
| email이메일 | 주문자 이메일 |
| phone | 주문자 일반 전화 |
| cellphone | 주문자 휴대 전화 |
| customer_notification | 고객 알림 |
| updated_date | 수정일 |
| user_id | 주문자 수정자 ID |
| user_name | 주문자 수정자 명 |

### Retrieve a list of customer history of an order   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |

```bash
Retrieve a list of customer history of an order        Retrieve a list of customer history of an order Retrieve history with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
