# Tutorial 9 - Advanced Programming - Timer
**Akmal Ramadhan - 2206081534 - Kelas A**

## Understanding How It Works
<img src="img/img1.png">

Walaupun `println!()` dijalankan setelah baris kode `spawner.spawn( async { ... });`, _string_ `hey hey` _printed_ sebelum _string_ `howdy!`. Mengapa? Karena fungsi `async` berjalan di luar eksekusi utama yang berarti program utama tidak menunggu fungsi `async` selesai sebelum melanjutkan eksekusi selanjutnya. Mencetak _string_ `hey hey` berada di luar fungsi `async` dan langsung dieksekusi oleh program utama sementara fungsi `async` menunggu hasil dari `future`. Sehingga, `hey hey` dicetak terlebih dahulu sebelum _task_ `async` dijalankan oleh `executor.`