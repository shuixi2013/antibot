# 启用Anti-Bot日志服务 {#concept_obb_qxt_cgb .concept}

日志服务（Log Service）支持实时采集阿里云爬虫风险管理（Anti-Bot Service，简称Anti-Bot）已防护的网站访问日志以及防护日志，并支持对采集到的日志数据进行实时检索与分析。

您可以在爬虫风险管理控制台中基于采集到的网站日志对网站的访问和攻击行为进行即时分析研究、协助您的安全管理人员制定防护策略。

## 操作步骤 {#section_v2q_zxt_cgb .section}

1.  登录[爬虫风险管理控制台](https://yundun.console.aliyun.com/?p=antibot)。
2.  定位到**数据报表** \> **日志服务**页面，选择您的实例所在地域。

    **说明：** 如果您是第一次使用爬虫风险管理的日志服务，需要单击**授权**，并根据页面提示完成授权操作，授权爬虫风险管理产品将记录的所有日志存储到您专属的日志服务Logstore中。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/79894/155644785434260_zh-CN.png)

3.  单击网站域名下拉框，选择需要启用日志服务的网站域名，单击启用开关。

    **说明：** 网站域名下拉列表中将展示所有您已接入爬虫风险管理进行防护的网站域名。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/79894/155644785534261_zh-CN.png)


至此，您已成功为该网站域名开启日志服务。日志服务会在您的阿里云账号中自动创建一个专属日志库和专属Logstore，爬虫风险管理自动将所有启用日志服务的网站域名的日志实时导入该专属日志库（antibot-logstore）。

然后，您就可以对启用日志服务的网站域名的访问日志进行检索和分析。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/79894/155644785534262_zh-CN.png)

## 限制与说明 {#section_fzx_gzt_cgb .section}

-   专属日志库不支持写入其他数据。

    **说明：** 爬虫风险管理记录的网站日志将被存储在您的专属日志库中，该日志库不支持通过包括API、SDK在内的任何方式写入其他数据。

-   暂不支持修改专属日志库的存储周期等基本设置。
-   切勿随意删除或修改日志服务为您创建的默认Project、Logstore、索引和仪表盘等设置。
-   日志服务将不定期更新、升级日志查询与分析功能，您专属日志库中的索引与默认报表也将自动更新。
-   如果子账号需要使用日志查询分析功能，您可以通过RAM为其授予日志服务的相关权限。

