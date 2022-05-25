# 조사내용 README파일로 정리하기
광기술 공학과 20161682 최은창

## top, ps, jobs, kill 명령어</br>

 ### top 명령어 

top 명령어는 리눅스 계열 서버의 OS 상태를 확인할 수 있는 CLI 어플리 케이션이다.

top 명령어를 통해 서버의 CPU 사용량, 메모리 사용량 등을 확인할 수 있으며, 

서버에서 구동 중인 모든 어플리케이션들을 CPU 사용률이나 메모리 사용률이 많은 순서대로 나열하여 모니터링이 가능한 명령어이다.


 * #### 사용법

사용법은 간단하다. 리눅스에서 top 명령어를 치고 들어가면 된다. 

리눅스 서버에서 top 명령어를 입력하면 다음과 같은 결과를 얻을 수 있다.

` $ top `

<그림>

위 그림처럼 top명령어는 밑줄친 부분으로 나눠서 윗부분과 아랫부분으로 나누어 볼 수 있다. 

윗 부분은 주로 현재 시스템의 상태를 보여주는데, 시스템 시간이나 uptime 등을 확인 해 볼 수 있고

아랫부분은 현재 실행하고 있는 프로세스 현황을 볼 수 있다.

* #### Top 정보 시스템 내용

13:47:52 : 현재 서버의 시간

9 day, 5:24 : uptime(켜져있는시간)

3 users : 유저

load average : 현재 시스템이 얼마나 일을 하고 있는지 1분, 5분, 15분 단위로 실행/대기 중인 프로세스 수를 나타내고 있음 

tasks : 프로세스 개수

* #### CPU

%us : 유저레벨에서 사용하고 있는 CPU 비중

%sy : 시스템 레벨에서 사용하고 있는 CPU 비중

%id: 유휴 상태의 CPU 비중

%wa : 시스템이 I/O 요청을 처리하지 못한 상태에서의 CPU idle 상태인 비중

일반적으로 %us와 %sy를 더한 값이 CPU 사용률이라고 보면 되며, id 값이 여유 cpu라고 보면 된다.

그 외에 wa 나 ni 등의 값들이 크다면 원인 분석이 필요할 수 있다.


* #### 프로세스 

PID : 프로세스 ID (PID)

USER : 프로세스를 실행시킨 사용자 ID

PRI : 프로세스의 우선순위(priority)

NI : NICE 값, 일의 nice valuce값이다. 마이너스를 가지는 ncie value는 우선순위가 높음.

VIRT : 가상 메모리의 사용량(SWAP+RES)

RES : 현재 페이지가 상주하고 있는 크기(Resident Size)

SHR : 분할된 페이지, 프로세스에 의해 사용된 메모리를 나눈 메모리의 총합.

S : 프로세스의 상태 [S(sleeping), R(running), W(swapped out process), Z(zombies)]

%CPU : 프로세스가 사용하는 CPU의 사용율

%MEM : 프로세스가 사용하는 메모리의 사용율

COMMAND : 실행된 명령어

#### Top 명령어 옵션
먼저 top 명령은 어플리케이션이기 때문에 실행 시 옵션과 실행 후 옵션이 있다.

`$ top [옵션]`

|옵션|설명|
|----|----|
|1|CPU 코어별 사용 현황|
|m|메모리 사용률 시각화 표시|
|shift+p|CPU 사용률이 높은 프로세스를 기준으로 나열|
|shift+m|메모리 사용률이 높은 프로세스를 기준으로 나열|
|shift+t|수행 시간이 긴 프로세스를 기준으로 나열|
|k|kill 할 프로세스 PID를 입력할 수 있음|
|H|상단의 Tasks 기준을 쓰레드로 변경|
|u|모니터링할 user를 선택하여, 해당 권한 프로세스 감시|

* ### ps 명령어 

<img width="399" alt="스크린샷 2022-05-25 오전 9 16 01" src="https://user-images.githubusercontent.com/83526046/170152352-0ad1ec1f-d3f1-4983-ae49-bb34951e5c07.png">

ps명령어는 현재 리눅스 시스템에서 실행 중인 프로세스에 대한 정보들을 출력하는 명렁어이다.

(이 명령어를 자주 사용하는 이유는 프로세스 사용을 중지시킬 kill명령어로 중지 시킬경우 PID정보가 필요하기 때문이다.)

PID : 프로세스 ID

TTY : 프로세스 입출력 담당 터미널

TIME : 구동시간

CMD : 프로세스 실행 명령어
 
 **-f 옵션 사용시**
 
 UID : 실행 유저
 
 PPID : 부모 프로세스 PID
 
 C : CPU 사용량
 
 STIME : 프로세스 시작 시간


` $ ps -[옵션] `

|옵션|설명|
|----|----|
|-e|모든 프로세스를 출력해준다.|
|-f|풀 포멧으로 보여둔다.(UID, PID 등)|
|-l|긴 포멧으로 보여준다.|
|p,-p|특정 PID의 프로세스를 보여준다.|
|-u|특정 사용자의 프로세스를 보여준다.|


## vim 에디터에서 매크로 활용방법
