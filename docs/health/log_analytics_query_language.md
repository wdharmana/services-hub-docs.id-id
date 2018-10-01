  <h1>Bahasa Kueri Analitik Log</h1>
    <p><br>
      Analitik Log Azure yang baru dan lebih baik baru-baru ini yang diumumkan baru-baru ini menyediakan bahasa kueri dengan Analitik Pintar.<br>
      <br>
      Agar dapat memaksimalkan penggunaan peningkatan, kami telah menyediakan beberapa kueri untuk memahami data penilaian menggunakan bahasa kueri baru.<br>
      <br>
      Coba bahasa kueri yang baru:</p>
    <ol>
      <li>Tingkatkan dalam 5 menit dengan <a href="https://go.microsoft.com/fwlink/?linkid=851478" target="_blank">referensi cepat bahasa kueri</a>.</li>
      <li>Kunjungi <a href="https://go.microsoft.com/fwlink/?linkid=856078" target="_blank">Mulai Menggunakan Kueri</a> untuk mempelajari cara menulis kueri baru.</li>
      <li>Gunakan <a href="https://go.microsoft.com/fwlink/?linkid=856079" target="_blank">Referensi Bahasa Kueri</a> untuk mendapatkan detail tentang fungsi, operator, dan tipe.</li>
      <li>Lihat tutorial kami tentang <a href="https://go.microsoft.com/fwlink/?linkid=851480" target="_blank">Bekerja dengan String</a>, serta <a href="https://go.microsoft.com/fwlink/?linkid=851481" target="_blank">Operasi Tanggal dan Waktu </a>untuk mempelajari tentang tipe data.</li>
      <li>Gunakan <a href="https://go.microsoft.com/fwlink/?linkid=851482" target="_blank">agregasi</a> untuk mendapatkan wawasan tentang data Anda.</li>
    </ol>
    <p>Semua kueri Bahasa Kueri Baru dapat dicoba di <a href="https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAAwsO9HEsLk4tLs5NzSsJSk3OzwUyUhJLMvPzFGoUyjNSi1IVQjJzU91T81KLEktSUxTsbBUS0%2FM1zFM0uQD2MhLEPQAAAA%3D%3D" target="_blank">Portal Demo</a>.</p>
    <p><a href="https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAAwsO9HEsLk4tLs5NzSsJSk3OzwUyUhJLMvPzFGoUyjNSi1IVQjJzU91T81KLEktSUxTsbBUS0%2FM1zFM0uQD2MhLEPQAAAA%3D%3D" target="_blank"><br>
      </a></p>
    <h2>Kueri yang Relevan:</h2>
1. Mendapatkan Data Rekomendasi Mentah untuk Penilaian tertentu
    <p>SQLAssessmentRecommendation<br>
      <a href="https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAAwsO9HEsLk4tLs5NzSsJSk3OzwUyUhJLMvPzuAB%2Bs2wVHAAAAA%3D%3D&amp;timespan=P7D" target="_blank">Coba Sekarang</a>
      <br>
      <br>
      <br>
2. Mendapatkan Data Log Penilaian untuk Komputer Tertentu <pre>Operation | where Computer == "ContosoADDS1.ContosoRetail.com" |
      summarize arg_max(TimeGenerated, *) by OperationCategory, Solution, Detail<br></pre>

<a href="https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAAzWNQQrCMBBF957i05VKKHiALiQBlwXrXqIdaqCTKdMErXh4W7HL%2F%2BC%2FVw%2BkPgWJ%2BOD5ICVY4SEnUlQVCisxyShH55pD%2BR9nSj705V24wPwaM7PX8CZ47a7sX9tLYDpRXMTUGux3uE2o15CdaSc6GTTS54UYuJ9y8wWLCKQcjQAAAA%3D%3D&amp;timespan=P7D" target="_blank">Coba Sekarang</a></p>
<p><a href="https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAAzWNQQrCMBBF957i05VKKHiALiQBlwXrXqIdaqCTKdMErXh4W7HL%2F%2BC%2FVw%2BkPgWJ%2BOD5ICVY4SEnUlQVCisxyShH55pD%2BR9nSj705V24wPwaM7PX8CZ47a7sX9tLYDpRXMTUGux3uE2o15CdaSc6GTTS54UYuJ9y8wWLCKQcjQAAAA%3D%3D&amp;timespan=P7D" target="_blank"></a>
    </p>
<i>Catatan: argmax digunakan untuk mengembalikan data terbaru. Detail tentang cara kerja arg_max tersedia di sini.</i>
<br>
<br>
<br>
<br>
3. Memeriksa Status Solusi untuk Berbagai Kategori Operasi di Semua Komputer<br>
<pre>Check whether Operations such as Assessment Target Check, .NET Check, Is
      Local Administrator Check etc. were successful or not.</pre>
    <pre> Operation | where Solution =="SQLAssessment" | summarize
       arg_max(TimeGenerated, *) by Computer, OperationCategory | sort by
    TimeGenerated desc , OperationStatus asc<br></pre>
    
  <a href="https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAA1WNsQrCQBBEe79iSKWSX0ghKWyEIGcvZ7LEA%2Fcu7O6hET%2FenCBoOzPvTTeReAspAi%2FcryQEl275kzRN5Y6HnSqpMkWrlolmZi%2FhSfAyntk%2F1qfAtKdYNDTU2G5wmdEmnrKR1Oi%2BB%2B3Sj0nmIkliZfWHYiDt8QM485YVXvvVGz044yimAAAA&amp;timespan=P7D" target="_blank">Coba Sekarang</a>
    <br>
    <br>
    <br>
    <br>
 4. Untuk Penilaian, dapatkan semua Objek Terpengaruh dan kapan objek tersebut Diakses<br>
    <pre>SQLAssessmentRecommendation | summarize AggregatedValue =
      max(TimeGenerated) by AffectedObjectName | sort by AggregatedValue desc</pre>

<a href="https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAA12MOwrDMBAF%2B5xiy%2FgQKVSlCTb%2B4H4tPQuFrARaGeKQw0dO6erNY2DG%2FmFUoSqIZYBNUsFxCSnSl3QT4Rw%2BION9hucCN%2FNrA91I%2BH2dguCOiHyIhpadzLrC1tMtz7otC45MyuUvTxEHtZcf0l7HGIIAAAA%3D&amp;timespan=P7D" target="_blank">Coba Sekarang</a>
    <br>
    <br>
    <br>
    <br>
  5. Memeriksa Data Rekomendasi Tersedia untuk Penilaian atau Tidak</b><br>

  <pre>SQLAssessmentRecommendation | summarize Result = count() &gt; 0(returns a
    true or false value based on whether data is available or not)<br></pre>

  <a href="https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAAwsO9HEsLk4tLs5NzSsJSk3OzwUyUhJLMvPzFGoUiktzcxOLMqtSFYJSi0tzShRsFZLzS%2FNKNDQV7BQMALZLUg88AAAA&amp;timespan=P7D" target="_blank">Coba Sekarang</a>
     <br>
  <br><br><br>
  6. Untuk Mendapatkan Detail Id Rekomendasi Tertentu yang Gagal</b><br>
<pre>SQLAssessmentRecommendation | where RecommendationId
    =="7821eda2-c420-4920-bc0c-ca8cd1d48482" and RecommendationResult=="Failed"
</pre>
<p><a href="https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAAwsO9HEsLk4tLs5NzSsJSk3OzwUyUhJLMvPzFGoUyjNSi1IVUIU9UxRsbZXMLYwMU1MSjXSTTYwMdE0sgURSskGybnKiRXKKYYqJhYmFkZJCYl4Kmu6g1OLSnBKgAW6JmTmpKUpcAGMRaVqBAAAA&amp;timespan=P7D"target="_blank">Coba Sekarang</a>
      <br>
      <br>
      <br>
       <br>
7. Mendapatkan Daftar yang Diprioritaskan dari Rekomendasi Gagal</b></p>
  <p>Tindakan ini akan mencantumkan rekomendasi yang gagal untuk kombinasi unik RecommendationId dan AffectedObjectUniqueName bagi operasi terbaru untuk Penilaian.<br>

  <pre>ADAssessmentRecommendation | summarize arg_max(TimeGenerated, *) by
      RecommendationId, AffectedObjectUniqueName |where RecommendationResult ==
      "Failed" | sort by RecommendationScore desc, TimeGenerated desc</pre>
      
  Lihat penggunaan arg_max seperti yang disebutkan dalam kueri 2 di atas.
  <p>
  <a href="https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAA2WOuw7CMAxFd77CYgLUX%2BhQCYFYQCowIze5haA6EXEqHurHE9gKk6%2BO7rFdLStVqAp8qmGC5GA5ueBpIO1FOLoXiOP5JPyYHZxgDY%2FICbagxZyaJ429TeZV28Lkxq655nn07tZjywIa7hdE%2FBg1tO8SUVnSdMWug51%2BjoeY%2FrfvTci%2BhZqCRs982eQNRA0EVs8AAAA%3D&amp;timespan=P7D"target="_blank">Coba Sekarang</a><br>
      <br>
      <br>
      <br>
 8. Mendapatkan Detail Terkait Rekomendasi yang Gagal untuk Objek Terpengaruh Tertentu </b>
      <br>
         <pre>SQLAssessmentRecommendation | where AffectedObjectName ==
      "ContosoMABSVM1.CONTOSORETAIL.COM" | summarize arg_max(TimeGenerated, *)
      by RecommendationId | where RecommendationResult == "Failed"<br></pre>
    
  <a href="https://portal.loganalytics.io/Demo?q=H4sIAAAAAAAAA1WNzQrCMBCE7z7F0pOKCD5AD7GoFNoG2%2BJVUrPVSDeBbIo%2F%2BPAGD0JPM8PA9zXHQjAjM6ENNV4cxaJVMM4CfOBxQ48g%2Bh4vAbXs7jErRQhpCknmbHDsSrFtTuVmncmqlY2sd63Ii7jKJAJ4JFLevBGUv55JPeetITygRa8icQXLBXQvmJpz%2FVdPjxp5HMJPvldmQJ3MvgD9VaDBAAAA&amp;timespan=P7D" target="_blank">Coba Sekarang</a></p>
        <br><br>
    Klik <a href="mailto:SHub_Feedback_RC@Microsoft.com?subject=Resource%20Center%20Feedback%3A%20%3CInsert%20feedback%20topic%3E%3E&amp;body=%3C%3Cplease%20submit%20your%20feedback%20with%20enough%20detail%20on%20the%20problem%2C%20reproduction%20steps%20and%20what%20you%20desire%20to%20happen%3E%3E" target="_blank">di sini</a> untuk memberikan umpan balik.
    <div></div>
