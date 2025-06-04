# MVC Life cycle

Spring MVC: Model-View-Controller 아키텍쳐를 구현한 Java 웹 프레임워크입니다.

라이프사이클:

1. 클라이언트 요청: 사용자가 웹 브라우저에서 URL을 요청합니다.
2. DispatcherServlet: 모든 요청은 프론트 컨트롤러인 DispatcherServlet에 의해 처리됩니다. DispatcherServlet은 Spring MVC의 핵심 요소로, 요청을 적절한 컨트롤러에 전달하는 역할을 합니다.
3. 핸들러 매핑(Handler Mapping): DispatcherServlet은 HandlerMapping을 통해 요청 URL에 매핑된 적절한 컨트롤러를 찾습니다.
4. 핸들러 어댑터(Handler Adapter): 선택된 컨트롤러를 실행하기 위한 적절한 어댑터를 선택
5. 컨트롤러(Contoller): 비즈니스 로직을 처리하고 결과 데이터(Model)와 뷰 이름(View Name)을 반환합니다.
6. 뷰 리졸버(View Resolver): 컨트롤러가 반환한 뷰 이름을 기반으로 실제 뷰를 찾습니다.
7. 뷰(View): 모델 데이터를 사용하여 HTML 등의 형태로 클라이언트에게 보여줄 결과를 생성합니다.
8. 응답: 최종적으로 생성된 뷰가 클라이언트에게 응답으로 전송됩니다.

REST API 서버에서는 View 부분이 템플릿 엔진을 통한 HTML 렌더링이 아닌 데이터 직렬화(serialization)로 대체된다는 점이 큰 차이점. 이런 방식을 종종 “헤드리스(Headless) MVC”라고도 부릅니다.
