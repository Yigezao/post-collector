# Post Collector · 帖子采集与结构化归档

> 面向内容整理的小工具集：从短视频/图文平台采集帖子文本与图片，做 OCR 与语音转写，
> 补全地理信息，最终沉淀成结构化的「景点库」。

## 能力

- **帖子采集**：基于 CDP 驱动浏览器，采集抖音 / 小红书的帖子文本与媒体
- **内容解析**：图片 OCR、音视频转写
- **地理补全**：按城市/关键词搜索景点，调用高德接口补全坐标与地址
- **结构化输出**：统一 schema 校验后落成可检索的库

## 目录

| 文件 | 作用 |
|---|---|
| `collect_post.py` / `douyin_post.py` / `xhs_post.py` | 各平台帖子采集 |
| `cdp_driver.py` / `login_site.py` | 浏览器驱动与登录态处理 |
| `discover_places.py` / `city_ids.py` / `geo_amap.py` | 景点发现与地理信息补全 |
| `ocr_images.py` / `transcribe.py` | OCR 与语音转写 |
| `post_schema.py` / `library_emit.py` | 数据结构定义与库输出 |
| `build_*.py` | 批量构建脚本 |

## 说明

- 本仓库**仅包含工具源码**，不含任何采集结果、浏览器配置或第三方模型文件。
- 采集需遵守目标平台的服务条款与 robots 规则，请自行确保合规使用。
