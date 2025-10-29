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

Widget tree adalah representasi logika dari semua UI widget. tree ini dicompute selama proses layout dan digunakan selama proses rendering serta hit testing. Widget direpresentasikan sebagai di tree sebagai node. setiap node bisa memiliki state yang mewakilinya. Setiap terjadi perubahan pada state, maka widget tersebut dan child nya akan dibangun ulang sesuai perubahan pada state

MyApp,MyHomePage,InfoCard,ItemCard
MyApp berfungsi sebagai root dari widget dan dapat melakukan global configuration
MyHomePage berguna sebagai page Menu dan Grid tempat InfoCard dan ItemCard dibuat
InfoCard berfungsi untuk card tentang info developer seperti NPM, Nama, dan Kelas 
ItemCard berfungsi untuk card button interaktif pada "All Product", "My Product", dan "Create Product"

Stateless widget: tidak punya state mereka tidak merubah diri mereka melalui internal. Namun dapat berubah dari kejadian external melalui widget parentnya dengan cara direbuild dengan data baru dari parent. Anak widget akan menerima arahan dari parent widget dan tidak dapat berubah dengan sendirinya. Stateless widget hanya memiliki final properti yang dibangun di constructor

Statefull widget: berubah secara dinamis seiring berjalannya page. Bersifat immutable namun mereka punya state yang mutable yang menggambarkan kondisi widget

Kita memilih stateless widget ketika tidak ada data yang diubah atau bersifat final dan memilih stateful widget ketika ingin mengubah data saat berinteraksi dengan widget oleh karena itu dibutuhkan state

konsep "hot reload" adalah memuat perubahan kode langsung ke virtual machine dan membangun ulang widget tree tanpa menghapus atau mengulang state aplikasi yang sedang berjalan. Proses ini tidak menjalankan ulang main() atau initstate()(cocok untuk stateless widget dan stateful widget yang tidak mengalami perubahan pada state)

Sedangkan "hot restart" memuat perubahan kode ke virtual machine dan memulai ulang flutter dari awal sehingga state akan hilang()

Checklist 1:Membuat sebuah program Flutter baru dengan tema E-Commerce yang sesuai dengan tugas-tugas sebelumnya.

saya menjalankan command flutter create ball_store pada command prompt kemudian masuk ke direktori proyek dan jalankan flutter run. Kemudian melakukan configurasi untuk enable web support dengan flutter config --enable-web

Checklist 2: Membuat tiga tombol sederhana dengan ikon dan teks.

Membuat class itemhomepage untuk wadah data dan membuat class itemcard sebagai class yang membuat widget dan mengubah data tersebut menjadi tampilan UI

Checklist 3: Memunculkan Snackbar

Membuat isi widget berada pada class InkWell kemudian menambahkan fitur interaktif onTap yang akan menampilkan snackbar ketika widget diclick




