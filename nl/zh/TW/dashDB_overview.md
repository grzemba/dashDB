---

copyright:
  years: 2014, 2017
lastupdated: "2017-05-16"

---

<!-- Attribute definitions --> 
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

#關於 dashDB
{: #dashDB_overview}

{{site.data.keyword.IBM}} {{site.data.keyword.dashdbshort}} 提供了兩種不同的資料庫解決方案：資料倉儲和分析解決方案（{{site.data.keyword.dashdbshort_notm}} for Analytics 方案），以及線上交易處理解決方案（{{site.data.keyword.dashdbshort_notm}} for Transactions 方案）。
{: shortdesc}

##dashDB 受管理服務
{: #managed_service}

完整的 {{site.data.keyword.dashdbshort_notm}} 受管理服務處理所有軟體升級、作業系統更新，以及硬體維護。此服務包括全年無休的資料庫及基礎架構性能監視。在硬體故障或軟體失敗的情況下，此服務會自動重新啟動。
{: shortdesc}

如需 {{site.data.keyword.dashdbshort_notm}} 受管理服務方面的相關資訊，請參閱：[{{site.data.keyword.dashdbshort_notm}} 受管理服務 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/support/knowledgecenter/SS6NHC/com.ibm.swg.im.dashdb.doc/managed_service.html)。

##方案及配置
{: #plans_cfgs}

您可以選擇 {{site.data.keyword.dashdbshort_notm}} 方案，該方案已針對您需要執行的工作進行配置且最佳化：
{: shortdesc}

   * 嘗試各種事物的入門方案
   * 小型、中型及大型正式作業方案
   * 適用於平行處理的 MPP 配置
   * 針對高可用性或 Oracle 相容性所配置的方案
   * 以及其他 ...

檢視 {{site.data.keyword.Bluemix}} 型錄中的可用方案：
   * 針對資料倉儲和分析 (OLAP) 工作負載所配置的方案：[{{site.data.keyword.dashdbshort_notm}} for Analytics](https://console.ng.bluemix.net/catalog/services/dashdb-for-analytics){:new_window}
   * 針對高速的交易處理 (OLTP) 所配置的方案：[{{site.data.keyword.dashdbshort_notm}} for Transactions](https://console.ng.bluemix.net/catalog/services/dashdb-for-transactions-sql-database){:new_window}

如果您在型錄中看不到所需要的配置，[請與 {{site.data.keyword.IBM_notm}} 銷售人員聯絡 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/connect/ibm/us/en/?lnk=fcw){:new_window}，來討論其他選項。

##dashDB for Analytics
{: #dashDB_an}

在 {{site.data.keyword.dashdbshort_notm}} for Analytics 資料倉儲方案中，使用 {{site.data.keyword.dashdbshort_notm}} 資料倉儲來儲存關聯式資料，包括地理空間資料之類的特殊類型。請使用我們的內建分析或自行連接您的應用程式，來分析您自己的資料，或是從其他雲端服務載入的資料。您可以利用高效能、記憶體內資料庫技術來處理分析工作負載的直欄式表格。{{site.data.keyword.dashdbshort_notm}} Web 主控台會處理一般資料管理作業，例如載入資料，以及像是執行查詢和 R Script 的分析作業。
{: shortdesc}

您也可以將外部應用程式和工具連接到 {{site.data.keyword.dashdbshort_notm}}，並使用它們進一步管理或分析您的資料。例如：
   * 連接 {{site.data.keyword.IBM_notm}} InfoSphere® Data Architect，以設計及部署資料庫綱目。
   * 連接 Esri ArcGIS 以執行地理空間分析，及將發佈與您的資料相對映。
   * 連接 {{site.data.keyword.IBM_notm}} Cognos® 伺服器，以針對您的資料執行 Cognos 報告。
   * 連接 SQL 型工具，例如 Tableau、Microstrategy 或 Microsoft Excel，以操作或分析您的資料。
   * 連接需要分析資料庫的 {{site.data.keyword.Bluemix_short}} 應用程式。
   * 連接 Aginity Workbench，以將 Netezza® 資料模型和資料移轉到 {{site.data.keyword.dashdbshort_notm}}。

##佈建 dashDB for Analytics
{: #whse_provision}

{{site.data.keyword.IBM_notm}} {{site.data.keyword.dashdbshort_notm}} for Analytics 資料倉儲可以佈建在 {{site.data.keyword.BluSoftlayer_full}} 上，也可以針對 AWS 佈建。
{: shortdesc}

如果您要針對 AWS 佈建 {{site.data.keyword.dashdbshort_notm}} for Analytics 資料倉儲，請選取 **{{site.data.keyword.IBM_notm}} {{site.data.keyword.dashdbshort_notm}} for Analytics MPP Small for AWS** 方案。

##dashDB for Transactions
{: #dashDB_tr}

在 {{site.data.keyword.dashdbshort_notm}} for Transactions 方案中，使用 {{site.data.keyword.dashdbshort_notm}} 關聯式資料庫來進行線上交易處理。您可以連接新的或現有的應用程式，而且可以開始處理交易並儲存資料。使用 DB2® and Oracle 相容性，您可以連接小型或大型應用程式，並且受益於受管理的企業級資料庫系統。您可以運用 {{site.data.keyword.dashdbshort_notm}} for Transactions Web 主控台來管理使用者、載入資料，並且取得連線資訊。
{: shortdesc}

<!-- ##dashDB web console overview
{: #console_overview}

You can manage your {{site.data.keyword.dashdbshort_notm}} database, analyze your data, and monitor sensitive data with the {{site.data.keyword.dashdbshort_notm}} web console accessible from {{site.data.keyword.Bluemix_notm}}.
{: shortdesc}

Open the web console by clicking the service tile on your application overview page, and then click **Open**.

Single sign-on authentication connects you directly to the web console. You can access connection information from the web console, and the **Downloads** page includes links to client drivers for accessing {{site.data.keyword.dashdbshort_notm}} from remote applications. You can also access sample data and reports.

###Sensitive data reporting

The {{site.data.keyword.dashdbshort_notm}} web console includes a sensitive data reporting feature that detects and monitors sensitive objects in the {{site.data.keyword.dashdbshort_notm}} data warehouse, such as credit card numbers and US Social Security numbers.

To run and view reports that identify columns that contain sensitive data and provide information about connections and activities that access the sensitive data, select **Monitor &gt; Sensitive Data** in the web console. -->


<!-- ##IBM Analytics Services
{: #analytics_services}

For more information about {{site.data.keyword.IBM_notm}} analytics services and finding your local services representative, see: [{{site.data.keyword.IBM_notm}} Analytics Services ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://www.ibm.com/software/data/services/).
{: shortdesc} -->














