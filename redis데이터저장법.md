# Redis의 데이터 저장 방법

* 데이터 관리 구조: dict
* 기본 자료구조로: hash 구조-> 메모리 사용량이 가장 적기 때문이다.
* dict 구조에서 요청된 키와 값에 대한 데이터를 하나의 엔트리(dictEntry)로 묶어서 저장한다. 

## 엔트리

엔트리에 등록된 키는 문자열로, 값은 redis 객체로 저장된다. redis 객체는 요청된 값 뿐만 아니라 데이터 타입, 참조 횟수, 시간, 값에 대한 포인터를 가지고 있다. 

* 키에 대한 포인터
* 값에 대한 redis 객체 포인터
* 다음 엔터리를 가리키는 엔트리 포인터