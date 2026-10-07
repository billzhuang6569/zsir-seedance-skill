# Seedance 2.0 视频 Prompt 生成器

以导演视角理解创作意图，补全叙事逻辑，为 Seedance 2.0（即梦 AI）生成结构化的中文和英文视频提示词。

## 功能

- 支持纯文字生成、首尾帧和全能参考三种创作模式。
- 从叙事、情绪和镜头动机出发设计画面，按场景复杂度控制提示词长度。
- 结合图片、视频和音频素材分配参考角色。
- 输出导演思路、中英文 Prompt，以及时长、入口和素材使用建议。
- 附带运镜、光影、景别、转场和声音关键词库。

## 安装

### Claude Code

安装到个人技能目录：

```bash
git clone https://github.com/billzhuang6569/zsir-seedance-skill.git ~/.claude/skills/seedance-prompt
```

也可以安装到项目中的 `.claude/skills/seedance-prompt` 目录。

### Codex

安装到个人技能目录：

```bash
git clone https://github.com/billzhuang6569/zsir-seedance-skill.git ~/.agents/skills/seedance-prompt
```

也可以安装到项目中的 `.agents/skills/seedance-prompt` 目录。安装后重新启动相应 Agent 会话，让它发现新技能。

### 其他支持 Agent Skills 的工具

将本仓库下载到工具的技能目录，保留 `SKILL.md` 与 `references/` 的相对位置。具体加载方式以工具文档为准。

## 使用

在支持该技能的 Agent 中提出视频提示词需求，例如：

> 帮我用 Seedance 写一个 8 秒视频提示词：下班后，一个女孩站在雨中的公交站，发现末班车已经离开。情绪克制，单镜头，中英双版本。

也可以提供图片、视频或音频参考，并说明希望采用首尾帧或全能参考模式。

技能会输出：

1. 创作模式。
2. 导演思路：素材识读、叙事解读、情绪目标、镜头设计及复杂度定级。
3. 中文 Prompt 和 English Prompt。
4. 使用建议。

本 Skill 负责生成提示词。视频生成需要在即梦或其他支持 Seedance 的平台中完成；平台规格以实际界面和最新文档为准。

## 文件

```text
SKILL.md                 技能定义与创作工作流
references/keywords.md   中英文镜头与视听关键词库
LICENSE                  MIT 开源许可证
```

## 来源

由作者从自己的 [一探 SkillHub 技能商店](https://sk.woe.show/marketplace/skills/862a3c6d-8534-4987-81ef-76ccac8b5962) 发布。`SKILL.md` 和 `references/keywords.md` 保留下载包中的原始内容。

## 许可证

[MIT](LICENSE)。允许使用、修改和再分发，请保留版权声明和许可证。
