---
name: portrait-passport
description: 生成标准的证件照风格的AI人像
type: FLUX
subtype: photorealistic
tags: [人像, 证件照, 签证]
created: 2026-04-24
tested: true
---

# FLUX 证件照

## 效果描述

生成符合证件照标准的清爽人像：五官清晰、背景纯净、整体正式得体。适用于签证、身份证、驾照等官方证件用途。

## 适用场景

- 签证申请照片
- 身份证照片
- 驾照证件照
- 简历照片
- 各类官方证件

## 正向提示词

```
official passport photograph style, visa photo, biometric picture,
neutral white or light blue background, subject facing camera directly,
neutral expression, eyes open and visible, natural skin tone,
minimal retouching, even lighting on face, no shadows on background,
slight shallow depth of field, passport photo standards,
high resolution, photorealistic, sharp focus on face
```

## 负面提示词

```
casual photo, selfie, snapshot, informal pose,
smile showing teeth, laughing, frowning, serious expression,
glasses reflections, red eyes, asymmetric,
shadows on face, uneven lighting, harsh lighting,
anime, cartoon, illustration, painting, drawing,
deformed, ugly, bad anatomy, extra limbs, extra fingers,
blurry, out of focus, low quality, low resolution,
jpeg artifacts, compression artifacts,
watermark, text, logo, frames, border
```

## 参数建议

| 参数 | 值 |
|:-----|:---|
| Steps | 25–30 |
| CFG | 3.5–4.5 |
| Sampler | euler_ancestral |
| 分辨率 | 1024×1024 (1:1) |
