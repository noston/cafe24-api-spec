# ORDERS DASHBOARD


## Orders dashboard

```json
Endpoints    GET /api/v2/admin/orders/dashboard
```

```json
GET /api/v2/admin/orders/dashboard
```

### Orders dashboard property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| cancellation_request_count | 취소신청 건수 |
| cancellation_received_count | 취소접수 건수 |
| cancellation_processing_count | 취소처리중 건수 |
| exchange_request_count | 교환신청 건수 |
| exchange_received_count | 교환접수 건수 |
| exchange_processing_count | 교환처리중 건수 |
| return_request_count | 반품신청 건수 |
| return_received_count | 반품접수 건수 |
| return_processing_count | 반품처리중 건수 |
| refund_pending_count | 환불전 건수 |
| total_order_amount | 총 주문 금액 |
| total_paid_amount | 총 실 결제금액 |
| total_refund_amount | 총 환불금액 |
| total_order_count | 총 주문금액 건수 |
| total_paid_count | 총 실결제 금액 건수 |
| total_refund_count | 총 환불금액 건수 |

### List all orders dashboard   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
List all orders dashboard        List all orders dashboard       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/dashboard' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "dashboard": {        "shop_no": 1,        "cancellation_request_count": 10,        "cancellation_received_count": 5,        "cancellation_processing_count": 5,        "exchange_request_count": 8,        "exchange_received_count": 3,        "exchange_processing_count": 3,        "return_request_count": 12,        "return_received_count": 6,        "return_processing_count": 6,        "refund_pending_count": 20,        "total_order_amount": "1500000.00",        "total_paid_amount": "120000.00",        "total_refund_amount": "100000.00",        "total_order_count": 50,        "total_paid_count": 40,        "total_refund_count": 10    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/dashboard' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "dashboard": {        "shop_no": 1,        "cancellation_request_count": 10,        "cancellation_received_count": 5,        "cancellation_processing_count": 5,        "exchange_request_count": 8,        "exchange_received_count": 3,        "exchange_processing_count": 3,        "return_request_count": 12,        "return_received_count": 6,        "return_processing_count": 6,        "refund_pending_count": 20,        "total_order_amount": "1500000.00",        "total_paid_amount": "120000.00",        "total_refund_amount": "100000.00",        "total_order_count": 50,        "total_paid_count": 40,        "total_refund_count": 10    }}
```
