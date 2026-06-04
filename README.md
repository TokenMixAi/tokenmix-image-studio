# TokenMix 图像工坊 · Image Studio

基于 TokenMix 的 AI 图像生成与编辑工具:文生图、图生图、局部重绘(inpaint),一个 key 即可调用 `gpt-image-2`、`seedream-5.0`、`flux-2-pro`、`imagen-4-ultra` 等多个图像模型。纯前端、数据存在你自己浏览器里。

## 快速开始

本工具默认已接入 TokenMix(`https://api.tokenmix.ai/v1`),无需改任何配置:

1. 到 [tokenmix.ai](https://tokenmix.ai) 注册,在控制台签发一个 `sk-tm-` 开头的 API Key
2. 打开工具,在「设置」里填入你的 Key
3. 开始生成。默认模型 `gpt-image-2`,也可在设置里改用 `seedream-5.0` / `flux-2-pro` / `imagen-4-ultra` 等 TokenMix 提供的图像模型

## 部署

纯前端应用,零后端、零运维。任选一种:

- **Cloudflare Pages / Vercel**:连接本仓库,构建命令 `npm run build`,输出目录 `dist`
- **Docker**:见 `deploy/` 目录
- **本地**:`npm ci && npm run build`,产物在 `dist/`

API Key 只保存在用户浏览器本地,不经过任何中间服务器。

## 关于

本项目基于开源项目 [GPT Image Playground](https://github.com/CookSleep/gpt_image_playground)(MIT License,作者 [@CookSleep](https://github.com/CookSleep))修改,将默认模型端点指向 TokenMix。感谢原作者。原项目的版权与 MIT 许可声明完整保留(见应用内「设置 → 关于」与 `LICENSE`)。

## License

MIT(沿用原项目,见 [LICENSE](./LICENSE))。
