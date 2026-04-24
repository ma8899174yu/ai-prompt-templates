# FLUX 提示词编写指南

> **适用模型**：FLUX.1 (schnell/dev/pro)
> **风格定位**：自然语言优先、高质量电影感、可直接使用

---

## FLUX vs Stable Diffusion 核心差异

| 特性 | FLUX | Stable Diffusion |
|------|------|-----------------|
| **提示词风格** | 自然语言，长句无压力 | 关键词堆砌，逗号分隔 |
| **质量描述** | 直接描述期望效果 | 使用特定质量标签 |
| **否定提示词** | 通常不需要 | 必要但效果有限 |
| **分辨率敏感度** | 较低 | 高 |
| **细节控制** | 语义理解强 | 需要Lora/ControlNet |

---

## FLUX 提示词黄金公式

```
[主体描述] + [场景/环境] + [光线/氛围] + [风格/媒介] + [质量修饰词]
```

### 示例对比

❌ SD风格（淘汰）：
```
masterpiece, best quality, 1girl, blonde hair, blue eyes, white dress, 
flower field, sunny, professional photography
```

✅ FLUX风格（推荐）：
```
A young woman with blonde hair and bright blue eyes wearing a flowing white dress 
stands in a field of wildflowers. Golden hour sunlight creates a warm, ethereal glow. 
Shot on medium format film with soft bokeh.
```

---

## 质量修饰词参考

### 摄影类
- `professional photography` / `commercial photography`
- `shot on [相机型号]` 如 Canon 5D, Leica M10, Hasselblad
- `85mm lens, f/1.8 aperture` / `35mm lens`
- `shallow depth of field` / `deep focus`
- `natural lighting` / `studio lighting`
- `golden hour` / `blue hour`

### 光线类
- `dramatic lighting` / `soft diffused light`
- `rim light` / `backlit` / `side lighting`
- `volumetric light rays` / `god rays`
- `catch lights in eyes`

### 画质类
- `8K resolution` / `ultra detailed`
- `RAW photo quality` / `RAW photo`
- `photorealistic` / `hyperrealistic`
- `sharp focus` / `tack sharp`

### 风格类
- `cinematic` / `documentary style`
- `editorial quality` / `magzine cover`
- `National Geographic style`
- `Vogue editorial`
- `film grain` / `vintage film look`

### 艺术家参考
- `Greg Rutkowski style`
- `Alphonse Mucha fusion`
- `Zhang Daqian style`
- `Ansel Adams style`
- `Ridley Scott film aesthetic`

---

## 常用参数建议

| 类型 | Steps | Guidance | 分辨率 |
|------|-------|----------|--------|
| 人像摄影 | 25-30 | 1.5-2.0 | 1024x1024 |
| 风景建筑 | 28-35 | 1.5-2.5 | 1536x1024 |
| Cinematic | 30-40 | 2.0-3.5 | 1792x768 (21:9) |
| 产品商业 | 20-25 | 1.0-1.5 | 1024x1024 |
| 艺术插画 | 25-35 | 1.5-3.0 | 1024x1536 |

---

## 负面提示词（通常可省略）

FLUX对负面提示词的依赖较低，以下情况可考虑使用：

1. 需要排除特定元素时
2. 生成角色时避免畸形
3. 避免特定风格时

**基础负面提示词**：
```
cartoon, anime, illustration, painting, drawing
deformed, ugly, bad anatomy
blurry, low quality, watermark
```

---

## 比例推荐

| 用途 | 比例 | 分辨率 |
|------|------|--------|
| Instagram | 1:1 | 1024x1024 |
| 电影感 | 21:9 | 1792x768 |
| 人像竖版 | 3:4 | 1024x1360 |
| 风景横版 | 3:2 | 1536x1024 |
| 社交媒体 | 9:16 | 768x1792 |

---

**更新日期**：2026-04-24
**维护者**：prompt-engineer
