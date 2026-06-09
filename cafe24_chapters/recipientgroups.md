# RECIPIENTGROUPS


## Recipientgroups

```json
Endpoints    GET /api/v2/admin/recipientgroups
GET /api/v2/admin/recipientgroups/{group_no}
POST /api/v2/admin/recipientgroups
PUT /api/v2/admin/recipientgroups/{group_no}
DELETE /api/v2/admin/recipientgroups/{group_no}
```

```json
GET /api/v2/admin/recipientgroups
GET /api/v2/admin/recipientgroups/{group_no}
POST /api/v2/admin/recipientgroups
PUT /api/v2/admin/recipientgroups/{group_no}
DELETE /api/v2/admin/recipientgroups/{group_no}
```

### Recipientgroups property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| group_no | 발송그룹 번호 |
| group_name최대글자수 : [40자] | 발송그룹명 |
| group_description최대글자수 : [255자] | 발송그룹 설명 |
| created_date | 등록일 |
| group_member_count | 발송그룹 회원 수 |
| news_mail | 뉴스메일 수신여부 T : 수신허용 F : 수신안함 D : 절대수신안함 |
| sms | 모바일 메시지 수신여부 T : 수신 F : 수신안함 |
| member_group_no | 회원등급번호 |
| member_class | 회원구분 p : 개인 c : 사업자 f : 외국인 |
| member_type | 회원타입 vip : 특별관리회원 poor : 불량회원 |
| join_path | 가입경로 P : PC M : 모바일 |
| inflow_path | 유입경로 |
| inflow_path_detail | 유입경로 상세정보 |
| date_type | 검색날짜 유형 join : 회원가입일 birthday : 생일 wedding : 결혼기념일 partner : 배우자생일 |
| start_date날짜 | 검색 시작일 |
| end_date날짜 | 검색 종료일 |
| solar_calendar | 양력여부 T : 양력 F : 음력 |
| age_min | 나이 검색 최소값 |
| age_max | 나이 검색 최대값 |
| gender | 성별 M : 남자 F : 여자 |
| available_points_min | 적립금 검색 최소값 |
| available_points_max | 적립금 검색 최대값 |
| use_mobile_app | 모바일앱 사용여부 T : 사용 F : 사용안함 |
| plusapp_member_join | 브랜드앱 경로 가입회원 여부 T : 사용함 F : 사용안함 |

### Retrieve distribution group list   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 알림 읽기권한 (mall.read_notification) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |
| offset최대값: [10000] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve distribution group list        Retrieve distribution group list       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/recipientgroups' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "recipientgroups": [        {            "shop_no": 1,            "group_no": 1,            "group_name": "Group - allow mail users",            "group_description": "allowed to receive mail for advertising information",            "created_date": "2021-09-15 11:15:56.139004",            "group_member_count": 10,            "news_mail": "T",            "sms": "T",            "member_group_no": 1,            "member_class": "p",            "member_type": "vip",            "join_path": "P",            "inflow_path": "",            "inflow_path_detail": "",            "date_type": "join",            "start_date": "2021-01-01",            "end_date": "2021-12-31",            "solar_calendar": "",            "age_min": 1,            "age_max": 99,            "gender": "M",            "available_points_min": "0.00",            "available_points_max": "1000000.00",            "use_mobile_app": "F",            "plusapp_member_join": "F"        },        {            "shop_no": 1,            "group_no": 2,            "group_name": "Group - Do not allow mail users",            "group_description": "do not allow receiving mail for advertising information",            "created_date": "2021-09-15 11:25:58.175215",            "group_member_count": 15,            "news_mail": "F",            "sms": "F",            "member_group_no": 1,            "member_class": "p",            "member_type": "vip",            "join_path": "P",            "inflow_path": "",            "inflow_path_detail": "",            "date_type": "join",            "start_date": "2021-01-01",            "end_date": "2021-12-31",            "solar_calendar": "",            "age_min": 1,            "age_max": 99,            "gender": "M",            "available_points_min": "0.00",            "available_points_max": "1000000.00",            "use_mobile_app": "F",            "plusapp_member_join": "F"        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/recipientgroups?limit=10&offset=10"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/recipientgroups' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "recipientgroups": [        {            "shop_no": 1,            "group_no": 1,            "group_name": "Group - allow mail users",            "group_description": "allowed to receive mail for advertising information",            "created_date": "2021-09-15 11:15:56.139004",            "group_member_count": 10,            "news_mail": "T",            "sms": "T",            "member_group_no": 1,            "member_class": "p",            "member_type": "vip",            "join_path": "P",            "inflow_path": "",            "inflow_path_detail": "",            "date_type": "join",            "start_date": "2021-01-01",            "end_date": "2021-12-31",            "solar_calendar": "",            "age_min": 1,            "age_max": 99,            "gender": "M",            "available_points_min": "0.00",            "available_points_max": "1000000.00",            "use_mobile_app": "F",            "plusapp_member_join": "F"        },        {            "shop_no": 1,            "group_no": 2,            "group_name": "Group - Do not allow mail users",            "group_description": "do not allow receiving mail for advertising information",            "created_date": "2021-09-15 11:25:58.175215",            "group_member_count": 15,            "news_mail": "F",            "sms": "F",            "member_group_no": 1,            "member_class": "p",            "member_type": "vip",            "join_path": "P",            "inflow_path": "",            "inflow_path_detail": "",            "date_type": "join",            "start_date": "2021-01-01",            "end_date": "2021-12-31",            "solar_calendar": "",            "age_min": 1,            "age_max": 99,            "gender": "M",            "available_points_min": "0.00",            "available_points_max": "1000000.00",            "use_mobile_app": "F",            "plusapp_member_join": "F"        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/recipientgroups?limit=10&offset=10"        }    ]}
```

### Retrieve distribution group details   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 알림 읽기권한 (mall.read_notification) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| group_noRequired최소값: [1] | 발송그룹 번호 |

```bash
Retrieve distribution group details        Retrieve distribution group details       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/recipientgroups/2' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "recipientgroup": {        "shop_no": 1,        "group_no": 2,        "group_name": "Group - Do not allow mail users",        "group_description": "do not allow receiving mail for advertising information",        "created_date": "2021-09-15 11:25:58.175215",        "group_member_count": 15,        "news_mail": "F",        "sms": "F",        "member_group_no": 1,        "member_class": "p",        "member_type": "vip",        "join_path": "P",        "inflow_path": "",        "inflow_path_detail": "",        "date_type": "join",        "start_date": "2021-01-01",        "end_date": "2021-12-31",        "solar_calendar": "",        "age_min": 1,        "age_max": 99,        "gender": "M",        "available_points_min": "0.00",        "available_points_max": "1000000.00",        "use_mobile_app": "F",        "plusapp_member_join": "F"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/recipientgroups/2' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "recipientgroup": {        "shop_no": 1,        "group_no": 2,        "group_name": "Group - Do not allow mail users",        "group_description": "do not allow receiving mail for advertising information",        "created_date": "2021-09-15 11:25:58.175215",        "group_member_count": 15,        "news_mail": "F",        "sms": "F",        "member_group_no": 1,        "member_class": "p",        "member_type": "vip",        "join_path": "P",        "inflow_path": "",        "inflow_path_detail": "",        "date_type": "join",        "start_date": "2021-01-01",        "end_date": "2021-12-31",        "solar_calendar": "",        "age_min": 1,        "age_max": 99,        "gender": "M",        "available_points_min": "0.00",        "available_points_max": "1000000.00",        "use_mobile_app": "F",        "plusapp_member_join": "F"    }}
```

### Create a distribution group   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 알림 쓰기권한 (mall.write_notification) |
| 호출건수 제한 | 30 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| group_nameRequired최대글자수 : [40자] | 발송그룹명 |
| group_description최대글자수 : [255자] | 발송그룹 설명 |
| news_mail | 뉴스메일 수신여부   T : 수신허용 F : 수신안함 D : 절대수신안함 |
| sms | 모바일 메시지 수신여부   T : 수신 F : 수신안함 |
| member_group_no최소값: [1] | 회원등급번호 |
| member_class | 회원구분   EC 일본, 베트남 버전에서는 사용할 수 없음.   p : 개인 c : 사업자 f : 외국인 |
| member_type | 회원타입   vip : 특별관리회원 poor : 불량회원 |
| join_path | 가입경로   P : PC M : 모바일 |
| inflow_path | 유입경로 |
| inflow_path_detail | 유입경로 상세정보 |
| date_type | 검색날짜 유형   join : 회원가입일 birthday : 생일 wedding : 결혼기념일 partner : 배우자생일 |
| start_date | 검색 시작일 |
| end_date | 검색 종료일 |
| solar_calendar | 양력여부   T : 양력 F : 음력 |
| age_min최소: [1]~최대: [99] | 나이 검색 최소값 |
| age_max최소: [1]~최대: [99] | 나이 검색 최대값 |
| gender | 성별   M : 남자 F : 여자 |
| available_points_min최소: [0]~최대: [999999999] | 적립금 검색 최소값 |
| available_points_max최소: [0]~최대: [999999999] | 적립금 검색 최대값 |
| use_mobile_app | 모바일앱 사용여부   T : 사용 F : 사용안함 |
| plusapp_member_join | 브랜드앱 경로 가입회원 여부   T : 사용함 F : 사용안함 |

```bash
Create a distribution group        Create a distribution group       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/recipientgroups' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "group_name": "Group - Do not allow mail users",        "group_description": "do not allow receiving mail for advertising information",        "news_mail": "F",        "sms": "F",        "member_group_no": 1,        "member_class": "p",        "member_type": "vip",        "join_path": "P",        "inflow_path": "",        "inflow_path_detail": "",        "date_type": "join",        "start_date": "2021-01-01",        "end_date": "2021-12-31",        "solar_calendar": "",        "age_min": 1,        "age_max": 99,        "gender": "M",        "available_points_min": "0.00",        "available_points_max": "1000000.00",        "use_mobile_app": "F",        "plusapp_member_join": "F"    }}'    Response  Copy     {    "recipientgroup": {        "shop_no": 1,        "group_no": 2,        "group_name": "Group - Do not allow mail users",        "group_description": "do not allow receiving mail for advertising information",        "created_date": "2021-09-15 11:25:58.175215",        "group_member_count": 15,        "news_mail": "F",        "sms": "F",        "member_group_no": 1,        "member_class": "p",        "member_type": "vip",        "join_path": "P",        "inflow_path": "",        "inflow_path_detail": "",        "date_type": "join",        "start_date": "2021-01-01",        "end_date": "2021-12-31",        "solar_calendar": "",        "age_min": 1,        "age_max": 99,        "gender": "M",        "available_points_min": "0.00",        "available_points_max": "1000000.00",        "use_mobile_app": "F",        "plusapp_member_join": "F"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/recipientgroups' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "group_name": "Group - Do not allow mail users",        "group_description": "do not allow receiving mail for advertising information",        "news_mail": "F",        "sms": "F",        "member_group_no": 1,        "member_class": "p",        "member_type": "vip",        "join_path": "P",        "inflow_path": "",        "inflow_path_detail": "",        "date_type": "join",        "start_date": "2021-01-01",        "end_date": "2021-12-31",        "solar_calendar": "",        "age_min": 1,        "age_max": 99,        "gender": "M",        "available_points_min": "0.00",        "available_points_max": "1000000.00",        "use_mobile_app": "F",        "plusapp_member_join": "F"    }}'
```

```json
{    "recipientgroup": {        "shop_no": 1,        "group_no": 2,        "group_name": "Group - Do not allow mail users",        "group_description": "do not allow receiving mail for advertising information",        "created_date": "2021-09-15 11:25:58.175215",        "group_member_count": 15,        "news_mail": "F",        "sms": "F",        "member_group_no": 1,        "member_class": "p",        "member_type": "vip",        "join_path": "P",        "inflow_path": "",        "inflow_path_detail": "",        "date_type": "join",        "start_date": "2021-01-01",        "end_date": "2021-12-31",        "solar_calendar": "",        "age_min": 1,        "age_max": 99,        "gender": "M",        "available_points_min": "0.00",        "available_points_max": "1000000.00",        "use_mobile_app": "F",        "plusapp_member_join": "F"    }}
```

### Edit distribution group   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 알림 쓰기권한 (mall.write_notification) |
| 호출건수 제한 | 30 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| group_noRequired최소값: [1] | 발송그룹 번호 |
| group_nameRequired최대글자수 : [40자] | 발송그룹명 |
| group_description최대글자수 : [255자] | 발송그룹 설명 |
| news_mail | 뉴스메일 수신여부   T : 수신허용 F : 수신안함 D : 절대수신안함 |
| sms | 모바일 메시지 수신여부   T : 수신 F : 수신안함 |
| member_group_no최소값: [1] | 회원등급번호 |
| member_class | 회원구분   EC 일본, 베트남 버전에서는 사용할 수 없음.   p : 개인 c : 사업자 f : 외국인 |
| member_type | 회원타입   vip : 특별관리회원 poor : 불량회원 |
| join_path | 가입경로   P : PC M : 모바일 |
| inflow_path | 유입경로 |
| inflow_path_detail | 유입경로 상세정보 |
| date_type | 검색날짜 유형   join : 회원가입일 birthday : 생일 wedding : 결혼기념일 partner : 배우자생일 |
| start_date | 검색 시작일 |
| end_date | 검색 종료일 |
| solar_calendar | 양력여부   T : 양력 F : 음력 |
| age_min최소: [1]~최대: [99] | 나이 검색 최소값 |
| age_max최소: [1]~최대: [99] | 나이 검색 최대값 |
| gender | 성별   M : 남자 F : 여자 |
| available_points_min최소: [0]~최대: [999999999] | 적립금 검색 최소값 |
| available_points_max최소: [0]~최대: [999999999] | 적립금 검색 최대값 |
| use_mobile_app | 모바일앱 사용여부   T : 사용 F : 사용안함 |
| plusapp_member_join | 브랜드앱 경로 가입회원 여부   T : 사용함 F : 사용안함 |

```bash
Edit distribution group        Edit distribution group       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/recipientgroups/1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "group_name": "Group - VIP member",        "group_description": "for vip member",        "news_mail": "T",        "sms": "T",        "member_group_no": 1,        "member_class": "p",        "member_type": "vip",        "join_path": "P",        "inflow_path": "",        "inflow_path_detail": "",        "date_type": "join",        "start_date": "2000-01-01",        "end_date": "2021-12-31",        "solar_calendar": "",        "age_min": 1,        "age_max": 99,        "gender": "M",        "available_points_min": "0.00",        "available_points_max": "1000000.00",        "use_mobile_app": "F",        "plusapp_member_join": "F"    }}'    Response  Copy     {    "recipientgroup": {        "shop_no": 1,        "group_no": 1,        "group_name": "Group - VIP member",        "group_description": "for vip member",        "created_date": "2021-09-15 11:15:56.139004",        "group_member_count": 25,        "news_mail": "T",        "sms": "T",        "member_group_no": 1,        "member_class": "p",        "member_type": "vip",        "join_path": "P",        "inflow_path": "",        "inflow_path_detail": "",        "date_type": "join",        "start_date": "2000-01-01",        "end_date": "2021-12-31",        "solar_calendar": "",        "age_min": 1,        "age_max": 99,        "gender": "M",        "available_points_min": "0.00",        "available_points_max": "1000000.00",        "use_mobile_app": "F",        "plusapp_member_join": "F"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/recipientgroups/1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "group_name": "Group - VIP member",        "group_description": "for vip member",        "news_mail": "T",        "sms": "T",        "member_group_no": 1,        "member_class": "p",        "member_type": "vip",        "join_path": "P",        "inflow_path": "",        "inflow_path_detail": "",        "date_type": "join",        "start_date": "2000-01-01",        "end_date": "2021-12-31",        "solar_calendar": "",        "age_min": 1,        "age_max": 99,        "gender": "M",        "available_points_min": "0.00",        "available_points_max": "1000000.00",        "use_mobile_app": "F",        "plusapp_member_join": "F"    }}'
```

```json
{    "recipientgroup": {        "shop_no": 1,        "group_no": 1,        "group_name": "Group - VIP member",        "group_description": "for vip member",        "created_date": "2021-09-15 11:15:56.139004",        "group_member_count": 25,        "news_mail": "T",        "sms": "T",        "member_group_no": 1,        "member_class": "p",        "member_type": "vip",        "join_path": "P",        "inflow_path": "",        "inflow_path_detail": "",        "date_type": "join",        "start_date": "2000-01-01",        "end_date": "2021-12-31",        "solar_calendar": "",        "age_min": 1,        "age_max": 99,        "gender": "M",        "available_points_min": "0.00",        "available_points_max": "1000000.00",        "use_mobile_app": "F",        "plusapp_member_join": "F"    }}
```

### Delete distribution group   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 알림 쓰기권한 (mall.write_notification) |
| 호출건수 제한 | 30 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| group_noRequired최소값: [1] | 발송그룹 번호 |

```bash
Delete distribution group        Delete distribution group       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/recipientgroups/3' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "recipientgroup": {        "shop_no": 1,        "group_no": 3    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/recipientgroups/3' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "recipientgroup": {        "shop_no": 1,        "group_no": 3    }}
```
