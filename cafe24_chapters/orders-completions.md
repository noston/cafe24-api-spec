# ORDERS COMPLETIONS


## Orders completions

```json
Endpoints    POST /api/v2/admin/orders/{order_id}/completions
```

```json
POST /api/v2/admin/orders/{order_id}/completions
```

### Orders completions property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| order_id | 주문번호 |
| payment_code | 결제코드 |
| return_code | 처리 결과 코드 |
| return_message | 처리 결과 메시지 |

### Complete an order after PG payment   cafe24

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
| order_idRequired | 주문번호 |
| payment_codeRequired | 결제코드 |
| dataRequired | 암호화된 PG 결제 데이터 |

```bash
Complete an order after PG payment        Complete an order after PG payment       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
