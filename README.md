<div align="center">

[English Version](#english-version) | **中文**

# 李可老中医 · 思维操作系统

**用AI复现一代中医急危重症大师的辨证思维**

> 「难症痼疾，师法仲景。」—— 李可

[![GitHub Stars](https://img.shields.io/github/stars/jangviktor-web/likeskill?style=flat-square&logo=github)](https://github.com/jangviktor-web/likeskill/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/jangviktor-web/likeskill?style=flat-square&logo=github)](https://github.com/jangviktor-web/likeskill/network/members)
[![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](https://github.com/jangviktor-web/likeskill/blob/master/LICENSE)
[![ClawHub](https://img.shields.io/badge/ClawHub-install%20like-green?style=flat-square)](https://clawhub.ai/skills/like)
[![Version](https://img.shields.io/badge/version-v2.0.2-blue?style=flat-square)]()
[![Cases](https://img.shields.io/badge/医案-423-green?style=flat-square)]()
[![Formulas](https://img.shields.io/badge/方剂-120+-orange?style=flat-square)]()
[![Score](https://img.shields.io/badge/验证评分-99/100-brightgreen?style=flat-square)]()

[⏬ 快速安装](#-快速安装) · [🎯 项目简介](#-项目简介) · [✨ 核心特性](#-核心特性) · [🚀 快速开始](#-快速开始) · [📚 详细使用](#-详细使用) · [📋 更新日志](#-更新日志)

</div>

---

## ⏬ 快速安装

```bash
# 方式一：ClawHub安装（推荐）
clawhub install like

# 方式二：GitHub克隆
git clone https://github.com/jangviktor-web/likeskill.git
cp -r likeskill/ ~/.claude/skills/like-perspective/
```

---

## 🎯 项目简介

**李可老中医**（1930-2013），山西灵石人，52年临床实践，擅以重剂附子救治急危重症，自创方剂28首，累计治疗器质性心脏病约6000例。

本skill将李可的辨证思维完整转化为AI可执行的知识系统——从症状到辨证到方剂的全链路路由，24种假证识别防止误诊。

---

## ✨ 核心特性

- **🏥 423个真实医案**：心衰61+中风10+肺病41+肿瘤51+其他260
- **🔍 25种假证识别**：假阳证24种+假阴证1种——辨证不出错才能治对病
- **💊 120+首经方剂量**：附子30-200g、细辛45-120g，考古验证
- **🧭 92种症状直通路由**：从症状直接到辨证到方剂的全链路
- **🧠 5个心智模型**：阳气为本/六经辨证/经方有效量/顾肾气保胃气/破格用药
- **📋 105+关键词索引**：精确到文件和医案编号

---

## 🚀 快速开始

```bash
# 安装
clawhub install like

# 在Claude Code中直接提问
# AI会自动加载李可skill并回答

# 示例1：心衰急救
用户：一个78岁老人，心衰晚期，四肢冰冷，血压测不到
AI：（加载cases/01）破格救心汤大剂，附子200g，武火急煎...

# 示例2：假阳证识别
用户：发烧39度，但怕冷，脉沉细
AI：（加载modules/05）此为假阳证，四逆汤回阳，不可清热

# 示例3：假阴证识别（新增）
用户：四肢厥冷，但脉沉实有力，舌红苔黄
AI：（加载modules/05）此为假阴证，白虎汤或承气汤，不可温阳
```

---

## 📚 详细使用

<details>
<summary>点击展开：场景一 - 急危重症急救</summary>

```bash
# 心衰急救
用户："病人昏迷不醒，测不到血压，四肢冰冷"
→ skill自动加载 cases/01_xinshuai.md
→ 输出：破格救心汤大剂（附子200g，干姜60g，炙甘草60g...）

# 中风急救
用户："中风昏迷，半身不遂"
→ skill自动加载 cases/02_zhongfeng.md
→ 输出：续命煮散（孙思邈方）或三生饮急救
```

</details>

<details>
<summary>点击展开：场景二 - 假证识别</summary>

```bash
# 假阳证（真寒假热）
用户："病人发烧39度，但怕冷，脉沉细"
→ skill自动加载 modules/05_zhenghou.md
→ 输出：此为假阳证，四逆汤回阳，不可清热

# 假阴证（真热假寒）- 新增
用户："四肢厥冷，但脉沉实有力，舌红苔黄"
→ skill自动加载 modules/05_zhenghou.md
→ 输出：此为假阴证，白虎汤或承气汤，不可温阳
```

</details>

<details>
<summary>点击展开：场景三 - 慢性病调理</summary>

```bash
# 糖尿病
用户："糖尿病多年，吃六味地黄丸效果不好"
→ skill自动加载 SKILL.md速查表 + cases/05_other.md
→ 输出：六味地黄丸是错的，用金匮肾气丸，从脾肾阳虚论治

# 高血压
用户："高血压头晕面红"
→ skill自动加载 SKILL.md速查表 + modules/01_yangqi.md
→ 输出：三阴病，浊阴窃踞阳位，温氏奔豚汤，不可平肝潜阳
```

</details>

<details>
<summary>点击展开：场景四 - 经方剂量查询</summary>

```bash
# 附子用量
用户："附子最大能用多少？"
→ skill自动加载 modules/03_jingfang.md
→ 输出：常规30-100g，重症100-200g，危症200-450g，极危可达750g

# 细辛用量
用户："细辛不过钱是真的吗？"
→ skill自动加载 modules/03_jingfang.md
→ 输出：宋代牢头误传，张仲景用三两（45g），李可用40年无问题
```

</details>

---

## ⚙️ 配置说明

<details>
<summary>点击展开：文件结构</summary>

| 文件 | 行数 | 说明 |
|------|------|------|
| `SKILL.md` | 890 | 主文件：心智模型+速查表+关键词索引+知识路由网络+表达DNA |
| `cases/01_xinshuai.md` | 856 | 心衰医案61个 |
| `cases/02_zhongfeng.md` | 269 | 中风医案10个 |
| `cases/03_feibing.md` | 529 | 肺病医案41个 |
| `cases/04_zhongliu.md` | 809 | 肿瘤医案51个 |
| `cases/05_other.md` | 3179 | 其他医案260个 |
| `modules/01_yangqi.md` | 525 | 阳气理论+假阳证+春夏养阳+高血压+凉茶+肥胖+肿瘤 |
| `modules/02_shanghan.md` | 336 | 六经辨证+彭子益圆运动理论 |
| `modules/03_jingfang.md` | 1797 | 经方有效量+附子煎服法+方剂索引120+首 |
| `modules/04_peiyuan.md` | 104 | 培元固本散 |
| `modules/05_zhenghou.md` | 144 | 辨证要点与假证识别 |
| `modules/06_maifa.md` | 139 | 脉诊经验 |

</details>

<details>
<summary>点击展开：知识路由网络</summary>

**问题类型→文件路由**：

| 用户问什么 | 首先查 | 然后查 | 最后查 |
|-----------|--------|--------|--------|
| "XX病怎么治" | SKILL.md速查表 | cases/对应文件 | modules/01 |
| "怎么急救/救命" | SKILL.md速查表 | cases/01或02 | modules/03 |
| "附子/细辛/麻黄用量" | modules/03 | SKILL.md速查表 | — |
| "这是什么证/辨证" | modules/02 | modules/05 | — |
| "假阳证/真假寒热" | modules/05 | modules/01 | — |

**六经辨证路由**：

| 六经 | 提纲关键词 | 主方 |
|------|-----------|------|
| 太阳病 | 发热恶寒、脉浮 | 麻黄汤/桂枝汤 |
| 阳明病 | 但热不寒、脉洪大 | 白虎汤/承气汤 |
| 少阳病 | 往来寒热、口苦咽干 | 小柴胡汤 |
| 太阴病 | 腹满吐利、食不下 | 理中汤 |
| 少阴病 | 脉微细、但欲寐 | 四逆汤/真武汤 |
| 厥阴病 | 消渴、寒热错杂 | 乌梅丸/当归四逆汤 |

</details>

<details>
<summary>点击展开：方剂速查</summary>

| 方剂名 | 主治 | 核心药物 | 剂量范围 |
|--------|------|---------|---------|
| **破格救心汤** | 心衰急救 | 附子、干姜、炙甘草、山萸肉 | 附子30-200g |
| **续命煮散** | 中风 | 麻黄、川芎、附子、细辛、石膏 | 每次4g煮散 |
| **小青龙虚化汤** | 肺心病 | 麻黄、附子、细辛、半夏 | 附子45-200g |
| **攻癌夺命汤** | 肿瘤 | 海藻、甘草、木鳖子、鳖甲 | 各30g |
| **温氏奔豚汤** | 奔豚气、肥胖 | 附子、油桂、沉香、砂仁 | 附子45-200g |
| **四逆汤** | 少阴病 | 附子、干姜、炙甘草 | 附子15-60g |
| **麻黄附子细辛汤** | 太少两感 | 麻黄、附子、细辛 | 各30-45g |
| **乌梅丸** | 厥阴病 | 乌梅、细辛、干姜、黄连 | 乌梅690g |
| **当归四逆汤** | 厥阴经证 | 当归、桂枝、芍药、细辛 | 当归50g、细辛45g |
| **金匮肾气丸** | 肾阳虚 | 肉桂、附子、熟地、山茱萸 | 每次5粒煮糊 |
| **培元固本散** | 慢性病善后 | 紫河车、鹿茸、红参、灵脂 | — |

</details>

---

## 📋 更新日志

<details>
<summary>点击展开：完整更新日志</summary>

### v2.0.2（2026-06-06）

**验证驱动修正**（验证评分89.3→99/100）：
- 修正决策树重复（改为引用Step 2，消除冗余）
- 攻癌夺命汤剂量补充（各30g，源文件核实）
- 温氏奔豚汤标注（附子45-200g，极端450g）
- 假阴证补充（真热假寒条目，防止误用温阳药）
- 速查表与症状路由分工说明（新增第七节）

### v2.0.1（2026-06-06）

**知识网络构建**：
- 构建92种症状直通路由（急症20+慢性病30+疑难杂症18+假证24）
- 优化关键词索引（+80条，总计105+条）
- 构建六经辨证路由（6经+主方+文件位置）
- 构建方剂速查路由（11个核心方剂）

### v2.0.0（2026-06-06）

**医案大扩充**：
- 《李可医案处方集》蒸馏（+262个医案）
- 《跟师李可抄方记·危重症篇》蒸馏（+19个医案）
- 《人体阳气与疾病》蒸馏（朱丹溪批判+彭子益理论）
- 《李可六经辨证学》蒸馏（六经提纲+验方+医案）
- 总医案数：64→423

### v1.2（2026-06-05）

**知识库扩充**：
- 9篇biji.com讲座笔记蒸馏
- 9篇原始视频转录文稿（~167KB）
- 新增决策启发式详细医案
- 新增经典语录

### v1.1（2026-06-05）

**访谈蒸馏**：
- 扶阳论坛演讲（2006年冬至）
- 《南风窗》2007年访谈
- 经方派网站访谈
- 好大夫在线"对话大医李可"

### v1.0（2026-06-05）

**初始版本**：
- 4本核心著作蒸馏
- SKILL.md + 5个cases + 6个modules
- 基础关键词索引

</details>

---

## 🤝 贡献指南

1. Fork 本仓库
2. 创建特性分支：`git checkout -b feature/add-cases`
3. 提交更改：`git commit -m 'feat: 添加XX医案'`
4. 推送分支：`git push origin feature/add-cases`
5. 创建 Pull Request

---

## 📄 开源协议

本项目采用 [MIT License](https://github.com/jangviktor-web/likeskill/blob/master/LICENSE) 开源。

**重要声明**：
- 本skill仅供学习参考，不能替代专业医疗建议
- 大剂量用药需在有经验的中医师指导下使用
- 临床处方须由执业中医师开立

---

## 🙏 致谢

- **李可老中医**：一代中医急危重症大师
- **孙其新教授**：整理出版《李可经方基础有效量》等著作
- **张涵**：李可弟子，《跟师李可抄方记》作者
- **雒晓东**：《李可医案处方集》编著者
- **邓铁涛国医大师**：题词"李可老中医是中医的脊梁"

---

<div align="center">

> 「我一生所用附子超过5吨之数，经治病人在万例以上，从无1例中毒。」—— 李可

**如果这个项目对你有帮助，请给个Star**

[![Star History Chart](https://api.star-history.com/svg?repos=jangviktor-web/likeskill&type=Date)](https://star-history.com/#jangviktor-web/likeskill&Date)

</div>

---

<a id="english-version"></a>

## English Version

**Li Ke TCM · Thinking Operating System**

An AI-powered skill that reproduces the diagnostic thinking of Master Li Ke (1930-2013), a renowned Traditional Chinese Medicine practitioner specializing in critical and emergency conditions.

**Key Features**:
- 423 real medical cases (61 heart failure + 10 stroke + 41 lung disease + 51 cancer + 260 others)
- 25 false syndrome identifications (24 false yang + 1 false yin)
- 120+ classical prescriptions with verified dosages
- 92 symptom-to-diagnosis routing paths
- 105+ keyword index entries

**Installation**:
```bash
clawhub install like
```

**Repository**: https://github.com/jangviktor-web/likeskill
**ClawHub**: https://clawhub.ai/skills/like

**License**: MIT
