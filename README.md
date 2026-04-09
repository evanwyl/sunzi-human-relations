# art-of-war-relations

![art-of-war-relations cover](README-cover.jpg)

用《孙子兵法》与《三十六计》的思路，分析职场、朋友、情侣、暧昧中的局势、主动权、虚实、进退与低成本动作。

这不是鸡汤 skill，也不是操控指南。
它的目标是把混乱的人际问题，拆成 **可判断、可解释、可行动** 的局势问题。

---

## What this skill does

这个 skill 做三件事：

1. **战略判断**
   - 用《孙子兵法》判断局势、虚实、时机、代价、值不值得动

2. **战术建议**
   - 用《三十六计》给出更具体的试探、换位、延迟、收缩、退出或重塑动作

3. **人物案例库学习**
   - 支持“同一个人一份 case file”
   - 下次再分析这个人时，先读档案，再结合兵法判断
   - 默认自动读，不自动写，只有用户明确触发才沉淀

---

## Good for

- 职场关系，抢功、甩锅、边缘化、资源争夺、领导拉扯
- 朋友关系失衡，边界不清，投入不对等，隐性不满
- 情侣冲突，冷战，修复，是否继续投入
- 暧昧关系，忽冷忽热，节奏权，试探，要不要摊牌
- 需要回复话术、判断对方意图、决定推进还是后撤

## Not for

- 骚扰、威胁、报复、羞辱、恶意操控
- 把所有正常关系都阴谋化
- 用兵法包装伤害行为

---

## Core design

这个 skill 不是一次性问答模板，而是三层结构：

### 1. Principles layer
位置：`references/principles.md`

作用：
- 用《孙子兵法》做战略层判断
- 解决“这是什么局、该不该动、先守还是先试”

### 2. Tactics layer
位置：`references/stratagems.md`

作用：
- 用《三十六计》做动作层建议
- 解决“怎么试探、怎么转向、怎么退出、怎么拿回主动权”

### 3. Case layers

#### 通用案例池
位置：`references/case-bank.md`

作用：
- 存高频局型
- 帮 skill 更快识别“这是哪种关系局”
- 不绑定具体某个人

#### 人物案例库
位置：`cases/people/*.md`

作用：
- 存某一个具体人的互动模式
- 支持按人物持续学习
- 让 skill 不必每次都从零开始判断

---

## Learning workflow

这个 skill 支持一个可成长的人物案例库机制。

### 默认规则

- **自动读，不自动写**
- 如果当前问题明显指向同一个人，优先读取对应人物档案
- 只有当用户明确说“沉淀这个人 / 记进案例库 / 把这段存进档案”时，才写回人物档案

### 为什么这样设计

因为这套机制要同时满足两件事：
- 真能成长
- 又不乱写、不越界、适合开源复用

所以我选择：
- 读取尽量顺滑
- 写入必须明确触发

详细规则看：`references/learning-workflow.md`

---

## Directory structure

```text
art-of-war-relations/
├── SKILL.md
├── README.md
├── cases/
│   ├── README.md
│   ├── people/
│   └── indexes/
│       ├── people-index.md
│       └── relationship-types.md
└── references/
    ├── boundaries.md
    ├── case-bank.md
    ├── case-file-template.md
    ├── diagnostic-cards.md
    ├── examples.md
    ├── learning-workflow.md
    ├── output-patterns.md
    ├── principles.md
    ├── scenario-mapping.md
    └── stratagems.md
```

---

## How to use

### 普通使用

直接提问题，例如：
- 同事总说是开玩笑，我该怎么回
- 前任突然找我，是想复合吗
- 这个朋友总是我主动，我还要继续吗

### 使用人物案例库

当某个人反复出现时：
1. 先给这个人建立一个 case file
2. 后续继续分析这个人时，skill 可以先读这个档案
3. 当你想把一次新互动沉淀进去时，明确说：
   - 沉淀这个人
   - 记进案例库
   - 把这段存进这个人的档案

---

## Naming convention

推荐文件名：
- `coworker-xiaowang.md`
- `friend-ahui.md`
- `ambiguous-chenchen.md`
- `ex-lulu.md`

推荐关系类型：
- coworker
- manager
- subordinate
- friend
- partner
- ex
- ambiguous
- family
- client
- collaborator

更详细的命名约定看：
- `cases/indexes/relationship-types.md`
- `references/case-file-template.md`

---

## Output style

好的输出不只给结论，还要给：
- 局势判断
- 主动权判断
- 建议 / 不建议
- 为什么这样建议
- 兵法依据
- 依据为什么成立

也就是说，这个 skill 不该只会说“用某某计”。
它必须说清楚：
- 为什么这条依据适合当前局
- 为什么这个动作比另一个更划算

---

## Important boundaries

- 人物案例库用来识别模式，不是用来神化猜心
- 不靠一次互动就给一个人永久定性
- 新记录可以修正旧判断
- 技巧服务于判断，不服务于伤害
- 能直接、体面、清楚解决的问题，不必硬套兵法

---

## Files to read first

如果你在维护或扩展这个 skill，最值得先看的文件是：

- `SKILL.md`
- `references/learning-workflow.md`
- `references/case-file-template.md`
- `references/case-bank.md`
- `references/examples.md`
- `cases/README.md`

---

## Open source note

这个 skill 的设计目标，不只是“我自己能用”，而是：
- 别人下载后也能直接看懂
- 不依赖私人记忆系统才能工作
- 可以自己补人物案例，逐步成长
- 架构完整，但不强塞预置私人案例

如果你想让它更强，优先补：
- 更难的通用案例
- 更多人物 case files
- 更细的场景子类型
- 更成熟的命中与读取规则

---

## Recommended release standard

如果要公开放到 GitHub，我建议至少满足这四条：

1. **原则层能独立阅读**
   - `references/principles.md` 不只是列句子
   - 每条原则都能回答“为什么适用、什么时候别乱用”

2. **战术层不鼓励误用**
   - `references/stratagems.md` 要区分“推荐动作”和“风险警示”
   - 不能把三十六计写成操控教程

3. **案例层能看出真实打法**
   - 至少有一批高频局型
   - 最好再带几条完整示例问答

4. **人物案例库机制讲清楚**
   - 自动读，不自动写
   - 只有用户明确触发才沉淀
   - 别让下载者靠猜规则使用

## Suggested next improvements

后续如果继续往上打磨，优先级我建议是：

- 补更多高频局型，尤其是复杂职场和高冲突情侣场景
- 增加 6 到 10 条完整示例问答
- 做一版英文 README 或双语说明，方便开源传播
- 增加更多“误用边界”案例，防止被理解成操控术
