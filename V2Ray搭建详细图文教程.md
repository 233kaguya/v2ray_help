<div class="post-content">
<p>搭建 V2Ray 看这篇文章就够了！这是最详细的 V2Ray 搭建教程，详细的图文教程确保你可以百分百成功搭建 V2Ray 使用。</p>

<h2 id="前言">前言</h2>

<p>此 V2Ray 教程完完全全是为小白准备的，从购买 VPS 到使用 SSH 登录并使用 V2Ray 一键安装脚本配置 V2Ray</p>

<p>详细的图文教程确保你可以百分百成功搭建 V2Ray 使用，哪怕你是第一次接触这些陌生的东西。</p>

<p>由于 V2Ray 的配置对于小白来说是非常不友好的，</p>

<p>所以此 V2Ray 教程的 V2Ray 服务器端配置将会使用我本人撰写的 <a href="https://github.com/233boy/v2ray/wiki/V2Ray一键安装脚本" rel="nofollow" target="_blank">V2Ray一键安装脚本</a></p>

<p>这是一个对小白友好的 V2Ray 一键脚本，简化 V2Ray 安装和管理，你还可以快速打开 BBR 来优化 V2Ray<br />
<!-- 此教程为 Windows 用户专属，如果你是 Mac 用户请查看：[V2Ray 一键搭建和优化详细图文教程 (Mac 用户专版)](/post/17/) --></p>

<h2 id="v2ray">V2Ray</h2>

<p>官网：<a href="https://www.v2fly.org/" rel="nofollow" target="_blank">https://www.v2fly.org/</a></p>

<p><a href="https://www.v2fly.org/" rel="nofollow" target="_blank">V2Ray(Project V)</a> 相对于 Shadowsocks，V2Ray 更像全能选手，拥有更多可选择的协议 / 传输载体 (Socks、HTTP、TLS、TCP、mKCP、WebSocket )，还有强大的路由功能，不仅仅于此，它亦包含 Shadowsocks 组件，你只需要安装 V2Ray，你就可以使用所有的 V2Ray 相关的特性包括使用 Shadowsocks，由于 V2Ray 是使用 GO 语言所撰写的，天生的平台部署优势，下载即可使用，当然啦，由于 V2Ray 的配置相对来说是很繁琐的，毫无夸张的说</p>

<p>但是有了本人所写的 <a href="https://github.com/233boy/v2ray/wiki/V2Ray一键安装脚本" rel="nofollow" target="_blank">V2Ray一键安装脚本</a> 加持下，使用 V2Ray 便会显得轻松多了。</p>

<h2 id="流程">流程</h2>

<p>总结一下此文章的大致流程，此 V2Ray 教程可百分百帮助你搭建 V2Ray 使用，哪怕你是第一次接触这些陌生的东西。</p>

<ul>
<li>购买一个 VPS<br />
想要搭建 V2Ray，就必须要拥有一台 VPS。<br /></li>
<li>获取 VPS 信息<br />
我们必须要知道 VPS IP 地址，root 用户密码，SSH 端口<br /></li>
<li>安装 Xshell<br />
Xshell 是一个 SSH 客户端，要登录 VPS，当然需要 SSH 客户端<br /></li>
<li>登录 VPS<br />
使用 Xshell 配置 VPS SSH 信息，然后登录<br /></li>
<li>安装 V2Ray<br />
极速安装，全程自动<br /></li>
<li>V2Ray 安装完成<br />
此时你可以使用客户端配置 V2Ray 使用了<br /></li>
<li>V2Ray 高级玩法<br />
配置 VMess-WS-TLS ， VLESS-gRPC-TLS，动态端口等<br />
<br /></li>
</ul>

<h2 id="机场推荐">机场推荐</h2>

<p>如果你只是单纯的翻，墙需求，可以购买机场的，不用自己搭建什么的，省心省力。</p>

<p>机场推荐： <a href="https://on.affpass.com/go/jms" rel="nofollow" target="_blank">Just My Socks</a></p>

<p><a href="https://on.affpass.com/go/jms" rel="nofollow" target="_blank">Just My Socks</a> 是搬瓦工提供的 Shadowsocks &amp; V2Ray 服务，不怕跑路，非国人商家，无须担心 IP 被墙问题。</p>

<p>购买教程：
<a href="https://bwgjms.com/post/how-to-buy-justmysocks/" target="_blank">
Just My Socks 详细图文购买教程  
</a>
</p>

<h2 id="购买一个vps">购买一个VPS</h2>

<!-- 如果你已经有VPS，请：[跳过这部分](#登录vps) -->

<p>想要搭建 V2Ray， 拥有一个 VPS 是必需的。</p>

<p>我们推荐使用：<a href="https://on.affpass.com/go/bwg" rel="nofollow" target="_blank">搬瓦工（Bandwagon Host）</a> VPS 来搭建 V2Ray</p>

<p>搬瓦工是一个对中国用户极度友好的 VPS 商家，有香港，CN2 GIA 优化线路，并且支持支付宝付款，当然也是支持退款的！</p>

<p>推荐购买的搬瓦工套餐如下，提醒，按住 <code>Ctrl</code> 键点击购买链接即可在新窗口打开。</p>

<table>
<thead>
<tr>
<th align="center">线路</th>
<th align="center">CPU</th>
<th align="center">内存</th>
<th align="center">硬盘</th>
<th align="center">带宽</th>
<th align="center">流量</th>
<th align="center">价格</th>
<th align="center">链接</th>
</tr>
</thead>

<tbody>
<tr>
<td align="center">香港</td>
<td align="center">2 核</td>
<td align="center">2048 MB</td>
<td align="center">40 GB</td>
<td align="center">1 G</td>
<td align="center">500GB / 月</td>
<td align="center"><strong>$89.99 / 月</strong></td>
<td align="center"><a href="https://on.affpass.com/go/bwg/95" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">香港</td>
<td align="center">4 核</td>
<td align="center">4096 MB</td>
<td align="center">80 GB</td>
<td align="center">1 G</td>
<td align="center">1000GB / 月</td>
<td align="center">$155.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/96" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">香港</td>
<td align="center">6 核</td>
<td align="center">8192 MB</td>
<td align="center">160 GB</td>
<td align="center">1 G</td>
<td align="center">2000GB / 月</td>
<td align="center">$299.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/97" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">香港</td>
<td align="center">8 核</td>
<td align="center">16384 MB</td>
<td align="center">320 GB</td>
<td align="center">1 G</td>
<td align="center">4000GB / 月</td>
<td align="center">$589.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/98" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">香港</td>
<td align="center">10 核</td>
<td align="center">32768 MB</td>
<td align="center">640 GB</td>
<td align="center">1 G</td>
<td align="center">6000GB / 月</td>
<td align="center">$989.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/122" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">香港</td>
<td align="center">12 核</td>
<td align="center">65536 MB</td>
<td align="center">1280 GB</td>
<td align="center">1 G</td>
<td align="center">8000GB / 月</td>
<td align="center">$1889.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/124" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
</tr>

<tr>
<td align="center">CN2 GIA</td>
<td align="center">2 核</td>
<td align="center">1 GB</td>
<td align="center">20 GB</td>
<td align="center"><strong>2.5 G</strong></td>
<td align="center">1000GB / 月</td>
<td align="center"><strong>$49.99 / 季</strong></td>
<td align="center"><a href="https://on.affpass.com/go/bwg/87" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2 GIA</td>
<td align="center">3 核</td>
<td align="center">2 GB</td>
<td align="center">40 GB</td>
<td align="center"><strong>2.5 G</strong></td>
<td align="center">2000GB / 月</td>
<td align="center">$89.99 / 季</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/88" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2 GIA</td>
<td align="center">4 核</td>
<td align="center">4 GB</td>
<td align="center">80 GB</td>
<td align="center"><strong>2.5 G</strong></td>
<td align="center">3000GB / 月</td>
<td align="center">$56.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/89" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2 GIA</td>
<td align="center">6 核</td>
<td align="center">8 GB</td>
<td align="center">160 GB</td>
<td align="center"><strong>5 G</strong></td>
<td align="center">5000GB / 月</td>
<td align="center">$86.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/90" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2 GIA</td>
<td align="center">8 核</td>
<td align="center">16 GB</td>
<td align="center">320 GB</td>
<td align="center"><strong>5 G</strong></td>
<td align="center">8000GB / 月</td>
<td align="center">$159.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/91" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2 GIA</td>
<td align="center">10 核</td>
<td align="center">32 GB</td>
<td align="center">640 GB</td>
<td align="center"><strong>10 G</strong></td>
<td align="center">10000GB / 月</td>
<td align="center">$289.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/92" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2 GIA</td>
<td align="center">12 核</td>
<td align="center">64 GB</td>
<td align="center">1280 GB</td>
<td align="center"><strong>10 G</strong></td>
<td align="center">12000GB / 月</td>
<td align="center">$549.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/93" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
</tr>

<tr>
<td align="center">日本</td>
<td align="center">2 核</td>
<td align="center">2 GB</td>
<td align="center">40 GB</td>
<td align="center">1.2 G</td>
<td align="center">500GB / 月</td>
<td align="center">$89.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/108" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">日本</td>
<td align="center">4 核</td>
<td align="center">4 GB</td>
<td align="center">80 GB</td>
<td align="center">1.2 G</td>
<td align="center">1000GB / 月</td>
<td align="center">$159.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/109" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">日本</td>
<td align="center">6 核</td>
<td align="center">8 GB</td>
<td align="center">160 GB</td>
<td align="center">1.2G</td>
<td align="center">2000GB / 月</td>
<td align="center">$299.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/110" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">日本</td>
<td align="center">8 核</td>
<td align="center">16 GB</td>
<td align="center">320 GB</td>
<td align="center">1.2 G</td>
<td align="center">4000GB / 月</td>
<td align="center">$589.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/111" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">日本</td>
<td align="center">10 核</td>
<td align="center">32768 MB</td>
<td align="center">640 GB</td>
<td align="center">1.2 G</td>
<td align="center">6000GB / 月</td>
<td align="center">$989.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/123" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">日本</td>
<td align="center">12 核</td>
<td align="center">65536 MB</td>
<td align="center">1280 GB</td>
<td align="center">1.2 G</td>
<td align="center">8000GB / 月</td>
<td align="center">$1889.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/125" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
</tr>

<tr>
<td align="center">迪拜</td>
<td align="center">2 核</td>
<td align="center">1 GB</td>
<td align="center">20 GB</td>
<td align="center">1 G</td>
<td align="center">500GB / 月</td>
<td align="center">$19.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/114" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">迪拜</td>
<td align="center">3 核</td>
<td align="center">2 GB</td>
<td align="center">40 GB</td>
<td align="center">1 G</td>
<td align="center">1000GB / 月</td>
<td align="center">$32.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/115" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">迪拜</td>
<td align="center">4 核</td>
<td align="center">4 GB</td>
<td align="center">80 GB</td>
<td align="center">1 G</td>
<td align="center">2000GB / 月</td>
<td align="center">$56.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/116" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">迪拜</td>
<td align="center">6 核</td>
<td align="center">8 GB</td>
<td align="center">160 GB</td>
<td align="center">1 G</td>
<td align="center">3000GB / 月</td>
<td align="center">$86.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/117" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">迪拜</td>
<td align="center">8 核</td>
<td align="center">16 GB</td>
<td align="center">320 GB</td>
<td align="center">1 G</td>
<td align="center">4000GB / 月</td>
<td align="center">$159.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/118" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">迪拜</td>
<td align="center">10 核</td>
<td align="center">32 GB</td>
<td align="center">640 GB</td>
<td align="center">1 G</td>
<td align="center">5000GB / 月</td>
<td align="center">$289.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/119" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">迪拜</td>
<td align="center">12 核</td>
<td align="center">64 GB</td>
<td align="center">1280 GB</td>
<td align="center">1 G</td>
<td align="center">6000GB / 月</td>
<td align="center">$549.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/120" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
</tr>

<tr>
<td align="center">CN2</td>
<td align="center">1 核</td>
<td align="center">1024 MB</td>
<td align="center">20 GB</td>
<td align="center">1 G</td>
<td align="center">1000GB / 月</td>
<td align="center"><strong>$49.99 / 年</strong></td>
<td align="center"><a href="https://on.affpass.com/go/bwg/57" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2</td>
<td align="center">1 核</td>
<td align="center">2048 MB</td>
<td align="center">40 GB</td>
<td align="center">1 G</td>
<td align="center">2000GB / 月</td>
<td align="center">$52.99 / 半年</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/58" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2</td>
<td align="center">2 核</td>
<td align="center">4096 MB</td>
<td align="center">80 GB</td>
<td align="center">1 G</td>
<td align="center">3000GB / 月</td>
<td align="center">$59.99 / 季</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/59" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2</td>
<td align="center">2 核</td>
<td align="center">8 GB</td>
<td align="center">160 GB</td>
<td align="center">1 G</td>
<td align="center">5000GB / 月</td>
<td align="center">$39.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/67" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2</td>
<td align="center">3 核</td>
<td align="center">16 GB</td>
<td align="center">320 GB</td>
<td align="center">1 G</td>
<td align="center">8000GB / 月</td>
<td align="center">$79.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/68" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2</td>
<td align="center">3 核</td>
<td align="center">16 GB</td>
<td align="center">320 GB</td>
<td align="center">1 G</td>
<td align="center">12000GB / 月</td>
<td align="center">$99.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/106" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2</td>
<td align="center">3 核</td>
<td align="center">16 GB</td>
<td align="center">320 GB</td>
<td align="center">1 G</td>
<td align="center">16000GB / 月</td>
<td align="center">$129.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/107" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
<td align="center">-</td>
</tr>

<tr>
<td align="center">普通</td>
<td align="center">2 核</td>
<td align="center">1024 MB</td>
<td align="center">20 GB</td>
<td align="center">1 G</td>
<td align="center">1 TB / 月</td>
<td align="center"><strong>$49.99 / 年</strong></td>
<td align="center"><a href="https://on.affpass.com/go/bwg/44" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">普通</td>
<td align="center">3 核</td>
<td align="center">2 GB</td>
<td align="center">40 GB</td>
<td align="center">1 G</td>
<td align="center">2 TB / 月</td>
<td align="center">$52.99 / 半年</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/45" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">普通</td>
<td align="center">4 核</td>
<td align="center">4 GB</td>
<td align="center">80 GB</td>
<td align="center">1 G</td>
<td align="center">3 TB / 月</td>
<td align="center">$19.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/46" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">普通</td>
<td align="center">5 核</td>
<td align="center">8 GB</td>
<td align="center">160 GB</td>
<td align="center">1 G</td>
<td align="center">4 TB / 月</td>
<td align="center">$39.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/47" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">普通</td>
<td align="center">6 核</td>
<td align="center">16 GB</td>
<td align="center">320 GB</td>
<td align="center">1 G</td>
<td align="center">5 TB / 月</td>
<td align="center">$79.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/48" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">普通</td>
<td align="center">7 核</td>
<td align="center">24 GB</td>
<td align="center">480 GB</td>
<td align="center">1 G</td>
<td align="center">6 TB / 月</td>
<td align="center">$119.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/49" rel="nofollow" target="_blank">购买</a></td>
</tr>
</tbody>
</table>

<p>选择哪个套餐？如果你不知道选择哪个套餐<br />
下面这是最常见的购买套餐</p>

<table>
<thead>
<tr>
<th align="center">线路</th>
<th align="center">CPU</th>
<th align="center">内存</th>
<th align="center">硬盘</th>
<th align="center">带宽</th>
<th align="center">流量</th>
<th align="center">价格</th>
<th align="center">链接</th>
</tr>
</thead>

<tbody>
<tr>
<td align="center">普通</td>
<td align="center">2 核</td>
<td align="center">1024 MB</td>
<td align="center">20 GB</td>
<td align="center">1 G</td>
<td align="center">1 TB / 月</td>
<td align="center"><strong>$49.99 / 年</strong></td>
<td align="center"><a href="https://on.affpass.com/go/bwg/44" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2</td>
<td align="center">1 核</td>
<td align="center">1024 MB</td>
<td align="center">20 GB</td>
<td align="center">1 G</td>
<td align="center">1000GB / 月</td>
<td align="center"><strong>$49.99 / 年</strong></td>
<td align="center"><a href="https://on.affpass.com/go/bwg/57" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">CN2 GIA</td>
<td align="center">2 核</td>
<td align="center">1 GB</td>
<td align="center">20 GB</td>
<td align="center"><strong>2.5 G</strong></td>
<td align="center">1000GB / 月</td>
<td align="center"><strong>$49.99 / 季</strong></td>
<td align="center"><a href="https://on.affpass.com/go/bwg/87" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">迪拜</td>
<td align="center">2 核</td>
<td align="center">1 GB</td>
<td align="center">20 GB</td>
<td align="center">1 G</td>
<td align="center">500GB / 月</td>
<td align="center">$19.99 / 月</td>
<td align="center"><a href="https://on.affpass.com/go/bwg/114" rel="nofollow" target="_blank">购买</a></td>
</tr>

<tr>
<td align="center">香港</td>
<td align="center">2 核</td>
<td align="center">2048 MB</td>
<td align="center">40 GB</td>
<td align="center">1 G</td>
<td align="center">500GB / 月</td>
<td align="center"><strong>$89.99 / 月</strong></td>
<td align="center"><a href="https://on.affpass.com/go/bwg/95" rel="nofollow" target="_blank">购买</a></td>
</tr>
</tbody>
</table>


<p>没有找到合适的套餐？你可以前往官网详细查看：<a href="https://on.affpass.com/go/bwg" rel="nofollow" target="_blank">https://bwh89.net/cart.php</a></p>

<p>哪个套餐好？<br />
一般来说，<strong>推荐购买 香港线路</strong> 或 <strong>CN2 GIA 线路</strong>，或者哪个便宜选择那个，说着当然如果你使用量比较多或者想要分享给同学和朋友一起用的话，选择合适的套餐即可。又或者你土豪的话，选择最贵的也行。</p>

<p><strong>VPS 速度：香港线路 &gt; 日本线路 &gt; CN2 GIA 线路 &gt; CN2 线路 &gt; 普通线路</strong></p>

<p><strong>香港套餐 VPS 的速度最快。</strong> 如果你非常在乎速度的话，建议购买香港线路的 VPS，当然，但价格贵，流量相对其他套餐来说也是比较少的……退一步的选择是 <code>CN2 GIA</code> 线路，这个线路的速度也比较好。</p>

<p>线路是比较重要的，像香港和 CN2 GIA 线路到晚上一般不会怎么炸，普通线路的到了晚上可能会出现很慢慢的感觉。</p>

<p>我本人比较推荐 <code>CN2 GIA</code> 线路，稳定性，速度与价格适中选择。</p>

<p>当然啦！如果你觉得价格太贵了，推荐你查看一下 


<a href="https://justmysocks.xyz/justmysocks-v2ray/" target="_blank">
Just My Socks  
</a>
，搬瓦工官方出品的代理服务，优质的 CN2 GIA 线路，<strong>每月仅需 $2.88 起！</strong>再也不用自己折腾搭建了，<strong>最最最最重要的是：被墙自动换 IP，无须担心 IP 被墙！</strong></p>

<p>Just My Socks 购买教程在这里：


<a href="https://justmysocks.xyz/justmysocks-v2ray/" target="_blank">
Just My Socks 购买及使用  
</a>
</p>

<p>毫无疑问！绝对的一分钱一分货。</p>

<blockquote>
<p>如果出现 out of stock 这样的提示，那就是这个套餐卖完了，选择其他套餐即可。</p>
</blockquote>

<h2 id="添加到购物车">添加到购物车</h2>

<p>在上面表格中选择想要购买的套餐，然后点击 <code>购买</code> 即可。</p>

<p>将 VPS 添加到购物车</p>



<img src="https://i.loli.net/2018/11/18/5bf1684742682.png" alt=""  loading="lazy" referrerPolicy="no-referrer">


<p>说明一下，在Billing Cycle选项那里选择：<code>$xxxx USD Annually</code>，按年付的意思</p>

<p><strong>推荐按年付，比按月付最高可省55%的钱</strong></p>

<p>如果你选择购买 <code>CN2 GIA</code> 的线路</p>

<p>在添加到购物车的时候，<code>Location</code> 的选项，可以选择 <code>JP - Equinix Osaka Softbank (JPOS_1)</code></p>

<p>这样来就是使用日本软银线路</p>

<p>然后点击<code>Add To Cart</code></p>

<h2 id="结算">结算</h2>

<p>推荐使用搬瓦工优惠码：
<a href="https://on.affpass.com/go/bwg" rel="nofollow" target="_blank">BWHNCXNVXV</a>
</p>

<p>这个优惠码是搬瓦工目前最高优惠的优惠码<br />
输入优惠码之后点击 <code>Validate Code &gt;&gt;</code></p>



<img src="https://i.loli.net/2018/11/18/5bf168474423c.png" alt="输入优惠码"  loading="lazy" referrerPolicy="no-referrer">


<p>然后点击 <code>Checkout</code><br />
如下图所示：已经使用搬瓦工优惠码</p>



<img src="https://i.loli.net/2018/11/18/5bf1684703cec.png" alt="Checkout"  loading="lazy" referrerPolicy="no-referrer">


<p>然后会提示你注册账号 （如果你没账号或者还没登录）<br />
请按照下面图片提示来填写~</p>



<img src="https://i.loli.net/2018/11/18/5bf16da6832c6.png" alt="Checkout now"  loading="lazy" referrerPolicy="no-referrer">


<p>要注意的是，Country 选项记得选择 <code>China</code>，Payment Method 选择 <code>Alipay</code><br />
不要忘了勾上 I have read and agree to the Terms of Service<br />
然后 <code>Complete Order</code></p>




<h2 id="付款">付款</h2>

<p>点击 <code>Pay now</code></p>

<p>之后便会跳转到支付宝付款界面，完成付款即可</p>



<img src="https://i.loli.net/2018/11/18/5bf1684732175.png" alt="Pay now"  loading="lazy" referrerPolicy="no-referrer">


<h2 id="获取vps信息">获取VPS信息</h2>

<p>确保你已经成功付款之后</p>

<p>打开：<a href="https://bwh89.net/services" rel="nofollow" target="_blank">https://bwh89.net/services</a></p>

<p>在 Manage 那选择 <code>Open KiwiVM</code></p>

<p>如果出现以下界面，稍等一会，等待资源分配即可。</p>



<img src="https://i.loli.net/2017/09/05/59ae8a8fc83e2.jpg" alt="Task in progress"  loading="lazy" referrerPolicy="no-referrer">


<p>等待两三分钟，刷新一下。<br />
这是已经在运行的界面，请记下 <code>IP address</code>然后点击 <code>stop</code></p>



<img src="https://i.loli.net/2018/11/18/5bf1684733cec.png" alt="停止VPS"  loading="lazy" referrerPolicy="no-referrer">


<p>当出现：Great Success! Virtual server will stop in a few seconds. 相关提示</p>

<p>证明 VPS 已经停止了，我们需要重装一个系统。点击左边的 <code>Install new OS</code></p>

<p>之后选择 <code>ubuntu-22.04-x86_64</code></p>

<p>再勾上：<code>I agree that all existing data on my VPS will be lost.</code></p>

<p>然后点击 <code>Reload</code></p>



<img src="https://vip2.loli.io/2023/05/13/DdpoZBJgR1jvtnF.png" alt="Install new OS"  loading="lazy" referrerPolicy="no-referrer">


<!-- 安装此系统之后便会自动启用 BBR 优化加速。 -->

<p>当点击 <code>Reload</code> 之后，稍等片刻将会出现下图所示的界面，</p>

<p>请务必记下： <code>You will need a new root password to access your VPS：xxxx</code></p>

<p>还有：<code>New SSH Port:</code></p>

<p>一个是 root密码，一个是 SSH端口</p>



<img src="https://i.loli.net/2018/11/18/5bf168473b33d.png" alt="Reload"  loading="lazy" referrerPolicy="no-referrer">


<p>OK，这时我们已经获取到VPS的信息了。</p>

<h2 id="安装-xshell">安装 Xshell</h2>

<p>Xshell 是一个易用的 SSH 客户端，要登录 VPS，当然需要 SSH 客户端</p>

<p><a href="https://file.affpass.com/file/Xshell+Xftp.zip" rel="nofollow" target="_blank">Xshell 下载链接点我</a></p>

<p>这是一个绿色版本的 Xshell ，打开链接后，就点击 <code>下载</code>，下载好了之后，就双击打开，然后点击 <code>浏览...</code> 可以选择解压的路径，比如说 D 盘，之后再选择 <code>解压</code> 即可。</p>



<img src="https://i.loli.net/2018/12/27/5c24f0c995b84.jpg" alt="解压 Xshell"  loading="lazy" referrerPolicy="no-referrer">


<p>然后在解压的目录找到 <code>Xshell+Xftp</code> 文件夹，打开它，之后找到 <code>!安装.bat</code> 并且右键选择 <code>以管理员身份运行</code>，安装完成后会有一个提示窗口，关闭即可。这样来就安装好了 Xshell</p>



<img src="https://i.loli.net/2018/12/27/5c24f0c9994a4.jpg" alt="安装 Xshell"  loading="lazy" referrerPolicy="no-referrer">


<h2 id="登录vps">登录VPS</h2>

<p>在桌面找到 Xshell ，打开它，新建一个会话。</p>



<img src="https://i.loli.net/2018/12/27/5c24f0c8d78f6.jpg" alt="新建会话"  loading="lazy" referrerPolicy="no-referrer">


<p>主机写上你的 VPS IP 地址，端口写上 SSH 端口。</p>



<img src="https://i.loli.net/2018/11/18/5bf1684735776.png" alt="new"  loading="lazy" referrerPolicy="no-referrer">


<p>之后点击 用户身份验证，用户名：<code>root</code>，密码：你的 root 密码。然后点击确定</p>



<img src="https://i.loli.net/2018/11/18/5bf1684737f3c.png" alt="user-and-passwd"  loading="lazy" referrerPolicy="no-referrer">


<p>之后选择连接。</p>



<img src="https://i.loli.net/2018/11/18/5bf1684739aab.png" alt="连接"  loading="lazy" referrerPolicy="no-referrer">


<p>然后会提示SSH安全警告，选择，接受并保存。</p>



<img src="https://i.loli.net/2018/11/18/5bf15f4b04c72.png" alt="SSH 安全警告"  loading="lazy" referrerPolicy="no-referrer">


<p>这是登录成功后的界面</p>



<img src="https://i.loli.net/2018/11/18/5bf15f4b0cd33.png" alt="登陆成功"  loading="lazy" referrerPolicy="no-referrer">


<h2 id="安装-v2ray">安装 V2Ray</h2>

<p>输入下面命令回车，你可以复制过去，然后在 Xshell 界面按 Shift + Insert 即可粘贴，不能按 Ctrl + V 的。。</p>
<div class="highlight"><pre style="color:#f8f8f2;background-color:#272822;-moz-tab-size:4;-o-tab-size:4;tab-size:4"><code class="language-bash" data-lang="bash">bash &lt;<span style="color:#f92672">(</span>wget -qO- -o- https://git.io/v2ray.sh<span style="color:#f92672">)</span></code></pre></div>
<h2 id="安装完成">安装完成</h2>

<p>当你执行了上面的安装命令，并且没有错误提示的话，那么你就能看到类似下面的图片</p>



<img src="https://vip2.loli.io/2023/05/11/WE8qUsZDgvxTVad.png" alt="V2Ray 脚本安装完成"  loading="lazy" referrerPolicy="no-referrer">


<p>脚本特意弄了一个时间显示，给反馈用来检测安装时间的&hellip;</p>

<p>理论上，绝大多数情况下 15秒内会安装完成</p>

<p>为方便你快速使用，脚本在安装完成后会自动创建一个 VMess-TCP 配置。</p>

<p>此时你可以复制 URL 到相关软件 (例如 v2rayN) 去测试一下是否正常使用。</p>

<p>如果无法正常使用，请尝试使用 <code>v2ray add ss</code> 添加一个 SS 来再测试一下</p>

<h2 id="v2ray-管理面板">V2Ray 管理面板</h2>

<p>现在可以尝试一下输入 <code>v2ray</code> 回车，即可管理 V2Ray</p>



<img src="https://vip2.loli.io/2023/05/11/irKCJBOREU2xdyZ.png" alt="V2Ray 脚本管理面板"  loading="lazy" referrerPolicy="no-referrer">


<p>提示，如果你不想执行任何功能，直接按 Enter 回车退出即可。</p>

<h2 id="无法使用">无法使用</h2>

<p>无法使用一般都是两种情况，一是无法连接上端口，二是客户端内核支持有问题。</p>

<p>如果你的 VPS 有外部防火墙，请确保你已经开放了端口</p>

<p>测试端口是否能连接上：</p>

<p>打开：<a href="https://ping.sx/check-port" rel="nofollow" target="_blank">https://ping.sx/check-port</a></p>

<p>Target 写你的 VPS IP，Port 写 V2Ray 的端口，然后点击 <code>Check</code>，如果 REACHABILITY 显示 <code>Timeout</code>，那是无法连接上端口</p>

<p>提醒，你可以使用 <code>v2ray ip</code> 查看 VPS IP。</p>

<p>关闭防火墙，执行如下命令：</p>

<p><code>systemctl stop firewalld; systemctl disable firewalld; ufw disable</code></p>

<p>关闭防火墙之后再测试一下端口是否通，如果不通，你可能还有外部防火墙没关，必须要能连接上端口才能正常使用。</p>

<p>如果 REACHABILITY 显示 <code>Reachable</code> 那就是能连接上端口，那就继续</p>

<p>使用 <code>v2ray add ss</code> 添加一个 SS 看看能不能正常使用，如果正常使用，证明运行没有问题。</p>

<p>提醒，默认安装的 V2Ray 内核为最新版本</p>

<p>如果无法使用，可能是你客户端的内核太旧</p>

<p>请尝试使用不同的客户端进行测试；比如 v2rayN；v2rayNG 等</p>

<p>请尝试设置 VMessAEAD，某些客户端会有相关选项</p>

<p>某些客户端得把 额外id(alterid) 填写为 0；比如垃圾苹果那边的东西</p>

<p>解决方案一，请尝试将服务器端的内核版本降级</p>

<p>使用 <code>v2ray update core 4.45.2</code> 降级即可</p>

<p>解决方案二，升级客户端内核</p>

<blockquote>
<p>备注，请尽量将客户端内核和服务器端内核保持一致！<strong>内核版本低于 5 可能会出现莫名其妙的问题</strong></p>
</blockquote>

<h2 id="快速入门">快速入门</h2>

<p>本人的 V2Ray 脚本简化了很多流程，例如我们常用的是 (添加、更改、查看、删除) 配置，以下内容让你可以快速掌握使用</p>

<p>添加配置：</p>

<ul>
<li><p><code>v2ray add</code> -&gt; 添加配置</p></li>

<li><p><code>v2ray add ss</code> -&gt; 添加一个 Shadowsocks 配置</p></li>

<li><p><code>v2ray add tcp</code> -&gt; 添加一个 VMess-TCP 配置</p></li>

<li><p><code>v2ray add kcpd</code> -&gt; 添加一个 VMess-mKCP-dynamic-port 动态端口配置</p></li>
</ul>

<p>备注，使用 <code>v2ray add</code> 添加配置的时候，仅 *TLS 相关协议配置必须提供域名，其他均可自动化处理。</p>

<p>如需查看更多 add 参数用法，请查看 V2Ray 脚本说明</p>

<p>&ndash;</p>

<p>更改配置：</p>

<ul>
<li><p><code>v2ray change</code> -&gt; 更改配置</p></li>

<li><p><code>v2ray change tcp</code> -&gt; 更改 TCP 相关配置</p></li>

<li><p><code>v2ray change tcp port auto</code> -&gt; 更改 TCP 相关配置的端口，端口使用自动创建，也可以使用 <code>v2ray port tcp auto</code></p></li>

<li><p><code>v2ray change kcp id auto</code> -&gt; 更改 mKCP 相关配置的 UUID，UUID 使用自动创建，也可以使用 <code>v2ray id tcp auto</code></p></li>
</ul>

<p>如需查看更多 change 参数用法，请查看 V2Ray 脚本说明</p>

<p>&ndash;</p>

<p>查看配置：</p>

<ul>
<li><p><code>v2ray info</code> -&gt; 查看配置</p></li>

<li><p><code>v2ray info tcp</code> -&gt; 查看 TCP 相关配置</p></li>

<li><p><code>v2ray info kcp</code> -&gt; 查看 kcp 相关配置</p></li>
</ul>

<p>&ndash;</p>

<p>删除配置：</p>

<ul>
<li><p><code>v2ray del</code> -&gt; 删除配置</p></li>

<li><p><code>v2ray del kcp</code> -&gt; 删除 KCP 相关配置</p></li>

<li><p><code>v2ray del tcp</code> -&gt; 删除 TCP 相关配置</p></li>
</ul>

<p><strong>提醒，谨慎使用 del 参数</strong></p>

<p>&ndash;</p>

<p>非常棒！你已经掌握最常用的功能 (添加、更改、查看、删除)</p>

<p>add / change / info / del ： 添加、更改、查看、删除</p>

<p>对于绝大多数用户来说</p>

<p>使用 <code>v2ray add</code> 添加配置，使用 <code>v2ray change</code> <code>v2ray info</code> <code>v2ray del</code> 来 (更改、查看、删除) 配置即可。</p>

<blockquote>
<p>提醒，如果只匹配到一个配置时则自动选择该配置，否则将显示匹配到的配置列表，要求选择其中一个配置</p>
</blockquote>

<h2 id="打开-bbr-优化">打开 BBR 优化</h2>

<p>使用：<code>v2ray bbr</code> 便会自动打开 BBR 优化了！非常简单方便</p>

<h2 id="mkcp">mKCP</h2>

<p>mKCP 这个东西其实就是 KCP 协议，反正你知道是能提速的就行，但是不保证都能提速，还能避免 TCP 阻断</p>

<p>使用方法：服务器输入 <code>v2ray add kcp</code> 回车，即可</p>

<p>备注：由于 UDP 的原因也许会被运营商 Qos，这是无解的。</p>

<p>还有就是使用 mKCP 会花费更多流量，请注意！</p>

<h2 id="动态端口">动态端口</h2>

<p>听说使用动态端口可能会对 ISP 封锁端口有点帮助作用。。</p>

<p>使用方法：服务器输入 <code>v2ray add kcpd</code> 回车，即可</p>

<p>也可以使用 <code>v2ray add tcpd</code></p>

<h2 id="vmess-ws-tls">VMess-WS-TLS</h2>

<p>实现 VMess-WS-TLS 超级无敌简单，前提是要拥有一个能正常解析的域名 (并且知道怎么解析域名)</p>

<p>服务器输入 <code>v2ray add ws</code> 回车，输入域名，搞定。</p>

<h2 id="vless-h2-tls">VLESS-H2-TLS</h2>

<p>实现 VLESS-H2-TLS 超级无敌简单，前提是要拥有一个能正常解析的域名 (并且知道怎么解析域名)</p>

<p>服务器输入 <code>v2ray add vh2</code> 回车，输入域名，搞定。</p>

<p>备注，VLESS-H2-TLS 相比 VMess-WS-TLS，在浏览网页时有一些优势，速度是差不多的啦</p>

<h2 id="trojan-grpc-tls">Trojan-gRPC-TLS</h2>

<p>实现 Trojan-gRPC-TLS 超级无敌简单，前提是要拥有一个能正常解析的域名 (并且知道怎么解析域名)</p>

<p>服务器输入 <code>v2ray add tgrpc</code> 回车，输入域名，搞定。</p>

<p>和其他 *TLS 配置的速度差异？有人说快，有人说慢，你自己对比吧</p>

<h2 id="哪个传输协议好">哪个传输协议好？</h2>

<p>心中无杂念，用 TCP</p>

<p>ISP 常作怪，用 动态端口</p>

<p>VPS速度不好，用 mKCP</p>

<p>处子之身，用 *TLS</p>

<h2 id="v2ray-脚本说明">V2Ray 脚本说明</h2>

<p>请看：<a href="https://github.com/233boy/v2ray/wiki/V2Ray一键安装脚本" rel="nofollow" target="_blank">V2Ray一键安装脚本</a></p>

<p>哎呀，虽然脚本很好用，但是为了你能更加了解掌握各种使用技巧，还是建议看一虾吧！</p>

<h2 id="v2ray-脚本帮助">V2Ray 脚本帮助</h2>

<p>使用：<code>v2ray help</code></p>

<h2 id="反馈问题">反馈问题</h2>

<p>Telegram 群组：<a href="https://t.me/tg233boy" rel="nofollow" target="_blank">https://t.me/tg233boy</a></p>

<p>Github 反馈：<a href="https://github.com/233boy/v2ray/issues" rel="nofollow" target="_blank">https://github.com/233boy/v2ray/issues</a></p>

<h2 id="分享">分享</h2>

<p>如果这篇文章对你帮助的话，记得分享给你的小伙伴们哦！</p>

<h2 id="其他">其他</h2>

<p>请勿违反国家法律法规，否则后果自负！</p>

<p>低调低调低调。</p>

<h2 id="结束">结束</h2>

<p>我有写少了什么吗？我这种小小白萌新看了这教程都觉得很明白了啊。</p>

<p>一次不会，那么就两次，还是不会，那就再来一次。可还是不会啊？大佬请收下我的膝盖。</p>
</div>