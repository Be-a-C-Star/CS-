# API

**API(Application Programming Interface)** 란 둘 이상의 컴퓨터 프로그램이 서로 통신하는 방법이자 그 사이에 있는 중계 계층을 의미한다. 서버와 클라이언트 뿐만 아니라 서버와 서버 사이의 통신에서도 사용되는 인터페이스이다. 특정 작업을 수행하거나, 데이터를 교환하는 데 사용되며, 여러 시스템 간의 통합 및 상호 운용성을 높이는 데 중요한 역할을 한다.

흔히 레스토랑을 예시로 드는데, 손님이 요리를 직원에게 주문하고, 직원은 쉐프에게 요청된 주문을 전달한다. 이후 쉐프는 요청이 들어온 음식을 만들어 직원에게 전달하면 직원은 손님에게 배송한다. 여기서 음식 서빙을 담당한 직원을 API로 볼 수 있으며, 손님은 서비스의 사용자, 쉐프는 서비스의 프로그램(서버)으로 생각할 수 있다. 손님은 주방에서 요리가 어떻게 만들어지는 지 알 필요가 있을까? 손님은 그저 요리를 주문하는 방법만 안다면, 주문 후엔 완성된 요리를 즐기면 그만이다. 이처럼 API에서도 사용자는 API를 통해 요청하는 방법만 안다면, 해당 API를 통해 받을 수 있는 응답(데이터 등)은 어떻게 저장되고 만들어지는지 몰라도 된다.

### Interface

인터페이스(Interface)는 컴퓨터를 공부하는 사람이라면 많이 들어볼 수 있고, 사용되는 단어이다. 서로 다른 두 개의 시스템, 장치 사이에서 정보나 신호를 주고받고 어떠한 조작을 할 수 있는 경계면 혹은 환경을 뜻한다. 이를 통해 해당 컴퓨터의 내부서버가 어떻게 구현되어있는지는 상관없이 인터페이스를 통해 통신 등이 가능하다. API 외에 다른 인터페이스를 예로 들면 흔히 컴퓨터 화면에서 마우스를 이용해 아이콘을 더블 클릭하여 실행하고, 드래그 앤 드랍으로 위치를 바꾸는 등의 행동은 GUI(Graphical User Interface)환경이라 가능하고 터미널(혹은 cmd)에서 명령어를 통해 컴퓨터를 조작하는 것은 CLI(Command-Line Interface)라고 부른다. 이 뿐만 아니라 인터페이스는 다양한 곳에서 많이 사용되는 용어 중 하나이다.

## 장점

- 보안성
  - 제공자는 서비스의 중요한 부분을 드러내지 않아도 되며 필요한 권한을 가진 애플리케이션만 접근할 수 있도록 설정할 수 있다. ex) DB 설계 구조, 서버의 상수값 등
- 캡슐화
  - 사용자는 어떻게 구현되는지 알 필요없이 필요한 정보만 받을 수 있다.
  - 내부 프로세스가 수정되더라도 API는 변경되지 않기 때문에 매번 사용자가 앱을 업데이트하는 상황을 줄일 수 있다.
- 재사용성, 효율성
  - 한 번 개발된 API는 여러 애플리케이션에서 재사용할 수 있어 유지 보수 및 확장이 용이하다.
  - OPEN API를 사용하면 코드의 중복을 줄이고, 복잡한 기능을 쉽게 구현할 수 있다. 다른 시스템에서 이미 만들어진 기능을 호출하여 사용할 수 있기 때문에 개발 속도가 빨라진다.
- 독립성
  - 플랫폼에 구애받지 않고 다양한 언어나 환경에서 사용할 수 있다. 예를 들어, REST API는 클라이언트가 어떤 언어로 작성되었든 HTTP 요청을 통해 통신할 수 있다.
- 자동화 기능
  - 제공자는 데이터를 한곳에 모을 수 있다. 예를 들어 어떤 특정한 것을 클릭하는 사용자에 대한 이벤트를 집계하고 싶을 때, 해당 API를 만들고 해당 이벤트가 발생하면 해당 API를 호출하게 만들면 해당 데이터를 한 곳에 모을 수 있다. ex) yes24의 베스트셀러, 검색페이지에서의 사용자이벤트
  - API를 통해 수작업 없이 시스템 간 데이터를 교환하고 작업을 자동화할 수 있다.

## API 종류

API는 여러 종류가 있고 접근 허용 범위와 사용 목적에 따라 private과 public으로 나눌 수 있다.

### Public API (OPEN API)

Public API는 모든 개발자나 외부 사용자에게 공개된 API이다. 누구나 접근하고 사용할 수 있는 것이 특징이며, 주로 개발자 커뮤니티나 외부 비즈니스 파트너와의 협업을 위해 제공된다.
ex) 구글 맵스 API, 트위터 API, 페이스북 Graph API 등

#### 사용 목적

- 외부 개발자들이 해당 서비스를 통합할 수 있도록 지원.
- API를 통해 외부 생태계를 형성하고, 더 많은 사용자나 파트너를 끌어들이는 목적.
- 외부 개발자들이 API를 활용해 다양한 애플리케이션이나 서비스를 개발하도록 유도.

#### 일반적으로 사용되는 API 종류

- REST API
  - 가장 널리 사용되는 Public API 방식으로 HTTP 기반으로 쉽게 접근 가능하며, 플랫폼에 독립적이어서 다양한 외부 시스템과 쉽게 연동된다.
- GraphQL
  - 데이터 최적화와 성능 개선이 필요한 경우, 특히 클라이언트가 원하는 데이터만 선택적으로 가져갈 수 있는 기능이 필요할 때 사용된다.
- SOAP
  - 금융, 정부, 대형 기관에서 보안이 중요한 환경에서 사용되는 API.

### Private API

Private API는 조직 내부에서만 사용되는 API로서 외부에는 공개되지 않고, 특정 조직이나 팀의 시스템 간의 통합, 자동화, 또는 내부 애플리케이션을 지원하는 목적으로 사용된다. 외부와의 통신보다 내부 시스템 간의 효율성을 높이고 보안을 유지하는 데 중점을 둔다.
ex) 조직 내의 사용자 관리 시스템과 회계 시스템을 연결하는 API, 내부 애플리케이션 간 데이터 처리 자동화를 위한 API 등

#### 사용 목적

- 기업 내부의 애플리케이션이나 서비스 간 데이터를 주고받거나 통합할 때
- 외부에 노출되지 않으며, 내부의 보안 정책을 준수하여 중요한 데이터를 보호
- 조직 내부에서 효율적인 데이터 처리 및 기능 호출을 위해 사용

#### 일반적으로 사용되는 API 종류

- REST API
  - Private API에서도 자주 사용되며, 특히 경량화된 통신이 필요할 때 유용하다.
- gRPC
  - 빠른 통신이 필요하거나, 내부 시스템 간에 매우 효율적인 바이너리 데이터 전송이 필요한 경우 주로 사용된다.
- SOAP
  - 보안과 신뢰성 요구가 높은 대기업의 내부 시스템 통합에서 여전히 사용된다.
- WebSocket
  - 실시간 데이터 처리가 필요한 내부 애플리케이션 간 통신에 사용된다.
