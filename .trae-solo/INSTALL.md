# qiushi-skill for Trae Solo

按下面步骤接入：

1. 确认仓库已克隆到本地。
2. 将项目复制到你的 Trae 项目的 .trae/skills/ 目录下：
   ```bash
   mkdir -p .trae/skills/qiushi-skill
   cp -R skills/* .trae/skills/qiushi-skill/
   ```
3. 新会话开始时，Trae 会自动发现并加载 skills。优先加载 `skills/arming-thought/SKILL.md`，建立实事求是原则，并在需要时调用其他方法论 skills。
4. 针对具体任务，可按需读取下列文件：
   - `skills/contradiction-analysis/SKILL.md`
   - `skills/practice-cognition/SKILL.md`
   - `skills/investigation-first/SKILL.md`
   - `skills/mass-line/SKILL.md`
   - `skills/criticism-self-criticism/SKILL.md`
   - `skills/protracted-strategy/SKILL.md`
   - `skills/concentrate-forces/SKILL.md`
   - `skills/spark-prairie-fire/SKILL.md`
   - `skills/overall-planning/SKILL.md`
   - `skills/workflows/SKILL.md`
5. 如果 Trae Solo 支持 Markdown slash commands，可额外加载 commands/ 目录作为手动命令入口；不支持时，直接读取同名命令文件内容即可。
6. 优先运行：
   ```bash
   npx qiushi-skill validate
   ```

完成后，手动验证两点：
- 会话起始时能够成功读取 `arming-thought`
- 针对一个具体问题时，能够按需切换到对应 skill，而不是机械全调用
