## 01 CPU와 메모리 

1. 컴퓨터의 구성
- 푸드트럭의 구성
- 컴퓨터의 구성
  - 컴퓨터가 이해하는 정보 : 데이터, 명령어
  - 컴퓨터의 네 가지 핵심 부품 : CPU, 메모리, 보조기억장치, 입출력장치 

2. 입출력 장치
- (주문서) 입력 장치 : 키보드 마우스 > 컴퓨터에게 명령을 요청하거나 데이터를 입력 
- (메뉴판, 음식수령대) 출력 장치 : 모니터 > 사용자에게 데이터를 보여주거나 처리결과를 보여주는 창구 

3. CPU : (요리사가 레시피에 따라 음식을 제작) 사용자의 명령에 대한 작업을 수행하는 처리장치
- CPU의 구성
  - ALU(우뇌, 산술논리 연산장치) : 비교, 판단 연산을 담당
  - CU(좌뇌, 제어부)와 내부버스 : 레시피 순서대로 스케줄을 제어부를 담당, CPU를 내부적으로 제어(각 장치를 연결)
  - 메모리 유닛(레지스터 "처리할 명령어를 저장", 캐시 메모리(L1) "왼손은 거들뿐, 처리속도를 높여줍니다, 부스터")
    - 레지스터
      - 메모리주소 레지스터 : 주기억장치의 주소를 저장
      - 프로그램 카운터 : 다음에 수행할 명령어의 주소를 저장
      - 명령어 레지스터 : 현재 실행 중인 명령어를 저장
      - 메모리 버퍼 레지스터 : 주기억장차에서 읽어온 데이터나 저장할 데이터를 임시로 저장
      - 누산기 : 연산 결과를 임시로 저장 

- CPU의 동작
  - 2진법(0,1 의 기계어 >> 어셈블리어 >> 사람이 알아볼 수 있도록 변환한 것이 프로그래밍 언어) 
  - 기계어(저장공간) >>  어셈블리어(CPU) >> 프로그래밍 언어(사람)
  - (1) 명령어 인출 : CU가 이번에 수행할 ㅁ명령어를 가져옵니다.
  - (2) 명령어 해독 : opcode 명령어로 해독하고, 코드를 인출, 그에 맞는 레지스터들을 준비
  - (3) 실행 : 해독된 명령어를 수행, ALU가 주체가 되어서 실행
  - (4) 반영 : 명령어의 수행 결과를 반영하며, 한 사이클이 끝남

- CPU의 성능
  - 클럭 : 1기가 헤르트(1초에 1기가만큼, 1024메가, 10억 번 정도 처리하는 것을 말합니다.)
    - 4.5GHz 라는 것은 초당 45억번의 명령어를 처리
  - 코어 : 중앙처리 장치, 멀티코어는 많은 연산을 빠르게 병렬처리한다는 것을 말합니다.   

4. 메모리 : (요리주문에 대해서 재료들을 둘 공간, 재료냉장고)
- 레지스터(메모리는 아니고, CPU)
- 캐시 메모리(L2, L3 => SRAM) : 휘발성 메모리, 전원이 꺼지면 지워짐, 제일 빠르게 조회할 수 있는 공간 
  - 메모리에서 작지만 비싼 메모리
  - 해당 요리를 만들기 위해서, 조리대에 올려놓는 메모리라고 생각합니다. 
  - L2, L3 캐시메모리는 CPU와 별도의 공간, 메인 메모리와 CPU 간의 속도차이를 극복하기 위한 것이라면
  - CPU 레지스터는 CPU 안에서 연산을 처리하기 위하여 데이터를 저장하는 공간
- 주 기억장치(메인 메모리, DRAM)
  - 역시 휘발성 메모리지만, 조금더 빠르게 저장할 수 있는 저장공간, 
  - Random Access Memory - 저장된 데이터를 순차적이 아닌 임의의 순서로 액세스할 수 있는 데이터 저장소
  - RAM은 DRAM과 SRAM이 있으나 주로 DRAM을 의미한다. 
  - SRAM : 정적 메모리, 전원공급되는 동안 내용은 사라지지 않으며, 재충전이 필요없다. 
  - DRAM : 동적 메모리, 전원이 공급되더라도, 주기적으로 재충전 되어야 기억된 내용을 유지할 수 있다. 
- 보조 기억장치(HDD, 하드디스크)
  - 전원이 꺼져도 지워지지 않는 저장공간 , 데이터와 프로그램을 반영구정으로 저장, 비휘발성 메모리 

- [삼성자산운용](https://www.youtube.com/watch?v=GlWhOm7B1CM)  
  - 메모리 반도체 : 정보를 저장 
    - 정보를 기억합니다. RAM, ROM
    - RAM(책장과 책상을 생각해봅시다 => 정보(책) 책상이 RAM)
      - 전원이 꺼지면, 정보가 사라지기에 휘발성 메모리 
      - [정보저장방식에 따라] D램, S램
      - D램:(동적) 저장된 정보가 시간이 흐름에 따라 소멸되는 반도체, 컴퓨터의 기억소자, 용량이 크고 처리속도가 빠름
      - S램:(정적)전원을 공급하는 한 데이터를 공급(회로가 복잡), 그래픽 카드 

  - 비메모리 반도체 : 정보를 처리

5. CPU와 메모리
- CPU와 메모리의 동작
- CPU와 메모리의 구조
- 최근 이슈
- 컴퓨터 구성 한눈에 보기 