互动眼球：免费起步模板

文件：
- index.html：完整的眼球追踪页面
- eye-white.png：眼白透明底素材
- iris.png：虹膜透明底素材
- pupil.png：瞳孔透明底素材

使用：
1. 把你自己的三张 PNG 放进这个文件夹。
2. 文件名分别改成 eye-white.png、iris.png、pupil.png。
3. 三张图需要保持相同画布尺寸和相同对齐位置。
4. 打开 index.html 即可先在浏览器本地预览。

调整：
- 在 index.html 中找到 MAX_X 和 MAX_Y。
- 0.035 代表最大移动幅度约为眼睛显示尺寸的 3.5%。
- 想移动更明显可以试 0.05；想更轻微可以试 0.02。
- 如果素材不是正方形，把 #eye 的 aspect-ratio 改成素材宽 / 高，例如 1000 / 600。

免费发布：
可以把这三个 PNG 和 index.html 放进一个 GitHub 公开仓库，再在仓库 Settings -> Pages 中选择从 main 分支发布。
GitHub Pages 的免费方案要求仓库公开，因此不要把个人隐私或不想公开的文件放进去。

注意：
这个模板是独立网页，不会自动嵌入 Straw.Page。能否免费嵌入仍取决于 Straw.Page 是否开放外部 iframe/embed 功能。
