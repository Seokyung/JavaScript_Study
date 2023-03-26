## 자바스크립트 데이터 타입

####  **📌 데이터 타입이란?**

**데이터 타입(Data Type)** 은 값의 종류를 말한다.

자바스크립트(ES6)는 원시 타입과 객체 타입으로 분류되는 7개의 데이터 타입을 제공한다.

| 구분                       | 데이터 타입                                       | 설명                                                |
| -------------------------- | ------------------------------------------------- | --------------------------------------------------- |
| 원시 타입                  | 숫자 타입 (Number Type)                           | 숫자, 정수와 실수 구분 없이 하나의 숫자 타입만 존재 |
| 문자열 타입 (String Type)  | 문자열                                            |
| 불리언 타입 (Boolean Type) | 논리적 참(true)과 거짓(false)                     |
| undefined 타입             | var 키워드로 선언된 변수에 암묵적으로 할당되는 값 |
| null 타입                  | 값이 없다는 것을 의도적으로 명시할 때 사용하는 값 |
| 심벌 타입 (Symbol Type)    | ES6에서 추가된 7번째 타입                         |
| 객체 타입                  |                                                   | 객체, 함수, 배열 등                                 |

####  **📌 숫자(Number) 타입**

자바스크립트 **숫자 타입** 은 모든 수를 실수로 처리한다. ECMAScript 사양에 따르면 숫자 타입의 값은 배정밀도 64비트 부동소수점 형식을 갖는다.

자바스크립트는 2진수, 8진수, 16진수를 표현하기 위한 데이터 타입을 제공하지 않기 때문에 모두 10진수로 해석된다.

```
var binary = 0b01000001; // 2진수
var octal = 0o101; // 8진수
var hex = 0x41; // 16진수

// 표기법만 다를 뿐 모두 같은 값이다. (10진수로 해석됨)
console.log(binary); // 65
console.log(octal); // 65
console.log(hex); // 65
console.log(binary === octal); // true
console.log(octal === hex); // true
```

숫자 타입이 모두 실수로 처리되기 때문에 정수로 표시되는 수끼리 나누더라도 실수가 나올 수 있다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fdb7Dci%2Fbtr2zlOeJoD%2FloAHr2vYub930tpsy5klb1%2Fimg.png" width="60%"/>

숫자 타입은 추가저으로 세 가지 특별한 값도 표현할 수 있다.

- Infinity : 양의 무한대
- \-Infinity : 음의 무한대
- NaN : 산술 연산 불가(not-a-number)

```
// 숫자 타입의 세 가지 특별한 값
console.log(10 / 0); // Infinity
console.log(10 / -1); // -Infinity
console.log(1 * 'String'); // NaN - 자바스크립트는 대소문자를 구분하기 때문에 NaN으로 표현하지 않으면 에러가 발생한다.
```

####  **📌 문자열(String) 타입**

**문자열 타입** 은 텍스트 데이터를 나타내는 데 사용한다.

문자열은 0개 이상의 16비트 유니코드 문자(UTF-16)의 집합으로 전 세계 대부분의 문자를 표현할 수 있다.

문자열은 작은따옴표(''), 큰따옴표("") 또는 백틱(\`\`)으로 텍스트를 감싼다.

문자열을 따옴표로 감싸는 이유는 키워드나 식별자 같은 토큰과 구분하기 위함이다. 따옴표로 문자열을 감싸지 않으면 스페이스와 같은 공백 문자도 포함시킬 수 없다.

자바스크립트의  문자열은 원시 타입이며, 변경 불가능한 값이다. 문자열을 생성하면 그 문자열을 변경할 수 없다는 뜻이다.

```
// 문자열 타입
var string;
string = '문자열'; // 작은따옴표 - 일반적인 표기법
string = "문자열"; // 큰따옴표
string = `문자열`; // 백틱(ES6)

string = '작은따옴표로 감싼 문자열 내의 "큰따옴표"는 문자열로 인식된다.';
string = "큰따옴표로 감싼 문자열 내의 '작은따옴표'는 문자열로 인식된다.";
```

####  **📌 템플릿 리터럴**

템플릿 리터럴은 **멀티라인 문자열(Muti-Line String)** , **표현식 삽입(Expression Interpolation)** , **태그드 템플릿(Tagged Template)** 등 편리한 문자열 처리 기능을 제공한다. 템플릿 리터럴은 백틱(\`\`)을 사용해 표현한다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FRuedy%2Fbtr2todZgJ2%2F6zlxlxcFiLUhr2n79ZP9N0%2Fimg.png" width="60%"/>

일반 문자열 내에서는 줄바꿈(개행)이 허용되지 않기 때문에 백슬래시(\\)로 시작하는 이스케이프 시퀀스(\\n, \\r, \\t 등)를 사용해야 한다.

이와 달리 템플릿 리터럴 내에서는 멀티라인 문자열 기능이 있어 이스케이프 시퀀스를 사용하지 않고도 줄바꿈이 허용되며, 모든 공백도 있는 그대로 적용된다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FxfueO%2Fbtr2ufBbfH0%2F7Id3DuLlU9AjU7NTWB1cp1%2Fimg.png" width="60%"/>

템플릿 리터럴 내에서는 ${}으로 표현식을 감싸 표현식을 삽입할 수 있다. 표현식의 평가 결과 문자열이 아니더라도 강제로 문자열로 타입이 변환되어 삽입된다.

표현식 삽입은 반드시 템플릿 리터럴 내에서 사용해야 한다. 일반 문자열에서의 표현식 삽입은 문자열로 취급된다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fctzjkb%2Fbtr2r50b7DC%2FFDR4ji03OdIkH6rmFgaX81%2Fimg.png" width="60%"/>

####  **📌 불리언(Boolean) 타입**

**불리언 타입** 의 값에는 논리적 참, 거짓을 나타내는 true와 false가 있다.

불리언 타입의 값은 참과 거짓으로 구분되는 조건에 의해 프로그램의 흐름을 제어하는 조건문에서 자주 사용한다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FrwifP%2Fbtr2Ct6lKR3%2FlKPSPOt94SCsiuRYOLGPA1%2Fimg.png" width="60%"/>

####  **📌 undefined 타입**

**undefined** 는 자바스크립트 엔진이 변수를 초기화 할 때 사용하는 값이다. 변수를 선언한 이후 값을 할당하지 않고 참조하면 undefined가 반환된다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbhJhVs%2Fbtr2C9muzeQ%2FODAFilpURLhuk36Fl8vMvK%2Fimg.png" width="60%"/>

####  **📌 null 타입**

**null** 은 변수에 값이 없다는 것을 의도적으로 명시(의도적 부재)할 때 사용한다. 변수에 null을 할당하는 것은 변수가 이전에 참조하던 값을 더 이상 참조하지 않겠다는 의미이다.

함수가 유효한 값을 반환할 수 없는 경우에도 명시적으로 null을 반환하기도 한다.

```
var foo = 'Kim';

foo = null; // 이전 참조를 제거한다. foo 변수는 더 이상 'Kim'을 참조하지 않는다.
```

####  **📌 심벌(Symbol) 타입**

**심벌** 값은 다른 값과 중복되지 않는 유일무이한 값이다. 주로 이름이 충돌할 위험이 없는 객체의 유일무이한 프로퍼티 키를 만들기 위해 사용한다.

심벌은 Symbol 함수를 호출해 생성한다. 이때 생성된 심벌 값은 외부에 노출되지 않으며, 다른 값과 절대 중복되지 않는다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FOwkbW%2Fbtr2znTlTxa%2F01tTa05j7J22yD6at40rik%2Fimg.png" width="60%"/>

####  **📌 객체 타입**

**객체** 는 변경 가능한 값으로, 원시 값을 제외한 모든 값은 객체 타입이다.

객체는 0개 이상의 프로퍼티로 구성된 집합이며, 프로퍼티는 키(key)와 값(value)으로 구성된다.

```
// 객체 타입
var person = {
	name: 'Jimin',
    age: 20,
};
```

####  **📌 데이터 타입의 필요성**

데이터 타입이 필요한 이유는 다음과 같다.

- 값을 저장할 때 **확보해야 하는 메모리 공간의 크기를 결정** 하기 위함이다.
- 값을 참조할 때 **한 번에 읽어 들여야 할 메모리 공간의 크기를 결정** 하기 위함이다.
- 메모리에서 읽어 들인 **2진수를 어떻게 해석할 지 판단** 하기 위함이다. (같은 2진수 값이어도 타입에 따라 다르게 해석된다.)

####  **📌 정적 타입 언어와 동적 타입 언어**

**정적 타입 언어(Static/Strong Type)** 는 변수를 선언할 때 데이터 타입을 사전에 선언해야 한다. 이를 명시적 타입 선언(Explicit Type Declaration)이라고 한다.

정적 타입 언어는 변수의 타입을 변경할 수 없으며, 변수에 선언한 타입에 맞는 값만 할당할 수 있다. 또한 컴파일 시점에 타입 체크를 수행해 통과하지 못하면 에러를 발생시키고 프로그램의 실행 자체를 막는다.

대표적인 정적 타입 언어로 C, C++, 자바(Java), 코틀린(Kotlin), 고(Go), 하스켈(Haskell), 러스트(Rust), 스칼라(Scala) 등이 있다.

```
// C언어에서의 변수 선언
int num; // num 변수에는 4바이트 정수 타입의 값만 할당할 수 있다.

char c; // c 변수에는 1바이트 정수 타입의 값만 할당할 수 있다.
```

**동적 타입 언어(Dynamic/Weak Type)** 는 변수를 선언할 때 타입을 선언하지 않고, var, let, const와 같은 키워드를 사용해 변수를 선언한다.

동적 타입 언어는 어떠한 데이터 타입의 값이라도 자유롭게 변수에 할당할 수 있다.

자바스크립트에서 변수 타입은 현재 변수에 할당되어 있는 값에 의해 동적으로 결정(타입 추론 Type Inference)된다. 즉, 값을 할당하는 시점에 변수 타입이 동적으로 결정되고 언제든지 재할당에 의해 타입이 변경될 수 있는 **동적 타이핑(Dynamic Typing)** 이라는 특징을 가진다.

대표적인 동적 타입 언어로는 자바스크립트, 파이썬(Python), PHP, 루비(Ruby), 리스프(Lisp), 펄(Perl) 등이 있다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FtFhlZ%2Fbtr2D4MlMTJ%2F2KgwmekcwT8VAjrmRkPeV0%2Fimg.png" width="40%"/>

####  **📌 동적 타입 언어 사용 시 주의사항**

동적 타입 언어는 유연성은 높지만 신뢰성은 떨어진다는 단점이 있다.

동적 타입 언어의 변수는 언제든지 변경될 수 있기 때문에 복잡한 프로그램에서는 변화하는 변수 값을 추적하기 어려울 수 있다.

게다가 자바스크립트는 개발자의 의도와 상관없이 자바스크립트 엔진에 의해 암묵적으로 타입이 자동으로 변환되기도 하기 때문에 잘못된 타입 예측으로 오류가 발생할 수 있다.

안정적인 프로그램을 만들기 위해 **동적 타입 언어에서 변수를 사용할 때 주의할 사항** 은 다음과 같다.

- 변수는 꼭 필요한 경우에 한해 제한적으로 사용한다.
- 변수의 유효 범위(스코프)는 최대한 좁게 만들어 변수의 부작용을 억제해야 한다.
- 전역 변수는 최대한 사용하지 않도록 한다.
- 변수보다는 상수(const)를 사용해 값의 변경을 억제한다.
- 변수 이름은 변수의 목적이나 의미를 파악할 수 있도록 짓는다.

###### 참고문헌 및 출처 : 모던 자바스크립트 Deep Dive (이웅모)
