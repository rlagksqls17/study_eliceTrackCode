R  for data analysis  

## 패키지

### 사용가능한 패키지 리스트

```R
as.data.frame(installed.packages()[,c(3:4)])
```
askpass              1.1        <NA>
base64enc          0.1-3        <NA>
BH              1.75.0-0        <NA>
brio               1.1.2        <NA>
callr              3.7.0        <NA>
caret             6.0-86        <NA>
CARRoT             2.5.1        <NA>
Ckmeans.1d.dp      4.3.3        <NA>
cli                2.5.0        <NA>
clipr              0.7.1        <NA>
colorspace         2.0-0        <NA>
commonmark           1.7        <NA>
cpp11              0.2.7        <NA>
crayon             1.4.1        <NA>
cyclocomp          1.1.0        <NA>
data.table        1.14.0        <NA>
desc               1.3.0        <NA>
DiagrammeR       1.0.6.1        <NA>
diffobj            0.3.4        <NA>
digest            0.6.27        <NA>
doParallel        1.0.16        <NA>
downloader           0.4        <NA>
dplyr              1.0.5        <NA>
e1071              1.7-6        <NA>
ellipsis           0.3.1        <NA>
evaluate            0.14        <NA>
fansi              0.4.2        <NA>
farver             2.1.0        <NA>
float              0.2-4        <NA>
foreach            1.5.1        <NA>
generics           0.1.0        <NA>
ggplot2            3.3.3        <NA>
glue               1.4.2        <NA>
gower              0.2.2        <NA>
gridExtra            2.3        <NA>
gtable             0.3.0        <NA>
highr                0.9        <NA>
hms                1.0.0        <NA>
htmltools        0.5.1.1        <NA>
htmlwidgets        1.5.3        <NA>
httpuv             1.6.0        <NA>
hunspell           3.0.1        <NA>
igraph             1.2.6        <NA>
influenceR         0.1.0        <NA>
ipred             0.9-11        <NA>
isoband            0.2.4        <NA>
iterators         1.0.13        <NA>
jpeg             0.1-8.1        <NA>
jsonlite           1.7.2        <NA>
knitr               1.33        <NA>
labeling           0.4.2        <NA>
later              1.2.0        <NA>
lava               1.6.9        <NA>
lazyeval           0.2.2        <NA>
lifecycle          1.0.0        <NA>
lmtest            0.9-38        <NA>
lubridate         1.7.10        <NA>
magrittr           2.0.1        <NA>
markdown             1.1        <NA>
mime                0.10        <NA>
mockery            0.4.2        <NA>
ModelMetrics     1.2.2.2        <NA>
munsell            0.5.0        <NA>
numDeriv      2016.8-1.1        <NA>
pillar             1.6.0        <NA>
pkgconfig          2.0.3        <NA>
pkgload            1.2.1        <NA>
plyr               1.8.6        <NA>
png                0.1-7        <NA>
praise             1.0.0        <NA>
pROC            1.17.0.1        <NA>
processx           3.5.1        <NA>
prodlim       2019.11.13        <NA>
promises         1.2.0.1        <NA>
proxy             0.4-25        <NA>
ps                 1.6.0        <NA>
purrr              0.3.4        <NA>
R6                 2.5.0        <NA>
randomForest      4.6-14        <NA>
rbibutils          2.1.1        <NA>
RColorBrewer       1.1-2        <NA>
Rcpp               1.0.6        <NA>
Rdpack             2.1.1        <NA>
readr              1.4.0        <NA>
recipes           0.1.16        <NA>
rematch2           2.1.2        <NA>
remotes            2.3.0        <NA>
reshape            0.8.8        <NA>
reshape2           1.4.4        <NA>
rex                1.2.0        <NA>
rlang             0.4.10        <NA>
rmarkdown            2.7        <NA>
rprojroot          2.0.2        <NA>
rstudioapi          0.13        <NA>
scales             1.1.1        <NA>
SQUAREM           2021.1        <NA>
stringi            1.5.3        <NA>
stringr            1.4.0        <NA>
sys                  3.4        <NA>
testthat           3.0.2        <NA>
tibble             3.1.1        <NA>
tidyr              1.1.3        <NA>
tidyselect         1.1.0        <NA>
timeDate        3043.102        <NA>
tinytex             0.31        <NA>
titanic            0.1.0        <NA>
utf8               1.2.1        <NA>
vcd                1.4-8        <NA>
vctrs              0.3.7        <NA>
viridis            0.6.0        <NA>
viridisLite        0.4.0        <NA>
visNetwork         2.0.9        <NA>
waldo              0.2.5        <NA>
withr              2.4.2        <NA>
xfun                0.22        <NA>
xgboost          1.4.1.1        <NA>
xmlparsedata       1.0.5        <NA>
yaml               2.2.1        <NA>
zoo                1.8-9        <NA>
base               3.6.3        base
boot              1.3-25 recommended
class             7.3-17 recommended
cluster            2.1.0 recommended
codetools         0.2-18 recommended
compiler           3.6.3        base
datasets           3.6.3        base
foreign           0.8-76 recommended
graphics           3.6.3        base
grDevices          3.6.3        base
grid               3.6.3        base
KernSmooth       2.23-18 recommended
lattice          0.20-41 recommended
MASS              7.3-53 recommended
Matrix             1.3-2 recommended
methods            3.6.3        base
mgcv              1.8-33 recommended
nlme             3.1-151 recommended
nnet              7.3-14 recommended
parallel           3.6.3        base
rpart             4.1-15 recommended
spatial           7.3-11 recommended
splines            3.6.3        base
stats              3.6.3        base
stats4             3.6.3        base
survival           3.2-7 recommended
tcltk              3.6.3        base
tools              3.6.3        base
utils              3.6.3        base

### 패키지 다루는 법  

```R
"""
패키지는 설치와 로드의 과정을 거친 후 사용 가능  
"""

# 패키지 설치
install.packages("패키지 명")

# 패키지 로드  
library(dplyr)  

# 패키지 업데이트  
update.packages("패키지 명")

# 설치된 목록 확인  
search()
```

## R 기초  

### 스크립트 다루기  

```R
"""
R 
Code 한 줄 실행 : 컨트롤 + R
Code 여러 줄 실행 : 드래그 후 컨트롤 + R  
주석 : #  
도움말 help(함수명)
명령어의 끝 명시 : ;
"""

# 현재 작업 중인 폴더의 경로 산출 
getwd()

# 현재 작업 중인 폴더에 있는 파일 목록 산출  
dir()  

# 파일 이름 확인하기  
list.files()  

# 변수 목록 보기  
ls()  

# 메모리의 모든 객체 삭제  
rm(list=ls())  
```

### 변수  생성

```R
"""
지수 : '^'
단항 플러스와 마이너스 부호 : '+', '-'
수열 생성 : '1:30'
특수 연산자 : '%any%'
	%/% = 나눗셈의 몫
	%% = 나눗셈의 나머지 
	%*% = 행렬곱 
곱하기, 나누기 : '*', '/'
더하기, 빼기 : '+'. '-'
좌우의 값이 같은지 비교 : 3==5 (return Boolean)  
좌우의 값이 다른지 비교 : 3!=5 (return Boolean)
					  3<>5 (return Boolean)
이상, 이하 비교 : 3<=5, 3>=5 (return Boolean)  
논리 부정 : '!' ex) !(3==4)
논리 AND 
	'&' : 논리 연산 데이터가 하나 이상인 경우 사용 
	'&&' : 논리 연산 데이터가 하나인 경우 사용
논리 OR  
	'|' : 논리 연산 데이터가 하나 이상인 경우 사용
	'||' : 논리 연산 데이터가 하나인 경우 사용  
왼쪽 값을 오른쪽으로 대입 3->a a=3  
오른쪽값을 왼쪽으로 대입 a<-3
"""

# 함수 내 인자 호출  
# x값은 10, y값은 1, z값은 TRUE 지정하여 abc 함수에 인수로 전달
abc(x=10, y=1, z=TRUE)

# 같은 의미
abc(10, 1, TRUE)
abc(10, y=1)
```

### 데이터 타입  

#### 스칼라  

R의 기본 데이터 타입은 벡터인데, 스칼라는 길이가 1인 벡터와 같음   

```R
# 숫자형  
a <- 1     # 정수 1 저장
b <- 2.7   # 소수 2.7 저장
mode(a)    # a 변수의 데이터 타입 확인
mode(b)    # b 변수의 데이터 타입 확인
[1] "numeric"


# 문자형  
a <- "가" # a라는 변수에 "가" 저장  
mode(a)
[1] "character"

	# 문자형 붙이기  
	hello <- "hello"
	x1 <- paste("a", hello, "b", sep="") # sep 사용하여 구분자 제거
	x1
	[1] "ahellob"

# 논리형  
a = TRUE  
mode(a)
[1] "logical"

# 팩터형
"""
범주형 자료를 표현하기 위한 데이터 타입
factor(data, levles, labels, ordered)

options:
	data = 범주형으로 표현하고자 하는 데이터
	levels = 구분하고자 하는 범주 목록을 지정
	labels = 범주별 표시값 지정
	ordered 
		TRUE = (상, 중, 하)와 같이 순서를 정할 수 있는 값  
		FALSE = (왼쪽, 오른쪽)과 같이 값에 대한 크기 비교를 할 수 없는 값  
"""  
factor(c("m", "m", "f", "f", "f"), levels=c("f", "m"),
      labels=c("여", "남"), ordered=F)  
[1] 남 남 여 여 여  
levels: 여 남  

# 결측치  
NA : 데이터 값이 없음을 의미 (상수)  
NULL : 정의되지 않은 값을 나타냄 (객체)
NAN : 수학적으로 계산이 불가능한 값  
INF : 무한대를 의미

# 데이터타입확인, 데이터 타입 확인, 데이터 타입
mode(객체명) # 객체의 데이터 타입 확인
is.numeric(객체명) # 객체가 숫자형 벡터인지 판단  
is.integer(객체명) # 객체가 정수형 벡터인지 판단  
is.double(객체명) # 객체가 실수형 벡터인지 판단  
is.character(객체명) # 객체가 문자형 벡터인지 판단  
is.factor(객체명) # 객체가 팩터인지 판단  
is.logical(객체명) # 객체가 논리형인지 판단  
is.null(객체명) # 객체가 NULL인지 판단  
is.na(객체명) # 객체가 NA인지 판단  

# 데이터타입 변환, 데이터 타입 변환, 데이터 타입  
as.numeric(객체명) # 객체를 숫자형으로 변환  
as.integer(객체명) # 객체를 숫자형(정수)로 변환  
as.double(객체명) # 객체를 숫자형(실수)로 변환  
as.character(객체명) # 객체를 문자형으로 변환  
as.factor(객체명) # 객체를 팩터로 변환   
```

#### 벡터

벡터는 R 프로그래밍의 기본적인 데이터 단위로 **다른 프로그래밍 언어의 1차원 배열**과도 같은 개념  

하나의 벡터는 같은 데이터 타입을 가진 원소들만 저장 가능  

예를 들어 문자열만 저장하는 배열 혹은 숫자들만 저장하는 배열이 벡터라고 할 수 있음  

```R
# c()를 사용한 벡터 저장
a = c(1, 2, 3)
a
[1] 1 2 3

# :를 사용한 벡터 저장
b = 1:3
b
[1] 1 2 3

# c(1, 2, 3)을 3번 반복   
rep(c(1, 2, 3), 3)
[1] 1 2 3 1 2 3

# 1을 1번 반복, 2를 2번 반복  
rep(c(1, 2), c(1, 2))  

# 1부터 10까지 2씩 증가하는 수열을 변수 c에 저장  
c = seq(1, 10, 2)  

----------------------------------------------------
# 인덱싱
# z 벡터 생성하고 두 번째 원소 출력  
> z = c(1: 5)
> z[2]
[1] 2

# z 벡터의 첫 번째, 세 번째 원소 출력  
> z[c(1, 3)] # 첫 번째 방법
> z[1:3] # 두 번째 방법  
[1] 1 3  

# z 벡터의 다섯 번째 원소만 제외하고 출력  
> z[-5]
[1] 1 2 3 4

# z 벡터의 원소 중 3보다 큰 값만을 출력  
> z[z>3]
[1] 4 5  

# names()를 이용하여 벡터의 각 원소에 대한 이름을 부여 가능  
	# 1 ~ 3 까지의 값이 저장된 벡터 x 생성
	> x <- c(1, 2, 3)
	# x의 각 요소에 대해 Kim, Park, Lee 라는 이름을 지정  
	> names(x) <- c("Kim", "Park", "Lee")  
	# x벡터에서 이름이 Kim인 원소 출력  
	> x["Kim"]
	Kim
	  1

# 벡터의 연산
벡터 간 연산을 실행할 때는 같은 위치의 원소들을 대응시켜 계산 함  
 2 4 6 8
    +  
 1 3 7 9
    =   
3 7 13 17  

# 벡터 간 연산의 예시 1
> x = c(1:4)
> x
[1] 1 2 3 4

> x*3
[1] 3 6 9 12

> x+5
[1] 6 7 8 9  

# 벡터 간 연산의 예시 2  
> y=c(5:8)

> x + y
[1] 6 8 10 12  
```

##### 벡터의 집합 연산  

```R
# x와 y가 동일하면 TRUE, 동일하지 않으면 FALSE를 반환  
identical(x, y) 

# x와 y의 합집합 데이터를 산출 (x, y는 벡터)
union(x, y)

# x와 y의 교집합 데이터를 산출 (x, y는 벡터)
intersect(x, y)

# x와 y의 차집합 데이터를 산출 (x, y는 벡터)
setdiff(x, y)

# x와 y가 같은 집합인지를 판단하여 TRUE 혹은 FALSE를 반환  
setequal(x, y)
```

##### 벡터의 기초통계  

```R
mean(x) # 벡터의 평균
sum(x) # 벡터의 합계  
max(x) # 벡터의 최댓값
min(x) # 벡터의 최솟값 
median(x) # 벡터의 중앙값  
abs(x) # 벡터의 절댓값  
log(x) # 벡터의 로그  
sd(x) # 벡터의 표준편차  
var(x) # 벡터의 분산 
cov(x, y) # 벡터의 공분산  
cor(x, y) # 벡터의 상관계수  
length(x) # 벡터 변수의 길이 값  
```

#### 행렬  

2차원의 벡터로 행과 열의 수가 지정된 구조의 데이터 타입  

벡터와 마찬가지로 하나의 행렬은 한 가지 유형의 스칼라 데이터만 저장 가능  

```R
matrix(data, nrow, ncol, byrow, dimnames)  

data : 행렬에 저장할 데이터  
nrow : 행의 수
ncol : 열의 수  
byrow : 행렬의 데이터 입력 순서 (TRUE : 행우선, FALSE: 열우선)
dimnames : 행렬의 각 차원에 부여할 이름 지정  


# 행렬 생성  
> matrix(1:9, nrow=3, ncol=3, dimnames=list(c("r1", "r2", "r3"), c("a", "b", "c")))

    a  b  c
r1  1  4  7  
r2  2  5  8
r3  3  6  9  


# 행렬 다루기  
행렬 차원 확인 및 부여  :  dim(x) <- c(3, 2) # x 행렬에 3 x 2 차원 부여  
행의 수 확인 : nrow(x) (부여 시 <- 추가) 
열의 수 확인 : ncol(x) (부여 시 <- 추가)
행렬의 원소 추출 : x[nrow, ncol] # x행렬의 3행3열의 원소 추출  
행렬의 특정 행 접근 : 
	x[nrow,] # x 행렬의 3행 추출
	x[-nrow,] # x 행렬의 3행을 제외한 나머지 행 추출  
행렬의 특정 열 접근 : 
	x[,ncol] # x 행렬의 3열 추출  
	x[,-ncol] # x 행렬의 3열을 제외한 나머지 열 추출  
행렬의 각 차원의 이름 확인 및 부여  (부여 시 <- 추가) 
	dimnames(x)<-list(c("r1", "r2", "r3"), c("a", "b", "c"))
행 이름 출력 및 부여 (부여 시 <- 추가)
	rownames(x)<-c("r1", "r2", "r3")
열 이름 출력 및 부여 (부여 시 <- 추가)
	colnames(x)<-c("a", "b", "c")


# 행렬의 연산
# 행렬 x가 존재할 경우
전치행렬 : t(X)  
대각행렬 : diag(x)  
역행렬 : solve(x)  
+, - 연산
	# x 행렬과 y 행렬의 각 원소 간의 덧셈
	x + y  
	# x 행렬과 y 행렬의 각 원소 간의 뺄셈  
	x - y  
	# x 행렬의 각 원소에 숫자 3을 더함  
	x + 3  
*, / 연산
	# x 행렬의 각 원소에 숫자 3을 곱함  
	x * 3  
행렬곱 : x %*% y  
```

#### 데이터 프레임  

데이터프레임은 벡터들의 모임이며, **데이터프레임에 속한 벡터들은 서로 다른 데이터 타입을 가질 수 있다.**  

**벡터는 데이터 프레임의 열을 이루며, 열은 변수, 행은 개체에 해당한다.**  

```R
data.frame(변수명1 = 벡터1, 변수명2 = 벡터2, ... 변수명 n = 벡터 n,
          stringsAsFactors=default.stringsAsFactors())
options:
	stringsAsFactors 
		FALSE : 문자열은 문자형으로 저장  
		TRUE : 문자열은 팩터형으로 저장

# 데이터프레임 생성  
x <- data.frame(이름 = c("이유리", "최민준", "김민지"),
               전공 = c("경영학과", "컴퓨터공학과", "데이터과학과"),
               성별 = c("여", "남", "여"), 나이=c(20, 22, 21))

# 데이터 출력 
> x 
	이름			전공	성별	나이
1  이유리		경영학과    여    20
2  최민준	 컴퓨터공학과	  남    22
3  김민지	 데이터과학과	  여    21

# 데이터의 구조 확인  
str(x)  

# pandas의 iloc과 유사한 기능
    # x의 3행 6열의 원소 출력
    x[3, 6]
    # x의 3행을 제외한 데이터 출력
    x[-3,]
    # x의 6열의 모든 행 출력  
    x[,6]

# pandas의 loc과 유사한 기능  
	# iris 데이터의 Species열 출력  
	iris$Species  

# 열이름 출력 및 부여 (부여 시 <- 추가)
colnames(x)<-c("a", "b", "c")  

# 행결합  
rbind(df1, df2, ...)
**결합할 두 객체의 열의 개수와 열의 이름이 동일해야 함  

# 열결합  
cbind(df1, df2, ...)
**결합할 두 객체의 행의 개수가 동일해야 함  

# 데이터 조회 
dataFrame[조건]
	# ex : x 데이터프레임에서 var1이 4보다 크고, var2가 5인 조건을 만족하는 레코드
	x[x$var1>4 & x$var2==5]  

subset(데이터명, 조건)
	# ex : x 데이터프레임에서 var1이 4보다 크고, var2가 5인 조건을 만족하는 레코드  
	subset(x, var1>4 & var2==0)

subset(데이터명, 조건, select = 열 이름)
	# ex : x 데이터프레임에서 var1이 4보다 큰 레코드의 
	# 		var2, var3 데이터 셋 조회
	# 		이때 변수명에 ""를 표시하지 않음  
	subset(x, var1>4, select=c(var2, var3))

# 데이터프레임의 상위 행을 반환  
head(데이터프레임명, n=반환할 행의 개수)
	# ex : x데이터의 상위 10개의 행 반환, n 인자의 기본값은 6  
	head(x, n=10)

# 데이터프레임의 하위 행을 반환
tail(데이터프레임명, n=반환할 행의 개수)
	# ex : x데이터의 하위 10개의 행 반환, n 인자의 기본값은 6  
	tail(x, n=10)  

# 데이터 뷰어 호출  
View(iris)

# 데이터 병합  
merge(df1, df2, by="df1과 df2의 공통 열이름(병합할 기준이 되는 열)")
	# ex : x와 y를 z라는 공통변수를 기준으로 병합  
	merge(x, y, by=z)

# NA값이 있는 행 삭제  
na.omit(데이터프레임)
	# ex : df에서 NA가 있는 행을 삭제하여 NA_Cleaning 변수에 저장
	NA_Cleaning<-na.omit(df)
```

#### 리스트  

벡터, 데이터프레임, 배열, 함수 등과 같은 R의 모든 객체를 담을 수 있는 데이터 구조  

```R
# 사용법  
list(key1 = value1, key2 = value2, ... , keyN = valueN)

    # 문자형 벡터 생성
    v1 <- c("가", "나", "다")
    v2 <- c(T, F, F)

    # 데이터프레임 생성  
    df<-data.frame(subject=c("미술", "음악", "체육"), class=c("1교시", "2교시", "3교시"))  

    # key를 지정하지 않고 리스트 생성  
    ls1 <- list(v1, v2, df, sum)  

    # key를 지정하여 리스트 생성  
    ls2 <- list(v1=v1, v2=v2, df=df, fun=sum)

# 리스트 다루기  
    # a라는 리스트에서 키 값이 key에 해당하는 원소 출력
    a&key

    # a라는 리스트에서 n번째 키 값에 해당하는 원소 출력
    a[n]

    # key값의 이름으로 원소 선택
    a[['key']]
    a$key
```

#### 배열  

행렬이 2차원이라면 배열은 3차원 또는 n차원 까지 확장된 형태의 다차원 데이터  

```R
array(data=NA, dim=length(data), dimnames=NULL)
"""
options
	data : 배열에 저장할 데이터 지정  
	dim : 배열의 차원을 c()로 묶어서 지정  
	dimnames : 차원의 이름 지정  
"""

# ex  
rname=c("1행", "2행", "3행")
cname=c("1열", "2열", "3열")
mname=c("matrix_1", "matrix_2", "matrix_3")
ar<-array(1:27, dim=c(3, 3, 3), dimnames=list(rname, cname, mname))
```

### 자주사용하는 함수  

```R
print(객체) # 객체를 콘솔에 출력  
cat(객체1, 객체2, ...) # 인자로 주어진 객체들을 연결하여 콘솔에 출력  
rm(변수) # 변수 삭제  
class(객체) # 객체의 물리적자료형 확인  
mode(객체) # 객체의 추상적자료형 확인  
data(데이터명) # R에 내장된 데이터 셋을 불러들임  
attach(데이터명) # 데이터를 R 검색경로에 추가하여 변수명만으로 바로 데이터에 접근 가능하도록 함  
detach(데이터명) # 데이터를 R 검색경로에서 제거  
length(벡터) # 벡터의 길이 산출  
nrow(데이터) # 행의 개수 산출
ncol(데이터) # 열의 개수 산출  
order(벡터) # 벡터에 저장된 값들을 정렬한 순서대로 순서값 부여  
sort(벡터) # 지정한 데이터를 정렬  
summary(데이터 명) # 데이터의 기초통계량 산출  
append(원본벡터, 추가할 벡터, 새로운 벡터를 추가할 위치)
# ex)  
> a <- c(1, 2, 5, 6)
> b <- c(3, 4)
> append(a, b, 3)
[1] 1 2 5 3 4 6  

table(객체) # 객체에 대한 도수분포표 생성  
table(객체1, 객체2) # 두 객체에 대한 이원 분할표 생성  
prop.table(table) # 도수분포표에 대한 범주별 비율 계산

# 데이터를 기준에 따라 분리
split(데이터프레임, 기준) 
split(문자열벡터, 기준)

# 데이터에서 by인자에 지정한 컬럼을 기준으로 지정한 함수를 적용  
aggregate(데이터, by="기준정렬", FUN=적용함수)
aggregate(데이터, data, FUN) # 데이터 전체에 적용  
```

### 문자열 다루기  

```R
문자열길이 반환 : nchar("문자열")
join : paste("문자열1", "문자열2", ..., sep=" ")
split : strsplit("문자열", 구분자)

# str(문자열)에서 대상문자열을 찾아 변경문자열로 한 번만 대치
replace : sub("대상문자열", "변경문자열", str)

# str에 있는 모든 대상문자열을 변경문자열로 대치  
		gsub("대상문자열", "변경문자열", str) 

# str에서 찾을 문자열이 포함된 문자열 혹은 인덱스 출력 
grep("찾을 문자열", str)  
```

### 데이터 입출력

```R
# 경로 확인하기
getwd()

# 폴더 안에 어떤 파일 있는지 확인하기
list.files()

# csv 데이터 파일 읽기  
read.csv("파일명", header=FALSE, sep="구분자", stringAsFactors=TRUE, ...)
"""
options
	header : 첫 행을 변수명으로 지정할지에 대한 여부  
	sep : 데이터셋을 불러올 때 사용할 열 구분자  
	stringsAsFactors : 문자형 데이터를 팩터로 인식하여 데이터를 불러올지에 대한 여부 
"""  

# csv 데이터 파일 저장  
write.csv(저장할 데이터, file="파일경로/파일명", sep="구분자", row.names=TRUE, col.names=TRUE, ...)
```

### 함수 정의 문법 

```R
function(인자1, 인자2, 인자3, ..., 인자n){
    표현식1 
    표현식2
    ... 표현식n
    return(반환 값)
}
```

### 조건문  

```R
# if/else
if(조건1){
    조건1이 참일 때 수행할 코드
} else if (조건2) {
    조건1이 거짓이고
    조건2가 참일 때 수행할 코드
} else {
    모든 조건이 거짓일 때 수행할 코드  
}  

# ifelse  
ifelse(조건, a, b) 
"""
조건이 참이면 a자리의 코드를 실행하고, 거짓이면 b자리의 코드를 실행
내부에 또 다른 ifelse 구문을 중첩하여 사용이 가능  
"""
```

### 반복문  

```R
# for  
for(변수 in 데이터){
    반복할 코드  
}

# while
변수 <- 초기값

while(조건){
    조건이 참일 때 수행할 코드  
}

# repeat  
repeat{
    반복할 코드  
}  
"""
끝없이 실행되기 때문에 주로 if문, break문과 함께 사용  
"""  
```

## 데이터 탐색

### 개수 확인  

```R
nrow(data) # 행 개수 확인 
dim(data) # 데이터의 개수 확인
```

### 결측치 인식

```R
is.na : 데이터의 요소가 NA값, 즉 결측치일 경우 TRUE를 반환하고 그렇지 않을 경우 FALSE를 반환해주는 함수이다. 인자인 x 자리에는 벡터, 리스트 등의 R 객체가 들어간다.  
"""
is.na 함수의 결과는 논리값이기 때문에 산술계산이 가능하다.  
NA가 존재하는 경우 결과값이 TRUE인데, R은 TRUE를 숫자 1로 인식하기 때문에 
is.na 함수를 적용한 후 합을 구하면 결측치의 개수를 쉽게 파악 가능하다.  
"""  


complete.cases(X) : 해당 데이터가 결측치를 가지고 있지 않은 완전한 데이터인지를 묻는 함수이다. 따라서 데이터에 결측치가 없으면 TRUE, 있으면 FALSE를 반환해주며, 인자 X자리에는 벡터 혹은 리스트 등의 R 객체가 들어간다.  
"""
is.na 함수는 데이터의 각 행에 대해 변수별로 na 값이 존재하는지의 여부를 반환하는 반면, complete, cases 함수는 여러 변수들 중 na 값이 하나라도 존재하는 행은 FALSE를 반환한다. 따라서 na 값이 하나라도 존재하는 행을 찾을 때에 편리하다.  
"""  
# is.na 함수 활용
is.na(airquality$Ozone)

# Ozone 변수에 존재하는 na 개수 산출  
sum(is.na(airquality$Ozone))
[1] 37
# Ozone 변수에서 na가 아닌 값과 na값의 개수 비교  
# table(): 변수별 도수를 구해주는 함수  
# FALSE : 해당 데이터가 na가 아닌 경우, TRUE : 해당 데이터가 na인 경우  
table(is.na(airquality$Ozone))  
FALSE  TRUE 
  116    37 

# airquality 의 변수별로 결측치의 개수를 구하는 사용자 정의 함수를 적용  
# sum(is.na(x)) : x 데이터에 존재하는 na값의 개수의 합계를 구함  
apply(airquality, 2, function(x) sum(is.na(x)))
  Ozone Solar.R    Wind    Temp   Month     Day 
     37       7       0       0       0       0 
      
# na 값이 하나라도 존재하는 행들은 air_na 변수에 저장  
# complete.cases 함수를 적용했을 때 FALSE를 반환하는 행들만 저장하면 됨  
air_na<-airquality[!complete.cases(airquality), ]
head(air_na)
   Ozone Solar.R Wind Temp Month Day
5     NA      NA 14.3   56     5   5
6     28      NA 14.9   66     5   6
10    NA     194  8.6   69     5  10
11     7      NA  6.9   74     5  11
25    NA      66 16.6   57     5  25
26    NA     266 14.9   58     5  26
      
# na 값을 하나도 가지고 있지 않은 행들은 air_com 변수에 저장  
# complete.cases함수를 적용했을 때 TRUE를 반환하는 행들만 저장하면 됨  
air_com <- airquality[complete.cases(airquality),]
  Ozone Solar.R Wind Temp Month Day
1    41     190  7.4   67     5   1
2    36     118  8.0   72     5   2
3    12     149 12.6   74     5   3
4    18     313 11.5   62     5   4
7    23     299  8.6   65     5   7
8    19      99 13.8   59     5   8
```

### 결측치 처리  

```R
# 1. 결측치 대치법  
데이터에 결측치가 존재할 때 이 결측치를 대치하기 위한 방법은 아래와 같이 단순 대치법과 다중대치법으로 분류된다.  

## 단순 대치법  
"""
completes analysis : 결측값이 존재하는 행을 삭제  
평균대치법 : 관측 또는 실험을 통해 얻어진 데이터의 평균으로 결측치를 대치  
	- 비조건부 평균 대치법 : 관측 데이터의 평균값으로 대치 
	- 조건부 평균 대치법 : 회귀분석을 활용한 대치법  
단순확률대치법 : 평균대치법에서 추정량 표준 오차의 과소 추정문제를 보완하고자 고안됨
	- Hot-deck 방법, nearest neighbor 방법 등이 있음  
"""  

## 다중 대치법  
단순 대치법을 한 번이 아닌 m번 수행하여 m개의 가상적 완전자료를 만드는 방법  
대치 => 분석 => 결합  


# 2. 결측치 제거  
데이터에서 특정 행의 모든 변수값 중 결측치가 하나라도 존재하는 경우, 해당 행을 제거한 후 데이터 분석을 진행하고자 할 때 결측치 제거를 수행한다. is.na 함수 혹은 complete.cases함수 적용 결과에 따라 결측치가 존재하는 행을 데이터에서 제외시키는 방법으로 수행하거나 na.omit이라는 결측치 제거 함수를 사용할 수 있다.  

na.omit은 인자로 지정한 데이터 프레임에서 결측치가 존재하는 행을 제외시켜주는 함수이다. 결측치 제거 시 사용할 수 있는 방법은 아래와 같으며, 이 외에도 다른 패키지나 조건을 활용하여 다양한 방식으로 결측치 제거를 수행할 수 있다.  

	# 결측치가 존재하는 제거
	데이터명[!is.na(데이터명), ]
	데이터명[complete.cases(데이터명), ]
	데이터명 %>% filter(!is.na(데이터명))  

	# na.omit 함수 활용  
	na.omit(데이터명)  


# 3. 평균 대치법  
결측치가 존재할 경우, 해당 변수 값들의 평균으로 빈 값들을 대치할 수 있다.  

# Q1. R의 내장데이터 airquality의 Ozone 변수 값이 존재하지 않는 경우, Ozone 변수 값들의 평균으로 대치해보자.  
# 데이터에 NA 가 존재할 경우 평균을 산출할 수 없다. 따라서 mean함수 내부의 na.rm 인자 값을 T로 지정해야 하며, 이렇게 할 경우 NA 값을 제거하고 나머지 값들에 대한 평균을 산출한다.  
airquality$Ozone <- ifelse(is.na(airquality$Ozone), mean(airquality$Ozone, na.rm=T), airquality$Ozone)

```

### 이상치 인식  

```R
# 이상치란?  
이상치는 관측된 데이터의 범위에서 많이 벗어나있는 아주 작거나 아주 큰 값으로서 정상 범위 밖에 있는 값을 뜻한다. 이러한 이상치는 잘못 입력된 값일 수도 있으나 실제로 존재하는 값일 수도 있으며, 전체 데이터 분포에 큰 영향을 미친다.  

이상치가 존재할 경우 분석 결과가 특정한 쪽으로 치우치거나 왜곡될 수 있다. 따라서 데이터에서 이상치를 인식한 후, 이를 제외하고 분석을 할 지 혹은 포함하거나 조정하여 분석을 할 지 판단한 후에 분석을 수행해야한다. 일반적으로 이상치는 사분위수, 정규분포 등을 활용해 판별한다.  

# 사분위수  
사분위수란 데이터 표본을 가장 작은 값부터 가장 큰 값으로 정렬한 후, 4등분 했을 때 각 등위에 해당하는 값을 의미한다.   

제1사분위수 : 데이터를 크기순으로 나열했을 때 25% 지점에 해당하는 수
제2사분위수 : 데이터를 크기순으로 나열했을 때 50% 지점에 해당하는 수
제3사분위수 : 데이터를 크기순으로 나열했을 때 75% 지점에 해당하는 수
사분위범위 : 제1사분위수와 제3사분위수 간의 거리 (Q3 - Q1)  

# 제p백분위수  
데이터를 크기순으로 나열했을 때, 해당 값보다 작거나 같은 자료의 수가 전체의 p% 이상이고, 해당 값보다 크거나 같은 자료의 수가 적어도 전체의 (100-p)% 이상이 되는 값을 의미한다. 따라서 제1사분위수는 25백분위수, 제2사분위수는 50백분위수, 제3사분위수는 75백분위수라고도 할 수 있다.  

quantile(x, prob=seq(0, 1, 0.25), na.rm=FALSE, ...)
```

### boxplot을 활용

```R
# 사분위수는 일반적으로 상자그림을 통해서 시각화한다.  
# 상자그림이란 데이터의 분포를 보여주며 아래와 같이 숫자형 데이터의 제1사분위수, 제2사분위수, 제3사분위수, 사분위 범위, 이상치를 시각화한 그림이다.

# 위 그림에서 상자의 시작 선은 제1사분위수, 상자 중간선은 제2분위수, 상자의 끝 선은 제3사분위수를 나타낸다. 따라서 상자의 길이는 전체 데이터의 50%에 해당하는 사분위 범위(IQR)을 시각적으로 나타내게 된다.  

# 상자 밖으로 이어져 있는 선은 수염이라고 하며, 수염의 시작선은 'Q1-1.5*IQR'보다 큰 값중에서 가장 작은 수이며, 수염의 마지막 선은 'Q3+1.5*IQR' 보다 작은 값 중에서 가장 큰 수를 각각 의미한다. 수염의 각 양옆에 분포된 점들은 이상치이며, upper whisker보다 크거나 lower whisker보다 작은 값들이 이에 해당한다.  

# 숫자들 중 특정 값이 [중앙값-1.5 * IQR ~ 중앙값 + 1.5 * IQR] 범위에서 벗어나 있는 경우 이상치로 간주한다. 이러한 값의 분포를 상자 그림을 통해 시각적으로 파악하고자 할 때는 boxplot함수를 사용할 수 있다.  

boxplot(formula, data=NULL, horizontal=FALSE, ...)
"""
options
	formula : y-grp의 형태로 지정하는데, 
			 grp는 g값을 그룹짓는 변수이며 y는 분포를 그릴 값에 해당
			 formula를 지정할 경우 grp별 y값에 대한 상자그림 그릴 수 있음
	data : 포뮬러를 적용할 데이터
	horizontal
		- 상자그림을 세로로 그릴지에 대한 여부
		- TRUE로 지정하면 세로로, FALSE로 지정하면 가로로 상자그림을 그림
	x : 상자그림으로 표현하고자 하는 숫자형 벡터  
"""  
```



## 데이터 변환  

### 파생변수 추가

```R
# $
데이터프레임$변수명<-추가할 변수의 데이터 벡터

# []
데이터프레임["변수명"]<-추가할 변수의 데이터 벡터  

# transform  
transform(데이터프레임, var1=data1, var2=data2, ...)
# ex
transform(iris, Sum.Length=Sepal.Length + Petal.Length)

# within  
within(데이터, 표현식)
# ex
score_df <- within(score_df, {
    grade = character(0)
    grade[score < 60] = "가"
    grade[score >= 60 & score < 70] = "양"
})
```

### 주성분분석  

```R
prcomp(데이터, center=TRUE, scale.=FALSE, ...)
"""
options
	데이터 : 주성분분석을 수행할 행렬 혹은 데이터프레임
	center : 값을 TRUE로 지정할 경우 데이터의 중심이 0이 되게 함  
	scale : 값을 TRUE로 지정할 경우 데이터를 표준화함
"""

princomp(데이터, cor=FALSE, scores=TRUE, ...)
"""
options
	데이터: 주성분분석을 수행할 행렬 혹은 데이터프레임
	cor:
		FALSE: 공분산행렬로 주성분 분석 수행
		TRUE: 상관행렬로 주성분 분석 수행
		공분산행렬은 변수의 측정 단위를 반영한 것이고,
		상관행렬은 변수의 측정 단위를 표준화한 것임
	scores: 각 주성분의 점수를 계산해야 하는지의 여부를 나타내는 논리 값  
"""

# ex  
# 주성분분석 객체를 만듦
Us.prin<-princomp(USArrests, cor=TRUE)
# 결과에 대한 요약 확인  
summary(Us.prin)
# 로딩을 통해 주성분 계수 가중치를 확인  
Us.prin$loadings  
# 차원축소로 얻어지는 주성분 점수를 확인  
Us.prin$scores  


```

### 요인분석  

```R
factanal(데이터, factors=n, rotation="varimax", scores="regression", ...)
"""
options
	데이터 : 요인분석을 수행할 숫자형 행렬 혹은 데이터 프레임
	factors : 요인의 개수 지정  
	rotation : 요인 회전방법을 선택 ("varimax", "promax", "none")
	scores : 요인점수 계산방법을 선택 ("regression", "Bartlett")
"""
```

### 표준화와 정규화  

```R
# 표준화 : 평균을 기준으로 거리 조정
scale(데이터, center=TRUE, scale=TRUE)
"""
options
	데이터 : 숫자형 벡터
	center : TRUE 면 데이터에서 해당 벡터의 평균을 뺌  
	scale
		center=TRUE, scale=TRUE 이면 데이터를 해당 벡터의 표준편차로 나눔
		cneter=FALSE, scale=TRUE 이면 데이터를 해당 벡터의 제곱평균제곱근(RMS)으로 나눔
		scale=FALSE이면 데이터를 어떤 값으로도 나누지 않음  
"""

# 정규화 : 데이터의 분포를 조정
# ex) Min, Max 정규화 (Xi - min) / (max - min)
> Min<-min(iris$Sepal.Length)
> Max<-max(iris$Sepal.Length)
> iris$SL_new<-scale(iris$Sepal.Length, center=Min, scale=Max-Min)

# ex) 사용자 정의 함수를 이용해서도 가능
> normalize<-function(x){
+ return((x - min(x)) / (max(x) - min(x)))
+ }
> num=c(50:500)
> num_new<-normalize(num)
> head(num_new)
[1] 0.000000000 0.002222222 0.004444444 0.006666667 0.008888889 0.011111111
```



## 데이터 시각화  

### 산점도

```R
# 데이터 확인 및 산점도를 통한 변수 간 상관관계 파악
library(datasets)
data(USArrests)
head(USArrests)

# pairs(): 둘 이상의 변수에 대해 모든 가능한 산점도를 그려줌  
pairs(USArrests, panel=panel.smooth, main="제목")
```

### 행렬도  

```R
# 제1주성분과 제2주성분으로 이루어진 좌표평면 상에 원 데이터 행들의 주성분점수를 산점도의 형태로 나타내고, 각 변수에 대한 주성분계수를 화살표로 시각화하여 그래프로 표현해줌
biplot(US.prin, scale = 0)
```

## 데이터 결합 및 요약  

### rbind  

```R
> customer1<-data.frame(id = c("c01","c02","c03","c04"), last_name = c("Lee","Kim","Choi","Park")) # customer1 변수 생성 (데이터 프레임 형)  
> customer2<-data.frame(id = c("c05","c06","c07"),last_name = c("Lim","Bae","Kim")) # customer2 변수 생성 (데이터 프레임 형)

> customer1
   id last_name
1 c01       Lee
2 c02       Kim
3 c03      Choi
4 c04      Park
> customer2
   id last_name
1 c05       Lim
2 c06       Bae
3 c07       Kim  

# 이를 rbind로 행 결합 가능  
> id_name = rbind(customer1, customer2)

> id_name
   id last_name
1 c01       Lee
2 c02       Kim
3 c03      Choi
4 c04      Park
5 c05       Lim
6 c06       Bae
7 c07       Kim
```

### cbind

```R
> age_income<-data.frame(age = c(20, 25, 37, 40, 32, 45, 37), income = c(2500, 6400, 0, 7000, 3400, 3800, 5010))

> age_income
  age income
1  20   2500
2  25   6400
3  37      0
4  40   7000
5  32   3400
6  45   3800
7  37   5010

> id_name
   id last_name
1 c01       Lee
2 c02       Kim
3 c03      Choi
4 c04      Park
5 c05       Lim
6 c06       Bae
7 c07       Kim

# cbind 이용해 열 결합  
> customer<-cbind(id_name, age_income)

> customer
   id last_name age income
1 c01       Lee  20   2500
2 c02       Kim  25   6400
3 c03      Choi  37      0
4 c04      Park  40   7000
5 c05       Lim  32   3400
6 c06       Bae  45   3800
7 c07       Kim  37   5010
```

### merge  

```R
# 기준이 되는 특정 칼럼의 값이 같은 행끼리 묶어 병합하는 함수  
merge(x, y, by, by.x, by.y, all=FALSE, all.x, all.y)
"""
options
	x, y : 병합할 데이터 프레임  
	by : 병합할 기준이 되는 칼럼  
	by.x, by.y : 데이터프레임 x와 y에서 기준으로 사용할 칼럼의 이름이 서로 다른 경우
				by.x와 by.y 인자를 통해 지정
	all : 기준 칼럼에 대한 공통 값이 x 혹은 y 중 어느 한쪽에 없는 경우의 처리를 위한 		  인자
		all=FALSE : x, y 모두가 공통 값을 가지고 있는 행만 병합
		all=TRUE : x 혹은 y 중 공통 값을 가지고 있지 않은 행에 대해서는 
				  NA로 값을 채운 뒤 x와 y의 전체 행이 병합됨
	all.x, all.y : x 혹은 y 중 한쪽에 공통된 값이 없지만 해당 데이터의 모든 행이
				 결과데이터에 포함되도록 하고자 할 때 사용
		all.x=TRUE : x 데이터의 모든 행이 결과에 포함
		all.y=TRUE : y 데이터의 모든 행이 결과에 포함  
"""

id_name<-data.frame(id = c("c01", "c02", "c03", "c04", "c05", "c06", "c07"),
+ last_name = c("Lee", "Kim", "Choi", "Park", "Lim", "Bae", "Kim"))

id_number <- data.frame(id = c("c03", "c04", "c05", "C06", "c07", "c08", "c09"),
+ number = c(3, 1, 0, 7, 3, 4, 1))

id_name
   id last_name
1 c01       Lee
2 c02       Kim
3 c03      Choi
4 c04      Park
5 c05       Lim
6 c06       Bae
7 c07       Kim

id_number
   id number
1 c03      3
2 c04      1
3 c05      0
4 C06      7
5 c07      3
6 c08      4
7 c09      1  

# id 칼럼 기준으로 공통된 값만 병합 (inner Join)
merge(id_name, id_number, by = 'id')
   id last_name number
1 c03      Choi      3
2 c04      Park      1
3 c05       Lim      0
4 c07       Kim      3

# id 칼럼 기준으로 공통값 없어도 두 데이터의 모든 행을 병합 (Outer Join)
merge(id_name, id_number, by = 'id', all = T)
    id last_name number
1  c01       Lee     NA
2  c02       Kim     NA
3  c03      Choi      3
4  c04      Park      1
5  c05       Lim      0
6  c06       Bae     NA
7  C06      <NA>      7
8  c07       Kim      3
9  c08      <NA>      4
10 c09      <NA>      1

# id 칼럼 기준으로 두 데이터를 병합, 이때 기준 칼럼에 공통값 없을 경우 id_name 데이터를 기준으로 병합 (Left Outer Join)
	# id_name에 id_number을 붙이고 빈 값을 NA로 채움
merge(id_name, id_number, by='id', all.x=T)
   id last_name number
1 c01       Lee     NA
2 c02       Kim     NA
3 c03      Choi      3
4 c04      Park      1
5 c05       Lim      0
6 c06       Bae      7
7 c07       Kim      3
# id 칼럼 기준으로 두 데이터 병합, 이때 기준 칼럼에 공통값 없을 경우 id_number 데이터를 기준으로 병합 (Right Outer Join)
	# id_number에 id_name을 붙이고 빈 값을 NA로 채움  
> merge(id_name, id_number, by = 'id', all.y = T)
   id last_name number
1 c03      Choi      3
2 c04      Park      1
3 c05       Lim      0
4 C06      <NA>      7
5 c07       Kim      3
6 c08      <NA>      4
7 c09      <NA>      1  
```

### aggregate  

```R
# 특정 칼럼을 기준으로 데이터를 그룹지어 집계함수를 적용
aggregate(x, by, FUN)
aggregate(formula, data, FUN)

"""
options
	x : R 객체
	by : 데이터를 그룹화 할 값들의 리스트  
	FUN : 적용할 함수

	formula : 종속변수 ~ 독립변수의 형태로 
			  <집계함수를 적용시킬 열 ~ 그룹화 할 기준이 되는 열> 형태로 입력
	data : 연산을 수행할 데이터 프레임 
"""

# Q1. iris 데이터에서 종별 Sepal.Width의 평균 구하기
> aggregate(Sepal.Width~Species, iris, mean)
     Species Sepal.Width
1     setosa       3.428
2 versicolor       2.770
3  virginica       2.974

# Q2. iris 데이터에서 종별 Sepal.Width와 Petal.Width의 평균 구하기 
> aggregate(cbind(Sepal.Width, Petal.Width)~Species, iris, mean)
     Species Sepal.Width Petal.Width
1     setosa       3.428       0.246
2 versicolor       2.770       1.326
3  virginica       2.974       2.026  
```

### table  

```R
# 범주형 변수에 대해서 각 범주별 도수를 알기 위해 도수분포표를 만들 때 이용  
table(범주형변수) - 도수분포표 생성
table(범주형변수1, 범주형변수2) - 두 변수 간 이원분할표 생성  

# table 함수를 이용하여 범주형 변수 Class에 대한 도수분포표를 생성  
> table(Titanic$Class)  
1st  2nd  3rd Crew 
8    8    8    8 

# Class 변수에 따른 Survived 변수의 도수를 표 형태로 나타냄  
> table(Titanic$Class, Titanic$Survived)
       No Yes
  1st   4   4
  2nd   4   4
  3rd   4   4
  Crew  4   4
```

### prop.table  

```R
# 범주형 변수에 대한 상대도수(비율)을 알고자 할 때 이용  
prop.table(table 객체)
prop.table(table 객체, 1) # 행별 상대도수 파악
prop.table(table 객체, 2) # 열별 상대도수 파악  

# Age에 따른 Survived에 대한 비율을 파악  
> prop.table(table(Titanic$Age, Titanic$Survived))
          No  Yes
  Child 0.25 0.25
  Adult 0.25 0.25

# 행 별 비율 파악  
> prop.table(table(Titanic$Age, Titanic$Survived), 1)
         No Yes
  Child 0.5 0.5
  Adult 0.5 0.5

# 열 별 비율 파악  
> prop.table(table(Titanic$Age, Titanic$Survived), 2)
         No Yes
  Child 0.5 0.5
  Adult 0.5 0.5
```

### subset (조건)

```R
# 전체데이터에서 특정 조건을 만족하는 값들만 추춣할 때는 subset 함수를 사용한다.
subset(data, subset, select=c(var1, var2, ...))
"""
options
	data : 데이터를 추출할 벡터, 행렬, 데이터프레임
	subset : 추출하고자 하는 데이터의 조건을 지정
	select : 데이터프레임에서 특정 열만을 조회하고자 할 때 해당 열들을 c()로 묶어 지정
"""

# Q1. 내장데이터 iris에서 종(Species)가 setosa 이면서, Sepal.Length의 값이 5.5 초과인 데이터들의 Species와 Sepal.Length 변수 값만 조회해보자.
> subset(iris,
+ subset = (Species == 'setosa' & Sepal.Length > 5.5), 
+ select = c(Species, Sepal.Length))
   Species Sepal.Length
15  setosa          5.8
16  setosa          5.7
19  setosa          5.7
```

## apply 계열 함수

```R
# 빠르고 쉽게 데이터 요약을 수행하여 원하는 정보를 확인
```

### apply  

```R
# apply는 데이터의 행 혹은 열 방향으로 주어진 함수를 한 번에 적용한 뒤
# 그 결과를 벡터, 배열, 리스트로 반환하는 함수이다.

apply(X, MARGIN, FUN)
"""
options
	X : 배열 또는 행렬
	MARGIN : MARGIN = 1 : 행 방향, MARGIN = 2 : 열 방향
	FUN : 적용할 함수
"""
# 4행 3열로 이루어진 행렬을 만든 후에 각 행별로 max 값을 구해보자. 
> a<-matrix(1:12, nrow=4, ncol=3)  
 
> a
     [,1] [,2] [,3]
[1,]    1    5    9
[2,]    2    6   10
[3,]    3    7   11
[4,]    4    8   12  
 
> apply(a, 1, max)
[1]  9 10 11 12


# iris 데이터의 1~4열에 대해서 평균을 구해보자.  
> apply(iris[,1:4], 2, mean)
Sepal.Length  Sepal.Width Petal.Length  Petal.Width 
    5.843333     3.057333     3.758000     1.199333
```

### lapply  

```R
# apply 함수는 벡터, 리스트, 표현식, 데이터 프레임 등에 함수를 적용하고, 그 결과를 리스트로 변환한다.  
# lapply는 데이터프레임에 대해서는 열 방향으로 함수를 적용한다.
> a <- c(1,2,3)
> lapply(a, FUN = function(x){x^2})
[[1]]
[1] 1
[[2]]
[1] 4
[[3]]
[1] 9

# 반환 값이 리스트임을 확인 가능
class(lapply(a, FUN = function(x){x^2}))
[1] "List"

# 만약 리스트로 반환된 결과를 벡터로 변환하고 싶을 때 unlist 함수 이용
b <- lapply(a, FUN=function(x){x^2})
unlist(b)
[1] 1 4 9  
```

### sapply  

```R
# sapply는 벡터, 리스트, 표현식, 데이터프레임 등에 함수를 적용하고, 그 결과를 벡터 혹은 행렬로 반환한다.
# lapply와 마찬가지로 데이터프레임에 대해서는 열별로 함수를 적용한다.

sapply(X, FUN. simplify=TRUE, ...)
"""
options
	X : 벡터, 리스트, 표현식, 데이터프레임
	FUN : 적용할 함수  
	simplify : 단순화에 대한 여부를 지정하기 위한 인자
		simplify=FALSE : 값을 설정하면 리스트가 반환됨
"""


"""
sapply 함수의 결과에 따른 반환 형태  
1. 변수마다 함수를 적용한 결과 값의 개수가 1개씩이면 벡터로 반환 
2. 변수마다 함수를 적용한 결과 값의 개수가 1보다 크면 행렬로 반환  
3. 함수를 적용한 결과 값의 개수가 변수마다 다르면 단순화할 수 없으므로 리스트로 반환  
"""  

# iris 데이터에서 각 컬럼에 summary 함수를 적용
> sapply(iris, summary)
$Sepal.Length
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
  4.300   5.100   5.800   5.843   6.400   7.900 

$Sepal.Width
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
  2.000   2.800   3.000   3.057   3.300   4.400 

$Petal.Length
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
  1.000   1.600   4.350   3.758   5.100   6.900 

$Petal.Width
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
  0.100   0.300   1.300   1.199   1.800   2.500 

$Species
    setosa versicolor  virginica 
        50         50         50 

> class(sapply(iris, summary))
[1] "list"
```

### mapply  

```R
# sapply의 확장 버전으로 여러 개의 리스트 또는 벡터로 주어진 인자를 받아 함수를 적용한 후 결과를 반환, 다수의 요소를 한 번에 적용이 가능  

mapply(FUN, 인자1, 인자2, ... 인자n, ...)

"""
options
	FUN : 적용할 함수  
	인자n : 함수에 넣을 인자에 해당하는 벡터 혹은 리스트  
"""  

# rep 함수 이용 시
> rep(1, 4)
1 1 1 1
> rep(2, 3)
2 2 2
> rep(3, 2)
3 3
> rep(4, 1)
4  

# mapply 사용 시
mapply(rep, c(1:4), c(4:1))
[[1]]
[1] 1 1 1 1
[[2]]
[2] 2 2 2
[[3]]
[3] 3 3
[[4]]
[4] 4
```

### vapply  

```R
# vapply는 sapply와 유사하나 출력결과의 형태를 사용자가 직접 지정할 수 있다.  
vapply(X, FUN, FUN, VALUE, ...)

"""
options
	X : 벡터, 리스트, 표현식, 데이터프레임
	FUN : 적용할 함수  
	FUN.VALUE : 함수 실행 후 출력되는 값의 형태를 지정  
"""  
> test <- c(1:100)

> test2 <- vapply(test, fivenum, c("Min"=0, "Q1"=0, "Median"=0, "Q3"=0, "Max"=0))

> test2
        [,1]
Min      1.0
Q1      25.5
Median  50.5
Q3      75.5
Max    100.0
```

### tapply

```R
# 데이터를 특정 기준에 따라 그룹으로 나눈 뒤 각 그룹별로 함수를 적용하여 결과 반환  
tapply(DATA, INDEX, FUN, ...)

"""
options
	DATA : 벡터 (데이터프레임의 특정 열)
	INDEX (기준) : 데이터를 그룹별로 나누기 위한 기준
				팩터를 지정해야하며 팩터가 아닌 경우 팩터로 형 변환 이뤄짐
				비교구문을 이용하여 그룹을 나누는 것도 가능  
	FUN : 적용할 함수
"""  

# R의 googleVis 패키지에 있는 Fruits 데이터에서 과일종류 별 판매량의 평균을 구해보자.
> head(Fruits)
    Fruit Year Location Sales Expenses Profit       Date
1  Apples 2008     West    98       78     20 2008-12-31
2  Apples 2009     West   111       79     32 2009-12-31
3  Apples 2010     West    89       76     13 2010-12-31
4 Oranges 2008     East    96       81     15 2008-12-31
5 Bananas 2008     East    85       76      9 2008-12-31
6 Oranges 2009     East    93       80     13 2009-12-31
 
# tapply 함수를 이용하여 과일종류별 판매량의 평균 산출  
> tapply(Fruits$Sales, Fruits$Fruit, mean)
  Apples  Bananas  Oranges 
99.33333 86.66667 95.66667 

# Fruits 데이터에서 Location이 West인 것과 아닌 것으로 그룹을 지정하여 Profit 평균 산출  
> tapply(Fruits$Profit, Fruits$Location=="West", mean)
   FALSE     TRUE 
11.66667 21.66667 
```

# R을 이용한 표본 추출

## 단순임의추출

```R
# 전체 데이터에서 데이터를 선택할 확률을 모두 동일하게 하여 표본을 추출하는 방법  

# 복원 추출 : 한 번 선택한 표본을 다시 추출  
# 비복원추출 : 한 번 선택된 표본은 다시 추출 불가  

sample(x, size, replace=FALSE, prob=NULL)
"""
options  
  x : 표본을 추출할 벡터  
  size : 표본의 크기  
  replace : 복원 추출 여부를 지정  
	replace=TRUE : 복원 추출
	replace=FALSE : 비복원 추출  
  prob : 데이터를 뽑을 때의 가중치 지정  
		예를 들어, prob=c(2, 4, 6)을 지정하면 
		첫 번째 데이터가 뽑힐 확률은 20%  
		두 번째 데이터가 뽑힐 확률은 40%
		세 번째 데이터가 뽑힐 확률은 60%
"""

# iris 데이터로 분석을 진행하기 위해 전체 데이터의 7:3 비율로 training data와 test data를 추출한 뒤 새로운 변수에 저장해보자. (단순 임의 추출 사용)  

# iris 데이터 행의 개수에서 70%에 해당하는 행번호를 랜덤으로 추출  
# nrow(): 데이터의 행 개수를 산출해주는 함수  
idx <- sample(1:nrow(iris), nrow(iris)*0.7, replace=FALSE)

# 추출한 행번호를 이용하여 training 데이터와 test 데이터 생성
training<-iris[idx,]
test<-iris[-idx,]
```

## 층화 임의 추출  

```R
특정 데이터가 여성 70% 남성 30 % 로 구성되어 있다고 가정해보자.  
각 계층을 고루 대표할 수 있도록 표본을 추출하기 위해서는 여성과 남성 집단에 대해 0.7:0.3 의 비율로 데이터를 뽑아야 한다.  
이처럼 여성과 남성이라는 계층별로 표본을 추출하는 것을 층화 임의 추출이라고 한다.  

strata(data, stratanames=NULL, size, method=c(), pik, description=FALSE)
"""
options 
  data : 표본을 추출할 데이터프레임 또는 행렬  
  stratanames : 데이터에서 계층을 구분하는 변수들 (여러 개일 경우 벡터로 나열)
  size : 각 계층에서 추출할 데이터의 개수  
  method : 
	srswor : 비복원 단순 임의 추출  
	srswr : 복원 단순 임의 추출
	poisson : 포아송 추출 
    systematic : 계통 추출
  pik : 데이터를 표본에 포함시킬 확률  
  description : 표본크기와 모집단 크기를 추출할지의 여부 (TRUE / FALSE)  
"""

# strata 함수를 통해 층화 임의 추출을 수행하여 얻어진 데이터는 getdata 함수를 통해 확인할 수 있다.   
# 즉 getdata는 원본 데이터에서 표본 추출을 통해 얻어진 데이터를 출력해준다.  
getdata(data, m)

# iris 데이터에서 Species가 setosa인 데이터를 20개, versicolor 인 데이터를 15개, versinica인 데이터를 15개 씩 층화 임의 추출을 사용해 추출해보자.
""" 
strata 함수를 이용하려면 samplig 패키지를 설치해야 함.
하지만 데이터 분석 기사에서 sampling 함수를 사용할 수 없으니 단순임의추출을 통해서 층화임의 추출을 표현해보도록 하겠음 
"""  
setosa <- iris %>% filter(Species=="setosa")
versicolor <- iris %>% filter(Species=="versicolor")
virginica <- iris %>% filter(Species=="virginica")

setosa_sample <- setosa[sample(1:nrow(setosa), 20, replace=TRUE),]
versicolor_sample <- versicolor[sample(1:nrow(versicolor), 15, replace=TRUE),]
virginica_sample <- virginica[sample(1:nrow(virginica), 15, replace=TRUE),]  

iris_sample <- bind_rows(setosa_sample, versicolor_sample, virginica_sample)
```



# 정규성 검정  

```R
# 1. 샤피로-윌크 검정

# 샤피로-윌크 검정의 귀무가설은 '데이터가 정규분포를 따른다' 이고, 대립가설은 '데이터가 정규분포를 따르지 않는다' 이다.

shapiro.test(data)
```

# 등분산성 검정  

```R
var.test(x, y, alternative)  
var.test(formula, data, alternative)  

"""
options
	x : 모집단 1로부터 측정한 관측값  
	y : 모집단 2로부터 측정한 관측값  
	formula : 수치형 벡터(종속변수) ~ 집단분류(독립변수)
	data : 등분산 검정을 수행할 데이터명  
	alternative : 양측검정시 "two.sided", 단측검정시 "less", "greater" 입력  
"""
```



# T-검정 (T-test)  

https://colab.research.google.com/drive/1PIZjm7zJ-CnXSKfzYah7ZZCEHllTFbXS?usp=sharing

## one sample t-test

```R
# one sample t-test

# 데이터가 정규분포를 따른다는 가정을 만족한 경우, t.test 함수를 사용하여 일표본-T검정을 수행한다.

# 반면 데이터가 정규성을 만족하지 않는 경우, wilcox.test 함수를 이용해 T-검정을 수행한다.

t.test(x, alternative=c("two.sided", "less", "greater"), mu=0)
wilcox.test(x, alternative=c("two.sided", "less", "greater"), mu=0)

"""
options  
	x : 표본으로부터 관측한 값 (수치형 벡터)  
	alternative 
		양측검정 : "two.sided" 입력
		단측검정 
			"less" : 표본 평균이 특정 값보다 작은지에 대해 검정을 수행할 시
			"greater" : 특정 값보다 큰지에 대한 검정 수행 시  
	mu : 검정시 기준이 되는 값  
"""
```

## two-sample t-test   

```R
# R에서 대응표본 t-검정을 수행하기 위해 사용하는 함수는 t.test이며, 문법은 아래와 같다.  

t.test(x, y, alternative=c("two.sided", "less", "greater"), paired=FALSE, m=0)  

"""
options 
	x : 처리방법이 x일 때의 관측값 (모집단에서 x처리 관측값)
	y : 처리방법이 y일 때의 관측값 (모집단에서 y처리 관측값)
 	alternative 
		양측검정시 "two.sided" 
		단측검정시 "less", "greater"  
	paired : 대응표본 t-검정을 수행할지에 대한 여부  
		FALSE : 기본값  
		TRUE : 대응표본 t-검정 수행시 TRUE로 지정  
	m 
		: 검정의 기준이 되는 값으로 기본 값은 0
		: 대응표본 t-검정에서는 모평균의 차이가 0인지를 검정하기 때문에,		
		  m인자는 적지 않아도 된다.  
"""
```

## Independent sample t-test

```R
t.test(x, y, alternative, var.equal=FALSE)
t.test(formula, data, alternative, var.equal=FALSE)  

"""
options  
	x : 모집단 1로부터 측정한 관측값 (수치형 벡터)
	y : 모집단 2로부터 측정한 관측값 (수치형 벡터)
	formula 
		수치형 벡터(종속변수) ~ 집단분류(독립변수)
		데이터프레임을 t.test함수에 적용시킬 때 사용  
	data : t-검정을 수행할 데이터명  
	alternative : 양측검정시 "two.sided", 단측검정시 "less", "greater" 입력  
	equal : 등분산성을 만족하는지의 여부 (TRUE or FALSE)  
"""  
```



# 교차분석  

https://colab.research.google.com/drive/1PIZjm7zJ-CnXSKfzYah7ZZCEHllTFbXS?usp=sharing

## 적합성 검정  

```R
chisq.test(x, y, p)  

"""
options  
	x : 검정하고자 하는 데이터가 저장된 숫자 벡터 혹은 행렬  
	y : 검정하고자 하는 데이터가 저장된 숫자 벡터 혹은 행렬 (x가 행렬일 경우 y인자는 무시된다.)
	p : 귀무가설을 통해 설정한 확률 값을 지정  
"""
```

## 독립성 검정  

```R
# 인자로는 두 변수에 대한 분할표가 들어감
chisq.test(x, y)

# 분할표를 생성하기 위해선 xtabs와 table 함수를 이용함  
xtabs(formula, data)
"""
options  
	formula : 분할표를 만들고자 하는 변수를 `n ~ a1 + a2 + a3`와 같은 형태로 지정  
		n - 빈도를 나타내는 변수(없다면 생략 가능)
		a1 ~ a3 : 분할표에서 범주를 나타내는 변수  
	data : 포뮬러를 적용시킬 데이터  
"""

# 위 함수는 결국 결과값은 같음 

table(범주형 변수) # 도수분포표 생성  
table(범주형 변수1, 범주형 변수2) # 두 변수 간 이원분할표 생성  
```

# ANOVA 분산분석  

## one-way ANOVA

```R
aov(formula, data)  

# 그룹을 구분하는 기준이 되는 변수는 반드시 팩터형이어야 한다.  
"""
options  
	formula : 반응변수 ~ 그룹변수  
	data : 분석하고자 하는 데이터 명  
"""  

# ANOVA분석 결과로 귀무가설이 기각되었을 경우, 어떠한 집단들 사이에서 통계적으로 유의한 차이가 있는지를 알아보기 위해 수행하는 사후분석에는 다양한 방법이 있다. 그 중 Turkey의 HSD 검정법을 수행할 수 있는 R의 TukeyHSD 함수 문법은 아래와 같다.  

TukeyHSD(x, conf.level = 0.95, ...)  
"""
options
	x : 분산분석의 결과  
	conf.level : 신뢰수준에 해당하며, 기본값은 0.95임  
"""
```

## two-way ANOVA  

```R
# 그룹을 구분하는 기준이 되는 변수는 반드시 팩터형이어야 한다  
aov(formula, data)  
"""
options  
	formula : 반응변수 ~ 그룹변수1 * 그룹변수2  
	data : 분석하고자 하는 데이터명  

	<formula 표현식>  
	: R의 aov, lm 등의 함수 내에서 사용되는 formula는 생성할 분석모형의 형태를 지정하기 위한 인자이다.  
	: formula에 지정하는 인자값의 기본 형태는 `종속변수 ~ 독립변수` 이다.  

	+ : 독립변수가 여러 개인 경우 +를 사용하여 연결 
	ex) 종속변수 ~ 독립변수1 + 독립변수2 + 독립변수3 

	. : 종속변수로 지정한 변수를 제외한 나머지 모든 변수를 독립변수로 지정
	ex) y ~ . : 종속변수는 y, 독립변수는 y를 제외한 나머지 모든 변수  

	- : 선택한 독립변수들 중 제외하고자 하는 변수 앞에 - 기호를 입력하여 삭제  
	ex) 종속변수 y~. -x3 : 종속변수는 y, 독립변수는 x3를 제외한 나머지 모든 변수  

	:  : 두 변수간 상호작용함을 만들 때 사용  
	ex) 종속변수 ~ 독립변수1:독립변수2  

  	* : 기호 앞 뒤에 있는 변수를 각각 모형의 독립변수로 사용할 뿐만 아니라 두 변수의 조합인 상호작용 항도 모형에 포함시킬 때 사용  
	ex) "종속변수 ~ 독립변수1*독립변수2" = "종속변수 ~ 독립변수1 + 독립변수2 + 독립변수1:독립변수2"
"""
```

# 상관분석

```R
# 두 데이터 간 상관계수를 산출하기 위해서 사용  
cor(x, y, method=c("pearson", "kendall", "spearman"), use)  
"""
x : 연속형 자료 (벡터, 행렬, 데이터프레임)
y : 연속형 자료 (벡터, 행렬, 데이터프레임, NULL)  
method 
	- 상관계수를 계산할 유형을 지정  
	- default : "pearson"
	- etc : "kendall", "spearman"
use  
	- na값 처리 방법  
	"everything" : 결측값 존재 시 NA 출력  
	"all.obs" : 결측값 존재 시 오류 메시지 출력  
	"complete.obs" : 변수별로 결측값을 제외하고 상관계수 계산  
	"pairwise.complete.obs" : 모든 변수 쌍에서 결측값이 없는 데이터들에 대해 상관계수 계산  
"""  

# 산출한 상관계수에 대한 가설 검정을 수행할 때는 cor.test 사용  
cor.test(x, y, alternative=c("two.sided", "less", "greater"), 
        method = c("pearson", "kendall", "spearman"))  


# 상관계수 행렬을 시각화하기 위해 pairs 함수와 corrplot 패키지의 corrplot 함수를 사용 가능, corrplot 함수는 변수 간 상관계수를 다양한 모양과 색깔의 도형을 시각화해줌  
pairs(x, labels, ...)
"""
x : 시각화 할 행렬  
labels : 그래프의 제목  
"""

corrplot(corr, method, ...)  
"""
corr : 시각화 할 상관행렬  
method : 데이터를 표현할 형태 지정
"""
```



# plyr  

```R
# 시험 사용 가능
# 이 패키지의 함수들은 데이터를 분할 한 뒤 원하는 방향으로 특정 함수를 적용하고, 그 결과를 재조합하여 반환해줌  
# 여러 함수로 처리해야 할 데이터의 분할, 함수 적용, 재조합을 한 번에 처리할 수 있기 때문에 매우 효율적이고 편리한 패키지  

# ply 패키지의 함수들의 대부분은 '**ply' 형태로 이루어져 있으며, 첫 번째 글자는 입력 데이터의 형태를 의미하고 두 번째 글자는 출력 데이터의 형태를 의미한다. 
"""
a : array(배열)
l : list(리스트)
d : data frame(데이터프레임)
_ : 아무런 출력을 하지 않음 (두 번째 자리인 출력 데이터타입 형태로만 지정 가능)
첫 글자 r : 지정한 표현식을 반복하는 경우에 사용  
첫 글자 m : 열별로 다중 인수 함수를 적용하여 결과를 반환할 때 사용  
"""    
```

## adply  

```R
# adply는 배열을 입력 받아 함수를 적용한 후 데이터 프레임으로 반환해줌
# 반드시 배열이 아니더라도 행렬과 같이 숫자 인덱스로 다룰 수 있는 데이터형(행렬, 데이터프레임)은 입력 데이터로 사용 가능  
# adply는 apply와 다르게 결과 데이터를 데이터 프레임 형태로 반환하기 때문에 데이터 타입이 자동으로 바뀌는 문제가 발생하지 않음 

adply(data, margins, fun)  
"""
options  
	data : 입력 데이터 (행렬, 배열, 데이터 프레임)
	margins : 함수를 적용할 방향 지정 
		- margins=1 : 행 방향
		- margins=2 : 열 방향
		- margins=c(1,2) : 행과 열 방향 모두
	fun : margin에 지정한 방향으로 적용할 함수  
"""

# R의 iris 데이터에서 Petal.Length 변수가 1.5 미만이면서 
# Species 변수 값이 'setosa'인 조건을 만족하는 경우 '1', 그렇지 않은 경우 '0'을 부여한 칼럼을 생성하여, 원래의 iris 데이터와 함께 데이터프레임 형태로 출력해보자.  
> adply(iris, 1,
+ function(row){ifelse(row$Petal.Length<1.5 & row$Species=="setosa", "1", "0")})
    Sepal.Length Sepal.Width Petal.Length Petal.Width    Species V1
1            5.1         3.5          1.4         0.2     setosa  1
2            4.9         3.0          1.4         0.2     setosa  1
3            4.7         3.2          1.3         0.2     setosa  1
4            4.6         3.1          1.5         0.2     setosa  0
5            5.0         3.6          1.4         0.2     setosa  1
```

## ddply  

```R
# ddply는 데이터프레임을 입력 받아 함수를 적용한 뒤 다시 데이터프레임으로 결과 반환함 
# adply는 데이터의 행 혹은 열 방향으로 함수를 적용하지만, ddply는 .variables 인자에 지정한 변수들로 데이터를 그룹화한 후 그룹별로 함수를 적용하고, 결과 값을 반환한다.  
ddply(data, .variables, ddply-func, fun)
"""
options 
	data : 입력 데이터  
	.variables : 데이터를 그룹화 할 기준이 되는 변수들을 입력  
	ddply-func : ddply 내부 함수
	fun : .variables에 지정한 변수들의 값이 같은 데이터별로 적용할 함수  
"""



# R의 iris 데이터에서 Species 별로 나머지 네 개 변수 
# Q1 (Sepal.Length, Sepal.Width, Petal.Length, Petal.Width)의 평균을 출력해보자.  

data(iris)
library(plyr)
ddply(iris, .(Species), function(sub){
    data.frame(
    	mean_SL=mean(sub$Sepal.Length), mean_SW=mean(sub$Sepal.Width),
        mean_PL=mean(sub$Petal.Length), mean_PW=mean(sub$Petal.Width)
    )
})

     Species mean_SL mean_SW mean_PL mean_PW
1     setosa   5.006   3.428   1.462   0.246
2 versicolor   5.936   2.770   4.260   1.326
3  virginica   6.588   2.974   5.552   2.026


# Q2 R의 iris 데이터에서 Species와 Petal.Length가 1.5 미만인지의 여부로 데이터를 그룹지어 네 개 변수 (Sepal.Length, Sepal.Width, Petal.Length, Petal.Width)의 평균을 출력해보자.  

ddply(iris, .(Species, Petal.Length<1.5), function(sub){
    data.frame(
    	mean_SL=mean(sub$Sepal.Length), mean_SW=mean(sub$Sepal.Width),
        mean_PL=mean(sub$Petal.Length), mean_PW=mean(sub$Petal.Width)    	
    )
})

     Species Petal.Length < 1.5  mean_SL  mean_SW  mean_PL   mean_PW
1     setosa              FALSE 5.107692 3.515385 1.588462 0.2730769
2     setosa               TRUE 4.895833 3.333333 1.325000 0.2166667
3 versicolor              FALSE 5.936000 2.770000 4.260000 1.3260000
4  virginica              FALSE 6.588000 2.974000 5.552000 2.0260000


```

### ddply-func  

```R
위에서 살펴본 ddply의 사용 예는 ddply함수 내부에 임의의 사용자 정의 함수를 기입하여 연산을 수행했다. 하지만 ddply에서는 매번 사용자 정의 함수를 만들지 않고도 자주 쓰는 유용한 기능들을 편리하게 사용할 수 있도록 내부 함수들을 제공한다.  
```

#### transform  

```R
# 원본 데이터에 새로운 연산 결과를 담은 칼럼을 추가하여 함께 출력
ddply(data, .variables, transform, 새로운 칼럼명=값 정의)

# plyr 패키지의 내장데이터 baseball은 1871년부터 2007년까지 총 1228명의 미국 야구선수들의 타격에 대한 정보가 저장된 데이터이다. 각 선수는 id 컬럼으로 구분되어 있으며, 데이터는 총 22개의 변수와 21699개의 행으로 이루어져 있다. baseball 데이터로 ddply 내부 함수들에 대한 실습을 진행해보자.  

# 'g' 칼럼은 각 선수가 해당 년도에 출전한 게임 수를 나타낸다. 원본 데이터에 각 선수의 연평균 출전횟수를 나타내는 'avgG' 칼럼을 추가해보자. 이 문제를 해결하기 위해 먼저 제이터를 id 기준으로 그룹화한 뒤, 각 선수의 출전횟수 총함 (sum(g))을 경기에 출전한 연도 수로 나누어준다.  
ddply(baseball, .(id), transform, avgG=sum(g)/length(year))
```

#### mutate  

```R
mutate는 transform을 개선시킨 함수로, 원본 데이터에 새로운 연산 결과를 담은 칼럼을 추가할 수 있을 뿐만 아니라, 같은 코드 내에서 앞서 추가한 컬럼을 뒤에 추가하는 칼럼에서 바로 참조할 수 있다.

즉 칼럼 1 생성,
칼럼 2 생성이 아니라

칼럼 1 생성 (칼럼 1 바탕으로 칼럼 2 생성) 원라인이 가능  

# transform 예제에서와 마찬가지로 'avgG' 칼럼을 추가하는데, 이번에는 mutate 함수를 이용해보자. 또한 새로 생성한 'avgG' 칼럼 값을 반올림한 'avgG_RND' 칼럼도 함께 생성하자.
ddply(baseball, .(id), mutate, avgG=sum(g)/length(year), avgG_RND=round(avgG))
```

#### summarise  

```R
summarise는 데이터의 요약 정보를 만들어주는 함수이다. transform과 mutate는 기존 데이터에 새로운 칼럼을 추가한 데이터 프레임을 생성해주지만, summarize 함수는 **지정한 계산 결과만 담은** 데이터프레임을 생성한다.  

# 선수별로 1871~2007년 사이 기간 동안 출전한 경기 중 가장 마지막에 출전한 경기의 연도 수를 구해 'year_fin' 변수에 저장하고, 관련 정보들만 뽑아서 요약해보자. 이를 위해 먼저 데이터를 id로 그룹화한 뒤, year변수의 최댓값을 계산하여 'year_fin' 변수에 부여한다.  
ddply(baseball, .(id), summarise, yaer_fin=max(year))
            id yaer_fin
1    aaronha01     1976
2    abernte02     1972
3    adairje01     1970
4    adamsba01     1926
5    adamsbo03     1959

# baseball 데이터의 team 변수는 선수의 소속팀을 의미하고, hr은 홈런의 수를 의미한다. ddply의 summarise를 활용해 팀별 홈런 수의 합을 구하고, hr_sum 변수에 출력해보자.  
ddply(baseball, .(team), summarise, hr_sum=sum(hr))
    team hr_sum
1    ALT      0
2    ANA    134
3    ARI    809
4    ATL   3272
5    BAL   4243
```

#### subset

```R
# subset은 데이터의 그룹별로 조건을 만족하는 행들만 출력해준다. 또한 select 인자를 사용해 원하는 칼럼만 지정하여 출력할 수도 있다.  
ddply(data, variables, subset, 조건, select=c(출력할 변수, 변수2, ... 변수n))

# subset을 이용하여 선수별로 마지막 경기 출전년도에 해당하는 행들의 일부 열(id, year, stint, team, lg, g)들만 추출해보자. 아래의 R 코드는 먼저 id로 데이터를 그룹화한 뒤, year값이 선수별 year변수의 최댓값과 같은 행만 subset으로 추출하는 방법이다.  
ddply(baseball, .(id), subset, year==max(year), select=c("id", "year", "stint", "team", "lg", "g"))
            id year  stint team lg  g
1    aaronha01 1976     1  ML4 AL  85
2    abernte02 1972     1  KCA AL  45
3    adairje01 1970     1  KCA AL   7
4    adamsba01 1926     1  PIT NL  19
5    adamsbo03 1959     1  CHN NL   3
```

# dplyr  

```R
dplyr 패키지는 R에서 데이터 전처리를 할 때 가장 많이 사용되는 패키지중 하나이다. 데이터의 일부 추출, 새로운 변수 생성, 다른 데이터와 병합 등의 다양한 기능을 지원한다.  

dplyr에서 많이 사용되는 주요 함수들은 %>% 기호로 연결하여 중첩사용이 가능하다.  
```

## filter

```R
# filter 함수는 데이터에서 조건에 맞는 행들을 추출해주며, 사용방법은 아래와 같다.  
데이터프레임 이름 %>% filter(조건)

# MASS 패키지에서 제공하는 Cars93 데이터는 1993년 미국에서 판매된 93대의 자동차에 대한 정보를 담고 있으며, 27개의 변수로 이루어져 있다. Cars93 데이터에서 제조사가 "Audi" 혹은 "BMW" 이면서, 엔진크기가 2.4 이상인 행들만 추출해보자.  
Cars93 %>% filter((Manufacturer=="Audi" | Manufacturer=="BMW") & EngineSize>=2.4)
```

## select  

```R
# select 함수는 데이터에서 특정 열만을 추출해주며, 사용방법은 아래와 같다.  
데이터프레임 이름 %>% select(선택할 변수명, ~제외할 변수명)

# Cars93 데이터의 모델번호, 종류, 가격 변수들만 추출해보자.  
# 사용할 select 함수가 dplyr의 함수임을 명시해주기
Cars93 %>% dplyr::select(Model, Type, Price)

# 제조사가 Chevolet 혹은 Volkswagen 이면서, 가격이 10이상인 행 들의 제조사, 모델, 종류, 가격 변수들만 추출해보자.  
Cars93 %>%
filter((Manufacturer=="Chevrolet" | Manufacturer=="Volkswagen") & Price>=10)%>%
dplyr::select(Manufacturer, Model, Type, Price)
```

## group_by 와 summarise  

```R
# group_by는 지정한 변수들을 기준으로 데이터를 그룹화하는 함수이며, summarise 는 통계치를 계산해주는 함수로 두 함수는 같이 사용되는 경우가 많다. 
데이터프레임이름 %>% group_by(그룹화 할 기준 변수1, 기준 변수2, ... 기준 변수n)
%>% summarise(새로운 변수명=계산식)  

"""
options (summarise 함수 내부)
	mean : 평균 산출  
	median : 중앙값 산출  
	sd : 표준편차 산출  
	min / max : 최솟값 / 최댓값 산출  
	sum : 함계 산출
	n : 행의 개수 세기  
"""

# Cars93 데이터의 제조사별 가격의 평균가 무게의 최댓값을 산출한 뒤 변수명을 각각 mean_Price, max_Weight로 지정하여 출력해보자.  
# ddply(baseball, .(id), summarise, yaer_fin=max(year))와 같음
Cars93 %>% group_by(Manufacturer) %>%
summarise(mean_Price=mean(Price), max_Weight=max(Weight))

# 종류와 에어백을 기준으로 데이터를 그룹화한 뒤, 자동차 평균 무게를 구해보자.  
Cars93 %>% group_by(Type, AirBags) %>% summarise(mean_Weight=mean(Weight))
```

## mutate  

```R
# mutate는 데이터에 새로운 파생변수를 추가해주는 함수이며, 사용법은 아래와 같다.  
데이터프레임 이름 %>% mutate(새로운 변수명 = 값)  

# Cars93 데이터에서 가격(Price 변수, 1000달러 기준)이 12미만이면 "low", 12이상 23미만이면 "middle", 23이상이면 "high" 값을 가지는 Pr_level 변수를 생성한 뒤, 모델, 가격, 새로운 파생변수 Pr_level만 출력해보자.  
Cars93 %>% mutate(Pr_level=ifelse(Price < 12, "low",
                                 ifelse(Price >= 12 & Price <23, "middle", "high"))) %>%
dplyr::select(Model, Price, Pr_level)
            Model Price Pr_level
1         Integra  15.9   middle
2          Legend  33.9     high
3              90  29.1     high
4             100  37.7     high
5            535i  30.0     high
```

## arange  

```R
# arrange는 특정 열 기준으로 데이터를 정렬해주는 함수이며, 사용법은 아래와 같다.  
데이터프레임 이름 %>% arrange(정렬 기준변수) # 오름차순 정렬 
데이터프레임 이름 %>% arrange(desc(정렬 기준변수)) # 내림차순 정렬  

# Cars93 데이터에서 종류가 "Midsize" 혹은 "Small"인 데이터의 Model, Type, Weight, Price 변수들만 추출한 뒤, 종류(Type) 별로 Weight 변수값들이 Weight의 중앙값보다 작은 경우는 "low", 중앙값 이상인 경우 "high" 값을 갖는 Weight_lv 변수를 생성하라. 그리고, Price 변수를 기준으로 데이터를 오름차순 정렬하여 출력하여라.  
Cars93 %>% 
filter(Type %in% c("Midsize", "Small")) %>% 
dplyr::select(Model, Type, Weight, Price) %>% 
group_by(Type) %>% 
mutate(Weight_lv=ifelse(Weight<median(Weight), "low", "high")) %>%  
arrange(Price)

   Model   Type  Weight Price Weight_lv
   <fct>   <fct>  <int> <dbl> <chr>    
 1 Festiva Small   1845   7.4 low      
 2 Excel   Small   2345   8   high     
 3 323     Small   2325   8.3 low      
 4 Metro   Small   1695   8.4 low      
 5 Justy   Small   2045   8.4 low 
```

## {left, right, inner, full}_join  

```R
# join이란 두 개 이상의 테이블을 특정 변수를 기준으로 결합하는 것을 의미한다.  
# R 기본 함수인 merge와 같은 역할을 한다.  
ADP 실기 책 100쪽 그림 참고

# 카페에서 판매하는 메뉴_코드(code), 이름(name)을 담은 데이터 "NAME" 과 메뉴 코드, 해당 메뉴의 가격을 담은 데이터 "PRICE"를 생성해보자. 그 후 각 메뉴의 고유코드를 의미하는 code 변수를 기준으로 left_join, right_join, inner_join, full_join을 수행하여 결과를 확인해보자.  
NAME<-data.frame(code=c("A01", "A02", "A03"),
                name=c("coffee", "cake", "cookie"))
NAME
  code   name
1  A01 coffee
2  A02   cake
3  A03 cookie

PRICE<-data.frame(code=c("A01", "A02", "A04"),
                 price=c(3000, 4000, 3000))
PRICE
  code price
1  A01  3000
2  A02  4000
3  A04  3000

# left_join, 나머지 병합도 이름만 바꿔주면 된다.  
cafe_lift <- left_join(NAME, PRICE, by="code")
```

## bind_rows 와 bind_cols  

```R
# bind_rows는 데이터의 행들을 이어 붙여 결합하는 함수이며, R의 기본 함수 rbind와 같은 역할을 한다. 하지만 rbind는 열 이름이 다르면 제대로 데이터가 결합되지 않는 반면, bind_rows는 이름이 다르더라도 빈자리는 NA값으로 채워지면서 데이터가 결합된다.  
# 또한 bind_rows 함수 내 id 인자를 사용할 경우, 각 행이 결합 당시 몇 번째 데이터 원천으로부터 온 것인지를 확인할 수 있으며 연산속도도 rbind에 비해 매우 빠르다.  

# 위 예제에서 생성한 NAME 데이터와 PRICE 데이터를 {base} 패키지의 rbind 함수와 [dplyr] 패키지의 bind_rows 함수를 이용해 행 기준으로 결합해보고 그 결과를 확인해보자.  # base::rbind 함수를 이용해 데이터 결합  
rbind(NAME, PRICE) # 에러 발생  

# dplyr::bind_rows 함수를 이용해 데이터 결합 
bind_rows(NAME, PRICE)
  code   name price
1  A01 coffee    NA
2  A02   cake    NA
3  A03 cookie    NA
4  A01   <NA>  3000
5  A02   <NA>  4000
6  A04   <NA>  3000

# 카페에서 판매되는 메뉴의 고유코드와 이름을 담음 데이터 A, B, C를 생성하고 세 개의 데이터를 행으로 결합해보자. 또한 각 행이 어떤 데이터로부터 결합된 것인지를 나타내는 id열도 함께 나타내보자.  
A<-data.frame(code=c(1,2), name=c("coffee", "cake"))
B<-data.frame(code=c(3,4), name=c("cookie", "juice"))
C<-data.frame(code=5, name="bread")

cafe_bind<-bind_rows(A,B,C, .id="id")
cafe_bind
  id code   name
1  1    1 coffee
2  1    2   cake
3  2    3 cookie
4  2    4  juice
5  3    5  bread

# id열을 통해 1, 2 행의 원천은 첫 번째 데이터, 3, 4행의 원천은 두 번째 데이터,
# 5행의 원천은 세 번째 데이터임을 알 수 잇음 

# bind_cols 함수는 bind_rows 함수와 다르게 cbind 함수와 마찬가지로 결합할 데이터들의 행 개수가 동일해야 하며, 그렇지 않을 경우 에러가 발생한다.  

```

# reshape2  

## melt  

```R
# melt 함수는 여러 변수로 이루어진 데이터를 id, vriables, value의 세 칼럼으로만 이루어진 데이터로 변환해준다. 즉 기존의 변수 명이 variables의 값이 되어 행으로 존재하며, 각 측정변수에 대한 값은 value에 저장된다. 

# melt 함수를 사용해 변환된 데이터를 이용하면 variable 별 value의 통계값을 매우 편리하게 사용할 수 있다.  

# emlt 함수는 데이터프레임, 배열, 리스트에 적용할 수 있다. 가장 많이 사용되는 데이터 타입인 데이터프레임에 적용할 때의 melt 함수 사용 및 활용법은 아래와 같다.  

melt(data, id.vars, measure.vars, na.rm=FALSE)  

"""
options  
  data : melt 함수를 적용할 데이터 프레임  
  id.vars : 데이터를 변형할 때 기준이 되는 식별자 컬람들  
  measure.vars : 식별자가 아닌 측정치 칼럼들  
			    (지정하지 않을 경우, 
					id.vars에 지정하지 않은 모든 칼럼이 measure.vars로 사용됨)
  na.rm : NA 값이 포함된 행을 삭제할지의 여부 (na.rm=FALSE이면, 
			NA가 포홤된 행을 제거하지 않음)
"""

# R의 airquality는 1973년 5월 ~ 9월 동안 뉴욕의 일일 대기 질 측정량에 대한 데이터로, 153개의 행과 6개의 변수로 이루어져 있다. 6개의 변수 중 Month와 Day를 식별자로 두고, 나머지 변수와 변수 값은 모든 데이터 내에 포함되는 형태로 변화해보자.  
install.packages("reshape2")
library("reshape2")

> head(airquality, 5)
  Ozone Solar.R Wind Temp Month Day
1    41     190  7.4   67     5   1
2    36     118  8.0   72     5   2
3    12     149 12.6   74     5   3
4    18     313 11.5   62     5   4
5    NA      NA 14.3   56     5   5
> head(melt(airquality, id.vars=c("Month", "Day"), na.rm=T), 5)
  Month Day variable value
1     5   1    Ozone    41
2     5   2    Ozone    36
3     5   3    Ozone    12
4     5   4    Ozone    18
6     5   6    Ozone    28
```

## dcast  

```R
cast 함수는 melt 함수로 녹여진 형태의 데이털르 다시 여러 칼럼을 가진 형태로 변환해주는 함수이다. 반환하는 데이터 형태가 데이터 프레임일 경우는 dcast 함수를 사용하고 반환할 데이터의 형태가 벡터/행렬/배열일 경우 acast를 사용할 수 있다. 본 내용에서는 dcast 함수에 대해 알아본다. 

dcast 함수를 사용하면 melt 함수가 적용된 형태의 데이터를 다시 melt 함수 적용 이전의 데이터 형태로 변환할 수도 있고, 앞서 배운 ddply 함수와 같이 식별자별 특정 변수의 측정치들에 대한 통계량을 계산할 수도 있다. 구체적인 활용법은 예제를 통해 함께 살펴보자.  

dcast(data, formula, fun.aggregate=NULL)  
"""
options  
  data : melt 함수가 적용된 형태의 데이터 프레임  
  formula : 데이터를 변환할 포뮬러 지정  
	"id 변수 ~ variable 변수" 형태로 입력  
	"~앞뒤로 여러 개의 변수를 나열할 경우 + 기호로 각 변수를 연결"
	명시적으로 나열되지 않은 모든 변수를 표현할 경우에는 ...을 사용
	아무런 변수도 지정하지 않을 경우에는 .을 사용  
fun.aggregate : id 변수를 기준으로 여러 행이 존재할 경우 해당 행들에 적용할 집합함수
"""
air_melt<-melt(airquality, id.vars=c("Month", "Day"), na.rm=T)
air_dcast<-dcast(air_melt, Month + Day ~ ...)
```

# data.table  

```R
data.table 패키지는 연산속도가 매우 빨라 크기가 큰 데이터를 처리하거나 탐색하는데 유용하며, 그만큼 자주 사용되는 패키지이다. 데이터 테이블을 데이터 프레임과 동일하게 취급되므로 데이터 프레임에 적용할 수 있는 함수들을 데이터 테이블에 적용할 수도 있다.  
```

## 데이터 테이블 생성  

```R
데이터 테이블의 클래스는 데이터 프레임을 포함하고 있으므로 데이터 테이블은 데이터 프레임으로 변환해서 사용이 가능하다. 데이터 테이블은 데이터 프레임을 생성하는 것과 비슷한 문법으로 만들어낼 수 있으며, 관련 함수들은 아래와 같다.  

# tag(변수명) = value(값)의 형태로 데이터 생성  
data.table(tag =value, ...)

# 데이터 테이블로 변환하고자 하는 데이터를 인자로 입력  
as.data.frame(데이터프레임)

# 모든 데이터 테이블 객체의 목록을 반환  
tables()

# 숫자 1, 2, 3이 저장된 x 변수와 문자 "가", "나", "다" 가 저장된 y 변수로 이루어진 데이터 테이블을 생성한 뒤, 데이터 타입을 확인해보자.  
install.packages("data.table")
library(data.table)

> mydata<-data.table(x=c(1:3), y=c("가", "나", "다"))
> mydata
   x  y
1: 1 가
2: 2 나
3: 3 다

> class(mydata)
[1] "data.table" "data.frame"

# 데이터 프레임 형태인 iris를 데이터 테이블로 변환한 후 클래스를 확인해보자.  
class(iris)
[1] "data.frame"

iris_dt<-as.data.table(iris)
class(iris_dt)
[1] "data.table" "data.frame"

# 모든 데이터 테이블 확인
tables()
      NAME NROW NCOL MB                                                      COLS KEY
1: iris_dt  150    5  0 Sepal.Length,Sepal.Width,Petal.Length,Petal.Width,Species    
2:  mydata    3    2  0                                                       x,y    
Total: 0MB
```

## 데이터 접근  

```R
# 데이터 테이블 내의 데이터는 []를 사용해서 간편하게 다룰 수 있으며, []를 사용하는 데이터프레임 접근법과는 차이가 있다. 아래와 같이 데이터테이블[행, 열, 그룹화 조건]의 문법을 사용해 데이터에 접근하며, 각 인자에 대한 구체적인 설명은 아래와 같다.  

데이터테이블[행, 열, by="그룹화 기준 변수"]  

"""
<행>
[]내 첫 번째 자리에는 행 번호 혹은 선택할 행에 대한 조건식을 지정한다. 
"""
# iris_dt의 1행 출력 
iris_dt[1, ]

# iris_dt의 1~5행 출력
iris_dt[c(1:5), ]

# Species 변수 값이 setosa인 행들만 출력  
iris_dt[iris_dt$Species=="setosa", ]

"""
<열>
[] 내의 두 번째 자리에는 칼럼명, 칼럼 번호 혹은 칼럼명을 사용한 연산식을 지정할 수 있으며 각각에 대한 설명과 예시는 아래와 같다.  
"""

# 1~3 행의 Petal.Length (세번째 열) 만 출력  
1) iris_dt[1:3, .(Petal.Length)]
2) iris_dt[1:3, 3]

# Sepal.Width, Petal.Width 열만 출력  
1) iris_dt[, list(Sepal.Width, Petal.Width)]
2) iris_dt[, .(Sepal.Width, Petal.Width)]

# Sepal.Length 값 평균을 출력  
iris_dt[, mean(Sepal.Length)]

# Species 별 Petal.Length의 평균 출력 (Species 변수로 데이터를 그룹화)
iris_df[, mean(Petal.Length), by=Species]

# Petal.Length 값이 1이상인 행들을 Species 로 그룹화한 뒤, 
# Sepal.Length와 Sepal.Width의 평균을 각각 mean.SL 과 mean.SW를 변수명으로 출력  
iris_dt[Petal.Length>=1, 
        .(mean.SL=mean(Sepal.Length), mena.SW=mean(Sepal.Width)), 
       							by = Species]
```

## 새로운 변수 생성  

```r 
# 데이터테이블에 새로운 변수를 생성할 때는 아래에 제시된 문법과 같이 ':='라는 기호를 사용한다.  

# 하나의 변수 추가  
데이터테이블[행, 새로운칼럼명:= 값, by = '그룹화 기준 변수']

# 여러 개의 변수 추가  
데이터테이블[행, c("칼럼명1", ..., "칼럼명n") := list(값1, ... , 값n),
      					by="그룹화 기준 변수"]

"""
'=' : 해당 연산식이 수행된 데이터만 조회  
':=' : 새로운 변수가 즉시 데이터에 추가됨
"""  
air<-as.data.table(airquality)
air[, Wind_class:=ifelse(Wind>=mean(Wind), "U", "D")]
```

## 데이터 정렬  

```R
# 데이터 테이블을 특정 변수 기준으로 정렬하고자 할 때는 아래와 같이 대괄호 []를 한 번 더 사용하여 해결이 가능하다.  

데이터테이블[행, 열, by = "그룹화 기준 변수"][order(칼럼명, decreasing=FALSE)]

# season별 Ozone 과 SOlar.R 변수들의 평균 산출 및 정렬 
air[, .(Ozone_mean=mean(Ozone, na.rm=T), Solar.R_mean=mean(Solar.R, na.rm=T)),
   by=.(season)][order(Ozone_mean, decreasing=T)]  
```

## key를 활용하여 데이터 다루기  

```R
데이터프레임에서는 특정 조건을 만족하는 행을 찾을 때 모든 행을 하나씩 검사하는 방식을 사용한다. 하지만 데이터 테이블에서는 색인을 지정한 후, 색인을 통해 각 행에 접근하는 방식을 사용하므로 데이터의 양과 검색 횟수가 많을 경우 매우 빠른 속도로 동작할 수 있다.  

"""
R의 내장 데이터 baseball을 데이터 테이블 형태로 변환한 뒤, year 변수를 key로 지정해보자.  그 후, 데이터테이블[J(제약조건), 열, by=] 코드를 활용하여 year 변수가 1960년에 해당하는 데이터를 조회하고, 1960년대 데이터들의 팀 (team변수) 별 경기 출전횟수(g 변수)의 평균을 구해보자.  
""" 
# baseball 데이터를 데이터 테이블로 변환
baseball<-as.data.table(baseball)

# year 변수를 key로 지정 
setkey(baseball, year)

# 1960년대 조회  
baseball[J(1960)]

# 1960년대 경기 정보 중 티멸 출전횟수의 평균 산출 
# 팀별 출전횟수의 평균을 저장할 변수 이름을 지정할 경우에는 'list(변수명 = 값)' 코드 활용
baseball[J(1960), list(gmean=mean(g)), by=team]
```

