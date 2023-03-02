# 컴퓨터 네트워크 소개
### 네트워크의 내부 구조
- 계층적 구조(Layered Architecture)
<br><br>

### 네트워크의 역사 (통신의 역사)
- 우편
- 봉화
- 전보
- 전화
<br><br>

### 컴퓨터 통신의 역사
- Network Edge(단말)
  - 예) 서버, 컴퓨터, 스마트폰
- Network Core
- lastmile
<br>![image](https://user-images.githubusercontent.com/101886039/222496108-e3bd99e8-ef54-41f1-b6f5-a3c7cd7bf163.png)
<br><br>

### Network Edge의 역사
- 기본 통신 수단 - 전화
  - Dial-up Modem
    - 전화선(음성 정보)을 그대로 이용해서 통신
    - 20Hz ~ 20,000Hz 대역폭을 가지지만 비용 문제로 보통의 음성정보만 잘 전달할 수 있을 정도의 대역폭을 제공(20,000Hz 이하)
    - Binary Data -> 가청 주파수 신호
      - 200bps ~ 9,600bps or 14,400bps
    - 전화를 걸어서 통신
    - 음성정보 = 데이터정보
    - Network Core = 전화망(전화가 오면 네트워크가 끊기고..)
  - DSL(Digital Subscriber Line)
    - 전화선을 통신선로로 사용
    - Last mile(마지막 1단계)만 전화선 사용
    - 즉, Network Core는 별도 존재
    - splitter 존재해서 전화국까지의 선은 공유하지만 전화가 오는 신호와 DSL에서 사용하는 신호에는 차이가 있음
    - 1~8Mbps 전송률
    - 비용은 줄이고 전송률은 더 극대화!
    - ![image](https://user-images.githubusercontent.com/101886039/222496223-d612cd4b-5040-405a-ac9c-0a84030c0c3b.png)
    - [DSL 더 알아보기](https://ko.wikipedia.org/wiki/%EB%94%94%EC%A7%80%ED%84%B8_%EA%B0%80%EC%9E%85%EC%9E%90_%ED%9A%8C%EC%84%A0)
    - dedicated channel(전용채널)
  - 케이블 모뎀
    - 케이블 TV 선로
    - 동축선
    - 데이터 양 많음
    - shared channel(공유채널)
- 사용자가 많아질수록 케이블모뎀이나 DSL으론 사용자의 요구를 전부 들어주기 힘들어서 나온 방식
  - FTTH(Fiber To The Home)
    - 집 앞까지 광케이블
    - 구리선을 이용해서 전기적 신호를 전송하는 것(대역폭 ↓, 설치 비용 ↓, 잡음에 취약)에서 광섬유를 이용해서 전자기파(가시광선) 전송
    - 대역폭 ↑
    - 단, 관리 및 설치 비용 ↑
    - 잡음 특성 우수
  - 코어망에서 개인용망으로 점점 옮겨오는 추세
- 기타 Last Mile 통신 기법
  - WIFI
    - 공유 채널
  - Ethernet
    - 전용선 사용
    - 보통 WIFI보다 빠름
  - 3G, LTE
    - 3G는 음성 최적화
    - LTE는 Data 최적화

<br>

### 통신선로의 종류
- 구리선
  - 예) 전화선(일반 pair선), Ethernet(Twisted pair선), 케이블 TV선(동축선)
- 광섬유
  - 단위 전송률의 가성비가 높음
- 무선(공기)
  - 잡음 ↑
  - 공유채널 

<br>

### 음성정보 vs 데이터정보
- 음성정보
  - Circuit Switching에 적합
  - 전화
- 데이터정보
  - Packet Switching에 적합
  - 인터넷

1. Circuit Switching
    - 시작과 끝이 명시적으로 구분
    - 꾸준히 정보가 전송
     - __통신의 시작에서 끝까지 통신을 위한 경로와 자원을 사전할당/독점__
     - 
2. Packet Switching
   - 시작과 끝이 모호
   - packet - 데이터 전송의 단위
   - 패킷마다 목적지 주소를 적어서 보내는 시스템

<br>

### 프로토콜
- 규약
- 계층적 규약 구조
- ISO/OSI 7계층 참고모델
  - 응용계층(카톡, 카페, 유튜브)
  - 표현계층(프레젠테이션 계층)(HTML)
  - 세션계층-응용.표현객체의 전달(HTTP)
  - 전송계층(Transport)-양 끝단 전송품질 보장
  - 네트워크계층-어떻게 네트워크 코어가 끝단간의 전송을 구현할 것인가?
  - 데이터링크계층-각 링크의 규약
- 인터넷 5계층
  - 응용계층(응용, 표현, 세션 계층을 하나로 묶음)
  - ...
