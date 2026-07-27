# 🚂 宝宝游戏屋

给小朋友们做的学习小游戏合集：学字母、学数字、玩中学。

**在线玩**：https://sxyjean09.github.io/children-game/

## 🎮 已上线的游戏

| 游戏 | 学习目标 | 适合 |
| --- | --- | --- |
| 🚂 [小火车拼字母](./games/train-alphabet/) | 26 个字母 + 拼音认读 | 2–5 岁 |
| 🅿️ [停车场找车位](./games/parking/) | 字母 + 数字（1–10） | 2–5 岁 |
| 🌉 [小车过字母桥](./games/bridge/) | 字母 + 数字（1–10） | 2–5 岁 |

## ✨ 设计原则

- **跨设备**：iPhone / iPad / Mac / Android / Windows 都能玩，触屏 + 鼠标都行
- **大按钮、大图标**：适合手指控制力弱的小朋友
- **容错强**：点错不扣分、不惩罚、不吓娃
- **反馈多**：TTS 朗读字母/数字 + Web Audio 兑底音效
- **不弹广告、不登录、不收费**

## 🛠️ 本地开发

```bash
# 任意目录下克隆
git clone https://github.com/sxyjean09/children-game.git
cd children-game

# 起一个静态服务器
python3 -m http.server 8000

# 浏览器打开
open http://localhost:8000
```

每个游戏是独立的单文件 `index.html`，没有构建步骤，改了就能用。

## 📁 仓库结构

```
children-game/
├── index.html              # 游戏大厅（首页）
├── games/
│   ├── train-alphabet/     # 🚂 小火车拼字母
│   ├── parking/            # 🅿️ 停车场找车位
│   └── bridge/             # 🌉 小车过字母桥
└── README.md
```

## 🚀 部署

GitHub Pages 自动部署（root + main 分支），push 即上线。

## 📝 后续计划

- 📦 集装箱码头（大小写配对、数字与数量对应）
- ⛽ 加油站（数字识别）
- 🇨🇳 简单汉字关卡（人/大/小/上/下/口/日）
- 🎵 背景音乐 + 关卡通关奖励