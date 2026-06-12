# 知识增量报告 (Knowledge Delta)

从运行时日志中提炼的结构化知识增量。每条 Delta 经过 L6 Learning 分析后，状态变为 `pending` → `verified` → `applied`。

---

## Delta 记录格式

| 字段 | 说明 |
| :--- | :--- |
| `id` | 唯一标识，格式 KD-YYYY-NNN |
| `source` | 来源（runtime-log / 用户反馈 / 外部搜索） |
| `category` | 分类：pricing / regulation / tactic / process / industry |
| `industry` | 适用行业 |
| `content` | 具体知识内容 |
| `target_file` | 应写入的 references 文件路径 |
| `status` | pending / verified / applied / rejected |
| `verified_at` | 验证时间 |
| `applied_at` | 应用时间 |

---

## Delta 记录

<!-- 种子示例 -->

| id | source | category | industry | content | target_file | status | verified_at | applied_at |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| KD-2026-001 | seed | regulation | 通用 | 2026年《个人信息保护法》新规：企业收集个人信息需单独同意，不得捆绑授权 | references/industry-knowledge.md | pending | — | — |
| KD-2026-002 | seed | pricing | 餐饮 | 2026年一线城市火锅店装修均价上涨至1200-2000元/㎡（原800-1500） | references/industries/catering.md | pending | — | — |
| KD-2026-003 | seed | tactic | 直播 | 新套路：DP公司用"虚拟人直播"替代真人但按真人收费，需在合同中明确"真人出镜时长占比≥80%" | references/industries/livestream.md | pending | — | — |
