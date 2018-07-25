# <a name="troubleshooting-mma-agent-configuration-with-ssl-proxy"></a>Memecahkan Masalah Konfigurasi Agen MMA dengan Proksi SSL
 
## <a name="problem-description"></a>Deskripsi masalah

Anda mungkin menjumpai pesan kesalahan ini dalam panduan penyiapan Agen Pengawasan Microsoft.

![Cuplikan layar kesalahan](health-kb-mmaagent-1.png)

Selain itu, file MonitoringAgent.log mungkin berisi pesan serupa

> Menolak sertifikat CN=YYYYY.azure.com karena tidak terkait dengan akar yang tepercaya, akar yang sebenarnya adalah CN=XXXX, OU=XXXX, O=XXXX 2018-03-06T15:45:21.1858236-06:00 Debug: Gagal mempercayai sertifikat jarak jauh: Koneksi yang mendasari telah ditutup: Tidak dapat membangun hubungan yang tepercaya untuk saluran aman SSL/TLS.
 
## <a name="possible-cause"></a>Kemungkinan penyebab

Masalah ini kemungkinan disebabkan oleh adanya kehadiran dalam jaringan perangkat (atau proksi yang mengganggu) yang melakukan pemeriksaan HTTP pada lalu lintas web.

Untuk informasi tambahan: Pemeriksaan HTTPS dan PKI Anda: https://blogs.technet.microsoft.com/crypto/2016/01/27/https-inspection-and-your-pki-2/ 

  
## <a name="resolution"></a>Resolusi

Untuk menyelesaikan masalah, lewati pemeriksaan HTTP pada perangkat untuk URL berikut

| Sumber daya                   | Nomor port | Lewati Pemeriksaan HTTP |
|----------------------------|-------------|------------------------|
| Agen                      |             |                        |
| *.ods.opinsights.azure.com | 443         | Ya                    |
| *.oms.opinsights.azure.com | 443         | Ya                    |
| *.blob.core.windows.net    | 443         | Ya                    |
| *.azure-automation.net     | 443         | Ya                    |

Seperti yang dijelaskan sebagai persyaratan Analitik Log Azure dalam artikel berikut

> Sambungkan Manajer Operasi ke Analitik Log – Persyaratan sistem: https://docs.microsoft.com/en-us/azure/log-analytics/log-analytics-om-agents#system-requirements

Klik <a href="mailto:SHub_Feedback_RC@Microsoft.com?subject=Resource%20Center%20Feedback%3A%20%3CInsert%20feedback%20topic%3E%3E&amp;body=%3C%3Cplease%20submit%20your%20feedback%20with%20enough%20detail%20on%20the%20problem%2C%20reproduction%20steps%20and%20what%20you%20desire%20to%20happen%3E%3E" target="_blank">di sini</a> untuk memberikan umpan balik.
