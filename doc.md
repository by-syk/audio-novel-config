### novels.json 有声小说目录

| JSON 字段 | 类型 | 必须 | 描述 |
| :--: | :--: | :--: | :-- |
| `novels` | array | 是 | 小说目录数组 |
| | | | |
| `name` | string | 是 | 小说名 |
| `id` | string | 是 | 小说 ID |
| `orator` | string | 是 | 播音作者 |
| `source` | string | 是 | 音频资源来源 |
| `maintainer` | string | 是 | 数据维护人员（格式：“名, …”或“名 <邮>, …”） |
| `done` | boolean | 是 | 数据整理状态 |
| `ps` | string | 否 | 维护人员备注 |
| `res` | string | 是 | 小说章节数据 URL |
| `cover` | string | 否 | 小说封面图片 URL |
| `updated` | string | 是 | 数据最近更新日期（格式：“yyyyMMdd”） |

> Demo：[novels.json](novels/data.json)

### novels/xxx.json 小说章节数据

| JSON 字段 | 类型 | 必须 | 描述 |
| :--: | :--: | :--: | :-- |
| `total` | integer | 是 | 章节数 |
| `resformat` | string | 是 | 默认音频资源文件格式（如 `.m4a`） |
| `chapters` | array | 是 | 章节目录数组 |
| | | | |
| `index` | integer | 是 | 章节序号（可重复；其他章节用非正整数表示） |
| `name` | string | 是 | 章节名 |
| `book` | string | 否 | 小说存在多部的情况下用于标明所属 |
| `res` | array | 否 | 分段音频资源数组，若无则暗示资源正在整理中 |
| | | | |
| `url` | string | 是 | 音频资源 URL |
| `id` | string | 是 | 资源 ID（用于本地缓存区分资源） |
| `format` | string | 否 | 资源文件格式，若无则与默认一致 |
| `start` | string | 否 | 音频截取开始时间（Premiere 格式），若无或空则为整段音频开始时间 |
| `end` | string | 是 | 音频截取结束时间（Premiere 格式） |

> Demo：[the-kings-avatar.json](novels/the-kings-avatar/data.json)
