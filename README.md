# ball_store

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

## Tutorial 7
Widget tree adalah representasi logika dari semua UI widget. tree ini dicompute selama proses layout dan digunakan selama proses rendering serta hit testing. Widget direpresentasikan sebagai di tree sebagai node. setiap node bisa memiliki state yang mewakilinya. Setiap terjadi perubahan pada state, maka widget tersebut dan child nya akan dibangun ulang sesuai perubahan pada state

MyApp,MyHomePage,InfoCard,ItemCard
MyApp berfungsi sebagai root dari widget dan dapat melakukan global configuration
MyHomePage berguna sebagai page Menu dan Grid tempat InfoCard dan ItemCard dibuat
InfoCard berfungsi untuk card tentang info developer seperti NPM, Nama, dan Kelas 
ItemCard berfungsi untuk card button interaktif pada "All Product", "My Product", dan "Create Product"

MaterialApp sering digunakan sebagai widget root adalah karena MaterialApp menyediakan konfigurasi global serta dapat mengatur route untuk page yang akan diakses

Stateless widget: tidak punya state mereka tidak merubah diri mereka melalui internal. Namun dapat berubah dari kejadian external melalui widget parentnya dengan cara direbuild dengan data baru dari parent. Anak widget akan menerima arahan dari parent widget dan tidak dapat berubah dengan sendirinya. Stateless widget hanya memiliki final properti yang dibangun di constructor

Statefull widget: berubah secara dinamis seiring berjalannya page. Bersifat immutable namun mereka punya state yang mutable yang menggambarkan kondisi widget

Kita memilih stateless widget ketika tidak ada data yang diubah atau bersifat final dan memilih stateful widget ketika ingin mengubah data saat berinteraksi dengan widget oleh karena itu dibutuhkan state

Build context adalah class yang digunakan untuk menampilkan snackbar,mengatur tema, menyesuaikan lebar device, dan lainnya penggunaan dalam method build adalah sebagai parameter

konsep "hot reload" adalah memuat perubahan kode langsung ke virtual machine dan membangun ulang widget tree tanpa menghapus atau mengulang state aplikasi yang sedang berjalan. Proses ini tidak menjalankan ulang main() atau initstate()(cocok untuk stateless widget dan stateful widget yang tidak mengalami perubahan pada state)

Sedangkan "hot restart" memuat perubahan kode ke virtual machine dan memulai ulang flutter dari awal sehingga state akan hilang()

Checklist 1:Membuat sebuah program Flutter baru dengan tema E-Commerce yang sesuai dengan tugas-tugas sebelumnya.

saya menjalankan command flutter create ball_store pada command prompt kemudian masuk ke direktori proyek dan jalankan flutter run. Kemudian melakukan configurasi untuk enable web support dengan flutter config --enable-web

Checklist 2: Membuat tiga tombol sederhana dengan ikon dan teks.

Membuat class itemhomepage untuk wadah data dan membuat class itemcard sebagai class yang membuat widget dan mengubah data tersebut menjadi tampilan UI

Checklist 3: Memunculkan Snackbar

Membuat isi widget berada pada class InkWell kemudian menambahkan fitur interaktif onTap yang akan menampilkan snackbar ketika widget diclick

## Tutorial 8
Jelaskan perbedaan antara Navigator.push() dan Navigator.pushReplacement() pada Flutter. Dalam kasus apa sebaiknya masing-masing digunakan pada aplikasi Football Shop kamu?

Jawab: Navigator.push() adalah method untuk menambahkan route kedalam stack route Sedangkan Navigator.pushReplacement() adalah method untuk mengganti route pada atas stack dengan route yang dipush.
Navigator.push() cocok untuk halaman detail produk
Navigator.pushReplacement() cocok untuk halaman payment jadi ketika sudah sukses ia tidak akan kembali ke halaman payment

Bagaimana kamu memanfaatkan hierarchy widget seperti Scaffold, AppBar, dan Drawer untuk membangun struktur halaman yang konsisten di seluruh aplikasi?

Jawab:Scaffold sebagai parent berperan menjadi kerangka dari halaman yang menyediakan struktur dasar untuk AppBar dan drawer. AppBar sebagai parameter dari Scaffold berguna untuk menampilkan judul dan Drawer sebagai parameter dari Scaffold yang berguna untuk menyediakan navigasi yang menampilkan menu utama dari halaman 
Kombinasi ketiganya membentuk halaman dengan tema yang konsisten.

Dalam konteks desain antarmuka, apa kelebihan menggunakan layout widget seperti Padding, SingleChildScrollView, dan ListView saat menampilkan elemen-elemen form? Berikan contoh penggunaannya dari aplikasi kamu.

Jawab:kelebihan Padding adalah memberi jarak kosong di sekeliling widget jadi form tidak bertempelan, kemudian kelebihan SingleChildScrollView adalah membuat halaman yang scrollable ini digunakan dalam form karena form memiliki field yang lumayan banyak, dan kelebihan ListView ia adalah widget scrollable yang dirancang untuk menampilkan daftar item.  Contoh penggunaannya adalah: padding untuk memisahkan antar field pada form. SingleChildScrollView untuk halaman yang memiliki banyak konten, terakhir ListView untuk drawer agar ketika daftar menu bertambah navigasi dapat di scroll sehingga tidak terjadi overflow

Bagaimana kamu menyesuaikan warna tema agar aplikasi Football Shop memiliki identitas visual yang konsisten dengan brand toko?

Jawab: Saya menciptakan warna brand toko di satu file bernama main.dart yang berisi widget myApp sehingga halaman lainnya hanya perlu menggunakan warna yang sudah disediakan pada main.dart untuk menciptakan konsistensi warna tema

