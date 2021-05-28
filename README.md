# 로또 게임

- [1. 과제 설명](#1-과제-설명)
- [2. 기능 목록](#2-기능목록)
    - [2.1. 난수 생성기](#21-난수-생성기-생성)
    - [2.2. LottoNumber 생성](#22-LottoNumber-생성)
    - [2.3. Lotto 생성](#23-Lotto-생성)
    - [2.4. Money 클래스 생성](#24-Money-클래스-생성)
    - [2.5. 로또 당첨 갯수 관련 Enum 클래스 추가 ](#25-ENUM-클래스-생성)
    - [2.6. 당첨 로또 관련 보너스 볼 추가 ](#25-보너스-볼-추가)
    - [2.7. 로또 게임 Play ](#25-로또-게임-Play)

---

### 1. 과제 설명

* 로또 요구사항을 파악한다.
* 요구사항에 대한 구현을 완료한 후 자신의 github 아이디에 해당하는 브랜치에 Pull Request(이하 PR)를 통해 코드 리뷰 요청을 한다.
* 코드 리뷰 피드백에 대한 개선 작업을 하고 다시 PUSH한다.
* 모든 피드백을 완료하면 다음 단계를 도전하고 앞의 과정을 반복한다.


### 2. 기능 목록

구현하는 기능 목록은 아래와 같다.



#### 2.1. 난수 생성기

- 중복이 없는 6개의 난수를 만드는 `RandomLottoNumGenerator` 클래스를 생성한다.
- TreeSet 자료구조를 통해 6개가 만들어지면 종료한다.


#### 2.2. LottoNumber 생성

- 로또 숫자가 1~45 까지의 값인지 확인하는 원시 값을 포장한 `LottoNumber` 클래스를 생성한다.
- 1~45 사이의 숫자가 아니라면 `inValidLottoNumberException` Exception을 throw 한다.


#### 2.3. Lotto 생성

- 6자리의 로또 숫자를 가진 일급 컬렉션 `Lotto` 클래스를 생성한다.
- `checkDuplicate` 메서드를 통해 중복된 숫자가 만들어지면 `DuplicatedNumberException` 을 throw 한다.



#### 2.4. Money 클래스 생성

- 입력 금액에 1000원이 넘어서 로또를 살 수 있는지 check 한다.
- 1000원이 되지 않는다면 `NotEnoughInitMoneyException` 을 throw 한다.

```
구입금액을 입력해 주세요.
14000
14개를 구매했습니다.
```

#### 2.5. 로또 당첨 갯수 관련 Enum 클래스 추가

- 3~6개의 카운트를 관리하며 `valueOf` 메서드를 통해 몇개를 맞췄을 때 몇등인지 알 수 있다.


```
1등: 6개 일치, 2,000,000,000원
                * 2등: 5개 일치, 보너스 번호 일치, 30,000,000원
                * 3등: 5개 일치, 1,500,000원
                * 4등: 4개 일치, 50,000원
                * 5등: 3개 일치, 5,000원
```

#### 2.6 로또 보너스 볼 추가

- 당첨 로또 번호와 추가로 보너스 볼 하나를 뽑게 된다.
- 이때 추가 보너스 볼은 당첨 로또 번호와 중복 되어서는 안된다.


#### 2.7. 로또 게임 Play 

- 로또 게임을 진행 할 수 있도록 `LottoGame` 클래스를 생성하고 해당 Money / 1000 만큼의 로또를 구매 한다.




