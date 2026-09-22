# Endfield Baker (终末地 · BAKER)

[English](README.md) | 中文

Endfield Baker（终末地 · BAKER）—— dsh web GUI 的明日方舟：终末地工业终端皮肤，
以纯资产目录形态收录在皮肤中心内。会话区按 BAKER 通讯界面重做，其余壳层沿用
终末地的工业语汇：细网格、斜纹信号条、等宽微标签与单像素浅灰描边。

## 是什么

- **纯资产**：`skin.json`（v2 清单）+ `skin.css`（L1 token 重映射，`--ef-*`
  原语）+ `patches.css`（L3 结构补丁，分节 0-12）+ `assets/`（标头图、卡片
  纹理、背景图）+ `preview/`（亮/暗截图）。无 package.json、无构建步骤、无
  hooks。
- **浅深共用一套调色板**：浅色与深色主题共用同一份夜航终端配色；`:root` 钉死
  `color-scheme: dark`，且不存在 `body[data-ds-dark-theme]` 覆盖，因此两张
  预览截图构造上呈现同一套配色。
- **逐点取样自原图**：页面底色、行填充、聊天页、输入条胶囊与两种信号色均从
  BAKER 参考图逐像素取样。
- **重做的会话区**：青色标头竖条、信号黄选中行、切角控制台卡片、白色胶囊输入
  条与磨砂灰聊天底板，顶栏下方以三色条与黑色实体收边。

## 配色

| 角色 | 颜色 | 画什么 |
| --- | --- | --- |
| 信号青 | `#19CFFD` | 品牌强调、主按钮、发送键、标头竖条 |
| 信号黄 | `#FFEF00` | 选中行、斜纹信号条 |
| 页面墨色 | `#131514` | 页面底色与面板 |
| 聊天灰 | `#343634` | 聊天页磨砂底板 |
| 输入胶囊 | `#F0EEEE` | 白色输入条与其文字列 |
| 警示橙 | `#FF6A52` | 危险与错误状态 |
| 确认绿 | `#35D69A` | 成功状态 |

## 预览

```sh
pnpm market:build                              # 刷新市场产物（market/dist）
open market/dist/preview.html?skin=endfield-baker&theme=light
```

`preview/light.png` 与 `preview/dark.png` 呈现同一套配色：本皮肤不按亮/暗
主题分叉。
