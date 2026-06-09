# SOCIALS NAVERSHOPPING


## Socials navershopping

```json
Endpoints    GET /api/v2/admin/socials/navershopping
```

```json
GET /api/v2/admin/socials/navershopping
```

### Socials navershopping property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 |
| mall_id Required | 몰아이디 |
| service_status Required | 서비스 상태 T:사용함 F:사용안함 |

### NAVER Shopping settings   cafe24

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
NAVER Shopping settings        NAVER Shopping settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/navershopping' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "navershopping": {        "shop_no": 1,        "mall_id": "samplemall",        "service_status": "T"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/navershopping' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "navershopping": {        "shop_no": 1,        "mall_id": "samplemall",        "service_status": "T"    }}
```
