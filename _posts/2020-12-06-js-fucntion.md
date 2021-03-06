---
title: Javascript 함수
date: 2020-11-16
categories: [javascript]
comments: true
---

## 함수(Function)

* function
* 특정 기능을 처리하는 자바스크립트 코드의 묶음이다.
```js
// 형태 1
function book(){
    var title = "js 책";
};
// 형태2
var point = function(one, two){
    var total = one + two;
    var bonus = total + 100;
}
```
--- 

## 함수의 구성요소

1. function 키워드
2. 함수 이름
3. 파라미터
    * 매개변수, 인자, 아규먼트로도 부른다.
    * 파라미터의 작성은 선택이다.
4. 함수 Body
    * 중괄호{} 안에 작성한 코드
    * 함수코드, 소스 텍스트로도 부른다.
    * 함수코드 작성은 선택이다.

---

## 함수의 이름 규칙

* 첫 문자
    * 영문자, $, 언더바(_) : 사용가눙
    * 숫자, &, *, @, + : 사용 불가
* 함수 이름 작명권장법
    * 함수 코드를 읽지 않더라도
    * 함수 이름과 파라미터로 기능을 알 수 있도록
    * 시맨틱(의미, 뜻)을 부여하여 작명한다.

---

## 호출받는 함수

* 함수는 호출되어야 실행된다. 
* 호출받는 함수
    함수가 호툴되었을 때 실행되는 함수이다.  
    함수라고 하면 호출받는 함수를 지칭한다.
* 파라미터
    호출한 함수에서 넘겨준 값을 받는다.  
    (one, two) 처럼 소괄호() 안에 파라미터 이름을 작성한다.

## 함수 호출

* 함수() 형태로 호출된다.
    함수 이름과 소괄호()를 작성한다.
    소괄호가 없으면 호출되지 않는다.
* 파라미터
    호툴된 함수에 넘겨줄 값을 작성한다.  
    소괄호 안에 작성한다.
    JS에서 지원하는 타입을 작성한다.  
    콤마(,)로 구분하여 다수 작성 가능하다.

```js
//호출받는 함수
function setValue(one, two){
    var total = one + two;
};
setValue(10, 20);
```
먼저 호출 받는 함수를 작성한다. 함수를 호출하며 파라미터 값 10,20을 호출받는 함수에 넘겨준다.  
호출된 함수에서 10->one, 20->two에 설정한다. 즉, 왼쪽에서 오른쪽으로 설정된다.  
그리고 setValue() 함수를 실행시킨다. 보통 호출받는 함수를 위에 작성하고 함수 호출을 아래에 작성한다. 이를 함수 라이프싸이클이라 한다.

---

## return

* 형태 : return 표현식opt;
* 표현식의 평가 결과가 반환된다.
```js
function getPoint(){
    return 10 * 30;
};
var result = getPoint();
log(result);
// 결과 값 : 300
```
먼저 getPoint() 함수를 호출한다.  
return의 오른쪽 표현식(10*30)을 평가한다. 그리고 평가결과 300을 반환한다.  
300을 가지고 getPoint()로 돌아간다.  
300을 return 변수에 할당한다.  

* 여기서 return을 작성하지 않으면 undefined 값을 반환한다.

* return과 표현식을 한 줄에 작성해야 한다.
    ```js
    // 실행됨
    return blha blha;
    //실행안됨
    return
    blha blha;
    
    ```
    한줄에 작성하지 않으면 return 끝에는 세미콜론이 자동으로 첨부가 되어버린다.
    그러면 return 뒤에 오는 표현식을 수행하지 않게 된다.

    ---
