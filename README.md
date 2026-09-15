# AI 面试练习 Skill

帮助学生基于目标岗位与自己的简历，完成低成本、贴近岗位且有回答证据支撑的面试练习。

**闭环：岗位与简历 → 一次一题 → 按回答追问 → 引用原话的分项报告 → 修改重答。**

## 能做什么

- 根据 JD 与简历匹配能力和问题；没有 JD 时显式使用通用岗位假设。
- 追问个人贡献、方法、指标口径、取舍和矛盾之处。
- 用回答 ID 与逐字引用支持 0–4 级分项反馈，未覆盖项标记未评估。
- 给出具体练习动作与完成标准，支持中途结束、跳过和重答对比。
- 支持中文、英文、技术与非技术岗位；默认 5 道主问题、每题最多 2 次追问。

## 安装

将本仓库的 `skills/ai-interview` 文件夹复制到 Codex 技能目录：

```bash
git clone https://github.com/Lntanohuang/ai-interview-skill.git
mkdir -p ~/.codex/skills
cp -R ai-interview-skill/skills/ai-interview ~/.codex/skills/
```

如已安装同名技能，请先比较文件再更新；自定义 `CODEX_HOME` 时使用其下的 `skills` 目录。重新开始会话后，用 `$ai-interview` 调用。其他支持 `SKILL.md` 的助手可按各自技能目录规则安装。

本技能是给 AI 助手执行的对话规范，不是独立应用。无需额外 API、数据库或付费题库；实际模型使用费用取决于宿主平台。

## 最小输入示例

```text
使用 $ai-interview。
目标岗位：数据分析实习生。
JD：SQL 数据清洗、转化漏斗分析、结果沟通。
我的简历：统计学大三；做过模拟电商数据课程项目，
我负责 SQL 去重与缺失值处理，使用 Excel 分析订单分布，没有真实业务上线。
请用中文练习 3 道主问题，一次只问一题，按我的回答追问，最后引用原话给报告。
```

- [更多输入示例与空白模板](examples/input-examples.md)
- [完整问答—追问—引用—反馈—重答示例](examples/full-session.md)
- [技能指令](skills/ai-interview/SKILL.md)
- [评分与报告规范](skills/ai-interview/references/rubric-and-report.md)

## 反馈边界

报告衡量本次回答表现，不预测录用，不替招聘方做决策。简历内容不自动当作已验证能力；缺少回答证据时不虚构分数或经历。建议输入匿名简历摘要。技能不主动向第三方发送材料；对话仍受所使用 AI 平台的数据处理设置约束。

仓库中的简历与对话均为虚构教学示例，不包含真实学生资料。
