# JVM구조
![JVM구조](https://user-images.githubusercontent.com/24876345/104185236-0dc80680-5458-11eb-8847-6701db69b9b8.png)

![image](https://user-images.githubusercontent.com/24876345/104185787-cdb55380-5458-11eb-99ac-1f86cfc670c6.png)

### Class Loader
* 자바 컴파일러가 .java 파일을 컴파일하면 .class 파일(바이트 코드)가 생성된다. 
* 이렇게 생성된 클래스 파일들을 엮어 Runtime Data Area 형태로 메모리에 적재하는 역할을 한다.

### Execution Engine
* 메모리에 적재된 클래스들을 기계어로 변경해 명령어 단위로 실행하는 역할을 한다.
* 명렁어를 하나 하나 실행하는 인터프리터 방식과 실행 시점에 자주 쓸만한 코드들을 기계어로 변환 시켜놓고 저장해서 사용하는 JIT 방식이 있다.

### Garbage Collector
* Heap 메모리 영영에 생성 된 객체들중에 Reachability를 잃은 객체를 탐색 후 제거하는 역할을 한다.


### Runtime Data Area
* Method Area
  - 클래스 멤버 변수, 메소드 정보, Type(Class or interface)정보, Constant Pool, static, final 변수 등이 생성된다. 상수 풀은 모든 Symbolic Refernce를 포함하고 있다.

* Heap Area
  - 동적으로 생성된 오브젝트와 배열이 저장되는 곳으로 Garbage Collection의 대상이 되는 영역이다.

* Stack Area
  - 지역 변수, 파라미터 등이 생성되는 영역, 동적으로 객체를 생성하면 실제 객체는 Heap에 할당되고 해당 레퍼런스만 Stack에 저장된다. Stack은 스레드별로 독자적으로 가진다.

* PC Register
  - 현재 쓰레드가 실행되는 부분의 주소와 명령을 저장하고 있다.(CPU의 PC Register와 다르다)

* Native Method Stack
  - 자바외 언어로 작성된 네이티브 코드를 위한 메모리 영역


출처: https://velog.io/@litien/JVM-%EA%B5%AC%EC%A1%B0
