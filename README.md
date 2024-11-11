NAMA : ISHAK HADI PERNAMA 
NIM : 362358302072

Praktikum 1: Dasar State dengan Model-View
1. Jelaskan maksud dari langkah 4 pada praktikum tersebut! Mengapa dilakukan demikian? Pada , file data_layer.dart dibuat untuk menggabungkan ekspor model plan.dart dan task.dart. Tujuannya agar proses impor menjadi lebih mudah dan rapi, karena hanya perlu mengimpor satu file data_layer.dart untuk mengakses semua model yang dibutuhkan. Ini membuat kode lebih efisien, mudah dipelihara, dan lebih mudah dibaca.

2. Mengapa perlu variabel plan di langkah 6 pada praktikum tersebut? Mengapa dibuat konstanta ? Variabel plan pada Langkah 6 diperlukan untuk menyimpan data rencana yang berisi daftar tugas dalam aplikasi. Variabel ini digunakan untuk memanipulasi dan memperbarui informasi rencana, seperti menambahkan tugas baru atau mengubah status tugas.

Dibuat sebagai konstanta karena pada saat pembuatan objek Plan, nilai-nilai default seperti nama dan daftar tugas ditetapkan melalui konstruktor. Menggunakan konstanta memastikan nilai awal objek tidak dapat diubah setelah objek dibuat, yang membantu menjaga integritas data dan menghindari perubahan yang tidak diinginkan.

Capture Pratikum 1

![prak1](https://github.com/user-attachments/assets/3406d5c1-01a1-4985-b841-92a0589b50e6)


3. Apa kegunaan method pada Langkah 11 dan 13 dalam lifecyle state ? Pada Langkah 11 dan Langkah 13, dua metode penting dalam siklus hidup StatefulWidget digunakan, yaitu initState() dan dispose().

initState() (Langkah 11): Metode ini dipanggil sekali saat State pertama kali dibuat. Di sini, kita menginisialisasi variabel seperti scrollController dan menambahkan listener untuk menangani peristiwa scroll. initState() memastikan bahwa pengaturan awal untuk scroll controller terjadi sebelum widget ditampilkan.

dispose() (Langkah 13): Metode ini dipanggil ketika State widget tidak lagi digunakan, biasanya saat widget dihapus dari widget tree. Di sini, kita membersihkan scrollController dengan memanggil dispose() untuk mencegah kebocoran memori dan melepaskan sumber daya yang digunakan oleh controller.

Kedua metode ini mengelola siklus hidup objek dengan baik, memastikan pengaturan yang benar saat widget pertama kali muncul dan membersihkan sumber daya saat tidak diperlukan lagi.

Tugas Praktikum 2: InheritedWidget
Jelaskan mana yang dimaksud InheritedWidget pada langkah 1 tersebut! Mengapa yang digunakan InheritedNotifier? Pada langkah 1, InheritedWidget adalah widget yang memungkinkan data diteruskan ke widget anak tanpa perlu meneruskannya secara manual. InheritedNotifier adalah subclass dari InheritedWidget yang lebih spesifik digunakan untuk menangani perubahan data, dengan menghubungkan ValueNotifier untuk mengelola state yang berubah. Ini memungkinkan widget yang bergantung padanya untuk otomatis memperbarui UI saat data berubah, membuat pengelolaan state menjadi lebih efisien dan mudah.

Jelaskan maksud dari method di langkah 3 pada praktikum tersebut! Mengapa dilakukan demikian? Tujuannya adalah untuk mempermudah perhitungan dan penampilan status progres dari task yang ada pada Plan. Dengan menambahkan dua method ini, kita dapat dengan mudah menampilkan jumlah task yang selesai dan progres keseluruhan tanpa harus menghitungnya berulang-ulang di tempat lain dalam kode, membuat logika aplikasi menjadi lebih terstruktur dan efisien.




Tugas Praktikum 3: State di Multiple Screens
Berdasarkan Praktikum 3 yang telah Anda lakukan, jelaskan maksud dari gambar diagram berikut ini!

9ce81bcd2817adc8

Diagram tersebut menjelaskan perbandingan dua struktur widget pada aplikasi Flutter, yang melibatkan navigasi antar layar menggunakan Navigator.push.

Struktur Kiri (Sebelum Navigasi)

MaterialApp: Komponen utama aplikasi Flutter.
PlanProvider: Widget yang menyediakan data untuk widget turunannya.
PlanCreatorScreen: Halaman awal yang menampilkan antarmuka pengguna.
Column: Widget yang mengatur elemen dalam tata letak vertikal.
TextField: Komponen input teks.
Expanded: Widget yang mengisi ruang yang tersisa.
ListView: Widget untuk menampilkan daftar item yang bisa digulir.
Struktur ini menggambarkan halaman awal yang memiliki komponen interaktif seperti input teks dan daftar elemen yang bisa digulir.

Struktur Kanan (Setelah Navigasi dengan Navigator.push)

MaterialApp: Tetap sebagai komponen utama aplikasi.
PlanScreen: Layar baru yang ditampilkan setelah navigasi.
Scaffold: Struktur kerangka dasar layar dengan dukungan AppBar, body, dll.
Column: Masih digunakan untuk tata letak vertikal.
Expanded: Digunakan untuk mengisi ruang kosong dalam Column.
SafeArea: Widget yang menjaga konten agar tidak terhalang oleh elemen lain, seperti status bar.
ListView dan Text: Digunakan untuk menampilkan daftar item dan teks.
Diagram ini mengilustrasikan bagaimana aplikasi berpindah dari satu layar ke layar lainnya. Navigator.push digunakan untuk navigasi dari PlanCreatorScreen ke PlanScreen, yang memiliki antarmuka lebih lengkap dengan elemen Scaffold dan SafeArea untuk memastikan konten tampil aman di layar.


Capture Pratikum 3 :


![PRAK3](https://github.com/user-attachments/assets/37fb7606-b737-4720-a853-186b6cac7387)

