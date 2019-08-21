本项目修改自[驯兽师联盟主页](https://www.tamersunion.net/) [主题](https://github.com/KTGWKenta/Clearision)，根据幻之字幕组需求做部分调整。
感谢[dimpurr](https://github.com/dimpurr/)与[KTGWKenta](https://github.com/KTGWKenta/)

安装插件: `External Media without Import` `MaxButtons` `MetaSlider` `to top` `WP Super Cache` `wp-postviews-plus`

图标插入方式: `<i class="fa fa-home" aria-hidden="true">&nbsp;</i>站点首页`

主题设置: 高级功能 勾选全部第三方组件

关闭评论邮件通知

获取评论真实IP，将如下代码插入WP根目录`wp-config.php`中
```
if(isset($_SERVER['HTTP_X_FORWARDED_FOR'])) 
{
    $list = explode(',',$_SERVER['HTTP_X_FORWARDED_FOR']);
    $_SERVER['REMOTE_ADDR'] = $list[0];
}
```

WP Super Cache: 启用缓存 新文章/新评论清除缓存

wp-postviews-plus: 将`views`修改为`次浏览`

背景图片: https://background-1256109664.cos.ap-shanghai.myqcloud.com/test{rand:1,3}.jpg

视频插入方式:
编辑html
```
<div>
<link rel="stylesheet" href="https://lib.baomitu.com/dplayer/1.25.0/DPlayer.min.css">
<div id="dplayer"></div>
<script src="https://lib.baomitu.com/dplayer/1.25.0/DPlayer.min.js"></script>
<script>
const dp = new DPlayer({
    container: document.getElementById('dplayer'),
    video: {
        url: 'https://gss3.baidu.com/6LZ0ej3k1Qd3ote6lo7D0j9wehsv/tieba-movideo/148685650_6e3c283c5d7590e51b9e96203721e487_35db7d61ce03.mp4'
    },
});
</script>
</div>
```

MetaSlider: 关闭图像裁剪 开启传送带模式 关闭悬停暂停

首页通知:
```
[metaslider id="67"]

<h2 style="display:inline-block; width: 80%;font-size: 20px;">新闻公告</h2>

<div style="display:inline-block; width: 20%; text-align: right;"><a href="https://mabors.com/newsletters/">历史新闻</a></div>

[newsletters amount="3" open="1"/]
```

概览分割方式: `<!--more-->`

正文栏目分割: `<h3>栏目</h3>`
