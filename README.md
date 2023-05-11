# 23-Project1-R
# 602377106 김준태

GIT 설치, CMD창에서 git -v 또는 git --version으로 설치 확인
VS Code 설치, 실행 후

### 사용자 정보 등록 (공유 PC는 --global 옵션 제거 권장)
* git config --global user.name “zzonvk"
* git config --global user.email "zzonvk@naver.com"

### 설정 내용 확인
* git config --global user.name
* git config --global user.email

### VsCode GiHub 연동

1. 폴더를 연후, 소스 제어의 Initialize Repository를 클릭

2. 터미널에 git 초기화된 폴더 에 파일을 생성하거나
변경 사항이 발생 하면 소스 제어에 바뀐 파일만큼의 숫자가 표시.

3. test 파일 만들기
* 실무프로젝트 첫 번째 모듈 생성.

4. 메시지라고 하는 곳에 커밋 제목과 설명을 작성. 메세지의 경우 제목을 적고 50글자 이내로 작성.
엔터키를 두번 누른 후 설명을 작성한다.

5. 변경된 내용 중 일부 파일만 푸시하는 경우 케밥 메뉴를 클릭하고 '푸시'를 선택하면 GitHub에 아직 Repository가 시작되기 전에 Add Remote(원격지점 추가) 버튼을 클릭한 후 원하는 레포지토리를 선택.

6. 변경된 내용을 모두 푸시하는 경우 더 이상의 수정될 파일이 없을시 커밋 버튼이 '게시 branch'으로 보임.
현재 작업 폴더와 같은 이름으로 원격에 생성

- public을 선택 시 다른 사용자가 해당 내용을 볼 수 있게 됨 private의 경우 비공개이므로 다른 사용자가 볼수 없음

7. 기본 브라우저로 GitHub에 플러그인 후
status bar의 구름 아이콘(게시 branch)을 클릭하거나 푸시 시 팝업창에서 VS Code와 GitHub를 연동.

---------------------------------------------------------------------------------------------
## R언어
* R은 통계를 포함한 데이터 분석 작업에 특화된 언어.

#### 소스창 
* RR 명령문을작성하고 실행하는 영역으로, 메모장과 유사함.
* 소스창 상단에 있는 실행 버튼(''') 을 눌러야 명령문이 실행됨
* temp <- iris[,5] "<-"은 "="과 같다.
#### 콘솔창 
* 소스창에서 작성한 R 명령문을 실행시켰을 떄 명령문의 실행 과정 및 결과가 표시되는 영역으로, 명령문을 입력한 후 키보드에서 <Enter>를 누르면 바로 실행.
#### 터미널창 
* 윈도우의 "명령 프롬프트"와 동일한 역할.
#### 환경창 
* R 명령문이 실행되는 동안 만들어지는 각종 변수나 자료구조의 내용을 보여주는 영역
#### 히스토리창 
* R 스튜디오에서 실행한 명령문, 결과 ,패키지 설치, 오류등 거의 모든 작업과정에 대한 이력이 표시
#### 커넥션창
* R과 데이터 관리를 위한 서버를 연결하는 창.
#### 파일창 
* 윈도우의 파일 탐색기와 동일한 역할을 수행.
#### 작업폴더
* R문서를 읽거나 쓸 때 기준이 되는 폴더.
* 'set as working directory' 버튼을 누르면 해당 폴더가 작업 폴더로 지정.
#### 플롯창 
* R 명령문으로 작성한 그래프가 표시되는 영역
#### 패키지창 
* R에서는 수많은 함수를 제공하나 이러한 함수들은 작성 목적이나 개발자에 따라 패키지 형태로 묶여 제공.

패키지의 개념
R 에선 데이터 분석을 위해 다양한 함수를 재공하는데 패키지는 이러한 함수를 기능별로 묶어놓은 일종의 꾸러미이다.
패키지 사용 방법

1. 패키지 설치 -> install.packages('ggploat2')
install.packages('cowsay)
# ggplot2,cowsay 패키지 설치

2. 패키지 로드 -> library(ggplot2)
library(cowsay)
ggplot2, cowsay 불러오기

3. 함수 사용하기
ggplot(data = iris, aes(x = Petal.Length, y= Petal.Width)) +geom.point()
say ('hi world), by='snowman

# 변수의 개념
프로그램 내에서 어떤 값을 저장해 놓을 수 있는 보관 상자

# 변수 만들기
a <-10
a에 10을 저장한다.

# 변수 내용 확인하기
total <- 1234
1234를 변수 total에 저장
total

#확인 1
print (total)

#확인 2
cat ('합계',total)

#확인 3
변수를 이용한 산술 연산
a <-10
a에 10을 저장
3 b <-3
b에 3을 저장
c <- a + b
c 에 a+b를 저장
print (a)
a, 10이 출력됨
print (b)
b, 3이 출력됨
print(c)
c, 13이 출력됨

# 변수에 대해 알아야 할 것들
변수의 값은 바뀔 수 있다.
a <- 12
a <- 50
print (a)
50이 출력된다.

하나에 변수애는 하나의 값만 저장 가능하다
num <- 2,5
에러 발생

변수와 변수의 연산은 변수에 저장된 값들의 연산으로 바뀌어 실행
c <- a+b
62 출력

# 변수명 작명 규칙
- 첫글짜는 영문자나, 마침표(.) 로 시작하는데 일반적으로 영문자로 시작
(마침표는 숨기고 싶은 파일 앞에 붙여준다.)
- 두 번째 글자부터는 영문자, 숫자, 마침표, 밑줄을 사용 가능
- 특수문자는 사용 불가능
- 변수명에서 소문자와 대문자를 별개의 문자로 취급
- 변수명 중간에 빈 칸을 넣을 수 X
# 변수에 저장될 수 있는 값의 종류
- 숫자형. 정수, 실수 모두 가능
- 문자형. 작은 따옴표나 큰 따옴표로 묶어 표현
- 논리형. TRUE, FALSE
- 특수값.
NULL: 정의되어 있지 않음. 자료형도 없고 길이도 0
NA: 결축값 (missing number)
NaN: 수학적으로 정의가 불가능한 값 (Not A Number) Inf, -Int: 양의 무한대 (Inf), 음의 무한대 (-Inf)

# 벡터 VECTOR

벡터의 개념
R에서는 여러 개의 값을 한 번에 저장하는 기능을 벡터 vector라고 한다. 일반적인 프로그래밍 용어로는 1차원 배열 (array)라고도 한다.
score <- c(1,2,3,4,5,6,7)
# score변수에 1,2,3,4,5,6,7 저장
mean(score)
평균값 출력
하나의 백터에는 동일한 자료형 (date type) 의 값이 저장되어야 함
w<- c(1,2,3,'a','b','c')
숫자와 문자를 섞어 벡터에 저장하게 되면 숫자가 모두 문자로 바뀌게 됨
연속적인 숫자로 이루어진 벡터
v1 <- 50:90
클론 (:)을 사용하면 연속된 정수로 이루어진 벡터를 만들 수 있다. 50:90은 50부터 90사이의 정수를 의미
v1 <-c(1,2,3,50:90)
c 함수 안에서 사용될 수 있다. 1,2,3,50부터 90까지의 수가 저장됐다.

일정한 간격의 숫자로 이루어진 벡터
seq(시작값, 종료값, 간격)
가나격은 소수도 가능하다. seq() 함수는 시작값에서 출발하여 일정 간격으로 정수값 또는 소수값을 생성하다가 종료값이 되면 생성을 종료한다.

v2 <- seq(1,101,3)
시작, 종료, 간격
v3 <- seq(0.1,1.0,0.1)
시작, 종료, 간격

반복된 숫자로만 이루어진 벡터
rep(반복 대상값, times = 반복횟수)
반복 대상값은 하나의 값일 수도 있고 여러개의 값일 수도 있다.

v4 <-rep(1, times =5)
1을 5번 반복
v5 <-rep(1:5,times=3)
1에서 5까지 3번 반복
v6<- rep(c(1:3,times=5))
1에서 3까지 5번 반복
벡터의 값에 이름 붙이기
absent <-c(1,2,3,4)
제작자는 숫자의 의미를 알지만 제 3자는 알기 어렵다. names (absent)
absent 벡터의 값들의 이름을 확인
names(absent) <-c('one','two','three','four')
값들의 이름을 확인
absent
absent 벡터의 내용 출력
names(absent)
absent 벡터의 값들의 이름을 확인.

벡터에서 원소값 확인하기

R에서는 벡터에 저장된 값들을 구별하기 위해서 앞쪽에의 값부터 순서를 부여하는데 이를 인덱스 (Index)라고 한다.

d <-c(1,2,3,4)
d --[1]은 저장된 값 중 첫번째 값을 지칭하므로, d[1] 을 출력하면 1이 출력된다.
d --벡터 전체를 출력
d[2] --2가 츨력된다.
벡터에서 여러 개의 값 한번에 추출하기

d[c(1,2)]
1,2 번째 자료 출력
d[1:3]
 1부터 3까지의 자료 출력
d[seq(1,5,2)]
홀수 번째의 자료 출력, 1부터 5까지의 값을 2씩 건너뛰어 가져온다는 의미.
d[-2]
-는 제외하고 를 의미한다. 두 번 째 값을 제외한 나머지 값을 모두 가져오라는 의미.

이름으로 값을 추출하기

일반적으로 벡터에 저장된 값 중 원하는 값을 가져오는 방법은 대응하는 인덱스를 저장하는 것으로 가능하다. 그리고 배운 바와 같이 인덱스는 순서를 지정하는 숫자이다. 그런데 인덱스를 사용하지 않고 값에 붙여진 이름으로도 원하는 값을 추출할 수 있다.

sales <-c(3,4,5,6)
names (sales) <-c('a','b','c','d')>
sales[1]
a
3
sales ['b']
b
3 

# 벡터에 저장된 원소값 변경하기
v1 <-c(1,2,3,4,5)
v1[2] <-3

v1의 두 번째 값을 3으로 변경
v1[c(1,5)] <-c (10,20)
1번째와 5번째 값을 10과 20으로 변경
library(ggplot2) library(cowsay) say("Hello wolrd", by="cat") say("Hello wolrd", by="snow") Sys.time() total <- 3030 total print(total) cat("total: ", total) print("total: ") a <- 2 b <- 30 a+b print(a+b) a <-50 c <- a+b print(c)

<h3>파일 입출력에서 알아야할 내용을 확인하자 219p</h3> <br>
계산 결과를 화면에 출력하는 대신, 특정 파일로 출력하도록 하면 파일에 출력 결과가 저장되어있다.
<h4>
<p>
setwd('c:/Rwork') <br> #작업 폴더 지정 <br>
getwd()<br>#파일 위치 확인 <br>
print('hello') <br>#화면으로 출력 <br>
a <- 10; b<-20 <br>
sink('result.txt',append=T)<br> #파일로 출력 <br>
cat('hello world') <br># 화면으로 출력 <br>
----이부분이 처리 결과를 파일을 출력하는 코드 <br>
sink('result.txt',append=T) <br> # 파일로 출력 시작 <br>
cat('a*b',a*b,'\n')
sink() <br>#파일로 출력 정지 <br>
-----여기까지<br>
sink('result.txt',append=F)<br> #메모장 지워짐 <br>
sink('result.txt',append=T) <br> #메모장 안지워짐 <br>
sink()  #이거 없이도 들어간다
</p>
<p>
- 탭이나 고백으로 분리된 파일 <br>
R 에서 분석할 데이터는 대부분 .csv 나 엑셀 파일이지만 열이 공백이나 탭으로 분리된 파일도 종종 접하게 된다. 이러한 경우 read.table() 함수를 통해 데이터를 읽을 수 있다. <br>
setwd('c:/Rwork') <br> # 작업 폴더 지정 <br>
air <- read.table('airquality.txt',header = T,sep='') <br># 파일 읽기 <br>
head(air) <br> #내용 확인<br>
View(air)<br>
tail(air)<br>
</p>
</h4>

<p>
<h3>제어문과 사용자 정의 함수 사용하기  </h3>
<h4> 
if-else문 <br>
조건문을 조건에 따라 실행할 명령문을 다르게 할 경우에 사용된다. <br>
<br>
if(job.type =='b'){ <br>
  bonus<-200 #직군이 b가 아닐때 실행 <br>
}else{ <br>
  bonus<-100 #직군이 b가 아닌 나머지 경우 실행<br>
}<br>
print(bonus)<br>
직군이 B이면 보너스를 200으로 하고, 나머지의 경우엔 100 지급. <br>
<br> ifelse 문 <br>
<br>ifelse (비교조건, 조건이 참일 떄 선택할 값, 조건이 거짓일 때 선택할 값) <br>
a <-10<br>
b<-20 <br>
c <- ifelse (a>b,a,b) <br> # a>b 조건을 만족하면 a에 c를 저장하고 만족하지 않으면 b를 c를 저장하라는 의미.  <br>
print(c)<br> 
</h4>
</p>

</h4>
<p>
<br> # 반복문 <br>

<br> for (반복 변수 in 반복 범위){<br> 
  반복할 명령문들 <br> 
}<br> <br> 
for (i in 1:5){<br>  #
  print('*')<br> 
}<br> # 1,2,3,4,5반복. 반복할때마다 i에 저장 <br> 
<br> 
<br> #반복 범위에 따라서 반복 변수의 값이 어떻게 변하는지를 나타낸다. 반복 변수들이 하나하나 출력된다 <br> 
for (i in 7:11){ <br> 
  print('i')<br> 
}<br> 
<br> 
<br> 구구단을 출력하기 위에선 cat함수를 사용한다. print는 하나의 함수를 출력할 때 사용되고,cat함수는 한 줄에 여러개의 값이 결합하여 출력할 때 사용된다. <br> 
for(i in 1:9){  #2단<br> 
  cat('2*', i,'=',2*i,'\n')<br>  
}<br> 
<br> 
#짝수인지 확인 <br> 
for(i in 1:20){<br> 
  if(i %%2==0){<br> # i를 2로 나눴을 때 나머지가 0인지 확인 <br> 
    cat(i,' ')<br> 
  }<br> 
}<br> 
</p>
</h4>
<h4>
<p>
# while <br>
<br> while (비교 조건){ <br>
  반복할 명령문 <br>
}<br>
<br>여기서 비교 조건은 반목을 수행할지 중지할지를 결정하는 조건문이고, 코드블럭 안에 반복할 명령문이 위치한다. <br>
<br>
sum <-0 <br>
i<-1<br>
<br>
while (i <=100){<br>
  sum <-sum +i  # sum에 1을 누적<br> 
  i<-i+1 #i 값을 1 증가 시킴. 이게 없으면 i 값에 변화가 일어나지 않고 while문이 영원히 실행됨. <br>
}<br>
print(sum)<br> # 5050 출력 
</p>

<p>
# apply <br>
반복작업의 대상이 매트릭스나 데이터프레임의 행이나 열인 경우 for ,while대신 apply 함수를 이용할 수 있다. 속도를 향상시킬 수 있다. <br>
apply() 함수는 매트릭스나 데이터프레임에 있는 행들이나 열을 하나하나 차례로 꺼내어 평균이나 합계를 구하는 작업을 수행할 때 유용하다 <br>
apply( 데이터셋, 행 /열 방향 지정, 적용 함수)<br>
<br>
apply(iris[,1:4],1,mean) <br>행 방향으로 함수 적용, 실행 결과는 150개의 행에 대한 행별 평균값 <br>
apply(iris[,1:4],2,mean)<br> 열 방향으로 함수 적용, 실행 결과는 4개의 열에 대한 평균 출력 <br>
apply(USJudgeRatings, 1,mean) <br> # 행별 평균 <br>
apply(USJudgeRatings, 2,mean)<br> # 열 별 평균 <br>
<p>
#사용자 정의 함수 <br>
사용자 스스로 함수를 만드는 것이다. <br>
함수명 <- function (매개변수목록)<br>{
  실행할 명령문 <br>
  return (함수의 실행 결과 )<br>
}<br><br>

mymax <-function(x,y){ # 만들고자하는 함수 mymax, 이 함수가 입력받는 매개변수 x,y <br>
  num.max <-x <br> 
  if(x>y){ # 큰 값을 num.max 안에 저장. <br>
} <br>
return  (num.max) <br> # 더 큰 값을 반환해준다. 
} <br> 작성된 코드는 작성 코드 자체를 한 번 실행해줘야한다. <br>
<br>
mymax(10,15) <br> #15출력 <br>
a <-mymax(21,15) <br> #a에 21 저장 <br>
a<br># 21 <br>
b <-mymax(33,22)<br> #33 저장
print(a+b)<br> #54출력 <br>
</p>

<p>
#257 매개변수의 기본값 설정 <br>
사용자 함수에서도 매개변수에 기본값을 저장할 수 있다. <br>
mydiv <-function(x,y=2){ <br>
  result <-x/y<br>
  return(result)<br>
}<br><br>

mydiv(x=10,y=3)<br>#매개변수의 이름과 매개변수 값을 쌍으로 저장 <br>
mydiv(10,3)<br><br> #매개변수 값만 저장 <br>
mydiv(10)<br><br> # x에 대한 값만 저장 <br>
</p>
<p>
#사용자 정의 함수의 저장과 재실행 <br>
setwd('c:/Rwork') <br> # 저장된 폴더 <br>
source('mydiv.R')<br># 저장된 폴더 안에 있는 함수 실행 <br>
a <- mydiv(20,4)<br> 함수사용, 함수 호출,<br>
b<- mydiv(20,4) <br> 함수 호출<br>
a+b <br>#12.5 출력 <br>
mydiv(mydiv(20,2),5)<br>2 출력 <br>
</p>

<p>
#조건에 맞는 데이터의 위치를 찾아보자 <br>

score <-c(65,47,86,35,75,85,78,45) <br>
which(score==85)<br> #성적이 85인 학생은 몇 번째에 있나 <br>
max(score) <br> # 가장 높은 점수 <br>
which(50<=score)<br> #50보다 크거나 같은 점수는 몇번째에 있나 <br>
which.min(score)<br> # 최저점은 몇번째에 있나 <br>
idx <-which(score <=60) <br>60 점 이하인 값들의 인덱스 <br>
score[idx] <-61<br> #60점 이하인 점수들은 61점으로 상향 조절 <br>
score<br> # 상향 조절된 점수 확인 <br>
<br>
idx <- which(score >=80) <br>#80점 이상인 값들의 인덱스 <br>
score.high <-score[idx] <br>80점 이상인 값들만 추출해서 저장 <br>
score.high<br> # 확인 <br>
<br>
#for에서 i값을 증가시킬 때, 무엇이다른지, 
#삼항연산자 ifelse문. 
#사용자지정함수 funciton 매개변수.
#source (mydiv.R)
</h4>
<h3>#복수의 선그래프 작성하기 </h3>
month =1:12 <br>
late1 =c(3,4,5,1,5,3,7,2,89,2,32,12) <br>
late2 =c(3,4,3,1,5,3,7,2,8,2,12,12) <br>
plot (month, # x데이터<br>
      late1, #y데이터 <br>
      main = 'late student', <br>
      type='b', #그래프 종류 선택<br>
      lty=1, #선의 종류 선택 <br>
      col='red', # 선의 색상 선택 <br>
      xlab='MOnth',#x축 레이블 <br>
      ylab='late cnt') #y축 레이블 <br>
<br>
lines (month, #x 데이터, line()함수는 그래프 위에 선을 겹쳐 그리는 역할을 한다<br>
       late2, #y데이터 <br>
       type='b', #선의 종류 선택 <br>
       col='blue') #선의 색상 선택 <br><br>
lines() 함수는 plot() 함수로 작성됨 스래프 위에 선을 겹쳐 그리는 역할을 한다. 함수를 추가할 때 마다 선이 하나씩 추가된다. <br>
<br>
<h2>상자 그림에 대해 알아보자 </h2>
<h3>사분위수를 시각화하여 그래프 형태로 나타낸 것, 하나의 그래프로 데이터의 분포
형태를 포함한 타양한 정보를 전달하기 때문에 단일변수 수치형 자료를 파악하는 데 자주 사용 된다
</h3>
<h4>
dist <-cars[,2] #자동차 제동거리 단위 (단위 :피트) <br>
boxplot(dist, main='자동차의 제동 거리') #상자그림은 데이터의 전반적인 분포를 이해하는 데엔 도움이 되지만 구체적인 값을 정확히 알긴 어렵다 <br>
#이를 알기 위해서는 boxplot.stats()함수를 사용하면 된다. 실행 결과는 list형태로 출력 된다 <br>
#<br>
boxplot.stats(dist) #$stats: 정상 범위의 데이터 내에서 사분위수에 해당하는 값들이 표시된다. <br>
boxplot.stats(dist)$out #특이값만 출력, $out: 특이값들의 목록을 저장한다. <br>
<br>
#그룹이 있는 테이터의 상자그림 <br>
boxplot(Petal.Length~Species, #데이터와 그룹 정보 <br>
        data=iris, #데이터가 저장된 자료 구조<br>
        main='품종별 꽃잎의 길이', #그래프의 제목<br>
        col=c('gray23','gray','gray11')) #상자들의 색<br>


<h3>#344 section3. 산점도란 무엇인가 <br> </h3>
산점도 (scatter plot) 는 다중변수 데이터에서 두 변쉥 포함된 값들을 2차원 그래프상에 점으로 표현하여 분포를 관찰 할 수 있도록 하는 도구이다. <br><br>

#두 변수 사이의 산점도 <br>
#산점도를 그려보면 두 변수의 데이터 분포와 변수 사이의 관계 파악 가능<br>
#산점도는 두 변수의 데이터 분포를 보는 것이므로 두 변수의 데이터 필요<br>
wt <-mtcars$wt # 중량 데이터, x축에 해당하는 데이터 (벡터)를 뜻 한다.<br>
mpg <-mtcars$mpg #연비 데이터 ,y축에 해당하는 데이터(벡터) 를 뜻한다.<br>
plot(wt,mpg, #2개의 변수 <br>
     main='중량 연비 그래프', #제목<br>
     xlab='중량', #x축 레이블<br>
     ylab='연비 (MPG)', #y축 레이블<br>
     col='gray65', #point 의 color<br>
     pch=19) #point의 종류(모양)<br>

산점도는 두 변수의 데이터 분포를 살펴보는 것이기 때문에 두 개의 변수에 대한 데이터가 필요하다. wt,mpg에 각각 중량과 연비 데이터를 저장한 후 plot() 함수를 이용하여 산점도를 작성한다. <br>

#347p 여러 변수들 간의 산점도 <br>
vars<-c('mpg','disp','drat','wt') # 대상 변수 <br>
target <- mtcars[ ,vars] # 대상 데이터 생성 <br>
head(target) <br>
plot(target,  # 대상 데이터 <br>
     min='Multi plots')<br>
 #mtcars 데이터셋에는 11개의 변수가 저장되어 있는데 이 중 4 개의 변수 데이터만 선택하여 target에 저장했습니다. <br>
<br>
#349p 그룹 정보가 있는 2개 변수의 산점도 349p<br>
iris.2 <-iris[,3:4] #데이터의 준비<br>
levels(iris$Species) #그룹 확인<br>
group <-as.numeric(iris$Species) #점의 모양과 색<br>
group<br>
color <-c('gray','gray7','red') #점의 색<br>
plot (iris.2, #plot() 함수를 이용해 산점도를 작성 <br>
      main='Iris plot',<br>
      pch=c(group), #품종별로 점의 모양을 다르게 지정하려면 pch를 숫자로 지정해야함<br>
      col=color[group])<br>
    
<br>
#기본그래프 1에 있는거 정확한 학습 필요<br>
<br>
<h2>#10장 데이터 탐색하기 </h2>
#단일 변수 데이터를 분석해보자 <br>
#데이터 준비<br>
installed.packages('carData')<br>
library(carData) <br>
room.class <-TitanicSurvival  #선실 정보<br>
room.class <br>
<br>#도수 분포 계산
tbl <-table (room.class)<br>
tbl<br>
sum(tbl) #전체  탑승객수<br>
<br>#막대 그래프 생성 <br>
barplot(tbl, main='선실병 탑승객', <br>
xlab='선실등급',<br>
ylab='탑승객수',<br>
col=c ('blue','green','yellow.))<br>
<br>#원그래프 작성 <br>
tbl/sum(tbl) <br>
par (mar=c(1,1,4,1)) <br>
pie(tbl,main ='선신별 탑승객',<br>
col=c('blue','green','yellow'))<br>
par(mar=c(5.1,4.1,4.1,2.1)) <br>
<br>
<br> #단일변수 수치형 데이터 분석<br>
#데이터 준비 <br>
grad <-state.x77[,'HS Grad'] #주별 고등학교 졸업률<br>
grad<br>
<br>#사분위수 <br>
summary(grad) <br>
var(grad) #분산<br>
sd(grad) #표준편차<br>
<br>#히스토그램 <br>
<br>
#타이타닉 중요
