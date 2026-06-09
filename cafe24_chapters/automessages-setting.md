# AUTOMESSAGES SETTING


## Automessages setting

```json
Endpoints    GET /api/v2/admin/automessages/setting
PUT /api/v2/admin/automessages/setting
```

```json
GET /api/v2/admin/automessages/setting
PUT /api/v2/admin/automessages/setting
```

### Automessages setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 DEFAULT 1 |
| use_sms | SMS 사용 여부 T: 사용함 F: 사용안함 |
| use_kakaoalimtalk | 카카오알림톡 사용 여부 T: 사용함 F: 사용안함 |
| use_push | PUSH 사용 여부 T: 사용함 F: 사용안함 |
| send_method | 자동 발송 메시지 발송 방법 S: SMS K: 카카오알림톡(발송 실패 시 SMS로 대체 발송) |
| send_method_push | 푸시 수신 대상에게 푸시 우선 발송 여부 T : 우선 발송함 F : 우선 발송 안함 |

### Retrieve the automated message settings   cafe24 youtube

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
Retrieve the automated message settings        Retrieve the automated message settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/automessages/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "automessages": {        "shop_no": 1,        "use_sms": "T",        "use_kakaoalimtalk": "T",        "use_push": "T",        "send_method": "S",        "send_method_push": "F"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/automessages/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "automessages": {        "shop_no": 1,        "use_sms": "T",        "use_kakaoalimtalk": "T",        "use_push": "T",        "send_method": "S",        "send_method_push": "F"    }}
```

### Update an automated message   cafe24 youtube

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
| send_methodRequired | 자동 발송 메시지 발송 방법   S: SMS K: 카카오알림톡(발송 실패 시 SMS로 대체 발송) |
| send_method_push | 푸시 수신 대상에게 푸시 우선 발송 여부   Youtube shopping 이용 시에는 미제공   T : 우선 발송함 F : 우선 발송 안함 |

```bash
Update an automated message        Update an automated message       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/automessages/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "send_method": "S",        "send_method_push": "F"    }}'    Response  Copy     {    "automessages": {        "shop_no": 1,        "send_method": "S",        "send_method_push": "F"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/automessages/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "send_method": "S",        "send_method_push": "F"    }}'
```

```json
{    "automessages": {        "shop_no": 1,        "send_method": "S",        "send_method_push": "F"    }}
```
