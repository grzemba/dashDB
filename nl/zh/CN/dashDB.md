---

copyright:
  years: 2014, 2017
lastupdated: "2017-05-16"

---

<!-- Attribute definitions --> 
{:javascript: #javascript .ph data-hd-programlang='javascript'}
{:java: #java .ph data-hd-programlang='java'}
{:ruby: #ruby .ph data-hd-programlang='ruby'}
{:php: #php .ph data-hd-programlang='php'}
{:python: #python .ph data-hd-programlang='python'}
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:pre: .pre}

#dashDB 入门
{: #dashDB}

{{site.data.keyword.IBM}} {{site.data.keyword.dashdbshort}} 受管服务是在云中为您供应的 SQL 数据库。您可以使用 {{site.data.keyword.dashdbshort_notm}} 就像使用任何数据库软件一样，但是却没有硬件设置或软件安装和维护所产生的开销和费用。
{: shortdesc}

##界面
{: #interfaces}

您可以通过四种方法来使用 {{site.data.keyword.dashdbshort_notm}} 数据库：
{: shortdesc}

   * {{site.data.keyword.dashdbshort_notm}} Web 控制台
   * REST API
   * 从本地计算机连接应用程序或喜爱的工具
   * 使用 {{site.data.keyword.dashdbshort_notm}} 作为 Bluemix 应用程序或服务的数据源

###dashDB Web 控制台
{: #web_console}

Web 控制台为您需要使用数据库的所有项目提供图形界面，包括：装入功能、SQL 编辑器、驱动程序下载等。
{: shortdesc}

![{{site.data.keyword.dashdbshort_notm}} Web 控制台仪表板页面的视图](images/console_v1.jpg)
<!-- ![View of {{site.data.keyword.dashdbshort_notm}} web console dashboard page](images/console_v2.jpg) -->

单击链接以浏览 {{site.data.keyword.dashdbshort_notm}} Web 控制台：[通览 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibm.biz/dashdb-general-quick-tour){:new_window}。

您可以通过两种方法来访问 {{site.data.keyword.dashdbshort_notm}} Web 控制台：
   * 从 {{site.data.keyword.Bluemix_notm}} 仪表板 - 您可以从 {{site.data.keyword.dashdbshort_notm}} 服务的“服务详细信息”页面打开 Web 控制台。
   * 直接 URL - 您可以针对 {{site.data.keyword.dashdbshort_notm}} 服务为 Web 控制台的 URL 设置书签。

###REST API
{: #apis}

使用 {{site.data.keyword.dashdbshort_notm}} for Analytics 计划，您可以利用 [{{site.data.keyword.dashdbshort_notm}} REST API ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibm.biz/dashdb-api){:new_window}，来执行文件管理、装入数据和运行 R 脚本的相关任务。
{: shortdesc}

###从本地计算机连接应用程序或喜爱的工具
{: #connect_apps}

通过完成以下步骤，配置本地环境以连接到 {{site.data.keyword.dashdbshort_notm}} 数据库：
{: shortdesc}

1. 从 {{site.data.keyword.dashdbshort_notm}} Web 控制台的“下载”页面下载 [{{site.data.keyword.dashdbshort_notm}}驱动程序包 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/support/knowledgecenter/SS6NHC/com.ibm.swg.im.dashdb.doc/connecting/connect_driver_package.html){:new_window}。
2. 在运行应用程序和工具的计算机上[安装驱动程序包 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/support/knowledgecenter/SS6NHC/com.ibm.swg.im.dashdb.doc/connecting/connect_driver_package_install.html){:new_window}。
3. 为 {{site.data.keyword.dashdbshort_notm}} 数据库[配置驱动程序文件 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/support/knowledgecenter/en/SS6NHC/com.ibm.swg.im.dashdb.doc/connecting/connect_driver_package_config.html){:new_window}。

###使用 dashDB 作为 Bluemix 应用程序或服务的数据源
{: #data_src}

在 {{site.data.keyword.Bluemix_notm}} 上托管的应用程序可以使用与本地应用程序连接到 {{site.data.keyword.dashdbshort_notm}} 数据库完全相同的方法，连接到 {{site.data.keyword.dashdbshort_notm}} 数据库。
{: shortdesc}

当应用程序使用 {{site.data.keyword.Bluemix_notm}} 平台时，您可以利用 `VCAP _SERVICES` 环境变量来简化指定数据库详细信息和凭证的任务：
1. 在 {{site.data.keyword.Bluemix_notm}} 仪表板上，在 {{site.data.keyword.dashdbshort_notm}} 服务的“服务详细信息”页面的**连接**选项卡上，单击**创建连接**按钮。
2. 选择 {{site.data.keyword.Bluemix_notm}} 应用程序以使用 {{site.data.keyword.dashdbshort_notm}} 数据库作为数据源，然后单击**连接**按钮。
3. 更新应用程序代码以从 `VCAP_SERVICES` 环境变量检索数据库详细信息和凭证：

    **没有“VCAP_SERVICES”的示例**

    ```php
    <?php
    $driver      = "DRIVER={IBM DB2 ODBC DRIVER};";

    $database    = "BLUDB";         # Get these database details from
    $hostname    = "<Host-name>";   # the Connect page of the dashDB
    $port        = 50000;           # web console.
    $user        = "<User-ID >";    #
    $password    = "<Password>";    #
    $dsn         = "DATABASE=$database;" .
                   "HOSTNAME=$hostname;" .
                   "PORT=$port;" .
                   "PROTOCOL=TCPIP;" .
                   "UID=$user;" .
                   "PWD=$password;";

    $conn_string = $driver . $dsn;

    $conn        = db2_connect( $conn_string, "", "" );
    ?>
    ```

    **具有“VCAP_SERVICES”的示例**

    ```php
    <?php
    $driver      = "DRIVER={IBM DB2 ODBC DRIVER};";

    $vcap        = json_decode( getenv( "VCAP_SERVICES" ), true );
    $dsn         = $vcap[ "dashDB" ][0][ "credentials" ][ "dsn" ];

    $conn_string = $driver . $dsn;
                                   
    $conn        = db2_connect( $conn_string, "", "" );
    ?>
    ```

##样本
{: #samples}

以下链接是演示在不同的语言中，如何从应用程序连接到 {{site.data.keyword.dashdbshort_notm}} 数据库的样本：
{: shortdesc}

   * [.NET ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/support/knowledgecenter/SS6NHC/com.ibm.swg.im.dashdb.doc/connecting/connect_connecting__net_applications.html){:new_window}
<!-- * [JAVA ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/SS6NHC/com.ibm.swg.im.dashdb.doc/connecting/connect_connecting_java.html){:new_window} -->
   * [JDBC ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/support/knowledgecenter/SS6NHC/com.ibm.swg.im.dashdb.doc/connecting/connect_connecting_jdbc_applications.html){:new_window}
<!-- * [Node.js ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/SS6NHC/com.ibm.swg.im.dashdb.doc/connecting/connect_connecting_nodejs.html){:new_window} -->
   * [PHP ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/support/knowledgecenter/SS6NHC/com.ibm.swg.im.dashdb.doc/connecting/connect_connecting_php.html){:new_window}
<!-- * [Python ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/SS6NHC/com.ibm.swg.im.dashdb.doc/connecting/connect_connecting_python.html){:new_window} -->
   * [GitHub 上的 dashDB 样本 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://github.com/IBM-Bluemix/dashdb-nodejs-helloworld){:new_window}


