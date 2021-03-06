﻿# team-asan
아산멤버들의 아이디어 정리 공간


## 마크다운 사용법

https://gist.github.com/ihoneymon/652be052a0727ad59601

========================== ypLim ====================================
Node JS
	- 대표 ORM : Sequelize
Express
	- nodeJS를 위한 빠르고 개방적이고 간결한 웹 프레임워크
	- 일반적인 Web Application 기능을 포함하는, 
	  WebApp을 개발하는데 필요한 수많은 모듈을 집합하여 사용자가 쓰기 쉽도록 만들어 둔 모듈
	- 정규식을 지원하는 강력한 라우팅 메커니즘, 심플한 라우트 필터링
	- 미들웨어 아키텍처를 활용하며 다양한 데이터 출력지원
	- 다중으로 템플릿 엔진을 허용하는 간단한 변수전달 뷰 시스템
	** 핵심 ㅡ> 라우터 자체에 미들웨어나 조건들을 끼워넣고 순서대로 순환해가며 처리해가는 것

ORM(Object Relational Mapping)
	- OOP언어와 데이터를 다루는 RDBMS와의 상이한 시스템을 매핑하여, 쉽게 데이터관련 OOP프로그래밍을 하도록 하기 위한 기술이다.
	- 객체지향 애플리케이션은 객체 지향대로 다루고, 관계형 데이터베이스는 
	   관계형 데이터베이스대로 설계하고 사용할 수 있도록 중간에서 도와주는 기술

	- Ex) 		OOP				RDBMS
		        클래스		<ㅡ>		테이블
		     Object-graph      <ㅡ>		Relation
	   로 표현이 가능한데 표현방식에서 상당한 차이점이 있어 매핑을 통해 변환을 해주어야 한다.
	장점 ㅡ> 
		● 개발자가 OOP나 CBD에 의한 개발에만 집중가능
		● RDBMS관련 부분의 고려사항 최소화
	 	● OOP언어/CBD개발 방법론에서 클래스나 컴포넌트 설계 및 개발에서 
		    이질적인 RDBMS 관련된 부분을 최소화하고, 원 제품의 로직 구현에 
 		    충실하고자 하는 의도에서 나온 산물
		● 생산성이 높아지고 캐시 등 다양한 저장소를 활용하기에 유연한 구조를 만들어 준다.
		● 탑다운(Top-down)방식의 설계를 채택할 수 있는 경우 장점이 극대화 된다.
	단점 ㅡ>
		● 현실적으로 자바계층에 맞춰 DB스키마를 설계할 수 없는 프로젝트가 상당히 많으며
	 	    이런 경우 ORM을 염두에 두지 않고 설계된 리거시 스키마를 그대로 두고 바텀업(bottom-up)방식으로 
             구현하는 접근을 할 수 밖에 없기에 ORM의 장점이 상당히 퇴색
	 	● ORM기술 자체도 최적화나 복잡도, 또는 추상화 등의 이유로 꾸준히 비판받아왔다. 
	 	● 현재는 ORM을 사용하지 않고도 영속성 문제를 깔끔하게 처리할 수 있는 
		    대안도 존재한다.
Maria DB
	- mysql 코어를 가지고 분리개발 한 것이 mariaDB
	   Mysql의 모든 명령어, 인터페이스, 라이브러리와 같은 API가 MariaDB에도 존재하며 
	   MariaDB는 사실상 MySQL의 완벽한 대체제라고 말할 수 있다.
	   기능상의 차이는 거의 없지만 MariaDB의 퍼포먼스가 더 좋고 엔진도 추가되어 
	   MySQL보다 뛰어나다.
	장점 ㅡ> 
    	가장 큰 장점은 속도, 2배가량 퍼포먼스가 개선되었다.
MVC (Model View Controller)
	- 디자인 패턴 중 하나 ㅡ> 하나의 애플리케이션(프로젝트)를 세 가지의 역할로 구분한 패턴
	 Model ㅡ> 애플리케이션의 정보 즉 데이터를 담당하며 데이터의 가공을 책임지는 컴포넌트
	 View ㅡ> 데이터 및 객체의 입력, 그리고 보여주는 출력을 담당하는 사용자 인터페이스 요소 
		  클라이언트 측 기술인 HTML/CSS/JavaScript 를 모아둔 컨테이너
	 Controller ㅡ> Model과 View의 다리역할을 하는, 비즈니스 로직을 담당하는 Controller
	● 왜 사용할까? 
	ㅡ> Model, View, Controller 서로 영향을 받지 않는 3가지로 분리하여 
	      각자의 역할에 집중할 수 있게끔 개발가능
	      애플리케이션의 확장성, 유지보수성, 유연성이 증가하고 중복코딩을 줄일 수 있다.
	유연성 ㅡ> 새로운 요구사항에 대해 최소한의 비용으로 보다 유연하게 대처할 수 있는 것
	     단점 - View가 Model을 이용하기에, 서로간의 의존성을 완벽히 피할 수 없다는 단점이 있다
		     ㅡ> 좋은 MVC는 의존성을 최대한 낮게 디자인한 패턴
	** NodeJS용 MVC 프레임워크로 Express(모듈) 가 있다.
AngularJS
	- 2013년 9월 1.0.8버전으로 정식 출시
	- AngularJS는 HTML을 확장시켜 동적인 Application을 지원하며 
	   데이터가 변경함에 있어 자동적으로 AngularJS에서 UI의 요소를 만들고 
	   데이터 필터링/소팅 등 많은 기능을 제공
	- AngularJS의 가장 핵심기능은 양방향 데이터바인딩 기능
	
	장점 
	- JavaScript나 jQuery에 비해 개발자의 부담이 훨씬 줄어든다.
	- 프레임워크 코어에 DOM변환 엔진을 넣어둠으로써 템플릿을 HTML파일로 작성가능
	   DOM변환 엔진을 통해 개발자는 AngularJS의 다양한 디렉티브(지시자)를 이용하여 
	   HTML문법을 확장가능
	● Scope / Model / View / Controller / Directives(지시자)
	** Scope ㅡ> 모델 변경을 감지하고 표현하기 위한 책임을 갖는다. 
				(scope를 통해 View와 Controller간의 소통이 가능)
	** Model ㅡ> 화면 템플릿에 합쳐지는 데이터를 가지고 있는 자바스크립트 객체(= 데이터)
		    	Scope는 항상 모델을 참조하고 있다.
	** View  ㅡ> Angular는 템플릿이 HTML이어서 바로 DOM으로 해석되고 
				 DOM안에 directive가 템플릿 엔진 $compile지시어를 통해 $watch를 설정하고 
				 모델의 변경을 계속 감시하게 된다.
		    	 View는 템플릿으로 Scope의 투영체이고, Scope는 Model과 View를 연결하며
		     	Controller로 이벤트를 보내는 역할을 한다.  
	** Controller ㅡ> scope에 model과 function을 정의해주는 역할 
						ㅡ> 그러면 View가 그것들을 사용
			   			자바스크립트이며 업무적 행위를 정의한다. 
			   			또한 DOM 렌더링 정보가 일체 없다.
	** Directives(지시어) ㅡ> HTML을 확장하여 주고 행위를 일으키는 주체 
				  			Ex) 데이터 바인딩을 위한 중괄호 표기 {{}}
				      		컨트롤러가 뷰의 어느 부분을 감독할지 정하는 ng-controller
				      		input을 해당 모델의 구성물에 바인딩하는 ng-model
				      		이들 모두 directive를 이용한 확장 문법이다.

Git (ahahah)
	- Repository(저장소) ㅡ> 파일이나 폴더를 저장해 두는 곳
							Git저장소의 장점은 파일이 변경이력별로 구분되어 저장된다.
	- 커밋 ㅡ> 파일 및 폴더의 추가 및 변경 사항을 저장소에 기록하기 위함
	- 커밋메세지형식 ㅡ> 명료하고 이해하기 쉽게 남기기
						1번째 줄 : 커밋 내의 변경 내용을 요약
						2번째 줄 : 빈칸
						3번째 줄 : 변경한 이유
	- 브랜치 ㅡ> 여러 개발자들이 동시에 다양한 작업을 할 수 있게 만들어 주는 기능
		   		독립적으로 어떠한 작업을 진행하기 위한 개념
	- 통합 브랜치 ㅡ> 언제든지 배포할 수 있는 버전을 만들 수 있어야 하는 브랜치
					  항상 안정적인 상태를 유지해야 하는 브랜치(보통 master로 사용)
	- 토픽 브랜치 ㅡ> 버그 수정이나 기능추가 등의 단위작업을 위한 브랜치
	- HEAD ㅡ> 현재 사용중인 브랜치의 선두 부분을 나타내는 이름
		 	 'HEAD'를 이동하면, 사용하는 브랜치가 변경된다.
	- stash ㅡ> 파일의 변경 내용을 일시적으로 기록해두는 영역
		  ex) 체크아웃 시 커밋하지 않은 변경내용 중 전환된 브랜치에서 이미 변경된 기록이 있을 경우
		      충돌이 일어날 수 있는데, 이 경우 stash로 변경 내용을 다른 곳에 저장 ㅡ> 충돌을 피한 후
		      체크아웃을 하면 된다.
	● merge와 rebase의 차이점
		merge				rebase
	변경내용의 이력이 모두 남아있기 / 이력은 단순해지지만, 원래의 커밋 이력이 변경됨.
	때문에 이력이 복잡해짐		/ 정확한 이력을 남겨야 할 필요가 있을 경우에는
					  			사용하면 안됨.
	* rebase : 토픽 브랜치에 통합 브랜치의 최신 코드를 적용할 경우에 사용
	* merge : 통합 브랜치에 토픽 브랜치를 불러올 경우에는 우선 rebase를 한 후 merge
	● develop 브랜치 ㅡ> 통합 브랜치의 역할을 하며, 평소에는 이 브랜치를 기반으로 개발진행

ER Diagram
	- 우리는 구조화된 데이터를 저장하기 위해 데이터베이스를 사용
	  이 데이터의 구조 및 그에 수반한 제약 조건들은 다양한 기법에 의해 설계될 수 있다.
	  그 기법 중 하나가 개체-관계 모델링(ERM), ERM프로세스의 산출물이 개체-관계 다이어그램(ERD)
	- 개념적 데이터 모델 혹은 시맨틱 데이터 모델의 한 타입이다.
	● ERD의 논리설계단(모델) - 의미명(한글이나 알아보기 쉬운 단어로 표현)
				 			  엔티티와 엔티티타입, 관계를 정의, 어떠한 정보를 객체화할 것인가에 대한 규정
				 			  물리 dbms벤더에 종속되는 최종과정
	● ERD의 물리설계단 - 실제 컬럼명
			   			각 엔티티 관계에 의해서 나오는 테이블 등 실제로 dbms에 생성될 테이블들이 설계
			   			논리모델이 실제 dbms에 적용시키는 상세화 과정
	툴 - er-win
Bootstrap
	- 동적인 웹 사이트 및 응용 웹 개발을 위한 프론트엔드 프레임워크
	- 입력 창, 버튼, 다양한 레이아웃 등을 HTML/CSS 기반의 디자인 템플릿으로 제공
		ㅡ> 손쉬운 웹페이지 제작
	오픈소스로 공개되어 있어 사용자의 목적에 따라 커스터마이징 및 재배포 가능
	장점 ㅡ> 
    	 - 기본적인 틀, 구현된 컴포넌트 사용법을 익히고 사용한다면 쉽게 사용가능
		 - 기본적으로 반응형 페이지를 지원하고 있다.
	단점 ㅡ> 
    	 - 작업속도나 생산성면에 있어서는 효율적일 수 있으나 사용자 입맛에 맞게
		   수정하기 위해서는 부트스트랩에 구현된 기능을 수정할 필요가 있으므로
		   비효율적일 수 있음
		 - IE8의 지원을 위해 많은 부분을 JavaScript에 의존하는 경향이 크기 때문에 무겁다.

Responsive Web
	- 디자인과 개발이 화면 사이즈, 플랫폼 등을 기본으로 하여 사용자의 환경과 행동에 맞춰 반응하는 것
	
	필요성
	- 스마트폰, 태블릿 PC 등 다양한 스마트디바이스들이 등장하면서 디바이스별로 중복적으로
	  화면을 만들지 않고 다양한 해상도/환경을 하나의 콘텐츠로 이용하고자 하는 니즈에서 탄생

	기대효과
	- 다양한 기기를 사용하는 사용자들을 만족시킬 수 있다.
	- 웹사이트가 쉽게 읽고 따라올 수 있을 때 사용자들이 해당 페이지에 더 오래 머물면서
	  컨텐츠를 살펴보고 구매나 예약 등의 서비스로 이어질 수 있음.
		ㅡ> 사용자의 만족도 / 영업 및 마케팅 촉진 
RESTful API
	- 웹 설계의 우수성을 살려 웹의 장점을 최대한 활용할 수 있는 아키텍처
	
	주 구성요소
	● 리소스 : 접근할 대상, URI를 통해 식별
		- ex) URI
		http://api.domain.com/books		ㅡ> 도서정보 컬렉션
		http://api.domain.com/books/1		ㅡ> 1번 도서 정보
		http://api.domain.com/books/1/photo 	ㅡ> 1번 도서의 사진
		
		- 리소스명은 동사보다 명사를 활용, 어떤 자원인지 표현하는데 집중할 것
		- URI 구성 예) /(컬렉션)/(아이템)/(컬렉션)/(아이템)/
				/sports/soccer/players/1/

	● 메소드 : 리소스에 대한 행위, 표준 HTTP메소드에 따라 자원에 접근(생성, 조회, 수정, 삭제)
		- HTTP 메소드		/ 	자원에 대한 행위
		  
		  POST			/	자원 생성 (Create)
		  GET			/ 	자원 조회 (Read)
		  PUT			/	자원 수정 (Update)
		  DELETE		/ 	자원 삭제 (Delete)
		
		- Endponit
		URI별 HTTP 메소드로 구현된 항목
		
		ex)
		HTTP메소드		URI(자원)		Endponit의 행위
		POST	 http://api.domain.com/books/		새로운 도서정보 생성
		GET	 http://api.domain.com/books/		도서정보 목록 조회
		GET	 http://api.domain.com/books/1/		1번 도서정보 조회
		PUT	 http://api.domain.com/books/1/		1번 도서정보 수정
		DELETE	 http://api.domain.com/books/1/		1번 도서정보 삭제
	
	● 메세지 : HTTP 헤더와 바디에 포함된 메세지는 메세지를 처리하기 위한 충분한 정보를 포함
		- RSET에서 자원에 대한 정보는 HTTP 바디와 HTTP 헤더, 응답 상태코드를 활용

		- HTTP 바디
		HTTP 바디에 포함된 데이터를 통해 자원에 대한 정보를 전달한다.
		데이터 포맷으로는 JSON을 많이 사용, XML / 사용자정의 포맷을 정해서도 사용 가능
		
		- HTTP 헤더
		HTTP 바디의 컨텐츠 종류를 명시할 수 있다.
		헤더에 정의된 컨텐츠 타입에 따라 데이터를 분석하도록 구현해야 한다.
		요청 HTTP 헤더 ㅡ> Accept 항목
		응답 HTTP 헤더 ㅡ> Content-type 으로 컨텐츠 타입을 설명
	
		- 컨텐츠 타입 종류
		* application/json
		* application/xml
		* text/plain
		* image/jpeg
		* image/png
		** Content Type? 
		 request에 실어보내는 데이터 타입의 정보를 표현
	
	● 제약조건(특징)

		- 인터페이스 일관성(Uniform Interface) 
		   아키텍처를 단순화하고 분리해 각 부분을 독립적으로 발전시킬 수 있음

		- 클라이언트/서버
		   클라이언트와 서버의 역할이 각각 구분
		   클라이언트: 사용자 인증, 상태(세션, 로그인정보)관리와 서버 리소스 요청을
			      책임지는 구조로 역할 구분(상호 의존성 줄임)
			 서버: API를 제공, API요청 시 비즈니스로직 처리와 데이터 저장을 책임진다.

		- 무상태(Stateless)
		   REST서버는 작업을 위한 상태정보(세션, 쿠키)를 관리하지 않아야 함.
		   시스템 영향없이 관리 및 업데이트 가능

		- 캐쉬(Cacheable)
		   HTTP 웹표준으로 HTTP가 가진 캐싱 기능이 적용됨

		- 계층화(Layered system)
		   서버를 다중 계층으로 구성할 수 있음. 비즈니스 로직을 수행하는 API 서버,
		   그 앞단에 사용자 인증, 암호화, 로드밸런싱 등의 계층을 추가해 구조상의 유연성 제공
	
	** REST는 어떤 자원(리소스)에 대한 어떤 행위(메소드)를 어떻게(메세지)할 지 HTTP기반으로 정해놓은 아키텍처
	** node.js로는 REST api를 단순한 구조로 사용할 수 있다.

JSON(JavaScript Object Notation)
	- JavaScript에서 객체를 만들 때 사용하는 표현식
	- 속성-값 형태로 이루어짐 (ex: {"memberNo" : 50, "addr" : "경기도 안양"} )
	- 이 표현식은 사람도 이해하기 쉽고, 기계도 이해하기 쉬우면서 데이터의 용량이 작다.(경량)
		ㅡ> 그래서 최근 JSON이 XML을 대체하여 설정의 저장이나 데이터의 전송 등에 많이 사용
	
	사용 목적
	- 단순히 데이터를 받아서 객체나 변수로 할당해서 사용하기 위함
	- 주로 Ajax를 사용해 데이터를 주고 받을 때 그 데이터 포맷으로 JSON을 사용
	
	장점
	- 프로그래밍 언어와 플랫폼에 독립적이므로, 서로 다른 시스템 간에 객체를 교환하기에 좋다.
	- 자바스크립트의 문법을 채용했기 때문에(자바스크립트 언어로부터 파생)
	  자바스크립트에서 eval 명령어를 통해 곧바로 사용할 수 있다.
	
	단점
	- 상호호환성과 이종 시스템들간의 이해를 방해하지 않기 위해 주석, 코멘트를 권장하지 않음
	(JSON의 단점을 보완한 것으로 JSON5가 있음)
	
Bitbucket
	- 무료 Git 솔루션으로써, 무제한 사설 Repository를 제공한다.

	장점
	- 기존의 svn / git의 repository에 있던 것들을 주소와 계정정보만 가지고 손쉽게 옮겨올 수 있다.

	단점
	- 팀원 제한이 5명 이하 이다.

