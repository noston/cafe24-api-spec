# TRANSLATIONS STORE


## Translations store

```json
Endpoints    GET /api/v2/admin/translations/store
PUT /api/v2/admin/translations/store
```

```json
GET /api/v2/admin/translations/store
PUT /api/v2/admin/translations/store
```

### Translations store property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| translations | 번역 정보 |

### Retrieve a list of store translations   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 번역 읽기권한 (mall.read_translation) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| language_code | 언어 코드   언어별로 번역된 정보에서 검색하고자 하는 언어를 선택하면, 해당 언어에 대한 번역 내용을 확인할 수 있습니다.   ,(콤마)로 여러 건을 검색할 수 있다. |

```bash
Retrieve a list of store translations        Retrieve a list of store translations       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/store' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "store": {        "shop_no": 1,        "translations": [            {                "language_code": "en_US",                "translated": "T",                "shop_name": "sample shop",                "company_name": "sample company",                "company_registration_no": "118-81-20586",                "president_name": "Jone Doe",                "phone": "02-0000-0000",                "email": "sample@sample.com",                "fax": "02-0000-0000",                "zipcode": "07071",                "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",                "address2": "Professional Construction Hall",                "customer_service_phone": "02-0000-0000",                "customer_service_hours": "9:00 AM ~ 5:00 PM",                "privacy_officer_name": "Jane Doe",                "privacy_officer_email": "sample1@sample.com",                "updated_date": "2022-01-10T11:19:27+09:00"            },            {                "language_code": "es_ES",                "translated": "T",                "shop_name": "tienda de muestras",                "company_name": "compañía de muestras",                "company_registration_no": "118-81-20586",                "president_name": "Jone Doe",                "phone": "02-0000-0000",                "email": "sample@sample.com",                "fax": "02-0000-0000",                "zipcode": "07071",                "address1": "Sindaebang dong Dongjak-gu, Seúl, República de Corea",                "address2": "Hall de construcción profesional",                "customer_service_phone": "02-0000-0000",                "customer_service_hours": "9 de la mañana a 5 de la tarde",                "privacy_officer_name": "Jane Doe",                "privacy_officer_email": "sample1@sample.com",                "updated_date": "2022-01-10T11:19:27+09:00"            }        ]    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/store' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "store": {        "shop_no": 1,        "translations": [            {                "language_code": "en_US",                "translated": "T",                "shop_name": "sample shop",                "company_name": "sample company",                "company_registration_no": "118-81-20586",                "president_name": "Jone Doe",                "phone": "02-0000-0000",                "email": "sample@sample.com",                "fax": "02-0000-0000",                "zipcode": "07071",                "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",                "address2": "Professional Construction Hall",                "customer_service_phone": "02-0000-0000",                "customer_service_hours": "9:00 AM ~ 5:00 PM",                "privacy_officer_name": "Jane Doe",                "privacy_officer_email": "sample1@sample.com",                "updated_date": "2022-01-10T11:19:27+09:00"            },            {                "language_code": "es_ES",                "translated": "T",                "shop_name": "tienda de muestras",                "company_name": "compañía de muestras",                "company_registration_no": "118-81-20586",                "president_name": "Jone Doe",                "phone": "02-0000-0000",                "email": "sample@sample.com",                "fax": "02-0000-0000",                "zipcode": "07071",                "address1": "Sindaebang dong Dongjak-gu, Seúl, República de Corea",                "address2": "Hall de construcción profesional",                "customer_service_phone": "02-0000-0000",                "customer_service_hours": "9 de la mañana a 5 de la tarde",                "privacy_officer_name": "Jane Doe",                "privacy_officer_email": "sample1@sample.com",                "updated_date": "2022-01-10T11:19:27+09:00"            }        ]    }}
```

### Update the translations of a store   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 번역 쓰기권한 (mall.write_translation) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| translations | 번역 정보 |
| translations 하위 요소 보기     language_codeRequired언어 코드 shop_name쇼핑몰명 company_name상호명 company_registration_no사업자등록번호 president_name대표자명 phone전화번호 email이메일 fax팩스번호 zipcode우편번호 address1기본 주소 address2상세 주소 customer_service_phone고객센터 상담/주문 전화 customer_service_hours고객센터 운영시간 privacy_officer_name개인정보보호 책임자명 privacy_officer_email개인정보보호 책임자 이메일 |

```bash
Update the translations of a store        Update the translations of a store       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/store' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "translations": [            {                "language_code": "en_US",                "shop_name": "sample shop",                "company_name": "sample company",                "company_registration_no": "118-81-20586",                "president_name": "Jone Doe",                "phone": "02-0000-0000",                "email": "sample@sample.com",                "fax": "02-0000-0000",                "zipcode": "07071",                "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",                "address2": "Professional Construction Hall",                "customer_service_phone": "02-0000-0000",                "customer_service_hours": "9:00 AM ~ 5:00 PM",                "privacy_officer_name": "Jane Doe",                "privacy_officer_email": "sample1@sample.com"            },            {                "language_code": "es_ES",                "shop_name": "tienda de muestras",                "company_name": "compañía de muestras",                "company_registration_no": "118-81-20586",                "president_name": "Jone Doe",                "phone": "02-0000-0000",                "email": "sample@sample.com",                "fax": "02-0000-0000",                "zipcode": "07071",                "address1": "Sindaebang dong Dongjak-gu, Seúl, República de Corea",                "address2": "Hall de construcción profesional",                "customer_service_phone": "02-0000-0000",                "customer_service_hours": "9 de la mañana a 5 de la tarde",                "privacy_officer_name": "Jane Doe",                "privacy_officer_email": "sample1@sample.com"            }        ]    }}'    Response  Copy     {    "store": {        "shop_no": 1,        "translations": [            {                "language_code": "en_US",                "translated": "T",                "shop_name": "sample shop",                "company_name": "sample company",                "company_registration_no": "118-81-20586",                "president_name": "Jone Doe",                "phone": "02-0000-0000",                "email": "sample@sample.com",                "fax": "02-0000-0000",                "zipcode": "07071",                "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",                "address2": "Professional Construction Hall",                "customer_service_phone": "02-0000-0000",                "customer_service_hours": "9:00 AM ~ 5:00 PM",                "privacy_officer_name": "Jane Doe",                "privacy_officer_email": "sample1@sample.com",                "updated_date": "2022-01-10T11:19:27+09:00"            },            {                "language_code": "es_ES",                "translated": "T",                "shop_name": "tienda de muestras",                "company_name": "compañía de muestras",                "company_registration_no": "118-81-20586",                "president_name": "Jone Doe",                "phone": "02-0000-0000",                "email": "sample@sample.com",                "fax": "02-0000-0000",                "zipcode": "07071",                "address1": "Sindaebang dong Dongjak-gu, Seúl, República de Corea",                "address2": "Hall de construcción profesional",                "customer_service_phone": "02-0000-0000",                "customer_service_hours": "9 de la mañana a 5 de la tarde",                "privacy_officer_name": "Jane Doe",                "privacy_officer_email": "sample1@sample.com",                "updated_date": "2022-01-10T11:19:27+09:00"            }        ]    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/store' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "translations": [            {                "language_code": "en_US",                "shop_name": "sample shop",                "company_name": "sample company",                "company_registration_no": "118-81-20586",                "president_name": "Jone Doe",                "phone": "02-0000-0000",                "email": "sample@sample.com",                "fax": "02-0000-0000",                "zipcode": "07071",                "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",                "address2": "Professional Construction Hall",                "customer_service_phone": "02-0000-0000",                "customer_service_hours": "9:00 AM ~ 5:00 PM",                "privacy_officer_name": "Jane Doe",                "privacy_officer_email": "sample1@sample.com"            },            {                "language_code": "es_ES",                "shop_name": "tienda de muestras",                "company_name": "compañía de muestras",                "company_registration_no": "118-81-20586",                "president_name": "Jone Doe",                "phone": "02-0000-0000",                "email": "sample@sample.com",                "fax": "02-0000-0000",                "zipcode": "07071",                "address1": "Sindaebang dong Dongjak-gu, Seúl, República de Corea",                "address2": "Hall de construcción profesional",                "customer_service_phone": "02-0000-0000",                "customer_service_hours": "9 de la mañana a 5 de la tarde",                "privacy_officer_name": "Jane Doe",                "privacy_officer_email": "sample1@sample.com"            }        ]    }}'
```

```json
{    "store": {        "shop_no": 1,        "translations": [            {                "language_code": "en_US",                "translated": "T",                "shop_name": "sample shop",                "company_name": "sample company",                "company_registration_no": "118-81-20586",                "president_name": "Jone Doe",                "phone": "02-0000-0000",                "email": "sample@sample.com",                "fax": "02-0000-0000",                "zipcode": "07071",                "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",                "address2": "Professional Construction Hall",                "customer_service_phone": "02-0000-0000",                "customer_service_hours": "9:00 AM ~ 5:00 PM",                "privacy_officer_name": "Jane Doe",                "privacy_officer_email": "sample1@sample.com",                "updated_date": "2022-01-10T11:19:27+09:00"            },            {                "language_code": "es_ES",                "translated": "T",                "shop_name": "tienda de muestras",                "company_name": "compañía de muestras",                "company_registration_no": "118-81-20586",                "president_name": "Jone Doe",                "phone": "02-0000-0000",                "email": "sample@sample.com",                "fax": "02-0000-0000",                "zipcode": "07071",                "address1": "Sindaebang dong Dongjak-gu, Seúl, República de Corea",                "address2": "Hall de construcción profesional",                "customer_service_phone": "02-0000-0000",                "customer_service_hours": "9 de la mañana a 5 de la tarde",                "privacy_officer_name": "Jane Doe",                "privacy_officer_email": "sample1@sample.com",                "updated_date": "2022-01-10T11:19:27+09:00"            }        ]    }}
```
