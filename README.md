# bing1118.github.io

打开就是一款游戏：奶龙 2048。纯静态、零依赖、零构建。

## 结构

```
bing1118.github.io/
├── index.html              # 奶龙 2048（单文件游戏，打开即玩）
├── .gitignore
└── img/
    └── tier-<等级>.png     # 11 张贴图：tier-02.png ~ tier-2048.png
```

命名约定：每个游戏一个文件夹，`index.html` 自包含（样式与逻辑全部内联），
贴图按 `tier-<2048 等级值>.png` 命名，与代码里的等级一一对应。

## 奶龙 2048 · 进化图鉴版

- 经典 2048 规则，11 级奶龙进化链，首次合出新等级点亮图鉴（localStorage 存档）。
- 闪光奶龙（×5 分）、连击加成、每局随机祝福、乱斗随机事件。
- 救援模式默认开：卡死不判负，随机救场继续玩。
- 方向键 / WASD / 手机滑动，棋盘按屏宽自动缩放。

## 部署

GitHub 建仓库 `bing1118.github.io`（与用户名同名），推送后 Settings → Pages → `main` / `(root)`。

```bash
git init
git add .
git commit -m "feat: 奶龙2048"
git branch -M main
git remote add origin https://github.com/bing1118/bing1118.github.io.git
git push -u origin main
```

## 致谢

奶龙贴图来自 [YHSome/BigNaiWa](https://github.com/YHSome/BigNaiWa)，版权归原作者，仅非商业同好使用。2048 玩法来自 Gabriele Cirulli。
