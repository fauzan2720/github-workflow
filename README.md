# github-workflow
Repository ini dibuat untuk memenuhi tugas literasi digital terkait Github Workflow

Pertama yang saya lakukan adalah membuat repository pada github saya.
Ketika berhasil membuat repository, saya membuat file dengan nama main.html.

## Clone repository dan melakukan perubahan file

*Semua pekerjaan saya menggunakan Git Bash*

Saya akan melakukan clone repository dengan perintah:
``git clone https://github.com/fauzan2720/github-workflow.git``

Setelah berhasil, kita masuk ke folder repository hasil clone dengan perintah:
``cd github-workflow``

Jika berhasil maka akan ada tulisan (main) berwarna hijau tosca disebelah kanan nama folder. (main) berarti kita sedang berada di branch main.
Selanjutnya saya akan melakukan perubahan pada file main.html.
Yang semula
``<h1>Ini adalah file dari branch main</h1>``
menjadi
``<h1>Ini adalah file dari branch main</h1>``
``<p>Ini adalah perubahan pada file main.html</p>``

Jika sudah, saya akan mengupload ke repositry, langkah pertama adalah melakukan perintah git add untuk menambahkan file perubahan ke list yang akan di commit. Ketik perintah:
``git add .``
Tanda (.) berarti akan mendeteksi seluruh file yang mengalami perubahan.

Setelah berhasil, saya melakukan commit dengan perintah:
``git commit -m "ini adalah commit dari branch main"``

Setelah itu saya melakukan push origin dengan perintah:
``git push -u origin main``

## Buat branch baru dan menggabungkan (merge) file ke branch main

Pertama saya membuat branch baru dengan nama branch master. Melakukan dengan perintah:
``git checkout -b master``
Jika berhasil, maka pada git bash yang semula (main) akan berubah menjadi (master)

Dan saya akan membuat file ke dalam branch master, dengan nama file master.html, dengan isi:
``<h1>Ini adalah file dari branch master</h1>``

Setelah itu lakukan cara yang sama seperti diatas untuk mengupload ke repository.
``git add .``
``git commit -m "ini adalah commit dari branch master"``
``git push -u origin master``

Selanjutnya saya akan menggabungkan file dari branch master ke branch main. Pertama kita beralih dulu ke branch main dengan perintah:
``git checkout main``
Sampai (master) berubah menjadi (main) pada git bash.

Lalu gabungkan file dengan perintah:
``git merge origin/master``
``git add .``
``git commit -m "ini adalah commit merge file dari branch master ke branch main"``
``git push -u origin main``

Terakhir saya akan merilis branch, yang artinya setiap file yang sudah fix akan saya masukkan ke branch release ini.
Lakukan dengan perintah:
``git checkout -b release/v1.0.0`` (membuat branch rilis)
``git add .``
``git commit -m "fix v1.0.0"``
``git push -u origin release/v1.0.0``

## Author

E41201367 - Fauzan Abdillah - Golongan C - Politeknik Negeri Jember
