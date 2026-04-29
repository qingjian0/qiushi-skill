# qiushi-skill for Trae Solo - Product Requirement Document

## Overview
- **Summary**: 优化 qiushi-skill 以支持 Trae Solo 平台，使其可以轻松安装和使用
- **Purpose**: 让 Trae Solo 用户可以方便地获取 qiushi-skill 提供的方法论框架
- **Target Users**: Trae Solo 用户，特别是需要结构化思考和问题解决方法论的开发者

## Goals
1. 为 Trae Solo 创建安装入口文档
2. 更新 CLI 工具以支持 Trae Solo 平台
3. 确保 qiushi-skill 的所有功能在 Trae Solo 中正常工作
4. 提供清晰的安装和使用指引

## Non-Goals (Out of Scope)
1. 重写 qiushi-skill 的核心逻辑
2. 添加新的方法论 skills 或功能
3. 修改其他平台的支持代码

## Background & Context
当前 qiushi-skill 已支持以下平台：
- Claude Code
- Cursor
- OpenClaw
- Hermes Agent
- Codex
- OpenCode
- nanobot

qiushi-skill 是一个为 AI agent 提供方法论框架的项目，基于毛泽东思想和唯物辩证法，提供以下核心功能：
- 实事求是原则
- 矛盾分析法
- 实践认识论
- 调查研究方法
- 群众路线
- 批评与自我批评
- 持久战略
- 集中兵力
- 星火燎原
- 统筹兼顾
- 工作流组合

项目使用 SKILL.md 作为技能入口，commands/ 作为手动命令入口，hooks/ 用于会话启动注入。

## Functional Requirements
- **FR-1**: 提供 Trae Solo 的安装入口文档
- **FR-2**: 更新 CLI 工具以支持 Trae Solo 作为安装目标
- **FR-3**: 更新平台支持文档以包含 Trae Solo
- **FR-4**: 确保现有 skills 在 Trae Solo 中正常加载和使用

## Non-Functional Requirements
- **NFR-1**: 保持与现有其他平台支持一致的代码风格
- **NFR-2**: 安装流程简单明了，与 qiushi-skill 整体体验一致
- **NFR-3**: 所有修改向后兼容，不破坏现有功能

## Constraints
- **Technical**: 需要与 qiushi-skill 现有的架构保持一致，使用现有的 skills、commands、hooks 目录结构
- **Business**: 遵循项目现有许可证（MIT），保持项目开源性质
- **Dependencies**: 依赖项目现有 Node.js 工具链（>=18.17）

## Assumptions
1. Trae Solo 支持类似其他平台的技能加载机制（通过 .trae/skills/ 目录）
2. Trae Solo 支持 Markdown 技能文件和 slash commands
3. Trae Solo 有标准的插件/技能安装位置

## Acceptance Criteria

### AC-1: Trae Solo 安装入口文档存在且完整
- **Given**: 用户希望在 Trae Solo 中安装 qiushi-skill
- **When**: 用户查看项目文档
- **Then**: 应该存在清晰的安装指引（.trae-solo/INSTALL.md），包含完整的安装步骤和验证方法
- **Verification**: human-judgment

### AC-2: CLI 工具支持 Trae Solo 目标
- **Given**: 用户使用 npx qiushi-skill 工具
- **When**: 用户运行 npx qiushi-skill --help 或 npx qiushi-skill install --target trae-solo
- **Then**: 应该显示 Trae Solo 作为有效目标，并提供相应的安装指引
- **Verification**: programmatic

### AC-3: 平台支持文档已更新
- **Given**: 用户查看项目的平台支持文档
- **When**: 用户查看 docs/platforms.md
- **Then**: 应该包含 Trae Solo 的条目，说明其安装和使用方式
- **Verification**: human-judgment

### AC-4: qiushi-skill 在 Trae Solo 中可以正常使用
- **Given**: qiushi-skill 已成功安装在 Trae Solo 中
- **When**: 用户启动新会话并使用 qiushi-skill
- **Then**: 应该可以正常加载 arming-thought skill 并按需调用其他方法论 skills
- **Verification**: human-judgment

## Open Questions
- [ ] Trae Solo 的确切技能安装路径是什么？
- [ ] Trae Solo 是否支持会话启动钩子（SessionStart hooks）？
- [ ] Trae Solo 是否有 marketplace 或插件目录支持？

---

*文档创建时间：2026-04-29*
