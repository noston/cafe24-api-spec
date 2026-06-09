# POINTS AUTOEXPIRATION


## Points autoexpiration

```json
Endpoints    GET /api/v2/admin/points/autoexpiration
POST /api/v2/admin/points/autoexpiration
DELETE /api/v2/admin/points/autoexpiration
```

```json
GET /api/v2/admin/points/autoexpiration
POST /api/v2/admin/points/autoexpiration
DELETE /api/v2/admin/points/autoexpiration
```

### Points autoexpiration property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| expiration_date | 최초 소멸 시행일 |
| interval_month | 소멸 실행 주기 1: 1개월 3: 3개월 6: 6개월 12: 1년 |
| target_period_month | 소멸 대상 적립금 6: 소멸일 기준 6개월 이전 적립금 12: 소멸일 기준 1년 이전 적립금 18: 소멸일 기준 1년 6개월 이전 적립금 24: 소멸일 기준 2년 이전 적립금 30: 소멸일 기준 2년 6개월 이전 적립금 36: 소멸일 기준 3년 이전 적립금 |
| group_no | 소멸 대상 회원등급 0: 전체 회원 |
| standard_point | 소멸 대상 기준 금액 |
| send_email | 이메일 발송 T: 설정함 F: 설정안함 |
| send_sms | SMS 발송 T: 설정함 F: 설정안함 |
| notification_time_day | 알람시기 선택 3: 3일 전 발송 7: 7일 전 발송 15: 15일 전 발송 30: 1개월 전 발송 |

### Retrieve an automatic points expiration   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 적립금 읽기권한 (mall.read_mileage) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve an automatic points expiration        Retrieve an automatic points expiration       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/points/autoexpiration' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "autoexpiration": {        "shop_no": 1,        "expiration_date": "2021-01-26",        "interval_month": 1,        "target_period_month": 12,        "group_no": 0,        "standard_point": "10.00",        "send_email": "T",        "send_sms": "F",        "notification_time_day": [            3,            7        ]    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/points/autoexpiration' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "autoexpiration": {        "shop_no": 1,        "expiration_date": "2021-01-26",        "interval_month": 1,        "target_period_month": 12,        "group_no": 0,        "standard_point": "10.00",        "send_email": "T",        "send_sms": "F",        "notification_time_day": [            3,            7        ]    }}
```

### Create an automatic points expiration   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 적립금 쓰기권한 (mall.write_mileage) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| expiration_dateRequired날짜 | 최초 소멸 시행일 |
| interval_monthRequired | 소멸 실행 주기   1: 1개월 3: 3개월 6: 6개월 12: 1년 |
| target_period_monthRequired | 소멸 대상 적립금   6: 소멸일 기준 6개월 이전 적립금 12: 소멸일 기준 1년 이전 적립금 18: 소멸일 기준 1년 6개월 이전 적립금 24: 소멸일 기준 2년 이전 적립금 30: 소멸일 기준 2년 6개월 이전 적립금 36: 소멸일 기준 3년 이전 적립금 |
| group_no | 소멸 대상 회원등급   0: 전체 회원   DEFAULT 0 |
| standard_pointRequired최소값: [1] | 소멸 대상 기준 금액   소멸할 적립금의 최소 기준 금액 입력 예) 100 기재 시, 100원 이상 적립금 보유 회원만 소멸 대상 |
| send_email | 이메일 발송   T: 설정함 F: 설정안함   DEFAULT F |
| send_sms | SMS 발송   T: 설정함 F: 설정안함   DEFAULT F |
| notification_time_day | 알람시기 선택   3: 3일 전 발송 7: 7일 전 발송 15: 15일 전 발송 30: 1개월 전 발송 |

```bash
Create an automatic points expiration        Create an automatic points expiration       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/points/autoexpiration' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "expiration_date": "2021-01-26",        "interval_month": 1,        "target_period_month": 12,        "group_no": 0,        "standard_point": "10.00",        "send_email": "T",        "send_sms": "F",        "notification_time_day": [            3,            7        ]    }}'    Response  Copy     {    "autoexpiration": {        "shop_no": 1,        "expiration_date": "2021-01-26",        "interval_month": 1,        "target_period_month": 12,        "group_no": 0,        "standard_point": "10.00",        "send_email": "T",        "send_sms": "F",        "notification_time_day": [            3,            7        ]    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/points/autoexpiration' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "expiration_date": "2021-01-26",        "interval_month": 1,        "target_period_month": 12,        "group_no": 0,        "standard_point": "10.00",        "send_email": "T",        "send_sms": "F",        "notification_time_day": [            3,            7        ]    }}'
```

```json
{    "autoexpiration": {        "shop_no": 1,        "expiration_date": "2021-01-26",        "interval_month": 1,        "target_period_month": 12,        "group_no": 0,        "standard_point": "10.00",        "send_email": "T",        "send_sms": "F",        "notification_time_day": [            3,            7        ]    }}
```

### Delete an automatic points expiration   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 적립금 쓰기권한 (mall.write_mileage) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Delete an automatic points expiration        Delete an automatic points expiration       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/points/autoexpiration' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "autoexpiration": {        "shop_no": 1    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/points/autoexpiration' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "autoexpiration": {        "shop_no": 1    }}
```
