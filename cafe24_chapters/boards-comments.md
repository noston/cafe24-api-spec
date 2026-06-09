# BOARDS COMMENTS


## Boards comments

```json
Endpoints    GET /api/v2/admin/boards/{board_no}/comments
```

```json
GET /api/v2/admin/boards/{board_no}/comments
```

### Boards comments property list

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
| links | link |

### Retrieve comments in bulk   cafe24 youtube

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
| since_comment_no최소값: [1]최대값: [2147483647] | 해당 댓글번호 이후 검색 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve comments in bulk        Retrieve comments in bulk       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
