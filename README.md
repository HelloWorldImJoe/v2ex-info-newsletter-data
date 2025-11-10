# v2ex-info-newsletter-data
日报数据

---

### 数据来源
数据来源于 [v2ex-info-data](https://data.v2ex.info)，由 [@JoeJoeJoe](https://www.v2ex.com/member/JoeJoeJoe) 提供。

### 数据格式
数据以 JSON 格式存储，每条记录字段描述如下：

> 时间为 UTC+8 时区

```
/// 日常运营数据json, 每分钟一条记录
hodl_snapshots.json {
    "id": 1,
    "hodl_10k_addresses_count": 1234,  // 持有至少 10,000 V2EX 代币的钱包地址数量
    "new_accounts_via_solana": 2017, // 通过 Solana 链接创建的新账户数量
    "total_solana_addresses_linked": 7889, // 通过 Solana 链接的钱包地址数量
    "sol_tip_operations_count": 4166, // Solana打赏次数
    "member_tips_sent": 460, // 会员发送的打赏总数
    "member_tips_received": 3153, // 会员收到的打赏总数
    "total_sol_tip_amount": 31.3648, // Solana打赏总金额
    "v2ex_token_tip_count": 1468, // V2EX代币打赏次数
    "total_v2ex_token_tip_amount": 235529.03, // V2EX代币打赏总金额
    "created_at": "2025-11-08 15:59:01", // 记录创建时间
    "current_online_users": 2358, // 当前在线用户数
    "peak_online_users": 6679, // 峰值在线用户数
    "holders": 4392, // V2EX 代币持有者数量
    "price": 0.003088832778846265, // V2EX 代币当前价格（美元）
    "price_change_24h": -1.7835432672931189, // V2EX 代币24小时价格变化百分比
    "btc_price": 101634.025, // 比特币当前价格（美元）
    "sol_price": 156.445, // Solana 当前价格（美元）
    "pump_price": 0.003682 // PUMP 代币当前价格（美元）
}

/// 持币地址变化记录, 每30分钟抓取一次, 如果有变化则新增一条记录
solana_address_details.json {
    "id": 3365,
    "owner_address": "7j8RCpqZJzQbCwzPPaDWpoHa9mFx7GL2Km4Fsfws7TKG", // 钱包地址
    "token_address": "9raUVuzeWUk53co63M4WXLWPWE4Xc6Lpn7RS9dnkpump", // 代币地址
    "token_account_address": "7tUCiw2Zp7dh8gzuqLXRv4odEKr6FVEgVjLEm9FAetgz", // 代币账户地址
    "v2ex_username": null, // 关联的 V2EX 用户名
    "avatar_url": null, // 头像 URL
    "hold_rank": 9, // 持有排名
    "hold_amount": 5024795.170572, // 持有数量
    "decimals": 6, // 代币小数位数
    "hold_percentage": 0.5024795170572001, // 持有比例
    "rank_delta": 0, // 排名变化
    "amount_delta": -2488.491408, // 数量变化
    "changed_at": "2025-11-08 15:31:34" // 记录变化时间
}

/// 持币地址排名, 每30分钟抓取一次完整排名数据, 只抓取前120名
solana_addresses.json {
    "id": 5,
    "owner_address": "DdGV4neesEuQUS5cX3x9A9An5i6BBJkPhHEN6PA3aRkf", // 钱包地址
    "v2ex_username": null, // 关联的 V2EX 用户名
    "avatar_url": null, // 头像 URL
    "token_address": "9raUVuzeWUk53co63M4WXLWPWE4Xc6Lpn7RS9dnkpump", // 代币地址
    "token_account_address": "GyHpdW7ei2g33oex16ToGfTQB4bPBY4Jfn6Wvd7Kou57", // 代币账户地址
    "hold_rank": 5, // 持有排名
    "hold_amount": 9032999.623853, // 持有数量
    "decimals": 6, // 代币小数位数
    "rank_delta": 0, // 排名变化
    "hold_percentage": 0.9032999623853001, // 持有比例
    "checked_at": "2025-11-08 00:31:08", // 记录检查时间
    "amount_delta": 0 // 数量变化
}

/// 前120名持币地址移除记录, 当地址不再位于前120名时新增一条记录
solana_addresses_removed.json {
    "id": 53,
    "owner_address": "E95MwfVAMes55C27Va4FnMJbqAbPj9VUpqD1KgWwgsVB", // 钱包地址
    "v2ex_username": null, // 关联的 V2EX 用户名
    "avatar_url": null, // 头像 URL
    "token_address": "9raUVuzeWUk53co63M4WXLWPWE4Xc6Lpn7RS9dnkpump", // 代币地址
    "token_account_address": "GzAXP1dwd4KSpGprFkcyTtMLdDWeRn9h2Hcyd7opdQjG", // 代币账户地址
    "hold_rank": 23, // 持有排名
    "hold_amount": 1779060.669985, // 持有数量
    "decimals": 6, // 代币小数位数
    "hold_percentage": 0.1779060669985, // 持有比例
    "rank_delta": 0, // 排名变化
    "removed_at": "2025-11-07 18:30:12" // 记录移除时间
}
```