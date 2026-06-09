# CUSTOMERS


## Customers

```json
Endpoints    GET /api/v2/admin/customers
DELETE /api/v2/admin/customers/{member_id}
```

```json
GET /api/v2/admin/customers
DELETE /api/v2/admin/customers/{member_id}
```

### Customers property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| member_id Required최대글자수 : [20자] | 회원아이디 |
| group_no | 회원등급번호 해당 회원의 회원등급의 번호 |
| member_authentication | 회원인증여부 회원 인증여부. 인증에 따라 회원은 4종류로 구분된다. 인증회원을 특별관리회원으로 설정할 경우 해당 회원은 가장 마지막에 설정한 특별관리회원으로 표시된다. T : 인증 F : 미인증 B : 특별관리회원 J : 14세미만회원 |
| use_blacklist | 불량회원설정 불량회원 여부. 불량회원일 경우 불량회원 타입에 따라 상품구매 차단, 로그인 차단, 로그인과 상품구매 모두를 차단할 수 있음. T : 설정함 F : 설정안함 |
| blacklist_type | 불량회원 차단설정 해당 회원의 불량회원 타입. 불량회원 타입에 따라 상품구매 차단, 로그인 차단, 로그인과 상품구매 모두를 차단할 수 있음. P : 상품구매차단 L : 로그인차단 A : 로그인&상품구매 차단 |
| authentication_method | 인증 수단 null : 인증안함 i : 아이핀인증 m : 휴대폰 본인인증 e : 이메일인증 d : 휴대폰 인증(중복 확인) a : 앱 인증(기타 인증) |
| sms | 모바일 메시지 수신여부 SMS를 수신할지 여부. '수신거부' 시 광고, 영리성 목적 외 서비스에 필요한 주요 메일은 정상적으로 수신함. T : 수신 F : 수신안함 |
| news_mail | 뉴스메일 수신여부 이메일을 수신할지 여부. '수신거부' 시 광고, 영리성 목적 외 서비스에 필요한 주요 메일은 정상적으로 수신함. T : 수신 F : 수신안함 |
| solar_calendar | 양력여부 T : 양력 F : 음력 |
| total_points | 총 적립금 |
| available_points | 가용 적립금 |
| used_points | 사용 적립금 |
| last_login_date | 최근 접속일시 해당 회원의 최종 로그인 일시 |
| gender | 성별 해당 회원의 성별 M : 남자 F : 여자 |
| use_mobile_app | 모바일앱 사용여부 T : 사용 F : 사용안함 |
| available_credits | 가용 예치금 |
| created_date | 가입일 |
| fixed_group | 회원등급 고정 여부 특정 회원이 회원자동등급변경에 적용되지 않기 위한 등급 고정 여부 회원자동등급변경 기능을 사용하는 몰에서만 사용 가능하다. T : 고정함 F : 고정안함 |

### Retrieve a list of customers   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 읽기권한 (mall.read_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| cellphone | 휴대전화   검색할 쇼핑몰 회원의 휴대전화번호. 개인정보 보호를 위해 전체 휴대전화번호를 입력해야 한다. cellphone 또는 member_id 중 하나는 반드시 검색 조건으로 지정되어야 한다.   ,(콤마)로 여러 건을 검색할 수 있다. |
| member_id최대글자수 : [20자] | 회원아이디   검색할 쇼핑몰 회원의 아이디. 개인정보 보호를 위해 전체 아이디를 입력해야 합니다.cellphone 또는 member_id 중 하나는 반드시 검색 조건으로 지정되어야 한다.   ,(콤마)로 여러 건을 검색할 수 있다. |

```bash
Retrieve a list of customers        Retrieve a list of customers Retrieve customer using cell phone number       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/customers?member_id=sampleid,testid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "customers": [        {            "shop_no": 1,            "member_id": "sampleid",            "group_no": 1,            "member_authentication": "T",            "use_blacklist": "F",            "blacklist_type": "",            "authentication_method": "i",            "sms": "T",            "news_mail": "T",            "solar_calendar": "T",            "total_points": "0.00",            "available_points": "0.00",            "used_points": "0.00",            "last_login_date ": "2019-04-16T11:19:27+09:00",            "created_date": "2019-04-20T11:19:27+09:00",            "gender ": "M",            "use_mobile_app ": "T",            "available_credits ": "0.00",            "fixed_group": "T"        },        {            "shop_no": 1,            "member_id": "testid",            "group_no": 1,            "member_authentication": "T",            "use_blacklist": "F",            "blacklist_type": "F",            "authentication_method": "m",            "sms": "F",            "news_mail": "F",            "solar_calendar": "F",            "total_points": "0.00",            "available_points": "0.00",            "used_points": "0.00",            "last_login_date ": "2019-04-16T11:19:27+09:00",            "created_date": "2019-04-20T11:19:27+09:00",            "gender ": "F",            "use_mobile_app ": "F",            "available_credits ": "0.00",            "fixed_group": "F"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/customers?member_id=sampleid,testid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "customers": [        {            "shop_no": 1,            "member_id": "sampleid",            "group_no": 1,            "member_authentication": "T",            "use_blacklist": "F",            "blacklist_type": "",            "authentication_method": "i",            "sms": "T",            "news_mail": "T",            "solar_calendar": "T",            "total_points": "0.00",            "available_points": "0.00",            "used_points": "0.00",            "last_login_date ": "2019-04-16T11:19:27+09:00",            "created_date": "2019-04-20T11:19:27+09:00",            "gender ": "M",            "use_mobile_app ": "T",            "available_credits ": "0.00",            "fixed_group": "T"        },        {            "shop_no": 1,            "member_id": "testid",            "group_no": 1,            "member_authentication": "T",            "use_blacklist": "F",            "blacklist_type": "F",            "authentication_method": "m",            "sms": "F",            "news_mail": "F",            "solar_calendar": "F",            "total_points": "0.00",            "available_points": "0.00",            "used_points": "0.00",            "last_login_date ": "2019-04-16T11:19:27+09:00",            "created_date": "2019-04-20T11:19:27+09:00",            "gender ": "F",            "use_mobile_app ": "F",            "available_credits ": "0.00",            "fixed_group": "F"        }    ]}
```

### Delete an account   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 쓰기권한 (mall.write_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired최대글자수 : [20자] | 회원아이디 |
| is_point_check | 적립금보유회원 탈퇴 처리 여부   F : 탈퇴 안 함 T : 탈퇴 처리 |

```bash
Delete an account        Delete an account       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/customers/{#id}' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "customer": {        "shop_no": 1,        "member_id": "sampleid"    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/customers/{#id}' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "customer": {        "shop_no": 1,        "member_id": "sampleid"    }}
```
