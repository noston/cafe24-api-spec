# TRANSLATIONS CATEGORIES


## Translations categories

```json
Endpoints    GET /api/v2/admin/translations/categories
PUT /api/v2/admin/translations/categories/{category_no}
```

```json
GET /api/v2/admin/translations/categories
PUT /api/v2/admin/translations/categories/{category_no}
```

### Translations categories property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| category_no | 분류 번호 |
| translations | 번역 정보 |

### Retrieve a list of product category translations   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 번역 읽기권한 (mall.read_translation) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| category_no | 분류 번호   ,(콤마)로 여러 건을 검색할 수 있다. |
| language_code | 언어 코드   번역 정보의 언어 코드에 해당되는 번역 정보를 검색  언어별로 번역된 정보에서 검색하고자 하는 언어를 선택하면, 해당 언어에 대한 번역 내용을 확인할 수 있습니다.   ,(콤마)로 여러 건을 검색할 수 있다. |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve a list of product category translations        Retrieve a list of product category translations       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/categories' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "categories": [        {            "shop_no": 1,            "category_no": 27,            "translations": [                {                    "language_code": "en_US",                    "translated": "T",                    "category_name": "(Detailed Category) Cropped",                    "seo": {                        "meta_title": "Browser Title",                        "meta_author": "Cafe24",                        "meta_description": "This is a sample product.",                        "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                    },                    "updated_date": "2018-01-19T11:19:27+09:00"                },                {                    "language_code": "es_ES",                    "translated": "T",                    "category_name": "(Detailed Category) Cropped",                    "seo": {                        "meta_title": "Browser Title",                        "meta_author": "Cafe24",                        "meta_description": "This is a sample product.",                        "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                    },                    "updated_date": "2018-01-19T11:19:27+09:00"                }            ]        },        {            "shop_no": 1,            "category_no": 28,            "translations": [                {                    "language_code": "en_US",                    "translated": "T",                    "category_name": "(Detailed Category) Cropped",                    "seo": {                        "meta_title": "Browser Title",                        "meta_author": "Cafe24",                        "meta_description": "This is a sample product.",                        "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                    },                    "updated_date": "2018-01-19T11:19:27+09:00"                },                {                    "language_code": "es_ES",                    "translated": "T",                    "category_name": "(Detailed Category) Cropped",                    "seo": {                        "meta_title": "Browser Title",                        "meta_author": "Cafe24",                        "meta_description": "This is a sample product.",                        "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                    },                    "updated_date": "2018-01-19T11:19:27+09:00"                }            ]        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/translations/categories?limit=10&offset=10"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/categories' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "categories": [        {            "shop_no": 1,            "category_no": 27,            "translations": [                {                    "language_code": "en_US",                    "translated": "T",                    "category_name": "(Detailed Category) Cropped",                    "seo": {                        "meta_title": "Browser Title",                        "meta_author": "Cafe24",                        "meta_description": "This is a sample product.",                        "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                    },                    "updated_date": "2018-01-19T11:19:27+09:00"                },                {                    "language_code": "es_ES",                    "translated": "T",                    "category_name": "(Detailed Category) Cropped",                    "seo": {                        "meta_title": "Browser Title",                        "meta_author": "Cafe24",                        "meta_description": "This is a sample product.",                        "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                    },                    "updated_date": "2018-01-19T11:19:27+09:00"                }            ]        },        {            "shop_no": 1,            "category_no": 28,            "translations": [                {                    "language_code": "en_US",                    "translated": "T",                    "category_name": "(Detailed Category) Cropped",                    "seo": {                        "meta_title": "Browser Title",                        "meta_author": "Cafe24",                        "meta_description": "This is a sample product.",                        "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                    },                    "updated_date": "2018-01-19T11:19:27+09:00"                },                {                    "language_code": "es_ES",                    "translated": "T",                    "category_name": "(Detailed Category) Cropped",                    "seo": {                        "meta_title": "Browser Title",                        "meta_author": "Cafe24",                        "meta_description": "This is a sample product.",                        "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                    },                    "updated_date": "2018-01-19T11:19:27+09:00"                }            ]        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/translations/categories?limit=10&offset=10"        }    ]}
```

### Update product category translation   cafe24

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
| category_noRequired | 분류 번호 |
| translations | 번역 정보 |
| translations 하위 요소 보기     language_codeRequired언어 코드 category_name분류명 seo Array    seo 하위 요소 보기     meta_title브라우저 타이틀 meta_author메타태그1 : Author meta_description메타태그2 : Description meta_keywords메타태그3 : Keywords |

```bash
Update product category translation        Update product category translation       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/categories/27' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "translations": [            {                "language_code": "en_US",                "category_name": "(Detailed Category) Cropped",                "seo": {                    "meta_title": "Browser Title",                    "meta_author": "Cafe24",                    "meta_description": "This is a sample product.",                    "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                }            },            {                "language_code": "es_ES",                "category_name": "(Detailed Category) Cropped",                "seo": {                    "meta_title": "Browser Title",                    "meta_author": "Cafe24",                    "meta_description": "This is a sample product.",                    "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                }            }        ]    }}'    Response  Copy     {    "category": {        "shop_no": 1,        "category_no": 27,        "translations": [            {                "language_code": "en_US",                "translated": "T",                "category_name": "(Detailed Category) Cropped",                "seo": {                    "meta_title": "Browser Title",                    "meta_author": "Cafe24",                    "meta_description": "This is a sample product.",                    "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                },                "updated_date": "2018-01-19T11:19:27+09:00"            },            {                "language_code": "es_ES",                "category_name": "(Detailed Category) Cropped",                "seo": {                    "meta_title": "Browser Title",                    "meta_author": "Cafe24",                    "meta_description": "This is a sample product.",                    "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                },                "updated_date": "2018-01-19T11:19:27+09:00"            }        ]    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/categories/27' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "translations": [            {                "language_code": "en_US",                "category_name": "(Detailed Category) Cropped",                "seo": {                    "meta_title": "Browser Title",                    "meta_author": "Cafe24",                    "meta_description": "This is a sample product.",                    "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                }            },            {                "language_code": "es_ES",                "category_name": "(Detailed Category) Cropped",                "seo": {                    "meta_title": "Browser Title",                    "meta_author": "Cafe24",                    "meta_description": "This is a sample product.",                    "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                }            }        ]    }}'
```

```json
{    "category": {        "shop_no": 1,        "category_no": 27,        "translations": [            {                "language_code": "en_US",                "translated": "T",                "category_name": "(Detailed Category) Cropped",                "seo": {                    "meta_title": "Browser Title",                    "meta_author": "Cafe24",                    "meta_description": "This is a sample product.",                    "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                },                "updated_date": "2018-01-19T11:19:27+09:00"            },            {                "language_code": "es_ES",                "category_name": "(Detailed Category) Cropped",                "seo": {                    "meta_title": "Browser Title",                    "meta_author": "Cafe24",                    "meta_description": "This is a sample product.",                    "meta_keywords": "sample keyword1,sample keyword2, sample keyword3, ..."                },                "updated_date": "2018-01-19T11:19:27+09:00"            }        ]    }}
```
