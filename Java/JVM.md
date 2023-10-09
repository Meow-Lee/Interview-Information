# Java

## JVM에 대하여
 - Java Virtual Machine으로 자바 가상 머신
 - 가상 머신이란, 프로그램을 실행하기 위한 물리적 머신과 유사한 머신을 sw로 구현한 것
 - Stack 기반의 가상 머신

## JVM의 역할
 - Class Loader를 통해 Java Application을 읽어들여 Java API와 함께 실행하는 것
 - Java와 OS 사이에서 중개자 역할을 수행하여 OS에 구애받지 않고 재사용을 가능하게 함
 - 메모리 관리, Garbage Collection을 수행

## 왜 JVM 인가?
 - 메모리 효율성을 위해 메모리 구조를 알아야하고, 궁극적으로 한정된 메모리를 효율적으로 사용해 최적의 성능을 내기 위함

## Java 프로그램 실행 과정
 1. JVM은 프로그램이 시작되면 실행될 프로그램의 메모리를 할당받아 용도에 따라 나누어 관리 (이 때 메모리는 Runtime Data Areas 에서 관리됨)
 2. 자바 컴파일러(javac)가 자바 소스코드(.java)를 읽어 자바 바이트코드(.class)로 변환
 3. Class Loader를 통해 class 파일들을 JVM으로 로딩
 4. 로딩된 class 파일들을 Execution Engine을 통해 해석
 5. 해석된 class 파일들은 Runtime Data Areas에 배치되어 실질적 수행 시에 실행됨 (이 과정에서 필요에 따라 GC와 같은 관리 작업 수행)

## 실행 과정 (그림)
<img width="843" alt="JVM" src="https://github.com/Meow-Lee/Interview-Information/assets/67636286/fd04ed39-f700-4411-8841-09cffa43ab6b">


## Reference
http://asfirstalways.tistory.com
