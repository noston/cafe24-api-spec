# SMS


## Sms

```json
Endpoints    POST /api/v2/admin/sms
```

```json
POST /api/v2/admin/sms
```

### Sms property list

| Attribute | Description |
| --- | --- |
| queue_code | 큐 코드 |

### Send a SMS   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 알림 쓰기권한 (mall.write_notification) |
| 호출건수 제한 | 1 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| sender_noRequired | 발신자 아이디   발신자의 고유한 일련번호 |
| contentRequired | 메시지 |
| recipients배열 최대사이즈: [100] | 수신자 전화번호 |
| member_id배열 최대사이즈: [100] | 회원아이디 |
| group_no | 회원등급번호   0 : 전체 등급 |
| exclude_unsubscriber | 수신거부자 제외 발송 여부   수신거부자를 제외하고 발송할지 여부를 설정할 수 있음.   T : 제외 F : 포함   DEFAULT T |
| type | 발송 타입   SMS 의 발송 타입. SMS 는 1건당 최대 90byte 까지 입력 가능하고 90byte 초과 시 여러 개로 나눠서 발송한다. LMS 는 1건당 최대 2000byte 까지 입력 가능하다.   SMS : 단문 LMS : 장문   DEFAULT SMS |
| title | 제목 |

```bash
Send a SMS        Send a SMS Send a SMS to a customer by using member_id field Send a SMS to a customer by using recipients field Try sending a SMS to a customer without using sender_no field Try sending a SMS to a customer without using content field       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/sms' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "sender_no": 2,        "content": "test message",        "member_id": [            "test1",            "test2"        ],        "exclude_unsubscriber": "T",        "type": "SMS"    }}'    Response  Copy     {    "sms": {        "queue_code": "Q1810191529096VAeUD"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/sms' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "sender_no": 2,        "content": "test message",        "member_id": [            "test1",            "test2"        ],        "exclude_unsubscriber": "T",        "type": "SMS"    }}'
```

```json
{    "sms": {        "queue_code": "Q1810191529096VAeUD"    }}
```
