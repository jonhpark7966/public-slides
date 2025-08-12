# 슬라이드 컨텐츠 구성

## 슬라이드 1: 타이틀
**제목:** 허깅페이스의 Action Data Scaling 전략
**부제:** LeRobot Worldwide Hackathon이 보여준 커뮤니티의 힘
**정보:** AI Robotics Korea 2025 | 수도리무브

---

## 슬라이드 2: 발표자 소개
**수도리무브 (Sudormrf)**
- Deep Learning 연구 그룹 (2018~)
- Computer Vision & LLM → VLA 
- YouTube Channel: 수도리무브
- LeRobot Worldwide Hackathon Seoul Host

**오늘의 주제:**
Physical AI 시대, 허깅페이스가 선택한 길

---

## 슬라이드 3: Physical AI의 부상
**최근 주목받는 로봇 AI 기업들**

| 기업 | 핵심 기술 | 투자 규모 |
|------|----------|----------|
| Physical Intelligence | π0 (VLA 모델) | $400M (Bezos, OpenAI) |
| Figure AI | Figure-01 + GPT | $675M (Microsoft, NVIDIA) |
| Tesla | Optimus + FSD | 자체 투자 |

**공통점:** Vision-Language-Action (VLA) 모델 개발

---

## 슬라이드 4: VLA란 무엇인가
**Vision-Language-Action Model**

기존 로보틱스:
```
Task 1 → Pipeline 1
Task 2 → Pipeline 2  
Task 3 → Pipeline 3
```

VLA 시대:
```
모든 Task → 하나의 VLA 모델
```

**핵심 질문:** VLA가 정말 성공할까? 

---

## 슬라이드 5: LLM의 성공 스토리
**Task-Specific → General Purpose**

| Before (2018) | After (2024) |
|---------------|--------------|
| 번역 모델 (GNMT) | GPT: "번역해줘" |
| 요약 모델 (BERTSUM) | GPT: "요약해줘" |
| 코딩 모델 (Codex) | GPT: "코딩해줘" |
| 수학 모델 (Minerva) | GPT: "풀어줘" |

**GPT-2 논문:** "Language Models are Unsupervised Multitask Learners"

---

## 슬라이드 6: Vision도 같은 길
**Computer Vision의 통합**

전문 모델 시대:
- Classification: ResNet, EfficientNet
- Detection: YOLO, Faster R-CNN
- Segmentation: U-Net, DeepLab

멀티모달 시대:
- GPT-4o: 모든 비전 태스크
- Gemini: 이미지 이해 + 생성
- Claude: 문서 + 코드 + 이미지

**진화 경로:** Text → Image → Video → **Action?**

---

## 슬라이드 7: 성공의 핵심 - Scaling Laws
**Chinchilla Scaling Laws (2022)**

```
Model Performance = f(N, D, C)
- N: Parameters (모델 크기)
- D: Data tokens (데이터 양)  
- C: Compute FLOPs (연산량)
```

**LLM/VLM 데이터 스케일:**
- GPT-3: 300B tokens
- GPT-4: 13T tokens (추정)
- Gemini: YouTube 전체

**결론:** 데이터가 곧 지능

---

## 슬라이드 8: VLA의 치명적 약점
**"액션 데이터는 인터넷에 없다"**

| 데이터 타입 | 인터넷 규모 | 수집 방법 |
|------------|------------|----------|
| Text | 수조 개 페이지 | Web Crawling |
| Image | 수백억 장 | Web Scraping |
| Video | YouTube (500시간/분) | API |
| **Action** | **거의 없음** | **Human Teleoperation** |

**문제:** 로봇 관절각, 그리퍼 위치, 힘 데이터는 수동 수집 필요

---

## 슬라이드 9: 현재의 Action 데이터 규모
**Reality Check**

| 프로젝트 | 데이터 규모 | 수집 기간 | 리소스 |
|---------|-----------|----------|--------|
| RT-1 (Google) | 130K episodes | 17개월 | 13 robots |
| RT-2 (Google) | 웹 데이터 + RT-1 | - | - |
| Open X-Embodiment | 1M+ trajectories | 2년 | 21 labs |
| Bridge V2 | 60K demos | 1년 | 5 robots |

**Jim Fan (NVIDIA):** "Robot data is human fuel"

---

## 슬라이드 10: Tesla와 PI의 접근
**Teleoperation 대규모 투자**

Tesla Optimus:
- 수백 명 텔레오퍼레이터 채용
- 24시간 데이터 수집
- 목표: 연간 수백만 trajectories

Physical Intelligence:
- $400M 투자로 데이터팀 구축
- π0 모델 학습용 데이터 수집

**한계:** 비용과 확장성 문제

---

## 슬라이드 11: NVIDIA의 해법 - 시뮬레이션
**3단계 시뮬레이션 전략**

**Stage 1: Digital Twin (디지털 트윈)**
- 현실 100% 복제
- 물리 정확도 최우선
- BMW 공장, Amazon 창고

**Stage 2: Digital Cousin (디지털 사촌)**
- 물리는 같고 외형만 다양화
- 생성 AI로 무한 변주
- 1 kitchen → 1000 kitchens

**Stage 3: Digital Nomad (디지털 노마드)**
- 비디오 확산 기반 월드모델
- 신경망이 물리 시뮬레이션
- Doctor Strange: 14,000,605 futures

---

## 슬라이드 12: 시뮬레이션의 한계
**Sim2Real Gap은 여전히 존재**

장점:
- 무한 데이터 생성
- 안전한 실험 환경
- 1000x 속도

단점:
- 현실 물리 100% 재현 불가
- 센서 노이즈 모델링 어려움
- Domain Adaptation 필요

**결론:** 실제 데이터가 여전히 필수

---

## 슬라이드 13: HuggingFace의 전략
**"Community Driven Scaling"**

NVIDIA: 시뮬레이션으로 **생성**
HuggingFace: 커뮤니티로 **수집**

**Democratizing Robotics:**
- 누구나 로봇 제작
- 누구나 데이터 수집
- 누구나 모델 학습

**성공 사례:** Transformers Library
- 400K+ models
- 100K+ datasets
- 5000+ contributors

---

## 슬라이드 14: SO-101 - 민주화된 하드웨어
**$200 DIY Robot Arm**

| 구성 요소 | 가격 | 구매처 |
|----------|------|--------|
| 3D 프린팅 파츠 | $30 | 직접 출력 |
| 서보 모터 (6개) | $120 | 타오바오/알리 |
| 제어 보드 | $30 | Arduino/ESP32 |
| 기타 부품 | $20 | 로컬 |

**특징:**
- GitHub 전체 설계도 공개
- 3시간 조립 가능
- 서울 해커톤: "프라모델보다 쉬워요"

---

## 슬라이드 15: LeRobot Platform
**Simple as 1-2-3**

```python
# Step 1: Collect Data (1줄)
python lerobot/scripts/teleop.py

# Step 2: Train Model (1줄)  
python lerobot/scripts/train.py

# Step 3: Deploy Robot (1줄)
python lerobot/scripts/eval.py
```

**자동화된 워크플로우:**
- Teleop → 자동 HuggingFace Hub 업로드
- Dataset → 자동 전처리 & 포맷팅
- Model → 자동 배포 & 공유

---

## 슬라이드 16: smolVLA - 커뮤니티의 첫 결실
**Small Vision-Language-Action Model**

| 특성 | 기존 VLA | smolVLA |
|------|---------|---------|
| 파라미터 | 5B+ | 300M |
| GPU 요구사항 | A100 | RTX 3060 |
| 학습 데이터 | 비공개 | 커뮤니티 데이터 |
| 라이선스 | Proprietary | Apache 2.0 |

**핵심:** 작지만 실용적, 누구나 fine-tuning 가능

---

## 슬라이드 17: Worldwide Hackathon 개요
**2024년 11월 14-15일**

**글로벌 규모:**
- 44개국 동시 개최
- 3000+ 참가자
- 190개 팀 데이터 제출

**핵심 규칙:**
1. 최소 50 에피소드 수집 의무
2. HuggingFace Hub 업로드 필수
3. 1분 데모 영상 제출
4. MIT 라이선스 자동 적용

---

## 슬라이드 18: 해커톤 성과 - 숫자로 보기
**48시간의 기적**

| 지표 | 수치 | 비교 |
|------|------|------|
| 총 에피소드 | 50,000+ | RT-1의 38% |
| 데이터셋 | 190개 | 새로운 태스크 다양성 |
| 모델 | 12개 | 다양한 아키텍처 실험 |
| 수집 시간 | 48시간 | Google 17개월 vs 2일 |

**의미:** 커뮤니티가 대기업 속도를 압도

---

## 슬라이드 19: 서울 해커톤 스토리
**Top 10에 2팀, Top 30에 3팀**

**Team Chopsticks (Top 10):**
- 현장에서 SO-101 조립 시작
- 젓가락질 태스크 정의
- 200 에피소드 수집
- smolVLA fine-tuning
- 김밥 집기 성공!

**Team Seoul-Robotics:**
- 커스텀 그리퍼 설계
- 3D 프린팅 현장 제작
- 실시간 데이터 파이프라인

**분위기:** "진짜 커뮤니티의 힘이구나!"

---

## 슬라이드 20: 서울 현장의 인사이트
**48시간 운영 경험**

**준비한 것:**
- 3D 프린터 3대
- 예비 부품 10세트
- GPU 서버 (RTX 4090 x4)
- 24시간 카페테리아

**배운 것:**
- 하드웨어 고장률 30%
- 팀워크 > 기술력
- 실시간 지식 공유 중요
- 글로벌 연결 (Zoom)의 힘

---

## 슬라이드 21: HuggingFace vs NVIDIA
**상호보완적 전략**

| | NVIDIA | HuggingFace |
|--|--------|-------------|
| 접근 | Top-down | Bottom-up |
| 데이터 | 시뮬레이션 생성 | 실제 수집 |
| 품질 | High fidelity | Real diversity |
| 비용 | GPU 집약적 | 인력 집약적 |
| 확장성 | 무한 | 커뮤니티 크기 |

**미래:** 두 접근의 융합이 답

---

## 슬라이드 22: 수도리무브의 미션
**한국 로봇 AI 커뮤니티 활성화**

**2025 로드맵:**
- Q1: LeRobot 한국어 문서화
- Q2: SO-101 한국 공급망 구축
- Q3: 무료 교육 세션 (월 1회)
- Q4: Korea Robotics Hackathon

**파트너십:**
- HuggingFace 공식 협력
- 국내 대학 연구실 연계
- 스타트업 협업

---

## 슬라이드 23: Call to Action
**Physical AI 시대, 함께 만들어갑시다**

**개인 참여 방법:**
1. LeRobot 설치 → 튜토리얼
2. SO-101 조립 → 데이터 수집
3. Hub 업로드 → 커뮤니티 기여

**기업/연구실:**
- 데이터 공개 검토
- 해커톤 스폰서십
- 공동 연구 프로젝트

**"LLM이 그랬듯, Physical AI도 커뮤니티가 만듭니다"**

---

## 슬라이드 24: 마무리
**감사합니다**

**Contact:**
- 수도리무브: sudormrf.com
- GitHub: @sudormrf
- HuggingFace: @sudormrf

**Resources:**
- LeRobot: huggingface.co/lerobot
- SO-101: github.com/TheRobotStudio
- Hackathon: lerobot-hackathon.com

질문 환영합니다!