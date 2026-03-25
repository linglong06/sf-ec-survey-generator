# SF EC Survey Generator

SAP SuccessFactors Employee Central (EC) 项目调研问卷生成器

## 功能特性

- 生成标准化的SF EC调研问卷Excel文件
- 支持从客户制度文档中提取答案预填充问卷
- 支持中英文双语输出
- 覆盖EC核心模块：组织管理、岗位管理、人事管理等
- 90道专业调研问题

## 工作流程

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  1. 展示问题    │ ──▶ │  2. 用户确认    │ ──▶ │  3. 提取答案    │ ──▶ │  4. 生成问卷    │
└─────────────────┘     └─────────────────┘     └─────────────────┘     └─────────────────┘
  展示完整问题列表        用户确认或调整问题      Claude分析文档          按确认的问题生成Excel
  按类别分组展示          生成临时问题列表        提取SF EC相关信息
```

**重要特性**：
- 在生成问卷前，会先展示完整问题列表供用户确认
- 用户可以修改、添加、删除问题，或精简模块
- ⚠️ 对话中的问题调整**仅影响本次问卷**，不会修改问题库文件

## 安装

### 作为Claude Skill使用

将整个目录复制到 `~/.claude/skills/` 目录下：

```bash
cp -r sf-ec-survey-generator ~/.claude/skills/
```

### 独立使用

```bash
# 安装依赖
pip install openpyxl

# 运行脚本
python scripts/generate_survey.py -o ./survey.xlsx
```

## 使用方法

### 基本用法

```bash
# 生成完整的双语问卷
python scripts/generate_survey.py -o ./survey.xlsx

# 仅生成组织管理和岗位管理模块
python scripts/generate_survey.py -o ./survey.xlsx -c 组织管理 岗位管理

# 仅生成中文版本
python scripts/generate_survey.py -o ./survey.xlsx -l cn
```

### 从制度文档提取答案

```bash
# 1. 生成答案模板
python scripts/generate_survey.py --template answers.json

# 2. 填写答案后生成问卷
python scripts/generate_survey.py -o ./survey.xlsx -a answers.json
```

### 命令参数

| 参数                   | 说明                  | 默认值                   |
| -------------------- | ------------------- | --------------------- |
| `-o, --output`       | 输出文件路径              | `./sf_ec_survey.xlsx` |
| `-c, --categories`   | 指定类别（可多选）           | 全部类别                  |
| `-l, --language`     | 语言：`cn`/`en`/`both` | `both`                |
| `-a, --answers`      | 答案JSON文件路径          | -                     |
| `--no-answer-column` | 不包含答案列              | 包含                    |
| `--no-source-column` | 不包含来源列              | 包含                    |
| `--no-sub-category`  | 不包含子类别行             | 包含                    |
| `--template`         | 生成答案JSON模板          | -                     |
| `--list-categories`  | 列出所有类别              | -                     |


### 可用类别

- `基本信息` - 公司概况、现有系统
- `组织管理` - 组织架构、组织层级、组织审批
- `组织信息` - 组织基础信息、组织属性
- `岗位管理` - 岗位体系、岗位信息、岗位编制
- `人事管理` - 员工信息、入职、转正、调动、离职、合同、薪酬、考勤、权限、报表

## 输出格式

### 带答案的问卷（7列）

| 列   | 内容            |
| --- | ------------- |
| A   | 序号            |
| B   | 问题类别          |
| C   | 问题名称（中文）      |
| D   | 问题名称（英文）      |
| E   | 初步答案（来自制度文档）  |
| F   | 来源（文件名/章节）    |
| G   | 回答（空白，供确认/补充） |


### 空白问卷（5列）


| 列   | 内容       |
| --- | -------- |
| A   | 序号       |
| B   | 问题类别     |
| C   | 问题名称（中文） |
| D   | 问题名称（英文） |
| E   | 回答       |


## 目录结构

```
sf-ec-survey-generator/
├── SKILL.md                 # Claude Skill定义文件
├── README.md                # 说明文档
├── scripts/
│   └── generate_survey.py   # 问卷生成脚本
└── references/
    └── ec_questions.md      # EC调研问题库
```

## 问题库管理

### 临时调整 vs 永久修改

| 场景 | 操作方式 | 影响范围 |
|------|---------|---------|
| 对话中说"把这个问题改一下" | Claude在会话中维护临时问题列表 | 仅本次问卷 |
| 对话中说"删除这个问题" | Claude从临时列表移除 | 仅本次问卷 |
| 对话中说"添加一个新问题" | Claude添加到临时列表 | 仅本次问卷 |
| 需要永久修改问题库 | 手动编辑 `ec_questions.md` 或 `generate_survey.py` | 所有后续问卷 |

### 行为准则

1. **对话中的问题调整**：Claude 只在内存中维护临时列表，不修改文件
2. **生成问卷时**：使用用户确认后的临时问题列表
3. **问题库文件**：保持原样，作为后续对话的默认问题来源

## 依赖

- Python 3.6+
- openpyxl

## License

MIT