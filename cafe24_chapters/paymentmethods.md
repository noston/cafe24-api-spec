# PAYMENTMETHODS


## Paymentmethods

```json
Endpoints    GET /api/v2/admin/paymentmethods
```

```json
GET /api/v2/admin/paymentmethods
```

### Paymentmethods property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| code | 결제수단 코드 |

### Retrieve a list of payment methods   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve a list of payment methods        Retrieve a list of payment methods       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/paymentmethods' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "paymentmethods": [        {            "shop_no": 1,            "code": "cash"        },        {            "shop_no": 1,            "code": "cod"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/paymentmethods' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "paymentmethods": [        {            "shop_no": 1,            "code": "cash"        },        {            "shop_no": 1,            "code": "cod"        }    ]}
```
