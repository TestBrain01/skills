---
name: testcase-skill
description: 解析产品需求文档，自动生成分层递进Markdown思维导图、XMind可导入缩进用例，全维度测试覆盖，测试开发专用
allowed-tools: []
version: 1.0
author: 测试开发工程师
---
# 全局调度规则
本Skill由多份分层Markdown文件组成，执行流程：
1. 优先读取01skill-prd-main.md
2. 加载02skill-prd-explain.md
3. 引用03skill-case-mian.md
4. 分别调用04skill-case-design、05skill-case-beauty渲染XMind文本+多层递进MD导图
5. 根据06skill-case-explore适配用户精简/自动化/专项用例指令
所有输出严格一级→二级→三级→四级叶子用例递进分层，不可跨级错乱。