# Data Structure
자료구조 : 데이터를 원하는 규칙 또는 목적에 맞게 저장하기 위한 구조
<br><br>
<details>
  <summary><h4>목차</h4></summary>
  
- [Array와 LinkedList](#Array와-LinkedList)
- [HashTable](#HashTable)
- [Stack](#Stack)
- [Queue](#Queue)
- [Graph와 Tree](#Graph와-Tree) 
- [](#)
- [](#)
- [](#) 
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
 
- HashTable 구조<br>![1](https://github.com/jaegangkim/Tech-Interview/blob/main/images/HashTable1.png?raw=true)
  - Key : 고유한 값 / 저장 공간의 효율성을 위해 Hash Function에 입력하여 Hash로 변경 후 저장
  - Hash Function : Key를 Hash로 바꿔주는 역할 / 해시 충돌이 발생할 확률을 최대한 줄이는 함수를 만드는 것이 중요
  - Hash : Hash Function의 결과 / 저장소에서 Value와 매칭되어 저장
  - Value : 저장소에 최종적으로 저장되는 값 / 키와 매칭되어 저장, 삭제, 검색, 수정 가능
 
#### Hash 충돌
- 서로 다른 Key가 Hash Function에서 같은 Hash로 나오는 경우 발생
- 충돌이 많아질수록 탐색의 시간 복잡도가 O(1)에서 O(n)으로 증가

> 해시의 충돌 현상을 해결할 수 있는 방법이 어떤 것들이 있나요?
>> 크게 Chaining과 Open Addressing이 있습니다. Chaining은 연결리스트로 노드를 계속 추가(같은 주소로 해싱되는 원소를 추가)해 나가는 방식이며, Open Addressing은 해시 함수로 얻은 주소가 아닌 다른 주소에 데이터를 저장할 수 있도록 허용하는 것입니다. 다음 주소를 결정하는 방식이 다양한데, 대표적으로는 선형 탐사, 제곱 탐사, 더블 해싱이 있습니다. 선형탐사는 정해진 고정 폭으로 옮겨 해시값의 중복을 피하는 방식이며, 제곱 탐사는 정해진 고정 폭을 제곱수로 옯겨 해시값의 중복을 피하는 방식입니다. 더블 해싱은 다른 해시 함수를 통해 2번째 해시 함수값 만큼씩 점프하여 중복을 피하는 방식입니다.<br><br>
>> Chaining : 추가적인 공간 사용 / 수정에 대한 작업이 용이함<br>
>> Open Addressing : 기존 메모리 사용 / 수정에 대한 작업이 복잡함

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

## Stack
: 한 쪽 끝에서만 자료를 넣고 뺄 수 있는 LIFO(Last In First Out) 형식의 자료 구조
#### 사용 예시
- pop() push(item) peek() isEmpty()
## Queue
: 컴퓨터의 기본적인 자료구조의 한가지로, 먼저 집어넣은 데이터가 먼저 나오는 FIFO(First In First Out)구조로 저장하는 형식
#### 사용 예시
- add(item) remove() peek() isEmpty()
- 입력 순서대로 처리해야 할 필요가 있는 경우 사용
- BFS(너비 우선 탐색) , 캐시 구현
## Graph와 Tree
#### Graph
: 단순히 노드(N, node)와 그 노드를 연결하는 간선(E,edge)을 하나로 모아놓은 자료 구조
- 객체 간의 관계를 표현할 수 있다
#### Tree
: 노드로 이루어진 자료 구조
- 비선형 자료구조로, 계층적 관계를 표현한다.
- 그래프의 한 종류로, '최소 연결 트리'라고도 불린다.
#### 차이점
![2](https://github.com/jaegangkim/Tech-Interview/blob/main/images/graph-vs-tree.png?raw=true)

###### 참고자료
- https://hee96-story.tistory.com/48
