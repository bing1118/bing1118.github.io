# bing1118.github.io

两个自己写的小东西，纯静态、零依赖、零构建。

## 结构

```
bing1118.github.io/
├── index.html              # 入口：两个小玩意
├── .gitignore
└── game/
    ├── nailong-2048/
    │   ├── index.html      # 奶龙 2048（单文件游戏，全部逻辑内联）
    │   └── img/
    │       └── tier-<等级>.png   # 11 张贴图：tier-02.png ~ tier-2048.png
    └── answers-book/
        └── index.html      # 答案之书（单文件，188 条答案内联）
```

命名约定：每个游戏一个文件夹，`index.html` 自包含（样式与逻辑全部内联），
贴图按 `tier-<2048 等级值>.png` 命名，与代码里的等级一一对应。

## 奶龙 2048 · 进化图鉴版

- 经典 2048 规则，11 级奶龙进化链，首次合出新等级点亮图鉴（localStorage 存档）。
- 闪光奶龙（×5 分）、连击加成、每局随机祝福、乱斗随机事件。
- 救援模式默认开：卡死不判负，随机救场继续玩。
- 方向键 / WASD / 手机滑动，棋盘按屏宽自动缩放。

## 答案之书

- 心里想着问题，点封面翻开随机一页；也可以用页码输入框直达任意一页，或前后翻页浏览。
- 188 条手写答案，楷体排版，黑色烫金封面 + 翻页动画。
- 测试钩子：`__ba_state()` / `__ba_open(p)`。

## 部署

GitHub 建仓库 `bing1118.github.io`（与用户名同名），推送后 Settings → Pages → `main` / `(root)`。

```bash
git init
git add .
git commit -m "feat: 奶龙2048 + 答案之书"
git branch -M main
git remote add origin https://github.com/bing1118/bing1118.github.io.git
git push -u origin main
```

## 致谢

奶龙贴图来自 [YHSome/BigNaiWa](https://github.com/YHSome/BigNaiWa)，版权归原作者，仅非商业同好使用。2048 玩法来自 Gabriele Cirulli。
