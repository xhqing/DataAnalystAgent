# Changelog

## [1.0.0] - 2026-10-03

### 变更（README 标配补全：中英双语拆分重构 + 版权署名段）

- **为什么改**：commit skill 第 9 步标配检测（2026-10-03，工作目录卫生检查触发的 `/add` → `/commit` 流程）发现本仓 README 不符合「英文版 `README.md` + 中文版 `README_cn.md` 互链」标准：`README.md` 为中英对照混排、缺 `README_cn.md`、底部缺「版权与署名」段。
- **改了什么**：① `README.md` 重构为英文版（原中英对照中的中文内容移入新建 `README_cn.md`），两版互链（`[简体中文](README_cn.md)` / `[English](README.md)`）；② 两版顶部 LOGO / 徽章块保持一致；③ 两版底部新增英文版 `## License & Attribution`、中文版 `## 版权与署名` 段（All Contributors 署名 + 许可证 + 项目地址引用）。

### 变更（README 徽章组合合规：移除 Stars / Last Commit 动态徽章 + 补 Version 徽章）

- **为什么改**：commit skill 第 9l 步检测（2026-10-03）发现两版 README 徽章行含 `Stars` / `Last Commit` 两枚 GitHub 动态徽章（规范禁用），且标准三枚（License / Version / Type）中缺 Version 徽章。
- **改了什么**：README（EN/CN）徽章区删除 `Stars`、`Last Commit` 动态徽章行，新增 `Version-1.0.0` 静态徽章（版本号取自本次新建的 `VERSION`）；Visitors 访问量徽章（指向 xhqing traffic/badges/ 的 endpoint 形态）属团队允许例外，保留不动。

### 新增（VERSION 1.0.0 与 .commit-cache.md：commit skill 第 9m 步标配补齐）

- **为什么改**：本仓缺 `VERSION` 文件（commit skill 第 9m 步要求任何项目都必须有 `CHANGELOG.md` 与 `VERSION`）；`.commit-cache.md` 为 commit skill 标配检测缓存文件，首次运行标配检测后建立。
- **改了什么**：① 新建 `VERSION`（1.0.0——取值顺序：无 `package.json` / 主 manifest，`CHANGELOG.md` 顶部无实际版本标题，取默认首版 1.0.0）；② 新建 `.commit-cache.md`，登记本次已完成的标准检测标记（readme-standard / license / github-about / agent-persona / attribution-name / readme-link-text / repo-sponsors / readme-badges / changelog-version）。

### 变更（CLAUDE.md 删去「由 Claude Code 自动加载」说明句）

- **为什么改**：用户 2026-09-12 要求 CLAUDE.md 不再强调本文由 Claude Code 加载，团队全部项目的 CLAUDE.md 统一清理此类语句。
- **改了什么**（2026-09-12）：`CLAUDE.md` 开头角色定位行删去句尾「本文件由 Claude Code 在每次会话开头自动加载。」，角色描述本身保留。

### 变更（assets/logo.svg 副标题去中文）

- **为什么改**：全局规则新增「Logo / 图标资产文字一律用英文」（2026-09-12 用户立，起因 Swing 仓库 logo 副标题混入中文被指出）：logo 是面向全球读者的视觉标识，中文受众已有 README_cn.md 双语通道；且 SVG 中文依赖查看环境的字体回退，渲染不可控。本次为按新规批量清理存量。
- **改了什么**：`assets/logo.svg` 副标题「Analyst · 数据分析师」→「Data Analyst」（顺带补全职称，与注册表「数据分析师」对齐）。

### 变更（措辞统一 fleet → team：根 CLAUDE.md 跟随全局统一）

- **为什么改**：用户 2026-08-16 已把 xhqing 主页 README 的自称从「舰队 / fleet」改为「团队 / team」，本仓根 `CLAUDE.md`（Echo 身份定义句）仍是 fleet 旧措辞；2026-08-21 用户裁定全量存量一次清零、统一为团队 / team。
- **改了什么**：根 `CLAUDE.md`「你让整个 fleet 越跑越聪明」→「整个团队」。仅改措辞，身份职责、产物契约均不变。

### 变更（Visitors 徽章更名 Visits/day (14d)：alt 文本与 xhqing 集中统计新 label 对齐）

- **为什么改**：用户要求（2026-08-17）访问量徽章名需表达「最近半月日均访问量」口径——xhqing 集中统计侧的 badge JSON label 已从 `Visitors` 改为 `Visits/day (14d)`（`Visits/day` 是 shields.io 表达日均的惯例写法、`(14d)` 标注 14 天滚动窗口），各仓 README 的徽章 alt 文本同步对齐，避免 alt 与徽章实际显示文字脱节。
- **改了什么**：README 徽章区 `alt="Visitors"` → `alt="Visits/day (14d)"`，仅改 alt 文本，endpoint URL、数据源、徽章口径均不变（口径改动记 xhqing 仓库 CHANGELOG，本仓只改 alt）。

### 变更（Visitors 徽章 alt 文本首字母大写：README 访问量徽章命名统一）

- **为什么改**：用户指令（2026-08-16）「Visitors 徽章全局统一，首字母大写」——配合全局 `~/.claude/CLAUDE.md`「徽章英文首字母必须大写」新规，集中统计上线时挂的访问量徽章 `alt="visitors"` 为小写存量，与 badge JSON label（`Visits/day`）及大写规范不一致，本次一次收口。
- **改了什么**：README（EN/CN）徽章区 visitors 徽章 `alt="visitors"` → `alt="Visitors"`，仅改 alt 显示文本，endpoint URL 与数据源不变。

### 新增（README 访问量徽章——舰队集中式访问统计）

- **为什么改**：全舰队上线集中式「真去重」访问统计（图片徽章方案无法去重，走官方 Traffic API 路线）：统计集中部署在 xhqing 仓库（`scripts/update_traffic.py` + 每日 GitHub Action），各 fleet 仓库只需在 README 挂徽章、零运行负担。
- **改了什么**：README（EN/CN）徽章区新增 visitors 徽章（shields.io endpoint 指向 `xhqing/xhqing` 仓库 `traffic/badges/<repo>.json`，由每日采集的官方 Traffic API 数据更新）。徽章数字含义：按日去重访客的累计（GitHub 只提供每日 uniques，跨天不去重），自 2026-08-16 起累计。
