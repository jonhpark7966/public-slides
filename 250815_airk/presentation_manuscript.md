# 허깅페이스의 Action Data Scaling, 르로봇 해커톤 

**AI Robotics Korea 2025 발표 원고**  
발표자: Sudoremove (LeRobot Worldwide Hackathon 서울 호스트)  
발표시간: 20분

---

## 표지 

안녕하세요, 저는 수도리무브 대표 박종현입니다.

저희는 딥러닝 시절에 학교를 다녔고, 최근까지는 비전과 LLM 을 주로 하다가 VLA 를 시작했습니다.
대학원 시절 부터 같이 공부하는 모임 이름이고요, 올해는 작게 유투브 채널을 시작했습니다.
두달전에 허깅페이스에서 르로봇 해커톤을 처음 개최하였는데, 서울 파트의 호스트를 맡았고 그 자격으로 이자리에 왔습니다.
허긷페이스의 르로봇이 Physical AI 시대에 어떤 의미를 갖고 있는지 이야기 하겠습니다.

---

## 1. Physicas AI, VLA의 등장

(Pysical intelligence, Tesla Optimus, Figure AI 데모들 이 나오면서.)


요즘 전 세계가 'Physical AI'에 주목하고 있습니다. 기대의 핵심은 범용 로봇 지능(VLA)입니다. 이는 기존 로보틱스가 과제별 파이프라인에 갇혀 있던 시대에서, 하나의 모델이 다양한 상황을 다루는 '제너럴리스트'로 전환한다는 뜻입니다.

여기 계신 분들은 아마 다 똑같이 생각하고 기대를 하고 계실텐데, VLA 가 잘 될꺼다. 로봇이 범용적으로 다양한 태스크를 수행할 수 있을 것이다. 왜죠?


---

## 2. LLM 의 성공

바로 LLM 이 성공하는 것을 봤기 때문이죠.
전세계인 모든 사람이 ChatGPT 를 봤습니다. 최근에슨 국제 수학 올림피아드에서 금메달도 땄죠. 이제 많이 똑똑합니다.

LLM 의 등장 전후를 한번 보겠습니다.

번역 하려면 번역 하는 모델이 따로 있어야 합니다. 더 옛날에는 어떤 룰 베이스의 로직이 있었고요.
요약 하려면 요약 하는 모델이 또 따로 있어야 합니다.
감성 분석 하려면 감성 분석하는 모델이 있어야 하죠.

요즘은 어떻죠?

GPT야 요약해줘. 딸깍. 번역해줘. 딸깍. 다 되죠. 범용 머신이에요. 
코딩해줘. 딸깍. 지금 이 자료도 LLM 이 만든거에요. 
애초에 GPT 2 paper 제목이 Multitask Learner, 범용 모델 입니다.


---

## 3. VLM 도 마찬가지

LLM 이 확장되어 나온 VLM Vision Language Model 도 마찬가지 입니다.

Classification 하려면 Resnet, Object detection 하려면 YOLO, Segmenation 하려면 Unet 다 따로 만들어야 합니다.
그런데 지금은? GPT-4o 나 Gemini 같은 멀티모달 모델한테 뭐냐고 물어보면 다 알려주고, 위치도 박스 쳐주고, 심지어 그림 그려달라고 하면 그려주죠.

Language 에서 Image, Audio, Video 까지 하나씩 확장해나가고 있어요. 이게 멀티모달리티죠.
다음은? 액션이다 라고 다들 생각하고 VLA 에 대해서 낙관적인 시선이 많은 것이죠. Physical AI 라는 키워드가 화제가 되는 흐름은 어찌보면 당연합니다.

VLA 과면 쉽게 성공할까요? 

---

## 4. LLM, VLM 의 성공 비결

LLM 은 어떻게 이렇게 똑똑할까요. 그 성공 요인을 알아보죠.
가장 중요한 요소는 단 한가지 입니다.

"Scaling" is all you need.

LLM 은 이미 전세계에 있는 모든 텍스트 데이터를 다 보고 학습했어요. 이미 2년 전에요.
인류가 역사적으로 생성한 모든 공개 데이터를 다 봤습니다.  

이미지도 마찬가지죠. 세상에 널린 이미지들을 다 보고 있어요. 
아마 지금 프론티어 모델들은 유투브를 보고 있을 거에요. 

그러니 모든 지식을 다 알고 있고, 그 world knowledge 를 바탕으로 범용 문제 해결 머신이 된 것이죠.
거기에 요즘엔 리즈닝, test time scaling 사고 시간도 스케일링해서 지능까지 가져오는 것이고요. 

그렇다면 VLA, 로봇에도 같은 공식이 통할까요? 

**이론적으로는 Yes, 현실적으로는 But...**

---

## 5. "액션 데이터는 인터넷에 없다"

텍스트, 이미지, 영상, 인터넷에 널려 있습니다. 그런데 액션 데이터는요?

(lerobot visualizer, action data 띄워두고 보여주기)

학습하기 좋게 정리된 액션 데이터가 없어요. 사람이라고 치면 사람의 관절 각도, 손의 좌표, 이런 것이 액션데이터인데요. 없죠.

이걸 해결하기 위한 노력들 다양하게 많이 하고 있습니다. 

---

## 6. NVIDIA 의 Action Data Scaling 전략

Jim Fan의 직설: "Robot Data is Human Fuel"

NVIDIA의 Jim Fan은 이렇게 말합니다:
> "로봇 데이터는 human fuel이다. 사람이 직접 텔레오퍼레이션으로 만들어야 한다."

(Tesla optimus teleoperation, Physical Intellilgence teleoperation 장면들)

수십명, 수백명 단위로 채용해서 모으고 있습니다. Teleoperation 만으로는 한계가 있죠.

---

## 7. 해법 1: NVIDIA의 시뮬레이션 3단계 전략

### 가상에서 만드는 무한 데이터

NVIDIA는 이 병목을 돌파할 독특한 3단계 전략을 제시합니다:

### Stage 1: 디지털 트윈 (Digital Twin)
**"현실의 완벽한 복제"**

- BMW 공장을 Omniverse에 1:1로 구현
- 물리 정확도 99.9% 
- 1000배 속도로 시뮬레이션
- **Zero-shot transfer**: 시뮬레이션에서 학습 → 실제 로봇에 바로 적용

### Stage 2: 디지털 사촌 (Digital Cousin)  
**"생성 AI로 만드는 무한 변주"**

Jim Fan의 표현을 빌리면:
> "현실과 물리는 같지만, 모습이 다른 수많은 사촌들"

- 물리엔진은 유지하되, 3D 자산/텍스처/레이아웃을 생성 AI로 대량 합성
- 주방 환경 하나를 1000가지 버전으로 변주
- 컵 하나를 10000가지 디자인으로 생성

### Stage 3: 디지털 노마드 (Digital Nomad)
**"꿈속을 떠도는 월드 모델"**

> "Doctor Strange처럼 14,000,605개의 가능한 미래를 시뮬레이션"

- 비디오 확산 모델 기반 월드 시뮬레이터
- 물리엔진 없이 신경망이 직접 미래 예측
- 유체, 연성체 등 복잡한 상호작용도 학습
- 1초에 수천 개의 가능한 시나리오 생성

**핵심**: Sim 1.x(물리 정확) + Sim 2.0(신경 창의) = 무한 데이터 생성기

월드 모델과 Compute 의 힘으로 양질의 가상의 데이터를 무제한으로 만들겠다는 것이죠. 
여전히 Sim2Real Gap 을 해결해야 하지만 성공한다면 단숨에 스케일링이 가능한 방법이라고 봅니다. 

이 외에도 영상에서 action data 를 추출해내서 수 많은 영상 데이터를 액션 데이터로 만들어 쓰는 방법이라던가, 여러 방법들이 연구되고 있습니다.

---

## 8. Hugging Face의 커뮤니티 전략

자 그럼 여기서, HuggingFace 의 전략을 보겠습니다. 

지금 HuggingFace 는 LLM 을 하는 사람들 사이에서는 가장 인기가 많은 곳이죠. 손만 대면 다 가져가고 있는데요. 
그 성공공식을 로봇 분야에 그대로 적용하려는 것이 보입니다. 

"Community Driven".


---

## 9. 1만 명이 모으면 1만 배 빨라진다

NVIDIA가 '생성'에 집중한다면, Hugging Face는 '수집'에 집중합니다.

"Democratizing" 모두가 다 로봇을 만들 수 있고, 데이터를 수집할 수 있고, VLA 학습을 할 수 있는 모든 도구를 공개하는 것이에요.

### SO-101: 누구나 만들 수 있는 로봇

이케아 가구처럼 조립하는 오픈소스 로봇:
- 3D 프린터로 출력 가능한 부품
- 타오바오에서 살 수 있는 모터
- GitHub에 공개된 전체 BOM(부품 목록)
- 조립 영상 튜토리얼
- 국가별 부품 공급업체 리스트

서울 해커톤에서도 3팀이 현장에서 조립 성공. 한 참가자는 "프라모델보다 쉽다"고 평가했습니다.

### LeRobot Platform 

너무 쓰기가 쉽게 되어 있습니다.
- Teleop 실행 하는거 python 스크립트 실행하면 됩니다. 자동으로 허깅페이스에 데이터가 올라갑니다.
- 그 데이터로 학습 시키는 것, 또 python 스크립트 하나 실행하면 됩니다.
- 그 모델로 로봇 구동하는 것, evaluation 이죠, 또 python 스크립트 하나 실행하면 되고요 허깅페이스에 데이터 올라갑니다.


### smolVLA

이렇게 커뮤니티가 so arm 101 로 만든 데이터를 모아서 학습시켜 만든 모델이 smolVLA 입니다.
이제 우리가 smolVLA 을 다운 받아서 우리 데이터로 직접 튜닝 시키면 되죠.



## 10. 월드와이드 해커톤: 데이터 수집의 축제

이제 이 커뮤니티를 가속하게 하기 위한 축제를 열어 줍니다. 월드와이드 해커톤.
저희가 이 해커톤의 서울 로컬 호스팅을 맡았습니다. 

**2025년 6월 14-15일 성과**:
- 참가: 전 세계 44개국, 3000명 이상 참가
- 데이터: 190개 데이터셋 제출 
- 총 에피소드: 50,000+ (이틀 만에!, 제출된 것만)

**천재적인 규칙**: 
1. 모든 팀은 최소 50개 에피소드를 Hub에 업로드
2. 1분 데모 영상 필수 제출
3. 데이터 라이선스는 자동으로 MIT

결과? **이틀 만에 Google이 17개월 걸린 데이터의 40%를 모았습니다.**

---

**서울 해커톤 사례**:

Top 10 에 2팀. 
Top 30 에 3팀.

심지어 3팀 중 2팀은 현장에 와서 로봇 조립부터 시작했어요. 
아이디어 회의 하고, 데이터 수집하고, 모델 학습하고, 데모까지.

재미있었어요. 진짜로. 정보 교류도 하고, 커스텀 로봇도 구경하고, 다 같이 피치 세션도 하고, 수상도 하고.
진짜 이런게 커뮤니티의 힘이구나 하는걸 느꼈습니다.


---

## 11. Transformers 전략의 재현

### 성공 공식을 그대로 로보틱스에

Hugging Face는 Transformers 라이브러리로 NLP 민주화를 이뤘습니다:

LLM 시대에서 Transformers 만들고, 학습 코드 만들고, 데이터 헙 만들고, 데이터 직접 수집해서 공개하고, LLM 레시피 공개하고. 이렇게 성공했습니다.

똑같이, LeRobot 만들고, 학습 코드 만들고, 데이터 헙 만들고,

차이점? 로보틱스는 **하드웨어**가 있다는 것. 그래서 SO-101 도 최대한 저가로 만들어서 공개한 것이죠.

**Transformers (2018-2024)**:
- 400K+ 모델
- 100K+ 데이터셋  
- 5000+ 외부 기여자
- 사실상의 표준 API

**LeRobot (2024-)**:
- 같은 플레이북 실행 중
- Hub 통합
- 표준 API
- 커뮤니티 드리븐

---

## 11. 수도리무브의 다음 행보

**Physical AI의 시대는 수 많은 개인이 만들어갑니다.**

LLM이 그랬듯이요.

미약하게나마 우리도 커뮤니티에 활성화에 기여를 하자.

한국어 도큐멘테이션, 허깅페이스의 오픈소스 로봇 한국 디스트리뷰터, 튜토리얼 영상, 

연말에 가능하면 무료로 르로봇 교육 세션을 진행하려고 합니다.

하고 싶으신 분들 모두 쉽게 입문하실 수 있게요.

Realworld Action Data Scaling, 여러분도 함께하시죠.


감사합니다.

---

## 참고 자료

### 핵심 논문
- RT-2: Vision-Language-Action Models (Google, 2023) - [arXiv:2307.15818](https://arxiv.org/abs/2307.15818)
- Open X-Embodiment: Robotic Learning Datasets (2023) - [robotics-transformer-x.github.io](https://robotics-transformer-x.github.io)
- Scaling Laws for Neural Language Models (2020) - [arXiv:2001.08361](https://arxiv.org/abs/2001.08361)

### 플랫폼 & 도구
- LeRobot Documentation - [huggingface.co/docs/lerobot](https://huggingface.co/docs/lerobot)
- SO-101 Assembly Guide - [github.com/TheRobotStudio/SO-ARM100](https://github.com/TheRobotStudio/SO-ARM100)
- SmolVLA Fine-tuning - [huggingface.co/docs/lerobot/smolvla](https://huggingface.co/docs/lerobot/smolvla)

### 시뮬레이션 & 전략
- Jim Fan: Physical Turing Test - [josherich.me/podcast/physical-turing-test](https://josherich.me/podcast/the-physical-turing-test-jim-fan-on-nvidias-roadmap-for-embodied-ai)
- NVIDIA Omniverse - [nvidia.com/omniverse](https://nvidia.com/omniverse)

### 커뮤니티
- LeRobot Worldwide Hackathon - [huggingface.co/LeRobot-worldwide-hackathon](https://huggingface.co/LeRobot-worldwide-hackathon)
- 서울 해커톤 후기 - [sudormrf.run/2025/06/24/huggingface-lerobot-hackathon-review](https://sudormrf.run/2025/06/24/huggingface-lerobot-hackathon-review)

---

*이 발표는 LeRobot Worldwide Hackathon Seoul 운영 경험과 Physical AI 분야의 최신 연구를 바탕으로 작성되었습니다.*