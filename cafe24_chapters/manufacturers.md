# MANUFACTURERS


## Manufacturers

```json
Endpoints    GET /api/v2/admin/manufacturers
GET /api/v2/admin/manufacturers/{manufacturer_code}
GET /api/v2/admin/manufacturers/count
POST /api/v2/admin/manufacturers
PUT /api/v2/admin/manufacturers/{manufacturer_code}
```

```json
GET /api/v2/admin/manufacturers
GET /api/v2/admin/manufacturers/{manufacturer_code}
GET /api/v2/admin/manufacturers/count
POST /api/v2/admin/manufacturers
PUT /api/v2/admin/manufacturers/{manufacturer_code}
```

### Manufacturers property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| manufacturer_code형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 제조사 코드 시스템이 부여한 제조사의 코드. 해당 쇼핑몰 내에서 제조사 코드는 중복되지 않는다. |
| manufacturer_name최대글자수 : [50자] | 제조사명 제조사의 이름. 제조사명은 쇼핑몰 관리자 화면에서 제조사를 구분할 수 있는 기본적인 정보이다. |
| president_name최대글자수 : [30자] | 대표자명 제조사의 대표자 이름. |
| use_manufacturer | 사용여부 해당 제조사를 사용하는지 여부 표시 T : 사용함 F : 사용안함 |
| email최대글자수 : [255자] | 이메일 제조사의 문의 메일. |
| phone최대글자수 : [20자] | 전화번호 제조사의 전화번호. |
| homepage최대글자수 : [255자] | 홈페이지 제조사의 홈페이지 주소 |
| zipcode | 우편번호 제조사의 사업장 우편번호. |
| country_code | 국가코드 |
| address1최대글자수 : [255자] | 기본 주소 제조사의 사업장 주소(시/군/구 단위 표기) |
| address2최대글자수 : [255자] | 상세 주소 제조사의 사업장 주소(상세 주소 표기) |
| created_date | 생성일 |

### Retrieve a list of manufacturers   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 읽기권한 (mall.read_collection) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| manufacturer_code | 제조사 코드   조회하고자 하는 제조사의 코드.   ,(콤마)로 여러 건을 검색할 수 있다. |
| manufacturer_name | 제조사명   ,(콤마)로 여러 건을 검색할 수 있다. |
| use_manufacturer | 제조사 사용여부   T : 사용함 F : 사용안함 |
| offset최대값: [8000] | 조회결과 시작위치   조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   조회하고자 하는 최대 건수를 지정할 수 있음. 예) 10 입력시 10건만 표시함.   DEFAULT 10 |

```bash
Retrieve a list of manufacturers        Retrieve a list of manufacturers Retrieve manufacturers with fields parameter Retrieve manufacturers using paging Retrieve a specific manufacturers with manufacturer_code parameter Retrieve multiple manufacturers       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/manufacturers' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "manufacturers": [        {            "shop_no": 1,            "manufacturer_code": "M0000000",            "manufacturer_name": "Sample Manufacturer",            "president_name": "Sample Administrator",            "use_manufacturer": "T"        },        {            "shop_no": 1,            "manufacturer_code": "M000000C",            "manufacturer_name": "Sample Manufacturer",            "president_name": "Sample Administrator",            "use_manufacturer": "F"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/manufacturers' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "manufacturers": [        {            "shop_no": 1,            "manufacturer_code": "M0000000",            "manufacturer_name": "Sample Manufacturer",            "president_name": "Sample Administrator",            "use_manufacturer": "T"        },        {            "shop_no": 1,            "manufacturer_code": "M000000C",            "manufacturer_name": "Sample Manufacturer",            "president_name": "Sample Administrator",            "use_manufacturer": "F"        }    ]}
```

### Retrieve a manufacturer   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 읽기권한 (mall.read_collection) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| manufacturer_codeRequired형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 제조사 코드 |

```bash
Retrieve a manufacturer        Retrieve a manufacturer Retrieve a manufacturer with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/manufacturers/M0000000' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "manufacturer": {        "shop_no": 1,        "manufacturer_code": "M0000000",        "manufacturer_name": "Sample Manufacturer",        "president_name": "Sample User",        "email": "sample@sample.com",        "phone": "010-000-0000",        "homepage": "http://sample.com",        "zipcode": "00000",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "created_date": "2018-09-01T15:00:00+09:00",        "use_manufacturer": "T"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/manufacturers/M0000000' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "manufacturer": {        "shop_no": 1,        "manufacturer_code": "M0000000",        "manufacturer_name": "Sample Manufacturer",        "president_name": "Sample User",        "email": "sample@sample.com",        "phone": "010-000-0000",        "homepage": "http://sample.com",        "zipcode": "00000",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "created_date": "2018-09-01T15:00:00+09:00",        "use_manufacturer": "T"    }}
```

### Retrieve a count of manufacturers   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 읽기권한 (mall.read_collection) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| manufacturer_code | 제조사 코드   조회하고자 하는 제조사의 코드.   ,(콤마)로 여러 건을 검색할 수 있다. |
| manufacturer_name | 제조사명   검색어를 제조사명에 포함하고 있는 공급사 검색(대소문자 구분 없음)   ,(콤마)로 여러 건을 검색할 수 있다. |
| use_manufacturer | 제조사 사용여부   T : 사용함 F : 사용안함 |

```bash
Retrieve a count of manufacturers        Retrieve a count of manufacturers       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/manufacturers/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "count": 2}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/manufacturers/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "count": 2}
```

### Create a manufacturer   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 쓰기권한 (mall.write_collection) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| manufacturer_nameRequired | 제조사명 |
| president_nameRequired최대글자수 : [30자] | 대표자명 |
| email최대글자수 : [255자]이메일 | 이메일 |
| phone최대글자수 : [20자]전화번호 | 전화번호 |
| homepage최대글자수 : [255자] | 홈페이지 |
| zipcode | 우편번호 |
| address1최대글자수 : [255자] | 기본 주소 |
| address2최대글자수 : [255자] | 상세 주소 |
| country_code | 국가코드 |
| use_manufacturer | 사용여부   T : 사용함 F : 사용안함 |

```bash
Create a manufacturer        Create a manufacturer Create a manufacturer using only manufacturer_name and president_name fields Try creating a manufacturer without manufacturer_name field Try creating a manufacturer without president_name field       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/manufacturers' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "manufacturer_name": "Sample Manufacturer",        "president_name": "Sample User",        "email": "sample@sample.com",        "phone": "010-000-0000",        "homepage": "http://sample.com",        "zipcode": "00000",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "use_manufacturer": "T"    }}'    Response  Copy     {    "manufacturer": {        "shop_no": 1,        "manufacturer_code": "M0000000",        "manufacturer_name": "Sample Manufacturer",        "president_name": "Sample User",        "email": "sample@sample.com",        "phone": "010-000-0000",        "homepage": "http://sample.com",        "zipcode": "00000",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "use_manufacturer": "T"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/manufacturers' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "manufacturer_name": "Sample Manufacturer",        "president_name": "Sample User",        "email": "sample@sample.com",        "phone": "010-000-0000",        "homepage": "http://sample.com",        "zipcode": "00000",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "use_manufacturer": "T"    }}'
```

```json
{    "manufacturer": {        "shop_no": 1,        "manufacturer_code": "M0000000",        "manufacturer_name": "Sample Manufacturer",        "president_name": "Sample User",        "email": "sample@sample.com",        "phone": "010-000-0000",        "homepage": "http://sample.com",        "zipcode": "00000",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "use_manufacturer": "T"    }}
```

### Update a manufacturer   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 쓰기권한 (mall.write_collection) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| manufacturer_codeRequired형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 제조사 코드 |
| manufacturer_name | 제조사명 |
| president_name | 대표자명 |
| email최대글자수 : [255자]이메일 | 이메일 |
| phone최대글자수 : [20자]전화번호 | 전화번호 |
| homepage최대글자수 : [255자] | 홈페이지 |
| zipcode | 우편번호 |
| address1최대글자수 : [255자] | 기본 주소 |
| address2최대글자수 : [255자] | 상세 주소 |
| country_code | 국가코드 |
| use_manufacturer | 사용여부   T : 사용함 F : 사용안함 |

```bash
Update a manufacturer        Update a manufacturer Update the manufacturer name Disable the manufacturer       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/manufacturers/M000000A' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "manufacturer_name": "Sample Manufacturer",        "president_name": "Sample User",        "email": "sample@sample.com",        "phone": "010-000-0000",        "homepage": "http://sample.com",        "zipcode": "00000",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "use_manufacturer": "T"    }}'    Response  Copy     {    "manufacturer": {        "shop_no": 1,        "manufacturer_code": "M000000A",        "manufacturer_name": "Sample Manufacturer",        "president_name": "Sample User",        "email": "sample@sample.com",        "phone": "010-000-0000",        "homepage": "http://sample.com",        "zipcode": "00000",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "use_manufacturer": "T"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/manufacturers/M000000A' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "manufacturer_name": "Sample Manufacturer",        "president_name": "Sample User",        "email": "sample@sample.com",        "phone": "010-000-0000",        "homepage": "http://sample.com",        "zipcode": "00000",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "use_manufacturer": "T"    }}'
```

```json
{    "manufacturer": {        "shop_no": 1,        "manufacturer_code": "M000000A",        "manufacturer_name": "Sample Manufacturer",        "president_name": "Sample User",        "email": "sample@sample.com",        "phone": "010-000-0000",        "homepage": "http://sample.com",        "zipcode": "00000",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "use_manufacturer": "T"    }}
```
