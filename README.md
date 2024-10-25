# java-racingcar-precourse

### 추가적인 기능 요구사항

- 자동차 이름은 쉼표(,)를 제외한 모든 문자를 사용할 수 있다.
- 자동차 이름은 공백을 포함할 수 있다.
- 자동차 이동 횟수는 자연수이어야 한다.

### RacingCarApplication

- [ ]  InputView, ProgressView, OutputView, Cars 객체를 생성한다.
- [ ]  생성한 객체를 주입하여 RacingCarController 객체를 생성한다.
- [ ]  초간단 자동차 경주 게임을 시작한다.

### **View**

- **InputView**
    - [x]  자동차 이름 입력 안내 문구를 출력한다.
        - `경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)`
    - [x]  사용자로부터 경주할 자동차 이름을 입력받는다.
    - [x]  자동차 이동 횟수 입력 안내 문구를 출력한다.
        - `시도할 횟수는 몇 회인가요?`
    - [x]  사용자로부터 자동차 이동 횟수를 입력받는다.
    - [x]  자동차 이동 횟수의 유효성을 검사한다.
        - [x]  자동차 이동 횟수가 공백이 아닌지 검사한다.
        - [x]  자동차 이동 횟수가 자연수인지 검사한다.
- **ProgressView**
    - [ ]  최초 차수의 진행 현황을 출력하기 전에 `실행 결과` 라는 문구를 출력한다.
    - [ ]  매 차수마다 자동차들의 이동거리를 출력한다.
      ```
      pobi : --
      woni : ----
      jun : ---
      ```
- **OutputView**
    - [ ]  우승자 안내 문구를 출력한다.
        - [ ]  공동 우승자가 있을 시에는 쉼표+공백으로 구분하여 출력한다.
        - `최종 우승자 : pobi, jun`

### **Model**

- **Car**
    - [x]  생성자로 자동차 이름을 저장한다.
        - [x]  자동차 이름이 5자 이하인지 검사한다.
    - [x]  자동차를 전진시킨다.
        - [x]  자동차 전진 조건을 확인한다.
            - [x]  0부터 9 사이의 무작위 값을 구한다.
            - [x]  무작위 값이 4 이상인지 확인한다.
        - [x]  자동차를 1 만큼 전진시킨다.
- **Cars**
    - [x]  자동차를 저장한다.
    - [ ]  자동차들을 전진시킨다.
    - [ ]  가장 멀리 이동한 자동차를 계산한다.

### Controller

- **RacingCarController**
    - [ ]  InputView를 통해 안내 문구를 출력한다.
    - [ ]  InputView를 통해 경주할 자동차 이름을 입력받는다.
    - [ ]  입력받은 자동차 이름대로 자동차들을 생성하고 저장한다.
    - [ ]  InputView를 통해 자동차 이동 횟수를 입력받는다.
    - [ ]  자동차 이동 횟수 만큼 경기를 진행한다.
        - [ ]  Cars를 통해 자동차들을 전진시킨다.
        - [ ]  ProgressView로 자동차 정보들을 전달하여 진행 상황을 출력한다.
        - 이동 횟수만큼 위 동작을 반복한다.
    - [ ]  Cars를 통해 우승자를 계산한다.
    - [ ]  OutputView를 통해 우승자를 출력한다.