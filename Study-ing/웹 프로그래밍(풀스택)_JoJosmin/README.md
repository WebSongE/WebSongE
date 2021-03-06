# 강의수강목표

[9월_둘째주(9/6 ~9/12)](#september-2)
* 1-1. Web개발의 이해 - FE/BE- ~ 1-3. CSS - FE

[9월_셋째주(9/13 ~ 9/19)](#september-3)
* 1-3.CSS - FE ~ 1-5. Servlet - BE

[9월_넷째주(9/20 ~ 9/26)](#september-4)
* 1- 5. Servlet - BE 
* 프로젝트 A-1

[9월_마지막주(9/27 ~ 10/3)](#september-5)
* 프로젝트 A

[10월_첫째주(10/4 ~ 10/10)](#october-1)
* 2-1 ~2-2

[10월_넷째주(10/25 ~ 10/31)](#october-4)
* 2-3 ~2-7
-------------------------------------------------------------------
## 강의수강진도기록
## september-2
### 9월 6일
> 1-1. Web개발의 이해 - FE/BE- 1)웹 프로그래밍을 위한 프로그램 언어

* 저급 언어: 기계 중심의 언어 ex) 기계어, 어셈블리어
--프로그래밍, 유지보수 어려움

* 고급언어: 사람 중심의 언어 ex) FORTRAN, C, Python 등

> 1-1. Web개발의 이해 - FE/BE- 2) 웹의 동작 (HTTP 프로토콜 이해)

* 인터넷: 네트워크들의 집합체

* HTTP: 서버와 클라이언트가 인터넷상에서 데이터 주고받기 위한 프로토콜
* HTTP 작동방식: 서버/클라이언트 모델(클라이언트 요청 시 서버가 응답)
  * 장: 불특정 다수 대상 적합, 클라이언트와 서버 간 최대 연결 수보다 많은 요청 처리 가능
  * 단: 클라이언트 이전 상황 알 수 없음(무상태)-->cookie 등장
 1) 클라이언트가 원하는 서버에 접속
 2) 클라이언트가 서버에 요청
 3) 요청에 따른 결과를 서버가 클라이언트에게 전달
요청 데이터 포맷
  * 요청헤더: 요청메서드/요청 uri/HTTP프로토콜 버전
  * 요청바디:(GET방식은 요청바디 없음)
응답 데이터 포맷
-응답헤더: 응답 HTTP프로토콜 버전/ 응답코드/응답메시지 
-응답바디: 실제 응답 리소스
 4) 서버와 클라이언트의 연결 종료
* URL: 인터넷 상의 자원의 위치

> 1-1. Web개발의 이해 - FE/BE- 3) 웹 Front-End 와 웹 Back-End

* 웹 프론트 엔드: 사용자에게 웹을 통해 콘텐츠(리소스) 제공, 사용자 요구사항에 반응
* 웹 프론트 엔드의 역할
  * 콘텐츠 잘 보여주기 위한 구조 생성(HTML)
  * 적절한 배치와 일관된 디자인(CSS)
  * 사용자 요청 반영(Javascript)

* 백엔드: 정보 처리, 저장, 요청에 따라 정보 내려줌 (서버 입장의 개발)
* 백 엔드 개발자가 알아야 할 것들
  * 프로그래밍 언어
  * 웹의 동작 원리
  * 알고리즘, 자료구조 등 지식
  * 운영체제, 네트워크 등 이해
  * 프레임워크에 대한 이해
  * DBMS에 대한 이해와 사용방법

### 9월 10일
> 1-1. Web개발의 이해 - FE/BE- 4)browser의 동작

* 브라우저: 월드와이드웹에서 정보를 검색, 표현, 탐색 위한 소프트웨어
  * UI, Browser engine(소프트웨어 동작), Rendering engine, Data Persistance, networking, JavaScript coder, UI Backend로 구성
  * 네트워크 모듈과 해석기 포함
  * 브라우저마다 서로 다른 엔진(Rendering engine) 포함
   * HTML 코드 해석, DOM(Document Object Model) tree 구조로 형성 -> Render tree형성 --> rneder tree 기준으로 css 합쳐 화면에 어떻게 배치할지 결정 -->화면에 그려짐
   * Webkit main flow
   ![webkitflow](https://user-images.githubusercontent.com/86174004/132713030-e433f15f-5d08-4f1e-9acb-35ad77069035.png)

  * block-명령
  
> 1-1. Web개발의 이해 - FE/BE- 5)browser에서의 웹 개발

* HTML은 태그사용해서 표현
   * html
   * head: HTML 문서에 관한 추가적 정보
   * body: 화면에 표현되어야할 것들
   * meta: 문서가 어떤 것인지 브라우저에 전달
   * li:리스트 태그
   * script : javascript 이용 태그
 * HTML은 계층적
 * 브라우저는 HTML 한 라인씩 해석
 * javascript코드가 head로 갈 경우 렌더링 방해 가능--> body 닫히기 직전 혹은 body이후에 작성

### 9월 11일

> 1-1. Web개발의 이해 - FE/BE- 6)웹서버

* 웹서버: 웹 서버 소프트웨어가 동작하는 컴퓨터
* 클라이언트가 요청하는 것 전달
* 웹브라우저, 웹크롤러 요청 리소스- 정적인 데이터 (컴퓨터 저장 파일), 동적인 결과(프로그램을 통해 만들어진 결과물)
* "렌더링한다": 리소스들을 얻어와 합쳐서 보여주는 것
* 리소스가 없거나 요청 소스 없으면 오류 발생
* 웹 서버 소프트웨어
   * Apache:오픈소스 소프트웨어
   * Nginx : 더 적은 자원으로 더 빠르게 데이터 서비스, 오픈소스
   * Microsoft IIS
   
> 1-1. Web개발의 이해 - FE/BE- 7)WAS

* 클라이언트/서버 구조 : 클라이언트는 서버에게 정보 요청해 응답 결과 사용
* DBMS: 다수의 사용자가 데이터베이스 내의 데이터에 접근할 수 있도록 해주는 소프트웨어
  * 서버 형태로 제공
* 미들웨어: 비스니스 로직을 미들웨어 서버에서 동작하도록 함으로써 입력과 출력만 클라이언트가 담당하게 함 (클라이언트 쪽 비즈니스 로직 많을 수록 비용up)
* WAS: 미들웨어 중 하나, 웹 클라이언트의 요청 중 웹 어플리케이션이 동작하도록 지원 목적
  * 프로그램 실행 환경과 데이터베이스 접속
  * 여러개의 트랜젝션(논리적 단위) 관리
  * 업무를 처리하는 비즈니스 로직 수행
* 웹 서버 vs WAS 
  * 웹서버: 정적인 기능 전달
  * WAS: 동적인 기능 전달
* WAS도 웹 서버 기능 내장: 정적인 콘텐츠 처리에 있서 성능 차이 X
* 규모 커질수록 웹 서버와 WAS 분리: 자원 이용의 효율성 및 장애 극복, 배포 및 유지보수 편의성 위해

> 1-2.HTML-FE - 1)HTML Tags

* 주석 : !--...--
* 링크
* 이미지
* 목록:ul
* 제목

> 1-2.HTML-FE - 2)HTML Layout 태그

 * header: 상단 영역
 * section
 * nav
 * footer :하단 영역
 * aside :side 쪽에서 추가적인 것들 표현가능
 *div: 본문에서 많이 사용
![5086 HTML5PageLayout_2](https://user-images.githubusercontent.com/86174004/132933875-700e47d9-1db6-47cc-8ca6-8245779a5280.jpg)

> 1-2.HTML-FE - 3)HTML 구조설계

 * 상단/본문/ 네비게이션(큰 부분 분리)-각 영역 안에 내용의 구조
 * 어떤 태그를 쓰느냐-정답x

> 1-2.HTML-FE - 4)class와 id속성
 * ID
   * 고유한 속성으로 한HTML당 하나 (하나 이상 써도 오류x 신경써야함)
   * 특별한 제어 가능, 검색 용이
 * class
   * 하나의 HTML문서 안 중복 사용 가능
   * 하나의 태그에 여러 개 class 이름을 공백 기준 나열 가능
   * 전체적 스타일 일관성 위해서는 사용이 필수적

## september-3

### 9월 13일
>  1-3.CSS - FE-1)CSS 선언방법
* css: selector, property, value로 구성
* style을 HTML에 적용하는 방법 (inline이 우선 순위)
  * inline :html태그 안에다가 작성(구조 스타일 섞여 유지보수 어려움)
  * internal:head안에 작성가능(별도의 css파일 필요 없음)
  * external: 외부파일(.css)로 지정
 
> 1-3.CSS - FE-2)상속과 우선순위 결정
* 상위 적용 스타일 하위에도 적용: box-model 제외(width, height, margin, padding, border)
* CSS파일에 두고 style태그로 표현시: inline > internal > external 순 우선순위
* inline > internal = external
* id > class > element 순 우선순위: 캐스캐이딩
* 같은 선택자: 나중에 선언한 것이 반영
* 더 구체적으로 표현된 것을 우선 적용
 
### 9월 15일
> 1-3.CSS - FE-3)CSS Selector

* element에 style지정을 위한 3가지 선택자
  * tag로 지정 :span-모든 span태그에 적용
  * id로 지정: id 가진 코드에 적용
  * class로 지정
  * id, class 요소와 함께 사용 가능
  * 그룹 선택 가능: , 이용
  * 하위 요소 선택: 공백 이용
  * 자식 선택: >이용
  * n번째 자식 요소를 선택 :nth child

> 1-3.CSS - FE-4)CSS 기본 Style 변경하기
  * font 색상 변경: color
  * font 사이즈 변경:font-size
  * 배경색:background-color
  * 글씨체 글꼴:font-family- Gulim, monospace, sans-serif
  * 웹폰트(다운로드)/unicode 사용해서 아이콘 표현가능
  
### 9월 18일
> 1-3.CSS - FE-5)Element가 배치되는 방법(CSS layout)
* layout 작업 ( Rendering과정 ): element를 화면에 배치하는 것
  * 위에서 아래로 배치되는 것이 기본
  * display: block
  * display: inline(좌우로 흘러감)(높이, 넓이 반영x) ( span, a, strong-모두 inline)--block 설정하면 위에서 아래로 흘러감
  * position- 어떤 위치에 엘리먼트를 배치할지 수월
   * static: 순서대로 배치
   * absolute: 기준점에 따라 특별한 위치(top/left/right/bottom)-top,left값 꼭 주기!
   * 기준점: 상위 엘리먼트로 단계적 찾아가며 static이 아닌position이 기준점
   * fixed는 viewport(좌측, 맨 위 기준 동작)
 * 엘리먼트가 배치되는 방식
   * margin:간격
   * float: 원래 flow에서 벗어날 수 있음
   * box-model: box의 크기와 간격에 관한 속성 - margin, padding, border, outline으로 생성, box-shadow: border 밖 테두리 그릴 수 있음
   * box-sizing: content-box(padding에 따라 크기 달라짐)
   * box-sizing: border-box(크기 변화x)
 * 엘리먼트의 크기: 기본적으로 부모의 크기(100%=부모의 크기 다 갖는 것)
 * layout 구현방법: float 사용해 2단,3단 컬럼 배치, 최근 css-grid, flex도 사용
   * 특별한 위치 배치: position absolute, 기준점 relative 설정
   * 네비게이션: block 엘리먼트 -> inline-block으로 변경해 가로 배치
   * 엘리먼트 안 텍스트 간격과 다른 엘리먼트 간격-padding과 margin 활용
  
### 9월 19일 

> 1-3.CSS - FE- 6) float 기반 샘플 화면 레이아웃 구성
* float에서 footer가 위로 올라가는 것에 대한 문제 - clear로 해결
* 자식이 float인 경우 - 자식으로 생각하지 않음 ( 높이값 생각x-overflow 속성으로 인식하게 할 수 있음)

> 1-3.CSS - FE- 7)디버깅-HTML-CSS

> 1-4. 개발환경 설정 - BE

## september-4

### 9월 24일

> 1-5.Survlet의 이해 -1) Survlet이란?
* 서블릿: 자바 웹 어플리케이션 중 동적인 처리를 하는 프로그램-WAS에 동작하는 JAVA클래스
* JSP와 서블릿 조화롭게 사용해야 최상의 결과 얻을 수 있음

> 1-5. Survlet의 이해 -2) Survlet 작성방법

> 1-5. Survlet의 이해 -3) Survlet 라이프 싸이클
* Survlet 생명주기 : HttpServlet의 3가지 메소드를 오버라이딩: init(), service(request, response),destroy()
* 새로고침 시에 service만 호출-service는 실제 요청된 개체가 메모리에 있는지 확인 후 있다면 
* 코드 수정시 destroy 호출- 새로고침시에 수정된 메모리 처음부터 호출
* WAS는 서블릿 요청 받으면 해당 서블릿이 메모리에 있는지 확인, 서블릿 클래스 메모리에 올리면-init(), 그 후 service()호출, 메모리 갱신이나 was 종료시에 destroy()
* service(request, response)메소드: 클라이언트 GET-doGet메소드 호출, 클라이언트 Post-doPost

>1-5. Survlet의 이해 -4) Request, Response 객체 이해하기
* WAS는 웹 브라우저로부터 Servlet요청을 받으면 요청할 때 가지고 있는 정보를 HttpServletRequest객체를 생성하여 저장,
웹 브라우저에게 응답을 보낼 때 사용하기 위하여 HttpServletResponse객체를 생성
생성된 HttpServletRequest, HttpServletResponse 객체를 서블릿에게 전달
* HttpServletRequest: request정보를 서블릿 전달 목적, 헤더정보, 파라미터, 쿠키, url,uri,body의 stream 읽어들이는 메소드 가짐
* HttpServletResponse: 서블릿에서 이를 이용해 content type, 응답코드, 응답 메시지 

## september-5
* 프로젝트 A
## october-1

### 10월 5일
> 2-1 Javascript-FE -1)자바스크립트 변수-연산자-타입
* 변수 선언
  * var
  * let
  * const: 재할당 불가
* 연산자
  * 삼항연산자
  * 비교연산자: === (타입까지 비교)
* type : undefined, null, boolean, number, string, object, function, array, Date, RegExp
  * 선언할 때가 아닌 실행타임에 결정
  * toString.call함수 사용/type of 사용/배열의 경우 isArray

> 2-1 Javascript-FE -2)자바스크립트 비교-반복-문자열
* 비교문:if, else if, else-- 한 줄 코딩도 가능, 삼항연산자로 대체가능
* 분기 -switch: case, default
* 반복:for, while -성능개선시 reverse 해서도 많이 사용
  * 배열의 경우 forEach메서드, for-of탐색도 있음. for-in-객체 탐색
* 자바스크립트의 문자, 문자열-같은타입(문자열)

> 2-1 Javascript-FE -3) 자바스크립트 함수
* 함수: 여러개의 인자를 받아서결과 출력, 값이 할당되지 않으면 파라미터는 undefined라는 값을 가짐
* 함수 표현식: 선언과 호출순서에 따라 함수 실횅 안 될 수 있음
* 호이스팅: 자바스크립트 함수-실행되기 전에 함수안에 필요한 변수값들을 미리 모아서 선언
* arguments 객체: 함수 실행시 argument지역변수가 자동 생성
  * 선언한 파라미터보다 인자가 많아 넘어온 인자를 arguments로 배열의 형태로 하나씩 접근 가능
  * 배열의 메서드 사용불가(배열타입 아님)
  * 필요한 경우에 체크할 때만 사용, 코드 짤 때는 의도를 알 수 없으므로  쓰는 것 자제
 * arrow function: 한줄로 함수 간단히 선언 가능

> 2-1 Javascript-FE -4) 자바스크립트 함수 호출 스택
* call stack: 함수 잠시 멈춰놓은 상태에서 다른 함수 불러옴
  * 연속적 호출 시 오류 발생 
### 10월 6일
>2-2 Web UI 개발-FE-1)windows 객체(setTimeout)
* setTimeout-인자로 함수 받음, 함수 반환가능
  * 비동기 실행: 동기적 실행 끝난 후 실행
  
>2-2 Web UI 개발-FE-2) DOM과 querySelector
* 브라우저에서 HTML코드를 DOM 객체형태의 모델로 저장-DOM Tree
* 브라우저에서 DOM Tree찾고 조작하는 걸 도와주는 메서드 제공
  * getElementByld()
  * Element.querySelector()
  * css selector

>2-2 Web UI 개발-FE-3) Browser Event, Event object, Event handler
* Event
  * 등록: addEventListener - 함수가 두번째 인자
  * 객체: event.target-element 속성 
  
>2-2 Web UI 개발-FE-4) Ajax통신의 이해
* Ajax: 동적으로필요한 시점에 컨텐츠를 받아와서 표현함
* JSON:표준적 데이터 포맷 결정 위해서 사용 
* Ajax 실행코드
  * XMLHttpRequest객체 생성, open메서드로 요청 준비, send메서드로 서버로 보냄
  * 요청처리 완료되면load이벤트 발생,콜백함수 실행
 
 >2-2 Web UI 개발-FE-5) javascript debugging
 * Pause, Continue
 * Step over next function call
 * Step into next function call 
 * Step out of current function
 * Active/Deactive breakpoint
 * Pause on exception

## october-4
### 10월 27일

>2-3 JSP-BE-3) JSP란?
