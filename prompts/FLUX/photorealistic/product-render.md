---
name: product-render
description: 电商级产品渲染图，适合3C产品、数码配件等商业展示
type: FLUX
subtype: photorealistic
tags: [产品, 电商, 渲染]
created: 2026-04-24
tested: true
---

# FLUX 产品渲染

## 效果描述

生成高端电商风格的产品渲染图：干净背景、精湛光影、产品质感突出。适合 3C 数码、化妆品、首饰等各类产品。

## 适用场景

- 电商平台主图
- 产品官网展示
- 品牌宣传物料
- 社交媒体产品图
- 产品画册设计

## 正向提示词

```
professional product photography, 3C electronics or cosmetics product,
clean white background, studio lighting with soft box,
product centered, sharp focus on product details,
reflection on surface, subtle shadow,
high-end commercial photography style,
e-commerce product shot, minimalist aesthetic,
8k resolution, photorealistic, RAW photo quality, color graded
```

## 负面提示词

```
messy background, cluttered scene, outdoor setting, distracting elements,
anime, cartoon, illustration, painting, drawing,
deformed, ugly, bad anatomy, blurry, distorted product,
low quality, low resolution, jpeg artifacts, compression artifacts,
watermark, signature, frames, border
```

## 参数建议

| 参数 | 值 |
|:-----|:---|
| Steps | 20–28 |
| CFG | 3.0–4.0 |
| Sampler | euler_ancestral |
| 分辨率 | 1024×1024 (1:1) |
