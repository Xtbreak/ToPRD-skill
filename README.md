# ToPRD-skill

从一个想法或已有项目生成可提交的 AI 产品 PRD。信息不足时先提问，再根据用户回答润色并保留核心内容。

默认输出 `AI产品PRD.md`。用户可分别选择额外的 `项目实现详解.md` 和 `项目面试问答.md`，项目面试题与连续追问结合实际代码、决策和本人经历生成。

## PRD 结构

1. 产品概述
2. 用户与需求场景
3. 版本范围与用户流程
4. 功能需求与规则
5. AI 评测与模型选型
6. 验收与上线效果
7. 交付计划与依赖

正式文档保留项目内容。问题在对话中解决。经用户确认的 **当前未做评测** 等实际状态，在正文中加粗呈现。

## 使用

把本仓库放到宿主的 skills 目录并命名为 `toprd-skill`，或将仓库链接到该目录。Codex 本地安装示例，目标目录应为空闲名称。

```bash
ln -s /你的仓库路径/ToPRD-skill ~/.codex/skills/toprd-skill
```

新会话中调用 `$toprd-skill`，例如“我想做一个论文 PDF 问答工具，帮我从零写 PRD”，或“根据这个项目目录补一份当前版本的 PRD”。也可单独要求项目详解或面试问答。具体能力取决于宿主是否能读取文件、运行项目和浏览资料。

入口为 [SKILL.md](SKILL.md)，按模式读取 references 下的规范。行为验证场景见 [tests/scenarios.md](tests/scenarios.md)。

## 来源与许可

基于 Digidai/product-manager-skills 的 PRD 方法进行改编，新增反推流程、七节 AI PRD、对话补全规则和可选面试材料。采用 CC BY-NC-SA 4.0，来源、版本及改编范围见 [ATTRIBUTION.md](ATTRIBUTION.md)，许可证见 [LICENSE](LICENSE)。
