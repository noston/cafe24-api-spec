# CUSTOMEREVENTS


## Customerevents

```json
Endpoints    GET /api/v2/admin/customerevents
POST /api/v2/admin/customerevents
PUT /api/v2/admin/customerevents
```

```json
GET /api/v2/admin/customerevents
POST /api/v2/admin/customerevents
PUT /api/v2/admin/customerevents
```

### Customerevents property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 DEFAULT 1 |
| no | 이벤트 번호 |
| type | 이벤트 유형 E: 회원정보수정 P: 비밀번호변경 L: 평생회원전환 |
| name | 이벤트 이름 |
| description | 이벤트 설명 |
| start_date | 이벤트 시작 시간 |
| end_date | 이벤트 종료 시간 |
| created_date | 이벤트 생성일 |
| items | 이벤트 항목 zipcode: 새 우편번호 주소 address: 주소 수정 cellphone: 휴대폰번호 password: 비밀번호 수정 모바일 메시지: 모바일 메시지 수신 동의 email: 이메일 수신 동의 |
| reward_condition | 이벤트 조건 O: 설정한 항목 중 1개 이상 수정한 경우 혜택 지급 A: 설정한 항목을 모두 수정한 경우 혜택 지급 |
| agree_restriction | 이메일/모바일 메시지 수신동의 지급 제한 설정 사용 여부 T: 사용함 F: 사용안함 |
| agree_restriction_period | 이메일/모바일 메시지 수신동의 변경 불가 기간 1: 1개월 3: 3개월 6: 6개월 12: 12개월 -1: 무기한 |
| auto_reward | 혜택 자동 지급 설정 여부 T: 사용함 F: 사용안함 |
| use_point | 혜택 자동 지급 적립금 사용 여부 T: 사용함 F: 사용안함 |
| point_amount | 혜택 자동 지급 적립금 |
| use_coupon | 혜택 자동 지급 쿠폰 사용 여부 T: 사용함 F: 사용안함 |
| coupon_no | 혜택 자동 지급 쿠폰 |
| popup_notification | 평생회원 전환 이벤트 안내 팝업 사용 여부 T: 사용함 F: 사용안함 |
| status | 이벤트 상태 |

### View member information event   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 읽기권한 (mall.read_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| name최대글자수 : [200자] | 이벤트 이름 |
| search_date | 검색 기준일   created_date: 이벤트 생성일 start_date: 이벤트 시작일 end_date: 이벤트 종료일   DEFAULT created_date |
| start_date날짜 | 검색 시작일 |
| end_date날짜 | 검색 종료일 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
View member information event        View member information event       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/customerevents?start_date=2025-01-31T00:00:00+09:00&end_date=2025-02-15T00:00:00+09:00' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "customerevents": [        {            "shop_no": 1,            "no": 1,            "type": "E",            "name": "Member Information Update Event",            "description": "This is a description for the member information update event.",            "start_date": "2025-01-31T00:00:00+09:00",            "end_date": "2025-02-28T00:00:00+09:00",            "created_date": "2025-01-30T12:34:56+09:00",            "items": [                "zipcode",                "email"            ],            "reward_condition": "A",            "agree_restriction": "T",            "agree_restriction_period": 3,            "auto_reward": "T",            "use_point": "T",            "point_amount": "1000.00",            "use_coupon": "T",            "coupon_no": "9000000000000000033",            "popup_notification": "F"        },        {            "shop_no": 1,            "no": 2,            "type": "L",            "name": "Lifetime Member Event",            "description": "This is a description for the lifetime member event.",            "start_date": "2025-01-30T12:34:56+09:00",            "end_date": "9999-12-31T23:59:59+09:00",            "created_date": "2025-01-30T12:34:56+09:00",            "items": null,            "reward_condition": null,            "agree_restriction": null,            "agree_restriction_period": null,            "auto_reward": "T",            "use_point": null,            "point_amount": null,            "use_coupon": "T",            "coupon_no": "9000000000000000034",            "popup_notification": "T"        }    ],    "links": [        {            "rel": "prev",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/customerevents?limit=10&offset=0"        },        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/customerevents?limit=10&offset=20"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/customerevents?start_date=2025-01-31T00:00:00+09:00&end_date=2025-02-15T00:00:00+09:00' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "customerevents": [        {            "shop_no": 1,            "no": 1,            "type": "E",            "name": "Member Information Update Event",            "description": "This is a description for the member information update event.",            "start_date": "2025-01-31T00:00:00+09:00",            "end_date": "2025-02-28T00:00:00+09:00",            "created_date": "2025-01-30T12:34:56+09:00",            "items": [                "zipcode",                "email"            ],            "reward_condition": "A",            "agree_restriction": "T",            "agree_restriction_period": 3,            "auto_reward": "T",            "use_point": "T",            "point_amount": "1000.00",            "use_coupon": "T",            "coupon_no": "9000000000000000033",            "popup_notification": "F"        },        {            "shop_no": 1,            "no": 2,            "type": "L",            "name": "Lifetime Member Event",            "description": "This is a description for the lifetime member event.",            "start_date": "2025-01-30T12:34:56+09:00",            "end_date": "9999-12-31T23:59:59+09:00",            "created_date": "2025-01-30T12:34:56+09:00",            "items": null,            "reward_condition": null,            "agree_restriction": null,            "agree_restriction_period": null,            "auto_reward": "T",            "use_point": null,            "point_amount": null,            "use_coupon": "T",            "coupon_no": "9000000000000000034",            "popup_notification": "T"        }    ],    "links": [        {            "rel": "prev",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/customerevents?limit=10&offset=0"        },        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/customerevents?limit=10&offset=20"        }    ]}
```

### Create a member information modification event   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 쓰기권한 (mall.write_promotion) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| typeRequired | 이벤트 유형   E: 회원정보수정 P: 비밀번호변경 L: 평생회원전환 |
| nameRequired최대글자수 : [200자] | 이벤트 이름 |
| description최대글자수 : [200자] | 이벤트 설명 |
| start_date날짜 | 이벤트 시작 시간 |
| end_date날짜 | 이벤트 종료 시간 |
| items배열 최대사이즈: [6] | 이벤트 항목   zipcode: 새 우편번호 주소 address: 주소 수정 cellphone: 휴대폰번호 password: 비밀번호 수정 모바일 메시지: 모바일 메시지 수신 동의 email: 이메일 수신 동의 |
| reward_condition | 이벤트 조건   O: 설정한 항목 중 1개 이상 수정한 경우 혜택 지급 A: 설정한 항목을 모두 수정한 경우 혜택 지급 |
| agree_restriction | 이메일/모바일 메시지 수신동의 지급 제한 설정 사용 여부   T: 사용함 F: 사용안함 |
| agree_restriction_period | 이메일/모바일 메시지 수신동의 변경 불가 기간   1: 1개월 3: 3개월 6: 6개월 12: 12개월 -1: 무기한 |
| auto_reward | 혜택 자동 지급 설정 여부   T: 사용함 F: 사용안함 |
| use_point | 혜택 자동 지급 적립금 사용 여부   T: 사용함 F: 사용안함 |
| point_amount | 혜택 자동 지급 적립금 |
| use_coupon | 혜택 자동 지급 쿠폰 사용 여부   T: 사용함 F: 사용안함 |
| coupon_no | 혜택 자동 지급 쿠폰 |
| popup_notification | 평생회원 전환 이벤트 안내 팝업 사용 여부   T: 사용함 F: 사용안함 |

```bash
Create a member information modification event        Create a member information modification event       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/customerevents' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "type": "E",        "name": "Member Information Update Event",        "description": "This is a description for the member information update event.",        "start_date": "2025-01-31T00:00:00+09:00",        "end_date": "2025-02-28T00:00:00+09:00",        "items": [            "zipcode",            "email"        ],        "reward_condition": "A",        "agree_restriction": "T",        "agree_restriction_period": 3,        "auto_reward": "T",        "use_point": "T",        "point_amount": "1000.00",        "use_coupon": "T",        "coupon_no": "9000000000000000033",        "popup_notification": "F"    }}'    Response  Copy     {    "customerevent": {        "shop_no": 1,        "no": 1,        "type": "E",        "name": "Member Information Update Event",        "description": "This is a description for the member information update event.",        "start_date": "2025-01-31T00:00:00+09:00",        "end_date": "2025-02-28T00:00:00+09:00",        "created_date": "2025-01-30T12:34:56+09:00",        "items": [            "zipcode",            "email"        ],        "reward_condition": "A",        "agree_restriction": "T",        "agree_restriction_period": 3,        "auto_reward": "T",        "use_point": "T",        "point_amount": "1000.00",        "use_coupon": "T",        "coupon_no": "9000000000000000033",        "popup_notification": "F"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/customerevents' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "type": "E",        "name": "Member Information Update Event",        "description": "This is a description for the member information update event.",        "start_date": "2025-01-31T00:00:00+09:00",        "end_date": "2025-02-28T00:00:00+09:00",        "items": [            "zipcode",            "email"        ],        "reward_condition": "A",        "agree_restriction": "T",        "agree_restriction_period": 3,        "auto_reward": "T",        "use_point": "T",        "point_amount": "1000.00",        "use_coupon": "T",        "coupon_no": "9000000000000000033",        "popup_notification": "F"    }}'
```

```json
{    "customerevent": {        "shop_no": 1,        "no": 1,        "type": "E",        "name": "Member Information Update Event",        "description": "This is a description for the member information update event.",        "start_date": "2025-01-31T00:00:00+09:00",        "end_date": "2025-02-28T00:00:00+09:00",        "created_date": "2025-01-30T12:34:56+09:00",        "items": [            "zipcode",            "email"        ],        "reward_condition": "A",        "agree_restriction": "T",        "agree_restriction_period": 3,        "auto_reward": "T",        "use_point": "T",        "point_amount": "1000.00",        "use_coupon": "T",        "coupon_no": "9000000000000000033",        "popup_notification": "F"    }}
```

### Update information update campaign status   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 쓰기권한 (mall.write_promotion) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| noRequired | 이벤트 번호 |
| statusRequired | 이벤트 상태   S: 이벤트종료 D: 이벤트삭제 |

```bash
Update information update campaign status        Update information update campaign status       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/customerevents' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "no": [            1,            2        ],        "status": "D"    }}'    Response  Copy     {    "customerevent": {        "shop_no": 1,        "no": [            1,            2        ],        "status": "D"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/customerevents' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "no": [            1,            2        ],        "status": "D"    }}'
```

```json
{    "customerevent": {        "shop_no": 1,        "no": [            1,            2        ],        "status": "D"    }}
```
