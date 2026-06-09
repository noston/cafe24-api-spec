# CASHRECEIPT CANCELLATION


## Cashreceipt cancellation

```json
Endpoints    PUT /api/v2/admin/cashreceipt/{cashreceipt_no}/cancellation
```

```json
PUT /api/v2/admin/cashreceipt/{cashreceipt_no}/cancellation
```

### Cashreceipt cancellation property list

| Attribute | Description |
| --- | --- |
| cashreceipt_no | 현금영수증 번호 |
| order_id | 주문번호 |
| status | 처리상태 신청취소: canceled_request 발행취소: canceled_issuance |

### Update a cash receipt cancellation   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| cashreceipt_noRequired최소값: [1] | 현금영수증 번호 |
| order_idRequired주문번호 | 주문번호 |
| typeRequired | 취소 타입   신청취소: request 발행취소: issue |

```bash
Update a cash receipt cancellation        Update a cash receipt cancellation       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
