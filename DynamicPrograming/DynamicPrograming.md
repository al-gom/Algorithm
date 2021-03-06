# 📌 다이나믹 프로그래밍<br>
## 🔖 메모리를 적절히 사용하여 *수행 시간 효율성을 비약적으로 향상*시키는 방법
### - 이미 계산된 결과(작은 문제)는 별도의 메모리 영역에 저장하여 다시 계산하지 않도록 합니다.
### - 다이나믹 프로그래밍의 구현은 일반적으로 두 가지 방식(탑다운/바텀업)으로 구성됩니다.
### - 완전 탐색을 이용했을 때 시간 복잡도가 매우 비효율적인 문제도 다이나믹 프로그래밍을 사용해 시간복잡도를 비약적으로 줄인다.
### - 동적 계획법이라고도 불리며 동적이라는 것은 일반적으로 자료구조에서 동적할당 즉, 프로그램이 실행되는 도중에 실행에 필요한 메모리를 할당하는 기법을 의미한 것과는 달리 별다른 의미 없이 사용된다.

## 🔖 특정 문제가 다음의 조건을 만족할 때 사용할 수 있다.
### 1. 최적 부분 구조(Optimal Substructure)
    큰 문제를 작은 문제로 나눌 수 있으며 작은 문제의 답을 모아서 큰 문제를 해결할 수 있다.
### 2. 중복되는 부분 문제(Overlapping Subprogram)
    동일한 작은 문제를 반복적으로 해결해야 합니다.

## 🔖 다이나믹 프로그래밍 VS 분할 정복
 - 다이나믹 프로그래밍과 분할 정복은 모두 최적 부분 구조를 가질 때 사용할 수 있다.
   큰 문제를 작은 문제로 나눌 수 있으며 작은 문제의 답을 모아서 큰 문제를
   해결할 수 있는 상황
 - 다이나믹 프로그래밍과 분할 정복의 차이점은 부분 문제의 중복이다.
   다이나믹 프로그래밍 문제에서는 각 부분 문제들이 서로 영향을 미치며 부분 문제가 중복된다.
   분할 정복 문제에서는 동일한 부분 문제가 반복적으로 계산되지 않는다.

## 🔖 분할 정복의 대표적인 예시인 퀵 정렬
#### - 한 번 기준 원소가 자리를 변경해서 자리를 잡으면 그 기준 원소의 위치는 바뀌지 않는다.
#### - 분할 이후에 해당 피벗을 다시 처리하는 부분 문제는 호출하지 않는다.

## 🔖 다이나믹 프로그래밍 문제에 접근하는 방법
#### - 주어진 문제가 다이나믹 프로그래밍 유형임을 파악하는 것이 중요하다
#### - 가장 먼저 그리디, 구현, 완전 탐색 등의 아이디어로 문제를 해결할 수 있는지 검토한다. <br>이후에, 다른 풀이 방법이 떠오르지 않는다면 다이나믹 프로그래밍을 고려한다. <br>작은 문제를 조합해 큰 문제를 해결할 특성을 가지며 부분문제가 중복되는 특성을 가지고 있다고 하면 다이나믹 프로그래밍을 고려해 볼수 있다
#### - 일단 재귀 함수로 비효율적인 완전 탐색 프로그램을 작성한 뒤에 (탑다운) 작은 문제에서 구한 답이 큰 문제에서 그대로 사용될 수 있으면, 코드를 개선하는 방법을 사용한다.
#### - 일반적인 코딩 테스트 수준에서는 기존 유형의 다이나믹 프로그래밍 문제가 출제되는 경우가 많다.

### 🔎 단순 재귀 함수로 피보나치 수열을 해결하면 지수 시간 복잡도를 가지게 된다. <br>예를 들어, 6번째 값을 호출할 때, 2번째 값이 5번이나 호출된다. <br>재귀 함수를 사용한다면 시간 복잡도는 O(2^N)으로 fibo(30)을 한다면 10억 가량의 연산을 수행해야한다.

## 🔖 피보나치 수열
- 피보나치 수열은 다음과 같은 형태의 수열이며, 다이나믹 프로그래밍으로 효과적으로
  계산할 수 있습니다.
  1 1 2 3 5 8 13 21 34 55 89 ...
- 프로그래밍에서는 이러한 수열을 배열이나 리스트를 이용해 표현합니다.

## 🔖 메모이제이션
#### - 다이나믹 프로그래밍을 구현하는 방법 중 하나이다.
#### - 한 번 계산한 결과를 메모리 공간에 메모하는 기법이다. <br>같은 문제를 다시 호출하면 메모했던 결과를 그래도 가져온다.
#### - 값을 기록해 놓는다는 점에서 캐싱이라고도 한다.
#### - 메모이제이션을 이용하는 경우 피보나치 수열 함수의 시간 복잡도는 O(N)이다

## 🔖 탑 다운 VS 바텀 업
#### - 탑다운(메모이제이션) 방식은 하향식이라고도 하며 재귀함수를 이용하며, 바텀업 방식은 상향식이라고도 하고 먼저 계산했던 문제들의 값을 활용해 그다음에 문제도 해결한다.
#### - 다이나믹 프로그래밍의 전형적인 형태는 바텀업 방식이다.
#### - 결과 저장용 리스트는 DP테이블이라고도 부른다.
#### - 엄밀히 말하면 이런 메모이제이션은 이전에 계산된 결과를 일시적으로 기록해 놓는 넒은 개념을 의미한다. <br>따라서 메모이제이션은 다이나믹 프로그래밍에 국한된 개념은 아니며 한 번 계산된 결과를 담아 놓기만 하고 다이나믹 프로그래밍을 위해 활용하지 않을 수 있다.