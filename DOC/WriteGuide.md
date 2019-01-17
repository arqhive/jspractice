# JavaScript Statement

컴퓨터 프로그램은 컴퓨터에 의해 "지침", "실행"할 목록이다. 프로그래밍 언어에서 이러한 프로그래밍 명령을 명령문이라고 한다.

HTML에서는 자바스크립트 프로그램이 웹 브라우저에 의해 실행된다.

Statement는 다음으로 구성된다.
1. 값 (value)
2. 연산자 (operator)
3. 표현식 (expression)
4. 키워드 및 주석 (comment)

## Convention

1. 세미콜론이 없어도 되지만 적극 권장됨
2. 읽기 좋게 연산자 주위에 공백을 넣는다.
3. 80자 이상에서는 줄을 바꾼다.
4. 들여쓰기는 2개의 space
5. 스크립트를 시작할 때 모든 변수를 선언하는 것이 좋은 프로그래밍 습관이다.


## Type

타입은 typeof 로 알 수 있다.

Primitive type 여섯가지
1. Boolean
2. null
3. undefined
4. Number(+, -, NaN)
5. String
6. Symbol (ES6)

+7. Object

## 여러가지

1. 변수를 선언하면 undefined 값이 담긴다.
2. 자바스크립트의 타입은 동적이다.
3. name:value 쌍을 property라고 부른다.
4. 두 개의 객체를 비교하면 값은 항상 false다.
5. 모든 자바스크립트 객체에는 toString 메소드가 있다.

## break, continue
for, switch 등과 같은 구문에서 break;를 만나게 된다면 더이상 진행하지 않는다.

continue를 만나면 해당 조건은 건너뛰고 다음 문장을 실행한다.

## 유형
값을 포함하는 5가지 유형
`string, number, boolean, object, function`

3가지 유형의 객체
`Object, Date, Array`

값을 포함 할 수 없는 두 가지 유형
`null, undefined`

## 에러 처리
try ~ catch 문

finally 키워드를 사용하면 try ~ catch 이후에 할 일을 기술 할 수 있다.

throw; 임의적으로 예외를 발생시킨다.

## 성능
반복문 외부에 배치 할 수 있는 값은 외부에 배치한다. 예) arr.length

자주 접근하는 DOM은 변수에 담아둔다.

    var obj;
    obj = document.getElementById('demo');

지속적으로 저장할 필요가 없는 값은 변수를 따로 만들지 않는다.

스크립트 코드를 HTML 아래에 두면 페이지가 먼저 로드 된 뒤 스크립트가 로드 된다.
