# Domain Aktual: hackathonmerdeka.id

Jadi, situs mikro untuk *hackathon* pertama Code4Nation dipelihara oleh @sabarr
dan rekan-rekannya di Tech in Asia mengunakan Wordpress. Terima kasih banyak!
Mungkin akan ada sedikit "bekas dan jejak" di sana-sini pada proses transisi
ke Github Page ini.

Mohon dicatat bahwa hak cipta dari setiap media yang ada di sini mungkin
masih dimiliki oleh kontributor terkait. Mohon pertanyakan jika ingin
mengadaptasi media tersebut ke tempat lain

## Berkontribusi

Anda bisa berkontribusi banyak hal:

- Membuat [tes untuk static page] ini.
- Memperbaiki kesalahan penulisan kata, seperti misalnya, tapi tidak terbatas
  pada: ejaan yang salah, tanda baca yang salah, dan kesalahan penulisan nama.
- Membuat panduan dan dokumentasi

Pada dasarnya, coba saja kirim PR.

## Menguji di Github.io / Domain Anda

Harap diingat bahwa `github.io` hanya memproses branch `gh-pages`, jadi
pastikan Anda merubah:
- Hapus file `CNAME` di `gh-pages` jika tidak terpakai
- Ubah domain yang ada di file `CNAME` dengan domain Anda jika dipakai
- Ubah isi parameter `url` di file `_config.yml` dengan domain Anda
- Ubah isi parameter `baseurl` dari kosong (`""`) menjadi `"hackathon"` jika anda tidak memakai domain khusus (jad alamatnya adalah `<nama user Anda>.github.io/hackathon` (tentu saja jika mengubah nama repo ini, gunakan nama yang sesuai).
- Jika setelah dicek ada yang rusak, berarti ada `{{ site.baseurl }}` dan/atau `{{ site.url }}` yang lupa ditambahkan. Mohon buat PR dan beritahukan kami di upstream!

## Menguji di Lokal (dan Lingkungan Pengembangan)

Anda mungkin tertarik untuk *mem-fork* repository ini dan mengirimkan PR. Jika
Anda terbiasa menggunakan Github, mungkin hal ini adalah hal yang trivial.
Kami akan beri panduan singkat bagaimana mencoba menampilkan [halaman utama]
di komputer lokal.

**Catatan:** Anda tidak perlu melakukan ini untuk membuat PR, akan tetapi jika
Anda melakukan perubahan yang berkaitan dengan tata letak dan/atau konten dari
situs web statis ini, mungkin Anda ingin melihat hasil pratinjaunya.

**Windows:**

1. Kami menyarankan Anda menggunakan [Rails Installer]. Ikuti petunjuk di sana.
   Setelah selesai, *restart* komputer Anda.
1. Cari `Command Prompt with Ruby and Rails` di Start Menu Anda. Jika Anda
   menggunakan Windows 8 dan/atau Windows 10, Anda dapat menekan tombol
   `Windows + S` kemudian ketikkan `Command Prompt with Ruby and Rails`.
1. `cd` ke tempat Anda *meng-clone* repository ini, kemudian ketikkan

        gem install bundler
        bundle install
        bundle exec jekyll serve

    `bundle install` adalah perintah yang digunakan untuk melakukan instalasi
    segala dependensi yang dibutuhkan untuk melakukan pratinjau di lokal.

    `bundle exec jekyll serve` adalah perintah untuk melakukan halaman pratinjau
    sekaligus melakukan kompilasi dari berkas Markdown ke berkas HTML. Jalankan
    `bundle exec jekyll --help` untuk perintah lengkap.

1. Buka `http://localhost:4000` dari peramban kesayangan Anda.

**Linux dan Mac OS X:**

1. Sebaiknya Anda menggunakan [rvm], sekalipun nantinya Anda hanya menggunakan
   satu versi Ruby. Di halaman depan rvm ada panduan cepat melakukan instalasi
   rvm dengan hanya dua baris perintah.
1. Lakukan instalasi Ruby versi 2.2 ke atas. Untuk saat ini bisa gunakan versi
   2.2.1:

        rvm install 2.2.1
        rvm use ruby-2.2.1

    Catatan: pada beberapa komputer, proses ini lama sekali, bisa setengah jam,
    karena proses ini akan melakukan instalasi dari kode sumber.

1. Fork dan clone repository `Code4Nation/hackathon`, kemudian `cd` ke tempat
   tersebut.

1. Jalankan:

        gem install bundler
        bundle install
        bundle exec jekyll serve

    `bundle install` adalah perintah yang digunakan untuk melakukan instalasi
    segala dependensi yang dibutuhkan untuk melakukan pratinjau di lokal.

    `bundle exec jekyll serve` adalah perintah untuk melakukan halaman pratinjau
    sekaligus melakukan kompilasi dari berkas Markdown ke berkas HTML. Jalankan
    `bundle exec jekyll --help` untuk perintah lengkap.

1. Buka `http://localhost:4000` dari peramban kesayangan Anda.

[tes untuk static page]: https://github.com/blog/1939-how-github-uses-github-to-document-github
[halaman utama]: http://code4nation.github.io/hackathon/
[Rails Installer]: http://railsinstaller.org/en
[rvm]: http://rvm.io
