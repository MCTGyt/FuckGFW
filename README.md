# FuckGFW
解决垃圾gfw

# 使用教学
域名301或302跳转到你的服务器
![](https://i.imgur.com/nfMV6FT.png)

# 如何修改
···
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>本站已被墙</title>
</head>
<body>
    <center>
        <h3>正如你所见，主站已被墙</h3>
        <p>请使用某些手段后点击以下按钮</p>
        <?php
/*
 * Created on 2016-9-4
 *
 */
 function httpcode($url){
  $ch = curl_init();
  $timeout = 3;
  curl_setopt($ch,CURLOPT_FOLLOWLOCATION,1);
  curl_setopt($ch,CURLOPT_RETURNTRANSFER,1);
  curl_setopt($ch, CURLOPT_HEADER, 1);
  curl_setopt ($ch, CURLOPT_CONNECTTIMEOUT, $timeout);
  curl_setopt($ch,CURLOPT_URL,$url);
  curl_exec($ch);
  return $httpcode = curl_getinfo($ch,CURLINFO_HTTP_CODE);
  curl_close($ch);

}
?>
        <?php
if (httpcode('http://mctg.orgs.hk') == "200") /*换成你的域名*/
    {
        echo "<a href='https://mctg.orgs.hk'>/*换成你的域名*/<img src='http://us-host.nets.hk/i/2022/03/01/ia2aii.png'></a>";/*换成你图床地址，或者继续用我的*/
    }
    else
    {
    echo "垃圾主机又特么死了，<a href='https://web.archive.org/web/*/mctg.orgs.hk'>点我前往网页时光机</a>";/*把mctg.orgs.hk换成你的域名，前提是在网页时光机里备份了*/
    }
?>
        <p>或使用备用博客(没墙但不推荐)</p>
        <?php
if (httpcode('http://mctgnb.nets.hk') == "200") /*换成你的域名*/
    {
        echo "<a href='https://mctgnb.nets.hk'>/*换成你的域名*/<img src='http://us-host.nets.hk/i/2022/03/01/ia2aii.png'></a>"; /*换成你图床地址，或者继续用我的*/
    }
    else
    {
    echo "垃圾主机又特么死了，<a href='https://web.archive.org/web/*/mctgnb.nets.hk'>点我前往网页时光机</a>"; /*把mctg.orgs.hk换成你的域名，前提是在网页时光机里备份了*/
    }
?>
<p class="small">本站由 <a href="https://idc.yiluntanbbs.cn/" target="_blank"> 令闻云端提供网站托管及cdn防护加速服务 </a>/*这行可以选择删除或者不删也行*/
    </center>
    <script>
        var Browser_Agent = navigator.userAgent;
    // 浏览器为ie的情况 
    if (Browser_Agent.indexOf( " MSIE " ) !=- 1 ){
        var a = navigator.browserLanguage;
        if (a != " zh-cn " ){
            // 跳转到英文网站
            location.href = "https://mctg.orgs.hk" ; /*换成你的域名*/
        }
    }
    // 浏览器非ie的情况 
    else {
        var b = navigator.language;
        if (b != " zh-CN " ){
            // 跳转到英文网站
            location.href = "https://mctg.orgs.hk" ; /*换成你的域名*/
        }
    }
    </script>
</html>
···
