# Milk's Best Friend

Category : forensic

There's nothing I love more than oreos, lions, and winning. https://mega.nz/#!DC5F2KgR!P8UotyST_6n2iW5BS1yYnum8KnU0-2Amw2nq3UoMq0Y Have Fun :)

![Lihat Gambar](https://github.com/Rizkian20/rizki/blob/main/Milk's%20Best%20Friend/oreo.jpg)

Jika terdapat file gambar pastikan lihat jenis file dengan command "file nama" dan isi string dari file "strings nama"

![Step 1](https://github.com/Rizkian20/rizki/blob/main/Milk's%20Best%20Friend/1.png)

Setelah dicari ternyata file tersebut benar berformat JPEG dan di dalam stringnya hanya tulisan acak dan tidak terdapat flag.
Selanjutnya kita coba menggunakan command binwalk, namun install terlebih dahulu menggunakan command "apt-get install binwalk".
Langkah selanjutnya yaitu ketik command "binwalk oreo.jpg" untuk mengetahui apak ada file lain yang disembunyikan di balik gambar tersebut

![Step 2](https://github.com/Rizkian20/rizki/blob/main/Milk's%20Best%20Friend/2.png)

Dari hasil tersebut dapat dilihat terdapat file gambar asli dan 1 file berekstensi rar. Ketikkan command "foremost -v oreo.jpg" untuk mengekstrak file tersebut

![Step 3](https://github.com/Rizkian20/rizki/blob/main/Milk's%20Best%20Friend/3.png)

Lalu masuk ke direktori "cd output/rar" untuk mengekstrak file rar dengan command " unrar x 0000018.rar"

![Step 4](https://github.com/Rizkian20/rizki/blob/main/Milk's%20Best%20Friend/4.png)

Dari hasil ekstrak terdapat file gambar "b.jpg" lalu kita lihat string gari gambar tersebut tetapi masuk dulu de direktori "cd 1" lalu ketikan command "strings b.jpg"

![Step 5](https://github.com/Rizkian20/rizki/blob/main/Milk's%20Best%20Friend/5.png)

Hasil dari string gambar "b.jpg" menunjukkan bahwa terdapat flag dari challenge ini yaitu
flag : flag{eat_more_oreos}

