# ThinkCut

[English README](README.md)

ThinkCut 是一个 Codex Skill，用来把模糊想法切成清晰判断、关键假设、压力测试和最小验证行动。

它适合处理产品想法、功能取舍、策略问题、执行计划、内容选题，或者任何“听起来有意思，但还不知道该不该做、怎么验证”的方案。

## 它解决什么问题

ThinkCut 会帮助 Agent 从这样的输入：

```text
我想做一个旅游搭子的小程序。
```

推进到这样的输出：

```text
决策：
先不要开发完整小程序。

关键假设：
旅行者愿意信任一个轻量匹配流程，并愿意见陌生搭子。

压力测试：
微信群、小红书、豆瓣、旅行社区等替代方案可能已经足够解决需求。

最小验证：
先用人工撮合的方式测试 20 个旅游搭子请求，再决定是否开发。
```

它的目标不是帮你想出更多点子，而是把模糊想法压成可以行动的下一步。

## 工作流

ThinkCut 使用五步流程：

1. **问题校准**
   把用户的模糊想法重述成一个具体决策。

2. **假设拆解**
   区分事实、假设、惯例和缺失证据。

3. **压力测试**
   找出可能让方案失败的关键分支。

4. **最小验证**
   找到成本最低、反馈最快、假设最少的验证动作。

5. **决策简报**
   输出当前判断、关键风险、验证方式、成功标准和下一步行动。

## 使用的方法论

ThinkCut 组合了这些方法：

- 苏格拉底式提问：用于校准问题
- 第一性原理：用于拆解假设和惯例
- 有边界的压力测试：用于发现关键风险
- 奥卡姆剃刀：用于降低复杂度
- 决策记录：用于固定判断和下一步行动

## 安装

克隆仓库，并复制到本机 Codex skills 目录：

```bash
git clone https://github.com/diyewu/ThinkCut.git
cd ThinkCut
mkdir -p ~/.codex/skills/thinkcut
rsync -a --exclude .git ./ ~/.codex/skills/thinkcut/
```

安装后需要重启 Codex，新的 skill 才会被识别。

如果你要安装当前实现分支：

```bash
git clone -b codex/implement-thinkcut https://github.com/diyewu/ThinkCut.git
cd ThinkCut
mkdir -p ~/.codex/skills/thinkcut
rsync -a --exclude .git ./ ~/.codex/skills/thinkcut/
```

## 使用方式

显式调用最稳定：

```text
$thinkcut 我想做一个旅游搭子小程序，帮我拆成关键假设、压力测试和最小验证方案。
```

也可以这样用：

```text
$thinkcut 帮我判断这个功能要不要做。
```

```text
$thinkcut 压力测试一下我的产品方案，并给我最小验证动作。
```

```text
$thinkcut 我有一个内容选题，帮我判断是否值得做。
```

## 标准输出

ThinkCut 通常会以一个简短的决策简报收尾：

```text
Decision:
Current judgment:
Facts:
Key assumptions:
Conventions to ignore:
Stress Pass:
Minimal validation:
Success criteria:
Failure signal:
Next action:
What would change the decision:
```

## 仓库结构

```text
ThinkCut/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── LICENSE
├── README.md
└── README.zh-CN.md
```

## License

ThinkCut 使用 Apache License, Version 2.0 开源。详见 [LICENSE](LICENSE)。
