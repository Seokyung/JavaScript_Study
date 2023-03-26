## 자바스크립트 연산자

#### **📌 연산자와 피연산자**

**연산자(Operator)** 는 하나 이상의 표현식을 대상으로 산술, 할당, 비교, 논리, 타입, 지수 연산 등을 수행해 하나의 값을 만든다.

연산자는 값으로 평가된 피연산자를 연산해 새로운 값을 만든다.

**피연산자(Operand)** 는 값으로 평가될 수 있는 표현식으로, 연산의 대상이 된다.

#### **📌 산술 연산자**

**산술 연산자(Arithmetic Operator)** 는 피연산자를 대상으로 수학적 계산을 수행해 새로운 숫자 값을 만든다. 산술 연산이 불가능한 경우에는 NaN을 반환한다.

**이항 산술 연산자(Binay Arithmetic Operator)** 는 2개의 피연산자를 산술 연산하여 숫자 값을 만든다.

모든 이항 산술 연산자는 피연산자의 값을 변경하는 **부수 효과** 가 없기 때문에 연산할 때 피연산자의 값이 바뀌는 경우는 없고 언제나 새로운 값을 만들어낸다.

| 이항 산술 연산자 | 의미   | 부수 효과 |
| ---------------- | ------ | --------- |
| +                | 덧셈   | X         |
| \-               | 뺄셈   | X         |
| \*               | 곱셈   | X         |
| /                | 나눗셈 | X         |
| %                | 나머지 | X         |

**단항 산술 연산자(Unary Arithmetic Operator)** 는 1개의 피연산자를 산술 연산하여 숫자 값을 만든다.ßß

| 단항 산술 연산자 | 의미                                                 | 부수 효과 |
| ---------------- | ---------------------------------------------------- | --------- |
| ++               | 증가                                                 | O         |
| \--              | 감소                                                 | O         |
| +                | 어떠한 효과도 없다. 음수를 양수로 반전하지도 않는다. | X         |
| \-               | 양수를 음수로, 음수를 양수로 반전한 값을 반환한다.   | X         |

증가/감소 연산자(++/--)는 부수 효과가 있다. 증가/감소 연산을 하면 피연산자의 값을 변경하는 암묵적 할당이 이루어진다는 것이다.

- 피연산자 앞에 위치한 **전위 증가/감소 연산자** 는 먼저 피연산자의 값을 증가/감소시킨 후, 다른 연산을 수행한다.
- 피연산자 뒤에 위치한 **후위 증가/감소 연산자** 는 먼저 다른 연산을 수행한 후, 피연산자의 값을 증가/감소시킨다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FmN3Cc%2Fbtr4xKFeSdZ%2FhOvIihDWs573zN5zki9DAk%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcePLPa%2Fbtr4vipqaTn%2FKUU5TOjFdPBiKJH7Kz0E80%2Fimg.png" />
<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbY1SwI%2Fbtr4ymKYA33%2F2bddeBDXW8Tda7MPdGd9G0%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fbtx1JP%2Fbtr4tiYccN6%2F8zJRLEBtp12f5D0fJt39Dk%2Fimg.png" />

**\+ 단항 연산자** 를 숫자 타입이 아닌 피연산자에 사용하면 피연산자를 숫자 타입으로 변환하여 반환한다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FEeuf4%2Fbtr4xKSK5hV%2FPFWHOBKAE9KBsM6SZaNpA1%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FR23IN%2Fbtr4zbP6ToI%2FRQ0SVsdaKROvTYg3KTKt3k%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbaVi6z%2Fbtr4t7u4kRX%2FAmOjhGLOZsRjNxZg1KLKx1%2Fimg.png" />

**\- 단항 연산자** 는 피연산자의 부호를 반전한 값을 반환한다. 숫자 타입이 아닌 피연산자에 사용하면 피연산자를 숫자 타입으로 변환하여 반환한다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FLquvl%2Fbtr4wFRVROT%2FOd8uLPVnMfI6CEPOjD8i20%2Fimg.png" />

- 연산자는 피연산자 중 하나 이상이 문자열인 경우 **문자열 연결 연산자** 로 동작한다.

문자열 연결 연산자를 사용하면 문자열이 아닌 피연산자는 자바스크립트 엔진에 의해 암묵적으로 타입이 자동 변환되는 **암묵적 타입 변환(Implicit Corection)** 또는 **타입 강제 변환(Type Corection)** 으로 인해 문자열로 타입이 변환된다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbbIBbd%2Fbtr4w6oeAtI%2FbHbfvZH0OvBEM7toNsr6Qk%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FKVrPR%2Fbtr4t5qAORt%2F5X9kzjFL9uxGfhmIduUoxK%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcNP8y2%2Fbtr4uKmaHao%2Fp1kMxjFKkr2BqxusxJtP90%2Fimg.png" />

#### **📌 할당 연산자**

**할당 연산자(Assignment Operator)** 는 우항에 있는 피연산자의 평가 결과를 좌항에 있는 변수에 할당한다. 좌항의 변수에 값을 할당하므로 변수 값이 변하는 부수 효과가 있다.

| 할당 연산자 | 예      | 동일 표현  | 부수 효과 |
| ----------- | ------- | ---------- | --------- |
| \=          | x = 5   | x = 5      | O         |
| +=          | x += 5  | x = x + 5  | O         |
| \-=         | x -= 5  | x = x - 5  | O         |
| \*=         | x \*= 5 | x = x \* 5 | O         |
| /=          | x /= 5  | x = x / 5  | O         |
| %=          | x %= 5  | x = x % 5  | O         |

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbUWqxL%2Fbtr4xhQIJb3%2F84kQRdCV9SRa4jxkSpUuEk%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcOdG1i%2Fbtr4vp22hjS%2FL9Gr35970SQdpr0J7U9Wq0%2Fimg.png" />

할당문은 값으로 평가되는 표현식인 문으로서 할당된 값으로 평가되기 때문에 여러 변수에 동일한 값을 연쇄 할당할 수 있다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fnbb5N%2Fbtr4tM5MutV%2FzijgaP9ycV6vokWQPer131%2Fimg.png" />

#### **📌 비교 연산자**

**비교 연산자(Comparison Operator)** 는 좌항과 우항의 피연산자를 비교한 다음 그 결과를 불리언 값으로 변환한다. 주로 제어문의 조건식에서 사용된다.

동등 비교(Loose Equality) 연산자와 일치 비교(Strict Equality) 연산자는 좌항과 우항의 피연산자가 같은 값으로 평가되는지 비교하여 불리언 값을 반환한다.

부동등 비교 연산자(!=)와 불일치 비교 연산자(!==)는 각각 동등 비교 연산자와 일치 비교 연산자의 반대 개념이다.

| 비교 연산자 | 의미        | 사례    | 설명                     | 부수 효과 |
| ----------- | ----------- | ------- | ------------------------ | --------- |
| \==         | 동등 비교   | x == y  | x와 y의 값이 같음        | X         |
| !=          | 부동등 비교 | x != y  | x와 y의 값이 다름        | X         |
| \===        | 일치 비교   | x === y | x와 y의 값과 타입이 같음 | X         |
| !==         | 불일치 비교 | x !== y | x와 y의 값과 타입이 다름 | X         |

**동등 비교 연산자(==)** 는 좌항과 우항의 피연산자를 비교할 때 먼저 암묵적 타입 변환을 통해 타입을 일치시킨 후 같은 값인지 비교한다.

즉, 좌항과 우항의 타입이 달라도 암묵적 타입 변환 후 값이 같으면 true가 반환되기 때문에 예측하기 어려운 결과가 나타날 수 있다. 따라서 동등 비교 연산자 대신 일치 비교 연산자를 사용할 것을 권장한다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fb4NuCT%2Fbtr4w4LLoPr%2FOa4q6J66nHSkxKyz4RfJTK%2Fimg.png" />

**일치 비교 연산자(===)** 는 좌항과 우항의 피연산자가 타입도 같고 값도 같은 경우에 한하여 true를 반환한다. 즉, 암묵적 타입 변환을 하지 않고 값을 비교하기 때문에 결과를 예측하기 쉽다.

NaN은 자신과 일치하지 않는 유일한 값이기 때문에 숫자가 NaN인지 조사하려면 일치 비교 연산자 대신 빌트인 함수 Number.isNaN을 사용해야 한다.

양의 0과 음의 0을 비교할 때에도 일치 비교, 동등 비교 연산자를 사용하면 true가 반환되기 때문에 Object.is 메서드를 사용해야 정확한 비교 결과를 얻을 수 있다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fb7RR8i%2Fbtr4yjBJGP6%2FZuASAiYaQLjNxon7nzI7KK%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fsk9m3%2Fbtr4ymkXxT9%2FHC1xSkbYZ3wkYfcuDtqYnK%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FddXvRz%2Fbtr4WFXsegN%2FcqCRuf5YlkPF2rDhCrrvzK%2Fimg.png" />

**대소 관계 비교 연산자** 는 피연산자의 크기를 비교해 불리언 값을 반환한다.

| 대소 관계 비교 연산자 | 예제   | 설명                  | 부수 효과 |
| --------------------- | ------ | --------------------- | --------- |
| \>                    | x > y  | x가 y보다 크다        | X         |
| <                     | x < y  | x가 y보다 작다        | X         |
| \>=                   | x >= y | x가 y보다 크거나 같다 | X         |
| <=                    | x <= y | x가 y보다 작거나 같다 | X         |

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FC6FO0%2Fbtr4vJuxs0g%2Fjeub89uA7m6qc6ezYHNJK1%2Fimg.png" />

#### **📌 삼항 조건 연산자**

**삼항 조건 연산자(Ternar Operator)** 는 조건식의 평가 결과에 따라 반환할 값을 결정한다. 표현식은 다음과 같이 사용한다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fc51rp9%2Fbtr4LH9CsYp%2FmCdMsks5hVeH9QpczDstlK%2Fimg.png" />

삼항 조건 연산자는 첫번째 피연산자가 true로 평가되면 두번째 피연산자를 반환하고, 첫번째 피연산자가 false로 평가되면 세번째 피연산자를 반환한다.

물음표(?) 앞의 첫번째 피연산자는 조건식, 즉 불리언 타입의 값으로 평가될 표현식이다. 조건식이 참이면 콜론(:) 앞의 두번째 피연산자가, 거짓이면 콜론 뒤의 세번째 피연산자가 평가되어 반환된다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcSl0qg%2Fbtr4zdnRsM6%2FoSnyRGElWtBUw1LPffAAik%2Fimg.png" />

삼항 조건 연산자 표현식은 조건문이기 때문에 if...else문을 사용해도 유사하게 처리할 수 있다. 하지만 삼항 조건 연산자 표현식은 if...else문과 달리 값으로 평가할 수 있는 표현식인 문이기 때문에 값처럼 다른 표현식의 일부가 될 수 있다.

조건에 따라 어떤 값을 결정해야 한다면 삼항 조건 연산자 표현식을 사용하는 것이 유리하지만, 조건에 따라 수행해야 할 문이 여러 개라면 if...else문을 사용하는 것이 가독성이 더 좋다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FctDTJN%2Fbtr4w4536QN%2FSkZ6tOwiZkFkNFnYVrTZZ1%2Fimg.png" />
<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdkAJ3P%2Fbtr4zdBn5Sp%2FkBGj7ifVQKEa7JPu3UXe8K%2Fimg.png" />

#### **📌 논리 연산자**

**논리 연산자(Logical Operator)** 는 우항과 좌항의 피연산자를 논리 연산한다. 부정 논리 연산자의 경우 우항의 피연산자를 논리 연산한다.

| 논리 연산자 | 의미         | 부수 효과 |
| ----------- | ------------ | --------- |
| \|\|        | 논리합 (OR)  | X         |
| &&          | 논리곱 (AND) | X         |
| !           | 부정 (NOT)   | X         |

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FLjvnK%2Fbtr4RBnIK56%2FOdkXq2cHJfRB5a8MtC68HK%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FsdY4K%2Fbtr4xLk6fY6%2F9kG3kp0ik1VOGRGnUybRSk%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdgSO5M%2Fbtr4G7U6f9S%2FzcBIvnI6xnNvraa9Dh4QZk%2Fimg.png" />

**논리 부정 연산자(!)** 는 언제나 불리언 값을 반환한다. 만약 피연산자가 불리언 값이 아니라면 불리언 타입으로 암묵적 타입 변환된다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcWjs2f%2Fbtr4xh5t9YR%2Fixu4GM8lMsKf8yEZPsHspK%2Fimg.png" />

**논리합(||) 또는 논리곱(&&) 연산자** 표현식은 언제나 2개의 피연산자 중 어느 한쪽으로 평가된다. 이를 단축 평가라고 한다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcQzyoE%2Fbtr4G7ngXKx%2FeVDfIEeyFxBLNZoiR2gks1%2Fimg.png" />

#### **📌 쉼표 연산자**

**쉼표 연산자(,)**는 왼쪽 피연산자부터 차례대로 피연산자를 평가하고 마지막 피연산자의 평가가 끝나면 마지막 피연산자의 평가 결과를 반환한다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbyvDwl%2Fbtr4LGXcCmz%2FXY2QfWIytqxcez0BQNKFQK%2Fimg.png" />

#### **📌 그룹 연산자**

소괄호( )로 피연산자를 감싸는 **그룹 연산자** 는 자신의 피연산자인 표현식을 가장 먼저 평가한다. 그룹 연산자는 연산자 우선순위가 가장 높기 때문에 연산자의 우선순위를 조절할 수 있다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbbZ6xs%2Fbtr4JKFwHM3%2FJFeHpB7tCSajxQZWFZTO0K%2Fimg.png" />

#### **📌 typeof 연산자**

**typeof 연산자** 는 피연산자의 데이터 타입을 문자열로 반환한다. 반환하는 데이터 타입 문자열에는 "string", "number", "boolean", "undefined", "symbol", "object", "function" 이 있다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F9cf7u%2Fbtr4xLer0GW%2FsbMl5e8kAl9awCTxCwNETk%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FlEFKK%2Fbtr4LEyv67g%2FkIrZJjUMmnFgoRuo66pmbk%2Fimg.png" />

typeof 연산자로 null 값을 연산하면 "null"이 아닌 "object" 가 반환된다. 즉, typeof 연산자가 반환하는 문자열과 데이터 타입이 정확하게 일치하지는 않는다. 값이 null 타입인지 확인하려면 대신 일치 연산자(==)를 사용하면 된다.

또한 선언하지 않은 식별자를 typeof 연산자로 연산하면 ReferenceError가 아닌 undefined를 반환하므로 주의해야 한다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FuD6fi%2Fbtr4DtqLfOa%2FJtb0CyBCc5Hn8dgKgOOIN0%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FuD6fi%2Fbtr4DtqLfOa%2FJtb0CyBCc5Hn8dgKgOOIN0%2Fimg.png" />

#### **📌 지수 연산자**

**지수 연산자(\*\*)** 는 좌항의 피연산자를 밑(base)으로, 우항의 피연산자를 지수(exponent)로 거듭 제곱하여 숫자 값을 반환한다.

음수를 거듭제곱의 밑으로 사용해 계산하려면 괄호로 묶어야 한다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FxtpXT%2Fbtr4AVPdyuY%2FMKU29KQUN9JnMFZodcHFAk%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fuir63%2Fbtr4LIO3kaV%2FfjuPVolhmJK3aqy2k0nTnK%2Fimg.png" />

지수 연산자는 할당 연산자와 함께 사용할 수 있다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FADIwM%2Fbtr415vbQaP%2FIJ8cNPjiZoS1JMN314NxR0%2Fimg.png" />

지수 연산자가 도입되기 전에는 **Math.pow 메서드** 를 사용했다. 지수 연산자는 우결합성을 갖기 때문에 연속해서 지수 연산을 하는 경우 Math.pow 메서드보다 가독성이 좋다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fb7AsF1%2Fbtr40SDbyi9%2FwKOWyEgyDuCBTqNfTw9fX0%2Fimg.png" />

#### **📌 그 외의 연산자**

이 연산자들에 대한 자세한 내용은 다른 포스팅에서 다룰 예정이다.

| 연산자     | 개요                                                        |
| ---------- | ----------------------------------------------------------- |
| ?.         | 옵셔널 체이닝 연산자                                        |
| ??         | null 병합 연산자                                            |
| delete     | 프로퍼티 삭제                                               |
| new        | 생성자 함수를 호출할 때 사용하여 인스턴스를 생성함          |
| instanceof | 좌변의 객체가 우변의 생성자 함수와 연결된 인스턴스인지 판별 |
| in         | 프로퍼티 존재 확인                                          |

#### **📌 연산자의 부수 효과**

다른 코드에 영향을 주는 부수 효과가 있는 연산자에는 **할당 연산자(=)** , **증가/감소 연산자(++/--)** , **delete 연산자** 가 있다.

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FT6SCZ%2Fbtr4LHP9VNT%2FDU5BHtXP4V4kyQ5jp1SkMk%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fbu38jB%2Fbtr4Dr8eXDF%2FIrwknmjjlxnu9LD24TogRK%2Fimg.png" /> <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FIep6M%2Fbtr4WGXlQb0%2FWEvp4WDQr3MvflEbGNkwJ0%2Fimg.png" />

#### **📌 연산자 우선 순위와 결합 순서**

**연산자 우선순위** 는 여러 개의 연산자로 이뤄진 문이 실행될 때 연산자가 실행되는 순서이다. 우선순위가 높을수록 먼저 실행된다.

연산자 우선순위가 가장 높은 그룹 연산자를 사용해 우선순위를 명시적으로 조절해 가독성을 높이면 실수를 줄일 수 있다.

| 우선순위 | 연산자                                                                                           |
| -------- | ------------------------------------------------------------------------------------------------ |
| 1        | ( )                                                                                              |
| 2        | new (매개변수 존재), ., \[ \] (프로퍼티 접근), ( ) (함수 호출), ?. (옵셔널 체이닝 연산자)        |
| 3        | new (매개변수 미존재)                                                                            |
| 4        | x++, x-- (후위 증감 연산자)                                                                      |
| 5        | !x (논리 부정(NOT) 연산자), +x, -x (+/-단항 연산자), ++x, --x (전위 증감 연산자), typeof, delete |
| 6        | \*\* (지수 연산자 - 이항 연산자 중에서 우선순위가 가장 높음)                                     |
| 7        | \*, /, % (이항 산술 연산자 - 곱셈, 나눗셈, 나머지 연산자)                                        |
| 8        | +, - (이항 산술 연산자 - 덧셈, 뺄셈 연산자)                                                      |
| 9        | <, <=, >, >= (대소 관계 비교 연산자), in, instanceof                                             |
| 10       | \==, !=, ===, !== (동등/일치 비교 연산자)                                                        |
| 11       | ?? (null 병합 연산자)                                                                            |
| 12       | && (논리곱(AND) 연산자)                                                                          |
| 13       | \|\| (논리합(OR) 연산자)                                                                         |
| 14       | ? ... : ... (삼항 조건 연산자)                                                                   |
| 15       | \=, +=, -=, \*=, /=, %= (할당 연산자)                                                            |
| 16       | , (쉼표 연산자)                                                                                  |

**연산자 결합 순서** 는 연산자의 어느 쪽(좌항 또는 우항)부터 평가를 수행할 것인가를 나타내는 순서이다.

| 결합 순서   | 연산자                                                                                   |
| ----------- | ---------------------------------------------------------------------------------------- |
| 좌항 → 우항 | +, -, /, %, <, <=, >, >=, &&, \|\|, ., \[\], (), ??, ?., in, instanceof                  |
| 우항 → 좌항 | ++, -- , =, +=, -=, \*=, /=, %=, !x, +x, -x, ++x, --x, typeof, delete, ? ... : ..., \*\* |

참고문헌 및 출처 : 모던 자바스크립트 Deep Dive (이웅모)
