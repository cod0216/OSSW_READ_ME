# 📖 조사내용 README파일로 정리하기
🎓광기술 공학과 20161682 최은창

## top, ps, jobs, kill 명령어

[1. top 명령어](#-top-명령어)

[2. ps 명령어](#-ps-명령어)

[3. jobs 명령어](#-jobs-명령어)

[4. kill 명령어](#-kill-명령어)


### ✏️ top 명령어

top 명령어는 리눅스 계열 서버의 OS 상태를 확인할 수 있는 CLI 어플리 케이션이다.

top 명령어를 통해 서버의 CPU 사용량, 메모리 사용량 등을 확인할 수 있다

 * #### 사용법

리눅스에서 top 명령어를 치고 들어가면 된다. 

` $ top `


<img width="1440" alt="스크린샷 2022-05-29 오후 6 40 23" src="https://user-images.githubusercontent.com/83526046/170861804-f13387a4-34fd-4409-bffe-7eea0c4c0067.png">
 


위 그림처럼 top명령어는 ***윗부분***과 ***아랫부분***으로 나누어 볼 수 있다. 

윗 부분은 주로 현재 시스템의 상태를 보여주는데, 시스템 시간이나 uptime 등을 확인 해 볼 수 있고

아랫부분은 현재 실행하고 있는 프로세스 현황을 볼 수 있다.

* #### Top 정보 시스템 내용

|내용|설명|
|:----:|:----|
|18:40:23|현재 서버의 시간|
|9 day, 5:24|uptime(켜져있는시간)|
|3 users|유저|
|load average|현재 시스템이 얼마나 일을 하고 있는지 1분, 5분, 15분 단위로 실행/대기 중인 프로세스 수를 나타내고 있음|
|tasks|프로세스 개수|

* #### CPU
|내용|설명|
|:----:|:----|
|%us|유저레벨에서 사용하고 있는 CPU 비중|
|%sy|시스템 레벨에서 사용하고 있는 CPU 비중|
|%id|유휴 상태의 CPU 비중|
|%wa|시스템이 I/O 요청을 처리하지 못한 상태에서의 CPU idle 상태인 비중|
|tasks|프로세스 개수|

>일반적으로 %us와 %sy를 더한 값이 CPU 사용률이라고 보면 되며, id 값이 여유 cpu라고 보면 된다.
>그 외에 wa 나 ni 등의 값들이 크다면 원인 분석이 필요할 수 있다.









* #### 프로세스 

|내용|설명|
|:----:|:----|
|PID|프로세스 ID (PID)|
|USER|프로세스를 실행시킨 사용자 ID|
|PRI|프로세스의 우선순위(priority)|
|NI|NICE 값, 일의 nice valuce값이다. 마이너스를 가지는 ncie value는 우선순위가 높음.|
|VIRT|가상 메모리의 사용량(SWAP+RES)|
|RES|현재 페이지가 상주하고 있는 크기(Resident Size)|
|SHR|분할된 페이지, 프로세스에 의해 사용된 메모리를 나눈 메모리의 총합.|
|S|프로세스의 상태 [S(sleeping), R(running), W(swapped out process), Z(zombies)]|
|%CPU|프로세스가 사용하는 CPU의 사용율|
|%MEM|프로세스가 사용하는 메모리의 사용율|
|COMMAND|실행된 명령어|

* #### Top 명령어 옵션

먼저 top 명령은 어플리케이션이기 때문에 실행 시 옵션과 실행 후 옵션이 있다.

|옵션|설명|
|:----:|:----|
|1|CPU 코어별 사용 현황|
|m|메모리 사용률 시각화 표시|
|shift+p|CPU 사용률이 높은 프로세스를 기준으로 나열|
|shift+m|메모리 사용률이 높은 프로세스를 기준으로 나열|
|shift+t|수행 시간이 긴 프로세스를 기준으로 나열|
|k|kill 할 프로세스 PID를 입력할 수 있음|
|H|상단의 Tasks 기준을 쓰레드로 변경|
|u|모니터링할 user를 선택하여, 해당 권한 프로세스 감시|

---
### ✏️ ps 명령어

<img width="399" alt="스크린샷 2022-05-25 오전 9 16 01" src="https://user-images.githubusercontent.com/83526046/170152352-0ad1ec1f-d3f1-4983-ae49-bb34951e5c07.png">

ps명령어는 현재 리눅스 시스템에서 실행 중인 프로세스에 대한 정보들을 출력하는 명렁어이다.

> 이 명령어를 자주 사용하는 이유는 프로세스 사용을 중지시킬 kill명령어로 중지 시킬경우 PID정보가 필요하기 때문이다.

|내용|설명|
|:----:|:----|
|PID|프로세스 ID|
|TTY|프로세스 입출력 담당 터미널|
|TIME|구동시간|
|CMD|프로세스 실행 명령어|
 
 **-f 옵션 사용시**
 
|내용|설명|
|:----:|:----|
|UID|실행 유저|
|PPID|부모 프로세스 PID|
|C|CPU 사용량|
|STIME|프로세스 시작 시간|

* #### ps 명령어 옵션

` $ ps -[옵션] `

|옵션|설명|
|:----:|:----|
|-e|모든 프로세스를 출력해준다.|
|-f|풀 포멧으로 보여둔다.(UID, PID 등)|
|-l|긴 포멧으로 보여준다.|
|p,-p|특정 PID의 프로세스를 보여준다.|
|-u|특정 사용자의 프로세스를 보여준다.|

---

### ✏️ jobs 명령어

jobs 명령어는 직업의 상태를 표시하는 명령어다. 현재 쉘 세션에서 실행 시킨 백 그라운드 작업의 목록이 출력되며, 각 작업에는 번호가 붙어 있어 kill 명령어 뒤에 '%번호' 등으로 사용할 수 있다.

> job 명령어는 현재 쉘 프로세스 자식 백 그라운드 프로세스들을 보여준다고 생각하면 된다.

<img width="916" alt="스크린샷 2022-05-29 오후 6 45 03" src="https://user-images.githubusercontent.com/83526046/170862862-7deeb15b-43ee-4a26-bdde-e0eb70c0ef83.png">


* #### 상태

|상태|설명|
|:----:|:----|
|Running|작업이 계속 진행중임|
|Done|작업이 완료되어 0을 반환|
|Done(code)|작업이 종료되었으며 0이 아닌 코드를 반환|
|Stopped|작업이 일시 중단|
|Stopped(SIGTSTP)|SIGTSTP 시그널이 작업을 일시 중단|
|Stopped(SIGSTOP)|SIGSTOP 시그널이 작업을 일시 중단|
|Stopped(SIGTTIN)|SIGTTIN 시그널이 작업을 일시 중단|
|Stopped(SIGTTOU)|SIGTTOU 시그널이 작업을 일시 중단|

* #### jobs 명령어 옵션

`$ job [옵션][작업번호] `

|옵션|설명|
|:----:|:----|
|-i|프로세스 그룹 ID를 state 필드 앞에 출력|
|-n|프로세스 그룹 중에 대표 프로세스 ID를 출력|
|-p|각 프로세스 ID에 대한 한 명씩 출력|
|command|지정한 명령어를 실행|

---

### ✏️ kill 명령어

kill 명령어는 프로세스를 강제 종료하는 명령어이다.

> 리눅스에서 작업을 할 때 응용프로그램이나 프로세스가 멈추는 경우가 있는데 이때 유용하게 사용 할 수 있는 명령어 이다.

<img width="1437" alt="스크린샷 2022-05-29 오후 7 14 59" src="https://user-images.githubusercontent.com/83526046/170862986-dabda231-b1b4-462e-a9dd-9582bcffacd2.png">

* #### kill 명령어 옵션

`$ kill [옵션] <PID>..`

|옵션|설명|
|:----:|:----|
|1|프로세스를 다시 로드|
|9|프로세스를 강제 종료|
|15|프로세스를 정상적으로 중지|
|l|사용 가능한 모든 신호 목록|



## vim 에디터에서 매크로 활용방법(q, @)

우선 vim 메크로를 시작하기 전에 vim에 대해 알아보자 

### vim이란 무엇인가? 

위키백과 내용을 인용한다

> Vim은 Bram Moolenaar가 만든 vi 호환 텍스트 편집기이다. CUI용 Vim과 GUI용 gVim이 있다. 본래 아미가 컴퓨터 용 프로그램이었으나 현재는 마이크로소프트 윈도우, 리눅스, 맥 오에스 텐을 비롯한 여러 환경을 지원한다. 

쉽게 말 CLI 환경에 사용 가능한 텍스트 편집기 이다.

그럼 본격적으로 vim 메크로 기능에 대해 알아보겠다.
**사용법**

1) `q[name]` 로 메크로 기록 시작
2) `q`로 메크로 기록 종료
3) `@[name]` 로 저장된 매크로 실행
4) `[number]@[name]`로 매크로 여러번 실행

### 2) q[name] 로 메크로 기록 시작 `q`로 멬,로 기록 종료

<img width="1440" alt="스크린샷 2022-05-30 오후 2 23 15" src="https://user-images.githubusercontent.com/83526046/170925300-33e779d1-d8b1-4680-9ce8-9c94ff410ddc.png">

Normal Mode 에서 qt, qg, qq 등 `q[name]` 을 입력할 경우 위 사진과 같이 “기록중” 이라는 글을 확인 할 수 있다.

일련의 동작들을 입력한 뒤 다시 `q`를 입력하면 매크로 기록이 종료된다.


### 2) @[name] - Vim Macro 실행하기

`@[name]`으로 특정 레지스터에 저장된 매크로를 실행시킬 수도 있고, `@@`로 직전에 실행한 매크로를 재 실행할 수도 있다. 

<img width="1440" alt="스크린샷 2022-05-30 오후 2 37 07" src="https://user-images.githubusercontent.com/83526046/170925361-5233edad-1b16-42a1-ae5e-bd2d85dc6a28.png">

위 그림처럼 qt에 dd를 눌러 9번 라인을 제거후 @t를 눌러 저장한 메크로를 실행시켜 8번 라인을 없앴음을 확인 할 수 있다.

### 3) [number]@[name]로 매크로 여러번 실행

<img alt="스크린샷 2022-05-30 오후 2 38 20" src="https://user-images.githubusercontent.com/83526046/170925429-dbe94059-20e6-456e-be93-a5e15cea6cdc.png" width="500" heigh="500"> <img alt="스크린샷 2022-05-30 오후 2 38 37" src="https://user-images.githubusercontent.com/83526046/170925446-b7baeef4-b0a4-41dd-821f-fa1b1c686331.png" width="500" heigh="500">


위 두 사진은 `qt`를 통해 라인 지우기를 메크로에 저장한 메크로를 `2@t`를 활용하여 연속으로 메크로가 2번 실행하게 하였다.

보면 ***6라인과 7라인이 지워진걸 확인*** 할 수 있다.

## 📚마치며
top, jobs, ps, kill등 프로세서 관리에 필요한 명령어들을 알아보는 시간을 가졌다. 

리눅스에서 사용 가능한 명령어들이지만 멕북을 사용하고 있느 나한테도 매우 유용한 명령어들이기에 이번 과제를 통해 공부해보고 나중에 더 추가적으로 공부할 수 있는 시간을 가져야겠다.

또한 vim 에디터의 메크로 경우 이 기능을 활용하여 복잡하거나 혹은 유용한 기능을 하는 키의 조합들을 저장하여 필요에 따라 바로 꺼내 사용 할 수 있다. 

주로 vim을 사용하기 때문에 이 기능을 이번 기회에 확실히 배워두고 자주 사용해야겠다.


——————

## 💡참고

 [Top](https://ironmask84.tistory.com/355 "top 명령어 참고 사이트")

 [Ps](https://jhnyang.tistory.com/268 "ps 명령어 참고 사이트")

 [Jobs](https://hbase.tistory.com/265 "ps 명령어 참고 사이트")

 [Kill](https://m.blog.naver.com/koromoon/220804715310 "kill 명령어 참고 사이트")

 [vim](https://ko.wikipedia.org/wiki/Vim "에디터 참고 사이트")
