# TAXMANAGER


## Taxmanager

```json
Endpoints    GET /api/v2/admin/taxmanager
```

```json
GET /api/v2/admin/taxmanager
```

### Taxmanager property list

| Attribute | Description |
| --- | --- |
| use | 세금 관리자 활성화 정보 |

### Retrieve activation information for Tax Manager   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

```bash
Retrieve activation information for Tax Manager        Retrieve activation information for Tax Manager       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/taxmanager' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "taxmanager": {        "use": "T"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/taxmanager' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "taxmanager": {        "use": "T"    }}
```
