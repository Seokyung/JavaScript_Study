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

**단항 산술 연산자(Unary Arithmetic Operator)** 는 1개의 피연산자를 산술 연산하여 숫자 값을 만든다.

| 단항 산술 연산자 | 의미                                                 | 부수 효과 |
| ---------------- | ---------------------------------------------------- | --------- |
| ++               | 증가                                                 | O         |
| \--              | 감소                                                 | O         |
| +                | 어떠한 효과도 없다. 음수를 양수로 반전하지도 않는다. | X         |
| \-               | 양수를 음수로, 음수를 양수로 반전한 값을 반환한다.   | X         |

증가/감소 연산자(++/--)는 부수 효과가 있다. 증가/감소 연산을 하면 피연산자의 값을 변경하는 암묵적 할당이 이루어진다는 것이다.

- 피연산자 앞에 위치한 **전위 증가/감소 연산자** 는 먼저 피연산자의 값을 증가/감소시킨 후, 다른 연산을 수행한다.
- 피연산자 뒤에 위치한 **후\*\***위 증가/감소 연산자\*\* 는 먼저 다른 연산을 수행한 후, 피연산자의 값을 증가/감소시킨다.

[##_ImageGrid|kage@mN3Cc/btr4xKFeSdZ/hOvIihDWs573zN5zki9DAk/img.png,kage@cePLPa/btr4vipqaTn/KUU5TOjFdPBiKJH7Kz0E80/img.png,kage@bY1SwI/btr4ymKYA33/2bddeBDXW8Tda7MPdGd9G0/img.png,kage@btx1JP/btr4tiYccN6/8zJRLEBtp12f5D0fJt39Dk/img.png|data-is-animation="false" data-origin-width="362" data-origin-height="148" data-filename="스크린샷 2023-03-18 오전 1.22.10.png" data-widthpercent="41.31" style="width: 40.828%; margin-right: 10px;",data-is-animation="false" data-origin-width="351" data-origin-height="101" data-filename="edited_스크린샷 2023-03-18 오전 1.22.28.png" data-widthpercent="58.69" style="width: 58.0092%;",data-is-animation="false" data-origin-width="354" data-origin-height="106" data-filename="edited_스크린샷 2023-03-18 오전 1.22.47.png" data-widthpercent="49.2" style="width: 48.6323%; margin-right: 10px; margin-top: 10px;",data-is-animation="false" data-origin-width="362" data-origin-height="105" data-filename="edited_스크린샷 2023-03-18 오전 1.23.02.png" data-widthpercent="50.8" style="width: 50.2049%; margin-top: 10px;"|_##]

**\+ 단항 연산자** 를 숫자 타입이 아닌 피연산자에 사용하면 피연산자를 숫자 타입으로 변환하여 반환한다.

[##_ImageGrid|kage@Eeuf4/btr4xKSK5hV/PFWHOBKAE9KBsM6SZaNpA1/img.png,kage@R23IN/btr4zbP6ToI/RQ0SVsdaKROvTYg3KTKt3k/img.png,kage@baVi6z/btr4t7u4kRX/AmOjhGLOZsRjNxZg1KLKx1/img.png|data-is-animation="false" data-origin-width="280" data-origin-height="162" data-filename="스크린샷 2023-03-18 오전 1.27.48.png" style="width: 33.8207%; margin-right: 10px;" data-widthpercent="34.63",data-origin-width="280" data-origin-height="166" data-is-animation="false" style="width: 33.0058%; margin-right: 10px;" data-widthpercent="33.79",data-is-animation="false" data-origin-width="268" data-origin-height="170" data-filename="스크린샷 2023-03-18 오전 1.32.51.png" style="width: 30.8479%;" data-widthpercent="31.58"|_##]

**\- 단항 연산자** 는 피연산자의 부호를 반전한 값을 반환한다. 숫자 타입이 아닌 피연산자에 사용하면 피연산자를 숫자 타입으로 변환하여 반환한다.

[##_Image|kage@Lquvl/btr4wFRVROT/Od8uLPVnMfI6CEPOjD8i20/img.png|CDM|1.3|{"originWidth":170,"originHeight":294,"style":"alignCenter","filename":"edited_스크린샷 2023-03-18 오전 1.34.56.png"}_##]

- 연산자는 피연산자 중 하나 이상이 문자열인 경우 **문자열 연결 연산자** 로 동작한다.

문자열 연결 연산자를 사용하면 문자열이 아닌 피연산자는 자바스크립트 엔진에 의해 암묵적으로 타입이 자동 변환되는 **암묵적 타입 변환(Implicit Corection)** 또는 **타입 강제 변환(Type Corection)** 으로 인해 문자열로 타입이 변환된다.

[##_ImageGrid|kage@bbIBbd/btr4w6oeAtI/bHbfvZH0OvBEM7toNsr6Qk/img.png,kage@KVrPR/btr4t5qAORt/5X9kzjFL9uxGfhmIduUoxK/img.png,kage@cNP8y2/btr4uKmaHao/p1kMxjFKkr2BqxusxJtP90/img.png|data-is-animation="false" data-origin-width="164" data-origin-height="152" data-filename="스크린샷 2023-03-18 오전 1.43.37.png" data-widthpercent="29.98" style="width: 29.2834%; margin-right: 10px;",data-is-animation="false" data-origin-width="196" data-origin-height="160" data-filename="스크린샷 2023-03-18 오전 1.46.55.png" style="width: 33.2473%; margin-right: 10px;" data-widthpercent="34.04",data-is-animation="false" data-origin-width="202" data-origin-height="156" data-filename="스크린샷 2023-03-18 오전 1.47.05.png" style="width: 35.1437%;" data-widthpercent="35.98"|_##]

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

[##_ImageGrid|kage@bUWqxL/btr4xhQIJb3/84kQRdCV9SRa4jxkSpUuEk/img.png,kage@cOdG1i/btr4vp22hjS/L9Gr35970SQdpr0J7U9Wq0/img.png|data-is-animation="false" data-origin-width="260" data-origin-height="434" data-filename="스크린샷 2023-03-18 오전 1.58.55.png" style="width: 46.0809%; margin-right: 10px;" data-widthpercent="46.62",data-is-animation="false" data-origin-width="262" data-origin-height="382" data-filename="스크린샷 2023-03-18 오전 1.59.08.png" style="width: 52.7564%;" data-widthpercent="53.38"|_##]

할당문은 값으로 평가되는 표현식인 문으로서 할당된 값으로 평가되기 때문에 여러 변수에 동일한 값을 연쇄 할당할 수 있다.

[##_Image|kage@nbb5N/btr4tM5MutV/zijgaP9ycV6vokWQPer131/img.png|CDM|1.3|{"originWidth":607,"originHeight":206,"style":"alignCenter","filename":"edited_스크린샷 2023-03-18 오전 1.56.11.png"}_##]

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

[##_Image|kage@b4NuCT/btr4w4LLoPr/Oa4q6J66nHSkxKyz4RfJTK/img.png|CDM|1.3|{"originWidth":284,"originHeight":300,"style":"alignCenter","filename":"edited_스크린샷 2023-03-20 오전 2.33.59.png"}_##]

**일치 비교 연산자(===)** 는 좌항과 우항의 피연산자가 타입도 같고 값도 같은 경우에 한하여 true를 반환한다. 즉, 암묵적 타입 변환을 하지 않고 값을 비교하기 때문에 결과를 예측하기 쉽다.

NaN은 자신과 일치하지 않는 유일한 값이기 때문에 숫자가 NaN인지 조사하려면 일치 비교 연산자 대신 빌트인 함수 Number.isNaN을 사용해야 한다.

양의 0과 음의 0을 비교할 때에도 일치 비교, 동등 비교 연산자를 사용하면 true가 반환되기 때문에 Object.is 메서드를 사용해야 정확한 비교 결과를 얻을 수 있다.

[##_ImageGrid|kage@b7RR8i/btr4yjBJGP6/ZuASAiYaQLjNxon7nzI7KK/img.png,kage@sk9m3/btr4ymkXxT9/HC1xSkbYZ3wkYfcuDtqYnK/img.png,kage@ddXvRz/btr4WFXsegN/cqCRuf5YlkPF2rDhCrrvzK/img.png|data-is-animation="false" data-origin-width="206" data-origin-height="158" data-filename="스크린샷 2023-03-20 오전 2.41.35.png" data-widthpercent="28.68" style="width: 28.0156%; margin-right: 10px;",data-is-animation="false" data-origin-width="310" data-origin-height="154" data-filename="스크린샷 2023-03-20 오전 2.41.48.png" style="width: 43.2544%; margin-right: 10px;" data-widthpercent="44.28",data-is-animation="false" data-origin-width="290" data-origin-height="236" data-filename="스크린샷 2023-03-20 오전 2.42.28.png" style="width: 26.4044%;" data-widthpercent="27.04"|_##]

**대소 관계 비교 연산자** 는 피연산자의 크기를 비교해 불리언 값을 반환한다.

| 대소 관계 비교 연산자 | 예제   |     | 설명                  | 부수 효과 |
| --------------------- | ------ | --- | --------------------- | --------- |
| \>                    | x > y  |     | x가 y보다 크다        | X         |
| <                     | x < y  |     | x가 y보다 작다        | X         |
| \>=                   | x >= y |     | x가 y보다 크거나 같다 | X         |
| <=                    | x <= y |     | x가 y보다 작거나 같다 | X         |

[##_Image|kage@C6FO0/btr4vJuxs0g/jeub89uA7m6qc6ezYHNJK1/img.png|CDM|1.3|{"originWidth":171,"originHeight":299,"style":"alignCenter","filename":"edited_스크린샷 2023-03-20 오전 2.48.28.png"}_##]

#### **📌 삼항 조건 연산자**

**삼항 조건 연산자(Ternar Operator)** 는 조건식의 평가 결과에 따라 반환할 값을 결정한다. 표현식은 다음과 같이 사용한다.

[##_Image|kage@c51rp9/btr4LH9CsYp/mCdMsks5hVeH9QpczDstlK/img.png|CDM|1.3|{"originWidth":1753,"originHeight":679,"style":"alignCenter","filename":"edited_edited_스크린샷 2023-03-20 오전 11.44.06.png"}_##]

삼항 조건 연산자는 첫번째 피연산자가 true로 평가되면 두번째 피연산자를 반환하고, 첫번째 피연산자가 false로 평가되면 세번째 피연산자를 반환한다.

물음표(?) 앞의 첫번째 피연산자는 조건식, 즉 불리언 타입의 값으로 평가될 표현식이다. 조건식이 참이면 콜론(:) 앞의 두번째 피연산자가, 거짓이면 콜론 뒤의 세번째 피연산자가 평가되어 반환된다.

[##_Image|kage@cSl0qg/btr4zdnRsM6/oSnyRGElWtBUw1LPffAAik/img.png|CDM|1.3|{"originWidth":520,"originHeight":130,"style":"alignCenter","filename":"스크린샷 2023-03-20 오전 2.55.06.png"}_##]

삼항 조건 연산자 표현식은 조건문이기 때문에 if...else문을 사용해도 유사하게 처리할 수 있다. 하지만 삼항 조건 연산자 표현식은 if...else문과 달리 값으로 평가할 수 있는 표현식인 문이기 때문에 값처럼 다른 표현식의 일부가 될 수 있다.

조건에 따라 어떤 값을 결정해야 한다면 삼항 조건 연산자 표현식을 사용하는 것이 유리하지만, 조건에 따라 수행해야 할 문이 여러 개라면 if...else문을 사용하는 것이 가독성이 더 좋다.

[##*Image|kage@ctDTJN/btr4w4536QN/SkZ6tOwiZkFkNFnYVrTZZ1/img.png|CDM|1.3|{"originWidth":390,"originHeight":156,"style":"alignCenter","filename":"edited*스크린샷 2023-03-20 오전 3.02.58.png"}\_##][##_image|kage@dkaj3p/btr4zdbn5sp/kbgj7ifvqkea7jpu3uxe8k/img.png|cdm|1.3|{"originwidth":964,"originheight":230,"style":"aligncenter","filename":"스크린샷 2023-03-20 오전 3.02.12.png"}_##]

#### **📌 논리 연산자**

**논리 연산자(Logical Operator)** 는 우항과 좌항의 피연산자를 논리 연산한다. 부정 논리 연산자의 경우 우항의 피연산자를 논리 연산한다.

| 논리 연산자 | 의미         | 부수 효과 |
| ----------- | ------------ | --------- |
| \|\|        | 논리합 (OR)  | X         |
| &&          | 논리곱 (AND) | X         |
| !           | 부정 (NOT)   | X         |

[##_ImageGrid|kage@LjvnK/btr4RBnIK56/OdkXq2cHJfRB5a8MtC68HK/img.png,kage@sdY4K/btr4xLk6fY6/9kG3kp0ik1VOGRGnUybRSk/img.png,kage@dgSO5M/btr4G7U6f9S/zcBIvnI6xnNvraa9Dh4QZk/img.png|data-is-animation="false" data-origin-width="270" data-origin-height="304" data-filename="스크린샷 2023-03-20 오전 11.53.32.png" style="width: 30.8343%; margin-right: 10px;" data-widthpercent="31.57",data-is-animation="false" data-origin-width="262" data-origin-height="300" data-filename="스크린샷 2023-03-20 오전 11.54.08.png" style="width: 30.3196%; margin-right: 10px;" data-widthpercent="31.04",data-is-animation="false" data-origin-width="162" data-origin-height="154" data-filename="스크린샷 2023-03-20 오전 11.54.43.png" style="width: 36.5206%;" data-widthpercent="37.39"|_##]

**논리 부정 연산자(!)** 는 언제나 불리언 값을 반환한다. 만약 피연산자가 불리언 값이 아니라면 불리언 타입으로 암묵적 타입 변환된다.

[##_Image|kage@cWjs2f/btr4xh5t9YR/ixu4GM8lMsKf8yEZPsHspK/img.png|CDM|1.3|{"originWidth":174,"originHeight":152,"style":"alignCenter","filename":"스크린샷 2023-03-20 오전 11.55.35.png"}_##]

**논리합(||) 또는 논리곱(&&) 연산자** 표현식은 언제나 2개의 피연산자 중 어느 한쪽으로 평가된다. 이를 단축 평가라고 한다.

[##_Image|kage@cQzyoE/btr4G7ngXKx/eVDfIEeyFxBLNZoiR2gks1/img.png|CDM|1.3|{"originWidth":276,"originHeight":152,"style":"alignCenter","filename":"스크린샷 2023-03-20 오전 11.56.19.png"}_##]

#### **📌 쉼표 연산자**

**쉼표 연산자(,)**는 왼쪽 피연산자부터 차례대로 피연산자를 평가하고 마지막 피연산자의 평가가 끝나면 마지막 피연산자의 평가 결과를 반환한다.

[##_Image|kage@byvDwl/btr4LGXcCmz/XY2QfWIytqxcez0BQNKFQK/img.png|CDM|1.3|{"originWidth":332,"originHeight":106,"style":"alignCenter","filename":"스크린샷 2023-03-20 오전 11.59.46.png"}_##]

#### **📌 그룹 연산자**

소괄호( )로 피연산자를 감싸는 **그룹 연산자** 는 자신의 피연산자인 표현식을 가장 먼저 평가한다. 그룹 연산자는 연산자 우선순위가 가장 높기 때문에 연산자의 우선순위를 조절할 수 있다.

[##_Image|kage@bbZ6xs/btr4JKFwHM3/JFeHpB7tCSajxQZWFZTO0K/img.png|CDM|1.3|{"originWidth":233,"originHeight":145,"style":"alignCenter","filename":"edited_스크린샷 2023-03-20 오후 12.21.46.png"}_##]

#### **📌 typeof 연산자**

**typeof 연산자** 는 피연산자의 데이터 타입을 문자열로 반환한다. 반환하는 데이터 타입 문자열에는 "string", "number", "boolean", "undefined", "symbol", "object", "function" 이 있다.

[##_ImageGrid|kage@9cf7u/btr4xLer0GW/sbMl5e8kAl9awCTxCwNETk/img.png,kage@lEFKK/btr4LEyv67g/kIrZJjUMmnFgoRuo66pmbk/img.png|data-is-animation="false" data-origin-width="276" data-origin-height="445" data-filename="edited_스크린샷 2023-03-20 오후 1.08.57.png" data-widthpercent="40.23" style="width: 39.7638%; margin-right: 10px;",data-is-animation="false" data-origin-width="340" data-origin-height="369" data-filename="edited_스크린샷 2023-03-20 오후 1.09.10.png" data-widthpercent="59.77" style="width: 59.0734%;"|_##]

typeof 연산자로 null 값을 연산하면 "null"이 아닌 "object" 가 반환된다. 즉, typeof 연산자가 반환하는 문자열과 데이터 타입이 정확하게 일치하지는 않는다. 값이 null 타입인지 확인하려면 대신 일치 연산자(==)를 사용하면 된다.

또한 선언하지 않은 식별자를 typeof 연산자로 연산하면 ReferenceError가 아닌 undefined를 반환하므로 주의해야 한다.

[##_ImageGrid|kage@uD6fi/btr4DtqLfOa/Jtb0CyBCc5Hn8dgKgOOIN0/img.png,kage@byu46n/btr4w6wnAgJ/ota14st9A2spdiu7DzMePk/img.png|data-is-animation="false" data-origin-width="324" data-origin-height="176" data-filename="스크린샷 2023-03-20 오후 1.10.50.png" style="width: 33.4705%; margin-right: 10px;" data-widthpercent="33.86",data-is-animation="false" data-origin-width="302" data-origin-height="84" data-filename="스크린샷 2023-03-20 오후 1.11.02.png" style="width: 65.3668%;" data-widthpercent="66.14"|_##]

#### **📌 지수 연산자**

**지수 연산자(\*\*)** 는 좌항의 피연산자를 밑(base)으로, 우항의 피연산자를 지수(exponent)로 거듭 제곱하여 숫자 값을 반환한다.

음수를 거듭제곱의 밑으로 사용해 계산하려면 괄호로 묶어야 한다.

[##_ImageGrid|kage@xtpXT/btr4AVPdyuY/MKU29KQUN9JnMFZodcHFAk/img.png,kage@uir63/btr4LIO3kaV/fjuPVolhmJK3aqy2k0nTnK/img.png|data-is-animation="false" data-origin-width="290" data-origin-height="306" data-filename="스크린샷 2023-03-20 오후 3.44.07.png" data-widthpercent="14.96" style="width: 14.7894%; margin-right: 10px;",data-is-animation="false" data-origin-width="1368" data-origin-height="254" data-filename="edited_스크린샷 2023-03-20 오후 3.44.48.png" data-widthpercent="85.04" style="width: 84.0478%;"|_##]

지수 연산자는 할당 연산자와 함께 사용할 수 있다.

[##_Image|kage@ADIwM/btr415vbQaP/IJ8cNPjiZoS1JMN314NxR0/img.png|CDM|1.3|{"originWidth":230,"originHeight":106,"style":"alignCenter","filename":"스크린샷 2023-03-20 오후 3.46.39.png"}_##]

지수 연산자가 도입되기 전에는 **Math.pow 메서드** 를 사용했다. 지수 연산자는 우결합성을 갖기 때문에 연속해서 지수 연산을 하는 경우 Math.pow 메서드보다 가독성이 좋다.

[##_Image|kage@b7AsF1/btr40SDbyi9/wKOWyEgyDuCBTqNfTw9fX0/img.png|CDM|1.3|{"originWidth":450,"originHeight":222,"style":"alignCenter","filename":"edited_스크린샷 2023-03-20 오후 3.49.00.png"}_##]

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

[##_ImageGrid|kage@T6SCZ/btr4LHP9VNT/DU5BHtXP4V4kyQ5jp1SkMk/img.png,kage@bu38jB/btr4Dr8eXDF/Irwknmjjlxnu9LD24TogRK/img.png,kage@Iep6M/btr4WGXlQb0/WEvp4WDQr3MvflEbGNkwJ0/img.png|data-is-animation="false" data-origin-width="264" data-origin-height="156" data-filename="스크린샷 2023-03-20 오후 3.59.06.png" data-widthpercent="24.43" style="width: 23.8665%; margin-right: 10px;",data-is-animation="false" data-origin-width="304" data-origin-height="110" data-filename="스크린샷 2023-03-20 오후 3.59.19.png" style="width: 38.9754%; margin-right: 10px;" data-widthpercent="39.9",data-is-animation="false" data-origin-width="410" data-origin-height="166" data-filename="스크린샷 2023-03-20 오후 3.59.27.png" style="width: 34.8325%;" data-widthpercent="35.67"|_##]

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
