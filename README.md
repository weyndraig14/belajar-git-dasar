GIT DASAR  

1) Poin utama :
   
   A. Apa itu git?
   
      Git adalah sebuah sistem kontrol versi yang sangat populer dan kuat yang digunakan oleh pengembang perangkat lunak untuk mengelola perubahan dalam kode sumber proyek, Dikembangkan oleh Linus Torvalds pada tahun 2005, Git dirancang untuk menjadi cepat, efisien, dan mudah digunakan, serta mendukung pekerjaan tim yang terdistribusi.

   B. Cara Kerja git

         a) Cara membuat repository git
 
           1. Repositori git dapat diinisialisasi di dalam folder proyek yang sudah ada, baik yang kosong maupun yang    berisi file. Untuk menginisialisasi repositori, gunakan perintah "git init" di dalam terminal/git bash.
           
           2. Setelah inisialisasi, sebuah folder baru bernama .git akan dibuat untuk menyimpan data repositori. Hindari memodifikasi konten folder ini.
           
           4. Git mengikuti alur kerja tiga langkah: modified, staged, dan committed. File dimodifikasi di working directory, staging untuk commit, lalu dicommit ke repositori.
           
           5. Git menggunakan penunjuk yang disebut "head" untuk menunjukkan commit terakhir dalam repositori.
           
           6. Setelah perubahan dicommit, tidak ada cara langsung untuk membatalkannya, pilihannya seperti rollback, reset, atau revert, masing-masing dengan implikasi yang berbeda.
  
           7. Mengganti nama file di Git dapat dideteksi sebagai operasi penghapusan dan penambahan. Git mendeteksi kemiripan dalam konten file untuk mengidentifikasi penggantian nama secara akurat.

         b) Code git dasar
       
           1. Gunakan "git status" untuk memeriksa perubahan dalam repositori, seperti file baru, file yang dimodifikasi, atau file yang dihapus.
           
           2. Untuk menambahkan perubahan secara permanen ke repository Git, gunakan perintah "git commit" setelah melakukan perubahan.
           
           3. Git menyediakan perintah seperti "git diff" untuk melihat perubahan yang dibuat pada berkas di repositori.
           
           4. Perubahan pada beberapa file dapat dilakukan dengan menggunakan "git add" sebelum melakukan commit.
           
           5. Penghapusan dan penambahan file dapat dilacak menggunakan "git status" dan dikelola dengan "git add" dan "git commit".
           
           6. Membatalkan perubahan dapat dilakukan dengan "git restore" untuk modifikasi atau penghapusan yang dilakukan di working directory.
  
           7. Untuk membatalkan perubahan yang staging untuk commit, "git restore --staged" dapat digunakan untuk memindahkan perubahan kembali ke working directory.

         c) Git log 

           1. Git memungkinkan Anda untuk melihat riwayat commit menggunakan perintah "git log".
           
           2. Perintah "git log" menampilkan detail commit seperti penulis, tanggal, dan pesan.
           
           3. Untuk menyederhanakan output "git log", Anda dapat menggunakan opsi "--oneline" untuk menampilkan satu commit per baris.
  
           4. Membandingkan commit di Git berfokus pada status akhir file daripada perubahan individual.
           
           5. Perintah "git diff" membandingkan perbedaan antara komit atau cabang.

         d) Reset commit

           1. Menggunakan "git reset" dengan opsi "--soft" memindahkan penunjuk HEAD ke commit yang berbeda tanpa mengubah staging index dan working directory, menjadikannya opsi yang aman untuk membatalkan komit.
          
           2. "git reset" dengan opsi "--mixed" memindahkan penunjuk HEAD dan mengatur ulang staging index ke commit yang ditentukan sambil mempertahankan perubahan di working directory, sehingga memungkinkan penyesuaian lebih lanjut sebelum melakukan commit.
          
           3. "git reset" dengan opsi "--hard" mereset penunjuk HEAD, staging index, dan working directory ke commit yang ditentukan, secara efektif menghapus semua perubahan, menjadikannya opsi yang paling merusak.
          
           4. Setelah operasi reset, perubahan dapat dipulihkan jika commit baru belum dibuat, tetapi membuat commit baru akan menggantikan riwayat commit, membuat perubahan tidak dapat dipulihkan.
          
           5. Mengatur ulang commit dapat berguna untuk memperbaiki kesalahan atau menambahkan perubahan yang terlupakan sebelum membuat commit baru.

         e) Amend commit

           1. Git menyediakan perintah "git commit --amend" untuk menambahkan perubahan secara otomatis pada snapshot terakhir, menggabungkannya dengan perubahan pada commit sebelumnya.
          
           2. Menggunakan "git commit --amend" memungkinkan untuk menambahkan perubahan pada commit sebelumnya tanpa membuat commit baru, menyederhanakan prosesnya dibandingkan dengan mengatur ulang dan melakukan commit ulang.
          
           3. Ketika menggunakan "git commit --amend", bahkan menambahkan satu karakter pun akan secara otomatis mengubah konten dan tanda tangan snapshot.
         
         f) Git checkout

           1. Dengan menggunakan "git checkout" untuk menavigasi ke commit tertentu, perubahan pada berkas dapat dilakukan secara bertahap, sehingga memungkinkan pemeriksaan tanpa mengubah repositori secara permanen.
          
           2. "git checkout" dengan nama branch memungkinkan untuk berpindah di antara branch-branch yang berbeda di repositori. Untuk menavigasi ke commit tertentu, "git checkout" diikuti dengan hash commit atau nama branch yang dapat digunakan.
          
           3. Perintah "git checkout" seperti mesin waktu, memungkinkan pengguna untuk berpindah-pindah di antara snapshot yang berbeda dalam riwayat repositori.

         g) Git revert

           1. Fitur "git revert" dari Git memungkinkan untuk membatalkan commit sebelumnya dengan membuat commit baru dengan perubahan yang berlawanan dengan perubahan yang dikembalikan.
          
           2. Tidak seperti reset, git revert tidak menghapus riwayat tetapi membuat commit baru yang membalikkan perubahan yang dibuat oleh commit sebelumnya.
          
           3. Ketika menggunakan Git, perintah "git revert" dapat secara otomatis membatalkan perubahan yang dibuat pada commit tertentu, membuat commit baru dengan perubahan yang berlawanan.
         
         h) .gitignore

           1. File .gitignore memungkinkan Anda menentukan file atau directory mana yang harus diabaikan oleh Git, berguna untuk mengecualikan file yang dibuat, log, atau jenis file tertentu dari kontrol versi.

         i) Git blame

           1. Perintah "git blame" Git membantu melacak siapa yang membuat perubahan pada sebuah file dan kapan, memberikan tampilan terperinci tentang kepengarangan setiap baris dan komit terkait.

2) Catatan tambahan
   
   a. Git sangat berguna untuk pekerjaan dalam sebuah tim dan sangat feleksibel karena ketika kita berganti device kita    tidak perlu khawatir dengan projeck kita, karena sudah tersimpan aman.

3) Kesimpulan

   GIT adalah alat yang sangat penting dan bermanfaat bagi pengembang perangkat lunak untuk mengelola 
proyek mereka dengan efisien. Dengan kemampuannya yang kuat dalam version control, kolaborasi, dan branching, GIT sangat membantu dalam proses pengembangan perangkat lunak yang kompleks.

 
 
   
