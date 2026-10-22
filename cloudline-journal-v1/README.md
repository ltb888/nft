# Cloudline Journal | 云际手记 — TON NFT 原创项目 V1

全新独立原创风景 NFT，不引用旧合集、旧钱包或 +888。

**当前状态：只完成资源和部署准备；未创建新钱包，未部署新合集，也未铸造 NFT。**

- 合集名称：Cloudline Journal
- 首枚 NFT：Morning Valley #001
- 封面：assets/cover.webp
- 单枚作品：assets/morning-valley-001.webp
- 链上集合元数据：管理员钱包签名部署时写入，和 metadata/collection.json 相匹配
- 单枚 NFT 元数据：GitHub 已发布的 metadata/item-001.json

## 钱包与部署保护

1. 在自己的 Tonkeeper 中新增全新钱包，备份助记词，不向服务器或聊天发送助记词。
2. 只提供钱包公开 TON 主网地址，作为合集管理员、付款人及第一枚 NFT 接收者。
3. 从 config.example.json 生成 config.json，把两个 NEW_TON_WALLET_ADDRESS 替换为同一真实新地址。不要在 config 中保存私钥。
4. 用 npm ci、npm run typecheck、npm run preflight 验证资源和收款地址。
5. npm run mint 触发 TonConnect 请求，必须本人确认。代码预计发送 0.15 TON，实际所需余额应覆盖费用，至少 0.2 TON，建议留足手续费。
6. 若部署记录存在，禁止重复发送；先以区块浏览器/TONAPI 确认合约与 NFT。

配置不能用旧钱包；所有合约地址均由新钱包部署后产生。Tonkeeper 的 UNVERIFIED 状态不因换钱包自动消除，需根据官方规则审核。
