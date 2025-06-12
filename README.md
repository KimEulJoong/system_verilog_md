# SystemVerilog 개요

SystemVerilog는 하드웨어 설계 및 검증을 위한 하드웨어 기술 언어(HDL)로, 기존 Verilog를 확장한 표준입니다. IEEE Std 1800-2017로 표준화되어 있습니다.
MobaXterm을 사용하여 vcs, verdi를 활용하였으며 기본적인 메모 사항을 .md 형식으로 정리하하였습니다. 

## 1. SystemVerilog란?

SystemVerilog는 RTL 설계, 테스트벤치 개발, 기능 검증 및 포멀 검증을 위한 다양한 기능을 제공합니다. 설계자와 검증자가 하나의 언어로 작업할 수 있게 지원합니다.

## 2. 주요 특징

- **디자인 모델링**
  - 모듈 (`module`)
  - 인터페이스 (`interface`)
  - 구조체, 공용체 (`struct`, `union`)
  - 열거형 (`enum`)
  - 클래스 기반 객체지향 프로그래밍

- **데이터 타입**
  - 논리형 (`logic`)
  - 4-상태형 (`0, 1, x, z`)
  - 정수형 (`int`, `integer`, `bit`)
  - 실수형 (`real`, `shortreal`)
  - 동적 배열, 연결 리스트 (`queue`, `dynamic array`, `associative array`)

- **절차적 블록**
  - `initial`, `always`, `final` 블록
  - `if`, `case`, `for`, `foreach`, `while`, `do-while`

- **클래스와 객체**
  - 클래스 정의, 상속, 다형성
  - 생성자 (`new()`), 메서드, 가상 메서드

## 3. 검증 기능

- **랜덤화**
  - `rand`, `randc` 키워드
  - `constraint` 블록을 통한 제약 조건 정의

- **어설션 (Assertions)**
  - 즉시 어설션 (`assert`)
  - 동시 어설션 (`assert property`)
  - SVA (SystemVerilog Assertions)

- **커버리지**
  - `covergroup`, `coverpoint`, `cross`

- **인터프로세스 통신**
  - `mailbox`, `semaphore`, `event`

## 4. 시뮬레이션 시간 제어

- `#`, `@`, `##` 등을 통한 시간 지연, 이벤트 대기
- `timeunit`, `timeprecision`, `timescale` 지시자

## 5. 디자인 계층 구조 및 네임스페이스

- 모듈 및 인스턴스 계층
- `package`를 통한 재사용 및 모듈화
- `import`, `export`를 통한 이름 공간 관리

## 6. 인터페이스와 Clocking block

- 인터페이스: 모듈 간 신호 그룹화
- Clocking block: 클럭 도메인 정의 및 동기화 제어
