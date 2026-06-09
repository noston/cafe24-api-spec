# SMS SETTING


## Sms setting

```json
Endpoints    GET /api/v2/admin/sms/setting
PUT /api/v2/admin/sms/setting
```

```json
GET /api/v2/admin/sms/setting
PUT /api/v2/admin/sms/setting
```

### Sms setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| use_sms | SMS 사용 여부 T: 사용함 F: 사용안함 |
| exclude_unsubscriber | 수신거부자 제외 발송 여부 T : 제외 F : 포함 |
| default_sender | 기본 발신번호 |
| unsubscribe_phone | 무료 수신거부 전화번호 |
| send_method | SMS 발송방법 S: 단문 분할발송 L: 장문발송(3건 차감) |
| send_method_automatic | SMS 발송방법 (자동) L: 장문발송(3건차감) S: 단문 분할발송 N: 단문발송 |

### Retrieve SMS settings   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve SMS settings        Retrieve SMS settings Try to retrieve SMS setting for the shop that does not provide SMS service       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/sms/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "sms": {        "shop_no": 1,        "use_sms": "F",        "exclude_unsubscriber": "T",        "default_sender": "01012345678",        "unsubscribe_phone": "01012345678",        "send_method": "S",        "send_method_automatic": "L"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/sms/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "sms": {        "shop_no": 1,        "use_sms": "F",        "exclude_unsubscriber": "T",        "default_sender": "01012345678",        "unsubscribe_phone": "01012345678",        "send_method": "S",        "send_method_automatic": "L"    }}
```

### Update SMS settings   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| use_sms | SMS 사용 여부   T: 사용함 F: 사용안함 |
| exclude_unsubscriber | 수신거부자 제외 발송 여부   T : 제외 F : 포함 |
| default_sender최대글자수 : [14자] | 기본 발신번호 |
| unsubscribe_phone최대글자수 : [14자] | 무료 수신거부 전화번호 |
| send_method | SMS 발송방법   S: 단문 분할발송 L: 장문발송(3건 차감) |
| send_method_automatic | SMS 발송방법 (자동)   L: 장문발송(3건차감) S: 단문 분할발송 N: 단문발송 |

```bash
Update SMS settings        Update SMS settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/sms/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_sms": "F",        "exclude_unsubscriber": "T",        "default_sender": "01012345678",        "unsubscribe_phone": "01012345678",        "send_method": "S",        "send_method_automatic": "L"    }}'    Response  Copy     {    "sms": {        "shop_no": 1,        "use_sms": "F",        "exclude_unsubscriber": "T",        "default_sender": "01012345678",        "unsubscribe_phone": "01012345678",        "send_method": "S",        "send_method_automatic": "L"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/sms/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_sms": "F",        "exclude_unsubscriber": "T",        "default_sender": "01012345678",        "unsubscribe_phone": "01012345678",        "send_method": "S",        "send_method_automatic": "L"    }}'
```

```json
{    "sms": {        "shop_no": 1,        "use_sms": "F",        "exclude_unsubscriber": "T",        "default_sender": "01012345678",        "unsubscribe_phone": "01012345678",        "send_method": "S",        "send_method_automatic": "L"    }}
```
