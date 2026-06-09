# BOARDS ARTICLES COMMENTS


## Boards articles comments

```json
Endpoints    GET /api/v2/admin/boards/{board_no}/articles/{article_no}/comments
POST /api/v2/admin/boards/{board_no}/articles/{article_no}/comments
DELETE /api/v2/admin/boards/{board_no}/articles/{article_no}/comments/{comment_no}
```

```json
GET /api/v2/admin/boards/{board_no}/articles/{article_no}/comments
POST /api/v2/admin/boards/{board_no}/articles/{article_no}/comments
DELETE /api/v2/admin/boards/{board_no}/articles/{article_no}/comments/{comment_no}
```

### Boards articles comments property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| board_no | 게시판 번호 |
| article_no | 게시물 번호 |
| comment_no | 댓글 번호 |
| content | 댓글 내용 |
| writer최대글자수 : [100자] | 작성자명 |
| member_id최대글자수 : [20자] | 회원아이디 |
| created_date날짜 | 생성일 |
| client_ipIP | 작성자 IP |
| rating최소: [1]~최대: [5] | 댓글 평점 |
| secret | 비밀글 여부 T : 사용함 F : 사용안함 |
| parent_comment_no | 부모 댓글 번호 |
| input_channel | 쇼핑몰 구분 P : PC M : 모바일 |
| attach_file_urls | 첨부 파일 상세 |

### Retrieve a list of comments for a board post   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 읽기권한 (mall.read_community) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| board_noRequired | 게시판 번호 |
| article_noRequired | 게시물 번호 |
| comment_no | 댓글 번호 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve a list of comments for a board post        Retrieve a list of comments for a board post Retrieve comments with fields parameter Retrieve comments using paging Retrieve a specific comments with comment_no parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create a comment for a board post   cafe24 youtube

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
| board_noRequired | 게시판 번호 |
| article_noRequired | 게시물 번호 |
| contentRequired | 댓글 내용 |
| writerRequired최대글자수 : [100자] | 작성자명 |
| passwordRequired글자수 최소: [1자]~최대: [20자] | 댓글 비밀번호 |
| member_id최대글자수 : [20자] | 회원아이디 |
| rating최소: [1]~최대: [5] | 댓글 평점   DEFAULT 0 |
| secret | 비밀글 여부   T : 사용함 F : 사용안함   DEFAULT F |
| parent_comment_no최소값: [1] | 부모 댓글 번호 |
| input_channel | 쇼핑몰 구분   P : PC M : 모바일   DEFAULT P |
| created_date날짜 | 생성일 |
| attach_file_urls | 첨부 파일 상세 |
| attach_file_urls 하위 요소 보기     name파일명 url파일 URL |

```bash
Create a comment for a board post        Create a comment for a board post Post a comment at an article of a board using only content, writer, and password fields Try posting a comment at an article of a board without using content field Try posting a comment at an article of a board without using writer field Try posting a comment at an article of a board without using password field       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete a comment for a board post   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 쓰기권한 (mall.write_community) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| board_noRequired | 게시판 번호 |
| article_noRequired | 게시물 번호 |
| comment_noRequired | 댓글 번호 |

```bash
Delete a comment for a board post        Delete a comment for a board post       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
