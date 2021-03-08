# 关于信息收集的一些记录

项目同步至：https://forum.ywhack.com/bountytips.php?getinfo

> 1.企业信息收集(企业信息/子公司/分公司/提供商/代理商等)

* [2021.03.07] - 🔗[天眼查 - 查企业/子公司/域名/公众号等](https://www.tianyancha.com/)
* [2021.03.07] - 🔗[爱企查 - 查企业/子公司/经营信息等（免费导出/免费调用）](https://aiqicha.baidu.com/)
* [2021.03.07] - 🔗[企查查 - 企业工商信息查询](https://www.qcc.com/)
* [2021.03.07] - 🔗[启信宝 - 企业信息查询](https://www.qixin.com/)
* [2021.03.07] - 🔗[cSubsidiary 天眼查自动信息收集工具](https://github.com/canc3s/cSubsidiary)
* [2021.03.07] - 🔗[站长之家 企业备案查询](http://icp.chinaz.com/)
* [2021.03.07] - ❗百度、Google等各类搜索引擎搜索企业信息(例如官网、关联公司、子域、网站地址、介绍、文件等等)

    ```
    site:*.domain.com
    inurl:domain.com
    intitle:keyword
    keyword filetyle:doc|pdf
    ```

* [2021.03.07] - ❗从各类公开媒体/通讯等渠道搜索企业相关信息,如：微博/微信/QQ/推特/钉钉等等...
* [2021.03.07] - ❗从网盘类可以搜企业关键词可以发现很多有用的资料,比如网盘搜，凌风云等等...
* [2021.03.07] - ❗各类招聘网站查找企业招聘信息,如果有可能还可以针对hr进行钓鱼/社工等.
* [2021.03.07] - ❗各省公开招标网站等,查询企业供应商信息等.
* [2021.03.08] - ❗查询企业服务器提供商/软件提供商等等.

> 2.资产信息搜集(子域/Web/APP/公众号/小程序/产品等)

* [2021.03.07] - 🔗[FOFA.so 利用fofa进行搜索公司相关资产](https://fofa.so/)

    ```
    title:domain.com
    header:xxx
    body:keyword
    ico-hash:xxx
    ```

* [2021.03.07] - 🔗[ZoomEye 使用钟馗之眼搜集企业相关资产](https://www.zoomeye.org/)
* [2021.03.07] - 🔗[搜狗微信 搜索企业相关微信公众号/文章等](https://weixin.sogou.com/)
* [2021.03.07] - 🔗[Shodan 搜索企业相关域名/IP/C段等信息](https://www.shodan.io/)
* [2021.03.07] - 🔗[phpinfo.me 在线子域名枚举](https://phpinfo.me/domain/)
* [2021.03.07] - 🔗[SecurityTrails 世界最大DNS数据库 可查很多子域名、历史解析等等信息](https://securitytrails.com/)
* [2021.03.07] - 🔗[censys.io 可以搜到很多有用的东西 比如真实IP 指纹 证书 域名等等](https://censys.io/)
* [2021.03.07] - 🔗[crt.sh 这个在线网站可以按通配符域名查询所有证书的详情](https://crt.sh/)
* [2021.03.07] - 🔗[RapidDNS 在线DNS查询工具 查询子域等等](https://rapiddns.io/)
* [2021.03.07] - 🔗[bgp.he.net 可以查询很多IP相关的信息](http://bgp.he.net/)
* [2021.03.07] - ❗很多在线的网站都能提取出网站的子域名等等.

    ```bash
    curl -s"http://web.archive.org/cdx/search/cdx?url=*.qq.com/*&output=text&fl=original&collapse=urlkey"|sort| sed -e's_https*://__'-e"s//.*//"-e's/:.*//'-e's/^www.//'| sort -u
    curl --silent https://sonar.omnisint.io/subdomains/domain.com | grep -oE "[a-zA-Z0-9._-]+\.freebuf.com" | sort -u
    curl --silent -X POST https://synapsint.com/report.php -d "name=https%3A%2F%2Ffreebuf.com" | grep -oE "[a-zA-Z0-9._-]+\.freebuf.com" | sort -u
    ....

    ```

* [2021.03.07] - ❗利用威胁情报平台进行一些资产的收集.

    ```url
    https://x.threatbook.cn
    https://ti.qianxin.com
    https://nti.nsfocus.com/apt/home
    https://ti.360.cn/#/homepage
    https://www.aisec.com/ti/
    .....

    ```

* [2021.03.07] - ❗从企业官网或子域名等页面元素/JS文件上进行提取有用的信息.这类工具很多,可以写个油猴脚本自动访问保存.

    ```url
    https://forum.ywhack.com/viewthread.php?tid=114800
    https://raw.githubusercontent.com/m4ll0k/Bug-Bounty-Toolz/master/jsalert.py
    .....

    ```

* [2021.03.07] - ❗代码托管平台上有很多好东西,比如Github上配合dorks就能搜索处很多信息.

    ```url
    https://github.com/obheda12/GitDorker
    .....

    ```

> 3.一些信息收集的工具

* [2021.01.19] - 🔗[EHole(棱洞)-红队重点攻击系统指纹探测工具](https://github.com/EdgeSecurityTeam/EHole)
* [2021.01.19] - 🔗[ESTeye(棱眼)-红蓝攻防中快速定位目标的真实资产](https://forum.ywhack.com/thread-114929-1-1.html)
* [2021.01.19] - 🔗[Nmap 好用的端口扫描工具](https://nmap.org/)
* [2021.01.19] - 🔗[DarkEye 渗透测试情报收集工具](https://github.com/zsdevX/DarkEye)
* [2021.01.19] - 🔗[AppInfoScanner 适用于红队的移动端(Android、iOS、WEB、H5、静态网站)信息收集工具](https://github.com/kelvinBen/AppInfoScanner)
* [2021.01.19] - 🔗[GitDorker Python程序，使用Github dorks从Github搜索敏感信息](https://github.com/obheda12/GitDorker)
* [2021.01.19] - 🔗[sherlock - 通过社交网络上的用户名搜寻社交媒体帐户](https://github.com/sherlock-project/sherlock)
* [2021.01.19] - 🔗[ServerScan一款使用Golang开发的高并发网络扫描、服务探测工具](https://github.com/Adminisme/ServerScan)
* [2021.01.19] - 🔗[Railgun是一款GUI界面的渗透工具，综合类的扫描工具](https://github.com/lz520520/railgun)
* [2021.01.19] - 🔗[OneForAll是一款功能强大的子域收集工具](https://github.com/shmilylty/OneForAll)
* [2021.01.20] - 🔗[dirsearch - Web path scanner 目录扫描工具](https://github.com/maurosoria/dirsearch)
* [2021.01.20] - 🔗[ffuf 用Go编写的模糊测试工具](https://github.com/ffuf/ffuf)
* [2021.01.20] - 🔗[用Rust编写的快速，简单，递归的内容发现工具](https://github.com/epi052/feroxbuster)
* [2021.01.21] - 🔗[Web Fuzzing Box - Web 模糊测试字典与一些Payloads](https://github.com/gh0stkey/Web-Fuzzing-Box)
* [2021.01.22] - 🔗[针对Webpack等前端打包工具构造的网站进行快速、高效安全检测的扫描工具](https://github.com/rtcatc/Packer-Fuzzer)
* [2021.01.22] - 🔗[apkleaks 用于APK的信息收集工具](https://github.com/dwisiswant0/apkleaks)
* [2021.03.07] - 🔗[cSubsidiary 天眼查自动信息收集工具](https://github.com/canc3s/cSubsidiary)

此项目不定期进行更新......

