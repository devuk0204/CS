## 컴퓨터구조와 개요 (Introduction to Computer Architecture)		
### 컴퓨터 구조란 무엇인가?	
- 정의 : 컴퓨터의 구성 요소간 
### 컴퓨터 시스템의 발전과 역사	
### 컴퓨터의 구성 요소 (Components of a Computer System)	
#### 중앙처리장치(CPU), 메모리, 입출력 장치 (I/O Devices)
### 폰노이만 아키텍처 (Von Neumann Architecture) vs. 하버드 아키텍처 (Harvard Architecture)	
### 컴퓨터 설계의 기본 원리 (Fundamental Principles of Computer Design)	
		
## 명령어 집합 구조(ISA, Instruction Set Architecture)		
### CISC (Complex Instruction Set Computer)	
### RISC (Reduced Instruction Set Computer)	
		
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
		
## 중앙처리장치 (CPU, Central Processing Unit)		
### CPU의 구조와 구성 요소 (CPU Architecture and Components)	
#### 산술 논리 장치(ALU, Arithmetic Logic Unit)
#### 레지스터 (Registers)
#### 제어 유닛(Control Unit)
### 명령어 사이클 (Instruction Cycle)	
#### 명령어 인출(Fetch), 해독(Decode), 실행(Execute), 메모리접근(Memory Access), ...
### 메모리 접근 방식 (Memory Access Methods)	
		
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
		
## 입출력 시스템 (I/O Systems)		
### 입출력 장치와 동작 원리 (I/O Devices and Operations)	
### 입출력 제어 방식 (I/O Control Mechanisms)	
#### 프로그램 제어(Programmed I/O)
#### 인터럽트 방식(Interrupt-driven I/O)
#### DMA(Direct Memory Access)
### 인터럽트 (Interrupts)	
### I/O 버스와 데이터 전송 (I/O Bus and Data Transfer)	
    
		
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
		
		
		
		
## 성능 평가와 최적화 (Performance Evaluation and Optimization)		
### 성능 측정 지표 (Performance Metrics)	
#### 처리량(Throughput), 응답 시간(Response Time), 클럭 주기(Clock Cycle)
### Amdahl의 법칙 (Amdahl's Law)	
### 시스템 성능 최적화 (System Performance Optimization)	
#### 캐시 최적화(Cache Optimization)
#### 분기 예측(Branch Prediction)