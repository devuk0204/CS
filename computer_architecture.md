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
- 폰 노이만 아키텍처
    -  프로그램과 데이터를 동일한 메모리에 저장하고, CPU가 메모리에서 명령어를 순차적으로 가져와 실행하는 컴퓨터 설계 모델
    -  구성 요소 - CPU, Memory, I/O Devices, Bus
    -  특징
       -   프로그램과 데이터를 동일한 메모리에 저장함으로써, 프로그램의 수정과 데이터의 접근이 용이
       -   명령어를 순차적으로 처리함으로써, 프로그램의 흐름을 예측 가능하게 함
    -  구조
        ![폰 노이만 아키텍처](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e5/Von_Neumann_Architecture.svg/250px-Von_Neumann_Architecture.svg.png)   
        Image source : https://commons.wikimedia.org/wiki/File:Von_Neumann_Architecture.svg

- 하버드 아키텍처
    -  명령어와 데이터를 별도의 메모리 공간에 저장하고, 독립적인 버스를 통해 접근하는 컴퓨터 설계 모델
    -  구성 요소 - CPU, Instruction Memory, Data Memory, I/O Devices, Instruction Bus, Data Bus
    -  특징
       -  명령어와 데이터를 별도의 메모리 공간에 저장함으로써, 두 공간에 동시에 접근하고 처리 가능하여 처리 속도가 빠름
       -  명령어 버스와 데이터 버스가 분리되어 있어, 병목 현상이 줄어들고, 데이터 전송의 병렬성이 확보되어 고속 데이터 처리와 실시간 연산이 요구되는 시스템에 유리
    -  구조
        ![하버드 아키텍처](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Harvard_architecture.svg/220px-Harvard_architecture.svg.png)   
        Image source : https://commons.wikimedia.org/wiki/File:Harvard_architecture.svg
- 폰 노이만 아키텍처와 하버드 아키텍처의 차이점
    -  메모리에 접근하는 법이 다름
    -  폰 노이만 아키텍처는 하나의 메모리에 명령어와 데이터를 저장해두고 접근하는 반면, 하버드 아키텍처는 명령어 메모리와 데이터 메모리를 따로 두고, 병렬 접근 가능

### 컴퓨터 설계의 기본 원리 (Fundamental Principles of Computer Design)	

--- 	
## 명령어 집합 구조(ISA, Instruction Set Architecture)		
- 정의 
    -  주어진 아키텍처가 실행할 수 있는 명령어들의 집합과 그 명령어들의 형식, 동작 빙식, 주소 지정 방식 등을 포함하는 설계 규칙
    -  하드웨어와 소프트웨어 사이의 인터페이스
### CISC (Complex Instruction Set Computer)	
- 정의
    -  복잡하고 다양한 명령어를 포함하는 명령어 집합 구조를 가진 컴퓨터 아키텍처
- 특징
    -  가변 길이 명령어를 가질 수 있어 명령어의 복잡성과 다양성을 증가시킴, 이를 통해 더 많은 기능을 하나의 명령어로 구현
    -  다양한 주소 지정 방식을 지원하여 데이터 접근 방법의 유언성을 제공하고, 복잡한 데이터 구조를 쉽게 처리 가능함
- 장점 
    -  복잡한 명령어를 사용하여 작업을 수행하는데 필요한 명령어 수가 줄어들어 코드의 밀도가 높아질 수 있음
    -  많은 기능을 하나의 명령어로 구현할 수 있어, 하드웨어의 복잡성을 숨기고 추상화된 인터페이스를 제공할 수 있음
- 단점
    -  복잡한 명령어 집합과 마이크로코드의 사용으로 CPU설계가 복잡해짐
    -  명렁어가 복잡하고 길이가 가변적이기 때문에, 효율적인 파이프라이닝을 구현하기 어려움
    -  하드웨어가 복잡한 명령어를 처리해야 하기 때문에, RISC에 비해 명령어의 실행 속도가 느림
-  예시
    -  Intel x86 아키텍처 CPU, AMD x86 호환 CPU, 모토로라 68000 시리즈, IBM 메인프레임 CPU 등
### RISC (Reduced Instruction Set Computer)	
- 정의
    -  단순하고, 고속의 명령어 집합을 사용하는 컴퓨터 아키텍처
- 특징
    -  명령어의 복잡성을 줄여 단순한 구조로 설계되고, 명령어 길이가 고정되어 있음
    -  레지스터를 적극적으로 사용하여 메모리 접근을 최소화함
    -  데이터 메모리에 접근하는 명령어(로드/스토어)와 데이터 레지스터간의 연산을 분리하여 처리
- 장점
    -  단순하고 고정된 명령어 구조로, 파이프라이닝을 효과적으로 구현할 수 있음
    -  복잡한 명령어 처리가 필요 없기 때문에, 전력 소비가 적고, 에너지 효율성이 높아 모바일 및 임베디드 시스템에 적합
- 단점
    -  하나의 복잡한 명령어를 여러 단순한 명령어로 구현해야 하기 때문에, 전체 명령어 수가 증가하여 코드의 길이가 길어질 수 있음
    -  데이터 메모리에 접근하는 명령어가 별도로 존재하기 때문에, 복잡한 메모리 연산을 직접 지원하지 않음
    -  많은 레지스터를 필요로 해서 하드웨어 설계가 복잡하고, 레지스터 수가 제한적일 경우 성능 저하로 이어질 수 있음
- 예시
    -  Apple A시리즈 칩, Qualcomm Snapdragon 시리즈, AWS Graviton 프로세서 등
--- 
## 데이터 표현 및 연산 (Data Representation and Operations)		
### 수의 체계 (Number Systems)
- 컴퓨터는 우리가 흔히 일생상활에서 사용하는 10진수가 아닌, 2진수, 8진수와 16진수를 사용
- 컴퓨터는 전자 신호의 ON(1)과 OFF(0) 상태를 기반으로 작동하기 때문에 2진법 기반의 숫자 체계를 사용
#### 2진수(Binary), 8진수(Octal), 16진수(Hexadecimal) 표현
- 2진수
    -  0과 1 두 가지 숫자만을 사용하여 수를 표현하는 체계
    -  각 자릿수가 하나의 bit이며, 2의 거듭제곱수를 나타냄
    -  $n$개 자릿수를 가진 이진수라면 $2^0$부터 시작하여 $2^{n-1}$까지가 각 자릿수에 대응
    -  예시
       -  2진수 $1001$을 10진수로 변환하면 $1*2^3 + 0*2^2 + 0*2^1 + 1*2^0$으로 $9$
       -  10진수 $7$을 2진수로 변환하면 $1*2^2 + 1*2^1 + 1*2^0$이므로 $111$
- 8진수
    -  0부터 7까지 8개의 숫자를 사용하여 수를 표현하는 체계
    -  8진수 한 자릿수가 2진수 3bit와 대응하며, 8의 거듭제곱수를 나타냄
    -  $n$개 자릿수를 가진 8진수라면 $8^0$부터 시작하여 $8^{n-1}$까지가 각 자릿수에 대응
    -  예시
       -  8진수 $101$을 10진수로 변환하면 $1*8^2 + 0*8^1 + 1*8^0$으로 $65$
       -  10진수 $18$을 8진수로 변환하면 $2*8^1 + 2*8^0$이므로 $22$
- 16진수
    -  0부터 9까지와 A부터 F(A : 10 ~ F : 15)까지 6개의 문자, 총 16개의 숫자로 수를 표현하는 체계
    -  각 자릿수가 2진수 4bit에 대응하며, 16의 거듭제곱수를 나타냄
    -  $n$개 자릿수를 가진 16진수라면 $16^0$부터 시작하여 $16^{n-1}$까지가 각 자릿수에 대응
    -  예시
       -  16진수 FA를 10진수로 변환하면 $F(15)*16^1 + A(10)*16^0$으로 $250$
       -  10진수 $720$를 16진수로 변환하면 $2*16^2 + D(13)*16^1 + 0*16^0$이므로 $2D0$
#### 체계 간 변환
- 2진수 - 8진수 변환
    - 8진수의 한 자리가 2진수의 3bit에 대응하므로 2진수를 오른쪽부터 세자리씩 끊어서 8진수로 변환한 후 순서대로 결합
    - 8진수를 2진수로 변환할때는 8진수 한 자리를 2진수 3bit로 변환한 후 순서대로 결합
    - 예시
      -  2진수 $1 101 011$을 8진수로 변환하면 $001 | 101 | 011$ -> $1 | 5 | 3$ 이므로 $153$
      -  8진수 $161$을 2진수로 변환하면 $1 | 6 | 1$ -> $001 | 110 | 001$ 이므로 $1110001$
- 2진수 - 16진수 변환
    - 16진수의 한 자리가 2진수의 4bit에 대응하므로 2진수를 오른쪽부터 네자리씩 끊어서 16진수로 변환한 후 순서대로 결합
    - 16진수를 2진수로 변환할때는 16진수 한 자리를 2진수 4bit로 변환한 후 순서대로 결합
    - 예시
      -  2진수 $111 0010 1001$을 16진수로 변환하면 $0111|0010|1001$ -> $7|2|9$이므로 $729$
      -  16진수 $C A 8$을 2진수로 변환하면 $C|A|8$ -> $1101|1010|1000$이므로 $110110101000$
- 8진수 - 16진수 변환
      - 8진수에서 16진수로 변환할때는, 8진수를 2진수로 변환 후 16진수로 변환
      - 16진수를 8진수로 변환할때는, 16진수를 2진수로 변환 후 8진수로 변환
### 정수와 실수 표현 (Integer and Floating-Point Representation)	
- 정수는 기본적으로 2진수를 통해 표현하며, 
#### 고정소수점과 부동소수점
#### IEEE 754 표준 (IEEE 754 Standard) - 표현, 정밀도, 반올림
### 데이터 연산 (Data Operations)	
#### 산술 연산 (Arithmetic Operations)
#### 논리 연산 (Logical Operations)
#### 시프트 연산 (Shift Operations)
### Signed vs. Unsigned 데이터	
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