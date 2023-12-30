# 백준 Python3 듀토리얼
## 데이터 입력
1.  데이터가 **한 줄**로 입력됬는데 **여러 개의 변수**로 입력을 받고 싶은 경우
  - a, b = map(int, input.split()) : 공백 기준으로 구분된 데이터가 많지 않을 때 (살짝 비효율적), int 형식으로 된 데이터를 입력 받을 떄
  - a, b = map(int, sys.stdin.readline().split()) : 이게 빠른방식, int 형식으로 된 데이터를 입력 받을 떄

2.  **문자열**로 이루어진 데이터를 받고 싶은 경우
  - data = sys.stdin.readline().rstrip()
    - .rstrip() : 문자열의 오른쪽 끝에서 부터 동일한 인자의 문자가 나오지 않을 때까지 제거하는 함수
    - .lstrip() : 문자열의 왼 쪽 끝에서 부터 동일한 인자의 문자가 나오지 않을 때까지 제거하는 함수
    - .strip() : 문자열의 양 쪽 끝에서 부터 동일한 인자의 문자가 나오지 않을 때까지 제거하는 함수
    - 만약 인자가 없다면 공백을 제거
  
3. 한줄로 주어지는 데이터를 list로 받고 싶은 경우, 이때 위의 함수에서 한 줄로 주어지는 데이터를 하나의 list로 얻기 위해선 list(map())으로 입력을 받아야한다.
 - board = [list(map(int, sys.stdin.readline().split())) for _ in range(N)] : N 은 입력받아야하는 줄의 개수
   - [x for _ in range(N)] x가 N번 실행되는 각 결과를 list의 원소로 구성되는 list 객체를 얻을 수 있는 방식
  
4.  

## 참고함수
1. map(function, iterable)

iterable에 funcition을 적용시켜 반환시켜준다.

변수 하나하나에 넣고 싶다면, a, b, c = map()으로 list로 만들고 싶다면 list(map(function, iterable))로 해주어여한다.

여기서 function은 x+1 같은 함수가 될 수도, int char같은 형식이 될 수도 있다.

- iterable : 반복 가능한 객체, ex) list, dict, set, str, bytes, tuple, range 등등
- iterator : 값을 차례대로 꺼낼 수 있는 객체 => iterable객체를 iter()함수를 통해서 iterator를 생성
  - iterator은 iter(a).__next__() 메소드를 통해 하나씩 객체를 꺼낼 수 있다.

2. 

## 참고자료
- https://velog.io/@kho5420/Git-GitHub-%EB%A0%88%ED%8C%8C%EC%A7%80%ED%86%A0%EB%A6%ACRepository-%EC%83%9D%EC%84%B1%ED%95%98%EA%B3%A0-%EC%86%8C%EC%8A%A4-%EC%98%AC%EB%A6%AC%EA%B8%B0
  - github commit 방법
- https://12716.tistory.com/entry/Github-GIthub%EC%97%90%EC%84%9C-READMEmd-%EC%9E%91%EC%84%B1%ED%95%98%EA%B8%B0
  - readme.md 작성문법
- https://paris-in-the-rain.tistory.com/72
  - 백준 입력방법
