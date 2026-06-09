# CONTROL


## Control

```json
Endpoints    PUT /api/v2/admin/control
```

```json
PUT /api/v2/admin/control
```

### Control property list

| Attribute | Description |
| --- | --- |
| payments_control | 주문 입금확인 제한여부 |
| direct_url | 연결 URL |

### Order control   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| payments_controlRequired | 주문 입금확인 제한여부   T:사용함  F:사용안함 |
| direct_urlRequiredURL | 연결 URL |

```bash
Order control        Order control       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/control' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "payments_control": "T",        "direct_url": "https://samplemall.cafe24.com/disp/admin/myapps/list"    }}'    Response  Copy     {    "control": {        "payments_control": "T",        "direct_url": "https://samplemall.cafe24.com/disp/admin/myapps/list"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/control' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "payments_control": "T",        "direct_url": "https://samplemall.cafe24.com/disp/admin/myapps/list"    }}'
```

```json
{    "control": {        "payments_control": "T",        "direct_url": "https://samplemall.cafe24.com/disp/admin/myapps/list"    }}
```
