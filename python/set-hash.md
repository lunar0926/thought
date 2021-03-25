# 집합 자료형\(set\) \(hash개념 추가하기\)

### python documentation에서

{% embed url="https://docs.python.org/3/library/stdtypes.html\#set" %}

Set types:

 A set object is an unordered collection of distinct hashable objects. Common uses include membership testing, removing duplicates from a sequence, and computing mathematical operations such as intersection, union, difference, and symmetric difference. 

 set 객체는 별개의 해시 가능한 객체들의 모음으로, 순서가 없다. 

* 여기서 hashable\(해시 가능\) objects 는 객체가 유지되는 동안은 절대로 바뀌지 않는 해시 값을 가지고 있고, 다른 객체와 비교될 수 있는 것을 말한다. 동등하게 비교되는 hashable objects는 서로 같은 해시 값을 가져야만 한다. 
* 해시 가능하다는 것은 객체가 딕셔너리의 키, set\(집합 자료형\)의 멤버로 사용될 수 있다. 왜냐하면 이러한 자료구조는 해시 값을 내부적으로 사용하기 때문이다.
* 파이썬에 있는 대부분의 불변 내장 객체들은 hashable하다. 변할 수 있는 containers\(리스트나 딕셔너리\)은 해시 가능하지 않다. 불변하는 containers\(튜플, frozensets\)는 그것들의 원소가 hashable할 때만 hashable하다.
* hash에 대한 개념을 더 이해할 필요가 있음. 

순서가 없고 중복을 허용하지 않는 집합 자료형의 특성 때문에 집합 자료형은 

* 특정 원소가 있는지 확인할 때\(membership testing\)
* 중복을 제거할 때
* 교집합\(intersection\), 합집합\(union\), 차집합\(difference\), 대칭차집합\(symmetric difference\)과 같은 수학적 연산를 계산하는데 사용할 수 있다.

### 집합 자료형 만들기 

```text
set(['a', 'b', 'c'])
a = {'a', 'b', 'c'}
```

set\(\), set\('foobar'\), set\(\['a', 'b', 'foo'\]\) 와 같이 자료형 생성자를 사용하거나 

{'jack', 'sjoerd'} 와 같이 중괄호 안에 comma로 구분된 원소를 넣어서 선언할 수 있다. 

중괄호가 쓰여서 나는 순간적으로 딕셔너리와 헷갈렸는데, 딕셔너리는 {key1:value1, key2:value2, ...} 와 같이 생성된다. 



