---
name: portrait-master
description: 生成高度逼真的商业级人像照片，适合写真、产品展示、人力资源等场景
type: FLUX
subtype: photorealistic
tags: [人像, 商业, 写实]
created: 2026-04-24
tested: true
---

# FLUX 写实人像大师

## 效果描述

生成细节丰富、皮肤纹理清晰、眼神有光的商业级人像照片，光影自然，背景虚化恰到好处。

## 适用场景

- 商业写真拍摄
- 简历照片制作
- 产品代言人像
- 社交媒体头像
- 品牌宣传物料

## 正向提示词

```
professional portrait photography, 35mm lens, f/1.8 aperture, soft natural lighting,
studio backdrop, subject looking directly at camera, slight smile, confident expression,
sharp focus on eyes, skin texture visible, natural skin pores, catch lights in eyes,
professional retouching, shallow depth of field, warm skin tones, Caucasian/Asian/African features,
wearing casual smart attire, modern minimalist studio, high-end commercial photography style,
8k resolution, photorealistic, RAW photo quality, color graded, slight vignette
```

## 负面提示词

```
anime, cartoon, illustration, painting, drawing, sketch,
deformed, disfigured, mutated, ugly, bad anatomy, wrong anatomy,
extra limbs, missing arms, extra legs, cropped, frame, border,
jpeg artifacts, compression artifacts, blurry, out of focus,
amateur photography, overexposed, underexposed, dark,
low resolution, low quality, watermark, signature, text, logo
```

## 参数建议

| 参数 | 值 |
|:-----|:---|
| Steps | 25–35 |
| CFG | 3.5–5 |
| Sampler | euler_ancestral / dpmpp_2m |
| 分辨率 | 1024×1024 (1:1) |
