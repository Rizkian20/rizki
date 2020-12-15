#Git Is Good
Category:forensic

Setelah download file dari challenge dari     https://mega.nz/#!C483DAYB!Jjr55hfJQJ5-jspnyrnVtqBkMHGJrd6Nn_QqM7iXEuc kita dapat mengetahui bahwa file tersebut berbentuk zip.

Dari judul challenge sudah diberikan clue bahwa untuk menyelesaikan challenge ini menggunakan git. Download git terlebih dahulu menggunakan terminal "apt-get install git"
Langkah pertama ekstrak file menggunakan command "unzip gitIsGood.zip"

![Step 1](https://github.com/Rizkian20/rizki/blob/main/Git%20Is%20Good/1.png)

Selanjutnya yaitu masuk ke file tadi "cd gitIsGood" lalu lihat di dalam tersebut isinya apa saja dengan command "ls -al"

![Step 2](https://github.com/Rizkian20/rizki/blob/main/Git%20Is%20Good/2.png)

Jika dilihat terdapat file dengan nama "flag.txt" dan 1 folder .git, lalu kita coba baca dengan command "cat flag.txt".Namun hasilnya menunjukkan bahwa file telah disunting, berarti terdapat perubahan file (dapat dilihat pada gambar 2).
Langkah selanjutnya yaitu melihat history perubahan dari file tersebut dengan command "git log"

![Step 3](https://github.com/Rizkian20/rizki/blob/main/Git%20Is%20Good/3.png)

Dari gambar di atas menunjukkan bahwa file telah diedit sebanyak 3 kali, untuk melihat detailnya gunakan command "git log -p"

![Step 4](https://github.com/Rizkian20/rizki/blob/main/Git%20Is%20Good/4.png)

Hasilnya dapat kita temukan flag yaitu :
flag : flag{protect_your_git}
