# Daily



### 2020_12_28

1. BOJ_1463
   - 주의사항: 딱히 없음
2. BOJ_9251 (LCS)
   - 주의사항
     - 각각의 문자열에서 문자가 동시에 추가되는 상황으로 코드를 짜야한다



### 2020_12_29

1. BOJ_1003
   - 주의사항
     - 언제나 인덱스 조심



### 2020_12_30

1. BOJ_1756
   - 탐색은 이분탐색을 항상 염두해두자
   - loop로만 구현 => recursion으로 해보기
2. BOJ_10434
   - 에라토스테네스의 체
   - 딕셔너리의 in 연산은 O(1) => visited로 활용했음
   



### 2020_12_31

1. BOJ_2805
   - 이분탐색은 O(logN) 이므로 탐색중간에 for문이 있어도 N * log N으로 가능
2. BOJ_1654
   - BOJ_2805와 유사한 문제
   - 특정값이 아닌 이상, 이하를 찾는 경우 리턴할 변수를 따로 설정해놔야함



### 2021_01_01

1. BOJ_10815
   - 단순한 탐색 문제
   - 이진 탐색(1280ms)보다 딕셔너리(592ms)를 이용한 것이 더 빨랐음
     - in 연산은 BOJ_10434 활용한 것 처럼 O(1) => 해시맵
     - 이진 탐색과 딕셔너리를 언제 사용해야 하는지 생각해서 사용하기
2. BOJ_2110
   - 잘못된 항목을 binary search 해서 계속 틀림
   - binary search에서 시간적 여유가 생긴다 => 조금은 무식한 방법을 사용해도 된다
3. BOJ_1790
   - 이진탐색 카테고리 안에 있었지만 그냥 푸는게 나을거 같아서 품
   - 이진탐색으로 다시 풀어볼 것



### 2021_01_02

1. BOJ_1764
   - 단순히 값이 있냐 없냐인 문제 => 딕셔너리를 사용해봤으나 문제 없음
2. BOJ_2512
   - 나무자르기, 랜선자르기 문제와 같음
3. BOJ_1789
   - 이진 탐색은 단순히 탐색에 사용
   - 애드혹 느낌



### 2021_01_03

1. BOJ_3079
   - 이분탐색 단독 문제
   - BOJ_2100, 2805, 2100, 2512 문제와 거의 같음



### 2021_01_04

1. BOJ_2343
   - 시간을 binary search 로 log n으로 탐색
   - 그 시간에 대해서 가능성을 n으로 탐색
   - O(n log n)인 전형적인 문제
   - 주의점: 초기 탐색범위를 잘 설정해야 함 => 좌측범위를 0으로 해서 해맴



### 2021_01_05

1. BOJ_2776
   - 별다른 어려운점은 없었음
   - 다른사람의 코드를 보니 dictionary를 쓴 경우가 더 빨랐음
     BOJ_1754에서 썻던것 처럼 단순히 있다 없다 에서는 딕셔너리가 더 좋은 선택이 될수도 있음
   
2. BOJ_17070

   1. DFS로 풀이 했을때 시간초과가 남
      - 단순히 16 * 16으로 완탐을 해도 되겠다 생각 => O(n^2) 으로 생각
      - 하지만 dfs로 답을 낼경우 방문한 곳을 또 방문해야 하는 문제점이 생김
      - 다시 알고리즘을 살펴보니 각각의 점에서 최소 2가지의 선택지가 있음 => O(2^n)
   2. dp 로 접근
      - 어떤 한점에 도착하는 경우가 그 전에 계산된 결과에 좌우됨
      - 각각의 점을 한번만 방문하면 가능 => O(n^2)

   - dfs, bfs를 사용하기 전에 한번더 생각해보기
   - 이제 시간초과가 나는 경우 풀이법이 숙련되지 않아 나타나는 경우는 많이 없을것 같음 => 시간 초과가 발생하면 아예 처음부터 다시 생각해보기

3. BOJ_17471

   - 처음에 모든 경우를 다해야 하는지 고민
   - 고민하지 말고 n을 보고 바로 시간을 추정해보자



### 2021_01_06

1. BOJ_9095
   - 2개가 아닌 3개의 숫자로 하는 피보나치 문제
2. BOJ_1932
   - 별다른 어려운점 없었음
   - 알고리즘 분류에서 dp로 들어간거라 언제 dp로 풀지 결정하는 방법을 생각해야 할듯



### 2021_01_07

1. BOJ_14425

   1. trie를 dictionary로 구현
      - O(L * M)  L == 사전에 있는 가장 긴 단어, M == 찾을 단어수
      - 밑에 set을 이용한 방법보다 매우 느림
      - 하지만 정확한 단어 검색이 아닌 add?? 와 같은 경우도 검색가능하게 custom 가능함
   2. set을 이용
      - set, dictionary의 경우 in 연산이 O(1)이므로 속도가 빠름
        but, 정확히 일치하는 문자열만 검색가능
   3. trie를 class로 만들어 보기

2. BOJ_5052

   1. trie를 dictionary로 구현
      - 이문제의 경우 정확히 일치하는 것을 찾는것이 아니기 때문에 set 사용 불가
   2. class로 만들어 보자
   3. startwith method 살펴보자

   - 주의사항 

     - 중간에 break를 걸고 나갈 때 input을 다 받지 않은 상태로 함수가 끝나 오류가 발생
       (백준 : 런타임 에러 (NZEC))




### 2021_01_08

1. BOJ_17270

   1. dijkstra를 이용한 풀이(heapq를 이용)
      - 마지막 조건을 순서대로 하는 부분에서 막힘
        문제를 잘 읽어야함
   2. 플로이드 와샬? 알고리즘 공부해보기

   - 다익스트라
     1. 시작점을 hq에 넣어둠
     2. heappop을 통해 hq에 저장된 노드들중 가장 빠르게 갈 수 있는 노드를 선택
     3. 해당 노드를 새로운 시작점으로 다음 노드들을 탐색
     4. 이미 계산된 가중치(dist)와 새롭게 계산되는 가중치(cur_time + weight)를 비교
     5. 새롭게 계산되는 가중치가 작으면 dist를 최신화 후 해당 노드를 새로운 가중치와 함께 hq에 삽입
     6. hq가 없어질때 까지 2~5를 반복



### 2021_01_09

1. BOJ_10989
   - 퀵소트를 사용했으나 메모리 초과가 발생
   - 파이썬 내부의 팀소트를 사용해도 메모리 초과가 발생
   - 카운팅소트를 이용 => 시간초과 발생 => sys.stdin.readline() 으로 해결
2. BOJ_11727
   - dp, memoization 기초
3. BOJ_2751
   - 단순 정렬 문제
   - 파이썬 내부의 팀소트 통과
   - 퀵소트
     1. 재귀로 구현시 재귀 깊이 에러
        - sys.setrecursionlimit => 메모리 초과
     2. 반복문으로 구현시 시간 초과
        - 최악의 경우인 n^2으로 추정
   - 카운팅소트 => 통과
     but, 불필요한 메모리를 씀
   - 최악의 경우에도 nlogn을 보장하는 힙소트나 머지소트도 공부해놔야 함

- 정렬

  | 알고리즘 | 평균수행시간 | 최악수행시간 | 알고리즘기법 |                             비고                             |
  | -------- | ------------ | ------------ | ------------ | :----------------------------------------------------------: |
  | 버블     | n^2          | n^2          | 비교, 교환   |                쉬운데 성능이 너무 별로라 안씀                |
  | 카운팅   | n + k        | n + k        | 교환 x       | n이 비교적 작을 때만 가능 속도는 빠른편 (k = 리스트중 가장 큰 값) |
  | 선택     | n^2          | n^2          | 비교, 교환   |              교환 횟수가 버블, 삽입보다는 작음               |
  | 퀵       | n log n      | n^2          | 분할 정복    |                     평균적으로 가장 빠름                     |
  | 삽입     | n^2          | n^2          | 비교, 교환   |                    n이 작으면 매우 효과적                    |
  | 병합     | n log n      | n log n      | 분할 정복    |                                                              |

  - 퀵정렬 (pivot == mid 인 방법)

    ```python
    """
    조건 1. left에 위치한 원소는 무조건 pivot보다 작아야함
    조건 2. right에 위치한 원소는 무조건 pivot보다 크거나 같아야함
    조건 3. pivot이 가리키는 원소는 계속 같아야 함
    조건 4. left 와 right가 만나는 위치가 pivot의 원소가 위치해야 하는 인덱스
    """
    
    def quick_sort(start, end):
        if start >= end:  # 배열의 원소가 1개 이하면 
            return  # 함수 종료
        left, right = start, end - 1
        pivot = (left + right) // 2  # 피벗을 정함
        while left < right:
            # 조건 1에 부합하면 다음 인덱스로 이동
            while arr[left] < arr[pivot] and left < right:
                left += 1
            # 조건 2에 부합하면 다음 인덱스로 이동
            while arr[right] >= arr[pivot] and left < right:
                right -= 1
            # left와 right를 swap해야 함
            if left < right:
                # left는 조건 1에 의해 pivot을 넘어갈 수 없음
                if left == pivot:
                    # 자리가 부족하므로 pivot의 위치를 변경
                    pivot = right
                arr[left], arr[right] = arr[right], arr[left]
        # pivot의 원소 위치 최신화
        arr[pivot], arr[right] = arr[right], arr[pivot]
        # 최종적으로 left == right == pivot이 되야함
        pivot = right
        quick_sort(start, pivot)
        quick_sort(pivot+1, end)
    ```



### 2021_01_10

1. BOJ_14225
   - 쉬운 brute force
2.  BOJ_14627
   - binary search



### 2021_01_11

1. BOJ_1181
   - 문자열 길이, 사전순 정렬 => `lambda x: (len(x), x)`
2. BOJ_1439
   - 투포인터?
3. BOJ_11653
   - 소인수 분해 => 무조건 에라토스테네스를 사용할 필요는 없음



### 2021_01_12

1. BOJ_3273
   - binary search
   - dictionary
   - two pointer



### 2021_01_14

1. BOJ_1629
   - 거듭제곱을 많이 해야 하는 경우 분할 정복을 사용 => log n 에 가능
2. BOJ_10775
   - 못품,,,,
   - union - find 자료구조를 공부하고 풀어보기
3. BOJ_17218
   - dp, lcs



### 2021_01_15

1. BOJ_19948
   - js로 풀어보기
2. BOJ_14921
   - two pointer



### 2021_01_16

1. BOJ_2133
   - dp
2. BOJ_9461
   - dp



### 2021_01_17

1. BOJ_5710
   - binary search
2. BOJ_2579
   - dp



### 2021_02_02

1. BOJ_1806
   - two pointer (part sum) => 시그마 배열
2. BOJ_13414
   - readline 쓸때 '\n' 등 조심
3. BOJ_2824
   - 숫자가 커진다고 해서 메모리를 많이 잡아먹지는 않음(배열과 다름)



### 2021_02_24

1. BOJ_1914
   - dp로 풀었으나 메모리를 많이 씀
   - 재귀로 풀어보기



### 2021_02_28

1. BOJ_11722
   - LIS 이용
     - LIS[i] 는 길이가 i 가되는 부분수열의 마지막 요소



### 2021_03_02

1. BOJ_13305
   - heapq를 사용해서 풀이
   - heapq를 사용하지 않고도 풀이법이 존재하며 더 빠름