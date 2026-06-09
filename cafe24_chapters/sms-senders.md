# SMS SENDERS


## Sms senders

```json
Endpoints    GET /api/v2/admin/sms/senders
```

```json
GET /api/v2/admin/sms/senders
```

### Sms senders property list

| Attribute | Description |
| --- | --- |
| sender_no | 발신자 아이디 발신자의 고유한 일련번호 |
| sender | 발신자 번호 발신자의 전화번호 |
| auth_status | 인증 상태 발신자의 전화번호의 인증 상태. 인증완료 상태인 발신자로만 SMS 를 발송할 수 있다. 00 : 삭제 10 : 등록 20 : 심사중 30 : 인증완료 40 : 반려 |
| memo | 메모 request_reason: 요청 사유 reject_reason: 반려 사유 |

### Retrieve a list of SMS senders   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 알림 읽기권한 (mall.read_notification) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   조회하고자 하는 최대 건수를 지정할 수 있음. 예) 10 입력시 10건만 표시함.   DEFAULT 10 |

```bash
Retrieve a list of SMS senders        Retrieve a list of SMS senders Retrieve senders with fields parameter Retrieve senders using paging       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/sms/senders' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "senders": [        {            "sender_no": 3,            "sender": "010-1234-5678",            "auth_status": "30",            "memo": {                "request_reason": "This is a number for emergency sms.",                "reject_reason": "Invalid phone number."            }        },        {            "sender_no": 2,            "sender": "01012345678",            "auth_status": "20",            "memo": {                "request_reason": "This is a number for regular sms.",                "reject_reason": "Invalid request reason."            }        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/sms/senders' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "senders": [        {            "sender_no": 3,            "sender": "010-1234-5678",            "auth_status": "30",            "memo": {                "request_reason": "This is a number for emergency sms.",                "reject_reason": "Invalid phone number."            }        },        {            "sender_no": 2,            "sender": "01012345678",            "auth_status": "20",            "memo": {                "request_reason": "This is a number for regular sms.",                "reject_reason": "Invalid request reason."            }        }    ]}
```
