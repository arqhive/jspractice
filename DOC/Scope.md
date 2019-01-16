# Scope (in web browser)
변수에 접근할 수 있는 범위

## Global Scope
변수가 함수 바깥이나 중괄호 바깥에 선언되었다면, 전역 스코프에 정의된다고 한다.


    var a = 1;
    var a = 2;

var 키워드를 사용한 경우 두번째 a가 첫번째 a를 덮어 쓰게 된다. (var는 사용하지 않는다.)

let, const 키워드를 사용한 경우 이미 선언되었다는 에러가 난다.

## Local Scope

### Function Scope
함수 내부에서 선언된 변수는 함수 내부에서만 접근이 가능하다.

### Block Scope
{} 내부에서 선언된 변수는 {}내부에서만 접근이 가능하다.


## 함수 호이스팅과 스코프

### Function delaration

    sayHello()

    function sayHello () {
      console.log('헬로우')
    }
----

    function sayHello () {
      console.log('헬로우')
    }

    sayHello()

위의 두가지 경우는 같은 결과를 보인다. 함수 선언식으로 함수가 선언되면, 스코프의 최상단으로 호이스팅 된다.

### Function expression (함수 표현식)
함수 표현식으로 초기화되면, 호이스팅 되지 않는다. (호이스팅은 선언!만 호이스팅 한다.)

    const sayHello = function () {
     console.log('난 호이스팅 안돼')
    }

### Lexical scoping

    function outerFunction () {
      const outer = 'I’m the outer function!'

      function innerFunction() {
        const inner = 'I’m the inner function!'
        console.log(outer) // 내부 함수가 외부 함수의 변수로 접근이 가능하다.
      }

      console.log(inner) // 외부 함수는 내부 함수로 접근 할 수 없다.
    }
