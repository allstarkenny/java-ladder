# 사다리 게임

## Step1 자바8 스트림, 람다, Optional
* [X] Lambda
* [X] Stream
* [X] Optional

## Step2 사다리(생성)

### 기능 요구사항
* 사다리 게임에 참여하는 사람에 이름을 최대5글자까지 부여할 수 있다. 사다리를 출력할 때 사람 이름도 같이 출력한다.
* 사람 이름은 쉼표(,)를 기준으로 구분한다.
* 사람 이름을 5자 기준으로 출력하기 때문에 사다리 폭도 넓어져야 한다.
* 사다리 타기가 정상적으로 동작하려면 라인이 겹치지 않도록 해야 한다.
* |-----|-----| 모양과 같이 가로 라인이 겹치는 경우 어느 방향으로 이동할지 결정할 수 없다.

### 프로그래밍 요구사항
* 자바 8의 스트림과 람다를 적용해 프로그래밍한다.
* 규칙 6: 모든 엔티티를 작게 유지한다.

### 파생 요구사항(설계)
* [ ] User
    * [X] 이름 길이는 최대 5자(이름에 대한 정상 포멧 검증)
* [ ] Users
    * [ ] 초기 위치(?)
    * [X] List<User>
* [ ] RawInputParser
    * [X] ,로 인풋 분리 기능 `String -> <List>String`
* [ ] VerticalLine
    * [X] height > 0
    * [ ] 가로 선 생성 조건 존재
* [X] Enum 으로 Left, Right, NoHorizontalLine
* [ ] Ladder
    * [ ] VerticalLine 의 묶음
        * [ ] Line 의 갯수는 User 수와 동일
    * [ ] 초기 위치 -> 최종 위치 계산
* [ ] ResultView
* [ ] InputView


## 진행 방법
* 사다리 게임 게임 요구사항을 파악한다.
* 요구사항에 대한 구현을 완료한 후 자신의 github 아이디에 해당하는 브랜치에 Pull Request(이하 PR)를 통해 코드 리뷰 요청을 한다.
* 코드 리뷰 피드백에 대한 개선 작업을 하고 다시 PUSH한다.
* 모든 피드백을 완료하면 다음 단계를 도전하고 앞의 과정을 반복한다.

## 온라인 코드 리뷰 과정
* [텍스트와 이미지로 살펴보는 온라인 코드 리뷰 과정](https://github.com/nextstep-step/nextstep-docs/tree/master/codereview)
