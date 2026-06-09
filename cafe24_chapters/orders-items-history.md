# ORDERS ITEMS HISTORY


## Orders items history

```json
Endpoints    GET /api/v2/admin/orders/{order_id}/items/{order_item_code}/history
```

```json
GET /api/v2/admin/orders/{order_id}/items/{order_item_code}/history
```

### Orders items history property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| process_date | 처리일시 |
| previous_order_status | 변경 전 주문상태 |
| current_order_status | 변경 후 주문상태 |
| manager_id | 처리한 운영자 아이디 |
| manager_name | 관리자명 |

### Order item processing history   cafe24 youtube

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
| order_item_codeRequired | 품주코드 |
| start_date | 검색 시작일 |
| end_date | 검색 종료일 |

```bash
Order item processing history        Order item processing history       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
