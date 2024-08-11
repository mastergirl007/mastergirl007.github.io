# 使用GitHub pages 托管个人博客并使用cloudflare的免费cdn的优选域名加速
## 方法一
cdn.主域名→（cname）→优选域名（cf网关）→（自定义主机名/回退源）→fallback.副域名→（cname）→gb.副域名→（A解析）→GitHub网关→（pages服务/自定义cdn.主域名）→仓库图片
## 方法二
cdn.主域名→（cname）→优选域名（cf网关）→（自定义主机名/回退源）→fallback.副域名→（cname）→GitHub_pages网址→（pages服务/自定义cdn.主域名）→仓库图片
## 注意
主域名不能托管在cloudflare，副域名要托管在cloudflare，如果都在，会出现1001错误
自定义主机名/回退源的 根本逻辑是 如果有用户通过特定域名即“自定义主机名”访问了cf，那么cf就会将访问传递给“回退源”
优选域名 cfip.cfcdn.vip 115155.xyz
ps 使用GitHub托管的博客，如果直接传图片，是挂载在GitHub上的，几乎无法打开，需要使用国内第三方图床
![1719901769-2024_mkt_m7_banner.png](https://p0.meituan.net/csc/b6d4c3210f889cc92c14496d31b124d4347279.png)
