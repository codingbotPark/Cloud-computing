1학년 2학기 전공역량강화 <클라우드컴퓨팅>
> 유미선생님 fakytaky@empas.com

---

# 클라우드 컴퓨팅
**사용자의 직접적인 활발한 관리 없이** 데이터 스토리지(클라우드 스토리지)와 컴퓨팅 파워와 같은 컴퓨터 **시스템 리소스를 필요시 바로 제공하는 것**

정의로는 개인이 가진 단말기를 통해 주로 입/출력 작업만 이루어 지고,  
정보분석 및 처리, 저장, 관리, 유통 등의 작업은 클라우드라고 불리는 제 3의 공간에서 이루어지는 컴퓨팅 시스템 형태이다

[위키백과<클라우드 컴퓨팅>](https://ko.wikipedia.org/wiki/%ED%81%B4%EB%9D%BC%EC%9A%B0%EB%93%9C_%EC%BB%B4%ED%93%A8%ED%8C%85)

<br>
<br>

**클라우드가 가능하도록 하는 것의 가장 기본적인 개념이 가상화이다**

예전에는 서버들을 물리적으로 관리하는 것이 트랜드였는데  
요즘에는 하드웨어의 발전 때문에 서버라는 것은 "구름너머 어디에 있겠지"라는 생각을 가지고 서버를 만든다고 생각하면 된다

<br>

### 가상화가 시작된 이유
서버 가상화가 없었을 때는 서버에 os와 운영프로그램을 올려서 실행했다
(cpu의 종류에따라 운영체제가 달라진다)
이 때 자원의 효율이 떨어진다
=> 비싼 장비를 구매했지만 제대로 못사용한다
=> 부화가 생기고 안생길 때가 생긴다(예) 사내메일 = 주간 | 백업 = 야간)
이런 상황에서 자원의 효율 문제를 해결하려고 가상화의 개념이 등장했다

vmware라는 회사
ctrix라는 회사의 ven-server (아마존에서도 사용)

Hyperv (마이크로소프트에서 사용)

cpu
memory
storage

가상화의 문제
효율성 (자원의 오버헤드)
성능 (os가 2개가 겹쳐있어서 데이터 변경이 많이 일어나야한다)
그럼에도 요즘은 하드웨어의 발전에 따라 극복해지는 추세

**가상머신은 모든 데이터들이 파일 형태로 저장되어 있다**

---

개발자가 배포, 운영자가 코드를 이해를 잘해서 운영도 잘해야 한다(Devops)

DevOps(데브옵스)는 Development(개발)과 Operations(운영)의 합성어로 소프트웨어 개발자와 정보기술 전문가의 소통, 협업 을 강조하는 개발 환경, 문화를 말한다  
소프트웨어 제품과 서비스를 빠른 시간에 개발, 배포하는 것을 목적으로 한다

[위키백과<데브옵스>](https://ko.wikipedia.org/wiki/%EB%8D%B0%EB%B8%8C%EC%98%B5%EC%8A%A4)

---

docker라는 기술이 container를 솔루션 하는 프로그램이다
현제 시장에서 가장 많이 사용되고 있다
<->
가상화 + 배포까지 해야 하기 때문에 개발자가 힘들다

kubermetes = 컨테이너라는 형태로 배포를 했을 때 해석하는 역할
서버라는 건 컴퓨터 -> 장애라는 것이 생길 수 있다
즉 서버가 죽으면 사이트가 마비된다

[위키백과<쿠버네티스>](https://ko.wikipedia.org/wiki/%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4)

이러한 문제를 모니터링을 통해  
서버가 죽었을 때 서버를 재시작 하는 일을 자동화 해준다(kubernetes가)

로드 밸런스 = 부화를 분산하는 작업
스케일 아웃 = 100명을 50명 씩 나누었을 때 1000명이 들어와서 500명이 들어온다면 하나의 서버를 더 추가해야할 것이다

오토 스케일링 = 스케일링 하는 작업을 자동화

금융권, 군대 등의 보안이 중요한 곳을 제외한,
기업들이 서버를 구매, 우리회사 안에서 사용 하는데
서버를 빌려 쓴다는 것 = aws
몇 개월 어치만 결제할게요

[위키백과<아마존 웹 서비스>](https://ko.wikipedia.org/wiki/%EC%95%84%EB%A7%88%EC%A1%B4_%EC%9B%B9_%EC%84%9C%EB%B9%84%EC%8A%A4)

앞으로 리눅스의 사용이 많아질 것이다
리눅스의 장점 = 가볍다, 무료이다, 오픈소스이다
오픈소스라는 것은 빠르게 보안이 가능하기 때문에 보안이 오히려 더 좋을 수 있다

---

컨테이너(Container)
서버가 하나, 운영체계도 하나, 여러 개의 응용 프로그램이 있을 때 문제가 생길 수 있다

DevOps의 입장에서 문제  
자원 (다른 응용 프로그램끼리의 자원 분배가 효율적이지 않을 수 있다)
이는 보안 에도 문제가 생길 수 있다(다른 응용 프로그램의 내용에 접근 등등)

이는 격리, 이런 기능들을 Linux가 제공하고 Docker를 사용해 구현할 수 있다  
즉 Docker는 Linux가 있어야 사용할 수 있다

장점은
성능손실이 없다

---

모노리틱 아키텍쳐는
개발이 쉽다 <=> 기능 결합도가 올라감, 개별 업데이트가 어려워짐

이러한 모노리틱 아키텍쳐의 특징으로
수정할 부분을 모아서 한 번에 고쳐야 했었다

이런 문제점때문에
MSA(Micro-Service-Architecture)
가 등장했다

이 MSA는 각각의 기능들을 변경할 수 있게되었다
즉 많은 배포가 이루어 진다(비즈니스 변경사항이 많다)

### docker와 kubermetes 를 앞으로 배움

<br>
<br>

# 리눅스 파일 시스템 구조 및 파일 관리

<br>

### 명령어 라인 구성

**command [-options] [argument]**

- command(명령) = 사용자가 입력하는 명령
- option(옵션) = 명령의 세부기능을 설명
- argument(인자) = 명령으로 전달되는 값

```
command -abc
```

위처럼 여러 기능들을 함께 사용 가능하다

<br>

### id - 사용자 정보 확인

**사용자의 UID와 GID를 확인**
현재 시스템으로 로그인한 사용자 또는 인자로 지정한 사용자의 정보를 보여준다

```
id
id -g
id -G
```

위처럼 옵션에는 -g(기본 그룹의 GID만) 와 -G(기본 그룹과 추가 그룹의 GID들) 가 있다

<br>

### who - 로그인 세션

**현재 로그인 한 모든 사용자 정보 출력**
현재 접속 된 사용자들의 이름, 접속 회선, 접속시간 등 자세한 정보 출력

```
who
who -q
who -H
```

위처럼 옵션에는 -q(계정의 이름, 수) 와 -H(출력 정보의 헤더표시) 가 있다

<br>

### passwd - 사용자 암호 변경

**사용자 패스워드 지정**
사용된 계정은 반드시 패스워드를 정의해야 한다  
passwd 명령어는 권한이 필요하다 (기본은 root)

`passwd [옵션][사용자ID]`

<br>

### 시스템 정보 수집하기

#### 현재 로그인 된 사용자 정보

```
users
who
finger
last
lastb
```

#### 운영체제 버전 과 하드웨어 정보

```
cat /etc/os-release
uname -a
free
lsscsi
```

#### 네트워크 정보

```
uname -a
ip address
```

### 사용자 전환

#### su(Switch User) - 사용자 전환

**일시적으로 다른 계정으로 전환**

```
su -worker
su -root
```

위와같이 다른 계정으로 일시적으로 전환할 수 있고,  
다른 계정으로 전환할 때는 비밀번호가 필요하다(root는 필요없다)

#### sudo(Switch User Do) - 다른 사용자의 권한으로 명령어 실행

**하나의 명령을 다른 사용자의 권한으로 실행**

```
sudo useradd hi
```

<br>

### 디렉토리 관리

#### 디렉토리란

- 윈도우에서는 폴더라 불린다
- 디렉토리 아래에 계층적으로 하위 디렉토리를 가지는 계층적 구조
- 트리 형태의 자료구조, 최상위를 /로 쓰고 root라 읽는다

**윈도우와 리눅스의 차이점**
윈도우 = 저장장치마다 개별 트리구조
유닉스 = 여러 개의 저장장치가 연결되어도 단일 트리 구조로 구성

#### 리눅스 파일시스템 계층 표준(FHS)

| 디렉토리    | 기능                                                                                                    |
| ----------- | ------------------------------------------------------------------------------------------------------- |
| /           | 루트 디렉토리, 파일시스템의 시작점(home디렉토리)                                                        |
| /boot       | 리눅스 커널, ram 디스크 이미지 등등 커널 로더 설정 파일 위치                                            |
| /dev        | 커널이 인식하는 모든 디바이스 파일이 위치                                                               |
| /etc        | 시스템 전반의 환경 설정 파일                                                                            |
| /home       | 각 사용자 계정의 홈 디렉토리 생성                                                                       |
| /opt        | 추가적인 소프트웨어의 기본적인 설치 경로                                                                |
| /tmp        | 시스템, 응용 프로그램 운영에 필요한 임시 파일들이 생성되는 경로                                         |
| /usr        | 기본적인 시스템 명령어의 실행 파일, 공용 라이브러리 등이 위치                                           |
| /var        | 상대적으로 자주 변경되는 데이터들이 위치                                                                |
| /proc, /sys | 리눅스 커널이 관리하는 가상 파일 시스템, 실시간으로 사용되는 리눅스 커널 정보 확인을 위해 자주 사용된다 |

#### pwd(print working directory) - 디렉토리 확인

**현재 자신이 위치한 디렉토리 확인**

```
pwd
```

#### 디렉토리 관리

**경로**
사용자가 원하는 디렉토리나 파일의 트리 형태 논리적인 자료구조 안에서 위치

**상대 경로와 절대 경로**
절대경로 = 파일 위치를 최상위 노드(/)를 기준으로 정의한 경로  
상대경로 = 현재 사용자의 위치를 기준으로 정의한 경로

**Spectial directory**
. = 현재 디렉토리
.. = 현재 디렉토리의 하나 상위 디렉토리

<br>

### cd(change directory) - 디렉토리 변경

**한 디렉토리에서 다른 디렉토리로 이동**

```
cd /etc
cd
```

위처럼 cd를 사용할 수 있고 이동 경로를 따로 주지 않으면 사용자 계정의 홈디렉토리로 이동된다

<br>

### ls(list) - 파일 리스트 출력

**파일이나 디렉토리의 리스트 출력**

`ls [옵션][디렉토리 이름]`

```
ls
ls -a
ls -l
ls -t
ls -h
```

위처럼 ls의 옵션에는 -a(숨김 파일까지 출력) 와 -l(자세한 정보) 와 -t(최근 수정, 생성 된 파일 순 정렬 출력) 와 -h(파일크기를 사람이 인식하기 쉬운 형태로 출력)

<br>

### 파일 관리

리눅스 파일의 특징

- 일반적으로 확장자를 가지지 않음
- 대소문자 구별
- 엄격한 소유, 허가 권한을 가짐

ls -l 을 했을 때  
` drwx-xr-x.``2``pbk``pbk``4096``2021-12-21 13:46``공개 `

![파일목록](https://thebook.io/img/006718/linux-101.jpg)
![파일목록접근권한](https://thebook.io/img/006718/linux-102.jpg)

<br>

### 디렉토리 관리

#### mkdir - 디렉토리 생성

**새로운 디렉토리 생성**

`mkdir [옵션][디렉토리 이름]`

```
mkdir class
mkdir -p class/linux/fundamentals
```

위처럼 mkdir의 옵션에는 -p(선택한 경로에 없는 디렉터리들을 모두 동시에 생성)

#### rmdir - 디렉토리 삭제

**복원 불가, 삭제하려는 디렉토리가 비어있어야 한다, 현재 위치의 디렉토리는 삭제할 수 없다**

```
rmdir pbk

rm -r
```

위처럼 rmdir을 사용할 수 있고 비어있지 않는 디렉토리를 지우기 위해 `rm -r` 을 통해 삭제할 수 있다

<br>

### 파일 관리

#### cat

**파일 내용 출력**
표준 출력 장치로 출력하는 기능  
파일 전체를 한꺼번에 출력, 긴 파일 출력시 불리

`cat [옵션] 텍스트 파일명`

```
cat f1
```

#### less

**파일 내용 출력**
긴 텍스트 파일을 출력할 때 유리

```
less f1
```

#### head / tail

head = 파일 내용 중 앞부분의 일부 문장 출력
tail = 파일 내용 중 뒷부분의 일부 문장 출력

`head [옵션] 텍스트 파일명`
`tail [옵션] 텍스트 파일명`

```
head f1
tail f1
head -c h1
tail -n h1
```

위처럼 head / tail을 사용할 수 있고, -c(출력할 용량을 지정) 와 -n(처음부터 n번째 문장까지만) 등의 옵션 있다

<br>

#### touch - 파일관리

**파일의 시간 정보 갱신**
옵션이 없다면 서버의 현재 시간으로 변경  
존재 하지 않는 파일명을 인수로 주면 사이즈가 0인 빈 파일을 생성

```
touch emptyfile
```

#### cp - 파일복사

**파일이나 디렉토리를 복사**

`cp [옵션] souce target`

```
cp backup backup-1
cp /etc/passwd /tmp/passwd/old

cp -a f1 f2
cp -r f1 f2
```
위처럼 cp를 사용할 수 있고, -a(파일의 모든 속성 복사) 와 -r(디렉토리의 하위 내용 모두 복사) 등의 옵션이 있다

#### mv - 파일관리
**파일 이동 및 이름 변경**

`mv [옵션] souce target`

```
mv passwd passwd.old

mv -b passwd passwd.old
```
위처럼 mv를 사용할 수 있고, -b(백업파일 생성 후 이동) 등의 옵션이 있다

#### rm - 파일 삭제
**한 번 삭제된 파일, 디렉토리는 복구 불가능**
`rm [옵션] 파일명/디렉토리`

```
rm backup-1

rm -i backup-1
rm -r backup-1
```
위처럼 rm을 사용할 수 있고, -i(파일 삭제전 삭제 여부 확인) 와 -r(디렉토리의 하위 모든 내용 제거) 등의 옵션이 있다

#### df - 파일 시스템 사용량 확인
**파일 시스템 단위로 사용량 정보를 확인**

```
df

df -h
```
위처럼 df를 사용할 수 있고, -h(용량을 사람이 읽기 편한 단위로 출력) 등의 옵션이 있다

#### 소유권과 허가권
**소유권 = 파일, 디렉토리의 소유권**
**허가권 = 파일, 디렉토리의 연산 허락권**

![리눅스 파일, 디렉토리의 소유권과 허가권](https://t1.daumcdn.net/cfile/tistory/1308C1174C2A003B96)

#### chown - 파일 소유자 변경
**파일 또는 디렉토리의 소유자를 변경**
시스템 관리자만 소유자 정보 변경 가능

`chown [옵션] 소유자명 파일/디렉토리`

```
chown centos backup

chown -R centos backup
```
위처럼 chown을 사용할 수 있고, -R(지정한 디렉토리, 하위에 존재하는 모든 디렉토리와 파일의 소유자를 동시변경) 등의 옵션이 있다

#### chgrp - 파일 그룹 변경
**파일 또는 디렉토리의 소유 그룹 정보를 변경**
시스템 관리자만 소유 그룹 정보 변경 가능

`chgrp [옵션] 그룹명 파일/디렉토리 이름`

```
chgrp centos testfile

chgrp -R centos testfile
```
위처럼 chgrp을 사용할 수 있고, -R(지정한 디렉토리, 하위에 존재하는 모든 디렉토리와 파일의 소유자를 동시변경) 등의 옵션이 있다

#### chmod - 파일 허가권 변경
**기호모드를 사용해서 지정한다**

`chmod [-u | -g | -o | -a][+ | - | =] [rwx] 파일명(디렉토리명)`
* -u = 파일의 소유자
* -g = 파일의 소유 그룹을 나타낸다
* -o = 기타 사용자를 나타낸다
* -a = 모든 사용자를 나타낸다

```
chmod g-w,o+x a.out
소유그룹(g)의 쓰기(w)권한을 없애고, 기타 사용자(o)의 실행(x)권한을 추가한다
```

#### grep - 문자열 검색
**특정 파일, 명령어 결과로 부터 특정 문자열이 포함된 라인을 출력**

```
grep ROOT /etc/passwd

grep -C ROOT /etc/passwd
grep -i ROOT /etc/passwd
```
위처럼 grep을 사용할 수 있고, -C(문자열을 포함한 라인의 수 출력) 와 -i(검색시 대소문자 식별X) 의 옵션이 있다

#### wc(word counter) - 파일의 크기 정보 출력
**특정 파일을 구성하는 단어 수를 출력한다는 뜻**

`wc [옵션] 파일명`

```
wc /etc/passwd

wc -c /etc/passwd 
wc -w /etc/passwd 
wc -l /etc/passwd 
```
위처럼 wc를 사용할 수 있고, -c(파일의 문자의 수) 와 -w(파일의 단어의 수) 와 -l(파일의 문장의 수) 등의 옵션이 있다

<br>

### 쉘 표준 입출력
**프로그램이 성공적으로 실행되기 위해 입력과 출력이 필요**
이러한 입출력은 특수한 파일을 통해 전달
* 표준입력 = 쉘이 키보드를 통해 입력을 받는 것
* 표준 출력 = 명령어 실행 결과를 모니터로 출력
* 표준 오류 = 명령어의 실패 결과를 모니터로 출력
**이 3가지 형태의 특수한 파일이 사전에 쉘(shell)에 의해 정의**

#### 리다이렉션
**< , > 기호를 사용해 표준 입출력의 방향을 재지정**

리다이렉션 기호 | 의미
--- | ---
< | 입력 방향을 재지정
\> | 출력 방향을 재지정
2> | 오류 방향을 재지정
&> | 표준출력 = 표준오류 동시 재지정

#### | - 파이프
**한 명령어의 수행 결과가 다른 명령어의 입력으로 사용되게 한다**

```
ps -e | wc -l
현재 실행중인 모든 프로세스(ps -e)의 줄의 개수,
즉 실행중인 프로세스의 개수를 출력한다
```

<br>

### 프로세스 관리

#### ps - 수행중인 프로세스 상태 출력
**현재 시스템에서 수행 중인 프로세스에 대한 정보 출력**
프로세스의 실행 상태, cpu사용 정보, 메로리 사용정보 등

```
ps

ps -e
```
위처럼 ps를 사용할 수 있고, -e(every:현재 터미널에서 수행 중인 프로세스의 PIN, 회선정보 등을 출력) 등의 옵션이 있다 

#### pstree - 수행 중인 프로세스의 계층 구조 출력
**시스템에 존재하는 부모 프로세스와 자식 프로세스 간의 계층 구조 출력**

```
pstree
```

#### top - 프로세스의 실행 정보 출력
**프로세스의 실행 상태를 실시간으로 확인**
일정시간마다 갱신, 프로세스 실행 정보 출력

```
top
```

#### kill - 프로세스 종료
**실행을 마친 프로세스가 종료되지 않으면 좀비가 된다 kill명령어를 사용해 프로세스 종료**

```
kill -9 1
kill -15 1
```
-9는 강제종료, -15는 작업 종료이다

<br>


## Container 조작

alias conrm='docker container rm -f $(docker container ps -aq)'
위의 코드로 conrm 을 했을 때 실행되고 있는 컨테이너들을 모두 삭제하는 단축어를 만들 수 있다


cgroups = container에게 자원 할당
chroot = container가 파일시스템 격리
namespaces = 컨테이너를 호스트 os, 다른 컨테이너 격리

image = 컨테이너 실행에 필요한 모든 파일 압축 (정확히 말하면 file)
container = 이미지를 기반으로 실행이 가능한 인스턴스 (image가 실행할 수 있는 형태로 만드려면 container로 만들어 주어야 한다)
registry = 중앙 이미지 저장소(index.dockerio, Docker Hub)

`docker container action`

#### docker container run
보통 -it(i:대화식 t:터미널, 단말기)라는 옵션을 같이 준다

#### docker container rm
보통 -f(stop하고 remove)라는 옵션을 같이 준다




exit가 아닌 ctrl + p + q 를 하면 컨테이너를 없애지 않고(프로세스를 멈추지 않고) 나갈 수 있다






## kubernetes
kubernetes cluster 