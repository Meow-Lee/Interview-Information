## GC(Garbage Collection)
- JVM의 메모리 관리 기법 중 하나로 시스템에서 동적으로 할당되었던 메모리 영역 중에서 필요없어진 메모리 영역을 회수하여 관리하는 기법

## Garbage Collection 과정
- JVM이 잠시 실행을 멈추고 GC를 실행하는 Thread를 제외한 모든 Thread들의 작업을 중단 후, 사용하지 않는 메모리를 제거하고 작업이 재개
- GC의 작업은 Young에 대한 Minor GC와 Old 영역에 대한 Major GC로 구분

## Garbage Collection
<img width="716" alt="GC" src="https://github.com/Meow-Lee/Interview-Information/assets/67636286/589980aa-0db9-4f48-85bf-7b098896a8f8">

### Minor GC
- 새로 생성된 대부분의 객체는 Eden 영역에 위치
- GC 과정을 거치고 살아남은 객체는 Survivor 영역 중 하나로 위치
- 여러 번의 GC 과정을 거치고도 살아남은 객체는 일정 시간 참조되고 있다는 의미이므로, Old 영역으로 이동

### Major GC
- Old 영역에 있는 객체들을 모두 검사하여 참조되지 않는 객체들을 한번에 삭제
- 이 작업은 실행이 오래 걸리고 실행 중 이 작업을 진행중인 Thread를 제외하고 모두 중단 (Stop-the-World 라고 함)
- GC 작업이 완료된 후 다시 재개

## GC의 소멸 대상 선정 원리
- Heap 내의 객체 중 Garbage를 찾아 회수
- Garbage란, 참조되고 있지 않은 객체를 뜻함
- 객체가 Garbage인지 판단하기 위해서 Reachability 개념을 사용
- Reachability란, 어떤 Heap 영역에 위치한 객체가 유효한 참조가 있으면 Reachability, 없다면 Unreachability라고 함

## Reference
http://asfirstalways.tistory.com/159
https://dev-coco.tistory.com/153
