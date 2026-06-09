# POINTS


## Points

```json
Endpoints    GET /api/v2/admin/points
POST /api/v2/admin/points
```

```json
GET /api/v2/admin/points
POST /api/v2/admin/points
```

### Points property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| case | 적립금 타입 |
| member_id | 회원아이디 |
| email | 이메일 |
| group_name | 회원등급명 |
| available_points_increase | 적립금 증가 |
| available_points_decrease | 적립금 차감 |
| available_points_total | 가용 적립금 |
| unavailable_points | 미가용 적립금 |
| order_date | 주문일 |
| issue_date | 적립금 지급일 |
| available_date | 미가용 적립금 사용 가능일 |
| admin_id | 관리자 아이디 |
| admin_name | 관리자 이름 |
| order_id | 주문번호 |
| reason | 적립 사유 적립금을 증가/차감하는 사유를 입력할 수 있다. |
| amount | 적립금 증감액 1회당 최대 1,000,000원 이하까지 적립금을 지급할 수 있음. 가용 적립금보다 큰 금액을 차감할 수 없다. |
| type | 적립금 증가/차감 여부 적립금을 증가시킬지 차감시킬지 여부를 선택할 수 있다. |

### Retrieve points   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 적립금 읽기권한 (mall.read_mileage) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_id최대글자수 : [20자] | 회원아이디 |
| email이메일 | 이메일 |
| order_id최대글자수 : [100자] | 주문아이디 |
| group_no | 회원등급번호 |
| start_dateRequired날짜 | 검색 시작일 |
| end_dateRequired날짜 | 검색 종료일 |
| case | 적립금 타입   적립금 타입 지정 없이 전체 조회시에는 D: 적립금 환불 타입은 제외되고 조회 되므로, 적립금 환불 타입을 조회하려면 타입을 지정해야 합니다.   A : 관리자 직접 적립금 부여B : 주문취소로 인한 환불시 환불금을 적립금으로 부여C : 적립대기중이던 적립금 취소D : 반품완료 후 사용가능E : csv파일로 등록된 회원F : 주문취소로 인해 상품에 대한 적립금 차감G : 추천한 신규 가입자에게 적립금 부여H : (기존 적립금 내역용 레거시 타입) 주문시 회원등급에 따른 적립금 부여(회원 등급 적립금)I : 주문취소로 인해 회원등급에 대한 적립금 환불J : 주문취소로 인해 쿠폰에 대한 적립금 환불K : 주문시 회원등급에 따른 적립금 부여(회원 등급 적립금)L : 주문시 사용한 쿠폰에 따른 적립금 부여(쿠폰 적립금)M : 상품구매시 사용한 적립금N : 신규가입시 적립금 부여O : 적립금 즉시지급 쿠폰(온라인/시리얼)P : 주문시 구매한 상품에 대한 적립금 부여(구매에 대한 적립금)Q : 즐겨찾기 적립금R : 추천받은 기존 가입자에게 적립금 부여S : 주문취소시 구매에 사용한 적립금 부여(적립금 복원(주문취소))T : 뉴스레터 동의 적립금U : 바로가기(링콘) 설치 후 로그인V : 피추천인 주문취소에 따른 감사적립금 차감W : 피추천인 주문에 따른 감사적립금 부여X : 바로가기(링콘) 접속 후 구매에 따른 추가 적립금 부여Y : (기존 적립금 내역용 레거시 타입) 주문시 구매한 상품에 대한 적립금 부여(구매에 대한 적립금)Z : 바로가기 아이콘 설치AA : 바로가기(링콘) 접속 후 구매에 따른 추가 적립금 차감AB : 적립금 소멸AD : 회원정보 이벤트 참여 적립금AE : 브랜드앱 주문 적립금AF : 주문취소에 의한 브랜드앱 주문 적립금 차감AG : 오프라인구매-적립금 사용AH : 오프라인취소-구매시 사용한 적립금 복원AI : 이벤트팩토리 적립금AK : 브랜드앱 푸시알림 ON 적립금AL : 브랜드앱 설치 적립금AM : API 를 통한 적립금AN : 브랜드앱 푸시 혜택받기로 인한 적립금AO : 구매 확정 취소에 의한 브랜드앱 적립금 차감AP : 구매 확정 취소에 의한 쿠폰 적립금 차감AQ : 구매 확정 취소에 의한 회원등급 적립금 차감AR : 구매 확정 취소에 의한 상품 적립금 차감 AS : 구매 확정 취소에 의한 링콘 적립금 차감1 : 모바일 메시지 수신동의 + 이메일 수신동의 적립금2 : 모바일 메시지 수신동의 적립금3 : 회원 정보 수정 이벤트4 : 오프라인취소-구매시 지급한 적립금 회수5 : 오프라인구매-적립금 지급6 : [품목추가] 관리자 직접 지급 [상품] 적립금7 : [품목추가] 관리자 직접 지급 [회원] 적립금8 : [품목교환] 관리자 직접 지급 [상품] 적립금9 : [품목교환] 관리자 직접 지급 [회원] 적립금 |
| points_category | 적립금 내역   available: 가용적립금 unavailable: 미가용 적립금 unavailable_coupon: 미가용회원/쿠폰적립금   DEFAULT available |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve points        Retrieve points Retrieve points with fields parameter Retrieve points using paging Retrieve a specific points with member_id parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/points?start_date=2019-01-01T00:00:00+09:00&end_date=2019-03-01T23:59:59+09:00' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "points": [        {            "shop_no": 1,            "case": "A",            "member_id": "testmember",            "email": "sample@sample.com",            "group_name": "sample group",            "available_points_increase": "500.00",            "available_points_decrease": null,            "available_points_total": "500.00",            "unavailable_points": null,            "order_date": null,            "issue_date": "2019-02-11T05:50:01+09:00",            "available_date": null,            "admin_id": "admin",            "admin_name": null,            "order_id": null,            "reason": "New products promotion"        },        {            "shop_no": 1,            "case": "A",            "member_id": "testmember",            "email": "sample@sample.com",            "group_name": "sample group",            "available_points_increase": null,            "available_points_decrease": "200.00",            "available_points_total": "300.00",            "unavailable_points": null,            "order_date": null,            "issue_date": "2019-02-11T05:55:01+09:00",            "available_date": null,            "admin_id": "admin",            "admin_name": null,            "order_id": null,            "reason": "Expired Points"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/points?start_date=2019-01-01T00:00:00+09:00&end_date=2019-03-01T23:59:59+09:00' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "points": [        {            "shop_no": 1,            "case": "A",            "member_id": "testmember",            "email": "sample@sample.com",            "group_name": "sample group",            "available_points_increase": "500.00",            "available_points_decrease": null,            "available_points_total": "500.00",            "unavailable_points": null,            "order_date": null,            "issue_date": "2019-02-11T05:50:01+09:00",            "available_date": null,            "admin_id": "admin",            "admin_name": null,            "order_id": null,            "reason": "New products promotion"        },        {            "shop_no": 1,            "case": "A",            "member_id": "testmember",            "email": "sample@sample.com",            "group_name": "sample group",            "available_points_increase": null,            "available_points_decrease": "200.00",            "available_points_total": "300.00",            "unavailable_points": null,            "order_date": null,            "issue_date": "2019-02-11T05:55:01+09:00",            "available_date": null,            "admin_id": "admin",            "admin_name": null,            "order_id": null,            "reason": "Expired Points"        }    ]}
```

### Issue and deduct points   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 적립금 쓰기권한 (mall.write_mileage) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. SMS는 한국어 멀티쇼핑몰에서만 발송 가능하다.   DEFAULT 1 |
| member_idRequired최대글자수 : [20자] | 회원아이디   회원 아이디 |
| order_id주문번호 | 주문번호 |
| amountRequired최소값: [0] | 적립금 증감액   1회당 최대 1,000,000원 이하까지 적립금을 지급할 수 있음. 가용 적립금보다 큰 금액을 차감할 수 없다. |
| typeRequired | 적립금 증가/차감 여부   적립금을 증가시킬지 차감시킬지 여부를 선택할 수 있다.   increase : 증가 decrease : 차감 |
| reason | 적립 사유   적립금을 증가/차감하는 사유를 입력할 수 있다. |

```bash
Issue and deduct points        Issue and deduct points Increase point of a certain customer using only member_id, amount, and type fields Decrease point of a certain customer using only member_id, amount, and type fields Try increasing point of a certain customer without using amount field Try increasing point of a certain customer without using type field       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/points' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "member_id": "testmember",        "order_id": "20200228-0000001",        "amount": "10.00",        "type": "increase",        "reason": "New products promotion"    }}'    Response  Copy     {    "points": {        "shop_no": 1,        "member_id": "testmember",        "order_id": "20200228-0000001",        "amount": "10.00",        "type": "increase",        "reason": "New products promotion"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/points' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "member_id": "testmember",        "order_id": "20200228-0000001",        "amount": "10.00",        "type": "increase",        "reason": "New products promotion"    }}'
```

```json
{    "points": {        "shop_no": 1,        "member_id": "testmember",        "order_id": "20200228-0000001",        "amount": "10.00",        "type": "increase",        "reason": "New products promotion"    }}
```
