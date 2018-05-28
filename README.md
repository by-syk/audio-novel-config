# audio-novel-config

### novels.json 有声小说目录

| JSON 字段 | 描述 |
| :--: | :-- |
| `novels` | 小说目录 |
| | |
| `name` | 小说名 |
| `id` | 小说 ID |
| `orator` | 播音作者 |
| `source` | 音频资源来源 |
| `maintainer` | 数据维护人员（格式：名 <邮>） |
| `update` | 数据最近更新日期（格式：**yyyyMMdd**） |
| `res` | 小说章节数据 URL |

### novels/xxx.json 小说章节数据

| JSON 字段 | 描述 |
| :--: | :-- |
| `total` | 章节数 |
| `chapters` | 章节目录 |
| | |
| `index` | 章节序号 |
| `name` | 章节名 |
| `res` | 分段音频资源 |
| | |
| `url` | 音频资源 URL |
| `id` | 资源 ID（用于本地缓存区分资源） |
| `format` | 资源文件格式（如 `.m4a`） |
| `start` | 音频截取开始时间（Premiere 格式） |
| `end` | 音频截取结束时间（Premiere 格式） |
