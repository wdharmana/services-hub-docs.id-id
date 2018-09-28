# <a name="getting-started-with-on-demand-assessments"></a>Memulai dengan Penilaian Atas Permintaan

Penilaian tersedia melalui Services Hub untuk membantu Anda mengoptimalkan ketersediaan, keamanan, dan kinerja investasi teknologi Microsoft Anda. Penilaian ini menggunakan Azure Log Analytics Microsoft, yang dirancang untuk memberi Anda manajemen TI dan keamanan yang disederhanakan di lingkungan Anda.

## <a name="starting-an-assessment"></a>Memulai Penilaian

### <a name="prerequisites"></a>Prasyarat

Agar dapat memanfaatkan sepenuhnya Penilaian Atas Permintaan yang tersedia melalui Services Hub, Anda harus:

1.  Berlangganan Azure. Anda dapat menggunakan pembayaran saat menggunakan akun gratis. Untuk informasi lebih lanjut, lihat:<a href="Azure_Sponsored_Subscription.md" target="_blank"> Opsi Langganan Azure</a>.

2.  Mampu menautkan Services Hub Anda, dan Akun Langganan Azure.

*Catatan: Rata-rata, dibutuhkan dua jam untuk mengonfigurasi awal lingkungan Anda untuk menjalankan penilaian atas permintaan. Setelah menjalankan penilaian, Anda dapat meninjau data di Azure Log Analytics. Ini akan memberi Anda daftar rekomendasi prioritas, yang dikategorikan di enam area fokus. Memungkinkan Anda dan tim untuk cepat memahami tingkat risiko, kesehatan lingkungan Anda, bertindak untuk mengurangi risiko, dan meningkatkan kesehatan TI Anda secara keseluruhan.*

#### <a name="linking-services-hub-to-your-azure-log-analytics-workspace"></a>Menautkan Services Hub ke Ruang Kerja Azure Log Analytics Anda

*Catatan: Hanya pemilik langganan Azure dan ruang kerja Analitik Log Azure yang dapat menautkan Hub Layanan ke Analitik Log Azure.*

1.  Masuk ke Services Hub.

2.  Navigasikan ke Tab Penilaian lalu klik Penilaian.

![Gambar Memulai KB Kesehatan 1](getting_started_with_on_demand_assessments/GettingStarted1.1.png)

3.  Klik tombol Penilaian Prakonfigurasi.

![Gambar Memulai KB Kesehatan 2](getting_started_with_on_demand_assessments/GettingStarted1.2.jpg)

#### <a name="selecting-your-azure-subscription"></a>Memilih Langganan Azure Anda

Ada tiga skenario alur kerja terhubung yang memungkinkan. Setiap skenario ditentukan oleh langganan Azure perusahaan Anda dan peran yang Anda tetapkan dalam langganan Azure.

### <a name="scenario-1"></a>Skenario 1

#### <a name="owner-of-the-azure-subscription-for-your-organization-will-see"></a>Pemilik Langganan Azure untuk Organisasi Anda akan melihat:

![Gambar Memulai KB Kesehatan 3](getting_started_with_on_demand_assessments/GettingStarted1.3.png)


### <a name="scenario-2"></a>Skenario 2

Organisasi yang memiliki langganan Azure tetapi bukan pemilik langganan Azure akan melihat:

![Gambar Memulai KB Kesehatan 4](getting_started_with_on_demand_assessments/GettingStarted1.4.png)

Mengurus dengan Admin Layanan perusahaan Anda, TAM, atau Koordinator Akun Dukungan untuk mengupayakan pemilik langganan Azure melakukan prakonfigurasi penilaian Anda.

### <a name="scenario-3"></a>Skenario 3

Organisasi tanpa langganan Azure, pengunjung akan melihat:

![Gambar Memulai KB Kesehatan 5](getting_started_with_on_demand_assessments/GettingStarted1.5.jpg)

Klik **Dapatkan Langganan Azure** untuk mendapatkan langganan yang disponsori Microsoft.

Untuk mempelajari lebih lanjut tentang privasi Azure, kunjungi <a href="https://www.microsoft.com/en-us/trustcenter" target="_blank">Pusat Kepercayaan Microsoft</a>.

## <a name="connecting-an-azure-account-with-azure-log-analytics"></a>Menghubungkan Akun Azure dengan Azure Log Analytics

Memilih ruang kerja <a href="https://mms.microsoft.com/Account?returnUrl=%2F" target="_blank">Azure Log Analytics organisasi Anda</a> dari menu daftar menurun.  Jika tidak memiliki ruang kerja, klik **Buat Baru** untuk membuatnya dan selesaikan tahap-tahap berikut:

1.  Beri nama ruang kerja Azure Log Analytics Anda - nama harus unik.

2.  Pilih grup Sumber Daya Azure. Jika tidak punya, Anda dapat membuatnya.

3.  Pilih wilayah yang paling sesuai dengan lokasi Anda dan setelah Anda meninjau perjanjian berlangganan, rincian penawaran, dan pernyataan privasi Anda dapat mencentang kotak untuk menyetujui. Setelah pilihan Anda dibuat, klik Kirim.

*Catatan: Setelah memilih ruang kerja, Anda dapat melakukan perubahan kapan saja dengan menavigasi ke Edit Ruang Kerja Analitik Log Azure di bawah nama Anda di Hub Layanan.*

![Gambar Memulai KB Kesehatan 6](getting_started_with_on_demand_assessments/GettingStarted1.6.png)

4.  Setelah mengeklik Kirim, Anda akan melihat halaman konfirmasi.

5.  Klik bilah biru berlabel **Klik di sini** to navigate to your assessments untuk menavigasi ke dasbor Azure Log Analytics lalu memulai konfigurasi penilaian Anda.


## <a name="configuring-an-assessment-in-azure-log-analytics"></a>Mengonfigurasi Penilaian di Analitik Log Azure

Setelah menautkan Services Hub Anda ke <a href="https://asd-westus-public.portal.mms.microsoft.com/#Workspace/overview/" target="_blank">Ruang Kerja Azure Log Analytics</a>, Anda dapat mulai mengonfigurasi penilaian atas permintaan Anda.

*Catatan: Hanya pengguna yang telah diberi akses Analitik Log Azure melalui portal Azure yang dapat melihat dasbor ini.*

*Catatan: Penilaian ini bersifat khusus bagi pengguna Hub Layanan dan akan memberikan wawasan mendetail serta memungkinkan Anda memecahkan masalah rekomendasi prioritas dan menangani masalah secara proaktif.*

1.  Klik **Paket Solusi Dukungan Microsoft Unified** untuk melihat daftar solusi yang tersedia.

2.  Klik **Tambahkan untuk penilaian mana saja** di Microsoft Unified Support Solutions Pack.

3.  Klik **Tambahkan** untuk melihat halaman konfigurasi dengan instruksi untuk menyiapkan dan mengonfigurasi penilaian

![Gambar Memulai KB Kesehatan 7](getting_started_with_on_demand_assessments/GettingStarted1.7.jpg)

## <a name="setting-up-an-assessment"></a>Menyiapkan Penilaian

1.  Unduh kedua dokumen dari halaman konfigurasi (Prasyarat untuk Penilaian dan Menyiapkan Penilaian). Dokumen-dokumen ini menjelaskan persyaratan sistem dan cara menginstal Microsoft Management Agent dan Gateway Azure Log Analytics.

*Catatan: Halaman dan dokumen konfigurasi ini hanya tersedia dalam jenis solusi Penilaian. Tidak semua Solusi dalam daftar memiliki halaman konfigurasi yang tersedia.*

2.  Ada dua skenario yang tersedia untuk mengonfigurasi penilaian. Menentukan terlebih dahulu mana yang terbaik untuk organisasi Anda:

    A. Gateway Azure Log Analytics dan Mesin Pengumpulan Data: Skenario ini memerlukan dua komputer dan merupakan opsi yang paling aman dan pilihan yang direkomendasikan untuk membantu melindungi kredensial akun istimewa yang digunakan pada tugas terjadwal yang terkonfigurasi pada mesin pengumpulan data. Satu komputer ditunjuk sebagai mesin pengumpulan data, dan komputer kedua adalah Gateway Azure Log Analytics. Dalam skenario ini, mesin pengumpulan data tidak memiliki koneksi Internet dan terhubung ke Gateway Azure Log Analytics untuk mengunggah data ke Azure Log Analytics. Azure Log Analytics Gateway harus memiliki akses Internet. Skenario ini direkomendasikan untuk lingkungan di mana koneksi Internet dibatasi dari mesin pengumpulan data atau di mana keamanan menjadi perhatian karena konfigurasi tugas terjadwal.
    
    
    B. Khusus Mesin Pengumpulan Data: Skenario ini dapat digunakan ketika mesin pengumpulan data dapat menghubungi Analitik Log Azure secara langsung. Diperlukan satu komputer yang akan ditetapkan sebagai mesin pengumpulan data dan membutuhkan akses Internet untuk mengunggah data ke Azure Log Analytics. Mesin pengumpulan data harus menjadi anggota domain atau hutan lingkungan yang sedang dinilai dan akan mengumpulkan data dari semua server pilihan Anda di lingkungan tersebut untuk menjalankan penilaian. Setelah data terkumpul, mesin pengumpulan data akan menganalisis informasi lalu mengunggah data ke Azure Log Analytics secara langsung; hal ini memerlukan sambungan HTTPS ke ruang kerja langganan Azure Log Analytics Anda.

## <a name="services-hub-assessment-page"></a>Halaman Penilaian Services Hub

Setelah menautkan Services Hub Anda ke ruang kerja Azure Log Analytics, dan mengonfigurasikan penilaian, Anda dapat melihat semua informasi penilaian Anda dari Services Hub. Untuk melihat halaman penilaian pribadi Anda, pilih Kesehatan dari navigasi utama, lalu klik Penilaian. Di sini Anda akan menemukan semua penilaian terkonfigurasi dengan data tingkat teratas yang diambil dari Azure Log Analytics.

<i>Catatan: Hanya pengguna dengan akses Azure Log Analytics yang akan dapat melihat data penilaian saat menjalankan aturan keamanan yang berlaku untuk Azure Log Analytics. Untuk akses, hubungi pemilik Azure di organisasi Anda. Penilaian yang tersedia dalam contoh di atas memiliki bilah gulir di bawahnya; gunakan untuk melihat Penilaian Tambahan yang tidak ditampilkan.</i>

1.  Klik pada setiap Penilaian untuk melihat hasil.

2.  Klik **Lihat di Azure Log Analytics** di sebelah kanan rekomendasi untuk meninjau rincian lengkap rekomendasi.


## <a name="additional-azure-log-analytics-information"></a>Informasi Azure Log Analytics Tambahan

Area Fokus Situs Analitik Log Azure: Wawasan dan Analitik: Dapatkan wawasan cepat tentang beban kerja

-   <a href="https://www.microsoft.com/en-us/cloud-platform/insight-and-analytics" target="_blank">Video Gambaran Umum</a>

-   <a href="https://oms.cloudguides.com/en-US/guides/Gaining%20insights%20with%20Microsoft%20Operations%20Management%20Suite" target="_blank">Mendapatkan wawasan dengan Analitik Log Microsoft Azure</a>

Area Fokus Situs Analitik Log Azure: Keamanan dan Kepatuhan: Merespons ancaman keamanan secara lebih cepat

-   <a href="https://www.microsoft.com/en-us/cloud-platform/security-and-compliance" target="_blank">Video Gambaran Umum</a>

-   <a href="https://oms.cloudguides.com/en-US/guides/Managing%20security%20and%20compliance%20with%20Microsoft%20Operations%20Management%20Suite" target="_blank">Mengelola keamanan dan kepatuhan dengan Analitik Log Microsoft Azure</a>

Area Fokus Situs Analitik Log Azure: Automasi dan Kontrol: Memungkinkan kontrol dan kepatuhan yang konsisten

-   <a href="https://www.microsoft.com/en-us/cloud-platform/automation-and-control" target="_blank">Video Gambaran Umum</a>

-   <a href="https://oms.cloudguides.com/en-US/Guides/Automation%20and%20configuration%20in%20Microsoft%20Operations%20Management%20Suite" target="_blank">Panduan demo</a>

Area Fokus Situs Analitik Log Azure: Perlindungan dan Pemulihan: Memastikan ketersediaan aplikasi dan data

-   <a href="https://www.microsoft.com/en-us/cloud-platform/protection-and-recovery" target="_blank">Video Gambaran Umum</a>

<br>

Klik <a href="mailto:SHub_Feedback_RC@Microsoft.com?subject=Resource%20Center%20Feedback%3A%20%3CInsert%20feedback%20topic%3E%3E&amp;body=%3C%3Cplease%20submit%20your%20feedback%20with%20enough%20detail%20on%20the%20problem%2C%20reproduction%20steps%20and%20what%20you%20desire%20to%20happen%3E%3E" target="_blank">di sini</a> untuk memberikan umpan balik.
