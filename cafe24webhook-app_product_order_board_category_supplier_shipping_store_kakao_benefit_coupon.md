# 이벤트별 샘플 데이터

**이 문서에서는 WebHook 이벤트별 샘플 데이터와 각 파라미터 정보에 대해 설명합니다.  
샘플 데이터는 \[개발자 어드민 > 상품관리 > App 관리 > STEP 1. 개발정보관리 >WebHook\]에서 각 이벤트 등록 후, 목록에서도 확인 가능합니다.**

  

**목차**

-   [앱 이벤트별 샘플 데이터](https://developers.cafe24.com/app/front/app/develop/webhook/sample#title1)
-   [앱 이벤트 파라미터 정의](https://developers.cafe24.com/app/front/app/develop/webhook/sample#title2)
-   [쇼핑몰 이벤트별 샘플 데이터](https://developers.cafe24.com/app/front/app/develop/webhook/sample#title3)
-   [쇼핑몰 이벤트 파라미터 정의](https://developers.cafe24.com/app/front/app/develop/webhook/sample#title4)

**Note!**

샘플 데이터는 WebHook 수신 테스트를 위해 제공되며, 실제로 전송되는 데이터와 다를 수 있습니다.

  

  

## 앱 이벤트별 샘플 데이터

  

앱 이벤트별 샘플 데이터   

이벤트 NO.

이벤트

샘플 데이터

90077

쇼핑몰에 설치된 앱이 삭제된 경우

{
  "event\_no": 90077,
  "resource":{
    "mall\_id": "leesunsin",
    "client\_id": "sample7eBNEqSfkd7I8hoA",
    "app\_name": "sample\_app",
    "deleted\_date": "2020-07-01T12:30:15+09:00"
  }
}

90078

쇼핑몰에 설치된 앱이 만료된 경우

{
  "event\_no": 90078,
  "resource":{
    "mall\_id": "leesunsin",
     "client\_id": "sample7eBNEqSfkd7I8hoA",
    "app\_name": "sample\_app",
    "expired\_date": "2020-07-01T12:30:15+09:00"
  }
}

90079

쇼핑몰에 설치된 앱의 만료일이 연장된 경우

{
  "event\_no": 90079,
  "resource":{
    "mall\_id": "leesunsin",
    "client\_id": "sample7eBNEqSfkd7I8hoA",
    "app\_name": "sample\_app",
    "expire\_date": "2020-08-31T23:59:59+09:00",
    "previous\_expire\_date": "2020-07-31T23:59:59+09:00",
    "updated\_date": "2020-07-01T12:30:15+09:00"
  }
}

90157

쇼핑몰에 설치된 앱이 결제된 경우

{
  "event\_no": 90157,
  "resource":{
  "mall\_id": "leesunsin",
  "client\_id": "sample7eBNEqSfkd7I8hoA",
  "order\_id": "Tb1dbe01667974041111",
  "payed\_date": "2022-12-01 13:54:30",
  "currency": "KRW",
  "amount": "1000",
  "channel": "APP"
  }
}

90158

쇼핑몰에 설치된 앱의 결제 환불을 요청한 경우

{
  "event\_no": 90158,
  "resource":{
 "mall\_id": "leesunsin",
  "client\_id": "sample7eBNEqSfkd7I8hoA",
  "order\_id": "Tb1dbe01667974041111",
  "reason\_code": "A",
  "reason\_detail": "The app does not function properly.",
  "request\_date": "2022-12-13T16:09:58+09:00"
  }
}

90159

쇼핑몰에 설치된 앱의 결제 환불이 완료된 경우

{
  "event\_no": 90159,
  "resource":{
 "mall\_id": "leesunsin",
  "client\_id": "sample7eBNEqSfkd7I8hoA",
  "order\_id": "Tb1dbe01667974041111",
  "currency": "KRW",
  "refunded\_amount": "200.00",
  "expire\_date": "2023-01-21T23:59:59+09:00",
  "refunded\_date": "2022-12-13T16:09:58+09:00"  
    }
}
}

  

## 앱 이벤트 파라미터 정의

앱 이벤트 파라미터 정의   

Parameter

Description

Memo

event\_no

이벤트 구분(타입)

mall\_id

쇼핑몰 ID

client\_id

앱 ID

app\_name

앱 관리 상품명

deleted\_date

앱 삭제일시

expired\_date

앱 만료일시

previous\_expire\_date

앱 만료일 연장 이전의 기존 만료일시

updated\_date

앱 만료일 연장 일시

order\_id

주문번호

payed\_date

결제일시

currency

결제통화

amount

결제금액

channel

요청채널

App : 인앱결제  
Web : 유료결제

reason\_code

환불 사유 코드

A : App의 기능이 정상동작 하지 않음  
B : App으로 인해 쇼핑몰 성능이 저하됨  
C : 개인정보유출 등 법적이슈가 있음  
D : 안내된 기능을 모두 충족하지 못함  
E : 구매자의 사유로 판매자와 합의하였음  
Z : 기타사유

reason\_detail

상세사유

request\_date

요청일시

refunded\_amount

환불금액

refunded\_date

환불일시

## 쇼핑몰 이벤트별 샘플 데이터

### 쇼핑몰 > 상품

쇼핑몰 > 상품   

이벤트 NO.

이벤트

샘플 데이터

90001

쇼핑몰에 상품이 등록된 경우

{
  "event\_no": 90001,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "product\_no":36518,
    "product\_code":"P000CCAO",
    "created\_date":"2020-07-17T15:26:52+09:00",
    "updated\_date":"2020-07-17T15:26:52+09:00",
    "product\_name":"Sample Product Name",
    "eng\_product\_name":"",
    "supply\_product\_name":"Supply Sample Name",
    "model\_name":"Sample Product CAFE2468",
    "custom\_product\_code":"CAFE2468",
    "product\_condition":"N",
    "summary\_description":"Flower Skirt",
    "simple\_description":"Sweet Ballerina Flower Pleated Skirt.",
    "description":"desc.",
    "display":"F",
    "selling":"T",
    "retail\_price":"0.00",
    "supply\_price":"20000.00",
    "price":"24680.00",
    "price\_content":null,
    "adult\_certification":"F",
    "manufacturer\_code":"M0000000",
    "supplier\_code":"S0000000",
    "brand\_code":"B0000000",
    "trend\_code":"T0000000",
    "made\_date":"2020-07-10",
    "release\_date":"2020-07-10",
    "origin\_place\_code":126,
    "shipping\_scope":"B",
    "translated":"F"
 }
}

90002

쇼핑몰 상품이 수정된 경우

90041

쇼핑몰 상품이 일괄 수정된 경우

{
  "event\_no": 90041,
  "resource":{
    "mall\_id":"cafe24bestshop", 
    "event\_shop\_no":"1",
    "product\_no":"17652,17394,17293,16807,16118",
    "action":"batch"
  }
}

90003

쇼핑몰 상품이 삭제된 경우

{
  "event\_no": 90003,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"4",
    "product\_no":7178,
    "product\_code":"P0000KQC"
  }
}

90022

쇼핑몰에서 상품을 복구한 경우

{
  "event\_no": 90022,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "product\_no":131
  }
}

90075

품목의 재고가 품절되었거나, 품절이 해제된 경우  
  
(재고 1개 -> 재고 0개)  
  
또는  
  
(재고 0개 -> 재고 1개)

{
  "event\_no": 90075,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "product\_no":36518,
    "product\_code":"P000CCAO",
    "created\_date":"2020-07-17T15:26:52+09:00",
    "updated\_date":"2020-07-17T15:26:52+09:00",
    "product\_name":"Sample Product Name",
    "eng\_product\_name":"",
    "supply\_product\_name":"Supply Sample Name",
    "model\_name":"Sample Product CAFE2468",
    "custom\_product\_code":"CAFE2468",
    "product\_condition":"N",
    "summary\_description":"Flower Skirt",
    "simple\_description":"Sweet Ballerina Flower Pleated Skirt.",
    "description":"desc.",
    "display":"F",
    "selling":"T",
    "retail\_price":"0.00",
    "supply\_price":"27000.00",
    "price":"24680.00",
    "price\_content":null,
    "adult\_certification":"F",
    "manufacturer\_code":"M0000000",
    "supplier\_code":"S0000000",
    "brand\_code":"B0000000",
    "trend\_code":"T0000000",
    "made\_date":"2020-07-10",
    "release\_date":"2020-07-10",
    "origin\_place\_code":126,
    "shipping\_scope":"B",
    "translated":"F",
    "status\_text":"In case that item stock is less than or equal 0",
    "variant\_code":"P000CCAO000B",
    "use\_soldout":"T"
  }
}

90150

쇼핑몰에 등록된 상품의 품절상태가 변경된 경우

{
    "event\_no": 90150,
    "resource": {
        "mall\_id": "cafe24bestshop",
        "event\_shop\_no": "1",
        "sold\_out\_by\_current\_shop": "T",
        "product\_no": "1",
        "sold\_out": {
            "1": "T",
            "2": "F",
            "3": "F"
        }
    }
}

### 쇼핑몰 > 주문

쇼핑몰 > 주문   

이벤트 NO.

이벤트

샘플 데이터

90023

쇼핑몰에 주문이 접수된 경우

{
  "event\_no": 90023,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "event\_code":"create\_order",
    "order\_id":"20200717-0029236",
    "payment\_gateway\_name":"",
    "currency":"KRW",
    "order\_date":"2020-07-17T15:28:14+09:00",
    "order\_place\_name":"naver pay",
    "member\_id":"gdhong",
    "member\_authentication":null,
    "buyer\_name":"Jessica Hong",
    "buyer\_email":"gdhong@cafe24corp.com",
    "buyer\_phone":"02-0000-0000",
    "buyer\_cellphone":"010-2424-2424",
    "group\_no\_when\_ordering":"",
    "first\_order":null,
    "order\_from\_mobile":"F",
    "paid":"T",
    "payment\_date":"2020-07-17T15:24:07+09:00",
    "billing\_name":"Jessica Hong",
    "bank\_code":null,
    "payment\_method":"mileage",
    "easypay\_name":"",
    "use\_escrow":"F",
    "bank\_account\_no":"",
    "order\_price\_amount":"24680.00",
    "membership\_discount\_amount":"0.00",
    "actual\_payment\_amount":"0.00",
    "mileage\_spent\_amount":"0.00",
    "shipping\_fee":"0.00",
    "shipping\_type":"A",
    "shipping\_status":"F",
    "wished\_delivery\_date":"0000-00-00",
    "wished\_delivery\_time":null,
    "store\_pickup":"F",
    "shipping\_message":"",
    "subscription\_id": "S-20200914-0000024",
    "order\_place\_id":"NCHECKOUT",
    "ordering\_product\_code":"P00000BO,P00000DQ",
    "ordering\_product\_name":"Sample Product Name 1,Sample Product Name 2"
  }
}

90024

쇼핑몰에 접수된 주문의 배송상태가 변경된 경우

{
  "event\_no": 90024,
  "resource":{
  "mall\_id":"cafe24bestshop",
  "event\_shop\_no":"1",
  "event\_code":"pickup\_complete\_order",
  "order\_id":"20200717-0029236",
  "payment\_gateway\_name":"",
  "currency":"KRW",
  "order\_date":"2020-07-17T15:28:14+09:00",
  "order\_place\_name":"네이버 페이",
  "member\_id":"gdhong",
  "member\_authentication":null,
  "buyer\_name":"홍길동",
  "buyer\_email":"gdhong@cafe24corp.com",
  "buyer\_phone":"02-0000-0000",
  "buyer\_cellphone":"010-2424-2424",
  "group\_no\_when\_ordering":"",
  "first\_order":null,
  "order\_from\_mobile":"T",
  "paid":"T",
  "payment\_date":"2020-07-17T15:24:07+09:00",
  "billing\_name":"홍길동",
  "bank\_code":null,
  "payment\_method":"card",
  "easypay\_name":"",
  "use\_escrow":"F",
  "bank\_account\_no":"",
  "order\_price\_amount":"24680.00",
  "membership\_discount\_amount":"0.00",
  "actual\_payment\_amount":"4000.00",
  "mileage\_spent\_amount":"0.00",
  "cancel\_date":null,
  "shipping\_fee":"0.00",
  "shipping\_type":"A",
  "shipping\_status":"T",
  "wished\_delivery\_date":"0000-00-00",
  "wished\_delivery\_time":null,
  "return\_confirmed\_date":null,
  "store\_pickup":"F",
  "shipping\_message":"",
  "order\_place\_id":"NCHECKOUT",
  "ordering\_product\_code":"P00000BO,P00000DQ",
  "ordering\_product\_name":"카페24 샘플 상품1,카페24 샘플 상품2",
  "included\_deferpay\_order":"F",
  "deferpay\_order\_id":"",
  "withdraw":"T",
  "withdraw\_type":"C"
  }
}

90071

쇼핑몰에 접수된 주문의 배송상태가 변경된 경우 (일괄)

{
  "event\_no": 90071,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "event\_code":"pickup\_complete\_order",
"order\_id":"20200717-0001242,20200717-0001251,20200717-0001261,20200717-0001270,20200717-0001287",
    "included\_deferpay\_order":"",
    "deferpay\_order\_id":""
  }
}

90025

쇼핑몰에 접수된 주문의 입금상태가 변경된 경우

{
  "event\_no": 90025,
  "resource": {
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "event\_code":"paid\_order",
    "order\_id":"20200717-0029236",
    "payment\_gateway\_name":"",
    "currency":"KRW",
    "order\_date":"2020-07-17T15:30:14+09:00",
    "order\_place\_name":"모바일웹",
    "member\_id":"gdhong",
    "member\_authentication":null,
    "buyer\_name":"홍길동",
    "buyer\_email":"gdhong@cafe24corp.com",
    "buyer\_phone":"02-0000-0000",
    "buyer\_cellphone":"010-2424-2424",
    "group\_no\_when\_ordering":"",
    "first\_order":"F",
    "order\_from\_mobile":"T",
    "paid":"T",
    "payment\_date":"2020-07-17T15:24:07+09:00",
    "billing\_name":"홍길동",
    "bank\_code":"bank\_20",
    "payment\_method":"cash",
    "easypay\_name":"",
    "use\_escrow":"F",
    "bank\_account\_no":"382-222254-13-001",
    "order\_price\_amount":"24680.00",
    "membership\_discount\_amount":"0.00",
    "actual\_payment\_amount":"27580",
    "mileage\_spent\_amount":"100.00",
    "shipping\_fee":"3000.00",
    "shipping\_type":"A",
    "shipping\_status":"F",
    "wished\_delivery\_date":"",
    "wished\_delivery\_time":null,
    "store\_pickup":"F",
    "shipping\_message":"빠른 배송 부탁드립니다.",
    "ordering\_product\_code":"P00000HK",
    "ordering\_product\_name":"카페24 샘플 상품1",
    "withdraw":"T",
    "withdraw\_type":"E"
  }
}

90026

쇼핑몰에 접수된 주문의 취소상태가 변경된 경우

{
  "event\_no": 90026,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "event\_code":"cancel\_order",
    "order\_id":"20200716-0000023",
    "payment\_gateway\_name":"inicis",
    "currency":"KRW",
    "order\_date":"2020-07-16T02:20:20+09:00",
    "order\_place\_name":"naver pay",
    "member\_id":"gdhong",
    "member\_authentication":null,
    "buyer\_name":"Jessica Hong",
    "buyer\_email":"gdhong@cafe24corp.com",
    "buyer\_phone":"02-0000-0000",
    "buyer\_cellphone":"010-2424-2424",
    "group\_no\_when\_ordering":"1",
    "first\_order":"T",
    "order\_from\_mobile":"T",
    "paid":"T",
    "payment\_date":"2020-07-17T15:24:07+09:00",
    "billing\_name":"Jessica Hong",
    "bank\_code":"",
    "payment\_method":"card",
    "easypay\_name":"",
    "use\_escrow":"F",
    "bank\_account\_no":"382-222254-13-001",
    "order\_price\_amount":"24680.00",
    "membership\_discount\_amount":"0.00",
    "actual\_payment\_amount":"24580",
    "mileage\_spent\_amount":"100.00",
    "cancel\_date":null,
    "shipping\_fee":"0.00",
    "shipping\_type":"A",
    "shipping\_status":"F",
    "wished\_delivery\_date":"",
    "wished\_delivery\_time":null,
    "store\_pickup":"F",
    "shipping\_message":"Quick Delivery please.",
    "order\_place\_id":"mobile",
    "ordering\_product\_code":"P00000HK",
    "ordering\_product\_name":"Sample Product Name 1"
  }
}

90072

쇼핑몰에 접수된 주문의 취소상태가 변경된 경우 (일괄)

{
  "event\_no": 90072,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "event\_code":"cancel\_order",
    "order\_id":"20200713-0000039,20200708-0000080"
  }
}

90027

쇼핑몰에 접수된 주문의 반품상태가 변경된 경우

{
    "event\_no": 90027,
    "resource": {
      "mall\_id":"cafe24bestshop",
      "event\_shop\_no":"1",
      "event\_code":"return\_order",
      "order\_id":"20200716-0000023",
      "payment\_gateway\_name":"inicis",
      "currency":"KRW",
      "order\_date":"2020-07-16T02:20:20+09:00",
      "order\_place\_name":"모바일웹",
      "member\_id":"gdhong",
      "member\_authentication":null,
      "buyer\_name":"홍길동",
      "buyer\_email":"gdhong@cafe24corp.com",
      "buyer\_phone":"02-0000-0000",
      "buyer\_cellphone":"010-2424-2424",
      "group\_no\_when\_ordering":"1",
      "first\_order":"T",
      "order\_from\_mobile":"T",
      "paid":"T",
      "payment\_date":"2020-07-17T15:24:07+09:00",
      "billing\_name":"홍길동",
      "bank\_code":"",
      "payment\_method":"card",
      "easypay\_name":"",
      "use\_escrow":"F",
      "bank\_account\_no":"382-222254-13-001",
      "order\_price\_amount":"24680.00",
      "membership\_discount\_amount":"0.00",
      "actual\_payment\_amount":"24580",
      "mileage\_spent\_amount":"100.00",
      "cancel\_date":null,
      "shipping\_fee":"0.00",
      "shipping\_type":"A",
      "shipping\_status":"F",
      "wished\_delivery\_date":"",
      "wished\_delivery\_time":null,
      "store\_pickup":"F",
      "shipping\_message":"빠른 배송 부탁드립니다.",
      "order\_place\_id":"mobile",
      "ordering\_product\_code":"P00000HK",
      "ordering\_product\_name":"카페24 샘플 상품1",
      "claim\_reason\_type": "P",
      "claim\_reason": "not satisfied",
      "claim\_reason\_type\_text": "상품 불만족"
    }
}

90074

쇼핑몰에 접수된 주문의 반품상태가 변경된 경우 (일괄)

{
  "event\_no": 90074,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "event\_code":"return\_order",
    "order\_id":"20200528-0000019,20200513-0000040"
  }
}

90028

쇼핑몰에 접수된 주문의 교환상태가 변경된 경우

{
  "event\_no": 90028,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "event\_code":"exchange\_order",
    "order\_id":"20200716-0000023",
    "payment\_gateway\_name":"inicis",
    "currency":"KRW",
    "order\_date":"2020-07-16T02:20:20+09:00",
    "order\_place\_name":"naver pay",
    "member\_id":"gdhong",
    "member\_authentication":null,
    "buyer\_name":"Jessica Hong",
    "buyer\_email":"gdhong@cafe24corp.com",
    "buyer\_phone":"02-0000-0000",
    "buyer\_cellphone":"010-2424-2424",
    "group\_no\_when\_ordering":"1",
    "first\_order":"T",
    "order\_from\_mobile":"T",
    "paid":"T",
    "payment\_date":"2020-07-17T15:24:07+09:00",
    "billing\_name":"Jessica Hong",
    "bank\_code":"",
    "payment\_method":"card",
    "easypay\_name":"",
    "use\_escrow":"F",
    "bank\_account\_no":"382-222254-13-001",
    "order\_price\_amount":"24680.00",
    "membership\_discount\_amount":"0.00",
    "actual\_payment\_amount":"24580",
    "mileage\_spent\_amount":"100.00",
    "cancel\_date":null,
    "shipping\_fee":"0.00",
    "shipping\_type":"A",
    "shipping\_status":"F",
    "wished\_delivery\_date":"",
    "wished\_delivery\_time":null,
    "store\_pickup":"F",
    "shipping\_message":"Quick Delivery please.",
    "order\_place\_id":"mobile",
    "ordering\_product\_code":"P00000HK",
    "ordering\_product\_name":"Sample Product Name1"
  }
}

90029

쇼핑몰에 접수된 주문의 환불상태가 변경된 경우

{
  "event\_no": 90029,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "event\_code":"refund\_order",
    "order\_id":"20200716-0000023",
    "payment\_gateway\_name":"dacom",
    "currency":"KRW",
    "order\_date":"2020-07-16T02:20:20+09:00",
    "order\_place\_name":"naver pay",
    "member\_id":"gdhong",
    "member\_authentication":null,
    "buyer\_name":"Jessica Hong",
    "buyer\_email":"gdhong@cafe24corp.com",
    "buyer\_phone":"02-0000-0000",
    "buyer\_cellphone":"010-2424-2424",
    "group\_no\_when\_ordering":"1",
    "first\_order":"F",
    "order\_from\_mobile":"T",
    "paid":"T",
    "payment\_date":"2020-07-17T15:24:07+09:00",
    "billing\_name":"Jessica Hong",
    "bank\_code":"",
    "payment\_method":"card",
    "easypay\_name":"",
    "use\_escrow":"F",
    "bank\_account\_no":"382-222254-13-001",
    "order\_price\_amount":"24680.00",
    "membership\_discount\_amount":"0.00",
    "actual\_payment\_amount":"24580",
    "mileage\_spent\_amount":"100.00",
    "cancel\_date":null,
    "shipping\_fee":"0.00",
    "shipping\_type":"A",
    "shipping\_status":"T",
    "wished\_delivery\_date":"",
    "wished\_delivery\_time":null,
    "return\_confirmed\_date":null,
    "store\_pickup":"F",
    "shipping\_message":"Quick Delivery please.",
    "order\_place\_id":"mobile",
    "ordering\_product\_code":"P00000HK",
    "ordering\_product\_name":"Sample Product Name1"
  }
}

90073

쇼핑몰에 접수된 주문의 환불상태가 변경된 경우 (일괄)

{
  "event\_no": 90073,
  "resource":{ 
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "event\_code":"refund\_order",
    "order\_id":"20200529-0000015,20200527-0000078"
  }
}

90031

쇼핑몰에 접수된 주문에 상품을 추가한 경우

{
  "event\_no": 90031,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "order\_id":"20191009-0000126",
    "payment\_gateway\_name":"",
    "currency":"KRW",
    "order\_date":"2019-10-09T15:52:56+09:00",
    "order\_place\_name":"naver pay",
    "member\_id":"gdhong",
    "member\_authentication":"B",
    "buyer\_name":"Jessica Hong",
    "buyer\_email":"gdhong@cafe24corp.com",
    "buyer\_phone":"02-0000-0000",
    "buyer\_cellphone":"010-2424-2424",
    "group\_no\_when\_ordering":"13",
    "first\_order":"F",
    "order\_from\_mobile":"F",
    "paid":"M",
    "payment\_date":"2019-10-09T15:53:08+09:00",
    "billing\_name":"Jessica Hong",
    "bank\_code":"bank\_82",
    "payment\_method":"cash",
    "easypay\_name":"",
    "use\_escrow":"F",
    "bank\_account\_no":"382-222254-13-001",
    "order\_price\_amount":"24680.00",
    "membership\_discount\_amount":"0.00",
    "actual\_payment\_amount":"24580",
    "mileage\_spent\_amount":"100.00",
    "cancel\_date":null,
    "shipping\_fee":"0.00",
    "shipping\_type":"A",
    "shipping\_status":"F",
    "wished\_delivery\_date":"Quick delivery please.",
    "wished\_delivery\_time":"ASAP",
    "shipping\_message":"",
    "order\_place\_id":"self",
    "ordering\_product\_code":"P0000BUC,P0000BUB",
    "ordering\_product\_name":"Sample Product Name 1,Sample Product Name 2"
}

90064

쇼핑몰에 접수된 주문의 수령자정보가 변경된 경우

{
  "event\_no": 90064,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "event\_code":"changing\_recipient\_information",
    "order\_id":"20200717-0024054",
    "order\_place\_id":"self"
  }
}

90066

쇼핑몰에 접수된 주문에 관리자메모가 등록된 경우

{
    "event\_no": 90066,
    "resource": {
       "mall\_id":"cafe24bestshop",
       "event\_shop\_no":"1",
       "event\_code":"insert\_admin\_memo",
       "order\_id":"20200717-0000092",
       "requested\_date":"2020-07-17 15:38:22",
       "order\_place\_id":"shopn",
       "ordering\_product\_code":"P00000TW",
       "ordering\_product\_name":"카페24 샘플 상품1",
       "executor\_id":"sample7eBNEqSfkd7I8hoA",
       "execute\_method":"V2X"
    }
}

90068

쇼핑몰에 접수된 주문에 관리자메모가 수정된 경우

{
    "event\_no": 90068,
    "resource": {
       "mall\_id":"cafe24bestshop",
       "event\_shop\_no":"1",
       "event\_code":"modify\_admin\_memo",
       "order\_id":"20200114-0002249",
       "requested\_date":"2020-01-22 10:21:51",
       "order\_place\_id":"mobile",
       "executor\_id":"sample7eBNEqSfkd7I8hoA",
       "execute\_method":"V2X"
    }
}

90069

쇼핑몰에 접수된 주문에 관리자메모가 삭제된 경우

{
    "event\_no": 90069,
    "resource": {
       "mall\_id":"cafe24bestshop",
       "event\_shop\_no":"1",
       "event\_code":"delete\_admin\_memo",
       "order\_id":"20190715-0000014",
       "requested\_date":"2019-07-15 08:53:46",
       "order\_place\_id":"self",
       "executor\_id":"sample7eBNEqSfkd7I8hoA",
       "execute\_method":"V2X"
    }
}

90070

쇼핑몰에서 주문서가 삭제된 경우

{
  "event\_no": 90070,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "event\_code":"old\_order\_delete",
    "order\_id":"20200228-0000016"
  }
}

90084

쇼핑몰 상품이 장바구니에 담긴 경우

{
  "event\_no": 90084,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "member\_id": "sampleid",
    "shipping\_type": "A",
    "product\_no": 781,
    "variant\_code": "P0000BEB000A",
    "quantity": 1,
    "product\_bundle": "F"
  }
}

90162

쇼핑몰에 접수된 주문의 송장번호가 변경된 경우

{ 
"event\_no": 90162,
"resource":{
 "mall\_id": "cafe24bestshop",
 "event\_shop\_no": "1",
 "event\_code":"update\_invoice\_no",
 "order\_id": "20200717-0029236",
 "shipping\_code": "D-20220723-0000019-00",
 "shipping\_company\_code": "0001",
 "tracking\_no": "123456789123"
  }
}

90193

쇼핑몰에 접수된 주문의 발송예정일이 등록된 경우 (품주별)

{
  "event\_no": 90193,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "order\_id": "20251115-0000123",
    "order\_item\_code": "20251115-0000123-01",
    "shipping\_expected\_date": "2026-04-20",
    "requested\_date": "2026-05-18T14:32:10+09:00"
  }
}

90194

쇼핑몰에 접수된 주문의 발송예정일이 수정된 경우 (품주별)

{
  "event\_no": 90194,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "order\_id": "20251115-0000123",
    "order\_item\_code": "20251115-0000123-01",
    "shipping\_expected\_date": "2026-05-10",
    "requested\_date": "2026-05-18T14:32:10+09:00"
  }
}

90195

쇼핑몰에 접수된 주문의 발송예정일이 등록된 경우 (일괄)

{
  "event\_no": 90195,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "items": \[
      {
        "order\_id": "20260521-0000013",
        "order\_item\_code": "20260521-0000013-01",
        "shipping\_expected\_date": "2026-05-28"
      },
      {
        "order\_id": "20260521-0000026",
        "order\_item\_code": "20260521-0000026-01",
        "shipping\_expected\_date": "2026-05-28"
      }
    \],
    "requested\_date": "2026-05-21T14:32:10+09:00"
  }
}

90196

쇼핑몰에 접수된 주문의 발송예정일이 수정된 경우 (일괄)

{
  "event\_no": 90196,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "items": \[
      {
        "order\_id": "20260521-0000013",
        "order\_item\_code": "20260521-0000013-01",
        "shipping\_expected\_date": "2026-06-15"
      },
      {
        "order\_id": "20260521-0000026",
        "order\_item\_code": "20260521-0000026-01",
        "shipping\_expected\_date": "2026-06-15"
      }
    \],
    "requested\_date": "2026-05-21T14:32:10+09:00"
  }
}

90197

쇼핑몰에 접수된 주문의 주문라벨이 등록된 경우 (품주별)

{
  "event\_no": 90197,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "order\_id": "20260610-0000021",
    "order\_item\_code": "20260610-0000021-01",
    "label\_no": 9,
    "label\_name": "label sample name",
    "operator": "cafe24bestshop",
    "requested\_date": "2026-05-21T14:32:10+09:00"
  }
}

90198

쇼핑몰에 접수된 주문의 주문라벨이 삭제된 경우 (품주별)

{
  "event\_no": 90198,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "order\_id": "20260610-0000021",
    "order\_item\_code": "20260610-0000021-01",
    "label\_no": 8,
    "label\_name": "label sample name",
    "operator": "cafe24bestshop",
    "requested\_date": "2026-05-21T14:32:10+09:00"
  }
}

90199

쇼핑몰에 접수된 주문의 주문라벨이 등록된 경우 (일괄)

{
  "event\_no": 90199,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "items": \[
      {
        "order\_id": "20260610-0000021",
        "order\_item\_code": "20260610-0000021-01",
        "label\_no": 10,
        "label\_name": "label sample name"
      },
      {
        "order\_id": "20260610-0000021",
        "order\_item\_code": "20260610-0000021-02",
        "label\_no": 10,
        "label\_name": "label sample name"
      }
    \],
    "operator": "cafe24bestshop",
    "requested\_date": "2026-05-21T14:32:10+09:00"
  }
}

90200

쇼핑몰에 접수된 주문의 주문라벨이 삭제된 경우 (일괄)

{
  "event\_no": 90200,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "items": \[
      {
        "order\_id": "20260610-0000021",
        "order\_item\_code": "20260610-0000021-01",
        "label\_no": 8,
        "label\_name": "label sample name"
      },
      {
        "order\_id": "20260610-0000021",
        "order\_item\_code": "20260610-0000021-02",
        "label\_no": 8,
        "label\_name": "label sample name"
      }
    \],
    "operator": "cafe24bestshop",
    "requested\_date": "2026-05-21T14:32:10+09:00"
  }
}

90160

쇼핑몰에 접수된 주문의 반품이 완료된 경우 (취소번호별)

{
    "event\_no": 90160,
    "resource": {
        "mall\_id": "sampleMall",
        "event\_shop\_no": "1",
        "order\_id": "20230316-0000287",
        "claim\_code": "C20230329-0001215",
        "claim\_reason\_type": "",
        "claim\_reason\_type\_text": "",
        "claim\_reason": "",
        "order\_price\_amount": "38000.00",
        "refund\_amount": "35000.00",
        "shipping\_fee": "0.00",
        "refund\_shipping\_fee": "0.00",
        "refund\_regional\_surcharge": "0.00",
        "return\_shipping\_fee": "0.00",
        "return\_regional\_surcharge": "0.00",
        "add\_discount\_amount": "0.00",
        "member\_grade\_discount\_amount": "0.00",
        "shipping\_discount\_amount": "0.00",
        "coupon\_discount\_amount": "-3000.00",
        "point\_used": "0.00",
        "credit\_used": "0.00"
    }
}

### 쇼핑몰 > 회원

쇼핑몰 > 회원   

이벤트 NO.

이벤트

샘플 데이터

90032

쇼핑몰에 신규 회원이 가입한 경우

{
  "event\_no": 90032,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "member\_id":"gdhong",
    "group\_no":1,
    "name":"Jake Park",
    "nick\_name":"vjakiev",
    "name\_english":"",
    "name\_phonetic":"",
    "created\_date":"2020-07-17T15:26:00+09:00",
    "member\_authentication":"T",
    "birthday":"",
    "gender":"",
    "phone":"02-0000-0000",
    "cellphone":"010-2468-2468",
    "sms":"T",
    "email":"gdhong@cafe24corp.com",
    "news\_mail":"T",
    "total\_mileage":"0.00",
    "available\_mileage":"0.00",
    "recommend\_id":"bestmember",
    "residence":"",
    "use\_mobile\_app":"T",
    "member\_type":"p"
  }
}

90063

쇼핑몰 회원이 SNS 계정을 연동한 경우

{
  "event\_no": 90063,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "member\_id":"member",
    "social\_name": "kakao",
    "social\_member\_code": 123456,
  }
}

90080

쇼핑몰 회원정보가 변경된 경우

{
  "event\_no": 90080,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "member\_id": "gdhong",
    "diff\_key": \[
      "name",
      "phone",
      "cellphone",
      "gender",
      "birthday"
    \],
    "sub\_event\_code": "EC\_FRONT"
  }
}

90143

쇼핑몰 회원이 로그인한 경우

{
  "event\_no": 90143,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "member\_id": "sampleid",
    "group\_name": "Standard Membership",
    "inflow\_name": "PC"
  }
}

90144

쇼핑몰 회원 등급이 변경된 경우

{
  "event\_no": 90144,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "member\_id": "sampleid",
    "after\_member\_group\_name": "Standard Membership"
  }
}

90145

쇼핑몰에 회원이 휴면회원으로 변경된 경우

{
  "event\_no": 90145,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "member\_id": "sampleid1, sampleid2, sampleid3"
  }
}

90146

쇼핑몰에 회원이 휴면회원 해제된 경우

{
  "event\_no": 90146,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "member\_id": "sampleid1, sampleid2, sampleid3"
  }
}

90147

쇼핑몰에 회원이 탈퇴한 경우

{
  "event\_no": 90147,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "member\_id": "sampleid1, sampleid2, sampleid3"
  }

90148

쇼핑몰 회원의 적립금이 변동된 경우

{
    "event\_no": 90148,
    "resource": {
        "mall\_id": "cafe24bestshop",
        "shop\_no": "1",
        "member\_id": "sampleid1",
        "mileage\_money": 100,
        "avail\_mileage": 1000,
        "issue\_datetime": "2022-01-25 16:54:45",
        "case": "B",
        "case\_text": "주문취소로 인한 환불시 환불금을 적립금으로 부여",
        "reason": null
    }
}

### 쇼핑몰 > 게시판

쇼핑몰 > 게시판   

이벤트 NO.

이벤트

샘플 데이터

90033

쇼핑몰에 게시물이 등록된 경우

{
  "event\_no": 90033,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "board\_no":9,
    "no":274,
    "has\_parent":"T",
    "member\_id":"bestmember",
    "writer":"bestmember"
  }
}

90034

쇼핑몰 게시물에 댓글이 등록된 경우

{
  "event\_no": 90034,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "board\_no":8,
    "member\_id":"cafe24bestshop",
    "writer":"Jake Park",
    "comment\_member\_id":"33578422@n",
    "comment\_writer":"Jenny",
    "article\_no":17,
    "comment\_no":5
  }
}

90035

쇼핑몰에 긴급문의가 접수된 경우

{
  "event\_no": 90035,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "member\_id":null,
    "writer":"bestmember"
  }
}

90036

쇼핑몰의 게시물이 삭제된 경우

{
  "event\_no": 90036,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "board\_no":4,
    "no":81,
    "member\_id":"bestmember",
    "writer":"bestmember"
  }
}

90037

쇼핑몰 게시물의 댓글이 삭제된 경우

{
  "event\_no": 90037,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "board\_no":6,
    "member\_id":"gdhong",
    "writer":"Jake Park",
    "comment\_member\_id":"gdhong",
    "comment\_writer":"Jenny",
    "article\_no":17,
    "comment\_no":5
  }
}

90038

쇼핑몰에 접수된 긴급문의가 삭제된 경우

{
  "event\_no": 90038,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "member\_id":"gdhong",
    "writer":"Jake Park"
  }
}

90039

쇼핑몰의 게시물이 수정된 경우

{
  "event\_no": 90039,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "board\_no":1,
    "no":82,
    "has\_parent":"F",
    "member\_id":"gdhong",
    "writer":"Jake Park"
  }
}

### 쇼핑몰 > 상품분류

쇼핑몰 > 상품분류   

이벤트 NO.

이벤트

샘플 데이터

90042

쇼핑몰에 상품분류가 추가된 경우

{
  "event\_no": 90042,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "category\_no":96,
    "category\_name":"Private Order",
    "use\_display":"F",
    "use\_main":"F",
    "display\_type":"A",
    "product\_display\_scope":"A",
    "product\_display\_type":"A",
    "product\_display\_key":"R",
    "product\_display\_sort":"D",
    "soldout\_product\_display":"N",
    "sub\_category\_product\_display":"F"
  }
}

90043

쇼핑몰의 상품분류가 수정된 경우

{
  "event\_no": 90043,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "category\_no":24,
    "category\_name":"(Category) Outerwear",
    "use\_display":"T",
    "use\_main":"T",
    "display\_type":"A",
    "product\_display\_scope":"A",
    "product\_display\_type":"A",
    "product\_display\_key":"R",
    "product\_display\_sort":"D",
    "soldout\_product\_display":"N",
    "sub\_category\_product\_display":"T"
  }
}

90046

쇼핑몰에서 상품분류의 상품 진열 설정을 일괄변경한 경우

{
  "event\_no": 90046,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "product\_display\_scope":"A",
    "product\_display\_type":"A",
    "product\_display\_key":"U",
    "product\_display\_sort":"A"
  }
}

90044

쇼핑몰에서 상품분류가 삭제된 경우

{
  "event\_no": 90044,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1",
    "category\_no":91
  }
}

90045

쇼핑몰 상품분류의 순서가 변경된 경우

{
  "event\_no": 90045,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1"
  }
}

### 쇼핑몰 > 공급사

쇼핑몰 > 공급사   

이벤트 NO.

이벤트

샘플 데이터

90090

쇼핑몰에 공급사가 등록된 경우

{
 "event\_no": 90090,
  "resource":{
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "supplier\_code": "S0000000",
    "supplier\_name": "Default Supplier",
    "use\_supplier": "T",
    "trading\_type": "D",
    "supplier\_type": "WS",
    "status": "A",
    "payment\_type": "D",
    "commission": "0.00",
    "payment\_period": "A"
  }
}

90091

쇼핑몰에 등록된 공급사가 수정된 경우

{
  "event\_no": 90091,
  "resource":{
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "supplier\_code": "S0000000",
    "supplier\_name": "Default Supplier",
    "use\_supplier": "T",
    "trading\_type": "D",
    "supplier\_type": "WS",
    "status": "A",
    "payment\_type": "D",
    "commission": "0.00",
    "payment\_period": "A"
  }
}

90092

쇼핑몰에 등록된 공급사가 일괄 수정된 경우

{
 "event\_no": 90092,
  "resource":{
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "supplier\_code": "S0000000,S000000A,S000000B"
  }
}

90093

쇼핑몰에 등록된 공급사가 삭제된 경우

{
 "event\_no": 90093,
  "resource":{
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "supplier\_code": "S0000000"
  }
}

### 쇼핑몰 > 배송

쇼핑몰 > 배송   

이벤트 NO.

이벤트

샘플 데이터

90100

쇼핑몰에 배송업체가 등록된 경우

{
    "event\_no": 90100,
    "resource": {
        "mall\_id": "cafe24bestshop",
        "event\_shop\_no": "1",
        "sc\_id": "3",
        "sc\_name": "FASTBOX",
        "is\_basic": "T",
        "phone1": "1588-3413",
        "phone2": "1588-3413",
        "email": "gdhong@cafe24corp.com",
        "shipping\_money": "3000",
        "homepage": "www.fastbox.com",
        "trace\_url": "https://www.fastbox.com/ko/tool/parcel/tracking?gnbInvcNo=000000000000",
        "sender\_name": "cafe24bestshop",
        "sender\_phone": "010-2424-2424",
        "sender\_cellphone": "010-2424-2424",
        "weight": "15",
        "volume": "20",
        "shipping\_type": "01",
        "box\_type": "01",
        "sender\_zipcode": "07071",
        "sender\_address1": "15 Boramaero 5gil Dongjakgu",
        "sender\_address2": "Cafe24 22F",
        "executor\_id":"cafe24bestshop",
        "execute\_method":"ADMIN"
    }
}

90101

쇼핑몰에 등록된 배송업체가 수정된 경우

{
    "event\_no": 90101,
    "resource": {
        "mall\_id": "cafe24bestshop",
        "event\_shop\_no": "1",
        "sc\_id": "3",
        "sc\_name": "FASTBOX",
        "is\_basic": "T",
        "phone1": "1588-3413",
        "phone2": "1588-3413",
        "email": "gdhong@cafe24corp.com",
        "shipping\_money": "3000",
        "homepage": "www.fastbox.com",
        "trace\_url": "https://www.fastbox.com/ko/tool/parcel/tracking?gnbInvcNo=000000000000",
        "executor\_id":"cafe24bestshop",
        "execute\_method":"ADMIN"
    }
}

90102

쇼핑몰에 등록된 배송업체가 삭제된 경우

{
    "event\_no": 90102,
    "resource": {
        "mall\_id": "cafe24bestshop",
        "event\_shop\_no": "1",
        "sc\_id": "3",
        "executor\_id":"cafe24bestshop",
        "execute\_method":"ADMIN"
    }
}

### 쇼핑몰 > 상점

쇼핑몰 > 상점   

이벤트 NO.

이벤트

샘플 데이터

90110

쇼핑몰에 멀티쇼핑몰이 추가된 경우

{
 "event\_no": 90110,
  "resource":{
    "mall\_id": "cafe24bestshop",
    "shop\_no": "2",
    "shop\_name": "MultiShop",
    "language": "en\_US",
    "currency": "USD",
    "is\_active": "T"
  }
}

90111

쇼핑몰에 등록된 멀티쇼핑몰이 수정된 경우

{
"event\_no": 90111,
  "resource":{
    "mall\_id": "cafe24bestshop",
    "shop\_no": "2",
    "shop\_name": "MultiShop",
    "is\_active": "T"
  }
}

90112

쇼핑몰에 등록된 멀티쇼핑몰이 삭제된 경우

{
"event\_no": 90112,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "event\_shop\_no":"1"
  }
}

90113

쇼핑몰에 부운영자가 등록된 경우

{
"event\_no": 90113,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "sub\_admin\_id":"subadmin1",
    "sub\_admin\_type":"A",
    "user\_name":"John Doe",
    "available":"T"
  }
}

90114

쇼핑몰에 등록된 부운영자가 수정된 경우

{
"event\_no": 90114,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "sub\_admin\_id":"subadmin1",
    "sub\_admin\_type":"A",
    "user\_name":"John Doe",
    "available":"T",
    "multishop\_access\_authority":"{1: 'T'}, {2: 'F'}, {3: 'T'}, {4: 'F'}"
  }
}

90115

쇼핑몰에 등록된 부운영자가 삭제된 경우

{
"event\_no": 90115,
  "resource":{
    "mall\_id":"cafe24bestshop",
    "sub\_admin\_id":"subadmin1",
  }
}

90116

개인정보제공 설정이 변경된 경우

{
"event\_no": 90116,
  "resource":{
  "mall\_id": "cafe24bestshop",
  "event\_shop\_no": "1",
  "use\_information\_agreement": "T",
  "use\_consignment\_agreement": "T"
  }
}

90117

쇼핑몰 도메인이 추가된 경우

{
"event\_no": 90117,
  "resource":{
  "mall\_id": "cafe24bestshop",
  "domain": "cafe24bestshop.cafe24.com"
  }
}

90119

쇼핑몰 도메인이 삭제된 경우

{
"event\_no": 90119,
  "resource":{
  "mall\_id": "cafe24bestshop",
  "domain": "cafe24bestshop.cafe24.com"
  }
}

90121

내 쇼핑몰 정보 설정이 수정된 경우

{
"event\_no": 90121,
  "resource":{
  "mall\_id": "cafe24bestshop",
  "event\_shop\_no":"1",
  "shop\_name":"cafe24bestshop"
  "country":"ko\_KR"
  "zipcode":"07071"
  "address1":"15 Boramaero 5gil Dongjakgu"
  "address2":"Cafe24 22F"
  "president\_phone":"02-3284-0300"
  }
}

90166

쇼핑몰이 삭제처리된 경우

{
  "event\_no": 90166,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "trigger\_name": "쇼핑몰이 삭제 처리된 경우"
  }
}

90167

쇼핑몰이 휴면처리된 경우

{
  "event\_no": 90167,
  "resource": {
    "trigger\_name": "쇼핑몰이 휴면처리된 경우",
    "sample": {
    "event\_shop\_no": "1",
      "mall\_id": "cafe24bestshop"
    }
  }
}

90168

쇼핑몰이 휴면해제된 경우

{
  "event\_no": 90168,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "trigger\_name": "쇼핑몰이 휴면해제된 경우"
  }
}

90169

쇼핑몰이 차단된 경우

{
  "event\_no": 90169,
  "resource": {
    "mall\_id": "cafe24bestshop",
    "event\_shop\_no": "1",
    "trigger\_name": "쇼핑몰이 차단된 경우"
  }
}

### 쇼핑몰 > 운영설정

쇼핑몰 > 운영설정   

이벤트 NO.

이벤트

샘플 데이터

90142

카카오싱크 설정이 변경된 경우

{
    "event\_no": 90142,
    "resource": {
        "mall\_id": "cafe24bestshop",
        "event\_shop\_no": "1",
        "kakaosync\_used": "F",
        "client\_id": "81b6ceb301d48df7670859c8db411ef4"
    }
}

### 쇼핑몰 > 혜택

쇼핑몰 > 혜택   

이벤트 NO.

이벤트

샘플 데이터

90047

쇼핑몰에 혜택이 등록된 경우

{
     "event\_no": 90047,
     "resource": {
        "mall\_id": "cafe24bestshop",
        "shop\_no": 1,
        "benefit\_no": 3,
        "use\_benefit": "T",
        "benefit\_name": "SampleBenefit",
        "benefit\_start\_date": "2019-01-01T12: 00: 00+09: 00",
        "benefit\_end\_date": "2019-01-31T12: 00: 00+09: 00",
        "customer\_group\_list": \[
          8,
          9
        \],
        "product\_binding\_type": "P",
        "product\_list": \[
          17,
          25,
          29
        \],
        "add\_category\_list": null,
        "except\_category\_list": \[
          168,
          175,
          177
        \]
    }
}

90048

쇼핑몰에 등록된 혜택이 수정된 경우

{
     "event\_no": 90048,
     "resource": {
        "mall\_id": "cafe24bestshop",
        "shop\_no": 1,
        "benefit\_no": 3,
        "use\_benefit": "T",
        "benefit\_name": "SampleBenefit",
        "benefit\_start\_date": "2019-01-01T12: 00: 00+09: 00",
        "benefit\_end\_date": "2019-01-31T12: 00: 00+09: 00",
        "customer\_group\_list": \[
          8,
          9
        \],
        "product\_binding\_type": "P",
        "product\_list": \[
          17,
          25,
          29
        \],
        "add\_category\_list": null,
        "except\_category\_list": \[
          168,
          175,
          177
        \]
    }
}

90050

혜택이 삭제된 경우

{
    "event\_no": 90050,
    "resource": {
        "mall\_id": "cafe24bestshop",
        "shop\_no": 1,
        "benefit\_no": 3
    }
}

### 쇼핑몰 > 쿠폰

쇼핑몰 > 쿠폰   

이벤트 NO.

이벤트

샘플 데이터

90151

쇼핑몰에 등록된 쿠폰이 수정된 경우

{
    "event\_no": 90151,
    "resource": {
        "mall\_id": "cafe24bestshop",
        "event\_shop\_no": 1,
        "coupon\_type": "O",
        "coupon\_no": 6072120804600000001,
        "coupon\_name": "Discount Coupon",
        "issue\_status\_code": "ISSUING",
        "issue\_status": "발급중"
    }
}

90152

쇼핑몰에 등록된 쿠폰이 삭제된 경우

{
    "event\_no": 90152,
    "resource": {
        "mall\_id": "cafe24bestshop",
        "event\_shop\_no": 1,
        "coupon\_type": "O",
        "coupon\_no": 6072120804600000001
    }
}

90153

쇼핑몰에 쿠폰이 등록된 경우

{
    "event\_no": 90153,
    "resource": {
        "mall\_id": "cafe24bestshop",
        "event\_shop\_no": 1,
        "coupon\_type": "O",
        "coupon\_no": 6072120804600000001,
        "coupon\_name": "Discount Coupon",
        "issue\_status\_code": "ISSUING",
        "issue\_status": "발급중"
    }
}

90154

쇼핑몰 쿠폰의 발급 상태가 변경된 경우

{
    "event\_no": "90154",
    "resource": {
        "mall\_id": "cafe24bestshop",
        "event\_shop\_no": 1,
        "coupon\_no": 6072120804600000001,
        "coupon\_name": "Discount Coupon",
        "issue\_status\_code": "ISSUING",
        "issue\_status": "발급중",
        "mode": "restart",
        "type": "now",
        "start\_date": "2022-01-01 14:39",
        "end\_date": "2022-01-01 16:38"
    }
}

## 쇼핑몰 이벤트 파라미터 정의

쇼핑몰 이벤트 파라미터 정의   

Parameter

Description

Memo

event\_no

이벤트 구분(타입)

각 이벤트 NO. 참조

mall\_id

쇼핑몰 ID

event\_shop\_no

멀티쇼핑몰 번호  
멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호

product\_no

상품번호  
상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음

created\_date

상품의 생성된 일시

date

updated\_date

상품이 수정된 일시

date

product\_name

상품명

최대글자수 : \[250자\]

eng\_product\_name

영문 상품명  
상품의 영문 이름. 해외 배송 등에 사용 가능함

최대글자수 : \[250자\]

supply\_product\_name

공금사 상품명

최대글자수 : \[250자\]

model\_name

상품의 모델명

최대글자수 : \[100자\]

custom\_product\_code

자체상품 코드  
사용자가 상품에 부여 가능한 코드. 재고 관리 등의 이유로 자체적으로 상품을 관리하고 있는 경우 사용함

최대글자수 : \[40자\]

product\_condition

상품상태

N : 신상품  
B : 반품상품  
R : 재고상품  
U : 중고상품  
E : 전시상품  
F : 리퍼상품  
S : 스크래치 상품

summary\_description

상품 요약 설명

최대글자수 : \[255자\]

simple\_description

상품 간략 설명

description

상품 상세 설명

display

진열상태

T : 진열함  
F : 진열안함

selling

판매상태

T : 판매함  
F : 판매안함

retail\_price

상품 소비자가

최소: \[0\]~최대: \[2147483647\]

supply\_price

상품 공급가

최소: \[0\]~최대: \[2147483647\]

price

상품 판매가

최소: \[0\]~최대: \[2147483647\]

price\_content

판매가 대체문구

최대글자수 : \[20자\]

adult\_certification

성인인증이 필요한 상품인지 여부

T : 사용함  
F : 사용안함

manufacturer\_code

제조사 코드

형식 : \[A-Z0-9\]  
글자수 최소: \[8자\]~최대: \[8자\]

supplier\_code

공급사 코드

형식 : \[A-Z0-9\]  
글자수 최소: \[8자\]~최대: \[8자\]

brand\_code

브랜드 코드

형식 : \[A-Z0-9\]  
글자수 최소: \[8자\]~최대: \[8자\]

price\_content

판매가 대체문구

최대글자수 : \[20자\]

trend\_code

트렌드 코드

형식 : \[A-Z0-9\]  
글자수 최소: \[8자\]~최대: \[8자\]

made\_date

제조일자

date

release\_date

출시일자

date

origin\_place\_code

원산지

manufacturer\_code

제조사 코드

형식 : \[A-Z0-9\]  
글자수 최소: \[8자\]~최대: \[8자\]

translated

번역상태

T : 번역함  
F : 번역안함

status\_text

현재 처리상태 문구 설명

use\_soldout

품목 품절표시 사용 여부 ???

T : 사용함  
F : 사용안함

order\_id

주문번호

payment\_gateway\_name

결제 PG사 이름

currency

화폐단위

KRW : ￦ 원  
USD : $ 달러  
JPY : ¥ 엔

order\_date

주문일

date

order\_place\_name

주문경로 텍스트

member\_id

회원 아이디

member\_authentication

회원 인증 여부

T : 인증  
F : 미인증  
B : 특별관리회원  
J : 14세미만회원

buyer\_name

주문자명

buyer\_email

주문자 이메일

buyer\_phone

주문자 일반 전화

buyer\_cellphone

주문자 휴대 전화

group\_no\_when\_ordering

주문 시 회원등급

first\_order

최초 주문여부

T : 최초 주문  
F : 최초 주문 아님

order\_from\_mobile

주문이 모바일에서 이루어졌는지 여부

T : 모바일 주문  
F : 모바일 주문 아님

paid

결제 완료 여부

T : 결제  
F : 미결제  
M : 부분 결제

payment\_date

결제일

date

billing\_name

결제자명

bank\_code

은행코드

**[bank\_code](https://appservice-guide.s3.ap-northeast-2.amazonaws.com/resource/ko/bank_code.xlsx)**

payment\_method

결제수단 코드

cash : 무통장  
card : 신용카드  
cell : 휴대폰  
tcash : 계좌이체  
prepaid : 선불금  
credit : 예치금  
point : 적립금  
pointfy : 통합포인트  
cvs : 편의점  
cod : 후불  
coupon : 쿠폰  
market\_discount : 마켓할인  
etc : 기타

easypay\_name

간편결제 결제사 이름

use\_escrow

에스크로 사용여부

T : 에스크로 사용  
F : 에스크로 미사용

bank\_account\_no

해당 주문건에 대한 쇼핑몰의 계좌번호

order\_price\_amount

주문금액

membership\_discount\_amount

회원할인금액

actual\_payment\_amount

실결제금액

mileage\_spent\_amount

적립금 사용금액

shipping\_fee

배송비

shipping\_type

배송 유형

A : 국내  
B : 해외

shipping\_status

배송상태

F : 배송전  
M : 배송중  
T : 배송완료  
W : 배송보류

wished\_delivery\_date

희망배송일

wished\_delivery\_time

희망배송시간

store\_pickup

매장수령여부

T : 매장수령  
F : 매장수령 아님

shipping\_message

배송 메세지

order\_place\_id

주문경로

cafe24:카페24  
mobile:모바일웹  
mobile\_d:모바일앱  
NCHECKOUT:네이버페이  
inpark:인터파크  
auction:옥션  
sk11st:11번가  
gmarket:G마켓  
coupang:쿠팡  
shopn:스마트스토어

ordering\_product\_code

주문 상품

ordering\_product\_name

주문 상품명

cancel\_date

주문취소일

return\_confirmed\_date

반품승인일시

included\_deferpay\_order

후불결제 포함여부

deferpay\_order\_id

후불결제 주문번호

requested\_date

관리자메모 변경일

쇼핑몰에 접수된 주문에 관리자메모가 등록된 경우

name

주문자명

nick\_name

운영자 별명

최대글자수 : \[50자\]

name\_english

회원 영문이름

name\_phonetic

회원 이름 발음 표기(일본어)

created\_date

가입일

birthday

해당 회원의 생일

gender

성별

M : 남자  
F : 여자

phone

일반 전화

cellphone

휴대 전화

sms

SMS 수신여부

T : 수신  
F : 수신안함

email

이메일

news\_mail

뉴스메일 수신여부

T : 수신  
F : 수신안함

brand\_code

브랜드 코드

형식 : \[A-Z0-9\]  
글자수 최소: \[8자\]~최대: \[8자\]

total\_mileage

총 마일리지

available\_mileage

가용 마일리지

recommend\_id

추천인 ID

residence

지역코드

use\_mobile\_app

모바일앱 사용여부

T : 사용  
F : 사용안함

member\_type

회원타입

p : 개인  
c : 사업자  
f : 외국인

board\_no

게시판 번호

has\_parent

게시물 여부

쇼핑몰에 게시물이 등록된 경우  
T : 있음  
F : 없음

writer

작성자명

comment\_member\_id

댓글 작성자 ID

article\_no

게시물번호

comment\_no

댓글번호

comment\_writer

댓글 작성자명

retail\_price

상품 소비자가

최소: \[0\]~최대: \[2147483647\]

category\_no

상품분류의 고유한 일련 번호

category\_name

상품분류명

최대글자수 : \[50자\]

use\_display

상품분류 표시상태  
해당 상품분류가 쇼핑몰 메인에 표시되는지 여부

T : 표시함  
F : 표시안함

use\_main

메인분류 표시상태

T : 표시함  
F : 표시안함

display\_type

쇼핑몰 표시설정

A : PC + 모바일  
P : PC  
M : 모바일  
F : 모두 사용안함

product\_display\_scope

상품분류 진열영역 구분

A : 전체  
G : 영역별

product\_display\_type

상품분류 진열방법

A : 자동정렬  
U : 사용자 지정  
M : 자동정렬 + 사용자 지정

product\_display\_key

상품분류 진열방법 키

A : 최근 추가된 상품  
R : 최근 등록상품  
U : 최근 수정상품  
N : 상품명 가나다순  
P : 판매가 높은 상품  
S : 판매량 높은 상품  
C : 조회수가 높은 상품  
L : 좋아요수가 높은 상품

product\_display\_sort

상품분류 진열방법 순서

D: 내림차순  
A : 오름차순

soldout\_product\_display

품절상품진열

B : 품절상품 맨 뒤로  
N : 품절상품 상관없음

sub\_category\_product\_display

하위분류 상품진열  
현재 상품 분류 하위 분류에 진열된 상품들까지 포함하여 진열할 것인지 여부

T : 진열함  
F : 진열안함

sub\_event\_code

회원정보 변경위치

EC\_FRONT : 프론트 회원정보수정에서 수정  
EC\_ADMIN : 몰 어드민에서 관리자가 수정

supplier\_name

공급사명

use\_supplier

공급사 사용여부

T: 사용함  
F: 사용안함

trading\_type

공급사 유형

D: 사입  
C: 직배송

supplier\_type

공급사 구조

WS: 도매업체  
SF: 사입업체  
BS: 입점업체  
ET: 기타

status

거래상태

A: 거래중  
P: 거래중지  
N: 거래해지

payment\_type

정산유형

P : 수수료형  
D : 매입형

commission

수수료율

payment\_period

정산주기

0: 선택안함  
C: 일일정산  
B: 주간정산  
A: 월간정산

sc\_id

배송업체 ID

sc\_name

배송업체명

is\_basic

기본배송사여부

T : 사용함  
F : 사용안함

phone1

대표 연락처

phone2

보조 연락처

shipping\_money

기본 배송비

trace\_url

배송 추적 URL

sender\_name

보내는 사람 이름

sender\_phone

보내는 사람 대표전화

sender\_cellphone

보내는 사람 휴대전화

weight

배송상품 무게

volume

배송상품 부피

shipping\_type

배송비 타입

01 : 선불  
02 : 착불  
03 : 신용

box\_type

박스 타입

01 : 극소  
02 : 소  
03 : 중  
04 : 대  
05 : 특대

sender\_zipcode

보내는사람 주소(우편번호)

sender\_address1

보내는사람 주소(기본주소)

sender\_address2

보내는사람 주소(상세주소)

sShopName

쇼핑몰명

sLanguage

언어코드

ko\_KR : 국문  
en\_US : 영문  
zh\_CN : 중문(간체)  
zh\_TW : 중문(번체)  
ja\_JP : 일문  
vi\_VN : 베트남어  
en\_PH : 영문

sCurrency

결제화폐

KRW / USD / JPY / CNY / TWD / EUR / BRL / VND / PHP

sIsActive

멀티쇼핑몰 활성화 여부

T : 활성화  
F : 비활성화

sub\_admin\_id

부운영자ID

sub\_admin\_type

부운영자 타입

A : 쇼핑몰운영자  
S : 공급사운영자

user\_name

부운영자명

기본몰에 설정된 부운영자명/공급사 운영자명만 제공

multishop\_access\_authority

멀티쇼핑몰 접근권한

T : 허용함  
F : 허용안함

use\_information\_agreement

개인정보 제3자 제공동의 사용여부

T : 사용함  
F : 사용안함

use\_consignment\_agreement

개인정보 위탁동의 사용여부

T : 사용함  
F : 사용안함

domain

도메인 주소

is\_under14\_joinable

14세미만 가입제한 설정상태

T : 인증 후 이용  
F : 가입불가

kakaosync\_used

카카오싱크 설정상태

T : 사용함  
F : 사용안함

group\_name

회원등급명

inflow\_name

유입경로

PC : PC로 접속 / Mobile : 모바일로 접속 mobile Web

country

사업장 국가  
사업장이 있는 국가명

zipcode

사업장 우편번호

address1

사업장 기본주소  
사업장의 주소 (시/군/도)

address2

사업장 상세주소

president\_phone

대표전화

Whether the product is bundle product

세트상품 여부

T : 세트상품, F : 세트상품 아님

Whether increased or decreased

적립금 증차감 여부

Increased(증가) / Decreased(차감)

Points amount

적립금 금액

Points balance

적립금 잔액

Updated Date

적립일

Shopping Mall Number

멀티쇼핑몰 번호

Updated Datetime

적립일시

sold\_out\_by\_current\_shop

상품 품절 여부

T : 품절, F : 품절 아님

sold\_out

전체 쇼핑몰의 상품 품절 여부

“1”:“T”,“2”:“F”

shop\_no

멀티쇼핑몰 번호

coupon\_type

쿠폰타입

O : 온라인 쿠폰 / S : 오프라인 시리얼 쿠폰

coupon\_no

쿠폰번호

ccoupon\_name

쿠폰명

issue\_status\_code

쿠폰 발급 상태 코드

issue\_status

쿠폰 발급 상태

발급중

mode

발급 상태 변경 유형

pause : 발급 중지 / restart : 발급 재개

type

발급 상태 변경 유형 상세

발급 중지 유형) later : 발급 중지 기간 설정 / now : 즉시 발급 중지  
발급 재개 유형) later : 발급 중지 해제일 변경 / now : 즉시 발급 재개

start\_date

시작일시

end\_date

해제일시

즉시 발급 중지일 경우 빈 값으로 나타납니다.

claim\_reason\_type\_text

반품 사유

고객변심, 상품 불만족, 상품불량, 배송 오류

withdraw

클레임 철회 여부

T: 철회된 주문 / F: 일반 주문

withdraw\_type

클레임 철회 종류

클레임이 철회된 주문만 해당 값이 반환됩니다.  
C: 입금전 취소 철회 / E: 입금전 교환 철회

case\_text

적립금 타입

관리자 직접 적림금 부여, 주문취소로 인한 환불시 환불금을 적립금으로 부여 등

case

적립금 타입 코드

A, B, C 등

reason

적립 사유

API를 활용하여 적립금 증차감 시 입력한 사유가 출력됩니다.

executor\_id

처리자 ID

execute\_method

처리자 구분

use\_benefit

혜택 진행여부

benefit\_name

혜택이름

benefit\_start\_date

혜택 시작일

benefit\_end\_date

혜택 종료일

customer\_group\_list

혜택 참여대상 설정

product\_binding\_type

혜택 상품 범위 설정

product\_list

혜택 적용 상품

add\_category\_list

혜택 적용 상품 분류

except\_category\_list

혜택 적용 제외상품

shipping\_code

배송번호

shipping\_company\_code

배송업체 코드

tracking\_no

송장번호

event\_code

주문 상태 관련 이벤트코드

create\_order (주문생성)  
pickup\_complete\_order (수거완료)  
product\_ready (상품 준비중)  
shipping\_end (배송완료 처리)  
purchase\_confirm (구매확정 처리)  
shipping\_ready (배송준비중 처리)  
shipping\_start (배송중 처리)  
shipping\_standby (배송대기 처리)  
do\_shipping\_holding (배송보류 처리)  
update\_invoice\_no (송장번호 변경)  
unpaid (입금전)  
paid\_order (입금확인)  
cancel\_order (취소처리)  
cancel\_order\_request (취소 신청)  
cancel\_unpaid\_order (입금전 주문취소)  
cancellation\_complete (취소 완료)  
auto\_order\_cancel (주문자동취소)  
return\_order (반품)  
return\_order\_process (반품 처리중)  
return\_order\_request (반품 신청)  
return\_complete\_refunded (반품 완료-환불 완료)  
return\_hold (반품 보류)  
exchange\_order (교환)  
exchange\_order\_request (교환 신청)  
exchange\_hold (교환 보류)  
exchange\_ready (교환 준비)  
refund\_order (환불 완료 처리)  
unrefund\_order (환불 전 처리)  
changing\_recipient\_information (수령자 정보 변경)  
insert\_admin\_memo (관리자 메모 등록)  
modify\_admin\_memo (관리자 메모 수정)  
delete\_admin\_memo (관리자 메모 삭제)  
old\_order\_delete (주문서 삭제)  
insert\_shipping\_expected\_date (발송예정일 등록)  
modify\_shipping\_expected\_date (발송예정일 수정)