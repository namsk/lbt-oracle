### Oracle 18c HR Database Install

Step 1. sysdba 계정으로 접속
```bash
$ sqlplus sys as sysdba
```

Step 2. Script 실행 가능하도록 설정
```bash
SQL> ALTER SESSION SET "_ORACLE_SCRIPT" = true;
```

Step 3. hr 설치 스크립트(sql) 실행
```bash
SQL> @?/demo/schema/human_resources/hr_main.sql
```

Step 3-1. HR 계정 비밀번호 입력
```bash
specify password for HR as parameter 1:
1의 값을 입력하십시오:hr
```

Step 3-2. 사용자의 테이블 공간 설정
```bash
specify default tablespeace for HR as parameter 2:
2의 값을 입력하십시오: users
```

Step 3-3. 임시 테이블 공간 설정
```bash
specify temporary tablespace for HR as parameter 3:
3의 값을 입력하십시오: temp
```

Step 3-4. 로그 기록 경로 설정
```bash
specify log path as parameter 4:
Enter value for 4: $ORACLE_HOME/demo/
```