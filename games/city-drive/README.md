# 城市小车 · 识字小游戏

10 个城市场景 + 10 种小车，让两岁多小朋友认识「油 / 警 / 学 / 医 / 消 / 邮 / 餐 / 园 / 市 / 工」10 个字。

## 怎么玩

1. 顶部任务条显示「请把 🚑 救护车开到 医院」
2. 点下面车库里的 🚑 救护车（被选中变黄）
3. 点场景里的医院 🏥
4. 小车开过去 → 撒花 → 大字「医」浮现 → 朗读"医！救护车到医院啦！"
5. 自动出下一题

## 玩什么

- **10 个场景**：加油站 ⛽、警察局 🚓、学校 🏫、医院 🏥、消防站 🚒、邮局 🏤、餐厅 🍽️、公园 🌳、超市 🛒、工地 🏗️
- **10 种小车**：油罐车 🚛、警车 🚓、校车 🚌、救护车 🚑、消防车 🚒、邮车 🚚、外卖车 🍕、观光车 🚐、购物车 🚙、工程车 🚜
- **城市布景**：横竖十字道路 + 黄色虚线 + 斑马线 + 红绿灯（自动切换）
- **目标高亮**：当前任务的建筑会脉冲动画 + 红色虚线光圈旋转

## 安卓无声音兜底（重点）

安卓部分机型 TTS 不能用，所以做了多重视觉兜底：

1. **顶部任务条** 永远显示「请把 🚑 救护车开到 医院」（最大字号 28px）
2. **目标建筑高亮**（脉冲 + 旋转光圈），眼睛就能跟着点
3. **点对时**：中间浮出大号红色「医」字（280px），同时撒花
4. **点错时**：屏幕红框闪烁 + 任务条更新文字「不对哦，救护车不是去餐厅的，再想想～」
5. **TTS 用女声 zh-CN**（如果系统装了）

## 跨设备

- iPhone / iPad / Mac / Android / Windows 都能玩
- 横屏竖屏自适应
- 触屏 + 鼠标都支持
- 单 HTML 文件，零依赖

## 怎么跑

### 本地测试

```bash
cd /Users/shenxiaoyu/.openclaw/workspace-coder/projects/children-game/games/city-drive
python3 -m http.server 8000
# 浏览器开 http://localhost:8000
# 或手机连同一 WiFi 访问 Mac IP
```

### 部署到 GitHub Pages

```bash
cd /Users/shenxiaoyu/.openclaw/workspace-coder/projects/children-game
git add games/city-drive/
git commit -m "feat(city-drive): 城市小车识字游戏，10 场景 + 安卓无声音兜底"
git push origin main
# 访问 https://sxyjean09.github.io/children-game/games/city-drive/
```

## 文件结构

```
city-drive/
├── index.html      # 单文件全功能（HTML + CSS + JS）
└── README.md       # 本文件
```

## 调试

- 跳过介绍页：URL 加 `?skip`
- 看浏览器控制台：F12 → Console

## 还可以更好（未做）

- 任务轮换：当前随机，可能连续出 2 次"医"
- 进度条：没记录"今天学了几个字"
- 撤销 / 上一个：点错后没法直接听正确答案，需要重新点
- 建筑点击区可能重叠（4-5 寸屏幕部分车开过去会盖住临近建筑）
