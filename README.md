# <U>DART STUDY</U>

## **Variable**

- 같은 Scope 안에서 변수는 **재정리**가 불가능하다.
- var 타입은 value값을 보고 **type**을 유추한다.
- print 함수 내부에서 $x <- $ 사용 시 x의 변수 값을 출력한다.
- dynamic type을 사용하면 value의 값을 보고 type을 **고정**한다.
- type 옆에 '?'를 붙이면 해당 변수는 **nullable** 상태이다.

* const와 final의 차이
* const는 build time의 값을 알아야 사용이 가능하다.
* final은 build time과 상관없이 사용 가능하다.

- x ??= y <- 해당 변수가 **null인 상태**이면 y로 값을 변경한다.
- x is type <- 해당 변수가 type과 비교하여 true, false를 반환한다.

#

## **List**

```dart
List<type> {변수명} = [value, value, ...];
```

#

## **Map**

```dart
Map\<type, type> {변수명} = {
    key : value,
    key : value,
    ...
};
```

- key,value 추가 함수
  ```dart
  {변수명}.addAll() // 함수 이용
  {변수명}[key] = value // 직접 추가
  ```

#

## **Set**

```dart
Set<type> {변수명} = {
    value,
    value,
    ...
};
```

- value가 중복으로 입력이 되거나 추가가 되어도 내부에서 중복을 처리한다.

#

## **For**

- for each문:

  ```dart
  for(type {변수명1} in {변수명2})
  ```

- {변수명<sub>2</sub>}의 값을 {변수명<sub>1</sub>}에 차례대로 값을 넘겨준다.

#

## **Enum**

```dart
enum {변수명} {
    지정 type 이름,
    지정 type 이름,
    ...
}
```

- 자신이 직접 type의 이름을 정하여 정확한 단어 비교(구분)를 한다.

#

## **Function**

```dart
type {함수명}(parameters) {}
```

- positional parameter
  - parameters 방식
  ```dart
  ({ type {변수명}, type {변수명}, ... })
  ```
  ```dart
  ({ type {변수명}, [type {변수명}, type {변수명}], ... })
  ```
  - [] <- optional parameter

* named paramter
  - parameters 방식
  ```dart
  {함수명}({
      required type {변수명},
      type {변수명}
  })
  ```
  - required가 없는 것 <- optional parameter

- optional parameter: 해당 parameter가 값을 받지 않아도 된다.

#### arrow function

```dart
{함수명} (parameters) => - code -
```

- code는 반환되는 식을 작성한다.

#

## **Typedef**

- signature에 부합하는 함수들을 arrow 함수로 만들어서 사용한다.

```dart
typedef {이름} = type Function (paramters); //signature

type {함수명1}(paramters) => - code -
type {함수명2}(paramters) => - code -
type {함수명3}(paramters, {이름} {변수명}) {
    return {변수명} (parameters);
}
```

- signature의 type과 parameters는 모두 같아야 한다.
- {함수명<sub>3</sub>}을 통해 {함수명<sub>1</sub>}, {함수명<sub>2</sub>} 중 무엇을 사용할 지 선언한다.
