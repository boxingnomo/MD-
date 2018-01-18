# ShadowsSocks客户端：

# ios-Surge到PC-ShadowsSocks

 [https://www.textarea.com/ExpectoPatronum/shiyong-shadowsocks-kexue-shangwang-265/](https://www.textarea.com/ExpectoPatronum/shiyong-shadowsocks-kexue-shangwang-265/) 

## Q1：Surge是什么？

![](https://static.notion-static.com/c5a0a91846a34d17ae1a1de9f266c600/d009b3de9c82d158393ac141860a19d8bd3e4282.jpg)

ios上的网络代理一直是被诟病的话题之一。

1. 手机网络不能使用代理
1. 默认的wifi下代理只能支持http

> “Surge 会接管全局的（几乎）所有通信，所以所有网络方面的电量消耗都会被算在 Surge 头上，实际上 Surge 的运行功耗很少，使用中也不会感到 Surge 对电量有明显影响。”

 **Surge** 是一个ios网络包抓取分析工具，它是基于ios9中Network Extension和VPN的新特性而来。

Surge是一个基于规则(Rule)的可配置型工具，我们可以利用Surge在ios网络层中添加代理，这样可以将ios设备的很多网络数据进行截获。从而实现对网络数据的分析和采集。它的基于规则的数据截获和转发能力，给我们提供了非常好的网络代理功能。

---

 **Q2： ShadowSocks服务 是什么？** 

ShadowSocks是一种基于Socks5代理方式的网络数据加密传输包。可以保护上网流量。基于多种加密方式，推荐使用 aes-256-cfb 加密。安装和使用需要本地端和服务端。本地客户端已经包含了多种版本，包括iOS，Android，Windows，MAC。本工具用于也被广泛用于突破防火长城，浏览被屏蔽、封锁和干扰的内容。

 **《目前热门科学上网方式介绍及优缺点简评》** 

 **https://cokebar.info/archives/236** 

 **Shadowsocks原理** 

简单理解的话，Shadowsocks是将以前通过SSH创建的Socks5协议拆开成Server端和client端，下面这个原理图能简单介绍其翻墙原理，基本上和利用SSH tunnel大致类似：

![](https://static.notion-static.com/ec009d2c73f84224ae1d88f6dfe0aa2c/57cd0fd4569a5.jpg)

PC客户端（即你的电脑）发出请求基于Socks5协议跟SS-Local端进行通讯，由于这个SS-Local一般是本机或路由器等局域网的其他机器，不经过GFW，所以解决GFW通过特征分析进行干扰的问题。

SS-Local和SS-Server两端通过多种可选的加密方法进行通讯，经过GFW的时候因为是常规的TCP包，没有明显特征码GFW也无法对通讯数据进行解密，因此通讯放行。

SS-Server将收到的加密数据进行解密，还原初始请求，再发送到用户需要访问的服务网站，获取响应原路再返回SS-04，返回途中依然使用了加密，使得流量是普通TCP包，并成功穿过GFW防火墙。

因此，Shadowsocks的优点在于它解决了GFW通过分析流量特征从而干扰的问题，这是它优于SSH和VPN翻墙的地方。

---

 **ShadowSocks服务的配置过程：** 

 **我的ShadowSocks服务商：https://hkjss.cn** 

 **PC端ShadowSocks客户端的设置：** 

![](https://static.notion-static.com/a600d5204f7e420c982f7e4049e84a0e/8b953c4agw1ewlz82eg1ij20jj0da40v.jpg)

![](https://static.notion-static.com/ae29c516d81a4597805cbf2338573a86/8b953c4agw1ewlz9yi9d2j20b0083ab4.jpg)

补充：

1.  [Surge+ShadowsSocks服务搭建方案](http://jingyan.baidu.com/article/29697b9102175eab20de3c06.html) 
1. Surge&ShadowSocks方案的优点：速度快；根据站点的IP情况自动分发：国内网站不采用代理，国外网站自动采用shadowsocks代理
1. 把Shadowsocks代理共享给局域网里的其他设备 [http://www.aixiaoxiao.cn/thread-155-1-1.html](http://www.aixiaoxiao.cn/thread-155-1-1.html) 【未读】

---

 **Q3:ShadowSocks在Chrome浏览器的代理设置** 

问题：在Q2的基础上。如果在Chrome访问的某个国外网址被墙了，但是pac代理规则里没有。那么这时只能在ss客户端切换到全局模式。

方法如下：

1. 点击【Chrome设置】-【系统】-【打开代理设置】

  ![](https://static.notion-static.com/a0be495177cf420ba0c127b429603ea2/.PNG)

1. 需要全局代理时选择代理服务器；不需要时取消。

如果不反复手动切换会影响到无需代理的国内网站访问。为了避免这种情况发生，我们可以增加PAC所包含的网址内容，此外可以采用以下的解决方案。

 **解决方案：ShadowSocks配合SwitchyOmega科学上网** 

什么是SwitchOmega？

SwitchyOmega是chrome下代理管理插件，为Chrome提供独立代理。可保持全局未加入代理，而在Chrome的相关网页中实现代理。

 [**插件下载地址**](https://chrome.google.com/webstore/detail/proxy-switchyomega/padekgcemlokbadohgkifijomclgjgif) ：

关于 **SwitchyOmega** 的设置，详见https://github.com/FelisCatus/SwitchyOmega/wiki/GFWList

(该文档情景模式为GFWeb)

![](https://static.notion-static.com/387758154a0f46e2ba0b3219de029867/step4.png)

其中："GFWeb"相当于全局模式；”自动切换“相当于PAC模式

---

 **Q4:【备选方案】更多的ShadowSocks客户端与服务** 

客户端会被下架，服务器会被关闭。多准备一点。

特别注意事项

以下参考事项需要在购买时特别注意，它们直接决定了您是否能够获得优秀的Shadowsocks使用体验；也决定了您在恶劣情况下能否保护您的利益。

服务周期：正规的Shadowsocks商家都是支持月付的，如果月付不可用，至少也需要支持季付。短周期的付费方式能够有效规避商家跑路的风险；且如果体验不好，可以切换至其他商家而不必担心已付费用的问题。注：如果您发现您希望购买的Shadowsocks服务只有年付，或者有“终身”的付费计划，您应该十分警惕此类商家。

支付方式：您应该选择支持正规在线付款方式的Shadowoscks商家，如支付宝、微信付款（注：不是转账）。如果出现服务无法使用，而商家不与理睬的情况，正规的付款渠道支持发起付款争议，您可以通过支付网关正当的收回您的付款。但是如果您直接转账给商家，后期一旦出现问题，没有任何人可以保护您的利益。

服务器数量：Shadowsocks商家的服务器数量是商家硬实力的体现，也直接决定了您能够获得多好的科学上网体验。当单个服务器出现问题时，您可以直接切换至其他地区的服务器解决问题；多地区的服务器部署保证了服务可用性，也能测试不同地区的科学上网速度。正常情况下，发展良好的Shadowsocks商家会提供20台以上服务器供用户使用。

iOS客户端：

系统客户端的查询网址：

Shadowsocket/wingy/surge

https://shadowsocks.org/en/download/clients.html

服务商：套餐考虑-时长or流量-设备数量-速度

 [https://www.biuss.com/](https://www.biuss.com/) 

https://wosster.com/