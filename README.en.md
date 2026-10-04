# WeChat Article Reading Brief

Read one to three public WeChat article URLs in a user-selected browser and receive traceable conclusions, steps, author, date, source, and visible gaps. Deleted, login-gated, verified, or truncated pages are reported honestly; summaries are never presented as full text.

![Promo artwork](promo.png)

## Input and output

Provide 1–3 public URLs, focus questions, and a user-selected `browserId`. The result records each article's main conclusion, key steps, author/date/source URL, and visible limitations. It is intended for a short article, section, or single scenario; tables are capped at 100 rows.

## Install

```bash
npx skills add xxjrq/wechat-article-reading-brief-free
```

This browser Skill requires Easy WebBridge: [GitHub](https://github.com/xxjrq/easy-webbridge) or [Gitee mirror](https://gitee.com/xxjrq/easy-webbridge). It uses one owned session group per task and never broadcasts to accounts or takes over existing tabs.

Run `node scripts/self-test.mjs` to validate local metadata, fixtures, and image dimensions. Fixtures are offline page simulations, not online collection results.

## License and reference

MIT; see [LICENSE](LICENSE). The workflow independently references [OpenCLI](https://github.com/jackwener/OpenCLI) and its [WeChat adapter note](https://github.com/jackwener/OpenCLI/blob/main/docs/adapters/browser/weixin.md), without copying their implementation.
