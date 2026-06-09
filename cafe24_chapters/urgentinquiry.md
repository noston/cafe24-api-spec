# URGENTINQUIRY


## Urgentinquiry

```json
Endpoints    GET /api/v2/admin/urgentinquiry
```

```json
GET /api/v2/admin/urgentinquiry
```

### Urgentinquiry property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| article_no | 게시물 번호 |
| article_type | 게시물 유형 |
| title | 제목 |
| writer | 작성자명 |
| member_id | 회원아이디 |
| start_date날짜 | 작성일 시작일자 |
| reply_status | 답변 처리 상태 F: 미처리 I: 처리중 T: 처리완료 |
| hit | 조회수 |
| content | 내용 |
| writer_email이메일 | 작성자 이메일 |
| phone전화번호 | 전화번호 |
| search_type | 검색 타입 P:상품 O:주문 |
| keyword | 검색어 |
| attached_file_detail | 첨부 파일 상세 |

### Retrieve an urgent inquiry post   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 읽기권한 (mall.read_community) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| start_date날짜 | 작성일 시작일자 |
| end_date날짜 | 작성일 종료일자 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve an urgent inquiry post        Retrieve an urgent inquiry post       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/urgentinquiry' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "urgentinquiry": [        {            "shop_no": 1,            "article_no": 2,            "article_type": "type text",            "title": "subject text",            "writer": "John Doe",            "member_id": "sampleid",            "start_date": "2022-04-06T10:32:34+09:00",            "reply_status": "T",            "hit": 8,            "content": "content text",            "writer_email": "sample@sample.com",            "phone": "010-1111-2222",            "search_type": "P",            "keyword": "P000000J",            "attached_file_detail": [                {                    "no": 1,                    "source": "dev_starter_p1.png",                    "name": "/2022/04/06/696717133bf7971d5125f2a05ce16d49.png"                },                {                    "no": 2,                    "source": "dev_basic_p2.png",                    "name": "/2022/04/06/d0d3944674d139312bdf79853201b4c6.png"                }            ]        },        {            "shop_no": 1,            "article_no": 3,            "article_type": "type text",            "title": "subject text",            "writer": "John Doe",            "member_id": "sampleid",            "start_date": "2022-04-06T10:32:34+09:00",            "reply_status": "T",            "hit": 8,            "content": "content text",            "writer_email": "sample@sample.com",            "phone": "010-1111-2222",            "search_type": "P",            "keyword": "P000000J",            "attached_file_detail": [                {                    "no": 1,                    "source": "dev_starter_p1.png",                    "name": "/2022/04/06/696717133bf7971d5125f2a05ce16d49.png"                },                {                    "no": 2,                    "source": "dev_basic_p2.png",                    "name": "/2022/04/06/d0d3944674d139312bdf79853201b4c6.png"                }            ]        }    ],    "links": [        {            "rel": "prev",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/urgentinquiry?limit=10&offset=0"        },        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/urgentinquiry?limit=10&offset=20"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/urgentinquiry' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "urgentinquiry": [        {            "shop_no": 1,            "article_no": 2,            "article_type": "type text",            "title": "subject text",            "writer": "John Doe",            "member_id": "sampleid",            "start_date": "2022-04-06T10:32:34+09:00",            "reply_status": "T",            "hit": 8,            "content": "content text",            "writer_email": "sample@sample.com",            "phone": "010-1111-2222",            "search_type": "P",            "keyword": "P000000J",            "attached_file_detail": [                {                    "no": 1,                    "source": "dev_starter_p1.png",                    "name": "/2022/04/06/696717133bf7971d5125f2a05ce16d49.png"                },                {                    "no": 2,                    "source": "dev_basic_p2.png",                    "name": "/2022/04/06/d0d3944674d139312bdf79853201b4c6.png"                }            ]        },        {            "shop_no": 1,            "article_no": 3,            "article_type": "type text",            "title": "subject text",            "writer": "John Doe",            "member_id": "sampleid",            "start_date": "2022-04-06T10:32:34+09:00",            "reply_status": "T",            "hit": 8,            "content": "content text",            "writer_email": "sample@sample.com",            "phone": "010-1111-2222",            "search_type": "P",            "keyword": "P000000J",            "attached_file_detail": [                {                    "no": 1,                    "source": "dev_starter_p1.png",                    "name": "/2022/04/06/696717133bf7971d5125f2a05ce16d49.png"                },                {                    "no": 2,                    "source": "dev_basic_p2.png",                    "name": "/2022/04/06/d0d3944674d139312bdf79853201b4c6.png"                }            ]        }    ],    "links": [        {            "rel": "prev",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/urgentinquiry?limit=10&offset=0"        },        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/urgentinquiry?limit=10&offset=20"        }    ]}
```
