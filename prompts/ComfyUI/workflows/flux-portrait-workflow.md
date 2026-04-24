---
name: flux-portrait-workflow
description: FLUX人像生成完整工作流，包含ControlNet和LoRA设置
type: ComfyUI
subtype: workflow
tags: [FLUX, 人像, 工作流, ControlNet, LoRA]
created: 2026-04-24
tested: true
difficulty: 4
---

# ComfyUI FLUX 人像工作流

**描述**：完整的FLUX人像生成工作流配置，包含ControlNet和LoRA设置

**提示词类型**：ComfyUI工作流

**工作流配置**：
```json
{
  "workflow_name": "FLUX人像增强工作流",
  "version": "1.0",

  "节点配置": {
    "CLIPTextEncode": {
      "positive": "professional portrait, photorealistic, 85mm lens, f/1.4, sharp focus on eyes, natural skin texture, catch lights, studio lighting, neutral background, 8K resolution",
      "negative": "anime, cartoon, illustration, painting, deformed, bad anatomy, extra limbs, blurry, low quality"
    },

    "FluxDevControlNet": {
      "model": "flux-controlnetPortrait-v10.safetensors",
      "strength": 0.7,
      "guidance": 3.5
    },

    "KSampler": {
      "model": "flux1-dev.safetensors",
      "seed": 42,
      "steps": 28,
      "cfg": 3.5,
      "sampler_name": "euler_ancestral",
      "scheduler": "simple"
    },

    "LoRA加载器": {
      "lora_1": "detail_enhancer.safetensors",
      "lora_strength_1": 0.8,
      "lora_2": "skin_smoothing.safetensors",
      "lora_strength_2": 0.3
    }
  },

  "后处理": {
    "upscale": {
      "model": "4x-UltraSharp",
      "scale": 2
    },
    "color_grading": "portrait_embedded_LUT.png"
  }
}
```

**使用说明**：
1. 加载 FluxDevControlNet 配合 flux-controlnetPortrait 模型
2. 建议使用参考图控制姿态和构图
3. LoRA强度可根据需要调整
4. 后处理使用Portrait Embedding LUT增强肤色

**适用场景**：
- 商业人像摄影
- 写真风格生成
- 人像修复增强
- AI模特展示

**参数建议**：

| 参数 | 值 |
|:-----|:---|
| Steps | 25-30 |
| CFG | 3.5 |
| Sampler | euler_ancestral |
| 分辨率 | 1024×1024 |