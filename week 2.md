# 컴퓨터 네트워크
[추가 정리](https://graceful-coriander-375.notion.site/week-2-f0cff7f4bfba49f58408cf30aa8a37a6)
### Circuit Switching
- 음성같은 데이터에 유리(꾸준한 데이터)

### Packet Switching
- 고장에 좀 더 자유로움

### 네트워크 품질 척도
- 속도
  - 대역폭(bandwidth)(=주파수 넓이)
    - 주파수 넓이는 전송률(data rate)과 비례
    - data rate(=through put) : Mb/s(Mbps)
    - 1MB/s(byte) = 8Mbps(8Mb/s)(bit)
    - end to end service quality에서 최소 quality가 나의 bandwidth 결정
- 신뢰도
  - packet loss
  - 잡음, 혼잡 등이 packet loss 발생시킴 -> 대역폭 ↓
- __지연시간__
  - 누적시간(통신을 할 떄 모든 지연시간의 합)
    - processing delay
      - 패킷의 정보를 처리하는데 드는 시간
      - 패킷 내 데이터의 에러 체크와 어디로 나가는지를 결정
      - 매우 짧은 시간동안만 발생
      - 라우터 내의 하드웨어 성능에 따라 결정되므로 가변적이지 않음
    - queueing delay
      - 전송을 위해 output link의 queue에서 기다리면서 발생하는 지연
      - 줄 서는데 드는 시간
      - 기술적으로 해결하기 가장 쉬운 지연시간
      - 병목현상 파악 후 자원을 조금 늘리면 해결
      - 라우터의 congestion(혼란) 정도가 결정하기 때문에 상황에 따라 가변적
    - transmission delay
      - queue를 빠져나가 라우터의 output link를 통해 빠져나가기 전까지 발생하는 delay
      - 즉, 전송하려는 패킷을 output link로 밀어내는데 걸리는 시간
      - 미디어의 패킷의 앞에서 끝까지 통과하는 시간
      - 전송률이 높아지면서 영향이 미미해짐
      - 패킷이 전송되는 link의 성능에 따라 갈리며 품질이 좋은 link를 사용할 경우 delay가 감소함
      - link의 bandwidth에 따라 결정되며 불변의 값이기 때문에 delay도 비교적 가변적이지 않음
    - propagation delay
      - 실제 link를 타고 데이터가 전송될 때 발생하는 delay
      - 물리적인 거리에 의한 지연
      - 거리와 link의 매체가 결정하고 다른 delay에 비해 매우 짧은 시간
    - [출처](https://ddongwon.tistory.com/70)

### 계층
- 분산된 시스템을 하나의 통합된 응용시스템으로 묶어주는 계층
- 예) 구글 검색 시스템, 종합 정보 시스템, 네이버 웹툰, lol ...
1. 애플리케이션 계층
   
2. presentation 계층
   - 분산된 응용의 표현 방법에 대한 규약
   - HTML(Hyper Text Markup Language)
   - UI
  
3. 세선(session layer)
   - 접속을 해서 접속이 끝날때까지 유지
   - 응용의 접속 및 통신의 방법과 관련된 규약
   - HTTP
   - 객체 교환

4. 전송(transport layer) - 비서 
   - 품질 보장
   - 신뢰성 품질 제공

5. 네트워크(network layer) - 우체국
   - 경로 설정
   - 네트워크 코어, swtich, 교환기?
   - 양 끝단으로의 전달
   - 패킷을 끝에서 끝으로 경로를 설정해서 전송할것인지

6. 링크(link layer)
   - 다음 단으로의 전달 책임
   - 패킷의 한 합의 전송을 책임지는 layer

7. 물리 계층 - 자동차, 도로 

<br>

### 응용 계층

카톡, 온라인 게임, 인터넷 브라우저 상의 응용, 메일...
