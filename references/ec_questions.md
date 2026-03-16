# EC 调研问卷问题库

本文档包含 SAP SuccessFactors Employee Central (EC) 蓝图设计阶段调研问卷的完整问题库，按功能模块分类，支持中英文双语。

## 问题类别结构

```
├── 基本信息 (Basic Information)
├── 组织管理 (Organization Management)
├── 组织信息 (Organization Information)
├── 岗位管理 (Position Management)
└── 人事管理 (Personnel Management)
```

---

## 1. 基本信息 (Basic Information)

### 1.1 公司概况


| 序号    | 问题(中文)              | 问题(英文)                                                                   |
| ----- | ------------------- | ------------------------------------------------------------------------ |
| 1.1.1 | 请简要介绍公司的业务范围和主营业务？  | Please briefly introduce the company's business scope and main business? |
| 1.1.2 | 公司目前的员工总数是多少？       | What is the total number of employees in the company?                    |
| 1.1.3 | 公司的组织架构层级有多少级？      | How many levels does the company's organizational structure have?        |
| 1.1.4 | 公司是否有多个法人实体？如有，请列出。 | Does the company have multiple legal entities? If yes, please list them. |
| 1.1.5 | 公司是否有海外分支机构或员工？     | Does the company have overseas branches or employees?                    |


### 1.2 现有系统


| 序号    | 问题(中文)           | 问题(英文)                                                  |
| ----- | ---------------- | ------------------------------------------------------- |
| 1.2.1 | 目前使用的人事管理系统是什么？  | What is the current HR management system?               |
| 1.2.2 | 现有系统的主要痛点有哪些？    | What are the main pain points of the current system?    |
| 1.2.3 | 是否有其他需要与SF集成的系统？ | Are there other systems that need to integrate with SF? |
| 1.2.4 | 现有人事数据的准确性如何？    | How accurate is the current HR data?                    |
| 1.2.5 | 数据迁移的范围和截止时间要求？  | What is the scope and deadline for data migration?      |


---

## 2. 组织管理 (Organization Management)

### 2.1 组织架构


| 序号    | 问题(中文)                       | 问题(英文)                                                                                       |
| ----- | ---------------------------- | -------------------------------------------------------------------------------------------- |
| 2.1.1 | 公司的组织架构类型是什么？（事业部制/职能制/矩阵制等） | What is the company's organizational structure type? (Business unit/Functional/Matrix, etc.) |
| 2.1.2 | 组织架构的调整频率如何？                 | How often is the organizational structure adjusted?                                          |
| 2.1.3 | 是否需要支持矩阵式汇报关系？               | Do you need to support matrix reporting relationships?                                       |
| 2.1.4 | 组织单元是否有有效期管理需求？              | Do organizational units require effective date management?                                   |
| 2.1.5 | 组织单元的自定义字段需求有哪些？             | What are the custom field requirements for organizational units?                             |


### 2.2 组织层级


| 序号    | 问题(中文)                       | 问题(英文)                                                                    |
| ----- | ---------------------------- | ------------------------------------------------------------------------- |
| 2.2.1 | 公司的组织层级如何定义？（如：公司-事业部-部门-小组） | How are organizational levels defined? (e.g., Company-BU-Department-Team) |
| 2.2.2 | 每个层级的命名规则是什么？                | What are the naming conventions for each level?                           |
| 2.2.3 | 组织单元的编码规则是什么？                | What are the coding rules for organizational units?                       |
| 2.2.4 | 是否有虚拟组织的需求？                  | Is there a need for virtual organizations?                                |


### 2.3 组织审批


| 序号    | 问题(中文)           | 问题(英文)                                                               |
| ----- | ---------------- | -------------------------------------------------------------------- |
| 2.3.1 | 组织架构变更的审批流程是怎样的？ | What is the approval process for organizational changes?             |
| 2.3.2 | 新增组织单元需要哪些必填信息？  | What are the required fields for creating a new organizational unit? |
| 2.3.3 | 组织合并/拆分的业务场景有哪些？ | What are the business scenarios for organization merge/split?        |


---

## 3. 组织信息 (Organization Information)

### 3.1 组织基础信息


| 序号    | 问题(中文)          | 问题(英文)                                                                  |
| ----- | --------------- | ----------------------------------------------------------------------- |
| 3.1.1 | 组织单元需要维护哪些基础信息？ | What basic information needs to be maintained for organizational units? |
| 3.1.2 | 组织的地点/办公地址如何管理？ | How are organization locations/office addresses managed?                |
| 3.1.3 | 组织负责人如何定义和关联？   | How are organization heads defined and linked?                          |
| 3.1.4 | 组织成本中心如何关联？     | How are organization cost centers linked?                               |


### 3.2 组织属性


| 序号    | 问题(中文)                            | 问题(英文)                                                                 |
| ----- | --------------------------------- | ---------------------------------------------------------------------- |
| 3.2.1 | 是否需要区分不同类型的组织单元？（如：职能部门、业务部门、项目组） | Do you need to distinguish different types of organizational units?    |
| 3.2.2 | 组织的状态如何管理？（如：正常、冻结、关闭）            | How is organization status managed? (e.g., Active, Frozen, Closed)     |
| 3.2.3 | 组织的预算信息是否需要在系统中管理？                | Does organization budget information need to be managed in the system? |
| 3.2.4 | 是否有组织层级权限控制的需求？                   | Is there a need for organization-level permission control?             |


---

## 4. 岗位管理 (Position Management)

### 4.1 岗位体系


| 序号    | 问题(中文)                 | 问题(英文)                                                                   |
| ----- | ---------------------- | ------------------------------------------------------------------------ |
| 4.1.1 | 公司目前的岗位管理体系是怎样的？       | What is the company's current position management system?                |
| 4.1.2 | 岗位和职位(Job)的区别和管理方式是什么？ | What is the difference and management approach between Position and Job? |
| 4.1.3 | 岗位序列/职级体系是怎样的？         | What is the job family/grade structure?                                  |
| 4.1.4 | 是否需要岗位编制管理？            | Is position headcount management required?                               |
| 4.1.5 | 岗位编码规则是什么？             | What are the position coding rules?                                      |


### 4.2 岗位信息


| 序号    | 问题(中文)                   | 问题(英文)                                                                                                               |
| ----- | ------------------------ | -------------------------------------------------------------------------------------------------------------------- |
| 4.2.1 | 岗位需要维护哪些属性信息？            | What attribute information needs to be maintained for positions?                                                     |
| 4.2.2 | 岗位与组织的关系是怎样的？一人一岗还是可以兼岗？ | What is the relationship between position and organization? One person one position or concurrent positions allowed? |
| 4.2.3 | 岗位的汇报关系如何定义？             | How is position reporting relationship defined?                                                                      |
| 4.2.4 | 岗位是否有有效期管理？              | Is there effective date management for positions?                                                                    |
| 4.2.5 | 岗位的自定义字段需求有哪些？           | What are the custom field requirements for positions?                                                                |


### 4.3 岗位编制


| 序号    | 问题(中文)           | 问题(英文)                                                            |
| ----- | ---------------- | ----------------------------------------------------------------- |
| 4.3.1 | 是否需要管理岗位编制数？     | Is it necessary to manage position headcount?                     |
| 4.3.2 | 编制超编时是否需要控制或预警？  | Is control or warning needed when headcount exceeds the limit?    |
| 4.3.3 | 编制的审批流程是怎样的？     | What is the approval process for headcount changes?               |
| 4.3.4 | 编制数据是否需要与招聘模块联动？ | Does headcount data need to integrate with the Recruiting module? |


---

## 5. 人事管理 (Personnel Management)

### 5.1 员工基础信息


| 序号    | 问题(中文)                 | 问题(英文)                                                                 |
| ----- | ---------------------- | ---------------------------------------------------------------------- |
| 5.1.1 | 员工信息需要维护哪些基础字段？        | What basic fields need to be maintained for employee information?      |
| 5.1.2 | 是否有自定义的员工信息字段需求？       | Are there custom employee information field requirements?              |
| 5.1.3 | 员工信息的敏感字段有哪些？如何控制访问权限？ | What are the sensitive employee fields? How is access control managed? |
| 5.1.4 | 员工照片的管理要求是什么？          | What are the requirements for employee photo management?               |
| 5.1.5 | 是否需要管理员工的紧急联系人信息？      | Is it necessary to manage employee emergency contact information?      |


### 5.2 入职管理


| 序号    | 问题(中文)          | 问题(英文)                                                    |
| ----- | --------------- | --------------------------------------------------------- |
| 5.2.1 | 新员工入职的业务流程是怎样的？ | What is the business process for new employee onboarding? |
| 5.2.2 | 入职前是否需要预入职流程？   | Is a pre-onboarding process required?                     |
| 5.2.3 | 入职时需要采集哪些信息？    | What information needs to be collected during onboarding? |
| 5.2.4 | 入职审批流程是怎样的？     | What is the onboarding approval workflow?                 |
| 5.2.5 | 是否需要与招聘模块集成？    | Is integration with the Recruiting module required?       |


### 5.3 转正管理


| 序号    | 问题(中文)            | 问题(英文)                                                        |
| ----- | ----------------- | ------------------------------------------------------------- |
| 5.3.1 | 试用期转正的业务规则是什么？    | What are the business rules for probation confirmation?       |
| 5.3.2 | 转正评估流程是怎样的？       | What is the probation evaluation process?                     |
| 5.3.3 | 转正审批流程是怎样的？       | What is the probation confirmation approval workflow?         |
| 5.3.4 | 是否有试用期延长的情况？如何处理？ | Are there cases of probation extension? How are they handled? |


### 5.4 调动管理


| 序号    | 问题(中文)                         | 问题(英文)                                                                                                           |
| ----- | ------------------------------ | ---------------------------------------------------------------------------------------------------------------- |
| 5.4.1 | 员工调动的类型有哪些？（内部调动、跨公司调动、晋升、降职等） | What are the types of employee transfers? (Internal transfer, Cross-company transfer, Promotion, Demotion, etc.) |
| 5.4.2 | 调动审批流程是怎样的？                    | What is the transfer approval workflow?                                                                          |
| 5.4.3 | 调动生效日期如何确定？                    | How is the transfer effective date determined?                                                                   |
| 5.4.4 | 调动是否需要同步更新薪酬信息？                | Does transfer need to synchronously update compensation information?                                             |
| 5.4.5 | 跨公司调动涉及的工龄计算规则是什么？             | What are the seniority calculation rules for cross-company transfers?                                            |


### 5.5 离职管理


| 序号    | 问题(中文)                  | 问题(英文)                                                                                                |
| ----- | ----------------------- | ----------------------------------------------------------------------------------------------------- |
| 5.5.1 | 离职类型有哪些？（主动离职、被动离职、退休等） | What are the types of termination? (Voluntary resignation, Involuntary termination, Retirement, etc.) |
| 5.5.2 | 离职申请和审批流程是怎样的？          | What is the resignation application and approval workflow?                                            |
| 5.5.3 | 离职交接流程是怎样的？             | What is the handover process for resignation?                                                         |
| 5.5.4 | 离职后员工数据的处理规则是什么？        | What are the data handling rules after employee termination?                                          |
| 5.5.5 | 是否有离职面谈的需求？             | Is there a requirement for exit interviews?                                                           |


### 5.6 合同管理


| 序号    | 问题(中文)            | 问题(英文)                                                         |
| ----- | ----------------- | -------------------------------------------------------------- |
| 5.6.1 | 劳动合同类型有哪些？        | What are the types of employment contracts?                    |
| 5.6.2 | 合同签订和续签的业务流程是怎样的？ | What is the business process for contract signing and renewal? |
| 5.6.3 | 合同到期提醒规则是什么？      | What are the contract expiration reminder rules?               |
| 5.6.4 | 是否需要管理电子合同？       | Is electronic contract management required?                    |
| 5.6.5 | 合同变更流程是怎样的？       | What is the contract change process?                           |


### 5.7 薪酬基础


| 序号    | 问题(中文)             | 问题(英文)                                                                |
| ----- | ------------------ | --------------------------------------------------------------------- |
| 5.7.1 | 薪酬结构是怎样的？包含哪些薪酬项目？ | What is the compensation structure? What pay components are included? |
| 5.7.2 | 薪酬数据是否需要在EC中管理？    | Does compensation data need to be managed in EC?                      |
| 5.7.3 | 薪资调整流程是怎样的？        | What is the salary adjustment process?                                |
| 5.7.4 | 是否有多个薪资组的区分？       | Are there multiple pay groups?                                        |
| 5.7.5 | 薪酬数据的保密级别如何？       | What is the confidentiality level of compensation data?               |


### 5.8 工作时间与考勤


| 序号    | 问题(中文)                       | 问题(英文)                                                                       |
| ----- | ---------------------------- | ---------------------------------------------------------------------------- |
| 5.8.1 | 公司的工时制度是什么？（标准工时/综合工时/不定时工时） | What is the company's working hour system? (Standard/Comprehensive/Flexible) |
| 5.8.2 | 是否需要在EC中管理工作时间信息？            | Is it necessary to manage working time information in EC?                    |
| 5.8.3 | 是否需要与考勤系统集成？                 | Is integration with the time attendance system required?                     |
| 5.8.4 | 加班规则和管理要求是什么？                | What are the overtime rules and management requirements?                     |


### 5.9 数据权限


| 序号    | 问题(中文)               | 问题(英文)                                                             |
| ----- | -------------------- | ------------------------------------------------------------------ |
| 5.9.1 | HR数据的访问权限规则是什么？      | What are the access permission rules for HR data?                  |
| 5.9.2 | 是否有按组织/字段/角色的权限控制需求？ | Is there a need for permission control by organization/field/role? |
| 5.9.3 | 敏感数据的脱敏规则是什么？        | What are the data masking rules for sensitive data?                |
| 5.9.4 | 数据审批流程的权限如何控制？       | How are permissions controlled for data approval workflows?        |


### 5.10 报表与分析


| 序号     | 问题(中文)          | 问题(英文)                                                        |
| ------ | --------------- | ------------------------------------------------------------- |
| 5.10.1 | 常用的HR报表有哪些？     | What are the commonly used HR reports?                        |
| 5.10.2 | 是否有自定义报表的需求？    | Is there a need for custom reports?                           |
| 5.10.3 | 报表数据的更新频率要求是什么？ | What are the data refresh frequency requirements for reports? |
| 5.10.4 | 是否需要移动端查看报表？    | Is mobile access for reports required?                        |


---

## 使用说明

### 问题选择策略

根据客户情况选择合适的问题：

1. **全量调研**：使用所有问题，适用于完整的蓝图设计阶段
2. **重点调研**：根据客户关注的模块，选择相应分类的问题
3. **补充调研**：基于已有信息，选择缺失部分的问题

### 问题优先级

- **必须询问**（P1）：标记为序号末尾带 `*` 的问题
- **建议询问**（P2）：标记为序号末尾带 `**` 的问题
- **可选询问**（P3）：其他问题

### 自定义问题

根据客户行业特点，可能需要补充以下问题：

- 行业特定的合规要求
- 地区特定的法律法规要求
- 客户特有的业务场景

---

## 附录：行业特定问题

### 制造业

- 倒班管理需求
- 生产车间组织架构
- 一线员工管理特点

### 零售业

- 门店组织架构
- 兼职/临时工管理
- 门店调动频繁度

### 金融业

- 合规审批要求
- 多法人实体管理
- 敏感岗位管理

### 互联网

- 项目制组织
- 灵活的职级体系
- 快速的组织调整

&nbsp;