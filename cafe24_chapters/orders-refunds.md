# ORDERS REFUNDS


## Orders refunds

```json
Endpoints    PUT /api/v2/admin/orders/{order_id}/refunds/{refund_code}
```

```json
PUT /api/v2/admin/orders/{order_id}/refunds/{refund_code}
```

### Orders refunds property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| refund_code | 환불번호 |
| status | 환불상태 |
| reason | 처리사유 |

### Update an order refund   cafe24 youtube

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
| refund_codeRequired | 환불번호 |
| statusRequired | 환불상태   complete : 환불완료 |
| reason최대글자수 : [2000자] | 처리사유 |
| send_sms | 환불처리후 SMS 발송 여부   T : 발송함 F : 발송안함   DEFAULT T |
| send_mail | 환불처리후 메일 발송 여부   T : 발송함 F : 발송안함   DEFAULT T |
| payment_gateway_cancel | PG 취소 요청 여부   T : 취소함 F : 취소안함   DEFAULT F |

```bash
Update an order refund        Update an order refund Try refund order that has been already refunded Try refund order with wrong refund_code Try refund when order does not supports PG cancel       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
