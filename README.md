# 20223195 컴퓨터공학과 김현우 과제2

**리눅스 명령어**

**"top 명령어"** 

![image](https://user-images.githubusercontent.com/106826719/172023202-70da3ffc-e8fd-4077-9b76-d7b3776377bb.png)
```
* top명령어는 화면 위쪽의 주황색 화면과 밑쪽의 빨간색 화면을 나눠서 볼 수 있습니다.

* 주황색은 현재 시스템의 상태를 보여주는 것으로 시스템 시간이나, uptime 등을 전체적으로 확인할 수 있습니다.

* 빨간색 화면은 현재 실행하고 있는 프로세스 현황을 볼 수 있습니다.
```
|명령어 또는 명령어 내용설명|내용설명|
|:---:|---|
|top|시스템의 상태를 전반적으로 가장 빠르게 파악 가능하며 옵션 없이 입력할 시 interval 간격(기본 3초)으로 화면을 갱신하여 정보를 보여준다. (사용자 수 그리고 시스템 부하율을 표시하는 명령어인 uptime의 결과를 가장 상단에 표시해주며, 그 아래로 각 프로세스별 부하율과 상태를 표시해준다.)|
|top 실행 전 옵션|순간의 정보를 확인하려면 -b 옵션 추가(batch 모드), -n : top 실행 주기 설정(반복 횟수)|
|top 실행 후 명령어|shift + p: CPU 사용률이 높은 프로세스 순서대로 표시|
|shift + m: 메모리 사용률이 높은 프로세스 순서대로 표시|shift + t: 프로세스가 돌아가고 있는 시간 순서대로 표시|
|shift + n: PID 기준 정렬| shift + r: 정렬 기준변경 (오름차순인 경우 내림차순으로, 내림차순인 경우 오름차순으로 변경)|
|k: 프로세스 kill -k 입력 후 종료할 PID 입력 signal을 입력하라고 하면 kill signal 인 9를 입력|a: 메모리 사용량에 따라 정렬|
|b: 앞에서 말한 Batch 모드 작동|d [초] : 화면 갱신 시간을 입력받은 초단위로 처리 (기본은 3초마다 갱신)|
|i: idle 프로세스와 좀비프로세스를 표시하지 않도록 처리|u [사용자]: 입력된 사용자의 프로세스만 표시|
|h: 도움말|H: 스레드 토글|
|i: 유휴 프로세스 토글|m: VIRT/USED 토글|
|M: 메모리 유닛 탐지|s: 보안 모드 작동|
|S: 누적 시간 모드 토글|숫자 1: CPU Core별로 사용량을 보여줍니다.|
|Top 명령어 페이지 이동 Page up: 프로세스의 이전페이지 목록|Page Down: 프로세스의 다음페이지 목록|

**"ps 명령어"**

![image](https://user-images.githubusercontent.com/106826719/172026249-27b4d70e-57a0-46c3-88f0-a66ee35bd528.png)
```
* ps명령어는 현재 실행중인 프로세스 목록과 상태를 보여줍니다. 

* ps의 옵션은 전통적인 유닉스인 System V, BSD, GNU에 따라 결과가 다르게 나타나고 표기법에도 차이를 보입니다.

* 옵션 사용시 System V 계열은 대시(dash,-)를 사용하고 BSD 계열은 대시(-)를 사용하지 않습니다.

* GNU에서의 옵션 표기는 두개의 대시(--)를 사용합니다. 따라서 원하는 프로세스의 상태를 출력하려면 정확한 옵션 사용이 중요합니다.

* 한 예로, 옵션 중 'a','-a'가 있는데 이 둘은 다릅니다.
```
|명령어 내용설명|출력 화면|
|:---:|---|
|ps: pid,cmd 등 기본적인 내용만 출력된다, 옵션 없이는 잘 사용하지 않는다.|![image](https://user-images.githubusercontent.com/106826719/172027193-9fdc6b67-9077-4305-8ebe-9a5c800fa98c.png)|
|-e: 모든 프로세스를 출력해 준다.(숨겨진 프로세스까지 모두 보여준다.)|![image](https://user-images.githubusercontent.com/106826719/172030599-810377bc-96a6-4c14-8556-04f220b8d4a6.png)|
|-f: 풀 포맷으로 보여준다.(uid(user ID), pid(process ID), ppid(parent ID), TTY(프로세스와 연결된 터미널) 등을 표시해준다.)|![image](https://user-images.githubusercontent.com/106826719/172027243-ad8f52b0-41a9-4a0c-8b0c-26810981e8bd.png)|
|-l: 긴 포맷으로 보여준다(풀 포맷정보 외에 F(프로세스 플래그), S(프로세스 상태), PRI(우선순위) 등 더 많은 정보를 보여준다.)|![image](https://user-images.githubusercontent.com/106826719/172027285-03ca49ca-885d-406a-8a9b-0e18251bba10.png)|
|p,-p: 특정 PID의 프로세스를 보여준다.|![image](https://user-images.githubusercontent.com/106826719/172030626-fb1f59e0-9f72-4833-9160-d181ba8e574f.png)|
|-u: 특정 사용자의 프로세스를 보여준다.|![image](https://user-images.githubusercontent.com/106826719/172030632-c90cb6d0-c763-475a-b25e-7b174574b24d.png)|

**"jobs 명령어"**

![image](https://user-images.githubusercontent.com/106826719/172031225-4957fb88-d46b-45ab-9d67-b35c9f4bb0e1.png)


```
* 리눅스 명령어 jobs는 작업이 중지된 상태

* 백그라운드로 진행 중인 작업 상태

* 변경 되었지만 보고되지 않은 상태 등을 표시하는 명령어다.
```
|명령어 내용설명|출력 화면|
|:---:|---|
|jobs: 해당 명령어를 사용하면 실행중인 현 재환경의 작업 상태를 보여주는 백그라운드 목록이 나타납니다.|![image](https://user-images.githubusercontent.com/106826719/172031257-3352259e-e205-40a7-a7d4-7d6951c000d1.png)|
|-l: 프로세스 그룹 ID를 state 필드 앞에 출력|![image](https://user-images.githubusercontent.com/106826719/172031290-38c815bd-228f-409a-9062-a9798025aa61.png)|
|-p: 각 프로세스 ID에 대해 한 행씩 출력|![image](https://user-images.githubusercontent.com/106826719/172031311-5d38f087-4b82-49cf-a3b4-a5655eb58f4b.png)|

|상태|설명|
|:---:|---|
|Running|작업이 일시 중단되지 않았고 종료하지 않고 계속 진행 중임을 뜻한다.|
|Done|작업이 완료되어 0을 반환하고 종료했음을 뜻한다.|
|Done (code)|작업이 정상적으로 완료했으며, 0이 아닌 코드를 반환했음을 뜻한다.|
|Stopped|작업이 일시 중단됨을 뜻한다.|
|Stopped (SIGTSTP)|SIGTSTP 신호가 작업을 일시 중단했음을 뜻한다.|
|Stopped (SIGSTOP)|SIGSTOP 신호가 일시 중단했음을 뜻한다.|
|Stopped (SIGTTIN)|SIGTTIN 신호가 작업을 일시 중단했음을 뜻한다.|
|Stopped (SIGTTOU)|SIGTTOU 신호가 작업을 일시 중단했음을 뜻한다.|

* 다음과 같이 jobs -p %v 다음과 같이 %를 붙이고 첫단어를 골라 붙여주면 v로 시작하는 모든 프로세스 ID를 확인할 수 있다.

**"kill 명령어"**

![image](https://user-images.githubusercontent.com/106826719/172031780-80d1ffbd-4642-4ac4-bd1f-2e3110d31dcf.png)
```
* kill 명령어는 대게 프로세스를 죽일때 사용합니다.

* 그러나 kill은 원래 내부적으로는 프로세스에 시그널을 보내 원하는 작업을 하게 하는 명령어입니다.
```
|명령어 내용설명|출력 화면|
|:---:|---|
|-l: kill 명령어에서 지원하는 시그널(Signal) 목록을 출력|![image](https://user-images.githubusercontent.com/106826719/172031968-77c5b142-d6e0-4309-acdc-a3a2e619de5c.png)|
* 사용 구문: kill -[옵션 or 시그널 (번호 또는 이름)] [PID]
* & kill -9 1234
* & kill -SIGKILL 1234

|Signal의 종료|내용|
|:---:|---|
|1) SIGHUP|연결 끊기. 프로세스의 설정파일을 다시 읽음|
|2) SIGINT|인터럽트|
|3) SIGQUTT|종료|
|4) SIGILL|잘못된 명령|
|5) SIGTRAP|트렙 추적|
|7) SIGBUS|버스 에러|
|8) SIGFPE|고정 소수점 예외|
|9) SIGKILL|죽이기|
|11) SIGSEGV|세그멘테이션 위반|
|13) SIGPIPE|읽을 것이 없는 파이프에 대한 시그널|
|14) SIGALPM|경고 클럭|
|15) SIGTERM|소프트웨어 종료 시그널|
|16) SIGSTKFLT|프로세서 스택 실패|
|17) SIGCHLD|자식 프로세서의 상태변화|
|18) SIGCONT|STOP 시그널 이후 계속 진행할 때 사용|
|19) SIGSTOP|정지|
|20) SIGTSTP|키보드에 의해 발생하는 시그널|

* Signal의 종료는 총 64가지가 존재한다.

