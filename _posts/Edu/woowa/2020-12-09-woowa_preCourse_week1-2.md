---
title: 우아한 테크 프리코스 1-2 주차 회고록
date: 2020-12-09-22:00
categories:
- Edu

tags:
- 우아한 테크 코스
- 교육

photos: 
- /post_images/woowa-logo.jpg

---

## 우아한 테크 코스 1,2 주차 회고
> 짧은 기간이지만 성장함을 느낄수 있던 과정

---

## 우아한 테크코스에 대한 개인적인 느낌
> 자기 주도적인 학습을 경험하게 해준다.

* `자기 주도적인 학습을 경험`? 굉장히 추상적이게 들릴 수 있다.
* 우아한 테크 코스에서는 어느 딱 정답이 정해진 답을 던져 주지 않는다.
    * 제약 조건을 주고, 그것을 지원자들이 스스로 해결 하도록 유도한다.
    * 이 `제약 조건`을 해결하기 위해서 `자기 주도적`으로 정보를 찾아가면서 공부를 해야한다.
        * 하지만 너무 막연하지는 않게 키워드를 같이 던져 준다.
        * 또한 구글링을 통해서 충분히 해결할 수 있는 수준의 문제를 던져 준다.
            * 그래도 막연하다면 오픈채팅방이나, 카카오톡으로 질문하면 된다!

### 나 같은 사람에게 정말로 필요했던 과정
* 부끄럽지만 나는, 취업을 위한 준비만 하던 사람이었지 **개발자가 되기 위한 준비**를 하고 있던 사람이 아님을 깨닫는 시간이었다.
    * `알고리즘`, `전산학`에 대해서만 공부를 어느정도 해놓았을뿐, 어떤 개발론적인 사고를 가지는 훈련이 거의 되어있지 않은 상태였었다.
* 하지만 이 과정을 통해서 많은 것을 배웠다.
    * 어떻게 설계 해야, 유지보수가 좋을지
    * 어떻게 구현 사람들이 좀 더 내 코드를 편하게 읽을 수 있을지
    * 이러한 고민들을 해보며, `개발 적인 사고력`을 향상 시킬 수 있었다고 생각한다.

### 재미
> 일단 무엇보다 재미있었다!

* 미션에서 요구하는 진행 방식과 내 개발 성격과 정말 맞아 떨어졌다.
    * 그래서 일단 **재미**있었다!
* 내가 코딩하는데에 가장 많은 시간을 할애한 `알고리즘 문제 해결` 의 경우에서도 비춰지듯이, 나는 정말 `설계`가 중요하다고 생각하는 사람이다.
    * 2시간동안 1문제를 푼다고 쳤을때, 나의 경우에는 `1시간 30분` 동안 고민, 설계하고 `30분` 동안 구현하는 스타일이다. 키보드에 손을 올리는 시간이 굉장히 적다.
* 우아한 테크 코스에서 주어지는 미션은 이런 설계를 굉장히 중요시 생각해야 한다.
    * 나는 이게 너무 재밌었고, 매번 미션을 시작하기가 두려웠다.
        * 한번 시작하면 시간가는지 모르고 계속하다가, 다음날 일정이 망가지곤 했다 ㅋㅋ..

---

## 2주간 받은 공통 피드백
> 이제 개발적인 이야기를 해보고자 한다. 피드백 받은것들 중 나에게 적용되는 부분들을 짚어봤다.

---

### 기능 목록을 업데이트 하라.
> 살아있는 문서를 만들기 위해서 노력하라.

* 처음부터 완벽하게 정리해야 한다는 부담을 가지기 보다는 구현하면서 문서를 계속 업데이트 하라.
    * 나의 경우, 처음부터 완벽하게 기능구현 목록을 만들어 놓고 구현에 들어가려고 했다.
    * 그것이 좋은 설계이고, 좋은 방식이라고 생각했기 떄문이다.
        * 하지만, 처음부터 완벽하게 기능 구현 목록을 만든다는 것은 **불가능** 하다.
        * 그리고 잘못된 기능 구현 목록에 계속 억지로 맞춰 구현하려고 하니 만족스럽지 못한 결과물이 나왔다.
    * 앞으로는 계속해서 문서를 업데이트 하면서 진행할 예정이다.

---

### 기능 목록 구현을 재검토 하라.

#### 너무 상세하게 적지 않는다.
* 그렇다고 대충 적으라는 이야기가 아니다.
    * 함수 설계와 구현과 같이 너무 상세하게 적을 필요가 없다는것이다.
        * `왜?` 언제든 변경될 수 있으니까!
    * 정상적인 경우도 중요하지만, 예외적인 상황도 기능 목록에 정리한다.
        * 예외 상황은 중간중간에 계속 찾는경우가 많다!, 계속 해서 추가해 나간다.

```c
// 좋은 예시
* 사용자가 입력한 이름을 쉼표 기준으로 분리한다.
* 사용자 이름이 5자 이하인지 확인한다.
..ETC

// 나의 경우
* ~ 하는 메소드 `뭐시기`
* ~ 하는 경우인가?
    * 맞다면 return true
    * 틀리다면 return false

// 바꾸자!
* 자동차가 4 이상인경우 전진한다.
* 승자인지를 확인한다.
```

---

### 값을 하드코딩 하지마라.
* 단순히 출력되는 문자열이 말고도, 기준이 되는 변수를 상수로 만들고 이름을 지어서 처리하라.
    * 재밌는건 1주차떄는 이것을 지켰는데 2주차 때는 놓쳤다. 3주차떄는 절대 놓치지 않는다!

```java
    public void carMove(int randomNum) {
        if (randomNum >= 4) this.position++;
    }

    /*
        4를 기준으로 움직임을 판단하는 경우이다.
        이 경우 4라는 값을 상수화 시키는게 좋다!
    */

    public final static int MOVE_BASE_POINT = 4;

        public void carMove(int randomNum) {
        if (randomNum >= MOVE_BASE_POINT) this.position++;
    }
```

---

### java api를 적극 활용한다.
> 메소드를 구현중 이미 제공되는 기능인지 `검색` 해보자!


```java
    private void printGameResult() {
        StringBuilder resultMsg = new StringBuilder(Constants.RACING_GAME_RESULT);
        int maxPosition = getMaxPosition();

        for (Car car : carList) {
            if (car.isImWinner(maxPosition)) {
                resultMsg.append(" ").append(car.getName()).append(",");
            }
        }
        System.out.println(resultMsg.substring(0, resultMsg.length() - 1));
    }
```

* 나의 경우 최종 결과를 출력해야 하는 부분에서 다음과 같이 직접 구현했다.
    * 이름 사이마다 콤마 `,` 가 있어야 하는 조건을 만족시키기 위해, 이름을 출력하고 항상 콤마를 붙인뒤 출력 직전에 콤마를 제거하였다.

<br>

```java
    public static void main(String[] args) throws IOException {
        List<String> winnersList = Arrays.asList("jw", "ys");
        String [] winnersArray = {"jw", "ys"};

        System.out.println(String.join(",", winnersList));  // jw,ys
        System.out.println(String.join("|", winnersArray)); // jw|ys
    }
```

* 하지만 다음과 같이 간단하게 구현이 가능했다.
    * java 8 부터 추가된 `String` 에서 join 메소드가 존재했다!
    * [잘 정리된 블로그](https://tourspace.tistory.com/8)를 보고 바로 학습했다.
* java가 주언어가 아니라, 필요한 문법만 그때그때 찾아서 쓰다보니 이런 기능이 있는지도 몰랐다.
    * 언어에 대해서 조금 더 깊게 공부할 필요성이 느껴진다.
    * `자바의 정석` 사놓은거 매일 조금씩이라도 읽자!

---

### 배열대신 collection을 사용하라.
> C++ 사용시 배열보다 벡터를 사용하던것처럼

* 이미 잘 만들어진 `api` 를 알고, 사용하는 것도 실력이다.

```java

// 이것보다는
public int[] answerNumbers =  new int[Constants.NUMBER_COUNT];

// 이렇게 collection으로 만들어서 쓰자.
public ArrayList<Integer> answerNumbers = new ArrayList<>(Constants.NUMBER_COUNT);

```


---

### 객체에 메시지를 보내라.
> 객체에서 get하고 판단하지말고, 객체가 판단하게 하라!

* 1주차때는 놓친 부분이지만 2주차때는 객체지향 생활 체조원칙이라는것을 보고 적용했다!

```java
    public void carMove(int randomNum) {
        if (randomNum >= MOVE_BASE_POINT) this.position++;
    }
```

---

### 인스턴스의 수를 줄이기 위해 노력한다.
> 불필요한 필드가 있는지를 확인하자.

* 굳이 없어도 되는것을 만들어서 관리하지말자.
    * 복잡도가 증가하고, 버그 발생 가능성이 높아진다.
    * `List` 안에 있는 원소들 중 어느 기준으로 선별된 다른 `List` 가 필요할경우, 그 `List`를 굳이 만들어서 관리하지말자
        * 한 메소드를 통해 기존 `List`를 탐색하고, 리턴값을 `List`로 해서 돌려주자!

---

### 비즈니스 로직과 UI 로직을 분리하라.
> 한클래스에서 두개의 로직을 담당하지 않게 하라!

* 내가 제일 놓치고 있던 부분이다.
* 내가 2주차때 제출한 소스의 일부분을 다시보자.


```java
public class Car {
    private final String name;
    private int position = 0;

    public Car(String name) {
        this.name = name;
    }

    // 추가 기능 구현
    public void carMove(int randomNum) {
        if (randomNum >= 4) this.position++;
    }

    public void printCurStatus() {
        System.out.print(this.name + " : ");
        printCurMovement();
        System.out.println();
    }

    private void printCurMovement() {
        for (int i = 0; i < this.position; ++i) {
            System.out.print('-');
        }
    }
}
```

* `Car` 클래스에서 차의 움직임과, 차의 현재 상태를 출력하는것을 둘다 처리하고 있다.
    * 이것은 `SOLID` 에서 `S`인 단일 책임 원칙을 위반한 것이다!
    * 따로 분리해주어야 한다.

* 그렇다면 어떻게 해결할 수 있을까?
    * 클래스를 분리한다!
        * 보여주는 부분을 `View` 용 클래스로 다시 만들어서 관리하자.

* 다음 미션에서는 `MVC 패턴을` 적용해 보려고한다.
* 두개의 링크를 통해서 학습했다.
    * https://hanee24.github.io/2018/02/14/what-is-mvc-pattern/
    * https://hodol.dev/posts/%EC%84%B8%EC%83%81%EC%97%90%EC%84%9C-%EC%A0%9C%EC%9D%BC-%EC%89%AC%EC%9A%B4-MVC-%ED%8C%A8%ED%84%B4

---

## 글을 마치며

### PR을 보면 분명 나보다 잘하시는 분들이 수두룩하다.
* 이런분들을 보며, `내가 여기에 최종 합격할 수 있을까?` 라는 걱정을 단 한번도 하지 않았다면 거짓말일 것이다.
* 하지만 내가 부족하다는것은 앞으로 더 성장할 수 있는 기회가 열려 있다고 생각한다.

### 반복하지만, 일단 `재미`가 있으니 괜찮다!
* 최종 합격하지 못해도 괜찮다. 일단 `재미`가 있었으니까.
* 남과 비교하며 고통 받을 시간에, 미션을 해결하면서 얻는 `재미` 를 좀 더 느끼는 시간을 가지고, 그 이전보다 성장한 나를 보면서 뿌듯해 하고 싶다.

### 우아한 테크코스의 리더 `박재성` 님 께서 이런말을 해주셨다.
> 이 시간이 고통이 아니라 즐거운 시간이기를 기대해 봅니다.

* `피할수 없는 고통은 즐겨라` 라는 말이 있다.
    * 나는 이말을 좀더 바꿔서 이야기 하고 싶다.
    * `피할수 없는 고통속에서 또다른 즐거움` 를 찾아라!