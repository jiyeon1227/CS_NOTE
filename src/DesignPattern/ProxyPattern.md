❓**프록시 패턴이란?**

❗프록시 패턴(proxy pattern)은 대상 객체에 접근하기 전 그 접근에 대한 흐름을 가로채 대상 객체 앞단의 인터페이스 역할을 하는 디자인 패턴. 이를 통해 객체의 속성, 변환 등을 보완하며 보안, 데이터 검증, 캐싱, 로깅에 사용

> - 보안(Security): 프록시는 클라이언트가 작업을 수행할 수 있는 권한이 있는지 확인하고 검사 결과가 긍정적인 경우에만 요청을 대상으로 전달한다.
> - 캐싱(Caching): 프록시가 내부 캐시를 유지하여 데이터가 캐시에 아직 존재하지 않는 경우에만 대상에서 작업이 실행되도록 한다.
> - 데이터 유효성 검사(Data validation): 프록시가 입력을 대상으로 전달하기 전에 유효성을 검사한다.
> - 지연 초기화(Lazy initialization): 대상의 생성 비용이 비싸다면 프록시는 그것을 필요로 할때까지 연기할 수 있다.
> - 로깅(Logging): 프록시는 메소드 호출과 상대 매개 변수를 인터셉트하고 이를 기록한다.
> - 원격 객체(Remote objects): 프록시는 원격 위치에 있는 객체를 가져와서 로컬처럼 보이게 할 수 있다.

❓**프록시 객체란?**

❗프록시(proxy)객체는 어떠한 대상의 기본적인 동작(속성 접근, 할당, 순회, 열거, 함수 호출 등)의 작업을 가로팰 수 있는 객체

❗프록시 객체는 프록시 패턴이 녹아들어있는 객체

❓**프록시 서버란?**

❗프록시 서버는 서버와 클라이언트 사이에서 클라이언트가 자신을 통해 다른 네트워크 서비스에 간접적으로 접속할 수 있게 해주는 컴퓨터 시스템이나 응용 프로그램

✏️프록시 서버로 쓰는 nginx

nginx는 비동기 이벤트기반의 구조와 다수의 연결을 효과적으로 처리 가능한 웹 서버. 주로 node.js서버 앞단의 프록시 서버로 활용됨 이를 통해 익명 사용자가 직접적으로 서버에 접근하는 것을 차단하고, 간접적으로 한 단계를 더 거치게 만들어 보안을 강화할 수 있음

✏️프록시 서버로 쓰이는 CloudFlare

CloudFlare는 전 세계적으로 분산된 서버가 있고 이를 통해 어떠한 시스템의 콘텐츠 전달을 빠르게 할 수 있는 CDN서비스.CloudFlare는 웹서버 앞단에 프록시 서버로 두어 DDOS공격 방어나 HTTPS구축에 쓰임. 또한, CloudFlare는 의심스러운 트레픽인지 먼저 판단에 일정부분 막아주는 역할도함

> DDOS(Distributed Denial od Service attack)
개념 : 특정 서버(컴퓨터)나 네트워크 장비를 대상으로 많은 데이터를 발생시켜 장애를 일으킴 → 가용성 저하