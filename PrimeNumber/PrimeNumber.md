# 📌 소수 판별 알고리즘
- 소수란 1보다 큰 자연수 중에서 1과 자기 자신을 제외한 자연수로 나누어 떨어지지 않는 자연수이다.
- 코딩테스트에서는 어떠한 자연수가 소수인지 아닌지를 판별해야 하는 문제가 자주 출제됩니다.
- 예) 2부터 x-1까지 모든 자연수에 대해 연산을 수행하므로 시간복잡도는 O(x)이다.

# 📌 약수의 성질
- 모든 약수가 가운데 약수를 기준으로 곱셈 연산에 대해 대칭을 이룬다.
- 예를 들어, 16의 경우 약수가 1,2,4,8,16인데 4를 기준으로 앞 뒤로 대충을 이룬다.
- 따라서 특정한 자연수의 모든 약수를 찾을 때 가운데 약수(제곱근)까지만 확인하면 된다.
- 약수의 성질을 이용한 알고리즘의 시간 복잡도는 O(N^1/2)이다.
# 📌  에라토스테네스의 체 알고리즘
### 🔖 다수의 소수 판별
    - 특정한 수의 범위 안에 존재하는 모든 소수를 찾을 때는 에라토스테네스의 체 알고리즘을 사용한다.
    - 범위를 설정하기 위해 N이라는 수를 설정하는데 N보다 작거나 같은 모든 소수를 찾을 수 있다.

### 🔖 동작 과정
    1. 2부터 N까지의 모든 자연수를 나열한다.
    2. 남은 수 중에서 아직 처리하지 않은 가장 작은 수 i를 찾는다. (i = 소수)
    3. 남은 수 중에서 i의 배수를 모두 제거한다.(i는 제거한다)
    4. 더 이상 반복할 수 없을 때까지 2번과 3번을 반복한다.

- 에라토스테네스의 체 알고리즘의 시간 복잡도는 사실상 선형 시간에 가까울 정도로 매우 빠르다
    `시간 복잡도 : O(NloglogN)`
  
- 에라토스테네스의 체 알고리즘은 다수의 소수를 찾아야 하는 문제에서 효과적으로 사용된다.
    - 하지만 각 자연수에 대한 소수 여부를 저장해야 하므로 메모리가 많이 필요하다
    - 10억이 소수인지 아닌지 판별해야 할때 에라토스테네스의 체를 사용할 수 있을까요?