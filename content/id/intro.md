Pengantar
============

Di era modern, perangkat lunak umumnya disampaikan sebagai layanan (services): sebut saja *web apps*, atau *software-as-a-service*.  App dengan twelve-factor adalah sebuah methodology untuk membangun app software-as-a-service yang:

* Menggunakan format **declarative** untuk otomatisasi persiapan (setup automation), untuk meminimalisasi waktu dan biaya bagi pengembang baru yang bergabung dalam proyek;
* Memiliki **clean contract** dengan sistem operasi yang mendasarinya, menawarkan **portabilitas maksimum** antara lingkungan eksekusi;
* Sesuai untuk **deployment** pada **platfom awan** yang modern, Mengabaikan kebutuhan akan server dan administrasi sistem;
* **Minimalkan perbedaan** antara pengembangan dan produksi, memungkinkan penyebaran berkelanjutan (**continuous deployment**) untuk ketangkasan maksimal;
* Dan dapat **meningkatkan skala** tanpa perubahan signifikan pada perkakas, arsitektur, atau praktik pengembangan.

Metodology **twelve-factor** dapat diterapkan pada aplikasi yang ditulis dalam bahasa pemrograman apapun, dan yang menggunakan kombinasi layanan pendukung (database, antrian, cache memori, dll).
