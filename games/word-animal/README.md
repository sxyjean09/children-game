# 认字游戏 · 小动物（word-animal）

> 宝宝的第一款认字游戏：从 2 个字的动物名称开始，图 + 字 + 选项 + 鼓励。

## 这是什么

- 玩法：屏幕中央展示一只动物 emoji，提示语形如 `它是 _狗` 或 `小_`，宝宝从 4 个大字选项里选出正确的那个字。
- 答对：动物做自己的招牌动作（小狗摇尾巴 / 小猫伸懒腰 / 小鸡抖翅膀 ...）+ 拟声词 TTS + 撒花 + 大字反馈语。
- 答错：按钮抖一下 + "再试试看～"，**不扣分、不惩罚、不消失**。

## 第一版内置 10 种动物

| Emoji | 名称 | 拟声词 | 动作 |
|-------|------|--------|------|
| 🐶 | 小狗 | 汪汪汪 | 摇尾巴 |
| 🐱 | 小猫 | 喵喵喵 | 伸懒腰 |
| 🐔 | 小鸡 | 叽叽叽 | 抖翅膀 |
| 🦆 | 小鸭 | 嘎嘎嘎 | 一摇一摆 |
| 🐰 | 小兔 | （蹦蹦跳跳） | 蹦蹦跳 |
| 🐟 | 小鱼 | （吐泡泡） | 游来游去 |
| 🐦 | 小鸟 | 叽叽喳喳 | 扇翅膀 |
| 🐷 | 小猪 | 哼哼哼 | 甩甩头 |
| 🐮 | 小牛 | 哞—— | 甩甩尾 |
| 🐑 | 小羊 | 咩咩咩 | 点点头 |

## 设计原则（按 AGENTS.md / SOUL.md 执行）

- **大按钮**：选项按钮高度 130px、字号 80px，整屏占比 ≥ 30%
- **大图标**：动物 emoji 180px，居中展示
- **操作容错**：答错只抖一下、给鼓励，不扣分不让动物消失
- **反馈强**：答对有拟声词 TTS + 撒花 + 弹大字 + 动物动作
- **不强制识字**：提示语"它是 _狗"留出空格视觉提示
- **不弹广告 / 不强制登录**
- **跨设备**：touch + mouse 都支持；iOS Safari 友好（需要用户点"开始"才能解锁 TTS）

## 怎么跑

### 本地预览

```bash
cd /Users/shenxiaoyu/.openclaw/workspace-coder/projects/children-game/games/word-animal
python3 -m http.server 8000
# 浏览器开 http://localhost:8000
```

### GitHub Pages 部署

项目已经放在 `children-game/games/word-animal/`，所以可以直接推到 `sxyjean09/children-game` 仓库的 main 分支，访问：

```
https://sxyjean09.github.io/children-game/games/word-animal/
```

具体步骤：
```bash
cd /Users/shenxiaoyu/.openclaw/workspace-coder/projects/children-game
git add games/word-animal/
git commit -m "feat(word-animal): 第一版认字游戏，10 种动物 + 拟声词 + 撒花"
git push origin main
```

## 已知限制 / 后续可改进

- [planned] **2.0 难度档**：把每题 4 选项改成 2 选项（更适合两岁孩子）
- [planned] **3.0 难度档**：加入更多 3 个字动物（小白兔 / 小花猫），加入「不」/「的」这种字
- [planned] **音效扩展**：摇尾巴动作现在只是 emoji 缩放，没真实动作；想做得更生动可以换 SVG / Lottie
- [planned] **拟声词自定义**：如果宝宝家里给某个动物起了别的拟声词，可以让家长改
- [planned] **关卡进度条**：当前只在顶部显示 1/10，未来可以加进度条可视化
- [planned] **顺序 / 乱序切换**：和停车场游戏一致地加乱序按钮
- [planned] **家长模式**：长按 logo 5 秒进入，关闭 TTS / 调节难度等

## 文件结构

```
games/word-animal/
├── index.html      # 单文件，全部内联（HTML + CSS + JS）
└── README.md       # 本文件
```
