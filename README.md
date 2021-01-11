# JVM구조
![JVM구조](https://user-images.githubusercontent.com/24876345/104185236-0dc80680-5458-11eb-8847-6701db69b9b8.png)

### Class Loader
* 자바 컴파일러가 .java 파일을 컴파일하면 .class 파일(바이트 코드)가 생성된다. 
* 이렇게 생성된 클래스 파일들을 엮어 Runtime Data Area 형태로 메모리에 적재하는 역할을 한다.

![image](https://user-images.githubusercontent.com/24876345/104185787-cdb55380-5458-11eb-99ac-1f86cfc670c6.png)

# Execution Engine
* 메모리에 적재된 클래스들을 기계어로 변경해 명령어 단위로 실행하는 역할을 한다.
* 명렁어를 하나 하나 실행하는 인터프리터 방식과 실행 시점에 자주 쓸만한 코드들을 기계어로 변환 시켜놓고 저장해서 사용하는 JIT 방식이 있다.

# Garbage Collector
* Heap 메모리 영영에 생성 된 객체들중에 Reachability를 잃은 객체를 탐색 후 제거하는 역할을 한다.

출처: https://velog.io/@litien/JVM-%EA%B5%AC%EC%A1%B0
