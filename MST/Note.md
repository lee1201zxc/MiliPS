## Kruskal 알고리즘
(1) 그래프의 간선들을 가중치의 오름차순으로 정렬
(2) 사이클을 형성하지 않는 간선을 순서대로 선택
  - 사이클을 생성하는지의 여부는 union-find 알고리즘을 이용한다.
  - union-set 알고리즘 : disjoing-set을 표현할 때 사용하는 알고리즘이다.
(3) 해당 간선을 현재의 MST 집합에 추가한다.

## Prim 알고리즘
(1) 시작 정점만이 MST 집합에 포함되면서 시작된다.
(2) 앞의 MST 집합에 인접한 정점들 중에서 최소 간석으로 연결된 정점을 선택한다.

union-find 알고리즘을 이용하면 Kruskal 알고리즘의 시간 복잡도는 간선들을 정렬하는 시간에 좌우된다.
즉, 간선 e개를 퀵 정렬과 같은 효율적인 알고리즘으로 정렬한다면
Kruskal 알고리즘의 시간 복잡도는 O(elog₂e) 이 된다.
Prim의 알고리즘의 시간 복잡도는 O(n^2) 이므로
그래프 내에 적은 숫자의 간선만을 가지는 ‘희소 그래프(Sparse Graph)’의 경우 Kruskal 알고리즘이 적합하고
그래프에 간선이 많이 존재하는 ‘밀집 그래프(Dense Graph)’ 의 경우는 Prim 알고리즘이 적합하다.
https://gmlwjd9405.github.io/2018/08/29/algorithm-kruskal-mst.html

주 반복문이 정점의 수 n만큼 반복하고, 내부 반복문이 n번 반복
Prim의 알고리즘의 시간 복잡도는 O(n^2) 이 된다.
Kruskal 알고리즘의 시간 복잡도는 O(elog₂e) 이므로
그래프 내에 적은 숫자의 간선만을 가지는 ‘희소 그래프(Sparse Graph)’의 경우 Kruskal 알고리즘이 적합하고
그래프에 간선이 많이 존재하는 ‘밀집 그래프(Dense Graph)’ 의 경우는 Prim 알고리즘이 적합하다.
https://gmlwjd9405.github.io/2018/08/30/algorithm-prim-mst.html
