# Project-finding-concat-data-python
This project about learning finding and concatenating data in python (In Indonesia)

Memanfaatkan fitur Python untuk cleaning data dalam packages pandas, misalnya kita ingin melakukan proses concatenating dataframes maka kita harus memuat data kemudian menjadikannya sebuah Python list.
Namun bagaimana jika kita memiliki ribuan data dan ingin kita load untuk kemudian dilakukan proses concatenating? Kita bisa menggunakan fungsi glob untuk menemukan files berdasarkan pattern.
Globbing:
Globbing adalah cara sederhana bagi python untuk melakukan pencocokan pola nama file. Kita bisa menggunakan berbagai wildcard untuk menentukan pola nama file yang kita cari. Wildcard adalah simbol yang akan cocok dengan jumlah karakter sembarang. (*?)
Simbol asterik (*) adalah tipe wildcard untuk pencocokan semua string. Simbol question mark (?) hanya mengijinkan kita untuk melakukan pencocokan 1 character saja.
Misalnya saja file *.csv akan mencocokan semua file dengan akhiran dot csv sedangkan file_?.csv akan mencocofilekan dengan single character. Single character tersebut bisa saja angka 0 - 9 atau hanya huruf A - Z.
Fungsi glob akan mengembalikan Python list dari nama file yang akan dilakukan proses pencocokan. Sehingga kita bisa gunakan list itu untuk kita muat ke pandas dataframes.

Langkah pertama kita import module glob dan package pandas.
Kemudian kita gunakan fungsi glob untuk mencari file dengan pattern * dot csv. Kemudian kita tampilkan semua file tersebut.
Misalkan disini saya ingin melihat informasi dari file “uber-raw-data-2014_05.csv”. Maka saya gunakan perintah pd.read_csv berdasarkan index file ke 1. Karena dapat kita lihat jika file “uber-raw-data-2014_05.csv” berada diurutan ke 2.
Jika kita ingin menampilkan semua isi dari file tersebut. Kita dapat menggunakan perulangan loops. Pertama kita buat list kosong untuk melakukan inisialisasi yang akan kita append atau tambahkan ke dataframes. Baru kemudian kita lakukan perulangan dengan for loops untuk masing - masing nama file.  Maka kita akan mendapatkan 300 rows dari 3 dataframes tersebut. sudah memiliki gabungan 3 dataframes dengan masing - masing file berisi 100 rows.
