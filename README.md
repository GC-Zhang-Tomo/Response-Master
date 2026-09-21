# Lab Reviewer Response

一个面向科研论文返修阶段的 Codex skill。它在初投稿件已经收到编辑或审稿人意见后使用，可完成：

1. 根据审稿意见、补充实验结果和导师要求撰写 point-by-point response；
2. 生成可由另一模型直接执行的 manuscript revision map；
3. 根据修改清单生成红字标记的 revised manuscript；
4. 检查 response、修改清单和 revised manuscript 之间的一致性。

## 适用范围

本 skill 只用于投稿后的返修阶段。它不用于投稿前润色，也不用于替审稿人撰写 peer-review report。

建议输入：

- 初次投稿的 manuscript；
- 完整的 editor/reviewer comments；
- 补充实验或分析结果，以及计划修改的内容；
- 导师或课题组的额外要求。

默认输出：

- `<short-title>_point_by_point_response.docx`
- `<short-title>_manuscript_revision_map.docx`
- `<short-title>_revised_red.docx`（需要实际修改稿时）

## 组内格式

- reviewer comment：黑色斜体；
- `REPLY:`：蓝色、粗体；
- response 正文：蓝色；
- response 中引用的修改后原文：蓝色斜体；
- revised manuscript 中新增或替换的文字：纯红色 `#FF0000`；
- 不把计划实验表述为已完成实验，不虚构数据、统计量、图号或参考文献。

详细规则见 [SKILL.md](SKILL.md) 和 [references](references)。

## 安装

将仓库克隆到某个项目的 `.agents/skills` 下：

```powershell
git clone <repository-url> .agents/skills/lab-reviewer-response
```

也可以放入个人 Codex skills 目录。重新打开项目后，Codex 应能读取 `SKILL.md` 并按描述触发该 skill。

## 可选脚本依赖

模板生成和结构检查脚本需要 Python 及 `python-docx`：

```powershell
python -m pip install -r requirements.txt
```

- `scripts/build_templates.py`：重新生成两个 Word 模板；
- `scripts/check_outputs.py`：检查 response、revision map 和红字 manuscript 的基本结构与格式。

## 数据边界

本仓库只包含通用规则、空白模板和检查脚本，不包含用于提炼风格的历史论文、审稿意见、实验数据或课题组未发表内容。实际返修材料应保存在受控工作目录中，不应提交到本仓库。

## 当前状态

当前为 demo 版本。格式规则由两套较完整的历史返修材料提炼而来；在用于正式投稿前，仍应由作者逐项核对科学事实、数字、统计结果、图表位置和最终措辞。
