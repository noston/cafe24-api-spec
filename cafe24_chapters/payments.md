# PAYMENTS


## Payments

```json
Endpoints    PUT /api/v2/admin/payments
```

```json
PUT /api/v2/admin/payments
```

### Payments property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| order_id | 주문번호 |
| status | 주문상태 paid: 입금확인 unpaid: 입금전 canceled: 결제취소 |
| payment_no | 결제번호 |
| auto_paid | 자동입금 여부 T: 자동입금 F: 수동입금 |
| cancel_request | 결제취소 요청 정보 |

### Update payment status for multiple orders   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired | 주문번호 |
| statusRequired | 결제상태   canceled의 경우 앱을 통해 추가된 PG사에서 결제를 취소할 경우에만 사용 가능   paid: 입금확인 unpaid: 입금전 canceled: 결제취소 |
| payment_no최소값: [1] | 결제번호 |
| auto_paid | 자동입금 여부   T: 자동입금 F: 수동입금 |
| recover_inventory | 재고복구   T : 복구함 F : 복구안함 |
| cancel_request | 결제취소 요청 정보 |
| cancel_request 하위 요소 보기     refund_status환불 처리 상태P: 환불완료 F: 환불실패DEFAULT F partial_cancel부분 취소 여부T: 부분취소 F: 전체취소DEFAULT F payment_gateway_name결제 PG사 이름 payment_method결제수단 코드card : 신용카드 tcash : 계좌이체 icash : 가상계좌 cell : 휴대폰 deferpay : 후불 cvs : 편의점 easypay : 간편결제 fpayment : 해외결제 response_code결제 PG 사의 응답 코드 response_message결제 PG 사의 응답 메시지 |

```bash
Update payment status for multiple orders        Update payment status for multiple orders Update the payment status of order to paid Update the payment status of order to unpaid Try to update the payment status of the order which is shipping       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/payments' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "order_id": "20180402-0000032",            "status": "paid",            "payment_no": 10        },        {            "order_id": "20180402-0000013",            "status": "unpaid",            "payment_no": 12        }    ]}'    Response  Copy     {    "payments": [        {            "shop_no": 1,            "order_id": "20180402-0000032",            "status": "paid",            "payment_no": 10,            "cancel_request": {                "refund_status": "F",                "partial_cancel": "F",                "payment_gateway_name": null,                "payment_method": null,                "response_code": null,                "response_message": null            }        },        {            "shop_no": 1,            "order_id": "20180402-0000013",            "status": "unpaid",            "payment_no": 12,            "cancel_request": {                "refund_status": "F",                "partial_cancel": "F",                "payment_gateway_name": null,                "payment_method": null,                "response_code": null,                "response_message": null            }        }    ]}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/payments' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "order_id": "20180402-0000032",            "status": "paid",            "payment_no": 10        },        {            "order_id": "20180402-0000013",            "status": "unpaid",            "payment_no": 12        }    ]}'
```

```json
{    "payments": [        {            "shop_no": 1,            "order_id": "20180402-0000032",            "status": "paid",            "payment_no": 10,            "cancel_request": {                "refund_status": "F",                "partial_cancel": "F",                "payment_gateway_name": null,                "payment_method": null,                "response_code": null,                "response_message": null            }        },        {            "shop_no": 1,            "order_id": "20180402-0000013",            "status": "unpaid",            "payment_no": 12,            "cancel_request": {                "refund_status": "F",                "partial_cancel": "F",                "payment_gateway_name": null,                "payment_method": null,                "response_code": null,                "response_message": null            }        }    ]}
```
