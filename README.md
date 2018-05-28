# audio-novel-config

### novels.json 有声小说目录

| JSON 字段 | 类型 | 必须 | 描述 |
| :--: | :--: | :--: | :-- |
| `novels` | array | 是 | 小说目录 |
| | | | |
| `name` | string | 是 | 小说名 |
| `id` | string | 是 | 小说 ID |
| `orator` | string | 是 | 播音作者 |
| `source` | string | 是 | 音频资源来源 |
| `maintainer` | string | 是 | 数据维护人员（格式：名 <邮>） |
| `done` | boolean | 是 | 数据整理状态 |
| `updated` | string | 是 | 数据最近更新日期（格式：**yyyyMMdd**） |
| `res` | string | 是 | 小说章节数据 URL |

> Demo：[novels.json](novels.json)

### novels/xxx.json 小说章节数据

| JSON 字段 | 类型 | 必须 | 描述 |
| :--: | :--: | :--: | :-- |
| `total` | integer | 是 | 章节数 |
| `chapters` | array | 是 | 章节目录 |
| | | | |
| `index` | integer | 是 | 章节序号 |
| `name` | string | 是 | 章节名 |
| `res` | array | 是 | 分段音频资源 |
| | | | |
| `url` | string | 是 | 音频资源 URL |
| `id` | string | 是 | 资源 ID（用于本地缓存区分资源） |
| `format` | string | 是 | 资源文件格式（如 `.m4a`） |
| `start` | string | 否 | 音频截取开始时间（Premiere 格式），如无或空则为整段音频开始时间 |
| `end` | string | 否 | 音频截取结束时间（Premiere 格式），如无或空则为整段音频结束时间 |

> Demo：[the-kings-avatar.json](novels/the-kings-avatar.json)
