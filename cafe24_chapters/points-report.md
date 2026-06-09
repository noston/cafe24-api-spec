# POINTS REPORT


## Points report

```json
Endpoints    GET /api/v2/admin/points/report
```

```json
GET /api/v2/admin/points/report
```

### Points report property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| available_points_increase | 가용 적립금 증가 |
| available_points_decrease | 가용 적립금 차감 |
| available_points_total | 가용 적립금 전체 |
| unavailable_points | 미가용 적립금 |
| unavailable_coupon_points | 미가용 회원 쿠폰 적립금 |

### Retrieve a points report by date range   cafe24

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
| group_no | 회원등급번호 |
| start_dateRequired날짜 | 검색 시작일 |
| end_dateRequired날짜 | 검색 종료일 |

```bash
Retrieve a points report by date range        Retrieve a points report by date range Retrieve report with fields parameter Retrieve a specific report with member_id parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/points/report?start_date=2019-01-01 00:00:00&end_date=2019-03-01 23:59:59' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "report": {        "shop_no": 1,        "available_points_increase": "100.00",        "available_points_decrease": "20.00",        "available_points_total": "80.00",        "unavailable_points": "1500.00",        "unavailable_coupon_points": "1169.00"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/points/report?start_date=2019-01-01 00:00:00&end_date=2019-03-01 23:59:59' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "report": {        "shop_no": 1,        "available_points_increase": "100.00",        "available_points_decrease": "20.00",        "available_points_total": "80.00",        "unavailable_points": "1500.00",        "unavailable_coupon_points": "1169.00"    }}
```
