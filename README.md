# GTA6 → Minecraft 体素化 · 项目笔记

从 RAGE 引擎资源（.ymap / .ydr / .ytd / .ybn / .ysc）解析出实体与贴图，分区块 1m 体素化成 Minecraft 结构的完整技术路线与规模测算。

存档：见 [ARCHIVE-2026-11-22.md](ARCHIVE-2026-11-22.md)

## 路线速览
1. `.ymap` 读实体表（position / rotation）→ 按 ±1500m 矩形裁剪
2. `.ydr` 取材质名 → 同名 `.ytd` 取 DDS → PNG
3. 1m 体素化，贴图平均色映射方块调色板
4. 分区块输出 `.litematic` / `.mca`（3km×3km ≈ 3.5 万区块，生成 5~15 小时）

## 立场
不提供游戏本体资源、种子或整包解包服务。仅处理自行合法取得的模型与贴图。
