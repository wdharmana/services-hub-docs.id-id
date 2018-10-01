# <a name="create-an-alert-when-data-collection-is-higher-than-expected"></a>Membuat Peringatan saat Pengumpulan Data Lebih Tinggi daripada yang Diharapkan

## <a name="this-section-describes-how-to-create-an-alert-if"></a>Bagian ini menjelaskan cara membuat peringatan jika:

> Volume data melebihi jumlah tertentu.

> Volume data diprediksi melebihi jumlah tertentu.

Peringatan Azure mendukung peringatan log yang menggunakan kueri pencarian.

Kueri berikut memberi hasil jika ada lebih dari 4 GB data terkumpul dalam 30 hari terakhir: 

```
union withsource = $table Usage | where
QuantityUnit == "MBytes" and iff(isnotnull(toint(IsBillable)),
IsBillable == true, IsBillable == "true") == true | extend Type =
$table | summarize DataGB = sum((Quantity / 1024)) by Type | where DataGB >
4 | where TimeGenerated >= ago(30d)
```

Jika Anda menerima peringatan, gunakan langkah-langkah dalam tautan berikut untuk menyelesaikan masalah penyebab penggunaan lebih tinggi daripada semestinya atau jika Anda ingin mengetahui detail lengkap tentang topik ini: <a href="https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-usage#create-an-alert-when-data-collection-is-higher-than-expected" target="_blank">https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-usage#create-an-alert-when-data-collection-is-higher-than-expected</a>

Klik <a href="mailto:SHub_Feedback_RC@Microsoft.com?subject=Resource%20Center%20Feedback%3A%20%3CInsert%20feedback%20topic%3E%3E&amp;body=%3C%3Cplease%20submit%20your%20feedback%20with%20enough%20detail%20on%20the%20problem%2C%20reproduction%20steps%20and%20what%20you%20desire%20to%20happen%3E%3E" target="_blank">di sini</a> untuk memberikan umpan balik.
