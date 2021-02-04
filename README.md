# java-racingcar
자동차 경주 게임 미션 저장소

## 우아한테크코스 코드리뷰
* [온라인 코드 리뷰 과정](https://github.com/woowacourse/woowacourse-docs/blob/master/maincourse/README.md)

## 기능 구현 목록
- 쉼표(,) 또는 콜론(:)을 구분자로 가지는 문자열을 전달하는 경우, 구분자를 기준으로 분리한 각 숫자의 합을 반환
  - 쉼표와 콜론을 구분자로 가지는 문자열인 경우, 구분자를 기준으로 분리한 각 숫자의 합을 반환 (예 : "1,2:3" => 6)
  - 빈 문자열("")인 경우, 0을 반환 (예 : "" => 0)
  - null을 전달하는 경우, 0을 반환 (예 : null => 0)
- 커스텀 구분자는 문자열 앞부분의 “//”와 “\\n” 사이에 위치하는 문자를 커스텀 구분자로 사용한다.
- 문자열 계산기에 숫자 이외의 값 또는 음수를 전달하는 경우 RuntimeException 예외를 throw한다. 단, 커스텀 구분자는 제외.

### 예와사항
- 음수를 전달하는 경우
- 숫자 이외의 값을 전달하는 경우

### 역할
- 문자열 전달 담당 - String 받아서 다른 객체에게 넘겨준다.
- 문자열 분리 담당 - String "," ":" 기준으로 분리한다.
- 문자열 계산 담당 - String 을 더한다.
- 커스텀 구분자 검사 당담? - 검사하고 구분자를 전달
- 예외를 찾아내는 검사 담당 -  "//-\n1,3-6"