문서정보 : 2022.10.17.~ 작성, 작성자 [@SAgiKPJH](https://github.com/SAgiKPJH)

<br>

### R을 이용한 기초통계학

R을 활용한 기초통계학에 대해서 배운다.

### 목표

- [ ] 1. R 입문
- [ ] 2. R Studio
- [ ] 3. 자료형과 연산자
- [ ] 4. 변수
- [ ] 5. 자료구조
- [ ] 6. 자료의 입출력
- [ ] 7. 함수
- [ ] 8. 조건문과 반복문

### 제작자
[@SAgiKPJH](https://github.com/SAgiKPJH)

### 참조

- [참조링크](참조링크)


---
<br><br><br>


#  1. R 입문

### 1. R언어의 역사

- S-언어(R의 원조): 1976년 AT&T Bell Lab에서 개발한 **통계 분석 프로그래밍 언어**
  - ‘S’라는 이름은 Statistical computing의 머리글; C-언어와 연관성 강조를 위함
- R-언어는 1993년 오클랜드대학에서 Ross Inaka와 Robert Gentleman이 개발
  - 두 개발자의 머리글자에서 따서 ‘R’이라 정함
- 1995년 자유 소프트웨어 재단의 허가로 인해 무료로 공개

<br>

### 2. R-언어의 특징

- 오픈소스 컴퓨팅 환경을 제공하는 R-언어는 **전산통계 및 빅데이터 분석 분야의 공용어**로 자리잡아가고 있다.
- 상용 소프트웨어 버금가는 상당한 수준의 그래픽 및 그림 기능 지원한다.
- 벡터, 행렬, 배열, 데이터프레임, 리스트 등 다양한 형태의 데이터 구조를 지원하여 데이터 처리 및 계산 능력이 우수하다.
- 사용자 스스로 개발하여 공유 가능한 패키지로 인해 확장성이 뛰어나다.
- 많은 장점에도 불구하고 빅데이터 분석 분야는 상당한 시간과 노력이 필요하다.

<br>

### 3. R-언어의 사용환경

- R-언어는 리눅스, 맥, 윈도우 시스템에서 **컴파일 및 실행**이 가능하고 서버용과 데스크탑용을 제공하고 있다.
- R-언어는 과학계산을 위한 훌륭한 오픈소스 언어로 우수한 성능과 편리한 소프트웨어 사용환경 덕분에 기업과 대학에서 널리 사용되고 있음
- R-언어의 단점은 R이 기본적으로 메모리에 전체 데이터셋을 로드해 사용하기 때문에 대규모 데이터셋을 다루기는 불편함


<br><br><br>


#  2. R Studio

## 2-1. R 설치

### 2-1-1. R 프로그램 다운로드

<img src="https://user-images.githubusercontent.com/66783849/196110408-2ac0d722-3871-4c80-a36b-bf3914d71d5a.png" width="350">

- [R 사이트](http://cran.r-project.org/) > ‘Download for Windows’ > ‘install R for the first time’ > ‘Download R 4.n.n for Windows’

<br>

### 2-1-2. R 설치

- (1) 설치 파일을 마우스 오른쪽 버턴을 눌러 ‘관리자 권한으로 실행’을 선택
- (2) 설치할 위치 선택 – C:\Program Files\R\R-4.0.2
- (3) 총 4개의 구성요소
  - Core Files (선택)
  - 32-bit Files (컴퓨터 사양에 따른 선택)
  - 64-bit Files (컴퓨터 사양에 따른 선택)
  - Message translation (선택)
- (4) 스타트 옵션 - No(기본값 사용)
- (5) 시작 메뉴 폴더 선택 – 기본적으로는 R임
- (6) 추가사항을 선택
  - 바탕화면에 아이콘생성
  - 레지스트리에 버전정보 저장
  - R을 .RData 파일들과 연결 
- (7) R의 설치가 끝나면 다음 과정으로 **Java JDK**를 설치해야 함

<br>

### 2-1-3. R의 설치완료 후 실행 및 구성

- (1) R의 실행 아이콘을 2번 클릭하여 [그림 A1.2]의 화면을 띄움
- (2) 화면의 주 메뉴 ‘패키지들’을 선택하고 이어 부메뉴 ‘CRAN 미러 설정...’을 선택하고 ‘(HTTP mirrors)’를 선택
- (3) 이후 ‘HTTPS CRAN mirrors’화면에서 ‘Korea (Seoul 1)’을 선택
- (4) ‘CRAN 미러 설정’ 단계가 끝나면 R 코드를 실행할 수 있음
  <img src="https://user-images.githubusercontent.com/66783849/196111898-d5a78c62-35aa-4ced-8344-9a08ff0a4ec2.png" width="350">
- R의 구성은 다음과 같다.
  - (1) 메뉴 바
    - R에서 사용할 수 있는 다양한 기본기능들이 나열되어 있음
  - (2) 단축 아이콘 툴 바
    - 자주 사용하는 기능들의 단축아이콘들이 나열됨
  - (3) R 콘솔
    - R명령어가 입력되고 결과가 출력되는 R의 핵심적인 작업공간
  - (4) 스크립트 창(R 편집기)
    - 파일 메뉴의 스크립트 부메뉴로 열수 있음

<br><br>

## 2-2. R Studio 설치

### 2-2-1. Rstudio 특징

- 위 R을 먼저 설치하고 RStudio를 설치해야 한다.
- RStudio는 R을 사용하는 통합개발환경(IDE; Integrated Development Envi-ronment)을 제공하여 사용자들이 보다 편리하게 접근가능함
- IDE를 사용하면 간편하고 확장된 기능 하에서 R을 실행할 수 있음
- RStudio의 단점은 **아주 큰 크기의 데이터셋을 로드할 때 어려울 수 있다**
- RStudio는 작업중인 데이터 객체(object)를 시각화하는데 좋은 도구임
- 데이터 분석에 필요한 전반적인 것을 한눈에 볼 수 있게 해줌

<br>

### 2-2-2. RStudio 설치, 사용법 및 구성

- R Studio를 다음과 같이 설치한다.
  - [RStudio 사이트](https://www.rstudio.com/) > Products > RStudio > RStudio Desktop > 다운로드
- R Studio는 다음과 같이 구성한다.  
  <img src="https://user-images.githubusercontent.com/66783849/196113148-cc3c4c36-fdc4-4475-a615-8571562fc6a6.png" width="350">
  - (1) : 스크립트 창
    - R에서 별도로 열 수 있는 R편집기 창과 동일한 역할
  - (2) : 환경 및 히스토리
    - R에서 볼 수 있는 R콘솔창과 동일함
  - (3) : R 콘솔
    - 환경과 작업 히스토리를 살표볼 수 있음
  - (4) : 그림 및 도움말
    - 저장 폴더, 그림, 패키지, 도움말, 뷰어 등 확인 영역

<br><br>

## 2-3. R 패키지 설치

-  R에서 어떤 작업을 수행하기 위해서는 해당 기능을 하는 패키지가 필요함
-  R을 설치할 때 함께 설치되는 기본 패키지가 있고 찾는 기능이 없는 경우
- 원하는 기능을 실행해 주는 패키지를 찾아서 추가로 설치해야함
- 패키지들은 [CRAN](http://cran.r-project.org) 사이트에서 모두 검색하여 알 수 있다.
  - (1) 사이트 왼쪽 Software - Packages
  - (2) 'Table of available packages, sorted by name'를 클릭하면 알파벳 이름순으로 패키지 목록을 확인할 수 있음

<br>

### 2-3-1. R에서 R 패키지 설치 및 사용

- 패키지를 추가로 설치하기 위해서는 필요한 패키지의 이름을 확인
- 명령어 install.packages(“패키지명”)과 library(패키지명)을 실행
  ```R
  install.packages("PackageName")
  library("packageName")
  ```
- 다수 패키지를 동시에 설치하려면 install.packages(c(“aaa”,“bbb”))를 실행
- 또는 CRAN(the Comprehensive R Archive Network) 미러 사이트가 설정이 완료되었다면 주메뉴 ‘패키지들’의 부메뉴 ‘패키지 불러오기’를 선택
- 선택화면에서 필요한 패키지를 지정하고 다운로드를 진행, 설치를 완료함
- 한번만 install.packages() 설치작업을 성공하면 이후 library()만 실행하면 됨

<br>

### 2-3-2. R Studio에서 R 패키지 설치

- RStudio를 이용하면 패키지 설치도 간편하게 진행할 수 있음
  - R 콘솔 창에서 직접 ‘install.packages(“패키지명”)’을 입력하고 library(패키지명)을 입력해도 가능함
- 우측 하단 인터페이스의 ‘Packages’ 탭를 글릭 => ‘Install’을 클릭 => (새로운 창에서) 패키지 이름을 입력

<br>

### 2-3-3. 패키지 업데이트 및 삭제

- 설치된 패키지를 업데이트하려면 update.packages(“패키지명”)을 사용
  ```R
  update.packages("PackageName")
  ```
- 패키지 명을 안 쓰면 모든 패키지의 업데이트 내역을 자동 확인해서 실행
- 어떤 패키지들이 설치되어 있는지 확인하려면 installed.packages()를 사용
  ```R
  installed.packages()
  ```
- 설치되어 있는 패키지를 삭제하려면 remove.packages(“패키지명”)을 사용
  ```R
  remove.packages(“PackageName”)
  ```
- 설치할 수 있는 패키지 확인을 위해서는 available.packages()를 사용
  ```R
  available.packages()
  ```
- R의 또 다른 장점은 다양한 **패키지 및 함수와 옵션에 대한 상세한 도움말을 제공**하는 점
- 해당 함수들에 대한 기본적인 설명과 각 인수들(arguments)에 대한 설명, 사용가능 옵션의 목록과 다양한 예제가 준비되어 있음


<br>

### 2-3-4. R의 작업 디렉토리

- 작업 디렉터리(working directory)라는 곳은 R로 작업을 할 때 필요한 데이터들을 미리 가져다 두는 약속된 디렉터리임
- 작업 디렉터리 지정: setwd(“디렉터리명”) 함수를 사용
- 함수 getwd()는 현재 작업디렉터리를 확인
  ```R
  # A1.2 R과 RStudio의 사용법 - A1.2.2 R 패키지 설치하기
  install.packages("패키지명") # R의 CRAN에서 내 PC으로 다운로드
  library(패키지명) # 이후 패키지를 나타내는 표현은 {패키지명}으로 사용함
  require(패키지명) # 위 library(패키지명) 명령과 동일함
  > ?par # 아래와 같은 기능, ‘#’ 이후는 주석을 의미함
  > help(par) # 위와 같은 기능
  ## 1.2.2 R 패키지 설치하기 - 4. R의 작업용 디렉터리
  > getwd() # 현재 설정되어 사용 중인 작업 디렉터리 출력
  > setwd("D:/Lecture/R확률통계") # 작업 디렉터리로 사용하고자하는 곳을 지정
  ```

### ⭐ 작업 디렉터리 지정을 위한 다른 방법

- 단순 지정방법인 ‘setwd(“디렉트리명”)’은 RStudio를 사용할 때마다 지정해야 하므로 번거로움
- 이 번거로움을 피하기 위해 아래와 같은 방법으로 RStudio 실행
- R(RStudio) 실행 아이콘을 마우스 우측버턴을 눌러 등록정보 창을 열고
  - ‘바로가기’ 메뉴의 ‘시작위치’ 란에 경로와 디렉터리이름을 삽입
  - (1) 먼저 작업하고자 하는 디렉터리("E:\\Lecture\\RNASrc") 생성
  - (2) RStudio 실행 아이콘을 (1)에서 생성한 디렉터리에 위치시킴
  - (3) RStudio 실행 아이콘을 마우스 우측버턴으로 눌러 메뉴 바의 ‘속성’을 선택
  - (4) 나타난 등록정보 창에서 ‘바로가기’ 메뉴의 ‘시작위치(S)’에
  - (5) 디렉터리명 ‘E:\\Lecture\\RNASrc’을 추가하고
  - (6) 창의 하단부에 있는 ‘적용(A)’과 ‘확인’ 버턴을 누름

<br><br>



<br><br><br>


#  3. 자료형과 연산자

## 3-1. R의 자료형

-  R의 자료형에는 숫자형(numeric), 정수형(integer), 문자형(character), 논리형 (logical), 복소수형(complex), 인수형(factor), NA형, NULL형, 날짜형 등
-  NA(Not Available)는 결측값이라고도 하며 정해진 범위 안에 있는 값이 아니어서 사용할 수 없는 경우를 의미함; 논리형(logical)으로 분류됨
-  인수형(factor)은 범주형 자료(예, 혈액형)를 다룰 때 문자형데이터를 저장하는 새로운 방식의 자료유형
-  NULL형은 값이 정해지지 않아서 얼마인지 모른다는 의미임

<br>

### 3-1-1. 숫자형과 산술연산자

- R에서 숫자는 정수와 실수로 구분(정수는 숫자 뒤 L추가, 예, 3L)
- 숫자 벡터를 생성하려면 c() 함수를 사용(예, x<-c(1,2,3,4,5))
- 실수형은 배정도 숫자로 소수점 또는 ‘e’를 사용하여 표현함
- R-언어에서 사용하는 산술연산자는 C-언어와 유사

산술연산자 | 의미 | 산술연산자 | 의미
-- | -- | -- | --
+x | 부호유지 | x/y | 요소들의   나누기
-x | 반대부호 | x^y, x**y | x의 y승
x+y | 요소들의   합 | x%%y | 정수   x/y의 나머지
x-y | 요소들의   차 | x%/%y | 정수   x/y의 몫
x*y | 요소들의   곱 | x%*%y | x와 y의 내적

  ```R
  # A1.3 자료형과 연산자 - A1.3.1 R의 자료형 – 1. 숫자형과 산술연산자
  > x <- c(1,2,3,4,5); x; class(x) # c()는 combine function이라는 의미임
  [1] 1 2 3 4 5
  [1] "numeric"

  > int_x <- c(1L,2L,3L,4L,5L); int_x; class(int_x) # 정수형은 숫자 뒤 L을 붙임
  [1] 1 2 3 4 5
  [1] "integer"
  
  > 3e2; 3e5; 3e-1; 3e-3; 3e-4
  [1] 300
  [1] 3e+05
  [1] 0.3
  [1] 0.003
  [1] 3e-04

  > y <- c(5,4,3,2,1); x+y; x^y # R에서 벡터의 연산은 요소별로 정의됨
  [1] 6 6 6 6 6
  [1]  1 16 27 16  5
  
  > 17%%3; 17%/%3
  [1] 2
  [1] 5
  ```

<br>

### 3-1-2. 문자형

- 문자를 처리할 때는 항상 쌍따옴표(") 또는 홑따옴표(')를 사용해야 함
- 데이터가 숫자형인지 문자형인지 알 수 없다면 class() 함수를 사용
  ```R
  # A1.3 자료형과 연산자 - A1.3.1 R의 자료형 – 2. 문자형(character)
  > char_x <- c("Pear","Apple"); char_x # 반드시 따옴표 사용필요
  [1] "Pear"  "Apple"
  
  > class(char_x)
  [1] "character"

  > Pear; Apple # Error: object 'Pear' not found : 변수(object)로 인식함
  Error: object 'Pear' not found

  > as.numeric('1')+as.numeric('2') # 함수 as.numeric()은 문자를 숫자로 변환
  [1] 3

  > as.numeric('a')+as.numeric('b') # 결과는 [1] NA
  [1] NA
  Warning messages:
  1: NAs introduced by coercion 
  2: NAs introduced by coercion 
  ```

<br>

### 3-1-3. 논리형

- TRUE(!=0) / FALSE(0) 및 논리형연산자(‘&’-곱, ‘|’-합, ‘!’-not)
- 데이터를 비교해서 참일 경우 TRUE(T)를 거짓일 경우 FALSE(F)를 반환함
- ‘&’ 기호는 양쪽이 모두 참일 때 결과가 참으로 나옴
- 반면 ‘|’ 기호는 둘 중 하나가 참일 때 결과가 참으로 나옴
  ```R
  # A1.3 자료형과 연산자 - A1.3.1 R의 자료형 – 3. 논리형(logical)
  > 5&0; 5&1 # 전자는 FALSE, 후자는 TRUE
  [1] FALSE
  [1] TRUE

  > 5|0; 1&-1 # 전자도 TRUE, 후자도 TRUE
  [1] TRUE
  [1] TRUE

  > !0; !1; class(!0) # 전자는 TRUE, 후자는 FALSE
  [1] TRUE
  [1] FALSE
  [1] "logical"
  ```

<br>

### 3-1-4. 인수형(factor)

- 범주형 자료를 다룰 때 문자형 데이터를 저장하는 새로운 방식의 프레임
- 수준(levels)이라 부르는 대푯값만을 포함하는 특별한 벡터임
- 여러 번 중복으로 나오는 데이터들을 각 값으로 모아서 대푯값으로 출력함
- 글자로 된 데이터를 Factor형으로 바꾸지 않고 있는 그대로 사용하고 싶을 경우 인수(argument) 옵션을 “stringsAsFactors=FALSE”로 지정함
  ```R
  # A1.3 자료형과 연산자 - A1.3.1 R의 자료형 – 4. 인수형(factor)
  > blood_type <- c("A","B","B","O","AB","A","B","A","O","AB"); blood_type
  [1] "A"  "B"  "B"  "O"  "AB" "A"  "B"  "A"  "O"  "AB"

  > summary(blood_type) # 함수 summary()는 객체의 요약 설명을 제공
     Length     Class      Mode 
       10 character character 

  > blood_type <- factor(blood_type); blood_type
   [1] A  B  B  O  AB A  B  A  O  AB
  Levels: A AB B O

  > class(blood_type); summary(blood_type)
  [1] "factor"
   A AB  B  O 
   3  2  3  2 
  ```

<br>

### 3-1-5. NA 및 Null

- NA는 결측값이라고도 하며 정해진 범위 안에 있지 않는 값
- NA가 들어 있는 값과 연산을 하게 되면 결과는 NA로 나옴
- 변수 값이 NA인지 아닌지 확인하려면 is.na() 함수를 사용
- 데이터에서 NA 값을 제거할려면 na.rm= 인수를 사용
- NULL이란 값이 정해지지 않아서 얼마인지 모름을 의미함
  ```R
  # A1.3 자료형과 연산자 - A1.3.1 R의 자료형 – 5. NA, NULL, 복소수형
  > cat(1, NA, 2,'\n'); sum(1,NA,2) # 후자의 합은 NA가 됨
  1 NA 2 
  [1] NA

  > cat(1,NULL,2,'\n'); sum(1,NULL,2) # 후자의 합은 3이 됨
  1 2 
  [1] 3
  
  > sum(1,3,NA); sum(1,3,NA, na.rm=T) # 후자는 NA가 제거 되고 합산됨
  [1] NA
  [1] 4
  ```

<br><br>

## 3-2. R의 날짜와 시간

- R에서는 날짜만 보는 함수가 있고 ‘날짜+시간’까지 함께 보는 함수가 있음
- 날짜와 시간을 동시에 보려면 POSIXct, POSIXlt 클래스를 사용
- 날짜와 시간을 보다 쉽게 관리해 주는 {lubridate} 패키지도 있음

### 3-2-1. 문자열(character string)을 날짜형으로 변환

- 함수 Sys.Date()는 사용자 컴퓨터의 현재의 날짜를 객체로 반환함
- 함수 Sys.time()은 사용자 컴퓨터의 현재의 날짜와 시간을 반환함
- 함수 as.Date()는 날짜를 날짜형 객체로 변환함
  ```R
  # A1.3 자료형과 연산자 - A1.3.2 날짜와 시간 – 1. 문자열을 날짜형으로 변환
  > Sys.Date()
  [1] "2017-02-01"

  > Sys.time() 
  [1] "2017-02-01 16:17:21 KST"

  > class("2017-02-01") 
  [1] "character"

  > class(as.Date("2017-02-01")) 
  [1] "Date" - 즉, 날짜를 객체로 변환함

  > class(Sys.Date()) 
  [1] "Date"

  > as.Date('2016/10/24'); class('2016/10/24'); class(as.Date('2016/10/24'))
  [1] "2016-10-24"
  [1] "character"
  [1] "Date"
  ```

### 3-2-2. 날짜형을 문자열로 변환

- 함수 format()를 사용하여 날짜형 객체를 문자열로 변환하여 사용가능함
- 함수 format()으로 날짜 외에도 다양하게 데이터포맷을 변경할 수 있음
- 함수 as.Date()의 인수로서 ‘format=~’의 지정을 위한 형식 알아보기
- format 함수 및 인수와 함께 몇 가지 옵션을 사용할 수 있음

형식 | 의미 | 형식 | 의미
-- | -- | -- | --
%d | 일자를   숫자로 인식 | %b | 월을   영어 약자로 인식
%m | 월을   숫자로 인식 | %B | 월을   전체 이름으로 인식
%Y | 연도를   숫자 4자리로 인식 | %y | 연도를   2자리 숫자로 인식

  ```R
  # A1.3 자료형과 연산자 - A1.3.2 날짜와 시간 – 2. 날짜형을 문자열로 변환
  > as.Date('08/13/2016') # 오류가 나옴
  Error in charToDate(x) : 문자열이 표준서식을 따르지 않습니다

  > as.Date('08/13/2016',format='%m/%d/%Y') # 오류 해소됨
  [1] "2016-08-13"

  > as.character(Sys.Date()) # 현재 날짜를 문자형 변수로 변환
  [1] "2016-08-13"

  > format(Sys.Date(),format='%m/%d/%Y') # mm/dd/yyyy 형의 문자열로 출력
  [1] "10/17/2022"

  > format(Sys.Date(),'%a') # 현재의 요일을 출력
  [1] "월"
  
  > format(Sys.Date(),'%b'); format(Sys.Date(),'%B') # 현재의 월을 출력
  [1] "10"
  [1] "10월"

  > format(Sys.Date(),'%m') # 현재의 월을 출력
  [1] "10"
  ```

<br>

### 3-2-3. 패키지 {lubridate}의 사용법

- {lubridate}는 날짜 요소를 분석하고 다루기 쉽도록 하는 도구를 제공함
- {lubridate}의 요소 선택 기능은 문자열을 POSIXct 날짜-시간 객체로 읽음
  ```R
  > install.packages("lubridate")
  # A1.3 자료형과 연산자 - A1.3.2 날짜와 시간 – 2. {lubridate}의 사용법
  > library(lubridate)
  > date1<-now(); date1 # 현재의 날짜와 시간 넣기
  [1] "2022-10-17 20:15:11 KST"

  > year(date1) # 연도만 출력하기
  [1] 2022

  > month(date1,label=T) # 월만 출력하되 영문 이름으로 출력
  Levels: 1 < 2 < 3 < 4 < 5 < 6 < 7 < 8 < 9 < 10 < 11 < 12

  > month(date1,label=F) # 월만 출력하되 숫자로 출력
  [1] 10

  > day(date1); wday(date1,label=T) # 일자출력; 요일을 출력하되 영문이름으로
  [1] 17
  [1] 월
  Levels: 일 < 월 < 화 < 수 < 목 < 금 < 토

  > date2<-date1-days(2); date2 # date1에서 2일을 뺀 결과 출력
  [1] "2022-10-15 20:15:11 KST"

  > month(date2)<-2; date2 # date2에서 월을 2월로 교체
  [1] "2022-02-15 20:15:11 KST"

  > date2+years(1); date2+months(2)+hours(-2) # 연도와 시간 연산 가능
  [1] "2023-02-15 20:15:11 KST"
  [1] "2022-04-15 18:15:11 KST"

  > date2+minutes(1); date2 + seconds(1) # 분, 초도 연산 가능함
  [1] "2022-02-15 20:16:11 KST"
  [1] "2022-02-15 20:15:12 KST"

  > date3<-hm("22:30"); date3 # hm()에서 h는 시간, m은 분을 의미
  [1] "22H 30M 0S"

  > date3<-hms("22:30:15"); date3 # hms()에서 h는 시간, m은 분, s는 초를 의미
  [1] "22H 30M 15S"
  ```


<br>

### 예제 [A1.1]

- (a) 현재 시점 오늘의 날짜와 요일을 출력하고 360일 이전 날짜와 요일을 출력하고 360일 이후 날짜와 요일을 출력하기
- (b) 현재 시점에서 50만초 이후에는 몇 월 며칠, 무슨 요일인가 출력하기
- (c) 현재 시점에서 5만분 이후에는 몇 월 며칠, 무슨 요일인가 출력하기
- (d) 현재 시점에서 5달 50일 500시간 이후의 월, 일, 요일을 출력하기
  ```R
  # A1.3.2 날짜와 시간 – 3. {lubridate}의 사용법 - [예제 1.1] 날짜와 요일 계산
  > date1 <- Sys.Date(); date1 # (a)
  [1] "2022-10-17"

  > format(date1,format='%a')
  [1] "월"

  > date2 <- date1 - 360; date2
  [1] "2021-10-22"

  > format(date2,format='%a')
  [1] "금"

  > date3 <- date1 + 360; date3
  [1] "2023-10-12"

  > format(date3,format='%a')
  [1] "목"

  > library(lubridate) # (b)
  > date4 <- now() + seconds(500000); date4
  [1] "2022-10-23 15:17:01 KST"

  > format(date4, format="%a")
  [1] "일"

  > date5 <- now() + minutes(50000); date5 # (c)
  [1] "2022-11-21 13:44:10 KST"

  > format(date5, format="%a")
  [1] "월"

  > date6 <- now() + months(5) + days(50) + hours(500); date6 # (d)
  [1] "2023-05-27 16:24:38 KST"

  > format(date6, format="%a")
  [1] "토"
  ```



<br><br><br>


#  4. 변수

- 변수란 사용자가 프로그래밍언어와 데이터를 주고받을 때 담는 그릇이다.
- 미리 정해진 데이터를 저장하고 전달할 때 사용하는 것을 상수라고 부른다.
- R에서는 변수의 자료형을 미리 지정하지 않아도 된다.

## 4.1 변수에 데이터를 할당

- 변수에 값을 할당할 때 “<-” 기호(권고됨) 또는 “=” 기호를 사용한다.
- 여러 개의 값을 하나의 변수에 담으려면 배열형 c() 함수를 사용한다.
- 하나의 변수에 여러 개의 데이터를 담으려면 데이터 형이 동일해야 한다.
- 영어와 숫자 모두 사용가능하나 첫 자는 반드시 문자여야 한다.
- 대소문자를 구별한다.
  ```R
  > var1 <- "홍길동"; var1; var2 <- 1996019; var2
  [1] "홍길동"
  [1] 1996019
  > var3 <- Sys.Date(); var3; var4 <- c("a","b","c"); var4
  [1] "2022-11-07"
  [1] "a" "b" "c"
  > var3 -> var4 -> var5; var4; var5
  [1] "2022-11-07"
  [1] "2022-11-07"
  > var6 <- var7 <- var3; var6; var7
  [1] "2022-11-07"
  [1] "2022-11-07"
  > string1 <- '정보통신'; string1
  [1] "정보통신"
  > comp <- c(1,"2"); comp # 숫자와 문자가 동시에 들어 있으면 문자로 변경됨
  [1] "1" "2"
  ```


<br><br><br>


#  5. 자료구조


<br><br><br>


#  6. 자료의 입출력


<br><br><br>


#  7. 함수


<br><br><br>


#  8. 조건문과 반복문


<br><br><br>

