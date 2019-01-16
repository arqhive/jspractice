#Event Bubbling
"Trigger clicks all the way up"

하위 요소에서 상위 요소로의 이벤트 전파 방식을 Event Bubbling 이라고 한다.

대부분 Bubbling이 발생한다. 예외로 focus는 발생하지 않음.

ex)

    <body>
      <div class="one">
        <div class="two">
          <div class="three">
          </div>
        </div>
      </div>
    </body>

    var divs = document.querySelectorAll('div');
    divs.forEach(function(div) {
      div.addEventListener('click', logEvent, {
        capture: true // 이 값을 주게 되면 이벤트가 상위에서 하위로 전파된다. (Event Caputure)
      });
    })

    function logEvent(event) {
      console.log(event.currentTarget.className);
    }

three, two, one 순으로 콘솔에 나타난다.

## 전파를 막는 방법
`event.stopPropagation();`

## event.target
최초 이벤트가 발생하는 엘리먼트

## event.currentTarget
실제로 이벤트가 실행되는 엘리먼트
