# Changelog

## 1.0.0 - 通用七层世界生成器（2026-09-26）

- 取消龙族父包和九个龙族子包前置，合并为 Seven Worlds (256x256x7) 模板。
- 保留红色独占第一层、七电脑分散其他六层、22对双向界门与原守卫资源梯度。
- 不再强制主题龙群，不需要外部收尾工具；旧固定地图与开发工具不进入玩家ZIP。
- 两个无第三方模组种子通过七层通行与首回合检查；一个有原生酒馆英雄替补提示。与万世天朝最小前置组合生成及首回合通过，无ERROR。
- 玩家包使用单一根目录，附安装步骤和许可；内部ID与旧传送门类型保留。

以下为历史版本记录，不是1.0.0安装要求。

## 0.2.5 - 玩家独层与电脑分散

- 标准与龙潮模板改为红色单人独占地表；七个电脑覆盖其他六层，仅熔火层有两个电脑。电脑阵营需保持随机。
- 七层互相直达，跨层入口数为7/7/6/6/6/6/6；全图22对独立双向门，保留出生区入口、道路和深层守卫梯度。
- 收尾增加每层至少五门、玩家层无电脑、电脑最大分散的事务检查，不合格时不替换原图；收尾地图的七个电脑席位固定为AIOnly。
- 保留模板标识与旧地图传送类型，旧存档和内置旧版地图不变。

## 0.2.4 - Four distinct destination worlds per level

- Replace the six-edge chain in both random templates with a seven-world, degree-four bidirectional network (14 pairs).
- Add one separate cross-level gate pair in each of the eight player start zones: 22 cross-level pairs total, 12 surface entrances, four distinct destination worlds per level.
- Declare 32 additional independent monolith types; retain domainFinalGate for existing maps. The resulting 41 available core/mod types cover even all 38 template connections becoming portals.
- Preserve existing guarded strength tiers for deeper destinations and road connections.
- Require four distinct direct neighbours per level in the finalizer; a connected but sparse chain now fails without replacing the input map.
- Keep existing maps and saves unchanged. The bundled scenario is the old fixed single-chain map; regenerate from a template for the new network.

## 0.2.3 - Current VCMI 1.8 development compatibility

- Target official develop build 0c8650a (2026-09-08) in the single menu installation at D:\vcmi.
- Declare a mod-owned ninth two-way portal type. Fix two bundled map references that otherwise prevent actual game startup.
- Preserve all 72,283 objects, seven terrain layers and the original portal connection graph.
- Refresh bundled map dependency versions for the adapted Dragon Clans release.
- Verify actual game startup and AI turns through day 14 in an isolated profile using the retained engine.
- This is a bounded headless smoke test, not a complete match, balance or all-skills validation.

## 0.2.2 - Bundled Seven Dragon Domain scenario

- Bundle `Content/Maps/seven-dragon-domain.vmap`, displayed as 七层龙域.
- Generate a real 256x256x7 Standard map with the official VCMI 1.7.5 RMG, seed 20260909.
- Apply themed dragon placement and validate the seven-level portal graph.
- Store an explicit Chinese map title, description and required Dragon Clans lineage metadata.
- Allow either humans or AI in all eight generated starting slots for ordinary single-player use.
- Normalize the native layer descriptors above the second level to valid underground types.
- Keep raw maps, backups and synthetic fixtures outside the release package.
- Enabling the mod exposes the scenario through VCMI's ordinary map selector.

## 0.2.1 - Local VCMI 1.7.5 compatibility build

- Declare the nine required Dragon Clans lineages explicitly.
- Validate the installed 1.6.1 creature catalog rather than assuming a 1.7.0 minimum.
- Fix the dirt terrain identifier from `dr` to `dt`.
- Use parsed map objects instead of whitespace-dependent text replacement.
- Preserve creature map masks, validate seven levels and prevent backup overwrite.
- Commit map replacement atomically after validation.
- Test Standard and Dragon Tide with both Windows PowerShell 5.1 and PowerShell 7.
- Verify finalized fixture maps with the official 1.7.5 native map reader.
- Add a drag-and-drop finalizer entry point. No nine-layer expansion is included.

## 0.2.0 - 2026-09-09

- Split the seven-layer generator from Dragon Clans into a standalone VCMI mod.
- Declare `dragon-clans` as a required dependency.
- Add portable Dragon Clans discovery for the map finalizer.
- Support both Windows PowerShell 5.1 and PowerShell 7.
- Add a reproducible VCMI Launcher-compatible release builder.
- Keep Standard (44 curated dragon groups) and Dragon Tide (88 curated dragon groups) profiles.
