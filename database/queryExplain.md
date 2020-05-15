# Index and Table Access

### Seq Scan

Seq Scan은 row를 찾기위해 table 전체를 순회합니다.

### Index Scan

Index Scan은 B-Tree trabersal를 수행하고 리프노드를 통해 일치하는 모든 항목을 찾아 rows를 가져옵니다. 이후 찾아온 rows를 토대로 순차적으로 스캔하여 row를 찾습니다

### Index Only Scan

Index Only Scan은 B-Tree trabersal를 수행하고 리프노드를 통해 일치하는 모든 항목을 찾아 row터를 가져옵니다.

인덱스 쿼리에 적합한 모든 열이 있기 때문에 다시 순차적으로 스캔하기위한 테이블 접근이 필요하지 않습니다.
