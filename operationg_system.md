운영체제 개요		
	운영체제의 역할과 목적	
	운영체제의 구조 (Structure of Operating Systems)	
		커널(Kernel)
		사용자 모드(User Mode) vs 커널 모드(Kernel Mode)
	운영체제의 종류 (Types of Operating Systems)	
		단일 사용자/다중 사용자(Single-user/Multitasking)
		단일 작업/다중 작업(Single-tasking/Multitasking)
		분산 OS(Distributed Operating Systems)
		실시간 OS(Real-Time Operating Systems)
		
프로세스 관리 (Process Management)		
	프로세스와 스레드 (Processes and Threads)	
		프로세스 상태(Process States) - 생성(New), 준비(Ready), 실행(Running), 대기(Waiting), 종료(Terminated)
		스레드(Thread) - 멀티스레딩(Multithreading)의 개념과 장점
	CPU 스케줄링 (CPU Scheduling)	
		선점형 스케줄링 (Preemptive Scheduling) - SJF (Shortest Job First), Priority Scheduling, Round Robin 등
		비선점형 스케줄링 (Non-preemptive Scheduling) - FCFS (First-Come-First-Served), Priority Scheduling 등
		스케줄링 성능 평가 (응답 시간, 대기 시간, 처리량 등)
	동기화 (Synchronization)	
		임계 구역 문제 (Critical Section Problem)
		세마포어(Semaphore)와 모니터(Monitor)
		뮤텍스(Mutex)와 조건 변수(Condition Variables)
	교착상태 (Deadlock)	
		교착상태의 조건 (Conditions for Deadlock)
		교착상태 해결 방법 (Deadlock Handling) - 예방(Prevention), 회피(Avoidance), 탐지(Detection), 복구(Recovery)
		
메모리 관리 (Memory Management)		
	메모리 계층 구조 (Memory Hierarchy)	
	주기억장치 관리 (Main Memory Management)	
		단순 관리 (Simple Management) - 고정 분할(Fixed Partition), 가변 분할(Variable Partition)
		페이징(Paging)과 세그멘테이션(Segmentation)
		페이징과 세그멘테이션의 조합
	가상 메모리 (Virtual Memory)	
		페이지 교체 알고리즘(Page Replacement Algorithms) - FIFO, LRU, Optimal
		스왑 공간 관리 (Swap Space Management)
		
파일 시스템 (File System)		
	파일의 개념과 구조 (Concept and Structure of Files)	
	디렉토리 구조 (Directory Structure) 	
		단일 레벨(Single Level), 다중 레벨(Multi-Level), 트리 구조(Tree Structure)
	파일 할당 방법 (File Allocation Methods)	
		연속 할당(Contiguous Allocation), 연결 할당(Linked Allocation), 색인 할당(Indexed Allocation)
	파일 시스템 구현 (File System Implementation)	
		디스크 스케줄링 알고리즘 (Disk Scheduling Algorithms)  - FCFS, SSTF, SCAN, C-SCAN 등
		파일 시스템 무결성 (File System Integrity) - 저널링(Journaling), RAID(Redundant Array of Independent Disks)
		
입출력 관리 (I/O Management)		
	I/O 하드웨어와 소프트웨어 (I/O Hardware and Software)	
	장치 드라이버의 역할 (Role of Device Drivers)	
	인터럽트와 폴링 (Interrupts and Polling)	
	DMA (Direct Memory Access)	
		
운영체제의 보안 (Security in Operating Systems)		
	사용자 인증 (User Authentication)	
	접근 제어 (Access Control) - 접근 제어 리스트(ACL), 역할 기반 접근 제어(RBAC)	
	암호화 및 데이터 보호 (Encryption and Data Protection)	
	보안 정책과 공격 방지 기법 (Security Policies and Attack Mitigation) - 방화벽, IDS/IPS, 악성코드 탐지	
		
분산 및 병렬 처리 (Distributed and Parallel Processing)		
	분산 시스템의 개념과 특성 (Concepts and Characteristics of Distributed Systems)	
	클러스터링 및 로드 밸런싱 (Clustering and Load Balancing)	
	병렬 처리와 병렬 컴퓨팅 (Parallel Processing and Computing)	
	동기화와 일관성 유지 (Synchronization and Consistency)	