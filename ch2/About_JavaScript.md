#### **📌 자바스크립트란**

웹 브라우저의 표준 프로그래밍 언어로, 프로그래밍 언어의 값, 타입, 객체와 프로퍼티, 함수, 표준 빌트인 객체 등의 핵심 문법을 규정하는 ECMAScript(ECMA-262)를 표준 사양으로 한다.

일반적으로 프로그래밍 언어로서 기본 뼈대를 이루는 ECMAScript와 브라우저가 별도로 지원하는 클라이언트 사이드 Web API(DOM, BOM, XMLHttpRequest, fetch, Web Storage 등)를 아우르는 개념이다.

#### **📌 자바스크립트의 특징**

- 개발자가 별도로 컴파일 작업을 수행하지 않는 **인터프리터 언어(Interpreter Language)**이다. 대부분의 모던 자바스크립트 엔진(크롬의 V8, 파이어폭스의 SpiderMonkey, 사파리의 JavaScriptCore, 마이크로소프트 엣지의 Chakra 등)은 인터프리터와 컴파일러의 장점을 결합해 동적 기능 지원을 살리면서 실행 속도가 느리다는 단점을 극복했다.
- 명령형, 함수형, 프로토타입 기반 객체지향 프로그래밍을 지원하는 **멀티 패러다임 프로그래밍 언어**이며 **프로토타입 기반의 객체지향 언어**이다.
- 함수를 다른 변수와 동일하게 다루는 **일급 함수**를 지원한다.

#### **📌 자바스크립트의 성장과 표준화**

브라우저에 따라 웹페이지가 정상적으로 동작하지 않는 크로스 브라우징 이슈를 해결하기 위해 넷스케이프 커뮤니케이션즈에서 비영리 표준화 기구인 ECMA 인터내셔널에 자바스크립트의 표준화를 요청해 1997년 7월 표준화된 자바스크립트 초판 사양(ECMAScript 1)인 ECMA-262가 완성됐다.

이후 1999년 ECMAScript 3(ES3)이 공개되었고, 2009년에는 HTML5와 함께 ECMAScript 5(ES5)가 출시되었다. 2015년에 공개된 ECMAScript 6(ECMAScript 2015, ES6)는 let/const 키워드, 화살표 함수, 클래스, 모듈 등과 같이 범용 프로그래밍 언어로서 갖춰야 할 기능들을 대거 도입하였다.

ECMAScript의 버전별 특징은 다음과 같다.

| 버전                   | 출시 연도 | 특징                                                                                                                                                                                      |
| ---------------------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ES1                    | 1997      | 초판                                                                                                                                                                                      |
| ES2                    | 1998      | ISO/IEC 16262 국제 표준과 동일한 규격을 적용                                                                                                                                              |
| ES3                    | 1999      | 정규 표현식, try ... catch, switch, do-while 추가                                                                                                                                         |
| ES5                    | 2009      | HTML5와 함께 출현한 표준안 JSON, strict mode, 접근자 프로퍼티, 프로퍼티 어트리뷰트 제어, 향상된 배열 조작 기능(forEach, map, filter, reduce, dome, every) 추가                            |
| ES6 (ECMAScript 2015)  | 2015      | let/const, 클래스, 화살표 함수, 템플릿 리터럴, 디스트럭처링 할당, 스프레드 문법, rest 파라미터, 심벌, 프로미스, Map/Set, 이터러블, for ... of, 제너레이터, Proxy, 모듈 import/export 추가 |
| ES7 (ECMAScript 2016)  | 2016      | 지수(\*\*) 연산자, Array.prototype.includes, String.prototype.includes 추가                                                                                                               |
| ES8 (ECMAScript 2017)  | 2017      | async/await, Object 정적 메서드(Object.values, Object.entries, Object.getOwnPropertyDescriptors) 추가                                                                                     |
| ES9 (ECMAScript 2018)  | 2018      | Object rest/spread 프로퍼티, Promise.prototype.finally, async generator, for await ... of 추가                                                                                            |
| ES10 (ECMAScript 2019) | 2019      | Object.fromEntries, Array.prototype.flat, Array.prototype.flatMap, optional catch binding 추가                                                                                            |
| ES11 (ECMAScript 2020) | 2020      | String.prototype.matchAll, BigInt, globalThis, Promise.allSettled, null 병합 연산자, 옵셔널 체이닝 연산자, for ... in enumeration order 추가                                              |
| ES12 (ECMAScript 2021) | 2021      | Promise.any, String.prototype.replaceAll, 숫자 구분 기호(\_), 논리 할당 연산자 추가                                                                                                       |

#### **📌 Ajax**

Ajax(Asynchronous JavaScript and XML)는 자바스크립트를 이용해 서버와 브라우저가 **비동기(Asynchronous) 방식**으로 데이터를 교환할 수 있게 하는 통신 기능이다. 서버와 통신하기 위해 XMLHttpRequest 객체를 사용하고 JSON, XML, HTML, 일반 텍스트 형식 등을 포함한 다양한 포맷을 주고받는다.

웹페이지가 업데이트될 때마다 전체를 렌더링하지 않고 서버에서 필요한 데이터만 전송받아 변경해야 하는 부분만 한정적으로 렌더링하는 비동기성을 갖고 있다.

즉, 페이지 새로고침 없이 서버에 요청(Request)하고 서버로부터 데이터를 응답(Response)받고 작업을 수행할 수 있게 해준다.

#### **📌 jQuery**

자바스크립트를 간편하게 사용할 수 있도록 단순화시킨 오픈 소스 기반의 자바스크립트 라이브러리이다.

jQuery를 사용하면 DOM(문서 객체 모델)과 이벤트 처리를 더욱 쉽게 제어할 수 있으며, 크로스 브라우징 이슈도 어느 정도 해결할 수 있다.

#### **📌 V8 자바스크립트 엔진**

웹 브라우저를 만드는 데 기반을 제공하는 오픈 소스 자바스크립트 엔진으로, 구글 크롬 브라우저와 안드로이드 브라우저에 탑재되어 있다.

더욱 빠른 성능을 가진 자바스크립트 엔진의 등장으로 자바스크립트는 데스크톱 애플리케이션과 유사한 사용자 경험(User Experience, UX)을 제공할 수 있는 웹 애플리케이션 프로그래밍 언어로 정착할 수 있게 되었다. 이로 인해 웹 서버에서 수행되던 로직들이 대거 클라이언트로 이동해 웹 애플리케이션 개발에서 프론트엔드 영역이 주목받게 되는 계기가 되었다.

#### **📌 Node.js**

구글 V8 자바스크립트 엔진으로 빌드된 자바스크립트 런타임 환경이다. 자바스크립트가 브라우저 이외의 환경에서도 동작할 수 있도록 자바스크립트 엔진을 브라우저에서 독립시킨 실행 환경이다.

서버쪽 개발에 주로 사용되며, 이에 필요한 모듈, 파일 시스템, HTTP 등 빌트인 API를 제공한다.

비동기 I/O를 지원하며 단일 스레드 이벤트 루프 기반으로 동작함으로써 요청 처리 성능이 좋다.

데이터를 실시간으로 처리하기 위해 I/O가 빈번히 발생하는 SPA에 적합하지만 CPU 사용률이 높은 애플리케이션에서는 권장되지 않는다.

Node.js의 등장으로 자바스크립트는 프론트엔드와 백엔드를 아우르는 범용 프로그래밍 언어가 되었으며, 크로스 플랫폼을 위한 가장 중요한 언어로 주목받게 되었다.

#### **📌 SPA 프레임워크**

개발의 규모와 복잡성이 커짐에 따라 변경에 유연하면서 확장하기 쉬운 애플리케이션 아키텍처의 구축이 어려워져 CBD(Component Based Development) 방법론을 기반으로 하는 **SPA(Single Page Application)**가 대중화되었다.

이로 인해 Angular, React, Vue.js와 같이 SPA를 구현하게 해주는 다양한 SPA 프레임워크/라이브러리들이 등장하게 되었고 많은 사용층을 확보했다.

#### **📌 ES6 브라우저 지원 현황**

대부분의 모던 브라우저들이 ES6를 지원하고 있다. 자세한 지원 현황은 다음 웹사이트에서 확인할 수 있다.

브라우저에서 지원하지 않는 최신 기능을 사용하거나 인터넷 익스플로러와 같은 구형 브라우저를 고려해야 한다면 바벨(Babel)과 같은 트랜스파일러를 사용해 ES6 이상의 사양으로 구현한 소스코드를 ES5 이하의 사양으로 다운그레이드 해줘야 한다.

[https://kangax.github.io/compat-table/es6/](https://kangax.github.io/compat-table/es6/ "ES6 브라우저 지원 현황")

[ECMAScript 6 compatibility table

Sort by Engine types Features Flagged features Show obsolete platforms Show unstable platforms <!-- --> V8 SpiderMonkey JavaScriptCore Chakra Carakan KJS Other ⬤ Minor difference (1 point) ⬤ Small feature (2 points) ⬤ Medium feature (4 points) ⬤ La

kangax.github.io](https://kangax.github.io/compat-table/es6/)

참고문헌 및 출처 : 모던 자바스크립트 Deep Dive (이웅모)
