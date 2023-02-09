# Data Structure
자료구조 : 데이터를 원하는 규칙 또는 목적에 맞게 저장하기 위한 구조
<br><br>
<details>
  <summary>목차</summary>
  
- [Array와 LinkedList](#Array와-LinkedList)
- [HashTable](#HashTable)
- [](#)
- [](#)
  
</details>

## Array와 LinkedList
#### Array
- 순차적으로 데이터를 저장한다.
- 데이터에 순서가 있기 때문에 index를 이용하여 원하는 데이터에 접근할 수 있다.
- 리스트의 크기가 고정되어 있어, 중간에 요소가 삽입되거나 삭제되는 경우 그 뒤의 모든 요소들을 움직여야 한다.

#### LinkedList
- 리스트 크기에 상관없이 데이터를 추가할 수 있다.
- 데이터 추가를 위해 새로운 노드를 생성하여 연결한다 -> 추가/삭제 연산이 빠르다.
- 무작위 접근이 불가능하며, 순차 접근만이 가능하다.<br>

>**Array는 검색이 빠르지만 삽입,삭제가 느리고 LinkedList는 검색이 느리지만 삽입,삭제가 빠르다.**

<br>

## HashTable
- HashTable 개념
  - Key와 Value를 1:1로 연관지어 저장하는 자료구조
  - 각 Key값은 해시함수에 의해 고유한 index를 가지게 되어 바로 접근할 수 있으므로 평균 O(1)의 시간 복잡도로 데이터를 조회한다. 하지만 index값이 충돌이 발생한 경우 Chanining에 연결된 리스트들까지 검색해야 하므로 O(N)까지 증가할 수 있다.
 
- HashTable 구조
  - ![1](https://github.com/jaegangkim/Tech-Interview/blob/main/images/HashTable1.png?raw=true)
  - Key : 고유한 값 / 저장 공간의 효율성을 위해 Hash Function에 입력하여 Hash로 변경 후 저장
  - Hash Function : Key를 Hash로 바꿔주는 역할 / 해시 충돌이 발생할 확률을 최대한 줄이는 함수를 만드는 것이 중요
  - Hash : Hash Function의 결과 / 저장소에서 Value와 매칭되어 저장
  - Value : 저장소에 최종적으로 저장되는 값 / 키와 매칭되어 저장, 삭제, 검색, 수정 가능
 
#### Hash 충돌
- 서로 다른 Key가 Hash Function에서 같은 Hash로 나오는 경우 발생
- 충돌이 많아질수록 탐색의 시간 복잡도가 O(1)에서 O(n)으로 증가

#### HashTable의 장단점
- 장점
  - 적은 리소스로 많은 데이터 관리 가능
  - 삽입, 검색, 삭제, 조회가 빠름
  - Key와 Hash에 연관성이 없어 보안에 유리함
  - 중복 제거에 유용
 
- 단점
  - 충돌 발생 가능성이 있음
  - 공간 복잡도 증가
  - 순서 무시
  - 해시 함수에 의존
 
#### HashTable과 HashMap의 차이점 
Key-Value구조 및 Key에 대한 Hash로 Value를 관리하는 것은 동일함
- HashTable
  - 동기
  - null값 미허용
- HashMap
  - 비동기
  - null값 허용








###### 참고자료
- https://hee96-story.tistory.com/48
