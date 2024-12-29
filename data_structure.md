# 자료구조(Data Structure)
## 리스트(List)
### 배열(Array)
- 정의 : 동일한 데이터 타입의 요소들을 순차적으로 저장하는 선형 데이터 구조
- 특징   
    - 동일한 데이터 타입의 요소들로만 구성
    - 요소들이 순차적으로 저장 - 메모리 상에서 연속된 공간에 데이터를 배치
    - 인덱스를 기반으로 배열의 요소에 접근
#### 고정 크기 배열 (Fixed-size Array)	
- 정의 : 미리 정의된 크기만큼의 메모리를 할당받아 동적으로 크기를 변경할 수 없는 배열
- 특징 : 선언시 단 한번만 메모리를 할당받음
- 장점 
    - 배열의 크기가 고정되어 있기 때문에 각 인덱스에 해당하는 메모리 주소를 빠르게 계산하여 접근 가능
    - 메모리 관리가 상대적으로 단순하고 일정한 성능을 보장
- 단점
    - 크기가 고정되어 있기 때문에 배열의 크기보다 데이터의 양이 적으면 메모리를 낭비하게될 가능성이 있음
    - 선언된 배열의 크기보다 더 많은 데이터를 저장해야 할 경우 새로운 배열을 만들어 데이터를 복사해야 함
- 예시
    <details><summary>C언어에서의 고정 크기 배열</summary>

    ```C
    int arr[5]; //고정 크기 배열 선언
    arr[0] = 10; //0번 인덱스에 10 할당
    ```
    </details>


#### 동적 배열 (Dynamic Array)
- 정의 : 배열의 크기가 동적으로 변화할 수 있는 배열
- 특징
    - 크기가 변경될 때 마다 새로운 메모리 블록을 할당하고, 기존 배열의 데이터를 새로운 배열로 복사
- 장점
    -  크기가 동적으로 변화하므로 선언시 필요한 크기를 예측할 필요가 없음
    -  데이터의 양에 따라 유동적으로 배열의 크기를 변경하여 메모리 낭비를 줄임
- 단점
    -  배열 크기가 늘어날 때마다 메모리 재할당과 복사가 발생하여 성능에 영향을 줄 수 있음
- 예시
    <details><summary>C언어에서의 동적 배열</summary>

    ```C
    int* arr = (int*)malloc(sizeof(int) * 10); //동적 배열, 크기 10 할당
    free(arr) //메모리 반납
    ```
    </details>

---
### 연결 리스트 (Linked List)	
- 정의 : 각 노드가 데이터와 포인터를 가지고 한 줄로 연결되어 있는 방식으로 데이터를 저장하는 선형 자료 구조
- 특징
    -  노드가 추가되거나 제거되면서 크기가 동적으로 변화할 수 있음
    -  각 노드가 메모리의 다른 위치에 저장되며, 노드들이 포인터를 통해 연결되어 있음
    -  삽입 삭제시 포인터만 변경하면 되어 배열보다 효율적이나 특정 요소를 찾을 때 전체를 순회해야해 검색 시간이 배열보다 느림
#### 단일 연결 리스트 (Singly-Linked List)
- 정의 : 각 노드가 데이터와 다음 노드를 가리키는 포인터를 가지고 일렬로 연결되어 있는 리스트
- 특징
    -  각 노드의 포인터는 다음 노드만을 가리킴
- 장점
    -  연결 리스트의 장점을 가지나 단일 연결 리스트만의 장점은 없음
- 단점
    -  특정 노드에 접근하기 위해서 헤드부터 원하는 노드까지 탐색해야 함
    -  역방향 탐색이 불가능함
- 예시
    <details><summary>단일 연결 리스트 예시</summary>

    ![단일 연결 리스트 이미지](./img/data_structure/singly_linked_list.png)   
    Image source : GeeksforGeeks

    </details>

#### 이중 연결 리스트 (Doubly-Linked List)		
- 정의 : 각 노드가 데이터와 이전과 다음 노드를 가리키는 포인터를 가지고 일렬로 연결되어 있는 리스트
- 특징
    -  각 노드의 포인터가 이전 노드와 다음 노드를 가리키는 포인터를 가지고 있음
- 장점
    -  양방향 탐색이 가능함
    -  단일 연결 리스트에 비해 노드의 이전 노드를 탐색하고 삭제하기가 용이
    -  헤드 노드와 테일 노드의 삽입 삭제가 용이
- 단점
    -  단일 연결 리스트에 비해 포인터를 하나 더 사용하여 메모리를 더 많이 사용
    -  단일 연결 리스트보다 포인터 관리가 복잡
- 예시


#### 원형 연결 리스트 (Circular-Linked List)		
- 정의 : 리스트의 마지막 노드가 헤드 노드를 가리켜서 노드들이 원형으로 연결되어 있는 리스트
- 특징
    -  단일 연결 리스트와 이중 연결 리스트 모두에서 구현이 가능
    -  마지막 노드의 포인터가 헤드 노드를 가리켜 리스트 전체가 순환가능한 구
- 장점
    -  리스트의 끝에서 처음 노드로 이동할 수 있어 순환 작업에 유리(ex: Round-Robin 스케줄링)
    -  어느 노드에서든 탐색을 시작하여 전체 탐색이 가능
- 단점
    -  순환 구조로 인해 종료 조건을 명확히 하지 않으면 무한 루프에 빠질 위험이 있음
- 예시


#### 다중 연결 리스트 (Multi-Linked List)
- 정의 : 앞의 연결 리스트들과 달리 단방향, 양방향으로 연결된 것이 아니라 각 노드가 여러개의 포인터를 가져 포인터들을 통해 여러 노드에 연결되어 있는 리스트
- 특징
    -  각 노드가 여러개의 포인터를 가지며 각각 다른 방향이나 리스트를 가리킬 수 있음
    -  행렬과 같은 다차원 데이터를 연결 리스트로 표현할 때 사용 가능
- 장점
    -  데이터가 여러 연결 리스트의 노드로 포함될 수 있어 복잡한 관계 표현 가능
    -  여러 방향으로 연결이 가능하여 데이터 탐색이나 관계 표현이 유연
- 단점
    - 다중 포인터를 관리해야 하므로 삽입, 삭제, 탐색의 구현이 매우 복잡
- 예시
  
---
## 스택
- 정의:
- 특징:				
### 배열 기반 스택 (Array-based Stack)			
- 정의 :
- 특징
- 장점
- 단점
- 예시
### 연결 리스트 기반 스택 (Linked List-based Stack)	
- 정의 :
- 특징
- 장점
- 단점
- 예시
### 최소값/최대값 추적 스택 (Min/Max Stack)			
- 정의 :
- 특징
- 장점
- 단점
- 예시
## 큐
- 정의:
- 특징:			
### 배열 기반 큐 (Array-based Queue)			
### 순환 큐 (Circular Queue)			
### 연결 리스트 기반 큐 (Linked List-based Queue)			
### 우선순위 큐 (Priority Queue)			
#### 배열 기반 우선순위 큐		
#### 힙 기반 우선순위 큐
## 데크	
- 정의:
- 특징:			
### 배열 기반 데크 (Array-based Deque)			
### 연결 리스트 기반 데크 (Linked List-based Deque)			
## 트리				
### 트리 (Tree)		
- 정의:
- 특징:	
#### 일반 트리		
#### Left-child-right-sibling 트리		
### 트리 순회
- 정의:
- 특징:
#### 전위 순회 (Pre-order Traversal)		
#### 중위 순회 (In-order Traversal)		
#### 후위 순회 (Post-order Traversal)		
#### 레벨 순회 (Level-order Traversal)		
### 이진 트리 (Binary Tree)			
- 정의:
- 특징:
#### 포화 이진 트리 (Full Binary Tree)		
#### 완전 이진 트리 (Complete Binary Tree)		
#### 경사 트리 (Skewed Tree)		
#### 수식 트리 (Expression Tree)		
### 이진 탐색 트리 (Binary Search Tree)			
- 정의:
- 특징:
#### 균형 이진 탐색 트리 (Balanced BST)		
##### AVL 트리 (AVL Tree)	
##### 레드-블랙 트리 (Red-Black Tree)	
##### Splay Tree	
#### B 트리 계열		
##### B 트리 (B-Tree)	
##### B+ 트리 (B+ Tree)	
##### B* 트리 (B* Tree)	
### 힙 (Heap)	
- 정의:
- 특징:		
#### 최대 힙 (Max-Heap)		
#### 최소 힙 (Min-Heap)		
#### 이진 힙 (Binary Heap)		
#### 피보나치 힙 (Fibonacci Heap)		
#### 이진 트리 기반 힙		
### 분리 집합 (Disjoint Set)	
- 정의:
- 특징:		
#### Union-Find 알고리즘		
#### 경로 압축 및 크기 조정		
## 그래프				
### 그래프 (Graph)	
- 정의:
- 특징:		
#### 방향 그래프 (Directed Graph)		
#### 무방향 그래프 (Undirected Graph)		
#### 가중 그래프 (Weighted Graph)		
#### 비가중 그래프 (Unweighted Graph)		
### 그래프 표현 방식			
- 정의:
- 특징:
#### 인접 행렬 (Adjacency Matrix)		
#### 인접 리스트 (Adjacency List)		
### 그래프 순회			
- 정의:
- 특징:
#### 너비 우선 탐색 (Breadth-First Search, BFS)		
#### 깊이 우선 탐색 (Depth-First Search, DFS)		
### 최단 경로 알고리즘		
- 정의:
- 특징:	
#### 다익스트라 알고리즘 (Dijkstra's Algorithm)		
#### 벨만-포드 알고리즘 (Bellman-Ford Algorithm)		
#### 플로이드-워셜 알고리즘 (Floyd-Warshall Algorithm)		
### 최소 신장 트리 (Minimum Spanning Tree)		
- 정의:
- 특징:	
#### 크루스칼 알고리즘 (Kruskal's Algorithm)		
#### 프림 알고리즘 (Prim's Algorithm)		
### 위상 정렬 (Topological Sorting)			
- 정의:
- 특징:
### 강결합 요소 탐색 (Strongly Connected Components)			
- 정의:
- 특징:
### 이분 그래프 탐색 (Bipartite Graph Check)			
- 정의:
- 특징:
## 해시
- 정의:
- 특징:				
### 해시 테이블 (Hash Table)			
### 해시 함수 (Hash Function)			
### 충돌 처리 (Collision Handling)			
#### 개방 주소법 (Open Addressing)		
#### 체이닝 (Chaining)		
### 동적 크기 조정 (Dynamic Resizing)			
### 블룸 필터 (Bloom Filter)			