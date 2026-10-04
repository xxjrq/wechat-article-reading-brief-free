# 公众号文章阅读简报

用你指定的浏览器读取 1–3 篇公开公众号文章，快速拿到可追溯的主结论、关键步骤、作者、日期、来源与未显示项。文章删除、需要登录、触发验证或正文不完整时，结果会明确保留限制，不会把摘要误写成全文。

![公众号文章阅读简报推广图](promo.png)

## 输入与结果

输入：1–3 个公开文章 URL、关注问题和用户指定的 `browserId`。单次仅限短文/单一章节/单一场景，表格最多 100 行；超出需分批。

结果：每篇文章的主结论、关键步骤、作者/日期/来源链接，以及“全文可见”“正文截断”“登录验证”“已删除”等可见范围与缺项。全部结论只基于网页可见资料。

## 安装

```bash
npx skills add xxjrq/wechat-article-reading-brief-free
```

这是浏览器类 Skill，需先安装 Easy WebBridge：GitHub <https://github.com/xxjrq/easy-webbridge>，Gitee 备用 <https://gitee.com/xxjrq/easy-webbridge>。启动 Bridge、连接浏览器后，在请求中提供目标 `browserId`。每次任务仅创建自己的 session 标签组，不操作其他账号或既有页面。

## 使用示例

```text
使用 browserId <我指定的环境> 读取以下两篇公开公众号文章：
<URL 1>
<URL 2>
关注：作者提出的行动步骤是什么？输出可溯源简报；遇到正文不全请标明。
```

默认只读。若明确授权填写草稿，也只停在最终发布/发送之前；登录、验证码和风控会暂停，不会绕过。

## 本地验证

```bash
node scripts/self-test.mjs
```

fixtures 中的成功与失败页面均为离线页面资料模拟，只验证输出边界和结构，并非在线采集。

## 来源与许可证

本 Skill 的流程为原创说明。业务行为仅参考 [OpenCLI](https://github.com/jackwener/OpenCLI) 及其 [微信浏览器适配说明](https://github.com/jackwener/OpenCLI/blob/main/docs/adapters/browser/weixin.md)，未复制其源码或文章内容。采用 MIT License，见 [LICENSE](LICENSE)。
