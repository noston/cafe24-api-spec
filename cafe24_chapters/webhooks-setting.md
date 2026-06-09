# WEBHOOKS SETTING


## Webhooks setting

```json
Endpoints    GET /api/v2/admin/webhooks/setting
PUT /api/v2/admin/webhooks/setting
```

```json
GET /api/v2/admin/webhooks/setting
PUT /api/v2/admin/webhooks/setting
```

### Webhooks setting property list

| Attribute | Description |
| --- | --- |
| scopes | 실시간 정보제공 권한 |
| reception_status | 웹훅 수신 상태 T : 활성화 F : 비활성화 |

### Retrieve webhook settings   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 읽기권한 (mall.read_application) |
| 호출건수 제한 | 40 |

```bash
Retrieve webhook settings        Retrieve webhook settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/webhooks/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "webhook": {        "scopes": [            "mall.read_application",            "mall.read_product"        ],        "reception_status": "T"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/webhooks/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "webhook": {        "scopes": [            "mall.read_application",            "mall.read_product"        ],        "reception_status": "T"    }}
```

### Edit webhook settings   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 쓰기권한 (mall.write_application) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| reception_status | 웹훅 수신 상태   T : 활성화 F : 비활성화 |

```bash
Edit webhook settings        Edit webhook settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/webhooks/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "reception_status": "T"    }}'    Response  Copy     {    "webhook": {        "reception_status": "T"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/webhooks/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "reception_status": "T"    }}'
```

```json
{    "webhook": {        "reception_status": "T"    }}
```
