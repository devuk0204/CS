데이터베이스 개요		
	데이터베이스의 정의와 필요성	
	파일 시스템과 데이터베이스의 차이	
	데이터베이스의 특징: 무결성, 일관성, 보안	
	데이터베이스 관리 시스템(DBMS)의 역할과 구조	
	데이터베이스 모델의 종류	
		관계형 데이터베이스
		비관계형 데이터베이스(NoSQL)
		계층형, 네트워크형 모델
		
데이터 모델링		
	데이터 모델링 개념과 프로세스	
	ER(Entity-Relationship) 다이어그램	
		엔터티, 속성, 관계
	정규화	
		제1정규형(1NF), 제2정규형(2NF), 제3정규형(3NF)
		BCNF와 다섯 번째 정규형(5NF)
	비정규화와 성능 최적화	
		
관계형 데이터베이스		
	관계형 데이터베이스의 개념	
	키의 종류	
		기본 키, 후보 키, 외래 키
	릴레이션 연산	
		셀렉션(Selection), 프로젝션(Projection), 조인(Join)
		집합 연산(Union, Intersection, Difference)
		
SQL		
	SQL의 개요와 구성	
	데이터 정의 언어(DDL)	
		CREATE, ALTER, DROP
	데이터 조작 언어(DML)	
		SELECT, INSERT, UPDATE, DELETE
		JOIN과 서브쿼리
	데이터 제어 언어(DCL)	
		GRANT, REVOKE
	트랜잭션 제어 언어(TCL)	
		COMMIT, ROLLBACK, SAVEPOINT
		
트랜잭션과 동시성 제어		
	트랜잭션의 개념	
	트랜잭션 특성(ACID)	
	동시성 문제	
		갱신 손실, 비일관성 읽기, 비반복 읽기
	트랜잭션 격리 수준	
		Read Uncommitted, Read Committed, Repeatable Read, Serializable
	동시성 제어 기법	
		잠금(Locking)과 타임스탬프
		
데이터베이스 설계		
	데이터베이스 설계 단계	
		요구사항 분석, 논리적 설계, 물리적 설계
	스키마 설계	
		개념 스키마, 논리 스키마, 물리 스키마
	인덱스 설계	
		클러스터드 인덱스와 비클러스터드 인덱스
		B-Tree, Hash 인덱스
		
데이터 무결성과 보안		
	무결성 제약 조건	
		기본 키, 외래 키, 고유성, 도메인
	보안과 권한 관리	
		사용자 인증과 역할
		데이터 암호화와 전송 보안
		
데이터베이스 성능 최적화		
	실행 계획(Execution Plan) 분석	
	쿼리 최적화	
		인덱스 활용
		정규화와 비정규화의 균형
	파티셔닝	
		수평 파티셔닝과 수직 파티셔닝
	샤딩과 데이터 분산	
		
비관계형 데이터베이스 (NoSQL)		
	NoSQL 개요와 특징	
	NoSQL의 유형	
		키-값 저장소: Redis, DynamoDB
		문서형 데이터베이스: MongoDB, CouchDB
		열 기반 데이터베이스: Cassandra, HBase
		그래프 데이터베이스: Neo4j
	CAP 이론과 BASE 모델	
		
분산 데이터베이스		
	분산 데이터베이스의 개념	
	데이터 복제	
		마스터-슬레이브 복제
		리더-팔로워 복제
	분산 트랜잭션	
		2PC(2-Phase Commit)
	분산 시스템의 데이터 일관성	
		
데이터베이스 관리 및 백업		
	백업 전략	
		풀 백업, 증분 백업, 차등 백업
	장애 복구	
		로그 기반 복구와 체크포인트
	데이터베이스 모니터링	