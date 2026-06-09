# RECIPES


## Recipes

```json
Endpoints    GET /api/v2/admin/recipes
POST /api/v2/admin/recipes
DELETE /api/v2/admin/recipes/{recipe_code}
```

```json
GET /api/v2/admin/recipes
POST /api/v2/admin/recipes
DELETE /api/v2/admin/recipes/{recipe_code}
```

### Recipes property list

| Attribute | Description |
| --- | --- |
| recipe_code | 레시피 코드 |
| recipe_name최대글자수 : [200자] | 레시피 이름 |
| active | 활성화 여부 T : 활성화 F : 비활성화 |

### Retrieve a list of recipes   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 읽기권한 (mall.read_application) |
| 호출건수 제한 | 40 |

```bash
Retrieve a list of recipes        Retrieve a list of recipes Retrieve recipes with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/recipes' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "recipes": [        {            "recipe_code": "111149-123456",            "recipe_name": "recipeName001",            "active": "T"        },        {            "recipe_code": "111149-123457",            "recipe_name": "recipeName002",            "active": "F"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/recipes' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "recipes": [        {            "recipe_code": "111149-123456",            "recipe_name": "recipeName001",            "active": "T"        },        {            "recipe_code": "111149-123457",            "recipe_name": "recipeName002",            "active": "F"        }    ]}
```

### Create a recipe   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 쓰기권한 (mall.write_application) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 100 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| recipe_codeRequired | 레시피 코드 |
| trigger_settings | 트리거 설정 |
| trigger_settings 하위 요소 보기     required_filters Array    required_filters 하위 요소 보기     name조건 이름 value조건 값 operator조건 연산자    optional_filters Array    optional_filters 하위 요소 보기     condition Array    condition 하위 요소 보기     name조건 이름 value조건 값 operator조건 연산자 |

```bash
Create a recipe        Create a recipe       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/recipes' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "requests": [        {            "recipe_code": "111149-123456",            "trigger_settings": {                "required_filters": [                    {                        "name": "event_shop_no",                        "value": 1,                        "operator": "eq"                    },                    {                        "name": "price",                        "value": 100,                        "operator": "ge"                    }                ],                "optional_filters": [                    {                        "condition": [                            {                                "name": "product_name",                                "value": "sample1",                                "operator": "like"                            },                            {                                "name": "supplier_code",                                "value": "S0000000",                                "operator": "eq"                            }                        ]                    },                    {                        "condition": [                            {                                "name": "product_name",                                "value": "sample2",                                "operator": "like"                            }                        ]                    }                ]            }        },        {            "recipe_code": "111149-123457",            "trigger_settings": {                "required_filters": [                    {                        "name": "event_shop_no",                        "value": 1,                        "operator": "eq"                    },                    {                        "name": "price",                        "value": 100,                        "operator": "ge"                    }                ],                "optional_filters": [                    {                        "condition": [                            {                                "name": "product_name",                                "value": "sample1",                                "operator": "like"                            },                            {                                "name": "supplier_code",                                "value": "S0000000",                                "operator": "eq"                            }                        ]                    },                    {                        "condition": [                            {                                "name": "product_name",                                "value": "sample2",                                "operator": "like"                            }                        ]                    }                ]            }        }    ]}'    Response  Copy     {    "recipes": [        {            "recipe_code": "111149-123456",            "active": "T"        },        {            "recipe_code": "111149-123457",            "active": "T"        }    ]}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/recipes' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "requests": [        {            "recipe_code": "111149-123456",            "trigger_settings": {                "required_filters": [                    {                        "name": "event_shop_no",                        "value": 1,                        "operator": "eq"                    },                    {                        "name": "price",                        "value": 100,                        "operator": "ge"                    }                ],                "optional_filters": [                    {                        "condition": [                            {                                "name": "product_name",                                "value": "sample1",                                "operator": "like"                            },                            {                                "name": "supplier_code",                                "value": "S0000000",                                "operator": "eq"                            }                        ]                    },                    {                        "condition": [                            {                                "name": "product_name",                                "value": "sample2",                                "operator": "like"                            }                        ]                    }                ]            }        },        {            "recipe_code": "111149-123457",            "trigger_settings": {                "required_filters": [                    {                        "name": "event_shop_no",                        "value": 1,                        "operator": "eq"                    },                    {                        "name": "price",                        "value": 100,                        "operator": "ge"                    }                ],                "optional_filters": [                    {                        "condition": [                            {                                "name": "product_name",                                "value": "sample1",                                "operator": "like"                            },                            {                                "name": "supplier_code",                                "value": "S0000000",                                "operator": "eq"                            }                        ]                    },                    {                        "condition": [                            {                                "name": "product_name",                                "value": "sample2",                                "operator": "like"                            }                        ]                    }                ]            }        }    ]}'
```

```json
{    "recipes": [        {            "recipe_code": "111149-123456",            "active": "T"        },        {            "recipe_code": "111149-123457",            "active": "T"        }    ]}
```

### Delete a recipe   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 쓰기권한 (mall.write_application) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| recipe_codeRequired | 레시피 코드 |

```bash
Delete a recipe        Delete a recipe       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/recipes/111490-111682' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "recipe": {        "recipe_code": "111490-111682"    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/recipes/111490-111682' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "recipe": {        "recipe_code": "111490-111682"    }}
```
