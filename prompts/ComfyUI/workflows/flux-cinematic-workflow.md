---
name: flux-cinematic-workflow
description: FLUX电影感图像生成工作流，包含Canny/Depth ControlNet和色彩分级
type: ComfyUI
subtype: workflow
tags: [FLUX, 电影感, 工作流, ControlNet, 色彩分级]
created: 2026-04-24
tested: true
difficulty: 4
---

# ComfyUI Cinematic 电影感工作流

**描述**：生成电影感图像的完整工作流配置

**提示词类型**：ComfyUI工作流

**工作流配置**：
```json
{
  "workflow_name": "FLUX Cinematic电影感工作流",
  "version": "1.0",
  "author": "AI Prompt Templates",

  "节点配置": {
    "CLIPTextEncode_Positive": {
      "提示词": "描述电影感的完整场景，包括主体、场景、光线、氛围、构图"
    },

    "FluxDevModel": {
      "model": "flux1-dev.safetensors",
      "seed": 12345,
      "steps": 35,
      "cfg": 3.5,
      "sampler": "euler_ancestral"
    },

    "ControlNet设置": {
      "canny": {
        "model": "flux-controlnetCanny.safetensors",
        "strength": 0.6
      },
      "depth": {
        "model": "flux-controlnetDepth.safetensors",
        "strength": 0.4
      }
    },

    "色彩分级": {
      "lut_file": "cinematic_lut.png",
      "intensity": 0.7
    }
  },

  "预设效果": {
    "film_grain": {
      "opacity": 0.15,
      "type": "35mm"
    },
    "letterbox": {
      "ratio": "2.39:1",
      "color": "black"
    },
    "anamorphic_flare": {
      "enabled": true,
      "intensity": 0.3
    }
  }
}
```

**使用说明**：
1. 先使用Canny ControlNet控制构图
2. Depth ControlNet增加空间感
3. 色彩分级使用电影LUT
4. 可根据需要添加Film Grain

**适用场景**：
- 电影概念图
- 游戏过场动画
- 短视频封面
- 影视海报

**参数建议**：

| 参数 | 值 |
|:-----|:---|
| Steps | 30-40 |
| CFG | 3.5 |
| Sampler | euler_ancestral |
| 分辨率 | 1792×768 (21:9) |