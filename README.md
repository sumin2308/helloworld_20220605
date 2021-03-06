# Top, Ps, Jobs, Kill 명령어
***
1) Top
* Top 명령어
- 현재 시스템의 프로세스 상태를 연속적으로 화면에 보여준다.
- 윈도우의 작업관리자와 비슷하다.
- 리눅스를 사용하는 디바이스의 성능이나 리눅스 서버의 성능을 체크할 때 유용하다.


<img src="https://user-images.githubusercontent.com/106833437/172017978-d6676239-3cfb-477e-b13e-80b7ae2aac4e.png" width="320" height="240">


* Top 항목

|항목|설명|
|--------|--------|
|PID|Process ID|
|PPID|Parent Process ID|
|UID|소유자의 User ID|
|USER|소유자|
|PRI|Priority|
|NI|Nice Value|
|SIZE|프로세스의 코드와 데이터의 크기|
|TSIZE|프로세스의 코드 사이즈|
|SWAP|프로세스가 swap한 메모리양|
|RSS|프로세스가 사용하는 실제 메모리양|
|SHARE|프로세스가 사용하는 공유 메모리의 양|
|STAT|현재 프로세스의 상태를 나타낸다.|
|LIB|라이브러리 페이지의 크기|
|%CPU|CPU 사용 시간 퍼센트|
|TIME|프로세스가 시작하여 사용한 총 CPU 시간|
|COMMAND|프로세스를 실행한 명령어 라인|

* Top 실행 중의 명령어 옵션


|명령어|옵션|
|-----|-----|
|SPACE|화면을 갱신한다.|
|h.?|도움말을 출력한다.|
|k|kill 명령을 내린다. PID 값을 입력하면 종료신호를 보낸다.|
|i|Zombi,idle 프로세스의 출력을 on/off 한다.|
|n 또는 #|출력한 프로세스의 수를 지정한다.|
|q|top을 종료|
|r|Nice 값을 변경|
|s|화면을 갱신하는 시간을 변경|
|F,f|보여줄 항목을 추가하거나 삭제|
|O,o|보여줄 항목의 순서를 바꿈|
|I|Top의 맨 윗줄을 on/off한다.|
|m|메모리의 관련된 항목을 on/off한다.|
|t|프로세스와 CPU항목을 on/off한다.|
|c|Command line의 옵션을 on/off한다.|
|M|프로세스의 RSS값을 정렬한다.|
|P|%CPU 값으로 정렬(기본값)|
|T|Time값으로 정렬|
|W|바꾼 설정을 저장|

***
2) Ps
* Ps 명령어
- 현재 실행중인 프로세스를 보여주는 리눅스 명령어이다.
- 현재 프로세스들의 상태를 PID와 함께 보여주며 리눅스에서는 사용자와 파일 뿐만아니라 프로세스도 번호로 관리한다.

<img src="https://user-images.githubusercontent.com/106833437/172018462-3006d44f-b885-48b2-a3a1-df50873e0bfd.png" width="800" height="240">


|Ps 상태|-----|
|-------|------|
|USER|BSD 계열에서 나타나는 항목으로 프로세스 소유자의 USERNAME|
|UID|SYSTEM V계열에서 나타나는 항목으로 프로세스 소유자의 USERNAME|
|PID|프로세스의 식별번호|
|%CPU|CPU사용비율의 추정치(BSD)|
|%MEM|메모리 사용비율의 추정치(BSD)|
|VSZ|K단위 또는 페이지 단위의 가상메모리 사용량|
|RSS|실제 메모리 사용량|
|TTY|프로세스와 연결된 터미널|
|STAT|현재 프로세스의 상태|

|Ps 값|----|
|------|------|
|R|실행 중 혹은 실행될 수 있는 상태|
|S|인터럽트가 가능한 대기상태|
|I|idle(비활동상태:BSD, 중간적 상태:sysV(보통 20초 이하의 대기 상태|
|T|정지된 상태|
|Z|좀비 프로세스|
|D|디스크 관련 대기상태(BSD)|
|P|페이지 관련 대기상태(BSD)|
|X|메모리 확보를 위한 대기 상태(sysV)|
|K|사용가능한 커널 프로세스(AIX)|
|W|스왑 OUT된 상태|
|N|낮은 우선순위 상태|
|<|높은 우선순위 상태|
|START|프로세스 시작 시간 또는 날짜|
|TIME|총 CPU사용시간|
|COMMAND|프로세스의 실행 명령행|
|STIME(sysV)|프로세스가 시작된 시간 혹은 날짜|
|C(sysV),CP(BSD)|짧은 기간 동안의 CPU사용률|
|F|프로세스의 플래그들|
|PPID|부모 프로세스의 PID|
|PRI|실제 실행 우선 순위|
|NI|nice 우선순위 번호|
|WCHAN|프로세스를 기다리고 있는 이벤트|
|PLAGS|프로세스와 관련된 숫자 값|

***
3) Jobs
* Jobs 명령어
- 백그라운드로 실행중인 프로세스나 현재 중지된 프로세스의 목록을 모두 출력해주는 명령어이다.
- +는 스택의 가장 위에 있다는 뜻이고 -는 바로 그 다음 밑에 있다는 뜻이다.

- 예시
<img src="https://user-images.githubusercontent.com/106833437/172018681-e9ab2044-1b5b-4464-a75c-6079c624ddb1.png" width="500" height="100">


***
4) Kill
* Kill 명령어
- 프로세스에 특정한 signal을 보내는 명령으로 보통 실행중인 프로세스에 종료 신호를 보낸다. 또한 보통 중지시킬 수 없는 프로세스를 종료시킬 때 많이 사용한다.

<img src="https://user-images.githubusercontent.com/106833437/172018974-4e9531cc-a212-411d-9bc2-31b4e9452f3a.png" width="500" height="100">


|번호|시그널|의미|
|-----|-----|-----|
|1|SIGHUP|터미널에서 접속이 끊겼을 때 보내지는 시그널, 변화된 내용을 적용하기 위해 재시작 할 때 사용된다.|
|2|SIGINT|인터럽트 시그널로 실행을 중지시킴, CTRL+c 입력시 보내지는 시그널|
|3|SIGQUIT|실행 중지 시그널로서 Ctrl+\ 입력시 보내지는 시그널|
|9|SIGKILL|프로세스를 강제로 종료 시키는 시그널|
|15|SIGTERM|kill의 기본 시그널로 정상 종료 시키는 시그널|
|18|SIGCONT|시그널에 의해 정지된 프로세스를 다시 실행시키는 시그널|
|19|SIGSTOP|정지 시그널|
|20|SIGTSTP|일시정지 시키는 시그널로서 Ctrl+z 입력시 보내지는 시그널|

***

# vim 에디터에서 매크로 활용방법

- q누른 후 a~z를 눌러 매크로 저장할 알파벳 선정 후 매크로로 등록할 행동을 하고 마지막에 q를 눌러 등록을 마치고 @a 등으로 매크로 실행한다. 그 이후에는 @@으로 직전에 실행한 매크로 다시 실행 가능하다.
- "Ap:현재 커서 위치에 기록된 매크로 내용 표시.
- "Ayy:출력된 매크로 내용에서 작업 수정/추가 등을 한 후 편집한 내용 다시 등록.

* 같은 명령 반복하는 매크로 기능

|번호|매크로 순서|----|
|------|--------|-------|
|1|q+a|a키에 recording 시작|
|2|반복을 위한 내가 원하는 동작|
|3|q|recoding 종료|
|4|@a|1회 실행|
|or|@@|방금 실행한 매크로 실행|
|or|10@a|매크로 10회 실행|
