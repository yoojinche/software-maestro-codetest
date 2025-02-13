# [Silver III] 순열 사이클 - 10451

## 📍 [문제 및 풀이 코드 링크](https://github.com/Jinyshin/Algorithm/tree/main/%EB%B0%B1%EC%A4%80/Silver/10451.%E2%80%85%EC%88%9C%EC%97%B4%E2%80%85%EC%82%AC%EC%9D%B4%ED%81%B4)

## 📍 풀이 방법

- 구해야 하는 것은 만들어지는 그래프의 개수 -> 그래프를 List에 저장하고 그 size()를 출력해야겠다 생각
- 처음에 입력받는 순열은 인덱스로 접근해야겠다고 생각함 -> 1-based indexing을 활용하기 위해 int[N + 1] 크기 배열 선언
- 순열의 각 원소들 순회하면서 그래프를 찾음
  - visited 배열 활용
  - graph(사이클)찾기(dfs); 키(인덱스)->밸류 -> 그 밸류를 키 -> 다시 밸류찾기

### 🌟 개선

- 그래프가 어떻게 구성되었는지는 중요하지 않고, 그래프가 몇개인지만 중요한 문제이므로 그래프를 저장하지 않는 방식으로 코드를 변경함
- dfs 탐색을 완료하면 cycle 개수 ++;
- 또한, contains() 메서드를 사용하는 부분을 visited 배열을 확인하도록 코드를 변경할 수 있다.
