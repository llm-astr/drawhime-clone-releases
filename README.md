# drawhime-clone-releases
DrawHime Clone 本地 AI 生图客户端 · 官方安装包发布仓库（自动更新源）

## 最新版本：v0.3.8（2026-09-16）

修复在新电脑安装后「启动引擎」报错的问题（旧版本错误引用开发机上的固定路径，本版已移除并自动纠正旧数据）。

无预置密钥安全版：安装包内不含任何 API Key 与 LoRA 文件。首次启动后请在「设置」中配置 grsai API Base URL 与 API Key。

- 文件：DrawHime-Clone-Setup-0.3.8.exe
- 大小：171,670,292 字节（约 164 MB）
- SHA256：`e6df70e953b564e7b9e19c65399a5256aca11b549feee34a1d826868ddccd933`

## 下载与合并（Windows）

GitHub 单文件限制，安装包以 14 个 base64 分卷存储（文件名后缀 `.001` ~ `.014`）。

1. 下载全部 14 个分卷（把下面命令里的 `{版本}` 换成 `0.3.8` 或 `0.3.7`，匿名可直接下载）：
   - `https://cdn.jsdelivr.net/gh/llm-astr/drawhime-clone-releases@main/DrawHime-Clone-Setup-{版本}.exe.b64.NNN`
   - 备选：`https://raw.githubusercontent.com/llm-astr/drawhime-clone-releases/main/DrawHime-Clone-Setup-{版本}.exe.b64.NNN`
2. 分卷放在同一文件夹，按顺序合并 base64 文本（以 0.3.8 为例）：

   ```
   copy /b DrawHime-Clone-Setup-0.3.8.exe.b64.001+DrawHime-Clone-Setup-0.3.8.exe.b64.002+DrawHime-Clone-Setup-0.3.8.exe.b64.003+DrawHime-Clone-Setup-0.3.8.exe.b64.004+DrawHime-Clone-Setup-0.3.8.exe.b64.005+DrawHime-Clone-Setup-0.3.8.exe.b64.006+DrawHime-Clone-Setup-0.3.8.exe.b64.007+DrawHime-Clone-Setup-0.3.8.exe.b64.008+DrawHime-Clone-Setup-0.3.8.exe.b64.009+DrawHime-Clone-Setup-0.3.8.exe.b64.010+DrawHime-Clone-Setup-0.3.8.exe.b64.011+DrawHime-Clone-Setup-0.3.8.exe.b64.012+DrawHime-Clone-Setup-0.3.8.exe.b64.013+DrawHime-Clone-Setup-0.3.8.exe.b64.014 setup.b64
   ```

3. 解码生成安装包：

   ```
   certutil -decode setup.b64 DrawHime-Clone-Setup-0.3.8.exe
   ```

4. 校验（可选）：

   ```
   certutil -hashfile DrawHime-Clone-Setup-0.3.8.exe SHA256
   ```

   结果应等于 `e6df70e953b564e7b9e19c65399a5256aca11b549feee34a1d826868ddccd933`。

可视化下载站（含分卷直链与图文教程）：https://miaoda.feishu.cn/app/app_17e77c9zdns

## 历史版本

| 版本 | 日期 | 说明 |
| --- | --- | --- |
| v0.3.8 | 2026-09-16 | 修复新电脑启动引擎报错（移除开发机固定路径，自动纠正旧数据），当前推荐 |
| v0.3.7 | 2026-09-16 | 去密钥安全版（已知问题：新电脑首次启动引擎会报错，请用 v0.3.8） |

### v0.3.7 存档

- 文件：DrawHime-Clone-Setup-0.3.7.exe，大小 171,669,982 字节
- SHA256：`dd0f2cbadd0d94a69299bc30e59e12fb333e03ef953f5fba1849946c6a801bd2`
- 分卷：`DrawHime-Clone-Setup-0.3.7.exe.b64.001` ~ `.014`（同上下载方式）
