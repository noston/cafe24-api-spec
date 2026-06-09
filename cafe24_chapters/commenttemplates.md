# COMMENTTEMPLATES


## Commenttemplates

```json
Endpoints    GET /api/v2/admin/commenttemplates
GET /api/v2/admin/commenttemplates/{comment_no}
POST /api/v2/admin/commenttemplates
PUT /api/v2/admin/commenttemplates/{comment_no}
DELETE /api/v2/admin/commenttemplates/{comment_no}
```

```json
GET /api/v2/admin/commenttemplates
GET /api/v2/admin/commenttemplates/{comment_no}
POST /api/v2/admin/commenttemplates
PUT /api/v2/admin/commenttemplates/{comment_no}
DELETE /api/v2/admin/commenttemplates/{comment_no}
```

### Commenttemplates property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| comment_no | 자주 쓰는 답변 번호 |
| title Required최대글자수 : [256자] | 자주 쓰는 답변 제목 |
| content Required최대글자수 : [4000자] | 자주 쓰는 답변 내용 |
| board_type최소값: [1] | 게시판 분류 1 : 운영 2 : 일반 3 : 자료실 4 : 기타 5 : 상품 6 : 갤러리 7 : 1:1상담 11 : 한줄메모 |
| created_date날짜 | 생성일 |

### Retrieve frequently used answers   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 읽기권한 (mall.read_community) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| board_type | 게시판 분류   1 : 운영 2 : 일반 3 : 자료실 4 : 기타 5 : 상품 6 : 갤러리 7 : 1:1상담 11 : 한줄메모 |
| title최대글자수 : [100자] | 자주 쓰는 답변 제목 |
| since_comment_no최소값: [1]최대값: [2147483647] | 자주 쓰는 답변 번호 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve frequently used answers        Retrieve frequently used answers       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "commenttemplates": [        {            "shop_no": 1,            "comment_no": 124,            "title": "Frequently Used Answer Title",            "content": "This is the content of a frequently used answer. This content is automatically entered into the board answer.",            "board_type": 1,            "created_date": "2023-05-15T14:30:25+09:00",            "links": [                {                    "rel": "next",                    "href": "https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates?since_no=124&limit=10"                }            ]        },        {            "shop_no": 1,            "comment_no": 123,            "title": "Frequently Used Answer Regarding Shipping",            "content": "The product you ordered will be shipped within 1-2 business days. For inquiries related to shipping, please contact customer service.",            "board_type": 1,            "created_date": "2023-05-14T11:20:37+09:00",            "links": [                {                    "rel": "next",                    "href": "https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates?since_no=123&limit=10"                }            ]        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "commenttemplates": [        {            "shop_no": 1,            "comment_no": 124,            "title": "Frequently Used Answer Title",            "content": "This is the content of a frequently used answer. This content is automatically entered into the board answer.",            "board_type": 1,            "created_date": "2023-05-15T14:30:25+09:00",            "links": [                {                    "rel": "next",                    "href": "https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates?since_no=124&limit=10"                }            ]        },        {            "shop_no": 1,            "comment_no": 123,            "title": "Frequently Used Answer Regarding Shipping",            "content": "The product you ordered will be shipped within 1-2 business days. For inquiries related to shipping, please contact customer service.",            "board_type": 1,            "created_date": "2023-05-14T11:20:37+09:00",            "links": [                {                    "rel": "next",                    "href": "https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates?since_no=123&limit=10"                }            ]        }    ]}
```

### Retrieve a frequently used answer   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 읽기권한 (mall.read_community) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| comment_noRequired최소값: [1] | 해당 댓글번호 이후 검색 |

```bash
Retrieve a frequently used answer        Retrieve a frequently used answer       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates/124' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "commenttemplate": {        "shop_no": 1,        "comment_no": 124,        "title": "Frequently Used Answer Regarding Shipping",        "content": "The order will be shipped within 1-2 business days from the date of purchase. Please contact the customer center for inquiries regarding shipping.",        "board_type": 1,        "created_date": "2023-05-14T11:20:37+09:00"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates/124' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "commenttemplate": {        "shop_no": 1,        "comment_no": 124,        "title": "Frequently Used Answer Regarding Shipping",        "content": "The order will be shipped within 1-2 business days from the date of purchase. Please contact the customer center for inquiries regarding shipping.",        "board_type": 1,        "created_date": "2023-05-14T11:20:37+09:00"    }}
```

### Create a frequently used answer   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 쓰기권한 (mall.write_community) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| titleRequired최대글자수 : [256자] | 자주 쓰는 답변 제목 |
| contentRequired최대글자수 : [4000자] | 자주 쓰는 답변 내용 |
| board_typeRequired최소값: [1] | 게시판 분류   1 : 운영 2 : 일반 3 : 자료실 4 : 기타 5 : 상품 6 : 갤러리 7 : 1:1상담 11 : 한줄메모 |

```bash
Create a frequently used answer        Create a frequently used answer       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "title": "Frequently Used Answer Title",        "content": "Frequently Used Answer Content",        "board_type": 1    }}'    Response  Copy     {    "commenttemplate": {        "shop_no": 1,        "comment_no": 1,        "title": "Frequently Used Answer Title",        "content": "Frequently Used Answer Content",        "board_type": 1,        "created_date": "2023-05-14T11:20:37+09:00"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "title": "Frequently Used Answer Title",        "content": "Frequently Used Answer Content",        "board_type": 1    }}'
```

```json
{    "commenttemplate": {        "shop_no": 1,        "comment_no": 1,        "title": "Frequently Used Answer Title",        "content": "Frequently Used Answer Content",        "board_type": 1,        "created_date": "2023-05-14T11:20:37+09:00"    }}
```

### Update a frequently used answer   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 쓰기권한 (mall.write_community) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| comment_noRequired최소값: [1] | 자주 쓰는 답변 번호 |
| title최대글자수 : [256자] | 자주 쓰는 답변 제목 |
| content최대글자수 : [4000자] | 자주 쓰는 답변 내용 |
| board_type최소값: [1] | 게시판 분류   1 : 운영 2 : 일반 3 : 자료실 4 : 기타 5 : 상품 6 : 갤러리 7 : 1:1상담 11 : 한줄메모 |

```bash
Update a frequently used answer        Update a frequently used answer       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates/123' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "subject": "Modified frequently used answer title",        "content": "This is the modified content of the frequently used answer. This content is automatically entered into the board answer.",        "board_type": 1    }}'    Response  Copy     {    "commenttemplate": {        "shop_no": 1,        "comment_no": 123,        "title": "Modified frequently used answer title",        "content": "This is the modified content of the frequently used answer. This content is automatically entered into the board answer.",        "board_type": 1,        "created_date": "2023-05-14T11:20:37+09:00"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates/123' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "subject": "Modified frequently used answer title",        "content": "This is the modified content of the frequently used answer. This content is automatically entered into the board answer.",        "board_type": 1    }}'
```

```json
{    "commenttemplate": {        "shop_no": 1,        "comment_no": 123,        "title": "Modified frequently used answer title",        "content": "This is the modified content of the frequently used answer. This content is automatically entered into the board answer.",        "board_type": 1,        "created_date": "2023-05-14T11:20:37+09:00"    }}
```

### Delete a frequently used answer   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 쓰기권한 (mall.write_community) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| comment_noRequired최소값: [1] | 자주 쓰는 답변 번호 |

```bash
Delete a frequently used answer        Delete a frequently used answer       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates/123' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "commenttemplate": {        "shop_no": 1,        "comment_no": 123,        "title": "Frequently Used Answer Title",        "content": "Frequently Used Answer Content",        "board_type": 1,        "created_date": "2023-05-14 11:20:37"    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/commenttemplates/123' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "commenttemplate": {        "shop_no": 1,        "comment_no": 123,        "title": "Frequently Used Answer Title",        "content": "Frequently Used Answer Content",        "board_type": 1,        "created_date": "2023-05-14 11:20:37"    }}
```
