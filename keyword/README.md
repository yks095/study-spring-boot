### 메소드들의 집합 = 라이브러리
### 라이브러리들의 집합 = 패키지
### 패키지들의 집합 = 모듈
### 모듈들의 집합 = 라이브러리1

### 프레임워크
 - 특정규약을 따름
 - 흐름이 존재
 - 규약을 지키면 코딩하기 보다 쉬움
 - 복잡한 문제를 해결하거나 서술하는데 사용되는 기본 구조
 - 웹페이지를 개발하는데에 나타나는 어려움을 줄이는 것이 주목적
 - 대표적으로 db연동, 템플릿 형태의 표준, 세션관리, 코드재사용 등의 기능을 포함


## 스프링과 스프링부트

### 스프링
 - 자바기반의 프레임워크
 - 톰캣이라는 서버가 내장되어있음

### jsp
 - 자바 서버 페이지

### 장고
 - 파이썬기반의 프레임워크

### 스프링부트
 - 스프링의 세팅을 쉽게하기위해 사용
 - 환경설정을 최소화

### 메이븐
 - 자바 프로젝트의 빌드를 자동화 해주는 빌드 툴
 - 자바 소스를 컴파일하고 패키지에서 deploy하는 일을 자동화 해주는 것

### 빌드
 - 소스코드를 컴퓨터에서 실행할 수 있는 파일로 만드는 것
### 컴파일
 - 소스코드를 번역
### run
 - 컴파일 + 빌드


### NoSQL
 - 쿼리를 안쓰고 데이터를 찾는 방식
### Rest
 - 웹설계의 우수성을 제대로 사용하기위해 생산한 아키텍쳐
### Redis
 - 오픈소스기반의 비관계형 db관리 시스템

### 쿠키
 - 클라이언트에 저장되는 키와 값이 들어있는 작은 데이터 파일

### 세션
 - 서버 메모리에 저장되는 정보
 - 쿠키와는달리 사용자 정보가 노출되지 않음(서버에 저장되기 때문에)

### 스타터
 - 특정 목적을 달성하기 위한 의존성 그룹

### jpa
 - 어플리케이션과 jdbc를 연결시켜주는 도구
### jdbc
 - 자바에서 db에 접속할 수 있도록 하는 자바 인터페이스

### 의존성과 의존성 주입

#### Class A가 제대로 작동하기 위해 Class B의 기능이 필요하다
#### 즉, A는 B가 없으면 제 기능을 못한다 = A가 B를 사용하고 있다.
 - B에 새로운 메소드가 추가되거나 기존 메소드의 형식이 바뀌면 A도 그에 따라 수정되거나 추가되어야 함.
 - B의 형식은 그대로 이지만, 기능이 내부적으로 변경되면 A의 기능에도 영향을 미침

두 개의 클래스 또는 모듈이 의존관계에 있다고 말할 때는 방향성을 부여해주어야 함.
누가 누구에게 의존하는 관계에 있다는 식이어야 함.

### 의존성 관계란
 - 객체와 객체의 결합관계
 - 하나의 객체에서 다른 객체의 변수나 메소드를 이용해야 하면, 이용하려는 객체에 대한 객체 생성과 새로 생성된 객체의 레퍼런스 정보가 필요함.
 - 프로그래밍에서 의존관계는 new로 표현된다.

### 의존성 주입이란
 - 객체의 실체를 외부 환경설정에서 컨트롤할 수 있도록 하는 것

### 의존성 주입을 사용하는 이유
 - 기능이 추가될 때 마다 코드의 변경을 최소화
 - 유지보수 및 테스트 측면에서 효율성 향상

### bean container
 - 스프링에서 의존관계들을 관리하는 컨테이너
 - 의존성 문제를 해결

### @RestController
 - Rest방식의 데이터 자체를 서비스로 제공
 - JSP저럼 View를 생성하는 것이 아닌 데이터 자체를 반환
 - ex) Json, xml, 문자열

### Rest방식
 - 웹에 존재하는 모든 자원의 고유한 uri부여

### YAML
 - 야믈
 - Yaml Ain't Markup Language
 - 모든 데이터를 리스트, 해쉬, 스칼라의 조합으로 적절히 표현할 수 있다는 믿음을 가지고 만들어 짐
 - 상대적으로 이해가 쉽고, 가독성이 좋음
 - XML의 특수기호를 사용하여 비슷함

### @Value
 - 프로퍼티의 키를 사용하여 특정한 값을 호출할 수 있음
 - 키를 정확히 입력해야하며 값이 없을 경우에 대해 예외 처리를 해주어야 함
 - 유일하게 spEL을 지원하여 매핑

### 메타데이터
  - 특정목적을 위해 만든 데이터
  - 데이터에 관한 구조화된 데이터로, 다른 데이터를 설명해주는 데이터

### POJO
  - Plain Old Java Object
  - 오래된 방식의 간단한 자바 오브젝트
  - 단순한 자바 객체

### Bean
  - 자바 객체
  - 컨테이너에 의해서 관리되고, 어플리케이션의 핵심을 이루는 객체를 beans라고 함
  - 스프링, IOC 컨테이너에 의해 인스턴스화 되어 조립되거나 관리되는 객체
  - 스프링 IOC컨테이너에 의해 관리되며 스프링이 제어권을 가지고 관계를 부여하는 객체
  - 스프링 컨테이너는 빈의 생성 주기, 관계, 사용등으 설정을 제어함

### IOC
  - 컨테이너는 개발자가 작성한 코드 컨트롤(객체의 생성과 소멸)을 대신 해줌

### Json
 - 데이터를 저장하는 포맷
 - 키와 값의 구조를 지키는 데이터 형식

### 어노테이션
 - 인터페이스를 기반으로한 어떠한 기능을 주입하는데에 사용되는 것

### H2
 - 자바로 작성된 인메모리 RDBMS

### @RunWith
  - JUnit에 내장된 러너를 사용하는 대신 어노테이션에 정의된 러너 클래스 사용
  - JUnit 프레임워크의 테스트 실행 방법을 확장할 때 사용하는 어노테이션

### JUnit
  - 자바의 대표적인 단위 테스트 프레임워크

### @SpringBootTest
 - 통합 테스트를 제공하는 기본적인 스프링 부트 테스트 어노테이션
 - 어플리케이션이 실행될 때의 설정을 임의로 바꾸어 테스트를 진행할 수 있다
 - 여러 단위 테스트를 하나의 통합된 테스트로 수행할 때 적합

### @RunWith
 - JUnit에 내장된 러너를 사용하는 대신 어노테이션에 정의된 러너 클래스를 사용

### @WebMvcTest
 - MVC를 위한 테스트
 - 웹 에서 테스트하기 힘든 컨트롤러를 테스트하는 데 적합
 - 웹 상에서 요청과 응답에 대해 테스트할 수 있다
 - 시큐리트 혹은 필터까지 자동으로 테스트하며 수동으로 추가/삭제까지 가능

### @DataJpaTest
 - JPA 관련 테스트 설정만 로드
 - 데이트소스의 설정이 정상적인지, JPA를 사용하여 데이터를 제대로 생성, 수정, 삭제하는지 등의 테스트가 가능
 - 내장형 데이터베이스를 사용하여 실제 데이터베이스를 사용하지 않고 테스트 DB로 테스트 가능
 - 인메모리 임베디드 데이터베이스 사용

### @RestClientTest
 - Rest관련 테스트를 도와줌
 - REST 통신의 데이터형으로 사용되는 JSON 형식이 예상대로 응답을 반환하는지 등을 테스트가

### @JsonTest
 - JSON의 직렬화와 역직렬화를 수행하는 라이브러리인 Gson과 Jackson API의 테스트를 제공
 - JSON 테스트는 크게 두가지로 나뉨
      1) 문자열로 나열된 JSON 데이터를 객체로 변환하여 변환된 객체값을 테스트
      2) 1번의 반대
 - JacksonTester 객체는 객체 변환과 관련된 다양한 API를 제공

### [MVC 패턴](https://github.com/ber01/Study-Spring-Boot/tree/master/keyword/MVC)

### [타임리프(Tymeleaf), 템플릿, 템플릿 엔진](https://github.com/rhkd4560/Study-SpringBoot/tree/master/Spring%204day/homework)

### [의존 라이브러리](https://github.com/dongh9508/Study-SpringBoot2/tree/master/keyword/LINK/dependency%20library)
 - Web
 - 타임리프
 - JPA
 - Devtools
 - Lombok
 - H2

### [각종 어노테이션 모음](https://github.com/etg6550/2019WinterProject/tree/master/Day4/HomeWork)
 - @Getter
 - @Id
 - @NoArgsConstructor
 - @Entity
 - @Column
 - @Builder
 - Serializable(직렬화)
 - @Table

### [각종 어노테이션 모음2](https://github.com/ber01/Study-Spring-Boot/tree/master/keyword/Annotation2)

### [스프링 부트 시큐리티, OAuth2](https://github.com/etg6550/2019WinterProject/tree/master/Day6)
 - 스프링 부트 시큐리티란?
 - OAuth2 인증 수행 방법
 - 권한 부여 코드 승인타입

### [각종 어노테이션 모음3](https://github.com/pdh6547/study-spring-boot/blob/master/Keyword/Homework/Annotaion%20and%20Interface.md)
 - @NestedConfigurationProperty
 - AuthorizationCodeResourceDetails
 - ResourceServerProperties
 - OAuth2 리소스 값
 - @Configuration
 - 동기, 비동기 통신

### [각종 어노테이션 모음4](https://github.com/hagome0/Study-Spring-Boot/tree/master/keyword/Annotaion%20and%20Interface2)
 - @EnableWebSecurity
 - WebSecurityConfigurerAdapter
 - HttpServletRequest
 - XFrameOptionsHeaderWriter
 - CharacterEncodingFilter
 - CsrfFilter

### [각종 어노테이션 모음5](https://github.com/woghd9072/study-spring-boot/tree/master/Keyword/Homework)
 - @EnableOAuth2Client
 - OAuth2ClientContext
 - BasicAuthenticationFilter
 - FilterRegistrationBean
 - Filter
 - CompositeFilter
 - OAuth2ClientAuthenticationProcessingFilter
 - OAuth2RestTemplate
 - UserInfoTokenService

### [p.138 ~ p.141 정리](https://github.com/mkshin96/study-spring-boot/blob/master/%EC%9A%A9%EC%96%B4%20%EC%A0%95%EB%A6%AC/p138~p141.md)

### [REST, RESTful, HATEOAS](https://github.com/mkshin96/study-spring-boot/blob/master/%EC%9A%A9%EC%96%B4%20%EC%A0%95%EB%A6%AC/REST.md)
