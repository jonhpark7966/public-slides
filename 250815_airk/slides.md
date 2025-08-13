---
theme: eloc
colorSchema: dark
title: 허깅페이스의 Action Data Scaling
info: |
  <span class="lerobot">LeRobot</span> Worldwide Hackathon이 보여준 커뮤니티의 힘
class: text-center
highlighter: shiki
drawings:
  persist: false
transition: slide-left
mdc: true
css: unocss
---

<link rel="stylesheet" href="/style.css">

## <span class="hf">허깅페이스</span>의 `Action Data Scaling`

> <span class="lerobot">LeRobot</span> Hackathon 의 의의

<div style="position: fixed; bottom: 20px; left: 20px;">
  <img src="/qr_code.svg" style="height: 250px;" />
</div>

<div style="position: fixed; bottom: 20px; right:20px; display: flex; gap: 10px; align-items: center;">
  <img src="/airk_logo.png" style="height: 100px; border-radius: 20px;" />
  <img src="/sudormrf.jpg" style="height: 100px; border-radius: 20px;" />
</div>
---

# <span class="primary-bold">`sudo rm -rf_`</span>

<div grid="~ cols-2 gapt4">
<div>

- <span class="lerobot">LeRobot</span> Worldwide Hackathon
  Seoul Host
- GPU, Vision → LLM → VLA
- Youtube [@sudoremove](https://www.youtube.com/@sudoremove)

</div>

<div>
<Youtube id="HgN0qIFSd8I" />
</div>
</div>

---

# `Physical AI`

<div grid="~ cols-2 gap-4" style="padding: 10px;">

<div class="text-center">
<h3 style="margin-bottom: 10px; font-size: 1.1em;">Physical Intelligence</h3>
<video controls autoplay muted loop style="width: 100%; height: 280px; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); object-fit: cover;">
  <source src="/physical_intelligence.mp4" type="video/mp4">
</video>
</div>

<div class="text-center">
<h3 style="margin-bottom: 10px; font-size: 1.1em; color: #888;">Figure AI</h3>
<video controls autoplay muted loop style="width: 100%; height: 280px; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); object-fit: cover;">
  <source src="/figure_demo.mp4" type="video/mp4">
</video>
</div>
</div>

<span class="primary">**VLA**</span> 기반의 Generalist




---

## ~~`Specialist`~~ -> `Generalist`


<video controls autoplay muted loop style="width: 50%; height: 50%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
  <source src="/chess_demo.mp4" type="video/mp4">
</video>

체스판의 `사이즈/색/재질`이 바뀌어도 체스를 둘 수 있을까?


---

## `LLM`의 성공


<div style="display: flex; justify-content: center;">

| **Before LLM** | **After LLM** |
|:-------------:|:------------:|
| 번역 모델 (Seq2Seq) | **GPT**: "번역해줘" |
| 요약 모델 (TextRank) | **GPT**: "요약해줘" |
| 코딩 모델 (DeepCoder) | **GPT**: "코딩해줘" |

</div>

<br>

**Task-Specific → General Purpose**

---

## `Vision`도 마찬가지


<div style="display: flex; justify-content: center;">

| **Before LLM** | **After LLM** |
|:-------------:|:------------:|
| 이미지 분류 (ResNet) | **GPT-4o**: "이거 뭐야?" |
| 객체 인식 (YOLO) | **GPT-4o**: "오브젝트 박스쳐" |
| Segmentation (U-Net) | **???** : "영역 색칠해" |

</div>
<br>

> text, image 에 이어서 <span class="primary-bold">`Action`</span> 도 잘 될까요?

---

## `Scaling` is all you need


<div style="display: flex; justify-content: center; align-items: center; padding: 20px;">
<img src="/scaling.webp" style="max-width: 80%; height: auto;" />
</div>

인터넷에 있는 **`모든`** 텍스트를 학습 했기 때문


---

## `VLA`의 Scaling 

<div grid="~ cols-2 gap-12" style="padding: 40px; align-items: center;">

<div style="text-align: center;">
<img src="/action_data.png" style="width: 90%; max-width: 380px;"/>
<p style="font-size: 0.7em; color: #666; margin-top: 8px;">
<a href="https://huggingface.co/spaces/lerobot/visualize_dataset_v1.6?dataset=cadene%2Fkoch_bimanual_folding&episode=7" target="_blank" style="color: #fb9c04; text-decoration: none;"><span class="lerobot">LeRobot</span> Data Visualizer ↗</a>
</p>
</div>

<div style="display: flex; align-items: center; justify-content: center; height: 100%; text-align: center;">

<h2 style="font-size: 1.2em; margin: 0;">
Action 데이터는 <br/>
<span class="underline-primary">인터넷에 없다</span>
</h2>
</div>

</div>

---

## 현재의 Action 데이터

| 프로젝트 | 데이터 규모 | 수집 기간 | 리소스 |
|---------|-----------|----------|--------|
| RT-1 (Google) | 130K | 17개월 | 13 robots |
| Open X-Embodiment | 1M+ | 2년 | 21 labs |

<br>


---

## <span class="tesla-bold">`Tesla`</span>'s Teleoperation

<video controls autoplay muted loop style="height: 280px; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); object-fit: cover;">
  <source src="/tesla_teleop.mp4" type="video/mp4">
</video>

수 백명의 Teleoperation 팀 운영

> <span class="nvidia">NVIDIA</span>: "Robot data is human fuel"

---

## <span class="nvidia-bold">`NVIDIA`</span>의 전략

<div style="text-align: center; margin: 0px 0;">
<video controls autoplay muted loop style="max-width: 800px; width: 100%; height: auto; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
  <source src="/cosmos_omniverse.mp4" type="video/mp4">
</video>
</div>

**장점:** 무제한 데이터  
**단점:** Sim2Real Gap 여전히 존재

---

## <span class="hf-bold">`HuggingFace`</span>의 전략

<span class="gradient-text">"Community Driven Scaling"</span>
> 1만명이 모으면, 1만배가 빨리진다

**Democratizing Robotics**  


---

## `SO-ARM 101`  Open Source Robot

<div grid="~ cols-2 gap-8" style="padding: 20px; align-items: center;">

<div style="text-align: center;">
<img src="/so-arm101.png" style="width: 90%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);" />
</div>

<div>

### $200 Budget Robot

- GitHub 전체 설계도 공개
- 3시간 조립 가능  
- 다양한 Add-on


</div>
</div>


---

## <span class="lerobot-bold">`LeRobot`</span> Platform

**Simple as 1-2-3**

```python
# Step 1: Collect Data
python lerobot/scripts/teleop.py

# Step 2: Train Model  
python lerobot/scripts/train.py

# Step 3: Deploy Robot
python lerobot/scripts/eval.py
```

자동 <span class="hf">HuggingFace</span> Hub 업로드 & 공유

---

## Open Weight `smolVLA`


<div style="text-align: center; margin: 20px 0;">
<img src="/smolvla.png" style="max-width: 700px; width: 100%; height: auto; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);" />
</div>

- 누구나 fine-tuning 가능하도록 튜토리얼 코드 제공  
- Community Dataset 으로 학습됨

---

## <span class="lerobot-bold">LeRobot</span> Worldwide Hackathon

**2025년 6월 14-15일**

<div style="text-align: center; margin: 20px 0;">
<img src="/world_hackathon.png" style="max-width: 600px; width: 100%; height: auto; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);" />
</div>

- 전세계 동시 개최, 44개국 오프라인 참여
- 3000+ 참가자, 190 팀 제출

---

## `32시간` 동안 모인 데이터

| 지표 | 수치 | 비고 |
|------|------|------|
| 총 에피소드 | 50,000+ | RT-1의 38% |
| 데이터셋 | 190개 | 다양한 태스크 |
| 수집 시간 | 32시간 | Google 17개월 vs 2일 |

**커뮤니티가 모여 수집한 Real-World 데이터** 

---

## `서울` 해커톤

<div grid="~ cols-2 gap-4" style="padding: 20px; height: 500px;">

<div style="display: flex; flex-direction: column; gap: 10px; align-items: flex-end;">
<video controls autoplay muted loop style="width: 70%; height: 250px; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.1); object-fit: cover;">
  <source src="/201-SeeNGripandBrothers-SquidGameSeeNGrip.mp4" type="video/mp4">
</video>
<video controls autoplay muted loop style="width: 70%; height: 250px; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.1); object-fit: cover;">
  <source src="/109-mos.mp4" type="video/mp4">
</video>
</div>

<div style="display: flex; justify-content: flex-start; align-items: center;">
<video controls autoplay muted loop style="width: 100%; height: 500px; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.1); object-fit: cover;">
  <source src="/25-197-aibot.mp4" type="video/mp4">
</video>
</div>

</div>

<br>

> Top 10에 2팀, Top 30에 3팀


---

### `서울 해커톤 현장`에서 배운 점

<div style="text-align: center; margin: 20px 0;">
<video controls autoplay muted style="max-width: 800px; width: 100%; height: auto; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
  <source src="/seoul_live_demo.mp4" type="video/mp4">
</video>
</div>

- Local & Global Community Driven 의 힘
- 진입 장벽이 매우 낮음

---

## <span class="hf">HuggingFace</span>, `Transformers` 전략의 재현

<div style="display: flex; justify-content: center; padding: 40px;">

| | **Transformers** (2018~) | <span class="lerobot-bold">**LeRobot**</span> (2024~) |
|:---:|:---:|:---:|
| **모델/데이터** | 400K+ 모델 호스팅<br/>100K+ 데이터셋 | 커뮤니티 데이터 수집 중<br/>Hub 통합으로 즉시 공유 |
| **생태계** | 5000+ 외부 기여자<br/>사실상의 표준 API | 같은 플레이북 실행 중<br/>표준화된 API 제공 |

</div>

> **성공 공식:** Library + Hub + Community (+ Hardware) = Ecosystem


---

## <span class="primary-bold">`수도리무브`</span> 의 다음 행보

> 한국에서 생태계 조성에 기여하기

- [x] <span class="lerobot">LeRobot</span> 튜토리얼 한국어 문서화, SO-ARM 101 공식 한국 공급망  
- [ ] 연말 무료 교육 세션 예정
- [ ] 커스텀 오픈소스 로봇 설계 & VLA 배포 

---

## `3줄` 요약

- Scaling 이 성공하면 VLA 도 성공한다
- Action Data 는 인터넷에 없다
- <span class="hf">HuggingFace</span> 는 모두가 Action Data 를 만들 수 있게 노력 중!


---
background: /HF-1.jpeg
dim: true
---

<div style="display: flex; flex-direction: column; justify-content: center; align-items: center; height: 100vh; position: relative;">

## `Physical AI`, 다 같이 열어가시죠

> 감사합니다

<div style="position: fixed; bottom: 30px; right: 30px; display: flex; gap: 15px; align-items: center;">
  <a href="https://youtube.com/@sudoremove" target="_blank" style="text-decoration: none; display: flex; align-items: center; gap: 6px; background: #ff0000; padding: 6px 12px; border-radius: 20px; color: white; font-size: 0.9em; font-weight: 500; box-shadow: 0 2px 10px rgba(255,0,0,0.3); transition: all 0.3s;">
    <span>Youtube</span>
  </a>
  <a href="https://sudormrf-run.github.io/community" target="_blank" style="text-decoration: none; display: flex; align-items: center; gap: 6px; background: #fb9c04; padding: 6px 12px; border-radius: 20px; color: white; font-size: 0.9em; font-weight: 500; box-shadow: 0 2px 10px rgba(251,156,4,0.3); transition: all 0.3s;">
    <span>Community</span>
  </a>
</div>

</div>