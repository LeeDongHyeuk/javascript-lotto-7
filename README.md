# javascript-lotto-precourse

## 로또

**로또**는 사용자가 입력한 로또 구입 금액과 당첨 번호에 따라 로또를 발행하고 당첨 내역 및 수익률을 알려주는 간단한 콘솔 기반 프로그램입니다.

## 주요 기능

- **금액에 따른 로또 발행** - 구입 금액에 따라 로또를 자동으로 발행합니다.
- **당첨 내역 확인** - 사용자가 발행한 로또 번호와 당첨 번호를 비교하여 1등부터 5등까지의 당첨 내역을 제공합니다.
- **수익률 계산** - 구입 금액 대비 수익률을 계산하여 출력합니다 (소수점 2자리까지 반올림).

## 기능 목록

### 입력

1. **로또 구입 금액 입력**

- **예외 처리**
  - 금액이 숫자로만 구성되어 있는지 확입합니다.
  - 1000원 단위인지 확입합니다.
  - 금액이 안전한 정수 범위인지 확인합니다.

2. **당첨 번호 입력**

- 사용자로부터 쉼표(,)로 구분한 당첨 번호를 입력받습니다.
  - **예외 처리**
    - 당첨 번호가 숫자로만 구성되어 있는지 확인합니다.
    - 당첨 번호가 1부터 45까지의 범위인지 확인합니다.
    - 번호가 정확히 6개인지 확인합니다.
    - 중복된 번호가 없는지 확인합니다.

3. **보너스 번호 입력**

- 당첨 번호 외에 보너스 번호를 입력받습니다.
  - **예외 처리**
    - 보너스 번호가 숫자로만 구성되어 있는지 확인합니다.
    - 보너스 번호가 1부터 45까지의 범위인지 확인합니다.
    - 보너스 번호가 당첨 번호와 중복되지 않는지 확인합니다.

### 발행 기능

- 입력받은 로또 구입 금액에 따라 로또를 발행합니다(1장당 1000원).
  - **예외 처리**
    - 같은 번호로만 구성된 로또가 있는지 확인합니다.
- 발행한 로또 수량과 각 로또 번호를 오름차순으로 정렬하여 출력합니다.

### 당첨 내역 확인 기능

- 발행된 로또 번호와 당첨 번호를 비교하여 1등부터 5등까지의 당첨 개수를 확인합니다.
- 각 등수별 당첨 개수와 당첨 금액을 콘솔에 출력합니다.

### 수익률 계산 기능

- 구입 금액 대비 수익률을 계산하여 소수점 둘째 자리에서 반올림합니다.
- 수익률을 콘솔에 출력합니다.

## 실행 결과 예시

```
구입금액을 입력해 주세요.
8000

8개를 구매했습니다.
[8, 21, 23, 41, 42, 43]
[3, 5, 11, 16, 32, 38]
[7, 11, 16, 35, 36, 44]
[1, 8, 11, 31, 41, 42]
[13, 14, 16, 38, 42, 45]
[7, 11, 30, 40, 42, 43]
[2, 13, 22, 32, 38, 45]
[1, 3, 5, 14, 22, 45]

당첨 번호를 입력해 주세요.
1,2,3,4,5,6

보너스 번호를 입력해 주세요.
7

당첨 통계
---
3개 일치 (5,000원) - 1개
4개 일치 (50,000원) - 0개
5개 일치 (1,500,000원) - 0개
5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
6개 일치 (2,000,000,000원) - 0개
총 수익률은 62.5%입니다.
```
