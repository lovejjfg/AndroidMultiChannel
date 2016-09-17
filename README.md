# AndroidMultiChannel

anroid多渠道打包工具，使用了apktool.jar 和 dom4j.jar !通过反编译获取`AndroidManifest.xml`的内容并做相关的修改！
然后重新打包签名！
# 准备工作
1、配置好jdk1.8的环境变量；
2、配置好Zipalign的环境变量；sdk/build-tools里面每个版本都是有这个东西的，加到环境变量中就好了！！！

# 使用姿势：
1、在`signer.properties`配置相关签名路径密码等信息.

    KEY_STORE_FILE_PATH=C:/Users/Administrator/.android/debug.keystore
    KEY_STORE_ALIAS=androiddebugkey
    KEY_STORE_PASSWORD=android

2、在`data.xml`中配置相关的渠道包信息

        <!-- 渠道配置 -->
        <channel name="UMENG_CHANNEL"><!-- name属性值为AndroidManifest.xml meta-data的渠道key名称 -->
            <!-- mark是渠道标记, name是渠道名称 -->
            <item mark="360" name="360"/>
            <item mark="myApp" name="应用宝"/>
            <item mark="baidu" name="百度"/>
        </channel>

3、运行jar文件夹中的`ChanelTool.jar`



