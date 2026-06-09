# SHIPPINGORIGINS


## Shippingorigins

```json
Endpoints    GET /api/v2/admin/shippingorigins
GET /api/v2/admin/shippingorigins/{origin_code}
POST /api/v2/admin/shippingorigins
PUT /api/v2/admin/shippingorigins/{origin_code}
DELETE /api/v2/admin/shippingorigins/{origin_code}
```

```json
GET /api/v2/admin/shippingorigins
GET /api/v2/admin/shippingorigins/{origin_code}
POST /api/v2/admin/shippingorigins
PUT /api/v2/admin/shippingorigins/{origin_code}
DELETE /api/v2/admin/shippingorigins/{origin_code}
```

### Shippingorigins property list

| Attribute | Description |
| --- | --- |
| origin_code Required형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 출고지 코드 |
| origin_name최대글자수 : [50자] | 출고지 명 |
| default | 출고지 기본설정 여부 T : 사용함 F : 사용안함 |
| country_code최대글자수 : [2자] | 국가코드 |
| zipcode최소글자수 : [2자]최대글자수 : [14자] | 우편번호 |
| address1최대글자수 : [255자] | 기본 주소 |
| address2최대글자수 : [255자] | 상세 주소 |
| contact | 대표 연락처 |
| secondary_contact | 보조 연락처 |
| variants | 출고지 품목 정보 |

### Retrieve a list of shipping origins   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 배송 읽기권한 (mall.read_shipping) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve a list of shipping origins        Retrieve a list of shipping origins       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "shippingorigins": [        {            "origin_code": "W0000000",            "origin_name": "Dongjak-gu Warehouse",            "default": "F",            "contact": "010-0000-0000",            "secondary_contact": "010-0000-0000",            "zipcode": "07071",            "country_code": "KR",            "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",            "address2": "Professional Construction Hall",            "variants": [                "P000000C000Q",                "P000000C000R"            ]        },        {            "origin_code": "W000000B",            "origin_name": "Boramae Warehouse",            "default": "F",            "contact": "010-0000-0000",            "secondary_contact": "010-0000-0000",            "zipcode": "07811",            "country_code": "KR",            "address1": "Dongjak-gu, Seoul, Republic of Korea",            "address2": "15, Boramae-ro 5-gil",            "variants": [                "P000000C000C",                "P000000C000F"            ]        }    ],    "links": [        {            "rel": "prev",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins?offset=0&limit=10"        },        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins?offset=20&limit=10"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "shippingorigins": [        {            "origin_code": "W0000000",            "origin_name": "Dongjak-gu Warehouse",            "default": "F",            "contact": "010-0000-0000",            "secondary_contact": "010-0000-0000",            "zipcode": "07071",            "country_code": "KR",            "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",            "address2": "Professional Construction Hall",            "variants": [                "P000000C000Q",                "P000000C000R"            ]        },        {            "origin_code": "W000000B",            "origin_name": "Boramae Warehouse",            "default": "F",            "contact": "010-0000-0000",            "secondary_contact": "010-0000-0000",            "zipcode": "07811",            "country_code": "KR",            "address1": "Dongjak-gu, Seoul, Republic of Korea",            "address2": "15, Boramae-ro 5-gil",            "variants": [                "P000000C000C",                "P000000C000F"            ]        }    ],    "links": [        {            "rel": "prev",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins?offset=0&limit=10"        },        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins?offset=20&limit=10"        }    ]}
```

### Retrieve a shipping origin   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 배송 읽기권한 (mall.read_shipping) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| origin_codeRequired형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 출고지 코드 |

```bash
Retrieve a shipping origin        Retrieve a shipping origin       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins/W000000Q' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "shippingorigin": {        "origin_code": "W000000Q",        "origin_name": "Dongjak-gu Warehouse",        "default": "F",        "contact": "010-0000-0000",        "secondary_contact": "010-0000-0000",        "zipcode": "07811",        "country_code": "KR",        "address1": "Dongjak-gu, Seoul, Republic of Korea",        "address2": "15, Boramae-ro 5-gil",        "variants": [            "P000000B000B",            "P000000B000C"        ]    },    "links": [        {            "rel": "self",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins/W000000Q"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins/W000000Q' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "shippingorigin": {        "origin_code": "W000000Q",        "origin_name": "Dongjak-gu Warehouse",        "default": "F",        "contact": "010-0000-0000",        "secondary_contact": "010-0000-0000",        "zipcode": "07811",        "country_code": "KR",        "address1": "Dongjak-gu, Seoul, Republic of Korea",        "address2": "15, Boramae-ro 5-gil",        "variants": [            "P000000B000B",            "P000000B000C"        ]    },    "links": [        {            "rel": "self",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins/W000000Q"        }    ]}
```

### Create a shipping origin   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 배송 쓰기권한 (mall.write_shipping) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| origin_nameRequired최대글자수 : [50자] | 출고지 명 |
| address1Required최대글자수 : [255자] | 기본 주소 |
| address2Required최대글자수 : [255자] | 상세 주소 |
| country_codeRequired최대글자수 : [2자] | 국가코드 |
| default | 출고지 기본설정 여부   T : 사용함 F : 사용안함   DEFAULT F |
| zipcode최소글자수 : [2자]최대글자수 : [14자] | 우편번호 |
| contact전화번호최대글자수 : [20자] | 대표 연락처 |
| secondary_contact전화번호최대글자수 : [20자] | 보조 연락처 |

```bash
Create a shipping origin        Create a shipping origin       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "origin_name": "Dongjak-gu warehouse",        "contact": "010-0000-0000",        "secondary_contact": "010-0000-0000",        "zipcode": "07071",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall"    }}'    Response  Copy     {    "shippingorigin": {        "origin_code": "W000000C",        "origin_name": "Dongjak-gu warehouse",        "default": "F",        "contact": "010-0000-0000",        "secondary_contact": "010-0000-0000",        "zipcode": "07071",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "variants": null    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "origin_name": "Dongjak-gu warehouse",        "contact": "010-0000-0000",        "secondary_contact": "010-0000-0000",        "zipcode": "07071",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall"    }}'
```

```json
{    "shippingorigin": {        "origin_code": "W000000C",        "origin_name": "Dongjak-gu warehouse",        "default": "F",        "contact": "010-0000-0000",        "secondary_contact": "010-0000-0000",        "zipcode": "07071",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "variants": null    }}
```

### Update a shipping origin   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 배송 쓰기권한 (mall.write_shipping) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| origin_codeRequired형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 출고지 코드 |
| origin_name최대글자수 : [50자] | 출고지 명 |
| country_code최대글자수 : [2자] | 국가코드 |
| default | 출고지 기본설정 여부   T : 사용함 F : 사용안함 |
| contact전화번호최대글자수 : [20자] | 대표 연락처 |
| secondary_contact전화번호최대글자수 : [20자] | 보조 연락처 |
| zipcode최소글자수 : [2자]최대글자수 : [14자] | 우편번호 |
| address1최대글자수 : [255자] | 기본 주소 |
| address2최대글자수 : [255자] | 상세 주소 |

```bash
Update a shipping origin        Update a shipping origin       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins/W000000Q' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "origin_name": "Dongjak-gu Warehouse",        "contact": "010-0000-0000",        "secondary_contact": "010-0000-0000",        "zipcode": "07071",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall"    }}'    Response  Copy     {    "shippingorigin": {        "origin_code": "W000000Q",        "origin_name": "Dongjak-gu Warehouse",        "default": "F",        "contact": "010-0000-0000",        "secondary_contact": "010-0000-0000",        "zipcode": "07071",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "variants": null    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins/W000000Q' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "origin_name": "Dongjak-gu Warehouse",        "contact": "010-0000-0000",        "secondary_contact": "010-0000-0000",        "zipcode": "07071",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall"    }}'
```

```json
{    "shippingorigin": {        "origin_code": "W000000Q",        "origin_name": "Dongjak-gu Warehouse",        "default": "F",        "contact": "010-0000-0000",        "secondary_contact": "010-0000-0000",        "zipcode": "07071",        "country_code": "KR",        "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",        "address2": "Professional Construction Hall",        "variants": null    }}
```

### Delete a shipping origin   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 배송 쓰기권한 (mall.write_shipping) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| origin_codeRequired형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 출고지 코드 |

```bash
Delete a shipping origin        Delete a shipping origin       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins/W000000Q' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "shippingorigin": {        "origin_code": "W000000Q"    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/shippingorigins/W000000Q' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "shippingorigin": {        "origin_code": "W000000Q"    }}
```
