# COLLECTREQUESTS


## Collectrequests

```json
Endpoints    PUT /api/v2/admin/collectrequests/{request_no}
```

```json
PUT /api/v2/admin/collectrequests/{request_no}
```

### Collectrequests property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| request_no | 요청 번호 |
| order_id | 주문번호 |
| order_item_code | 품주코드 |
| shipping_company_name | 수거 배송사명 |
| collect_tracking_no | 수거 송장 번호 |

### Update a collection request   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 30 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| request_noRequired | 요청 번호 |
| collect_tracking_noRequired최대글자수 : [40자] | 수거 송장 번호 |

```bash
Update a collection request        Update a collection request       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/collectrequests/10' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "collect_tracking_no": "636945749436"    }}'    Response  Copy     {    "collectrequest": {        "shop_no": 1,        "request_no": 10,        "order_id": "20210101-0000001",        "order_item_code": [            "20210101-0000001-01",            "20210101-0000001-02"        ],        "shipping_company_name": "KOREA EXPRESS",        "collect_tracking_no": "636945749436"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/collectrequests/10' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "collect_tracking_no": "636945749436"    }}'
```

```json
{    "collectrequest": {        "shop_no": 1,        "request_no": 10,        "order_id": "20210101-0000001",        "order_item_code": [            "20210101-0000001-01",            "20210101-0000001-02"        ],        "shipping_company_name": "KOREA EXPRESS",        "collect_tracking_no": "636945749436"    }}
```
