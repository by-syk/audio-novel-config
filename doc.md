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
| `minmega` | float | 否 | 音频资源每分钟兆字节（mb/min） |
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
| `indexformat` | string | 否 | 章节序号格式，阿拉伯数字占位：{n}，中文数字占位：{N}（如“第 {n} 章”、“第{N}话”、“第{n}期”等） |
| `chapters` | array | 是 | 章节目录数组（有序） |
| | | | |
| `index` | integer | 是 | 章节序号（可重复；其他章节用非正整数表示） |
| `name` | string | 是 | 章节名 |
| `book` | string | 否 | 小说存在多部的情况下用于标明所属 |
| `res` | array | 否 | 分段音频资源数组，若无则暗示资源正在整理中 |
| | | | |
| `url` | string | 是 | 音频资源 URL |
| `id` | string | 是 | 资源 ID（用于本地缓存区分资源） |
| `format` | string | 否 | 资源文件格式，若无则与默认一致 |
| `start` | string | 否 | 音频截取开始时间（格式：“HH:mm:ss:SSS”），若无或空则为整段音频开始时间 |
| `end` | string | 是 | 音频截取结束时间（格式：“HH:mm:ss:SSS”） |

> Demo：[the-kings-avatar.json](novels/the-kings-avatar/data.json)
