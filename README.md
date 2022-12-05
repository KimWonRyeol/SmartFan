# SmartFan
객체 추적 기반 스마트 선풍기

- 2022년도 2학기 임베디드시스템 1분반 1조 Apple Pi 팀
- 20200252 김원렬, 20200370 김혜진, 20200573 서준혁

## 기능
### 본체 회전 모드 설정
- 일반 회전 모드: 정해진 구간을 반복하여 회전한다.
- 객체 유도 모드: 사용자를 객체로 인식하여 객체를 따라가면서 회전한다.
- 고정 모드: 선풍기 머리를 고정하여 회전하지 않는다.
### 타이머 설정
- 사용자로부터 시간을 입력받는다. (1분 ~ 60분)
- 입력 받은 시간이 지나면 자동으로 본체 회전과 팬 회전을 종료한다.
### 바람 세기 설정
- 사용자로부터 바람 세기를 입력받아 팬의 회전 세기를 변경한다.
- 0: 종료, 1: 미풍, 2: 약풍, 3: 강풍
### 통신
- 모든 통신은 스마트폰과 블루투스로 연결하여 명령을 입력받는다.

<br/>

## 모듈
- Fan: Keyes140C04 모듈(L9110 모터 드라이버+DC 모터)
- 선풍기 본체 회전: 서보 모터
- 시간 계산: RTC 칩(DS3231)
- 객체 탐지: 초음파 센서
- 통신: UART 블루투스 모듈(HC-06)
- 3단계 세기 표현: LED 3개

<br/>

## 역할 분담
| 학번 | 이름 | 역할 |
|--------|-----|-------------------------------------------------------------|
|20200252|김원렬|📝회의 내용 기록<br/>🔡회로 구성<br/>👨‍💻객체 탐지 기능 구현<br/>🙋🏻‍♂구현 내용 시연|
|20200370|김혜진|👩‍👦‍👦프로젝트 총괄, 회의 진행 독려<br/>👩‍💻회전, 세기 조정 기능 구현|
|20200573|서준혁|🔡회로 구성<br/>👨‍💻통신 기능, 멀티프로세싱 구현<br/>🙋🏻‍♂최종 발표|

<br/>

## 개발 일정
| 기간 | 기능 | 진행 |
|------|-----|------|
|11/28~12/4|제작 계획 수립, 프로젝트 기획|O|
|12/5~12/9|회로 구성, 통신 인터페이스 명세, 회전/세기 조정 기능 구현, 객체 탐지 기능 구현||
|12/10~12/13|통신 및 테스트, 디버깅||
|12/14~12/20|보고서 작성||
|12/16, 12/20|결과 및 최종 데모 발표||
