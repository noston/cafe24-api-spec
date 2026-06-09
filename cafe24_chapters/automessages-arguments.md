# AUTOMESSAGES ARGUMENTS


## Automessages arguments

```json
Endpoints    GET /api/v2/admin/automessages/arguments
```

```json
GET /api/v2/admin/automessages/arguments
```

### Automessages arguments property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 DEFAULT 1 |
| name | 변수명 |
| description | 변수 설명 |
| sample | 변수 예제 |
| string_length | 메시지 표시 최대 글자수 글자수 : 설정된 글자수 만큼 표시 가변 : 글자수 제한 없이 모두 표시 |
| send_case | 사용 가능 발송 상황 |

### Retrieve the list of available variables for automated messages   cafe24 youtube

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
Retrieve the list of available variables for automated messages        Retrieve the list of available variables for automated messages       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/automessages/arguments' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "arguments": [        {            "shop_no": 1,            "name": "[NAME]",            "description": "Customer name",            "sample": "John Doe",            "string_length": "3",            "send_case": "All occasions"        },        {            "shop_no": 1,            "name": "[PRODUCT]",            "description": "Product name",            "sample": "iPhone X",            "string_length": "8",            "send_case": "Back-in-stock notification (Manual), Notification on shipment, Successful delivery, or Refund"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/automessages/arguments' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "arguments": [        {            "shop_no": 1,            "name": "[NAME]",            "description": "Customer name",            "sample": "John Doe",            "string_length": "3",            "send_case": "All occasions"        },        {            "shop_no": 1,            "name": "[PRODUCT]",            "description": "Product name",            "sample": "iPhone X",            "string_length": "8",            "send_case": "Back-in-stock notification (Manual), Notification on shipment, Successful delivery, or Refund"        }    ]}
```
