# SF EC Survey Generator

SAP SuccessFactors Employee Central (EC) 项目调研问卷生成器

## 功能特性

- 生成标准化的SF EC调研问卷Excel文件
- 支持从客户制度文档中提取答案预填充问卷
- 支持中英文双语输出
- 覆盖EC核心模块：组织管理、岗位管理、人事管理等
- 100+道专业调研问题

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
| `--template`         | 生成答案JSON模板          | -                     |


### 可用类别

- `基本信息` - 公司概况、现有系统
- `组织管理` - 组织架构、组织层级、组织审批
- `组织信息` - 组织基础信息、组织属性
- `岗位管理` - 岗位体系、岗位信息、岗位编制
- `人事管理` - 员工信息、入职、转正、调动、离职、合同、薪酬、考勤、权限、报表

## 输出格式

### 带答案的问卷（6列）


| 列   | 内容            |
| --- | ------------- |
| A   | 序号            |
| B   | 问题类别          |
| C   | 问题名称（中文）      |
| D   | 问题名称（英文）      |
| E   | 初步答案（来自制度文档）  |
| F   | 回答（空白，供确认/补充） |


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

## 依赖

- Python 3.6+
- openpyxl

## License

MIT