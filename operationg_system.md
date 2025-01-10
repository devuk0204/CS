## 운영체제 개요
- 컴퓨터 하드웨어와 사용자, 응용 프로그램 간 중계자 역할을 하는 소프트웨어
- 시스템 자원을 관리하고, 응용 프로그램이 하드웨어을 효율적으로 사용할 수 있도록 지원하며, 사용자에게 인터페이스를 제공
### 운영체제의 역할과 목적	
- 컴퓨터 시스템의 효율성과 안전성을 보장하기 위함
- 자원 관리 
  - CPU, 메모리, 저장장치, 네트워크 자원 등 시스템 자원을 관리하여 응용 프로그램들이 자원을 공유하면서도 충돌 없이 실행될 수 있도록 관리
  - CPU 스케줄링 - 여러 프로세스가 CPU를 공유할 떄, 스케줄링 알고리즘을 통해 CPU자원을 분배
  - 메모리 관리 - 가상 메모리, 페이징, 세그멘테이션 등을 통해 메모리의 효율적인 사용과 보호 제공
  - 디스크 관리 - 파일 시스템을 통해 데이터 저장과 접근을 관리
- 사용자 인터페이스(UI, User Interface) 제공 
  - 사용자와 컴퓨터 시스템 간 상호작용을 가능하게 하는 인터페이스 제공
  - CLI(Command Line Interface) - 텍스트 기반의 명령어 입력을 통해 시스템을 제어
  - GUI(Graphic User Interface) - 아이콘, 윈도우, 메뉴 등을 사용하여 직관적인 인터페이스 제공
- 파일 시스템 관리
  - 파일 시스템을 제공해 파일의 생성, 삭제, 읽기, 쓰기 등을 수행하며, 데이터의 무결성과 보안을 보장
  - 파일 조직 - 디렉토리 구조, 파일 할당 방식 등을 통해 데이터를 논리적으로 조직
  - 데이터 보호 - 파일 접근 권한과 암호화를 통해 데이터의 보안 유지
- 보안 및 접근 제어 
  - 시스템 자원과 데이터에 대한 접근을 제어하고, 외부 위협으로부터 시스템을 보호
  - 사용자 인증 - 사용자 ID와 PW를 통해 접근 권한 확인
  - 권한 부여 - 사용자 및 그룹에 따라 자원에 대한 접근 권한 설정
  - 침입 방지 - 방화벽, 바이러스 검사 등을 통해 외부 공격으로부터 시스템 보호
### 운영체제의 구조 (Structure of Operating Systems)	
- 일반적으로 커널과 사용자 공간으로 구분
#### 커널(Kernel)
- 하드웨어와 직접 상호작용하며 시스템 자원을 관리
- 기능
	|구분|설명|
	|---|---|
	|프로세스 관리|	프로세스에 CPU를 배분하고 작업에 필요한 환경을 제공|
	|메모리 관리|프로세스에 작업 공간을 배치하고 실제 메모리보다 큰 가상공간을 제공|
	|파일 시스템 관리|데이터를 저장하고 접근할 수 있는 인터페이스를 제공|
	|입출력 관리|필요한 입력과 출력 서비스를 제공|
	|프로세스 간 통신 관리|공동 작업을 위한 각 프로세스 간 통신 환경을 지원|
#### 사용자 모드(User Mode) vs 커널 모드(Kernel Mode)
### 운영체제의 종류 (Types of Operating Systems)	
#### 단일 사용자/다중 사용자(Single-user/Multitasking)
#### 단일 작업/다중 작업(Single-tasking/Multitasking)
#### 분산 OS(Distributed Operating Systems)
#### 실시간 OS(Real-Time Operating Systems)
---
## 프로세스 관리 (Process Management)		
### 프로세스와 스레드 (Processes and Threads)	
#### 프로세스 상태(Process States) - 생성(New), 준비(Ready), 실행(Running), 대기(Waiting), 종료(Terminated)
#### 스레드(Thread) - 멀티스레딩(Multithreading)의 개념과 장점
### CPU 스케줄링 (CPU Scheduling)	
#### 선점형 스케줄링 (Preemptive Scheduling) - SJF (Shortest Job First), Priority Scheduling, Round Robin 등
#### 비선점형 스케줄링 (Non-preemptive Scheduling) - FCFS (First-Come-First-Served), Priority Scheduling 등
#### 스케줄링 성능 평가 (응답 시간, 대기 시간, 처리량 등)
### 동기화 (Synchronization)	
#### 임계 구역 문제 (Critical Section Problem)
#### 세마포어(Semaphore)와 모니터(Monitor)
#### 뮤텍스(Mutex)와 조건 변수(Condition Variables)
### 교착상태 (Deadlock)	
#### 교착상태의 조건 (Conditions for Deadlock)
#### 교착상태 해결 방법 (Deadlock Handling) - 예방(Prevention), 회피(Avoidance), 탐지(Detection), 복구(Recovery)
---	
## 메모리 관리 (Memory Management)		
### 메모리 계층 구조 (Memory Hierarchy)	
### 주기억장치 관리 (Main Memory Management)	
#### 단순 관리 (Simple Management) - 고정 분할(Fixed Partition), 가변 분할(Variable Partition)
#### 페이징(Paging)과 세그멘테이션(Segmentation)
#### 페이징과 세그멘테이션의 조합
### 가상 메모리 (Virtual Memory)	
#### 페이지 교체 알고리즘(Page Replacement Algorithms) - FIFO, LRU, Optimal
#### 스왑 공간 관리 (Swap Space Management)
---		
## 파일 시스템 (File System)		
### 파일의 개념과 구조 (Concept and Structure of Files)	
### 디렉토리 구조 (Directory Structure) 	
#### 단일 레벨(Single Level), 다중 레벨(Multi-Level), 트리 구조(Tree Structure)
### 파일 할당 방법 (File Allocation Methods)	
#### 연속 할당(Contiguous Allocation), 연결 할당(Linked Allocation), 색인 할당(Indexed Allocation)
### 파일 시스템 구현 (File System Implementation)	
#### 디스크 스케줄링 알고리즘 (Disk Scheduling Algorithms)  - FCFS, SSTF, SCAN, C-SCAN 등
#### 파일 시스템 무결성 (File System Integrity) - 저널링(Journaling), RAID(Redundant Array of Independent Disks)
---		
## 입출력 관리 (I/O Management)		
### I/O 하드웨어와 소프트웨어 (I/O Hardware and Software)	
### 장치 드라이버의 역할 (Role of Device Drivers)	
### 인터럽트와 폴링 (Interrupts and Polling)	
### DMA (Direct Memory Access)	
---		
## 운영체제의 보안 (Security in Operating Systems)		
### 사용자 인증 (User Authentication)	
### 접근 제어 (Access Control) - 접근 제어 리스트(ACL), 역할 기반 접근 제어(RBAC)	
### 암호화 및 데이터 보호 (Encryption and Data Protection)	
### 보안 정책과 공격 방지 기법 (Security Policies and Attack Mitigation) - 방화벽, IDS/IPS, 악성코드 탐지	
---	
## 분산 및 병렬 처리 (Distributed and Parallel Processing)		
### 분산 시스템의 개념과 특성 (Concepts and Characteristics of Distributed Systems)	
### 클러스터링 및 로드 밸런싱 (Clustering and Load Balancing)	
### 병렬 처리와 병렬 컴퓨팅 (Parallel Processing and Computing)	
### 동기화와 일관성 유지 (Synchronization and Consistency)	