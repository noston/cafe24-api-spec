# URGENTINQUIRY REPLY


## Urgentinquiry reply

```json
Endpoints    GET /api/v2/admin/urgentinquiry/{article_no}/reply
POST /api/v2/admin/urgentinquiry/{article_no}/reply
PUT /api/v2/admin/urgentinquiry/{article_no}/reply
```

```json
GET /api/v2/admin/urgentinquiry/{article_no}/reply
POST /api/v2/admin/urgentinquiry/{article_no}/reply
PUT /api/v2/admin/urgentinquiry/{article_no}/reply
```

### Urgentinquiry reply property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| article_no | 게시물 번호 |
| created_date날짜 | 답변 등록일 |
| status | 답변 처리 상태 F: 미처리 I: 처리중 T: 처리완료 |
| content | 답변 내용 |
| method | 답변 방법 E:이메일 S:SMS A:전부 |
| count | 답변 처리 횟수 |
| user_id | 처리중 또는 답변완료 한 운영자 아이디 |
| attached_file_detail | 첨부 파일 상세 |

### Retrieve a reply for urgent inquiry post   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 읽기권한 (mall.read_community) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| article_noRequired | 게시물 번호 |

```bash
Retrieve a reply for urgent inquiry post        Retrieve a reply for urgent inquiry post       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create a reply for urgent inquiry post   cafe24 youtube

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
| article_noRequired | 게시물 번호 |
| contentRequired | 답변 내용 |
| status | 답변 처리 상태   F: 미처리 I: 처리중 T: 처리완료   DEFAULT F |
| user_idRequired최대글자수 : [20자] | 처리중 또는 답변완료 한 운영자 아이디 |
| attach_file_urls | 첨부 파일 상세 |
| attach_file_urls 하위 요소 보기     nameRequired파일명 urlRequired파일 URL |

```bash
Create a reply for urgent inquiry post        Create a reply for urgent inquiry post Try creating a reply without required parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update a reply for urgent inquiry post   cafe24 youtube

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
| article_noRequired | 게시물 번호 |
| contentRequired | 답변 내용 |
| status | 답변 처리 상태   F: 미처리 I: 처리중 T: 처리완료 |
| user_id최대글자수 : [20자] | 처리중 또는 답변완료 한 운영자 아이디 |
| attach_file_urls | 첨부 파일 상세 |
| attach_file_urls 하위 요소 보기     nameRequired파일명 urlRequired파일 URL |

```bash
Update a reply for urgent inquiry post        Update a reply for urgent inquiry post Try updating a reply without required parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
