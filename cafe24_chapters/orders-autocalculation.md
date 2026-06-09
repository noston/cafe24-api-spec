# ORDERS AUTOCALCULATION


## Orders autocalculation

```json
Endpoints    DELETE /api/v2/admin/orders/{order_id}/autocalculation
```

```json
DELETE /api/v2/admin/orders/{order_id}/autocalculation
```

### Orders autocalculation property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 DEFAULT 1 |
| order_id | 주문번호 |

### Remove auto calculation setting of an order   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |

```bash
Remove auto calculation setting of an order        Remove auto calculation setting of an order       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
