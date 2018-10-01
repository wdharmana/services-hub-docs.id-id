# <a name="azure-roles-for-log-analytics-and-how-they-relate-to-the-services-hub"></a>Peran Azure untuk Analitik Log dan Hubungannya terhadap Hub Layanan
 
Akun Anda di Hub Layanan akan ditautkan ke akun Analitik Log Azure.

## <a name="purpose-of-linking"></a>Tujuan penautan:

- Penilaian Unified Sesuai Permintaan di akun Analitik Log Azure hanya akan diaktifkan jika seseorang menautkan ruang kerja Services Hub (yang digunakan saat masuk ke Services Hub) dengan akun Analitik Log Azure miliknya. 

- Penilaian Unified Sesuai Permintaan tersedia bagi ruang kerja yang telah diaktifkan secara khusus pada saat proses penautan (penautan antara Services Hub dan akun Analitik Log Azure).

- Proses penautan akan mengaktifkan Penilaian Terpadu Sesuai Permintaan di ruang kerja Analitik Log Azure yang sedang ditautkan (dihubungkan).

- Hanya pemegang peran tertentu di Azure yang dapat menautkan dari Services Hub ke Analitik Log Azure atau ruang kerja Analitik Log Azure. Akun pengguna yang sudah masuk ke Hub Layanan akan melakukan pengeditan tersebut di Analitik Log Azure.

## <a name="azure-roles"></a>Peran Azure
Berikut adalah berbagai peran Azure beserta izin yang dimilikinya dalam Services Hub terkait dengan penilaian dan penautan Hub Layanan ke Analitik Log.

### <a name="the-following-users-can-link-your-existing-azure-log-analytics-workspaces-to-services-hub-workspace"></a>Pengguna berikut ini dapat menautkan ruang kerja Analitik Log Azure Anda yang sudah ada ke ruang kerja Hub Layanan:
- Pemilik Azure
- Kontributor Azure
- Kontributor Analitik Log Azure

### <a name="the-following-users-can-create-new-azure-log-analytics-workspace-that-are-linked-to-services-hub-workspace"></a>Pengguna berikut ini dapat membuat ruang kerja Analitik Log Azure baru yang ditautkan ke ruang kerja Hub Layanan:
- Pemilik Azure
- Kontributor Azure
- Kontributor Analitik Log Azure

### <a name="the-following-roles-can-addremove-solutions-from-azure-log-analytics"></a>Peran berikut ini dapat Menambahkan/Menghapus solusi dari Analitik Log Azure:
- Pemilik Azure
- Kontributor Azure
- Kontributor Analitik Log Azure

### <a name="the-following-roles-can-manage-user-access-for-azure-log-analytics"></a>Peran berikut ini dapat mengelola akses pengguna untuk Analitik Log Azure:
- Pemilik Azure
- Administrator Akses Pengguna Azure

### <a name="the-following-users-can-configure-the-assessments-from-azure-log-analytics-workspace"></a>Pengguna berikut ini dapat mengonfigurasi penilaian dari ruang kerja Analitik Log Azure:
- Pemilik Azure
- Kontributor Azure
- Kontributor untuk sumber daya ruang kerja Analitik Log Azure (lingkup ditetapkan sebatas sumber daya Analitik Log sehingga peran hanya diterapkan pada sumber daya tertentu dan tidak memiliki penetapan izin di luar ruang kerja.)
 
T: Bagaimana cara mengonfigurasi peran di Azure?

J: <a href="https://docs.microsoft.com/en-us/azure/active-directory/role-based-access-control-configure" target="_blank">https://docs.microsoft.com/en-us/azure/active-directory/role-based-access-control-configure</a>


| Peran                                                 | Tindakan                                 |                                           |                                         |                 |                 |                |                   |                  |                                  |
|-------------------------------------------------------|-----------------------------------------|-------------------------------------------|-----------------------------------------|-----------------|-----------------|----------------|-------------------|------------------|----------------------------------|
|                                                       | Menautkan Ruang Kerja yang Ada ke Hub Layanan | Membuat dan Menautkan ruang kerja di Hub layanan | Mengakses ruang kerja pada Analitik Log Azure | Mencari menggunakan V1 | Mencari menggunakan V2 | Menambahkan solusi | Menghapus solusi | Menambahkan/Menghapus pengguna | Melihat Kunci konfigurasi ruang kerja |
| Pemilik Azure                                           | X                                       | X                                         | X                                       | X               | X               | X              | X                 | X                | X                                |
| Kontributor Azure                                     | X                                       | X                                         | X                                       | X               | X               | X              | X                 |                  | X                                |
| Pembaca Azure                                          |                                         |                                           | X                                       | X               | X               |                |                   |                  |                                  |
| Kontributor Analitik Log Azure                       | X                                       | X                                         | X                                       | X               | X               | X              | X                 |                  |                                  |
| Pembaca Analitik Log Azure                            |                                         |                                           | X                                       | X               | X               |                |                   |                  |                                  |
| Admin Akses Pengguna Azure                               |                                         |                                           | X                                       | X               | X               |                |                   | X                |                                  |
| Kontributor Analitik Log Azure + CLA*                | X                                       | X                                         | X                                       | X               | X               | X              | X                 |                  | X                                |
| Pembaca Analitik Log Azure + CLA                      |                                         |                                           | X                                       | X               | X               |                |                   |                  | X                                |
| CLA                                                   |                                         |                                           | X                                       | X               | X               |                |                   |                  | X                                |
| *CLA = Kontributor untuk Sumber Daya Analitik Log tertentu |                                         |                                           |                                         |                 |                 |                |                   |                  |                                  |

Klik <a href="mailto:SHub_Feedback_RC@Microsoft.com?subject=Resource%20Center%20Feedback%3A%20%3CInsert%20feedback%20topic%3E%3E&amp;body=%3C%3Cplease%20submit%20your%20feedback%20with%20enough%20detail%20on%20the%20problem%2C%20reproduction%20steps%20and%20what%20you%20desire%20to%20happen%3E%3E" target="_blank">di sini</a> untuk memberikan umpan balik.
