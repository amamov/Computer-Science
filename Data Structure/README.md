# 자료구조와 알고리즘

![ds](../images/ds.png)

데이터를 효과적으로 저장하고, 처리하는 방법에 대해서 바르게 이해할 필요가 있습니다. 자료구조를 제대로 이해하지 못하면 불필요하게 메모리와 성능을 낭비할 여지가 있습니다.

1. 효율적인 자료구조 설계를 위해 알고리즘 지식이 필요합니다.
2. 효율적인 알고리즘을 작성하기 위해서는 문제 상황에 맞는 적절한 자료구조가 사용되어야 합니다.
3. 따라서 자료구조론과 알고리즘 이론은 모두 동일선상에 놓을 수 있습니다.

- **자료구조 (Data Structure)**
  - 각 원소들이 논리적으로 정의된 규칙에 의해 나열되며 자료에 대한 처리를 효율적으로 수행할 수 있도록 자료를 구분하여 표현한 것
- **알고리즘 (Algorithm)**
  - 문제를 풀어가는 절차

<br>

데이터를 효과적으로 저장하고, 처리하는 방법에 대해서 바르게 이해할 필요가 있습니다. 자료구조를 제대로 이해하지 못하면 불필요하게 메모리와 성능을 낭비할 여지가 있습니다.

1. 효율적인 자료구조 설계를 위해 알고리즘 지식이 필요합니다.
2. 효율적인 알고리즘을 작성하기 위해서는 문제 상황에 맞는 적절한 자료구조가 사용되어야 합니다.
3. 따라서 자료구조론과 알고리즘 이론은 모두 동일선상에 놓을 수 있습니다.

<br>

## 기본적인 자료구조

추상 데이터 타입(ADT)은 유사한 동작을 가진 자료구조의 클래스에 대한 수학적 모델을 가리킨다. 많은 추상 데이터 타입은 각기 클래스는 다르지만, 기능적으로 동일하게 구현된 자료구조를 가지고 있다. 자료구조는 크게 **배열 기반의 연속 방식**과 **포인터 기반의 연결 방식**으로 분류한다. 또한 아래와 같이 **선형 구조**와 **비선형 구조**로 분류할 수 있다.

- **자료구조의 분류**

  1. 선형구조
     - 배열 (Array)
     - 연결리스트 (Linked List)
     - 스택 (Stack)
     - 큐 (Queue)
  2. 비선형 구조
     - 트리 (Tree)
     - 그래프 (Graph)

<br>

- **자료구조의 선택 기준**
  - 자료의 처리 시간
  - 자료의 크기
  - 자료의 활용 빈도
  - 자료의 갱신 정도
  - 프로그램의 용이성

<br>

- **자료구조의 특징**
  - 효율성
  - 추상화
  - 재사용성

<br>

## 프로그램의 성능 측정 방법론

1. 시간 복잡도(Time Complexity)란 알고리즘에 사용되는 **연산 횟수**를 의미합니다.

2. 공간 복잡도(Space Complexity)란 알고리즘에 사용되는 **메모리의 양**을 의미합니다.

효율적인 알고리즘을 사용한다고 가정했을 때 일반적으로 시간과 공간은 반비례 관계입니다.

<br>

### 시간 복잡도 : 연산 횟수

시간 복잡도를 표현할 때는 **최악의 경우**를 나타내는 `Big-O 표기법`을 사용합니다. 다음 알고리즘은 **𝑂(n)** 의 시간 복잡도를 가집니다.

```python
total = 0
for i in range(10):
    total += 1
print(total)
```

다음 알고리즘은 𝑂(n<sup>2</sup>) 의 시간 복잡도를 가집니다.

```python
total = 0
for i in range(10):
    for j in range(10):
        total += 1
print(total)
```

다음 알고리즘의 시간 복잡도는 **𝑂(1)** 입니다.

```python
total = 10 * (10 + 1) / 2
print(total)
```

시간 복잡도를 표기할 때는 항상 큰 항과 계수만 표시합니다.
𝑂(3n<sup>2</sup> + n) = 𝑂(n<sup>2</sup>)

**𝑂(1) < 𝑂(n) < 𝑂(nlogn) < 𝑂(n<sup>2</sup>) < 𝑂(n<sup>3</sup>)**

예를 들어 n이 1000이라면 𝑂(n)은 1000번 연산, 𝑂(nlogn)은 약 10000번 연산, 𝑂(n<sup>2</sup>)은 1000000번의 연산을 의미합니다.

보통 연산 횟수가 10억을 넘어가면 1초 이상의 시간이 소요됩니다. 현실적의 다양한 문제에서는 시간 제한이 1초 정도라고 생각하시면 됩니다.

<br>

### 공간 복잡도 : 메모리 양

공간 복잡도를 표기할 때는 일반적으로 MB 단위로 표기합니다.

- `int a[1000]` : 4KB(=4000byte)
- `int a[1000000]` : 4MB
- `int a[2000][2000]` : 16MB
