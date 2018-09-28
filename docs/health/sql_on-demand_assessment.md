# <a name="setting-up-a-sql-on-demand-assessment"></a>Menyiapkan Penilaian Sesuai Permintaan SQL

1.  Dari dasbor Services Hub, klik **Kesehatan**, lalu **Penilaian**.

2.  Gulir ke bawah untuk mengakses bagian Penilaian Sesuai Permintaan yang Tersedia, lalu klik SQL Server untuk membuka dialog deskripsi Penilaian Sesuai Permintaan. 

3.  Klik **Tambahkan Penilaian** untuk menilai halaman konfigurasi. Baca informasi di halaman ini dengan cermat untuk memahami skenario mana yang dapat digunakan di lingkungan Anda. Unduh dan tinjau dokumen penyiapan dan prasyaratnya.

4.  Untuk memulai, luncurkan prompt perintah Powershell administratif. Dalam prompt perintah, ketikkan Set-SQLAssessment.

5.  Berikutnya, tentukan server SQL mana yang ingin Anda nilai. Untuk kluster failover, berikan nama jaringan virtual kluster failover.

6.  Selanjutnya, tentukan direktori kerja lokal untuk menyimpan data yang dikumpulkan.

7.  Kemudian, berikan nama pengguna akun domain yang merupakan anggota grup Administrator lokal beserta peran SysAdmin pada SQL Server yang sudah dipilih.

8.  Tambahkan kata sandi untuk akun tersebut.

9.  Pada saat ini, perintah akan membuat tugas terjadwal untuk penilaian.

*Catatan: Anda juga dapat meninjau detail log di sini.*

10. Berikutnya, lanjutkan dan tinjau tugas terjadwal yang baru saja dibuat dengan memulai Penjadwal Tugas.

11. Perluas Microsoft dari Pustaka Penjadwal Tugas, lalu pilih Analitik Log Azure, dan klik SQLAssessment untuk melihat tugas terjadwal bagi penilaian tersebut. Secara default, tugas akan dimulai sekitar satu jam dan berulang setiap 7 hari.

12. Klik tab **Tindakan** untuk melihat bahwa tugas memulai perintah dalam direktori kerja Anda.


Klik <a href="mailto:SHub_Feedback_RC@Microsoft.com?subject=Resource%20Center%20Feedback%3A%20%3CInsert%20feedback%20topic%3E%3E&amp;body=%3C%3Cplease%20submit%20your%20feedback%20with%20enough%20detail%20on%20the%20problem%2C%20reproduction%20steps%20and%20what%20you%20desire%20to%20happen%3E%3E" target="_blank">di sini</a> untuk memberikan umpan balik.
