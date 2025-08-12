---
theme: eloc
css: unocss
---

<link rel="stylesheet" href="/style.css">

# 색상 스타일 가이드

## Primary & Secondary 색상 사용법

### 1. 텍스트 색상
<span class="primary">Primary 색상 텍스트</span>
<span class="secondary">Secondary 색상 텍스트</span>
<span class="accent">Accent 색상 텍스트</span>

### 2. 굵은 텍스트
<span class="primary-bold">Primary Bold</span>
<span class="secondary-bold">Secondary Bold</span>

### 3. 배경 색상
<span class="bg-primary">Primary 배경</span>
<span class="bg-secondary">Secondary 배경</span>
<span class="bg-accent">Accent 배경</span>

---

# 특수 효과

### 그라디언트 텍스트
<span class="gradient-text">Gradient Text Effect</span>

### 하이라이트
이것은 <span class="highlight">하이라이트된 텍스트</span> 입니다.

### 언더라인
<span class="underline-primary">Primary 언더라인</span>
<span class="underline-secondary">Secondary 언더라인</span>

### 박스 스타일
<div class="box-primary">
Primary 박스 스타일로 강조된 내용
</div>

<div class="box-secondary">
Secondary 박스 스타일로 강조된 내용
</div>

---

# 실제 사용 예시

## VLA의 <span class="primary-bold">치명적 약점</span>

**"액션 데이터는 <span class="underline-primary">인터넷에 없다</span>"**

<div class="box-secondary">
로봇 데이터 수집의 핵심:
- <span class="primary">Human Teleoperation</span>
- <span class="secondary">Community Scaling</span>
- <span class="accent">Open Source</span>
</div>

### <span class="gradient-text">48시간의 기적</span>

커뮤니티가 <span class="bg-accent">대기업 속도를 압도</span>

---

# 색상 팔레트

<div style="display: flex; gap: 20px; margin-top: 40px;">
  <div style="text-align: center;">
    <div style="width: 100px; height: 100px; background: var(--primary); border-radius: 8px;"></div>
    <p>Primary</p>
    <code>#FF6B6B</code>
  </div>
  <div style="text-align: center;">
    <div style="width: 100px; height: 100px; background: var(--secondary); border-radius: 8px;"></div>
    <p>Secondary</p>
    <code>#4ECDC4</code>
  </div>
  <div style="text-align: center;">
    <div style="width: 100px; height: 100px; background: var(--accent); border-radius: 8px;"></div>
    <p>Accent</p>
    <code>#FFE66D</code>
  </div>
</div>