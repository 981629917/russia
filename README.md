# 俄罗斯方块 Tetris（Vibe Coding 部署作业）

一个纯前端、单文件的俄罗斯方块小游戏，支持电脑键盘和手机触屏操作。无需数据库、无需后端，符合「GitHub + Vercel」部署作业要求。

## 功能
- 7 种标准方块（I/O/T/S/Z/J/L）、旋转（带简易踢墙）
- 得分 / 消行 / 等级，等级越高下落越快
- 下一个方块预览、暂停 / 重开
- 电脑：← → 移动，↑ 旋转，↓ 加速，空格 瞬落，P 暂停
- 手机：屏幕下方按钮操作

## 本地运行（Mac）
```bash
cd tetris
python3 -m http.server 8000
# 浏览器打开 http://localhost:8000
```

## 部署到 Vercel（GitHub + Vercel 方案）
1. 把代码推到 GitHub：
   ```bash
   cd tetris
   git init
   git add .
   git commit -m "我的第一个俄罗斯方块"
   git branch -M main
   git remote add origin https://github.com/你的用户名/tetris.git
   git push -u origin main
   ```
   > ⚠️ GitHub 自 2021 起 HTTPS 推送不再接受账号密码，弹密码时填 Personal Access Token；
   > 或先 `brew install gh` 然后 `gh auth login`，之后推送不再要密码。
2. 打开 vercel.com → Continue with GitHub 登录
3. Add New Project → Import 你的 `tetris` 仓库
4. Framework Preset 选 **Other**（纯静态 HTML）
5. 点 Deploy → 约 1 分钟拿到 `xxx.vercel.app`
6. 把链接发到手机微信，能打开即上线成功 ✅
