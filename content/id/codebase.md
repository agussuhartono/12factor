## I. Codebase
### Satu basis kode dilacak dalam kontrol revisi, banyak penyebaran

Aplikasi 'twelve-factor' selalu dilacak dalam sistem kontrol versi, seperti [Git](http://git-scm.com/), [Mercurial](https://www.mercurial-scm.org/), atau [Subversion](http://subversion.apache.org/). Salinan database pelacakan revisi dikenal sebagai *code repository* (repositori kode), sering disingkat *code repo* atau hanya *repo* saja.

Sebuah *codebase* merupakan repo tunggal (di dalam sistem kontrol revisi terpusat seperti Subversion), atau setiap set repos yang berbagi komit akar (dalam sebuah sistem kontrol revisi terdesentralisasi seperti Git).

![Satu basis kode (codebase) dipetakan ke banyak pengerahan (deploy)](/images/codebase-deploys.png)

Selalu ada korelasi satu-ke-satu antara basis kode (codebase) dan aplikasi:

* Jika ada beberapa codebases, bukan sebuah app -- ia sistem terdistribusi. Setiap komponen dalam sistem terdistribusi adalah aplikasi, dan masing-masing dapat secara individual mematuhi dua belas faktor (twelve-factor).
* Beberapa aplikasi yang berbagi kode yang sama adalah pelanggaran terhadap dua belas faktor (twelve-factor).  Solusinya disini adalah berbagi kode bersama ke dalam perpustakaan yang bisa disertakan melalui [pengelola ketergantungan (dependency manager)](./dependencies).

Hanya ada satu basis kode (codebase) per aplikasi, tapi akan ada banyak penyebaran aplikasi.  Sebuah pengerahan (*deploy*) adalah menjalankan instan dari aplikasi.  Ini biasanya merupakan situs produksi, dan satu atau beberapa situs pementasan.  Selain itu, setiap pengembang memiliki salinan aplikasi yang berjalan di lingkungan pengembangan lokal mereka, masing-masing yang juga memenuhi syarat sebagai pengerahan (_deploy_).

Basis kode sama di semua tempat pengerahan, meskipun versi yang berbeda mungkin aktif di setiap tempat pengerahan (deploy).  Sebagai contoh, seorang pengembang memiliki beberapa komitmen yang belum dikirim ke pementasan; pementasan memiliki beberapa komitmen yang belum dikerahkan untuk produksi. Tapi mereka semua berbagi basis kode yang sama, sehingga membuat mereka dikenali sebagai pengerahan yang berbeda dari aplikasi yang sama.

