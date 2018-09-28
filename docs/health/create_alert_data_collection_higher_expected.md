<H1>Membuat Peringatan saat Pengumpulan Data Lebih Tinggi daripada yang Diharapkan</H1>
    <h3><br>
      Bagian ini menjelaskan cara membuat peringatan jika:</h3>
    <div>• Volume data melebihi jumlah tertentu.<br>
      • Volume data diprediksi melebihi jumlah tertentu.<br>
    </div>
    <div>Peringatan Azure mendukung peringatan log yang menggunakan kueri pencarian.<br>
      Kueri berikut memberi hasil jika ada lebih dari 100 GB data terkumpul dalam 24 jam terakhir:</div>
    <pre>union withsource = $table Usage | where<br>QuantityUnit == "MBytes" and iff(isnotnull(toint(IsBillable)),<br>IsBillable == true, IsBillable == "true") == true | extend Type =<br>$table | summarize DataGB = sum((Quantity / 1024)) by Type | where DataGB &gt;<br>4 | where TimeGenerated &gt;= ago(30d)</pre><div><br></div><div>Jika Anda menerima peringatan, gunakan langkah-langkah dalam tautan berikut untuk menyelesaikan masalah penyebab penggunaan lebih tinggi daripada semestinya atau jika Anda ingin mengetahui detail lengkap tentang topik ini: <a href="https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-usage#create-an-alert-when-data-collection-is-higher-than-expected" target="_blank">https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-usage#create-an-alert-when-data-collection-is-higher-than-expected</a><br></div><div>
    <div><br>
    </div>
    <div>Klik <a href="mailto:SHub_Feedback_RC@Microsoft.com?subject=Resource%20Center%20Feedback%3A%20%3CInsert%20feedback%20topic%3E%3E&amp;body=%3C%3Cplease%20submit%20your%20feedback%20with%20enough%20detail%20on%20the%20problem%2C%20reproduction%20steps%20and%20what%20you%20desire%20to%20happen%3E%3E" >di sini</a> untuk memberikan umpan balik. </div>
    <div><br>
    </div>
    <div></div>