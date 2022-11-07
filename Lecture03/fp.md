# <U>Functional Programming(FP)</U>

## **Conversion**

- Map type으로 변환
  ```dart
  {변수}.asMap();
  ```
- Set type으로 변환
  ```dart
  {변수}.toSet();
  ```
- List type으로 변환
  ```dart
  {변수}.toList();
  ```

#

## **Built-in Function**

## map

- 기본 방식
  ```dart
  {변수}.map((paramter) => {
      return - code -
  });
  ```
- arrow 방식
  ```dart
  {변수}.map((paramter) => - code -);
  ```
  Collection type(List, Map, Set, ...) 내부 value 및 key 관리

## where

- 기본 방식
  ```dart
  {변수}.where((parameter) => {
      - code -
  });
  ```
- arrow 방식
  ```dart
  {변수}.where((paramter) => - code -);
  ```
  Collection type 내부 value 및 key 일치값 찾기

## reduce

- 기본 방식
  ```dart
  {변수}.recude((prev, next) => {
      return - code -
  });
  ```
- arrow 방식

  ```dart
  {변수}.reduce((prev, next) => - code -);
  ```

  초기 prev, next는 첫번째 index와 두번째 index 값이 들어온다.  
  이후 prev는 return 값이 next는 세번째 index부터 차례로 들어온다.

  <U>{변수}의 type과 return type이 같아야 한다.</U>

## fold

- 기본 방식
  ```dart
  {변수}.fold<type>(start, (prev, next) => {
      return - code -
  });
  ```
- arrow 방식

  ```dart
  {변수}.fold<type>(start, (prev, next) => - code -);
  ```

  reduce와 같은 구조

  reduce와 다르게 type의 변경이 가능하고 start parameter로 시작 기준을 정할 수 있다.
