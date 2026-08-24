# DeliveryAdvisor · DeliveryWeb

> 26-交付-Delivery 行业 Web 项目 · Phase 0 骨架
> 路径:`Consultant/26-交付-Delivery/_DeliveryLib/DeliveryWeb/`

## 这是什么

`DeliveryWeb` 是"交付(Delivery / 物流 / 快递 / 配送 / 交通基础设施)"行业的可视化站点,内容来自同级的 `_DeliveryLib/`(10 个章节目录:交付起源 / 分支 / 逻辑 / 故事 / 趣味 / 大师 / 思想 / 应用 / 之美 / 趣闻)。

**当前阶段:Phase 0 — 基础骨架**
**下一阶段:Phase 1 — 内容章节填充(10 个章节,与 `_DeliveryLib/` 子目录一一对应)**

## 目录约定

```
DeliveryWeb/
├── README.md            本文件
├── index.html           站点首页(Phase 0 占位)
├── assets/
│   ├── css/site.css     全站基础样式
│   └── js/site.js       全站脚本入口(Phase 0 空,Phase 1+ 填充)
├── content/             Phase 1 起,放按章节组织的 markdown
│                          (01_交付起源与演变 / 02_... / 10_...)
├── .plan/               每日增量计划(T4 产物,YYYYMMDD.md)
├── .Log/                每日巡检报告(T5 产物,巡检-交付-YYYYMMDD.md)
└── 项目开发计划.md       T1 主计划(待 T1 落地,Phase 0/1 任务清单)
```

## 巡检制度

每个工作日 02:10 由 26-交付-Delivery 顾问自动巡检本仓库,生成 `巡检-交付-YYYYMMDD.md` 落到 `.Log/` 目录。巡检覆盖:

| 维度 | 检查内容 |
|------|---------|
| 阶段 | 当前 Phase(0 骨架 / 1 内容填充 / 2 增强)是否与实际产物一致 |
| 文件 | 文件数 / 代码量 / git status 是否符合阶段预期 |
| 计划 | `.plan/YYYYMMDD.md` 是否落盘(T4 任务是否已写当日计划) |
| 缺口 | 与下一阶段门控的差距(如 Phase 0 → Phase 1 的 T1 主计划 / content/ 章节) |
| 上游 | 同级 `_DeliveryLib/` 10 章节素材是否齐备 |

巡检报告是**只读观察**,不做改动;改动走 T1-T5 任务链路。巡检若发现关键缺口(如 T1 主计划未起草),会在结论中**显式标记"本顾问不应主动代为起草"**,留给张勇决策。

## 本地启动

```bash
cd _DeliveryLib/DeliveryWeb
python3 -m http.server 8000
# 浏览器打开 http://localhost:8000/
```

不需要 npm / 构建工具,纯静态站点。

## 与 DeliveryLib 的关系

`_DeliveryLib/` 是素材库(10 个分类子目录,原始 markdown / 图片 / 资料),
`DeliveryWeb/` 是它的可视化外壳。Phase 1 起,Web 站点按 10 章节结构消费 `_DeliveryLib/` 内容。

## 变更记录

- 2026-08-25 · README 补"巡检制度"章节,正式入档 02:10 巡检 / `.Log/` 机制 · T4 增量
- 2026-08-25 · 新建 `.Log/巡检-交付-20260825.md`(首份巡检报告)· T5 自动
- 2026-08-24 · Phase 0 骨架 · 改写 README,新增 index.html / assets 目录 · T4 增量
- 2026-08-23 · 初始 commit(`dd307ac`)· 仅含 README 占位
