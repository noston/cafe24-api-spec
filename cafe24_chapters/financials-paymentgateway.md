# FINANCIALS PAYMENTGATEWAY


## Financials paymentgateway

```json
Endpoints    GET /api/v2/admin/financials/paymentgateway
```

```json
GET /api/v2/admin/financials/paymentgateway
```

### Financials paymentgateway property list

| Attribute | Description |
| --- | --- |
| partner_id | PG사 발급 가맹점 ID |
| payment_gateway_name | PG 이름 inicis : 이니시스 kcp : KCP allat : 올앳 ksnet : KSNET dacom : 토스페이먼츠 allthegate : 올더게이트 settlebank : 세틀뱅크 smartro : 스마트로 kicc : 한국정보통신 mobilians : 모빌리언스 danal : 다날 |
| contract_date | PG 계약일 |
| setting_date | PG 세팅일 |
| bank_code | 정산입금 은행코드 은행 코드 조회하기 |
| bank_account_no | 정산입금 계좌정보 |
| status | 금융제휴여부 T:제휴함  F: 제휴안함 |
| bank_account_name | 정산입금 예금주명 |
| payment_method_information | 결제수단별 정산 정보 ※ payment_method_information 하위 요소에 대한 값 정의  1) payment_method_information > period(정산 기간)  D : 일별 W : 주별 M : 월별 |

### Retrieve a list of Payment Gateway contract details   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| payment_gateway_name | PG 이름 |
| partner_id | PG사 발급 가맹점 ID |

```bash
Retrieve a list of Payment Gateway contract details        Retrieve a list of Payment Gateway contract details Retrieve paymentgateway with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/financials/paymentgateway?payment_gateway_name=cafe24Test_S' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "paymentgateway": {        "partner_id": "cafe24_Test",        "payment_gateway_name": "cafe24payTest",        "contract_date": "2020-01-01",        "setting_date": "2020-01-02",        "status": "T",        "bank_code": "013",        "bank_account_no": "123456789123",        "bank_account_name": "Test",        "payment_method_information": [            {                "payment_method": "card",                "period": "M",                "period_information": "1"            },            {                "payment_method": "tcash",                "period": "W",                "period_information": "1"            }        ]    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/financials/paymentgateway?payment_gateway_name=cafe24Test_S' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "paymentgateway": {        "partner_id": "cafe24_Test",        "payment_gateway_name": "cafe24payTest",        "contract_date": "2020-01-01",        "setting_date": "2020-01-02",        "status": "T",        "bank_code": "013",        "bank_account_no": "123456789123",        "bank_account_name": "Test",        "payment_method_information": [            {                "payment_method": "card",                "period": "M",                "period_information": "1"            },            {                "payment_method": "tcash",                "period": "W",                "period_information": "1"            }        ]    }}
```
