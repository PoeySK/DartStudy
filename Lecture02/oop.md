# <U>Object Oriented Programming(OOP)</U>

## **Class**

- Instance 생성시 <span style="color: yellow">new</span> 키워드 사용하지 않아도 된다.
- constructor
  ```dart
  class x {
      type value1;
      type value2;
      x(this.value1, this.value2); // 생성자 선언
  }
  ```
- named constructor
  ```dart
  class x{
      type value1;
      type value2;
      x.{이름}(type valu01, type value02)
          : this.value1 = value01,
          this.value2 = value02;
  }
  ```
  - {이름}이라는 생성자에 이름을 지정해준다.
  - Instance를 선언할 때 생성자의 이름을 넣어 생성한다.

#

## **Immutable Programming**

- class 내부의 변수를 fianl, const로 선언해준다.
  - 함부로 변경을 할 수 없도록 한다.

#

## **Const Constructor**

- const로 선언한 Instance가 2개 존재할 때, 내용이 같으면 그 Instance를 비교하면 같은 것으로 인지한다.
- const로 선언하지 않으면 다른 것으로 인지한다.

#

## **Getter/Setter**

- Getter
  ```dart
  type get {이름} {
      return - code -;
  }
  ```
- Setter
  ```dart
  type set {이름}(parameter) {
      - code -
  }
  ```
  - parameter의 값은 무조건 하나만 가능하다.

#

## **Private**

- 변수, 함수, class 등 선언한 이름 앞에 '\_'를 추가해주어 private 형태로 선언한다.

  - ex)

    ```dart
    int number = 1; // not private variable
    int _number = 2; // private variable

    class Test {} // not private class
    class _Test {} // private class

    ...
    ```

#

## **Inheritance**

- 부모 class가 named constructor인 경우

  ```dart
  class {이름} extends {부모 class 이름} {

      - 부모 class 코드 -

      {이름}(

          - 부모 class 변수 -

      ) : super(
          value : value,
          value : value,
          ...
      )
  }
  ```

- 부모 class가 named constructor가 아닌 경우

  ```dart
  class {이름} extends {부모 class 이름} {

      - 부모 class 코드 -

      {이름}(

          - 부모 class 변수 -

      ) : super(변수);
  }
  ```

#

## **Interface**

- Dart 언어에서는 interface 키워드가 따로 없으므로 abstract class 키워드를 이용해 interface를 이용한다.
  ```dart
  abstract class {이름}{
      - code -
  }
  ```

#

## **Generic**

- Dart 언어에서도 generic 방식을 적용할 수 있다.
