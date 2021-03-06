# NGSI-LD(Linked Data)

## Linked Data 란 

**웹에서 기계가 읽을 수 있는 연결된 데이터를 공유하기 위한 일련의 설계 원칙**

**서로 다른 소스에서 오는 방대한 데이터 세트를 처리하고 이를 Open Data에 연결할 수 있어 지식 검색과 효율적인 데이터 기반 분석이 향상된다**

보통 우리가 사용하는 웹사이트에는 우리가 access 할 수 있는 많은 데이터가 있다.

그리고 웹사이트의 정말 멋진 점 중 하나는 데이터를 외부에 배치하여 우리가 쉽게 얻을 수 있다는 것이다.

웹을 통해 텍스트와 차트를 혼합할 수 있고 한 문서에서 다른 문서로 링크할 수 도 있다.

인터넷의 모든 사용자는 한 웹 페이지의 링크가 알려진 위치에서 다른 페이지를 로드하도록 브라우저를 안내할 수 있는 방식인 하이퍼 텍스트 링크의 개념에 익숙할 것이다.

우리는 관계 발견 가능성과 링크 작동 방식을 이해할 수 있지만 컴퓨터는 이를 훨씬 더 어렵게 여기며 별도의 위치에 있는 한 데이터 요소에서 다른 데이터 요소로 이동할 수 있도록 잘 정의된 프로토콜이 필요하다.

컴퓨터는 웹페이지를 가져와서 해체를 하는데 페이지에서 작은 비트와 바이트를  가져와  컴퓨터가 이해할 수 있는 방식으로 패키지화를 시킨다.

여기서 우리가 할 일은 페이지의 데이터 조각을 가져와 패키지화 시켜 컴퓨터가 이해할 수 있도록 돕는 것이다.

링



![](https://velog.velcdn.com/images/shkim11997/post/5d6ce2b6-11cf-437c-a534-5c00ed1df44e/image.png)

오늘날 웹에서 데이터를 표현하는  가장 좋은 방법

![](https://velog.velcdn.com/images/shkim11997/post/b3433dd7-e183-46f2-939e-1b7d9acb7d12/image.png)

하지만 여기서 웹에 있는 이질적인 정보를 함께 연결하는데 사용하는 방법 중 제일 좋은 것은 웹에서 기계가 이해할 수 있도록 컴퓨터에 데이터를 표한하는 가장  쉬운 방법은 `속성`과 `값` 메커니즘이다.

 ![](https://velog.velcdn.com/images/shkim11997/post/d625d453-e15b-4775-b7cc-16b06dfa6208/image.png)

## Linked Data 규칙

사물, 사건, 사람, 위치 등이 더 많이 연결될수록 데이터 웹은 더 강력해진다, 그러나 서로 다른 소스의 방대한 데이터 세트를 연결, 병합 및 통합하려면 몇 가지 기본 지침을 따라야 한다.

`World Wide Web의 발명가이자 Semantic Web 및 Linked Data의 창시자이자 옹호자인 Tim Berners-Lee 경은 이미 2006년에 Linked Data의 4가지 설계 원칙을 제시했다.`

1. URI를 사물의 이름으로 사용

   >URI(Uniform Resource Identifier)는 웹에서 사용할 수 있는 디지털 콘텐츠에서 실제 개체 및 추상 개념에 이르기까지 모든 것에 고유한 이름을 부여하는 데 사용되는 단일 글로벌 식별 시스템입니다. URI의 도움으로 우리는 서로 다른 것들을 구별하거나 한 데이터세트의 한 항목이 다른 데이터세트의 다른 항목과 동일하다는 것을 알 수 있다

2. HTTP URI 사용

   >HTTP 프로토콜은 리소스 검색을 위한 간단한 메커니즘을 제공하므로 이 프로토콜과 함께 URI로 사물을 식별할 수 있으면 더 쉽게 찾을 수 있습니다. 이렇게 하면 모든 종류의 데이터를 신속하게 게시하고 전역 데이터 공간에 추가할 수 있다

3. 누군가가 URI를 찾을 때 표준(RDF,SPARQL)을 사용

   >URI를 효율적으로 사용하려면 쿼리에 [RDF](https://www.ontotext.com/knowledgehub/fundamentals/what-is-rdf-triplestore/) 또는 [SPARQL](https://www.ontotext.com/knowledgehub/fundamentals/what-is-sparql/) 을 사용해야 한다.

   > [RDF는 W3C](https://www.w3.org/) 에서 개발한 웹상의 데이터 게시 및 교환을 위한 그래프 기반 표현 형식입니다 . [또한 시맨틱 그래프 데이터베이스( RDF triplestore](https://www.ontotext.com/knowledgehub/fundamentals/what-is-rdf-triplestore/) 라고도 함)에도 사용됩니다. 이는 상호 연결된 데이터를 저장하고 기존 데이터에서 새로운 사실을 추론하기 위해 개발된 기술입니다.
   >
   > 반면에 SPARQL은 RDF 형식으로 저장된 데이터를 검색하고 조작하기 위한 W3C 표준화 쿼리 언어입니다. 따라서 데이터 웹(또는 모든 데이터베이스)을 검색하고 관계를 발견할 수 있습니다.

4. URI에 대한 링크를 포함

   >하이퍼텍스트 웹과 유사하게 다른 URI에 대한 링크는 데이터를 상호 연결하고 다른 것을 찾을 수 있도록 합니다. 새로운 정보를 기존 리소스와 상호 연결함으로써 기존 데이터 간의 재사용 및 상호 연결을 극대화하고 기계 처리 가능한 의미의 풍부하게 상호 연결된 네트워크를 만든다

## Linked Data 개발절차

### 준비단계 

* 현황조사
* 구책대상선정
* 계획수립
* 실행계획
* 원천데이터준비
* 원천데이터백업

### 구축 및 발행단계

* 명세화
* 용어설계
* 온톨리지 설계
* 데이터변환(RDF화)
* 저장 및 발행
* 등록

---

컴퓨터에서 읽을 수 있는 링크 시스템을 만들려면 잘 정의된 `데이터 형식(JSON-LD)` 을 사용하고 데이터 엔티티와 엔티티 간의 관계에 대해 고유한 `ID(URL 또는 URN)` 를 할당해야 한다.





# 출처

https://documenter.getpostman.com/view/513743/SVYjSMgh
