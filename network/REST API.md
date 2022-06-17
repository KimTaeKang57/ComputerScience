# REST API (Representational State Transfer API)
- REST API란 REST를 기반으로 만들어진 API를 의미합니다. 

### REST 란 ? (Representational State Transfer)
- 자원을 이름으로 구분하여 해당 자원의 상태를 주고받는 모든 것. 즉, 자원의 표현에 의한 상태 전달

A. 자원(Resource)의 표현(representation)
- 자원 : 해당 소프트웨어가 관리하는 모든 것 (ex : 문서 그림 데이터 해당 소프트웨어 그 자체 등)
- 자원의 표현 : 그 자원을 표현하기 위한 이름 
B. 상태(정보) 전달
- 데이터가 요청되어지는 시점에서 자원의 상태(정보)를 전달한다. JSON 혹은 XML를 통해 데이터를 주고 받는 것이 일반적이다.

1. HTTP URI를 통해 자원(Resource)을 명시하고
2. HTTP Method(POST, GET, PUT, DELETE 등)를 통해
3. 해당 자원(URI)에 대한 CRUD Operation을 적용하는 것을 의미합니다.
즉, REST는 자원 기반의 구조 설계의 중심에 자원이 있고 HTTP Method를 통해 Resource를 처리하도록 설계된 아키텍처를 의미한다.
웹 사이트의 이미지, 텍스트, DB 내용 등의 모든 자원에 고유한 ID인 HTTP URl를 부여한다.

### CRUD Operation이란
- CRUD는 대부분의 컴퓨터 소프트웨어가 가지는 기본적인 데이터 처리 기능인 Create(생성), Read(읽기), Update(갱신), Delete(삭제)를 묶어서 일컫는 말로

Create : 데이터 생성(POST)
Read : 데이터 조회(GET)
Update : 데이터 수정(PUT)
Delete : 데이터 삭제(DELETE)
로 동작한다.

### REST 구성 요소
1. 자원(Resource) : HTTP URI
- Client는 URI를 이용하여 자원을 지정하고 해당 자원의 상태(정보)에 대한 조작을 Server에 요청한다.
2. 자원에 대한 행위(Verb) : HTTP Method
- HTTP Method
3. 자원에 대한 행위의 내용(Representations) : HTTP Message Pay Load
- JSON 혹은 XML

### REST의 특징
1. Server-client 구조
2. Stateless(무상태)
3. Cacheable(캐시 처리 가능)
4. Layered System(계층화) : REST Server는 다중 계층으로 구성될 수 있다. API Server는 순수 비즈니스 로직을 수행하고 그 앞단에 보안, 로드밸런싱, 암호화, 사용자 인증 등을 추가하여 구조상의 유연성을 줄 수 있다.
5. Uniform Intergace(인터페이스 일관성)

# REST API 란?
- REST 기반으로 서비스 API를 구현하는 것
- 
### API 란?
- API란 클라이언트가 리소스를 요청할 수 있도록 서버측에서 제공된 인터페이스를 말한다. 이러한 API로 데이터와 기능의 집합을 제공하여 컴퓨터 프로그램간 상호작용을 촉진하며, 서로 정보를 교환가능 하도록 한다.
- 
1. URI는 동사보다는 명사를, 대문자보다는 소문자를 사용해야함
2. 마지막에 슬래시를 포함하지 않음 (/)
3. 언더바 대신 하이픈을 사용
4. 파일확장자는 URI에 포함 x
5. 행위를 포함하지 않음 (ex : ../delete-post/1 -> ../post/1
와 같은 규칙을 지켜야 한다.

# REST ful 이란?
- REST FUL 이란 REST의 원리를 따르는 시스템을 의미한다. REST API의 설계규칙을 올바르게 지킨 시스템을 REST FUL하다 말할 수 있으며, 모든 CRUD 기능을 POST로 처리 하는 API 혹은 URI 규칙을 올바르게 지키지 않은 API는 REST API의 설계 규칙을 올바르게 지키지 못한 시스템은 REST API를 사용하였지만 REST FUL 하지 못한 시스템이라고 할 수 있습니다.
