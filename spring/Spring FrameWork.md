# 스프링 프레임워크 란?
- 자바 플랫폼을 위한 오픈 소스 애플리케이션 프레임워크 
- 엔터프라이즈 애플리케이션 개발의 복잡성을 줄여주기 위한 목적으로 만들어짐

## 스프링 탄생 배경
- 기존의 EJB 개념이 어렵고 단점이 많다는 문제점이 부각되어 EJB를 사용하지 않고도 객체간 의존성 해결이 가능한 컨테이너를 개발했는데, 이것이 스프링의 시작이 되었음. 즉, 특정 기술에 종속되지 않고 객체를 관리할 수 있는 컨테이너를 제공하는 것이 스프링의 기본 철학.
## 프레임워크(FrameWork) 란? vs 라이브러리
- 프레임워크 : 뼈대, 기반 구조 / '특정 프로그램을 개발하기 위한 여러 요소들과 메뉴얼인 룰을 제공하는 프로그램'
- 라이브러리 : 도구의 모음 / '소프트웨어를 개발하기 쉽게 어떤 기능을 제공하는 도구들'

프레임워크를 가지고 프로그램을 만들기 시작하면 어떤 '규약'을 지키면서 만들어야한다. 하지만 라이브러리는 프레임워크의 규약을 지키면서 나머지 '자유'로운 부분은 어떠한 도구를 써도 무방함

### 스프링의 장점
- 경량 컨테이너 : 객체의 라이프 사이클 관리, Java EE 구현을 위한 다양한 API를 제공함
- DI, AOP, POJO를 지원 (이후 따로 정리)
- 다양한 API와의 연동 지원을 통한 Java EE 구현이 가능

### 스프링 프레임워크의 특징
- 경량 컨테이너로서 자바 객체를 직접 관리함, 각각의 객체 라이프 사이클을 관리하며 스프링으로부터 필요한 객체를 얻어올 수 있음
- POJO 방식의 프레임워크 : 특정한 인터페이스를 구현하거나 상속을 받을 필요가없어 기존에 존재하는 라이브러리 등을 지원하기에 용이하고 객체가 가벼움
- IOC 지원 : 컨트롤의 제어권이 아니라 프레임워크에 있어서 필요에 따라 스프링에서 사용자의 코드를 호출함
- DI 지원 : 각각의 계층이나 서비스들 간에 의존성이 존재할 경우 프레임워크가 서로 연결시켜줌
- AOP 지원 : 트랜잭션, 로깅 보안과 같이 여러 모듈에서 공통적으로 사용하는 기능의 경우 해당 기능을 분리하여 관리할 수 있음
- 영속성과 관련된 다양한 서비스를 지원
- 확장성이 높음

## 스프링 컨테이너
- 스프링 컨테이너는 특정 클래스를 상속하거나 인터페이스를 구현하지 않는 평범한 자바 클래스(POJO)를 이용하여 EJB의 기능은 유지하면서 복잡성을 제거하고, 객체들의 라이프사이클을 관리함
<img width="535" alt="스크린샷 2022-08-08 오후 11 22 15" src="https://user-images.githubusercontent.com/83891837/183440376-5a1d2684-2a6f-40e2-ac51-a6fe2b6ad104.png">

각 라이브러리의 객체들은 스프링 컨테이너에서 관리하기 때문에 사용법이 일관적임. 스프링 컨테이너는 여러 객체들이 모여있는 공장과 같은 개념. Bean Factory 또는 IOC Container 라고도 함
