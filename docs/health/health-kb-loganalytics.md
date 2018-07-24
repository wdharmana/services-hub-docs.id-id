# <a name="get-deeper-insights-from-your-data-with-the-new-log-analytics-query-language"></a>Dapatkan Wawasan yang Lebih Mendalam dari Data Anda dengan Bahasa Kueri Analitik Log Azure yang Baru

[Analitik Log Azure](https://azure.microsoft.com/en-us/blog/announcing-the-new-and-improved-azure-log-analytics/) menyediakan bahasa kueri yang canggih dengan Analitik Cerdas bawaan.

Untuk mengoptimalkan penggunaan Analitik Log Azure, kami telah menyediakan beberapa kueri menggunakan bahasa yang baru.

### <a name="try-the-new-query-language"></a>Coba bahasa kueri yang baru:

1.  Tinjau [referensi cepat bahasa kueri](https://go.microsoft.com/fwlink/?linkid=851478).

2.  Kunjungi [Mulai Menggunakan Kueri](https://go.microsoft.com/fwlink/?linkid=856078) untuk mempelajari cara menulis kueri baru.

3.  Gunakan [Referensi Bahasa Kueri](https://go.microsoft.com/fwlink/?linkid=856079) untuk mendapatkan detail tentang fungsi, operator, dan tipe.

4.  Tinjau tutorial berikut: [Bekerja dengan String](https://go.microsoft.com/fwlink/?linkid=851480) serta [Operasi tanggal dan waktu](https://go.microsoft.com/fwlink/?linkid=851481) untuk mempelajari tentang tipe data.

5.  Gunakan [agregasi](https://go.microsoft.com/fwlink/?linkid=851482) untuk mendapatkan wawasan tentang data Anda.

**Kueri yang Relevan:**

*Catatan: Semua kueri Bahasa Kueri Baru dapat dicoba di [Portal Demo](https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAAwsO9HEsLk4tLs5NzSsJSk3OzwUyUhJLMvPzFGoUyjNSi1IVQjJzU91T81KLEktSUxTsbBUS0%2FM1zFM0uQD2MhLEPQAAAA%3D%3D).

6.  Mendapatkan Data Rekomendasi Mentah untuk Penilaian tertentu.

> SQLAssessmentRecommendation
> 
> [Coba Sekarang](https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAAwsO9HEsLk4tLs5NzSsJSk3OzwUyUhJLMvPzuAB%2Bs2wVHAAAAA%3D%3D&timespan=P7D)

7.  Mendapatkan Data Log Penilaian untuk Komputer tertentu.

> Operation \| where Computer == \"ContosoADDS1.ContosoRetail.com\" \| summarize arg\_max(TimeGenerated, \*) by OperationCategory, Solution, Detail
>
> [Coba Sekarang](https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAAzWNQQrCMBBF957i05VKKHiALiQBlwXrXqIdaqCTKdMErXh4W7HL%2F%2BC%2FVw%2BkPgWJ%2BOD5ICVY4SEnUlQVCisxyShH55pD%2BR9nSj705V24wPwaM7PX8CZ47a7sX9tLYDpRXMTUGux3uE2o15CdaSc6GTTS54UYuJ9y8wWLCKQcjQAAAA%3D%3D&timespan=P7D)
>
*Catatan: arg\_max digunakan untuk mengembalikan data terbaru. Detail tentang cara kerja arg\_max tersedia [di sini](https://docs.loganalytics.io/docs/Language-Reference/Aggregation-functions/arg_max()).

8.  Memeriksa Status Solusi untuk berbagai Kategori Operasi di semua komputer.

> Periksa apakah operasi seperti Assessment Target Check dan .NET Check, Is Local Administrator Check berhasil atau tidak.
>
> Operation \| where Solution ==\"SQLAssessment\" \| summarize arg\_max(TimeGenerated, \*) by Computer, OperationCategory \| sort by TimeGenerated desc , OperationStatus asc
>
> [Coba Sekarang](https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAA1WNsQrCQBBEe79iSKWSX0ghKWyEIGcvZ7LEA%2Fcu7O6hET%2FenCBoOzPvTTeReAspAi%2FcryQEl275kzRN5Y6HnSqpMkWrlolmZi%2FhSfAyntk%2F1qfAtKdYNDTU2G5wmdEmnrKR1Oi%2BB%2B3Sj0nmIkliZfWHYiDt8QM485YVXvvVGz044yimAAAA&timespan=P7D)

9.  Untuk penilaian, mendapatkan semua Objek Terpengaruh dan kapan objek tersebut diakses.

> SQLAssessmentRecommendation \| summarize AggregatedValue = max(TimeGenerated) by AffectedObjectName \| sort by AggregatedValue desc
>
> [Coba Sekarang](https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAA12MOwrDMBAF%2B5xiy%2FgQKVSlCTb%2B4H4tPQuFrARaGeKQw0dO6erNY2DG%2FmFUoSqIZYBNUsFxCSnSl3QT4Rw%2BION9hucCN%2FNrA91I%2BH2dguCOiHyIhpadzLrC1tMtz7otC45MyuUvTxEHtZcf0l7HGIIAAAA%3D&timespan=P7D)

10.  Untuk memeriksa apakah tersedia data rekomendasi untuk penilaian atau tidak.

> SQLAssessmentRecommendation \| summarize Result = count() \> 0
>
> (mengembalikan nilai benar atau salah berdasarkan ketersediaan data)
>
> [Coba Sekarang](https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAAwsO9HEsLk4tLs5NzSsJSk3OzwUyUhJLMvPzFGoUiktzcxOLMqtSFYJSi0tzShRsFZLzS%2FNKNDQV7BQMALZLUg88AAAA&timespan=P7D)

11.  Untuk mendapatkan detail ID rekomendasi tertentu yang gagal.

> SQLAssessmentRecommendation \| where RecommendationId ==\"7821eda2-c420-4920-bc0c-ca8cd1d48482\" and RecommendationResult==\"Failed\"
>
> [Coba Sekarang](https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAAwsO9HEsLk4tLs5NzSsJSk3OzwUyUhJLMvPzFGoUyjNSi1IVUIU9UxRsbZXMLYwMU1MSjXSTTYwMdE0sgURSskGybnKiRXKKYYqJhYmFkZJCYl4Kmu6g1OLSnBKgAW6JmTmpKUpcAGMRaVqBAAAA&timespan=P7D)

12.  Mendapatkan daftar rekomendasi gagal yang diprioritaskan.

> Tindakan ini akan membuat daftar rekomendasi yang gagal untuk kombinasi unik RecommendationId dan AffectedObjectUniqueName bagi operasi penilaian terbaru.
>
> ADAssessmentRecommendation \| summarize arg\_max(TimeGenerated, \*) by RecommendationId, AffectedObjectUniqueName \|where RecommendationResult == \"Failed\" \| sort by RecommendationScore desc, TimeGenerated desc
>
> Lihat penggunaan arg\_max seperti yang disebutkan dalam kueri 2 di atas.
>
> [Coba Sekarang](https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAA2WOuw7CMAxFd77CYgLUX%2BhQCYFYQCowIze5haA6EXEqHurHE9gKk6%2BO7rFdLStVqAp8qmGC5GA5ueBpIO1FOLoXiOP5JPyYHZxgDY%2FICbagxZyaJ429TeZV28Lkxq655nn07tZjywIa7hdE%2FBg1tO8SUVnSdMWug51%2BjoeY%2FrfvTci%2BhZqCRs982eQNRA0EVs8AAAA%3D&timespan=P7D)

13.  Mendapatkan detail terkait rekomendasi yang gagal untuk objek terpengaruh tertentu.

> SQLAssessmentRecommendation \| where AffectedObjectName == \"ContosoMABSVM1.CONTOSORETAIL.COM\" \| summarize arg\_max(TimeGenerated, \*) by RecommendationId \| where RecommendationResult == \"Failed\"
>
> [Coba Sekarang](https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAA1WNzQrCMBCE7z7F0pOKCD5AD7GoFNoG2%2BJVUrPVSDeBbIo%2F%2BPAGD0JPM8PA9zXHQjAjM6ENNV4cxaJVMM4CfOBxQ48g%2Bh4vAbXs7jErRQhpCknmbHDsSrFtTuVmncmqlY2sd63Ii7jKJAJ4JFLevBGUv55JPeetITygRa8icQXLBXQvmJpz%2FVdPjxp5HMJPvldmQJ3MvgD9VaDBAAAA&timespan=P7D)



Klik <a href="mailto:SHub_Feedback_RC@Microsoft.com?subject=Resource%20Center%20Feedback%3A%20%3CInsert%20feedback%20topic%3E%3E&amp;body=%3C%3Cplease%20submit%20your%20feedback%20with%20enough%20detail%20on%20the%20problem%2C%20reproduction%20steps%20and%20what%20you%20desire%20to%20happen%3E%3E" target="_blank">di sini</a> untuk memberikan umpan balik.
