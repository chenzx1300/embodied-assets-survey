# 具身智能 · 工业资产生成深度调研 / Embodied AI Industrial Asset Survey (2026-10)

> 双语(中 / EN)静态 HTML 调研报告,聚焦"为具身机器人训练生成可交互工业资产"的两条技术路线。
> Bilingual (中 / EN) static-HTML deep-research reports on **generating interactive industrial assets for embodied-robot training**.

---

## 📚 文档目录 / Documents

| 文档 | 路径 | 主题 |
|---|---|---|
| **Direction A** | [`docs/video-to-interactive-assets.html`](./docs/video-to-interactive-assets.html) | 视频 → 可交互工业资产(Video → Interactive Assets) |
| **Direction B** | [`docs/image-to-exchangeable-assets.html`](./docs/image-to-exchangeable-assets.html) | 图片 → 可交换工业资产(Image → Exchangeable Assets) |

---

## 🌐 在线阅读 / Online Reading

部署在 GitHub Pages:
- Direction A: `https://chenzx1300.github.io/embodied-assets-survey/video-to-interactive-assets.html`
- Direction B: `https://chenzx1300.github.io/embodied-assets-survey/image-to-exchangeable-assets.html`

---

## 🎯 核心问题 / Core Question

**具身机器人训练需要海量"机器人做某件事"的数据,但真实遥操作成本极高(数千美元/小时),且仿真器里没有那么多螺丝钉、连接件。**

如何用一段手机视频或一张图片,**几秒钟到几小时内**,自动生成可被 Isaac Sim / MuJoCo / Genesis 读取的**几何精确、物理可信、可交互的工业资产**?

---

## 🔍 调研方法 / Methodology

- **范围**:2025-2026 年 48+ 篇论文 / arXiv / 官方博客 / 产品发布
- **多源对抗式核实**:每条关键论断至少 2 个独立信源
- **量化对比**:几何精度、物理属性、可导出格式、训练成本、sim-to-real gap
- **第一性原理**:从"信息瓶颈"出发,推导 6 条技术路线的合理分工
- **行业全景**:NVIDIA / Google DeepMind / Physical Intelligence / Tesla / Figure / 1X / Unitree / 智元 / 银河智元 / 光轮智能

---

## ⭐ 关键结论 / Key Conclusions

1. **VLM 介入深度谱(0-4 档)**:LLM 不应做主力,只在"语义路由"(档位 2)介入最经济
2. **OVOW + NVIDIA SimFoundry 双引擎**:学术 + 工业互补,无需从零造轮子
3. **光轮智能是数据上游**:80% 头部具身团队都在用其数据,直接合作优于自建
4. **TRELLIS.2 是当前 SOTA 几何生成器**:开源 + 商业可用,优先采用
5. **3 个月实施 MVP**:W1 商务并行启动 + OVOW/SimFoundry 双引擎并行,可压到 12 周

---

## 📊 技术路线速览 / Technical Routes at a Glance

| 路线 | 输入 | 输出 | 工业落地度 |
|---|---|---|---|
| 3.1 2D 像素世界模型 | 视频 | 2D 像素 | ❌ 不适合工业资产 |
| 3.2 4D Gaussian Splatting | 视频 | 4D 高斯点云 | ⚠️ 可视化好,仿真差 |
| 3.3 视频重建 + 物理反演 | 视频 | USD/URDF | ✅ 接近落地 |
| 3.4 Cosmos + Newton 混合 | 视频 | USD 场景 | ✅ NVIDIA 官方推荐 |
| **3.5 VLM + 专用几何** ★ | 视频/图片 | URDF/USD | ✅ **★★★★★ 最高** |
| 3.6 3D-first 视频生成 | 3D | 4D 视频 | ⚠️ 工业暂不适用 |

---

## 🛠️ 本地预览 / Local Preview

```bash
# 在仓库根目录直接打开浏览器:
open docs/video-to-interactive-assets.html
open docs/image-to-exchangeable-assets.html

# 或起一个本地服务器:
python -m http.server 8000
# 然后访问 http://localhost:8000/docs/video-to-interactive-assets.html
```

---

## 📅 版本历史 / Version History

| 版本 | 日期 | 重大变更 |
|---|---|---|
| **v3 重写版** | 2026-10-11 | VLM 介入深度谱 (0-4) 骨架;§7 实施路径压到 12 周 |
| v2 扩展版 | 2026-Q3 | 加入 OVOW + SimFoundry |
| v1 初版 | 2026-Q2 | 6 条技术路线初稿 |

---

## 📝 引用 / Citation

```bibtex
@misc{chen2026_embodied_assets_survey,
  author = {Zhou, Xing Chen},
  title = {Generating Interactive Industrial Assets for Embodied Robot Training: A Deep Survey},
  year = {2026},
  month = {10},
  url = {https://github.com/chenzx1300/embodied-assets-survey}
}
```

---

## 📜 许可证 / License

调研报告采用 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)。
引用的论文 / 产品 / 博客版权归原作者所有。
</content>
</invoke>