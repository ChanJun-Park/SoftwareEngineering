# Chapter08 Understanding Requirements

## Requirements Engineering

소프트웨어 솔루션에 대해서 sponser, developer, user의 요구사항을 공학적으로 분석하는 것. 공학적으로 접근한다는 것은 비즈니스의 가치를 두고 분석한다는 뜻이다. 다음의 7단계가 있다.

- **Inception**(개시) : 다음과 같은 질문들에 답해본다.
  - basic understanding of the problem. problem은 stakeholder 의 요구사항.
  - 해당 solution을 사용할 사람들
  - 요구되어지는 소프트웨어의 본질(기능, 작동 방식, 메뉴얼)
  - sponser, developer, user 사이의 communtication과 collaboration에 대한 효과성
- **Elicitation**(끌어내기) : 모든 stakeholder로부터 구체적인 요구사항을 끌어낸다.
- **Elaboration**(퇴고) : data, function, behavioral requirements를 반영하는 analysis model을 만든다
- **Negotiation**(협상) : developer와 customer 사이에서 현실적인 실행 가능 시스템에 대한 동의를 한다
- **Sepcification**(명세화)
  - A written document
  - A set of models
  - A formal mathematical
  - A collection of user scenarios(use-cases)
  - A prototype
- **Validation**(확인) : 다음과 같은 것들을 살펴보는 review 과정
  - 내용이나 해석상의 오류
  - 명확히 해야하는 분야가 있을 수 있음
  - 빠진 정보
  - 비일관성 (비일관성은 매우 큰 제품이나 시스템을 만들 경우 가장 문제가 되는 요인이다.)
  - 서로 상충되거나 비현실적인 요구사항들
- **Requirements management** : 요구사항이 충실히 수행되는지 관리하는 것

### Inception(개시)

- Indentify stakholders
- 여러 관점을 인식한다.
- 협업을 위해서 일한다.
- 첫번째로 질문해볼 문제들
  - 요구사항을 제시하는 사람들이 누구인가?
  - 실제로 솔루션을 사용할 사람들은 누구인가?
  - 솔루션을 통해 이익을 얻는 사람은 누구인가
  - 솔루션을 위해서 다른 source가 필요한가?

### Eliciting Requirements

- 소프트웨어 엔지니어, customer가 참석하는 미팅을 실행
- 참석과 준비를 위한 규칙이 정해진다.
- agenda가 제시된다.
- 전반적인 조정자(facilitator)가 있어서 미팅을 주선하고, 이를 조율할 수 있다.
- key가 되는 요구사항을 선출하기 위해서 definition mechanism(flow chart, work sheet, electronic bulletin board 등등)이 사용된다.
- 이 과정의 목표는
  - 문제를 인식하고
  - 솔루션의 요소들을 제안하고
  - 다른 접근들간에서 협상하며
  - 솔루션 요구사항에 대한 예비 집합을 명세한다.

### Elicitation Work Products

Elicitation 과정에서 생성하는 작업산출물?

- a statement of nead and feasibility : 요구사항의 필요성, 구현 가능성에 대한 명세
- a bounded statement of scope for the system or product : 시스템 또는 제품의 범위에 대한 제한된 명세
- a list of customers, users, and other stakeholders who participated in requirements elicitation : 요구사항 도출에 참여하는 당사자들의 리스트를 작성한다.
- a description of the system's technical environment : 시스템의 기술적 환경을 서술한다.
- a list of requirements and the domain constraints that apply to each : 요구사항의 리스트들과 도메인에서의 제약사항(보안)들을 서술한다.
- a set of usage scenarios that provide insight into the use of the system or product under different operating conditions : 다양한 조건에서 사용되는 시스템 또는 제품에 대한 통찰을 제공하는 사용 시나리오 작성
- any prototypes developed to better define requirements : 요구사항을 더 정확이 정의하기 위해 프로토타입도 만들 수 있다.

### Quality Function Deployment

위 요구사항에 따라서 analysis model을 생성한다. 이 analysis model의 최종 목표는 소프트웨어의 품질을 보장하는 것이다. 소프트웨어의 가치는 사용자에 의해서 인식된다.

- Function deployment determines the "value" of each function required of the system
- Information deployment identifies data objects end events
- Task deployment examines the behavior of the system
- Value analysis determines the relative priority of requirements

### Use-Cases

한 시스템의 사용에 대한 스레드를 설명하는 사용자 시나리오의 collection 이다. 각 시나리오는 시스템과 상호작용하는 actor - 사람 또는 device의 관점으로 묘사된다. 각각의 시나리오는 다음과 같은 질문들에 대한 대답으로 생각 할 수 있다.

- 누가 main actor이고 누가 secondary actor인가
- actor의 goal은 무엇인가
- 모든 story가 시작하기 전의 사전 조건은 무엇인가
- main task나 functions 이 actor에 의해서 실행되는가
- story가 described 될때 어떤 확장이 가능한가
- actor의 행동에 어떤 variation이 가능한가
- actor는 어떤 system information을 획득하거나, 생산하거나 교환하는가
- actor가 외부 환경에 대한 변화를 시스템에 알려주어야 하는가
- actor는 system으로 부터 어떤 정보를 요구하는가
- actor는 unexpected change 에 대한 정보를 받기를 원하는가

### Building the Analysis Model

Analysis Model의 여러가지 요소들이 존재한다.

- **Scenario-based elements** : 어떻게 사용할 것인지에 대한 설명 위주
  - Functional : 소프트웨어 function의 processing, 사용법(입력, 출력)에 대한 설명 위주
  - Use-case : actor와 system간의 상호작용 묘사 위주. 구체적인 구현은 다루지 않음
- **Class-based elements** : 누가 기능을 수행하는가 위주
- **Behavioral elements** : 무엇을 한 것인가를 중점적으로 설명
  - state diagram
- **Flow-oriented elements**
  - Data flow diagram : data에는 2가지 종류가 있음(data, instruction). 모든 일이 하나의 장소(single machine)에서 실행될 필요가 없다.

### Negotiating Requirements

- key가 되는 stakeholder를 파악한다. 이들이 negotiation에 참여하는 사람들이다.
- 각 stakeholder의 win condition(승리 조건)을 파악한다. 이러한 승리 조건은 명확하게 나타나지 않을 수 있다.
- Negotiate : win-win 이 되도록 이끄는 요구사항을 도출하기 위해서 협상한다.

### Requirements Monitoring

한 순간에 이루어지는 것이 아니라 시간이 지나감에 따라서 계속해서 수행해야 하는 과정이다. 특별히 incremental development에 필요한 작업이다.

- Distributed debugging : 에러를 발견하고 원인을 파악한다. 프로그래밍 상의 버그가 아니라 analysis 상의 오류를 말한다.
- Run-time verification : 소프트웨어가 그것의 명세와 일치하게 동작하는지 확인한다.
- Run-time validation : 점차 진화하는 소프트웨어가 사용자의 요구를 만족시키는지, 전체적인 목적에 부합하는지 평가한다.
- Business activity monitoring : 시스템이 비즈니스 목적을 만족시키는지 평가한다.
- Evolution and codesign : 시스템이 진화함에 따라 stakeholder들에게 정보를 제공한다. 함께 디자인하고 발전시켜나간다.

### Validating Requirements

절대적인 가치가 아니라 상대적인 가치

- 각각의 요구사항이 시스템/제품의 전반적인 목적에 부합하는가?
- 모든 요구사항이 적당한 추상화를 통해서 명세되었는가?
- 그 요구사항이 정말로 필요한가? 아니면 전반적인 목적에 비추어 봤을때 본질적이지 않은 추가적인 기능인가?
- 모든 요구사항이 bounded 되어있고 모호하지 않게 정의되었는가?
- 다른 요구사항과 충돌하는 요구사항이 존재하는가?
- 등등...
