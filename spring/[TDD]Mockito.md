# Mockito란?
Mockito는 개발자가 동작을 직접 제어할 수 있는 가짜(Mock) 객체를 지원하는 테스트 프레임워크이다. 일반적으로 Spring으로 웹 애플리케이션을 개발하면, 여러 객체들 간의 의존성이 생긴다. 이러한 의존성은 단위 테스트 작성을 어렵게 만드는데, 이를 해결하기 위해 가짜 객체를 주입시켜주는 Mockito 라이브러리를 활용할 수 있다. Mockito를 활용하면 가짜 객체에 원하는 결과를 Stub하여 단위 테스트를 진행할 수 있다.

물론 Mock을 하지 않아도 된다면 하지 않는 것이 가장 좋다.

 

## Mockito 사용법
1. Mock 객체 의존성 주입
Mockito에서 Mock(가짜) 객체의 의존성 주입을 위해서는 3가지 어노테이션이 사용된다
- @Mock: Mock 객체를 만들어 반환해주는 어노테이션
- @Spy: Stub하지 않은 메소드들은 원본 메소드 그대로 사용하는 어노테이션
- @InjectMocks: @Mock 또는 @Spy로 생성된 가짜 객체를 자동으로 주입시켜주는 어노테이션


예를 들어 UserController에 대한 단위 테스트를 작성하고자 할 때, UserService를 사용하고 있다면 @Mock 어노테이션을 통해 가짜 UserService를 만들고, @injectMocks를 통해 UserController에 이를 주입시킬 수 있다.

 

2. Stub로 결과 처리

의존성이 있는 객체는 가짜 객체(Mock Object)를 주입하여 어떤 결과를 반환하라고 정해진 답변을 준비시켜야 한다. Mockito에서는 다음 메소드를 제공한다.

- doReturn(): Mock 객체가 특정한 값을 반환해야 하는 경우
- doNothing(): Mock 객체가 아무 것도 반환하지 않는 경우(void)
- doThrow(): Mock 객체가 예외를 발생시키는 경우

 

3. Mockito와 Junit의 결합

Mockito도 테스팅 프레임워크이기 때문에 JUnit과 결합되기 위해서는 별도의 작업이 필요하다. @ExtendWith(MockitoExtension.class)를 사용해야 결합이 가능하다.
