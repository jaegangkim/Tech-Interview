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
  - Key를 이용하여 Value 도출

- HashTable 기능
  - 연관배열 구조와 동일한 기능 지원
  - Key,Value가 주어졌을 때, 두 값을 저장
  - Key가 주어지면 해당 Key와 연관된 Value 조회, 수정, 삭제
 
- HashTable 구조
