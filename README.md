<div align="center">

# 李可老中医 · 思维操作系统

**用AI复现一代中医急危重症大师的辨证思维**

> 「难症痼疾，师法仲景。」—— 李可

[![GitHub Stars](https://img.shields.io/github/stars/jangviktor-web/likeskill?style=flat-square&logo=github)](https://github.com/jangviktor-web/likeskill/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/jangviktor-web/likeskill?style=flat-square&logo=github)](https://github.com/jangviktor-web/likeskill/network/members)
[![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](https://github.com/jangviktor-web/likeskill/blob/master/LICENSE)
[![ClawHub](https://img.shields.io/badge/ClawHub-install%20like-green?style=flat-square)](https://clawhub.ai/skills/like)
[![Version](https://img.shields.io/badge/version-v2.0.1-blue?style=flat-square)]()
[![Cases](https://img.shields.io/badge/医案-423-green?style=flat-square)]()
[![Formulas](https://img.shields.io/badge/方剂-120+-orange?style=flat-square)]()
[![Symptoms](https://img.shields.io/badge/症状路由-92-yellow?style=flat-square)]()
[![False Syndromes](https://img.shields.io/badge/假证识别-24-red?style=flat-square)]()
[![Score](https://img.shields.io/badge/验证评分-91.3/100-brightgreen?style=flat-square)]()

[⏬ 快速安装](#-快速安装) · [🎯 项目简介](#-项目简介) · [✨ 核心特性](#-核心特性) · [🚀 快速开始](#-快速开始) · [📚 详细使用](#-详细使用) · [⚙️ 配置说明](#️-配置说明)

</div>

---

## ⏬ 快速安装

```bash
# 方式一：ClawHub安装（推荐）
clawhub install like

# 方式二：GitHub克隆
git clone https://github.com/jangviktor-web/likeskill.git
cp -r likeskill/ ~/.claude/skills/like-perspective/

# 方式三：手动下载
# 从 GitHub Releases 下载 zip，解压到 Claude Code skills 目录
```

---

## 🎯 项目简介

**李可老中医**（1930-2013），山西灵石人，52年临床实践，擅以重剂附子救治急危重症，自创方剂28首，累计治疗器质性心脏病约6000例，其中1000+例为西医放弃治疗的病危患者。被邓铁涛誉为"中医的脊梁"。

本skill基于**13个来源**（11本著作+2篇访谈），经过多轮蒸馏、验证、优化，将李可的辨证思维完整转化为AI可执行的知识系统。

**解决什么问题**：让AI能够像李可一样思考——遇到心衰知道用破格救心汤，遇到假阳证能识别出来不误治，遇到经方能给出精确剂量。

**核心优势**：不是简单的医案堆砌，而是完整的**思维操作系统**——从症状到辨证到方剂的全链路路由，24种假证识别防止误诊。

---

## 🖼️ 演示

<div align="center">

```
用户问："一个老人发烧39度，但怕冷，脉沉细，怎么治？"

AI回答：
┌─────────────────────────────────────────────┐
│ 辨证分析                                     │
│ 此为少阴病·假阳证。                          │
│ 发烧+怕冷看似太阳伤寒，但脉沉细为少阴提纲。   │
│ 高热是阴盛格阳之假象，不可清热。              │
├─────────────────────────────────────────────┤
│ 李可思路                                     │
│ 「生死关头，救阳为急。」                      │
│ 「目赤、咽痛、高热俱属假象。」                │
├─────────────────────────────────────────────┤
│ 方剂建议                                     │
│ · 方名：四逆汤                               │
│ · 组成：制附子30g，干姜30g，炙甘草60g        │
│ · 用法：武火急煎，频服                       │
│ · 加减：兼表证合麻黄附子细辛汤               │
├─────────────────────────────────────────────┤
│ 注意事项                                     │
│ · 切忌误用寒凉退热药（银翘散、板蓝根等）      │
│ · 详见 modules/05_zhenghou.md 假阳证章节      │
└─────────────────────────────────────────────┘
```

</div>

---

## ✨ 核心特性

- **🏥 423个真实医案**：心衰61例+中风10例+肺病41例+肿瘤51例+其他260例，每例含完整四诊、处方、剂量、疗效

- **🔍 24种假证识别**：目赤≠肝火、高热≠实热、面红≠肝阳上亢、无苔舌≠阴虚——辨证不出错才能治对病

- **💊 120+首经方剂量**：附子30-200g、细辛45-120g、麻黄30-90g——汉代一两=15.625g，经考古验证

- **🧭 92种症状直通路由**：用户说什么→skill查什么，从症状直接到辨证到方剂的全链路

- **🧠 5个心智模型**：阳气为本、六经辨证统百病、经方基础有效量、顾肾气保胃气、破格用药救危亡

- **📋 105+关键词索引**：覆盖常见疾病47种+方剂31首+理论27条，精确到文件和医案编号

---

## 🚀 快速开始

### 第一步：安装

```bash
clawhub install like
```

### 第二步：激活

当用户提到以下场景时自动激活：

```
"心衰怎么急救？"
"附子用量多少？"
"发烧但怕冷，脉沉细，是什么证？"
"李可怎么看糖尿病？"
"用李可的视角分析这个病案"
```

### 第三步：使用

```bash
# 在Claude Code中直接提问
# AI会自动加载李可skill并回答

用户：一个78岁老人，心衰晚期，四肢冰冷，血压测不到，怎么急救？

AI：（自动加载 cases/01_xinshuai.md + modules/03_jingfang.md）
    辨证分析 → 李可思路 → 破格救心汤大剂（附子200g）→ 注意事项
```

---

## 📚 详细使用

### 场景一：急危重症急救

```bash
# 心衰急救
用户："病人昏迷不醒，测不到血压，四肢冰冷"
→ skill自动加载 cases/01_xinshuai.md
→ 输出：破格救心汤大剂（附子200g，干姜60g，炙甘草60g...）

# 中风急救
用户："中风昏迷，半身不遂"
→ skill自动加载 cases/02_zhongfeng.md + modules/03_jingfang.md
→ 输出：续命煮散（孙思邈方）或三生饮急救
```

### 场景二：假证识别

```bash
# 假阳证
用户："病人发烧39度，但怕冷，脉沉细"
→ skill自动加载 modules/05_zhenghou.md
→ 输出：此为假阳证，四逆汤回阳，不可清热

# 真寒假热
用户："面红如妆，口渴，但手脚冰凉"
→ skill自动加载 modules/05_zhenghou.md
→ 输出：戴阳证，四逆汤回阳
```

### 场景三：慢性病调理

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

### 场景四：经方剂量查询

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

---

## ⚙️ 配置说明

### 文件结构

| 文件 | 行数 | 说明 |
|------|------|------|
| `SKILL.md` | 794 | 主文件：心智模型+决策启发式+速查表+关键词索引+表达DNA |
| `knowledge-network.md` | 207 | 知识网络：92种症状路由+24种假证识别+六经路由 |
| `cases/01_xinshuai.md` | 856 | 心衰医案61个 |
| `cases/02_zhongfeng.md` | 269 | 中风医案10个 |
| `cases/03_feibing.md` | 529 | 肺病医案41个 |
| `cases/04_zhongliu.md` | 809 | 肿瘤医案51个 |
| `cases/05_other.md` | 3179 | 其他医案260个 |
| `modules/01_yangqi.md` | 525 | 阳气理论+假阳证+春夏养阳+高血压+凉茶+肥胖+肿瘤 |
| `modules/02_shanghan.md` | 336 | 六经辨证+彭子益圆运动理论 |
| `modules/03_jingfang.md` | 1797 | 经方有效量+附子煎服法+瞑眩反应+方剂索引120+首 |
| `modules/04_peiyuan.md` | 104 | 培元固本散 |
| `modules/05_zhenghou.md` | 144 | 辨证要点与假证识别 |
| `modules/06_maifa.md` | 139 | 脉诊经验 |

### 知识路由配置

```
用户问题 → SKILL.md速查表 → 直接回答
         → cases/对应文件 → 医案查询
         → modules/对应文件 → 理论查询
         → knowledge-network.md → 症状路由
```

### 触发词配置

| 触发词 | 说明 |
|--------|------|
| `李可` | 通用触发 |
| `用李可的视角` | 角色扮演触发 |
| `心衰怎么急救` | 急危重症触发 |
| `附子用量` | 经方剂量触发 |
| `假阳证` | 假证识别触发 |
| `破格救心汤` | 方剂查询触发 |
| `六经辨证` | 理论查询触发 |

---

## 🤝 贡献指南

欢迎贡献医案、方剂、理论内容！

1. Fork 本仓库
2. 创建特性分支：`git checkout -b feature/add-cases`
3. 提交更改：`git commit -m 'feat: 添加XX医案'`
4. 推送分支：`git push origin feature/add-cases`
5. 创建 Pull Request

### 内容规范

- 医案必须有**真实患者信息**（姓名、年龄、诊断）
- 处方必须有**具体剂量**（不要写"适量"）
- 必须标注**来源**（哪本书、哪篇访谈）
- OCR错误必须**修正后**再提交

---

## 📄 开源协议

本项目采用 [MIT License](https://github.com/jangviktor-web/likeskill/blob/master/LICENSE) 开源。

**重要声明**：
- 本skill仅供学习参考，不能替代专业医疗建议
- 大剂量用药需在有经验的中医师指导下使用
- 临床处方须由执业中医师开立
- 李可逝世于2013年，对之后的疾病无直接经验

---

## 🙏 致谢

- **李可老中医**：一代中医急危重症大师，毕生致力于中医复兴
- **孙其新教授**：整理出版《李可经方基础有效量》《李可六经辨证学》等著作
- **张涵**：李可弟子，《跟师李可抄方记》作者，提供第一手跟师记录
- **雒晓东**：《李可医案处方集》编著者
- **邓铁涛国医大师**：题词"李可老中医是中医的脊梁"

### 相关项目

- [倪海厦skill](https://github.com/jangviktor-web/nihaixia-skill)：倪海厦中医思维操作系统（全科教学型）
- [Claude Code Skills](https://github.com/anthropics/skills)：Anthropic官方Claude Code技能库
- [ClawHub](https://clawhub.ai)：AI技能市场

---

<div align="center">

**如果这个项目对你有帮助，请给个Star支持一下**

[![Star History Chart](https://api.star-history.com/svg?repos=jangviktor-web/likeskill&type=Date)](https://star-history.com/#jangviktor-web/likeskill&Date)

---

> 「我一生所用附子超过5吨之数，经治病人在万例以上，从无1例中毒。」
> —— 李可（1930-2013）

</div>
