Splunk EnterpriseでEPSS(Exploit Prediction Scoring System )をパースするためのprops.confとtransforms.confです。
EPSSのデータは以下Firstのサイトから入手ができます。
https://www.first.org/epss/data_stats<P>

このパーサーでは日付別の全データを対象にパースするパーサーとなります。
日付別のデーターは以下のURLフォーマットで入手可能です。
 https://epss.cyentia.com/epss_scores-YYYY-mm-dd.csv.gz<P>

<li>データはCSV形式のデータをgzで圧縮されています。
<li>各データ及びフィールドには日付が含まれていません。そのため、transforms.confでsourceからデータの日付をパースして付け加える処理を行っています。
<li>props.conf及びtransforms.confを/opt/splunk/etc/apps/[your_apps_name]/local/配下に置いてください。
<li>デフォルトのsourcetypeは"epss_data"です。