### <font color=Purple size=5>遥祝各位老板：生意兴隆通四海，财源茂盛达三江</font>

### <font color="red">请使用官方交流群解答疑问：👉︎👉︎👉︎ [点击进入交流群](https://ext.dcloud.net.cn/publisher/start-session?pluginId=23449) 👈︎👈︎👈︎




# <font color="red">TikTok 授权登录与分享 插件使用教程(注：需要使用vpn)

[tiktok开发者网站](https://developers.tiktok.com/)


1、引入插件

```	
    var TikTok = uni.requireNativePlugin('TiktokUniPlugin');
```

2、初始化tiktoksdk 需要使用申请的clientkey

```	
	var res = TikTok.initWithAppid("sbawije4xvw4c01u7o");
	console.log("-----res", res)
```

3、是否安装tiktok app

```	
	var result = TikTok.tiktokAppInstalled();
    console.log("-----是否安装", result)
```

4、tiktok授权登录

```	
    TikTok.tiktokAuth({"scope":"user.info.basic","state":""},
        (ret, ret1) => {
			console.log(ret, ret1)
            //ret.errorCode  //OK = 0 授权成功， ERROR_UNKNOW = -1 未知错误， ERROR_CANCEL = -2 用户手动取消
            //ret.authCode   //临时票据code，用来换取access_token
	})
```

5、分享图片

```	
    //uniapp 图片选择方法
    uni.chooseImage({
		count: 7,
		success: (res) => {
				// 调用插件方法
				TikTok.tiktokShareImages(res,
					(ret, ret1) => {
							console.log(ret,ret1)
                            
                            //TikTokOpenSDKSuccess = 0,
                            //TikTokOpenSDKErrorCodeCommon = -1,
                            //TikTokOpenSDKErrorCodeUserCanceled = -2,
                            //TikTokOpenSDKErrorCodeSendFailed = -3,
                            //TikTokOpenSDKErrorCodeAuthDenied = -4,
                            //TikTokOpenSDKErrorCodeUnsupported = -5,

						})
					}
		})

```


6、分享视频

```	
    //uniapp 视频选择方法
   	uni.chooseVideo({
		sourceType: ['album'],
		success: function(res) {
            //插件方法
            TikTok.tiktokShareVideo(res,
                (ret,ret1) => {
                    console.log(ret,ret1)
                      
                      //TikTokOpenSDKSuccess = 0,
                      //TikTokOpenSDKErrorCodeCommon = -1,
                      //TikTokOpenSDKErrorCodeUserCanceled = -2,
                      //TikTokOpenSDKErrorCodeSendFailed = -3,
                      //TikTokOpenSDKErrorCodeAuthDenied = -4,
                      //TikTokOpenSDKErrorCodeUnsupported = -5,
                })
        }
	});

```

7、配置urlscheme  在manifest.json 配置 iOS UrlScheme 为 clientkey

```	
   /* ios打包配置 */
    "ios" : {
        "urltypes" : "sbawije4xvw4c01u7o"
    }
```

<font color=red size=5>

### 主营业务：

 1、软件开发、App、小程序、管理后台；
 
 2、App代上架、马甲包制作、华为、苹果、小米市场上架等；
 
 3、小程序、app备案、软著申请服务等；
 
 4、网赚项目源码出售、接入流量主广告；
 
 5、代写毕业设计和论文审查；

<img src="https://codesuccess.online/h5/rjkflogo2.jpg" width="500px" />

</font>


## 项目推荐：(点击前往)

<a href="https://ext.dcloud.net.cn/plugin?id=22889"><img src="https://codesuccess.online/h5/app/image/22889.png" width="150px"  style="margin:10px"></a>
<a href="https://ext.dcloud.net.cn/plugin?id=22987"><img src="https://codesuccess.online/h5/app/image/22987.png" width="150px"  style="margin:10px"></a>
<a href="https://ext.dcloud.net.cn/plugin?id=19789"><img src="https://codesuccess.online/h5/app/image/19789.png" width="150px"  style="margin:10px"></a>
<a href="https://ext.dcloud.net.cn/plugin?id=19852"><img src="https://codesuccess.online/h5/app/image/19852.png" width="150px"  style="margin:10px"></a>
<a href="https://ext.dcloud.net.cn/plugin?id=23356"><img src="https://codesuccess.online/h5/app/image/23356.png" width="150px"  style="margin:10px"></a>
<a href="https://ext.dcloud.net.cn/plugin?id=23369"><img src="https://codesuccess.online/h5/app/image/23369.jpg" width="150px"  style="margin:10px"></a>
<a href="https://ext.dcloud.net.cn/plugin?id=23394"><img src="https://codesuccess.online/h5/app/image/23394.png" width="150px"  style="margin:10px"></a>
<a href="https://ext.dcloud.net.cn/plugin?id=23395"><img src="https://codesuccess.online/h5/app/image/23395.png" width="150px"  style="margin:10px"></a>
<a href="https://ext.dcloud.net.cn/plugin?id=23406"><img src="https://codesuccess.online/h5/app/image/23406.png" width="150px"  style="margin:10px"></a>
<a href="https://ext.dcloud.net.cn/plugin?id=23416"><img src="https://codesuccess.online/h5/app/image/23416.jpg" width="150px"  style="margin:10px"></a>
<a href="https://ext.dcloud.net.cn/plugin?id=23426"><img src="https://codesuccess.online/h5/app/image/23426.png" width="150px"  style="margin:10px"></a>
<a href="https://ext.dcloud.net.cn/plugin?id=23449"><img src="https://codesuccess.online/h5/app/image/23449.png" width="150px"  style="margin:10px"></a>
