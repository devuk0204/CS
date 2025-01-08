## 컴퓨터구조와 개요 (Introduction to Computer Architecture)		
### 컴퓨터 구조란 무엇인가?	
- 정의 
    -  컴퓨터 시스템의 기능, 조직, 구현에 대한 법칙과 방법
    -  컴퓨터 시스템의 구성 요소와 그들 간의 상호 작용을 설명하는 개념으로, 하드웨어와 소프트웨어의 상호 작용을 포함
### 컴퓨터 시스템의 발전과 역사	
역사
### 컴퓨터의 구성 요소 (Components of a Computer System)
#### 중앙처리장치(CPU) [바로가기](#중앙처리장치-cpu-central-processing-unit)
- 정의
    -  컴퓨터 시스템에서 명령어를 해석하고 실행하는 장치
    -  데이터의 처리와 제어 흐름을 담당
#### 메모리(Memory) [바로가기](#메모리-구조-memory-architecture)
- 정의
    -  컴퓨터 시스템 내에서 데이터와 명령어를 저장하고, 필요할 때 접근할 수 있도록 하는 하드웨어 장치
    -  주기억장치(Primary memory)와 보조기억장치(Secondary Storage)로 구분된다
- 종류
    -  주기억장치
       -  ROM(Read Only Memory) - 컴퓨터 전원이 끊어져도 기록된 데이터들이 소멸하지 않는 비휘발성 메모리로, BIOS와 같은 주요 데이터를 저장한다
       -  RAM(Random Access Memory) - 전원이 끊어지면 기록된 데이터들이 소멸하는 휘발성 메모리이며, 읽고 쓰기가 가능함 
    -  보조기억장치
       -  HDD(Hard Disk Drive) - 자기 디스크를 사용해 데이터를 저장하는 장치, 회전하는 플래터와 읽기/쓰기 헤더를 이용함
       -  SDD(Solid State Drive) - 반도체를 이용하여 데이터를 저장하는 장치, 플래시 메모리를 사용하고, HDD와 비교해 작교 가벼우며 처리 속도가 빠름
       -  USB(Universal Serial Bus) - USB 포트에 꽂아 사용하는 이동형 저장장치, 플래시 메모리를 사용함
#### 입출력 장치 (I/O Devices) [바로가기](#입출력-시스템-io-systems)
- 정의
    -  컴퓨터 시스템과 외부 환경 간의 데이터 교환을 가능하게 하는 하드웨어 장치
- 종류
    -  입력장치 - 키보드, 마우스, 터치스크린, 스캐너 등
    -  출력장치 - 모니터, 프린터, 스피커 등
    -  입출력장치 - 터치스크린, 모뎀, 네트워크 카드, 외장 하드 등
### 폰노이만 아키텍처 (Von Neumann Architecture) vs. 하버드 아키텍처 (Harvard Architecture)	
- 폰 노이만 아키텍쳐
    -  프로그램과 데이터를 동일한 메모리에 저장하고, CPU가 메모리에서 명령어를 순차적으로 가져와 실행하는 컴퓨터 설계 모델
    -  구성 요소 - CPU, Memory, I/O Devices, Bus
    -  특징
       -   프로그램과 데이터를 동일한 메모리에 저장함으로써, 프로그램의 수정과 데이터의 접근이 용이
       -   명령어를 순차적으로 처리함으로써, 프로그램의 흐름을 예측 가능하게 함
    -  작동 원리   
        1. 페치(Fetch) - 프로그램 카운터(PC, Program Counter)에 저장된 메모리 주소에서 명령어를 가져옴
        2. 디코드(Decode) - 가져온 명령어의 연산 코드(OP code)를 분석하고, 필요한 데이터의 연산 방식을 파악
        3. 실행(Excute) - ALU를 사용하여 산술 또는 논리 연산을 수행하고, 결과를 레지스터나 메모리에 저장
        4. 반복 - 다음 명령어의 주소를 프로그램 카운터에 업데이트하고, 다시 페치 단계로 돌아감
- 하버드 아키텍쳐
### 컴퓨터 설계의 기본 원리 (Fundamental Principles of Computer Design)	
--- 	
## 명령어 집합 구조(ISA, Instruction Set Architecture)		
### CISC (Complex Instruction Set Computer)	
### RISC (Reduced Instruction Set Computer)	
--- 
## 데이터 표현 및 연산 (Data Representation and Operations)		
### 수의 체계 (Number Systems)	
#### 이진수(Binary), 8진수(Octal), 16진수(Hexadecimal) 표현
#### 체계 간 변환
### 정수와 실수 표현 (Integer and Floating-Point Representation)	
#### 고정소수점과 부동소수점
#### IEEE 754 표준 (IEEE 754 Standard) - 표현, 정밀도, 반올림
### 데이터 연산 (Data Operations)	
#### 산술 연산 (Arithmetic Operations)
#### 논리 연산 (Logical Operations)
#### 시프트 연산 (Shift Operations)
### SIgned vs. Unsigned 데이터	
--- 	
## 중앙처리장치 (CPU, Central Processing Unit)		
### CPU의 구조와 구성 요소 (CPU Architecture and Components)	
          -  산술 논리 장치(ALU, Arithmetic Logic Unit) - 산술 연산과 논리 연산 수행
          -  제어 장치(Control Unit) - 명령어 해석, ALU와 메모리 간 데이터 흐름 제어
          -  레지스터(Register) - CPU 내부에서 데이터를 일시적으로 저장
#### 산술 논리 장치(ALU, Arithmetic Logic Unit)
#### 레지스터 (Registers)
#### 제어 유닛(Control Unit)
### 명령어 사이클 (Instruction Cycle)	
#### 명령어 인출(Fetch), 해독(Decode), 실행(Execute), 메모리접근(Memory Access), ...
### 메모리 접근 방식 (Memory Access Methods)	
--- 		
## 메모리 구조 (Memory Architecture)		
### 메모리 계층 구조 (Memory Hierarchy)	
### 캐시 메모리 (Cache Memory)	
#### 직접 매핑(Direct Mapping)
#### 집합 연관(Set-Associative)
#### 완전 연관(Fully Associative)
#### 캐시 적중률(Cache Hit Rate)
### 가상 메모리 (Virtual Memory)	
#### 페이징(Paging)
#### 세그멘테이션(Segmentation)
#### 페이지 교체 알고리즘
##### LRU
##### FIFO
##### 최적 교체(Optimal Replacement)
### TLB (Translation Lookaside Buffer)	
--- 		
## 입출력 시스템 (I/O Systems)		
### 입출력 장치와 동작 원리 (I/O Devices and Operations)	
### 입출력 제어 방식 (I/O Control Mechanisms)	
#### 프로그램 제어(Programmed I/O)
#### 인터럽트 방식(Interrupt-driven I/O)
#### DMA(Direct Memory Access)
### 인터럽트 (Interrupts)	
### I/O 버스와 데이터 전송 (I/O Bus and Data Transfer)	
--- 		
## 프로세서 설계 (Processor Design)		
### 데이터 경로 설계 (Datapath Design)	
#### 단일 사이클(Single-Cycle Design)
#### 멀티 사이클(Multi-Cycle Design)
### 제어 유닛 설계 (Control Unit Design)	
#### 하드와이어드 제어 (Hardwired Control)
#### 마이크로프로그램 제어 (Microprogrammed Control)
### 파이프라인 처리 (Pipelining)	
#### 파이프라인의 개념과 이점
#### 위험 요소(Hazards)
##### 데이터 위험(Data Hazards)
##### 제어 위험(Control Hazards)
##### 구조적 위험(Structural Hazards)
--- 	
## 성능 평가와 최적화 (Performance Evaluation and Optimization)		
### 성능 측정 지표 (Performance Metrics)	
#### 처리량(Throughput), 응답 시간(Response Time), 클럭 주기(Clock Cycle)
### Amdahl의 법칙 (Amdahl's Law)	
### 시스템 성능 최적화 (System Performance Optimization)	
#### 캐시 최적화(Cache Optimization)
#### 분기 예측(Branch Prediction)