# <a name="data-does-not-appear-in-azure-log-analytics-due-to-profile"></a>Data Tidak Muncul dalam Analitik Log Azure karena Profil


## <a name="symptoms"></a>Gejala

### <a name="issue-data-does-not-appear-in-azure-log-analytics-due-to-profile-related-data-collection-problem"></a>Masalah: Data tidak muncul dalam Analitik Log Azure karena masalah pengumpulan data terkait profil

-   Dalam beberapa konfigurasi, pengumpulan data penilaian Analitik Log Azure akan gagal karena cara penanganan profil pengguna di windows.

-   Tugas terjadwal milik penilaian tersebut memang berhasil dilakukan, tetapi data masalah tidak muncul di ruang kerja Analitik Log Azure.

-   Log pelaksanaan dan/atau penemuan penilaian berisi pesan "Upaya operasi ilegal telah dilakukan pada kunci registri yang ditandai untuk penghapusan."

 
## <a name="cause"></a>Penyebab

Windows mungkin membongkar penampung registri pengguna ketika digunakan oleh aplikasi klien penilaian.

 
## <a name="resolution"></a>Resolusi

Ubah pengaturan berikut ini dalam editor kebijakan grup (gpedit.msc) dari \"tidak dikonfigurasi\" menjadi \"diaktifkan\" 

Lokasi: Konfigurasi Komputer-\>Templat Administratif-\>Sistem-\> Profil Pengguna

Jangan membongkar registri pengguna secara paksa pada log keluar pengguna.

Tinjau artikel berikut ini untuk instruksi mendetail: [https://support.microsoft.com/en-us/help/2287297/a-com-application-may-stop-working-on-windows-server-2008-when-a-user](https://support.microsoft.com/en-us/help/2287297/a-com-application-may-stop-working-on-windows-server-2008-when-a-user)

## <a name="more-information"></a>Informasi Selengkapnya

Masalah ini terkait dengan cara PowerShell jarak jauh dimulai dan hanya akan memengaruhi tipe penilaian tertentu ketika pengguna yang dikonfigurasi tidak masuk saat pelaksanaan tugas.

Masalah ini merupakan salah satu penyebab utama terhentinya unggahan data penilaian secara tiba-tiba. Pengguna admin masuk untuk pelaksanaan pertama yang dijadwalkan 1 jam dari penginstalan. Seiring waktu, akun tersebut kemudian keluar atau mesin dinyalakan ulang sehingga pelaksanaan berikutnya gagal tanpa diketahui.


Klik <a href="mailto:SHub_Feedback_RC@Microsoft.com?subject=Resource%20Center%20Feedback%3A%20%3CInsert%20feedback%20topic%3E%3E&amp;body=%3C%3Cplease%20submit%20your%20feedback%20with%20enough%20detail%20on%20the%20problem%2C%20reproduction%20steps%20and%20what%20you%20desire%20to%20happen%3E%3E" target="_blank">di sini</a> untuk memberikan umpan balik.
