# Servlet

> Servlet은 Java로 작성된 서버측 프로그램으로, 웹 요청(주로 HTTP 요청)을 처리하고 동적으로 웹 페이지를 생성하거나 데이터를 반환하는 역할. 클라이언트와 서버 간의 Request-Response 모델을 구현

> 동적 웹 페이지를 만들 때 사용되는 Java 기반의 웹 애플리케이션 프로그래밍 기술

> 웹을 만들 때, Request와 Response에는 규칙이 존재하는데, 이러한 웹 요청과 응답의 흐름을 **간단한 메서드 호출만으로 체계적으로 다룰 수 있게 하는 기술**

---

## Servlet의 주요 특징

- 클라이언트의 Request에 대한 **동적으로 동작**하는 웹 애플리케이션 컴포넌트 (Servlet 이전에는 정적 웹)
- HTML을 사용해 응답반환
- Java의 스레드를 이용
- MVC 패턴에서 Controller로 이용
- HTML 변경 시 Servlet을 재 컴파일 해야함
- 플랫폼에 대해 독립적이며 Java 기반으로 Java 언어의 장점을 활용
- HTTP 프로토콜 지원
- Servlet 컨테이너(ex. Tomcat)가 객체 생명주기를 관리하며, 메모리 및 스레드 관리를 지원함

---

## Servlet 동작 원리

1. 클라이언트가 웹 브라우저를 통해 HTTP 요청을 전송
2. 웹 서버는 요청을 Servlet 컨테이너로 전달
3. 컨테이너는 요청에 매핑된 적절한 Servlet 클래스를 실행
4. Servlet의 service() 메서드는 요청을 doGet() 또는 doPost()와 같은 메서드로 전달하여 처리
5. 처리 결과를 HTTP 응답 형태로 클라이언트에게 반환

---

## Servlet의 장단점

- 장점
  - 플랫폼 독립적이고 안정적
  - 멀티쓰레드를 지원하여 효율적인 요청 처리가 가능
  - JSP와 연동 가능
- 단점
  - 복잡한 HTML 생성을 위한 코드 작성이 어려움
    - 때문에 JSP와 함께 사용됨
  - MVC 구조를 명확히 하기 위해 보완기술이 필요함

---

### 추가

#### JSP와의 차이점

- Servlet은 Java 코드로 HTML을 생성하는 반면, JSP는 HTML 내에 Java 코드를 삽입하여 동작함

- 일반적으로 JSP는 프레젠테이션 레이어, Servlet은 비지니스 로직과 컨트롤러 역할을 담당
