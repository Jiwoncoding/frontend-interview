## JavaScript 면접 질문
### this
자바스크립트에서 모든 함수는 실행될 때마다 함수 내부에 this라는 객체가 추가된다. arguments라는 유사 배열 객체와 함께 함수 내부로 암묵적으로 전달되는 것이다. 그렇기 때문에 자바스크립트에서의 this는 함수가 호출된 상황에 따라 그 모습을 달리한다.
- 객체의 메서드를 호출할 때 해당 메서드를 호출한 객체로 바인딩
- 함수를 호출할 때 전역객체에 바인딩
- 생성자 함수를 통해 객체를 생성할 때 객체 자신이 this, 자신의 부모인 프로토타입 객체와 연결

### Promise
프론트엔드의 규모가 커지면서 콜백이 중첩되는 경우가 발생하였고 이러한 콜백 지옥을 해결할 방안으로 나온 것이 Promise 패턴이다.
Promise 패턴을 사용하면 비동기 작업들을 순차적으로 진행하거나, 병렬로 진행하는 등의 컨트롤이 보다 수월해진다. 또한 예외처리에 대한 구조가 존재하기 때문에 오류 처리 등에 대해 보다 가시적으로 관리할 수 있다.

### Async/Await
비동기 코드를 작성하는 새로운 방법이다. function 키워드 앞에 async를 붙여주면 되고 function 내부의 promise를 반환하는 비동기 처리 함수 앞에 await를 붙여주기만 하면 된다.

### Arrow Function
화살표 함수는 항상 익명이며, 자신의 this, arguments, super 그리고 new.target을 바인딩하지 않는다. 그래서 생성자로는 사용할 수 없다. 함수 본연의 입출력 기능을 아주 직관적으로 잘 표현.

### require와 import의 차이점
require() 는 프로그램의 어느 지점에서나 호출 할 수 있지만 import() 는 파일의 시작 부분에서만 실행할 수 있다.

### ES6에서 arrow 함수를 언제 쓰고 왜 쓰는지
함수 본연의 기능을 아주 잘 표현한 문법이고 여러가지 기능을 하는 코드를 한 단어로 묶고 싶고 재사용 하고 싶을 때 입출력기능을 만들 때 사용한다. arrow 함수를 사용하면 함수 본연의 입출력기능을 아주 직관적으로 잘 표현한다.

### 입출력기능
소괄호에 뭔가 집어넣으면 return을 이용해 뭔가 뱉어내는 것 

### CORS를 대처하는 방법과 우회하는 방법
서버 측에서 Access-Control-Allow-Origin 헤더에 접근권한을 설정할 수 있다. 이 방법은 보안적 이슈에 직면할 수 있기 때문에 지양해야한다. 우회하는 방법에는 프록시설정이 있는데, 외부 도메인서버에 접근하고자할 때 바로 외부 도메인 서버를 통하는 것이 아닌 자신의 서버를 매개로 하여 외부서버에 요청하는 방식이다. 서버에서 요청을 하게될 때에는 브라우저의 규약인 CORS 정책에 영향을 받지않기 때문에 우회할 수 있다.

### MVVM 모델
MVVM(Model-View-ViewModel) 패턴을 사용하면 애플리케이션의 비즈니스 및 프레젠테이션 논리를 UI와 명확하게 구분할 수 있다.

### Promise와 Callback
- Promise : promise를 사용하면 비동기에서 온 값이 promise 객체에 저장되기 때문에 코드 작성이 용이해진다.
- Callback : callback을 사용하면 비동기 로직의 결과값을 처리하기 위해서는 callback안에서만 처리를 해야하고, 콜백 밖에서는 비동기에서 온 값을 알 수가 없다.

### Ajax
비동기적으로 JS를 사용해서 데이터를 받아와 동적으로 DOM을 갱신 및 조작하는 웹 개발 기법. 기존의 페이지를 전부 로딩하는 방식이 아닌 일부만 업데이트하는 방식

### 이벤트 위임
- 이벤트 버블링: 하위 엘리먼트에 이벤트가 발생할 때 그 엘리먼트로부터 시작해서 상위요소까지 이벤트가 전달되는 방식
- 이벤트 캡쳐링: 하위 엘리먼트에 이벤트 핸들러가 있을 때 상위 엘리먼트로부터 이벤트가 발생하기 시작해서 하위 엘리먼트까지 이벤트가 전달되는 방식
- 이벤트 위임: 하위 엘리먼트들이 여러개 있을 때, 하위 엘리먼트들에 각각 이벤트 핸들러를 달지 않고 상위 엘리먼트에 이벤트 핸들러를 달아 하위 엘리먼트들을 제어하는 방식

### 실행 콘텍스트
코드의 실행 환경에 대한 여러가지 정보를 담고 있는 개념으로 자바스크립트 엔진에 의해 만들어지고 사용되는 코드 정보를 담은 객체의 집합
- 자바스크립트 코드 종류 3가지: 글로벌 코드, 함수 코드, eval()

### 스코프
자바스크립트 엔진이 참조의 대상이 되는 식별자를 검색할 때 사용하는 규칙의 집합
- 렉시컬 스코프: 프로그래머가 코드를 짤 때, 변수 및 함수/블록 스코프를 어디에 작성하였는가에 따라 정해지는 스코프
- 스코프 체인: 현재 스코프에서 식별자를 검색할 때 상위 스코프를 연쇄적으로 찾아가는 방식

### 호이스팅
"끌어올린다"라는 뜻으로 변수 및 함수 선언문이 스코프 내의 최상단으로 끌어올려지는 현상이다. 함수 표현식은 호이스팅 되지 않고 함수와 변수 선언문 중에는 함수 선언문이 먼저다.

### 클로저
함수가 속한 렉시컬 스코프를 기억하여 함수가 렉시컬 스코프 밖에서 실행될 때도 그 스코프에 접근할 수 있게 하는 기능으로 대표적인 예로는 반복문 클로저가 있다.

### 네이티브 객체 vs 호스트 객체
- 네이티브 객체: Object, Function, Date, Math, ParseInt...
- 호스트 객체: window, document, location, querySelectorAll...

### var vs let vs const
- var: 함수 스코프, 함수 스코프의 최상단으로 호이스팅, 선언전에 출력하면 undefined, 재선언 가능, 재할당 가능
- let: 블록 스코프, 블로 스코프의 최상단으로 호이스팅, ReferenceError가 발생하는데 이런 현상을 TDZ라고 한다. 즉 선언은 되었지만 참조는 할 수 없는 사각지대를 갖는 것, 재선언 불가능, 재할당 가능
- const: 블록 스코프, 블록 스코프의 최상단으로 호이스팅, 재선언 불가능, 재할당 불가능

### IIFE(Immediately-invoked Function Expression)
즉시 실행 함수 표현식, 익명함수와 기명함수 모두 가능. IIFE를 사용하는 이유는 변수를 전역 스코프에 선언하는 것을 피함으로써 전역 스코프를 오염시키지 않기 위해 사용한다.

### 이벤트 루프
자바스크립트는 단일 스레드 기반으로 자바스크립트 엔진이 단일 콜 스택을 가진다. 이 말은 동기적으로 처리된다는 뜻인데, 비동기적 요청을 처리하기 위해서는 자바스크립트 엔진과 그 실행환경을 상호 연동시켜주는 장치가 필요한데 이것을 이벤트 루프라고 한다.

### 프로토타입
자바스크립트 객체 자신의 원형prototype
- 보이지 않는 속성인 `[[prototype]]`이 자신의 프로토타입 객체를 참조
- 함수 객체는 접근할 수 있는 속성인 `.prototype`을 갖는다. new 연산자로 자신을 생성자 함수로 사용한 경우, 그걸로 만들어진 새로운 객체의 `[[prototype]]`이 참조하는 값
- 프로토타입 체인: 어떤 객체의 프로퍼티를 참조하거나 값을 할당할 때 해당 객체에 프로퍼티가 없을 경우, 그 객체의 프로토타입 객체를 연쇄적으로 보면서 프로퍼티를 찾는 방식

### new의 동작 방식
- 빈 객체 생성
- `[[prototype]]`속성을 생성자 호출할 함수의 prototype 속성으로 지정
- 객체 생성하고 이 객체를 this로 지정
- 함수를 호출하고 해당 함수의 this로 위에서 지정한 객체 사용
- 함수의 리턴값이 원시값이라면 새로 만들어진 객체가 리턴되고 리턴값이 객체라면 해당 객체가 리턴

### 객체지향프로그래밍 OOP
컴퓨터 프로그램을 명령어의 목록으로 보는 시각에서 벗어나 여러 개의 독립된 단위, 즉 '객체'들의 모임으로 파악하고자 하는 것으로 각각의 객체는 메시지를 주고받고 데이터를 처리할 수 있다.




