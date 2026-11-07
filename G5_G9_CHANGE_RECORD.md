# G5/G9 产品修改记录

- 产品编号：$(@{number=56; product_id=JLZ-EDU-AG-011; chinese_name=教务运营助手; english_name=Academic Operations Agent; repository_name=edu-academic-operations-agent; repository_url=https://github.com/jinlize-tech/edu-academic-operations-agent; product_type=Agent; category_code=04; category=04 教务运营中心; description=教务综合运营和异常处理。; target_users=System.Object[]; core_input=校区目标、教务数据、班级状态、人员、异常和当前阶段; main_output=教务诊断、优先级、30天行动方案、会议议程、指标和升级项; product_risk=数据不完整时给出过度自动化建议; dedup_label=需要明确差异化; dedup_note=与MT-CRM区分：围绕教务运营，不运营销售客户；与单项教务Skill区别为多步骤综合协调。; development_status=Planned / 待研发; license=Apache-2.0; spec_version=1.0.0; workbuddy_status=PLANNED_FOR_WORKBUDDY}.product_id)
- 产品名称：教务运营助手
- 基线：EDUCATION_BASELINE_V1.0.0
- 基线提交：$BaselineCommit
- 原版本：1.0.0
- 新版本：1.0.1

## 本次修改

1. 强化产品专属执行流程、输入核对和输出验收规则。
2. 新增 scripts/validate_input.js，实际检查必填字段、冲突、未确认数据和敏感信息。
3. 新增正常、缺失、冲突、敏感信息和非法JSON场景输入。
4. 测试升级为 T1–T7 分层并保存逐项检查结果。
5. 安装包加入 Apache-2.0 LICENSE 和 THIRD_PARTY_NOTICES.md。
6. 安装包升级为 1.0.1，加入许可证、第三方声明和输入校验脚本，保留 1.0.0 ZIP。
7. 按本产品冻结规格补充专属处理规则、输入到成果的核对矩阵和去重边界。

## 产品专属增强

- 核心任务：教务综合运营和异常处理。
- 主要风险：数据不完整时给出过度自动化建议
- 去重边界：与MT-CRM区分：围绕教务运营，不运营销售客户；与单项教务Skill区别为多步骤综合协调。

- 先提取班级、教师、教室、时间、学生约束和硬性规则，再生成排程草案。
- 硬冲突不得被软约束覆盖；无法消解时列出冲突、影响和升级责任人。
- 所有变更保留原状态、目标状态、生效时间和回退方式。
- 正式课表、考勤和审批结果必须由有权限人员确认后生效。

## 运行边界

- 本地模型行为：NOT_RUNTIME_VERIFIED
- WorkBuddy平台验证：WORKBUDDY_VALIDATION_NOT_IN_SCOPE
- 本轮不执行上传、安装、审核或正式发布。
