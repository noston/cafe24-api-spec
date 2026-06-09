# CASHRECEIPT


## Cashreceipt

```json
Endpoints    GET /api/v2/admin/cashreceipt
POST /api/v2/admin/cashreceipt
PUT /api/v2/admin/cashreceipt/{cashreceipt_no}
```

```json
GET /api/v2/admin/cashreceipt
POST /api/v2/admin/cashreceipt
PUT /api/v2/admin/cashreceipt/{cashreceipt_no}
```

### Cashreceipt property list

| Attribute | Description |
| --- | --- |
| cashreceipt_no | 현금영수증 번호 |
| approval_no | 승인번호 |
| request_date | 신청일자 |
| order_id | 주문번호 |
| member_id | 회원아이디 |
| name | 요청자 이름 |
| order_price_amount | 상품구매금액 |
| vat | 부가세 |
| subtotal | 총 신청금액 |
| order_status | 주문상태 입금전: unpaid 미배송: unshipped 배송중: shipping 배송대기: standby 배송완료: shipped 부분취소: partially_canceled 전체취소: canceled |
| status | 처리상태 신청: request 발행대기: await_issuance 발행: issued 발행거부: issuance_rejected 신청취소: canceled_request 발행취소: canceled_issuance 발행실패: failed_issuance |
| pg_name | 신청결제사 |
| cash_bill_no | 현금영수증 일련 번호 |
| partner_id | PG사 발급 가맹점 ID |
| type | 발행 타입 개인: personal 사업자: business |
| company_registration_no | 사업자등록번호 |
| cellphone | 휴대전화 |
| tax_amount | 과세금액 |
| tax_free_amount | 면세금액 |
| supply_price | 공급가액 |

### Retrieve a list of cash receipts   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| start_dateRequired날짜 | 검색 시작일 |
| end_dateRequired날짜 | 검색 종료일 |
| order_id주문번호 | 주문번호   ,(콤마)로 여러 건을 검색할 수 있다. |
| approval_no최대글자수 : [9자] | 승인번호 |
| name최대글자수 : [20자] | 요청자 이름 |
| member_id최대글자수 : [20자] | 회원아이디 |
| status | 처리상태   전체: all 신청: request 발행: issued 신청취소: canceled_request 발행취소: canceled_issuance 발행실패: failed_issuance   DEFAULT all |
| limit최소: [1]~최대: [500] | 조회결과 최대건수   DEFAULT 10 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve a list of cash receipts        Retrieve a list of cash receipts       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/cashreceipt?start_date=2020-09-01T00:00:00+09:00&end_date=2020-11-30T23:59:59+09:00' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "cashreceipt": [        {            "cashreceipt_no": 11,            "approval_no": "265409188",            "request_date": "2020-10-16",            "order_id": "20201013-0000096",            "member_id": "sampleid",            "name": "John Doe",            "order_price_amount": "13500.00",            "vat": "1227.00",            "subtotal": "13500.00",            "order_status": "non_delivered",            "status": "issued",            "pg_name": "allat",            "cash_bill_no": "2001468853",            "partner_id": "allat_parter_id"        },        {            "cashreceipt_no": 10,            "approval_no": "265409188",            "request_date": "2020-10-16",            "order_id": "20201013-0000102",            "member_id": "sampleid",            "name": "John Doe",            "order_price_amount": "13500.00",            "vat": "1227.00",            "subtotal": "13500.00",            "order_status": "canceled",            "status": "canceled_issuance",            "pg_name": "allat",            "cash_bill_no": "2001468853",            "partner_id": "allat_parter_id"        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/cashreceipt?limit=10&offset=10"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/cashreceipt?start_date=2020-09-01T00:00:00+09:00&end_date=2020-11-30T23:59:59+09:00' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "cashreceipt": [        {            "cashreceipt_no": 11,            "approval_no": "265409188",            "request_date": "2020-10-16",            "order_id": "20201013-0000096",            "member_id": "sampleid",            "name": "John Doe",            "order_price_amount": "13500.00",            "vat": "1227.00",            "subtotal": "13500.00",            "order_status": "non_delivered",            "status": "issued",            "pg_name": "allat",            "cash_bill_no": "2001468853",            "partner_id": "allat_parter_id"        },        {            "cashreceipt_no": 10,            "approval_no": "265409188",            "request_date": "2020-10-16",            "order_id": "20201013-0000102",            "member_id": "sampleid",            "name": "John Doe",            "order_price_amount": "13500.00",            "vat": "1227.00",            "subtotal": "13500.00",            "order_status": "canceled",            "status": "canceled_issuance",            "pg_name": "allat",            "cash_bill_no": "2001468853",            "partner_id": "allat_parter_id"        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/cashreceipt?limit=10&offset=10"        }    ]}
```

### Create a cash receipt   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| order_idRequired주문번호 | 주문번호 |
| typeRequired | 발행 타입   개인: personal 사업자: business |
| company_registration_no사업자번호최대글자수 : [10자] | 사업자등록번호 |
| cellphone모바일최대글자수 : [11자] | 휴대전화 |

```bash
Create a cash receipt        Create a cash receipt       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/cashreceipt' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "order_id": "20201013-0000096",        "type": "personal",        "cellphone": "01000000000"    }}'    Response  Copy     {    "cashreceipt": {        "cashreceipt_no": 10,        "approval_no": "265409188",        "order_id": "20201013-0000096",        "type": "personal",        "company_registration_no": null,        "cellphone": "01000000000",        "tax_amount": "13500.00",        "tax_free_amount": "0.00",        "supply_price": "12273.00",        "vat": "1227.00"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/cashreceipt' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "order_id": "20201013-0000096",        "type": "personal",        "cellphone": "01000000000"    }}'
```

```json
{    "cashreceipt": {        "cashreceipt_no": 10,        "approval_no": "265409188",        "order_id": "20201013-0000096",        "type": "personal",        "company_registration_no": null,        "cellphone": "01000000000",        "tax_amount": "13500.00",        "tax_free_amount": "0.00",        "supply_price": "12273.00",        "vat": "1227.00"    }}
```

### Update a cash receipt   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| cashreceipt_noRequired최소값: [1] | 현금영수증 번호 |
| order_idRequired주문번호 | 주문번호 |
| type | 발행 타입   개인: personal 사업자: business |
| company_registration_no사업자번호최대글자수 : [10자] | 사업자등록번호 |
| cellphone모바일최대글자수 : [11자] | 휴대전화 |

```bash
Update a cash receipt        Update a cash receipt       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/cashreceipt/10' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "order_id": "20201013-0000096",        "type": "personal",        "cellphone": "01000000000"    }}'    Response  Copy     {    "cashreceipt": {        "cashreceipt_no": 10,        "approval_no": "265409188",        "order_id": "20201013-0000096",        "type": "personal",        "company_registration_no": null,        "cellphone": "01000000000",        "tax_amount": "13500.00",        "tax_free_amount": "0.00",        "supply_price": "12273.00",        "vat": "1227.00"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/cashreceipt/10' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "order_id": "20201013-0000096",        "type": "personal",        "cellphone": "01000000000"    }}'
```

```json
{    "cashreceipt": {        "cashreceipt_no": 10,        "approval_no": "265409188",        "order_id": "20201013-0000096",        "type": "personal",        "company_registration_no": null,        "cellphone": "01000000000",        "tax_amount": "13500.00",        "tax_free_amount": "0.00",        "supply_price": "12273.00",        "vat": "1227.00"    }}
```
