# 能力、入口与来源边界

核验日期：2026-09-28。Prompt 方法与平台参数分开；参数写在使用说明，按当前入口确认后交给执行工具。本 Skill 不执行生成。

## 官方已确认

- [ByteDance 发布说明](https://seed.bytedance.com/zh/blog/one-take-creation-flexible-referencing-introducing-seedance-2-5)：2026-07-31；单次最长 30 秒、多轮延长；参考上限 30 图 / 10 视频 / 10 音频；强化白模、动作、编辑。
- [官方 Prompt Writing Guide](https://bytedance.larkoffice.com/docx/A88jd0B47oAd8zxWp5ycZFMfnxh)：本次通过原始文档 UI 读取任务和素材规则；[BytePlus 官方发布页](https://docs.byteplus.com/en/docs/ModelArk/2607689)标记更新于 2026-09-22。
- Guide 的素材表：50 份总上限；视频合计不超过 30 秒，音频合计不超过 30 秒；建议数量与硬上限分开。每份素材写明贡献；多视角不等于多个实例。
- Guide 的任务规则：编辑锁源视频比例与近似时长；首帧/首尾帧锁第一张图比例；延长锁源片比例。多模态参考可以显式指定首尾图。时间戳是预算，非逐帧精确编辑点。
- Guide 的结构规则：分阶段与结束状态；唯一编辑母版；延长先对齐边界；区分粗白模运动骨架与精白模结构重渲染。

## CLI 局部验证

[即梦官方 CLI 入口](https://jimeng.jianying.com/cli)于核验日指向官方 CDN，版本清单 1.4.18（2026-09-10）；本次下载二进制 build `ec1b9fa-dirty`（2026-09-09）。

`text2video -h` 明确列出 `seedance2.5`：4–30 秒、480p/720p/1080p、VIP-only；实际可用性由后端决定。旧本地 build `7eaa4ae-dirty` 未列 2.5。该差异说明不能把安装版能力或 8 月社区文档的分辨率当永久通则。

不据此保证其它入口开放相同规格。无核验时不硬编码 Prompt 字数、模型 ID、价格、地区、分辨率或账号权限。中文/英文素材 token 保留平台实际插入形式，不自行假设它们可以互换。

## 社区材料：供方法比较与案例发现

- [sjinn-ai/seedance2.5-skills](https://github.com/sjinn-ai/seedance2.5-skills)：有官方指南链接、任务拆分与参考权威边界；是社区实现，不是官方 Skill。仅提取可比较的问题，不复制其实现。
- [stimQQ 案例库](https://github.com/stimQQ/awesome-seedance2.5-prompts)：明确区分作者发表的 Prompt 和根据成片重建的 Prompt。重建文本不是原始生成证据。
- [AtlasCloudAI 案例与 Skill](https://github.com/AtlasCloudAI/awesome-seedance-2.5-prompts-skills)：案例面广，但本次 README 仍写 2.0 执行默认及过时的预计发布时间。逐例核对来源与模型，不能用仓库标题证明 2.5 实测。

候选版的合同组合和双语输出规则是本次设计，不冒称官方原文。自写示例只能证明输出可审阅；只有真实提交、终态、媒体读回才算生成证据。单次样例不证明全类型成功率。

## 人物表演补充（2026-09-28）

- [facial-expression-prompting](https://github.com/zhouwei713/facial-expression-prompting)：作者提出动机、反应递进和镜头配合；本版只参考其问题意识，不继承必填动机链、固定时长建议或必须运镜的做法。
- [Seedance-ShotDesign-Skills 表演模块](https://github.com/woodfantasy/Seedance-ShotDesign-Skills/blob/main/references/micro-expressions.md)：按人物特写/情感表演触发加载可供参考；其中关于肌肉时间、面部不对称的精确数值与绝对说法未验证，不纳入。
- 官方指南目录可见 §3.4 Emotional Direction and Observable Performance；本次补充时原文 UI 因电脑锁屏不可用，未复读正文。不把社区对该章的转述升级为官方已核验规则。

表演条件路由来自本次用户明确要求；表现策略为候选设计。两份社区材料均不是表演质量提高的独立实测证明。
