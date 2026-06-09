# BOARDS ARTICLES


## Boards articles

```json
Endpoints    GET /api/v2/admin/boards/{board_no}/articles
POST /api/v2/admin/boards/{board_no}/articles
PUT /api/v2/admin/boards/{board_no}/articles/{article_no}
DELETE /api/v2/admin/boards/{board_no}/articles/{article_no}
```

```json
GET /api/v2/admin/boards/{board_no}/articles
POST /api/v2/admin/boards/{board_no}/articles
PUT /api/v2/admin/boards/{board_no}/articles/{article_no}
DELETE /api/v2/admin/boards/{board_no}/articles/{article_no}
```

### Boards articles property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| article_no최대값: [2147483647] | 게시물 번호 |
| parent_article_no | 부모 게시물 번호 |
| board_no Required | 게시판 번호 |
| product_no | 상품번호 |
| category_no | 분류 번호 |
| board_category_no | 게시판 카테고리 번호 |
| reply_sequence | 답변 게시물 순서 |
| reply_depth | 답변 차수 |
| created_date날짜 | 생성일 |
| writer | 작성자명 |
| writer_email이메일 | 작성자 이메일 |
| member_id | 회원아이디 |
| title | 제목 |
| content | 내용 |
| supplier_id형식 : [a-z0-9]글자수 최소: [4자]~최대: [16자] | 공급사 아이디 |
| client_ipIP | 작성자 IP |
| nick_name | 별명 |
| rating최소: [1]~최대: [5] | 평점 |
| sales_channel최대글자수 : [20자] | 매체사 |
| reply_mail | 1:1 게시판 문의내용에 대한 답변 메일 여부 Y : 사용함 N : 사용안함 |
| display | 게시 여부 T : 게시함 F : 게시안함 |
| secret | 비밀글 여부 T : 사용함 F : 사용안함 |
| notice | 공지 여부 T : 사용함 F : 사용안함 |
| fixed | 고정글 여부 T : 사용함 F : 사용안함 |
| deleted | 삭제 구분 T: 삭제 F: 비삭제 B: 등록전 |
| input_channel | 게시물 작성 경로 P : PC M : 모바일 |
| order_id | 주문번호 |
| attach_file_urls | 첨부 파일 상세 |
| hit | 조회수 |
| reply | 1:1 게시판 문의내용에 대한 답변여부 T : 사용함 F : 사용안함 |
| reply_user_id | 처리중 또는 답변완료 한 운영자 아이디 |
| reply_status | 답변 처리 상태 N : 답변전 P : 처리중 C : 처리완료 |
| naverpay_review_id | 네이버페이 리뷰 아이디 |
| display_time | 노출시간 사용여부 |
| display_time_start_hour | 노출시간 시작 시각 |
| display_time_end_hour | 노출시간 종료 시각 |
| attached_file_detail | 첨부 파일 상세 |
| attached_file_urls | 첨부 파일 상세 |

### Retrieve a list of posts for a board   cafe24

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
| article_no최소값: [1] | 게시물 번호   ,(콤마)로 여러 건을 검색할 수 있다. |
| board_category_no | 게시판 카테고리 번호 |
| start_date날짜 | 검색 시작일(작성일)   검색을 시작할 기준일 또는 작성일 |
| end_date날짜 | 검색 종료일   검색을 종료할 기준일 검색 시작일과 같이 사용해야함. 검색기간은 한 호출에 1년 이상 검색 불가. |
| input_channel | 쇼핑몰 구분   P : PC M : 모바일 |
| search | 검색 영역   subject : 제목 content : 내용 writer_name : 작성자 product : 상품명 member_id : 회원 아이디 |
| keyword | 검색어 |
| reply_status | 답변상태   N : 답변 전 P : 처리중 C : 답변 완료 |
| comment | 댓글여부   T : 있음 F : 없음 |
| attached_file | 첨부파일 여부   T : 있음 F : 없음 |
| article_type | 게시물 유형   ,(콤마)로 여러 건을 검색할 수 있다.   all : 전체 normal : 일반글 notice : 공지글 fixed : 고정글 |
| product_no | 상품번호 |
| has_product | 상품정보 포함 여부   T : 있음 F : 없음 |
| is_notice | 공지 여부   T : 있음 F : 없음 |
| is_display | 게시 여부   T : 있음 F : 없음 |
| supplier_id형식 : [a-z0-9]글자수 최소: [4자]~최대: [16자] | 공급사 아이디 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve a list of posts for a board        Retrieve a list of posts for a board Retrieve articles with fields parameter Retrieve articles using paging Retrieve a specific articles with product_no parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create a board post   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 쓰기권한 (mall.write_community) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| board_noRequired | 게시판 번호 |
| writerRequired최대글자수 : [100자] | 작성자명 |
| titleRequired최대글자수 : [256자] | 제목 |
| contentRequired | 내용 |
| client_ipRequiredIP | 작성자 IP |
| reply_article_no | 답변 게시물 번호   게시물에 답변을 추가하고자 할 경우 게시물의 번호를 입력한다. |
| created_date날짜 | 생성일 |
| writer_email이메일 | 작성자 이메일 |
| member_id최대글자수 : [20자] | 회원아이디   member_id가 mall_id인 경우: 작성자는 shop_name이 반환됩니다. member_id를 입력하지 않거나, 회원 ID인 경우: 작성자는 writer 값이 반환됩니다. |
| notice | 공지 여부   T : 사용함 F : 사용안함   DEFAULT F |
| fixed | 고정글 여부   T : 사용함 F : 사용안함   DEFAULT F |
| deleted | 삭제 구분   T: 삭제 F: 비삭제 B: 등록전   DEFAULT F |
| reply | 1:1 게시판 문의내용에 대한 답변여부   T : 사용함 F : 사용안함   DEFAULT F |
| rating최소: [1]~최대: [5] | 평점 |
| sales_channel최대글자수 : [20자] | 매체사 |
| secret | 비밀글 여부   T : 사용함 F : 사용안함   DEFAULT F |
| password | 게시글 비밀번호 |
| reply_mail | 1:1 게시판 문의내용에 대한 답변 메일 여부   Y : 사용함 N : 사용안함   DEFAULT N |
| board_category_no | 게시판 카테고리 번호 |
| nick_name최대글자수 : [50자] | 별명 |
| input_channel | 게시물 작성 경로   P : PC M : 모바일   DEFAULT P |
| reply_user_id최대글자수 : [20자] | 처리중 또는 답변완료 한 운영자 아이디 |
| reply_status | 답변 처리 상태   N : 답변전 P : 처리중 C : 처리완료 |
| product_no최대값: [2147483647] | 상품번호 |
| category_no | 분류 번호 |
| order_id주문번호최대글자수 : [32자] | 주문번호 |
| naverpay_review_id최대글자수 : [20자] | 네이버페이 리뷰 아이디 |
| attach_file_urls | 첨부 파일 상세 |
| attach_file_urls 하위 요소 보기     name파일명 url파일 URL |

```bash
Create a board post        Create a board post Post an article of a board using only writer, title, content, and client_ip fields Try posting an article of a board without using writer field Try posting an article of a board without using title field Try posting an article of a board without using content field Try posting an article of a board without using client_ip field       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update a board post   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 쓰기권한 (mall.write_community) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| board_noRequired | 게시판 번호 |
| article_noRequired | 게시물 번호 |
| title최대글자수 : [256자] | 제목 |
| content | 내용 |
| rating최소: [1]~최대: [5] | 평점 |
| sales_channel최대글자수 : [20자] | 매체사 |
| board_category_no | 게시판 카테고리 번호 |
| display | 게시 여부   T : 게시함 F : 게시안함 |
| notice | 공지 여부   T : 사용함 F : 사용안함 |
| fixed | 고정글 여부   T : 사용함 F : 사용안함 |
| display_time_start_hour | 노출시간 시작 시각 |
| display_time_end_hour | 노출시간 종료 시각 |
| attach_file_url1URL | 파일 URL |
| attach_file_url2URL | 파일 URL |
| attach_file_url3URL | 파일 URL |
| attach_file_url4URL | 파일 URL |
| attach_file_url5URL | 파일 URL |

```bash
Update a board post        Update a board post Edit a title and contents of the article Update a display status of the article       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete a board post   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 쓰기권한 (mall.write_community) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| board_noRequired | 게시판 번호 |
| article_noRequired최대값: [2147483647] | 게시물 번호 |

```bash
Delete a board post        Delete a board post       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
