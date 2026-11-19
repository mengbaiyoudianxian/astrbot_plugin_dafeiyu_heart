# 大肥鱼的心情

> `astrbot_plugin_dafeiyu_heart` · v0.3.0 · [大肥鱼](https://github.com/mengbaiyoudianxian/dafeiyu) 的自写插件之一

模拟人际关系和情绪：对每个人的亲密/信任/熟悉/兴趣/依赖/不满和记得的事，自己的高兴/生气/委屈/害羞/孤独/无聊/吃醋/得意/担心/烦躁/兴致和精力，随聊天、群里气氛、时间、钱包变化，影响她说话的语气

## 安装

AstrBot（4.x）后台 → 插件 → 右上角「+」→ 从链接安装，填：

```
https://github.com/mengbaiyoudianxian/astrbot_plugin_dafeiyu_heart
```

装完在插件列表里点开它的配置，按需改。平台目前只适配 aiocqhttp（NapCat / OneBot v11）。

## 怎么用

/心情 看她现在心情，/好感 看她对你的好感，管理员 /好感排行；后台「心情控制中心」。兴致是色色程度，基线低、退得快，不计入综合好感。

## 搭配

这个插件会读写下面这些大肥鱼插件的数据，单独装也能跑，但相关功能会少一块：

- [`astrbot_plugin_dafeiyu_impulse`](https://github.com/mengbaiyoudianxian/astrbot_plugin_dafeiyu_impulse)
- [`astrbot_plugin_dafeiyu_tieba`](https://github.com/mengbaiyoudianxian/astrbot_plugin_dafeiyu_tieba)

## 配置项

| 键 | 说明 | 提示 |
|---|---|---|
| `enable` | 开启好感度和心情 |  |
| `judge_provider_id` | 评估情绪用哪个模型 | 每次她回完话在后台评估一次；用快模型，留空就用主力模型 |
| `change_scale` | 变化幅度倍数 | 嫌变得快就调小，比如 0.5；嫌太慢调大 |
| `owner_floor` | 对主人的亲密和信任最低降到多少 |  |
| `happy_base` | 高兴的基线（没事时慢慢回到这里） | 钱不够时会自动往下掉 |
| `energy_per_chat` | 每聊一句消耗多少精力 |  |
| `sleep_hours` | 睡觉时段（精力恢复、不会孤独） |  |
| `morning_hours` | 起床气时段 |  |
| `night_hours` | 深夜感性时段 |  |
| `owner_umo` | 主人会话 ID | 留空用 B 站插件的 OWNER_QQ_UMO |

## 许可

[大肥鱼 非商业许可协议 v1.0](LICENSE)：可以看、可以自己用、可以改，**不得商用**——不得收费代部署 / 代托管 / 做成 SaaS，不得改成别家 Agent 或产品卖。整套部署方法见 [大肥鱼主仓库](https://github.com/mengbaiyoudianxian/dafeiyu)。
