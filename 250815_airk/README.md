# AI Robotics Korea 2025 발표 자료

## 커뮤니티가 움직일 때: LeRobot, 실물 데이터, 그리고 물리적 AI 스케일링

### 발표자
- Sudoremove (LeRobot Worldwide Hackathon 서울 호스트)

### 파일 구조
```
250815_airk/
├── README.md                      # 이 파일
├── presentation_todo.md           # 발표 준비 체크리스트
├── presentation_manuscript.md     # 전체 발표 원고
├── slides.md                      # Slidev 프레젠테이션 파일
└── package.json                   # Slidev 의존성
```

### 슬라이드 실행 방법

1. 의존성 설치:
```bash
npm install
```

2. 개발 모드로 실행 (자동으로 브라우저 열림):
```bash
npm run dev
```

3. 정적 빌드:
```bash
npm run build
```

4. PDF로 내보내기:
```bash
npm run export
```

### 발표 내용 요약

20분 발표로 다음 내용을 다룹니다:

1. **Physical AI와 VLA의 등장** - 로봇이 언어-시각-행동을 통합하는 시대
2. **LLM 스케일링 법칙** - 로보틱스에 적용 가능한가?
3. **데이터 병목 문제** - "Robot Data is Human Fuel"
4. **NVIDIA의 시뮬레이션 전략** - 디지털 트윈, 사촌, 노마드
5. **Hugging Face의 커뮤니티 전략** - SO-101, LeRobot, 해커톤
6. **SmolVLA** - 경량 VLA 모델의 의미
7. **서울 해커톤 인사이트** - 현장 운영 경험
8. **한국의 기회** - 하드웨어 강국 + AI 인재

### 핵심 메시지

- LLM의 성공 공식(스케일링)을 로보틱스에도 적용 가능
- 데이터 병목을 해결하는 두 접근: 시뮬레이션(NVIDIA) + 커뮤니티(Hugging Face)
- Physical AI 시대는 거대 기업이 아닌 커뮤니티가 만들어감

### 참고 자료

- [LeRobot Documentation](https://huggingface.co/docs/lerobot)
- [SO-101 Assembly Guide](https://github.com/TheRobotStudio/SO-ARM100)
- [서울 해커톤 후기](https://sudormrf.run/2025/06/24/huggingface-lerobot-hackathon-review)

### 라이선스

이 프레젠테이션은 [Creative Commons Attribution 4.0 International License (CC BY 4.0)](./LICENSE)에 따라 라이선스가 부여됩니다.

Copyright (c) 2025 박종현@sudoremove

이 저작물을 자유롭게 공유하고 수정할 수 있으며, 상업적 이용도 가능합니다. 단, 적절한 저작자 표시를 해주시기 바랍니다.