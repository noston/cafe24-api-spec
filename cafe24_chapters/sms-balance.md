# SMS BALANCE


## Sms balance

```json
Endpoints    GET /api/v2/admin/sms/balance
```

```json
GET /api/v2/admin/sms/balance
```

### Sms balance property list

| Attribute | Description |
| --- | --- |
| balance | SMS 잔여 건수 |
| sms_count | 단문(SMS) 발송 가능 건수 |
| lms_count | 장문(LMS) 발송 가능 건수 |

### Retrieve the SMS balance   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 알림 읽기권한 (mall.read_notification) |
| 호출건수 제한 | 40 |

```bash
Retrieve the SMS balance        Retrieve the SMS balance       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/sms/balance' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "sms": {        "balance": "10.3",        "sms_count": 10,        "lms_count": 3    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/sms/balance' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "sms": {        "balance": "10.3",        "sms_count": 10,        "lms_count": 3    }}
```
