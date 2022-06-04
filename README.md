# 20223195 컴퓨터공학과 김현우 과제2

**리눅스 명령어**

**"명령어 설명"** 

![image](https://user-images.githubusercontent.com/106826719/172023202-70da3ffc-e8fd-4077-9b76-d7b3776377bb.png)
```
**Top 화면은 위쪽의 주황색 화면과 밑쪽의 빨간색 화면을 나눠서 볼 수 있습니다.**

**주황색은 현재 시스템의 상태를 보여주는 것으로 시스템 시간이나, uptime 등을 전체적으로 확인할 수 있습니다.**

빨간색 화면은 현재 실행하고 있는 프로세스 현황을 볼 수 있습니다.
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


