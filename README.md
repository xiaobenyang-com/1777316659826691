# 智能搜索工具集 

Smart Search MCP 是一个专注于技术领域的智能搜索工具集，提供14个增强型搜索工具，覆盖国际和国内主流技术平台，具备智能URL生成、输入验证、高级搜索技巧等功能，适用于开发者快速查找技术文档、API参考、开源项目等。
Smart Search MCP is an intelligent search toolkit focused on the technology field, providing 14 enhanced search tools covering mainstream international and domestic technology platforms. It has functions such as intelligent URL generation, input verification, and advanced search techniques, making it suitable for developers to quickly find technical documents, API references, open source projects, etc.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| ai_search_web | 🔍 网络搜索 - 通用网络搜索（Google/Bing/百度/搜狗）  【重要】此工具会返回搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |
| ai_search_github | 🐙 GitHub搜索 - 搜索GitHub仓库、代码、问题和用户  【重要】此工具会返回GitHub搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |
| ai_search_stackoverflow | 💬 StackOverflow搜索 - 搜索技术问题和解决方案  【重要】此工具会返回StackOverflow搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |
| ai_search_npm | 📦 NPM包搜索 - 搜索NPM包和相关文档  【重要】此工具会返回NPM搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |
| ai_search_docs | 📚 技术文档搜索 - 搜索常见框架和工具的官方文档（React、Vue、Node.js等）  【重要】此工具会返回文档搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |
| ai_search_api_reference | 🔗 API参考搜索 - 快速查找API文档和使用示例  【重要】此工具会返回API文档搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |
| ai_search_wechat_docs | 📱 微信开发者文档搜索 - 搜索微信小程序、公众号、开放平台文档  【重要】此工具会返回微信文档搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |
| ai_search_csdn | 📝 CSDN搜索 - 搜索CSDN技术博客和问答  【重要】此工具会返回CSDN搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |
| ai_search_juejin | 💎 掘金搜索 - 搜索掘金技术社区文章  【重要】此工具会返回掘金搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |
| ai_search_segmentfault | 🔧 SegmentFault搜索 - 搜索思否技术问答和文章  【重要】此工具会返回SegmentFault搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |
| ai_search_cnblogs | 📚 博客园搜索 - 搜索博客园技术博客  【重要】此工具会返回博客园搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |
| ai_search_oschina | 🌐 开源中国搜索 - 搜索开源中国技术资讯和项目  【重要】此工具会返回开源中国搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |
| ai_search_aliyun_docs | ☁️ 阿里云文档搜索 - 搜索阿里云产品文档和API  【重要】此工具会返回阿里云文档搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |
| ai_search_tencent_docs | ☁️ 腾讯云文档搜索 - 搜索腾讯云产品文档和API  【重要】此工具会返回腾讯云文档搜索URL，Claude Code应该使用WebFetch工具访问该URL以获取真实搜索结果。 |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659826691](https://mcp.xiaobenyang.com/inspector/1777316659826691)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659826691](https://mcp.xiaobenyang.com/inspector/1777316659826691)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "智能搜索工具集": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659826691/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "智能搜索工具集": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659826691/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "智能搜索工具集": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659826691",
          },
          "transport": "stdio"
        }
      }
}

```
