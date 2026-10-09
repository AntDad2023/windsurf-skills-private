# Master-Paper-Reviewer

中文学位论文（硕士／博士、MPA／MBA 等专业学位论文）评审技能。

纯指令型技能：**无脚本、无外部依赖、不联网**，拷贝即可用。

---

## 一、用途

用于中国高校**学位论文**的评审与修改稿复核：

- 题目—内容主线切题性检验（防止"文题不符"被盲审否决）
- 章节结构主线、理论不悬空、问题—对策对应
- 对策落地性（责任到岗位、工作量测算、试点与兜底）
- 实证可信度（抽样框、信效度、内生性、数值自洽）
- GB/T 7713.1—2006 与 GB/T 7714—2015 格式规范
- 送审与答辩视角
- 多轮修改的**零基准复审**

不适用：期刊论文评审。期刊论文请用配套技能 `academic-paper-reviewer`。

---

## 二、文件清单与校验值

| 文件 | 大小 | git blob SHA-1 | SHA-256 |
|---|---|---|---|
| `SKILL.md` | 10576 B | `18caa3c1a42454ee83fabc8296beba695f87579c` | `48f9c8d378f736ff23f37fca83f14fcdca7dc9cfe342ffd9b3f5b39bdc338558` |

版本 1.0.0 ／ 建立日期 2026-10-05。

---

## 三、安装

把 `Master-Paper-Reviewer/` 整个目录放到目标机器的技能目录下即可：

```
# WorkBuddy（用户级，推荐）
~/.workbuddy/skills/Master-Paper-Reviewer/SKILL.md

# Claude Code 风格
~/.claude/skills/Master-Paper-Reviewer/SKILL.md

# 项目级（只对当前项目生效）
<项目目录>/.workbuddy/skills/Master-Paper-Reviewer/SKILL.md
```

**要求**：目录名必须与 `SKILL.md` frontmatter 中的 `name: Master-Paper-Reviewer` 完全一致。

---

## 四、在另一台机器上获取

本仓库为**私有仓库**，需先授权 GitHub 账号：

```bash
git clone https://github.com/AntDad2023/windsurf-skills-private.git
# 只取本技能
cp -r windsurf-skills-private/Master-Paper-Reviewer ~/.workbuddy/skills/
```

单文件下载（需带 token 的 API 或网页登录后下载 raw）：

```
https://raw.githubusercontent.com/AntDad2023/windsurf-skills-private/master/Master-Paper-Reviewer/SKILL.md
```

---

## 五、校验下载是否完整

```bash
sha256sum SKILL.md
# 期望：48f9c8d378f736ff23f37fca83f14fcdca7dc9cfe342ffd9b3f5b39bdc338558

# macOS
shasum -a 256 SKILL.md
```

---

## 六、加载自检

安装后在对话中提一句"用 Master-Paper-Reviewer 评阅这篇学位论文"，技能应被触发。若未被识别，按顺序检查：

1. 目录名与 `name` 字段是否一致；
2. `SKILL.md` 首行是否为 `---`（frontmatter 起始符），第 11 行是否为 `---`（结束符）；
3. 文件编码是否仍为 UTF-8（无 BOM）；
4. 技能列表缓存是否需重建（WorkBuddy 可清理 `.skill-list-cache.json` 后重启）。

---

## 七、维护

由使用者按评审实践迭代。修订后在 `SKILL.md` 的 `metadata.version` 与 `## 版本` 表中同步更新，并刷新本文件第二、五节的校验值。
