## Module 5 - Java Profiling

Nama: Freia Arianti Zulaika

NPM: 2306152254

#### Endpoint `all-student`

Sebelum melakukan _profiling_ (GUI JMeter)
<img width="1189" alt="Screenshot 2025-03-13 at 23 39 42" src="https://github.com/user-attachments/assets/0b92c8c0-c53e-4020-9829-943f1b14b40d" />

Sebelum melakukan _profiling_ (CLI JMeter)
<img width="1090" alt="Screenshot 2025-03-13 at 23 36 37" src="https://github.com/user-attachments/assets/d7636fdd-774a-4702-867f-94d9d19c8bff" />

Setelah melakukan _profiling_ (GUI JMeter)
<img width="1187" alt="Screenshot 2025-03-13 at 23 40 49" src="https://github.com/user-attachments/assets/f93400ec-87e4-4981-863e-dfe8017e38d1" />

Setelah melakukan _profiling_ (CLI JMeter)
<img width="1114" alt="Screenshot 2025-03-13 at 23 37 34" src="https://github.com/user-attachments/assets/16eb11ed-0555-4741-b1be-672491fd12a7" />

#### Endpoint `highest-gpa`
Sebelum melakukan _profiling_ (GUI JMeter)
<img width="1056" alt="Screenshot 2025-03-13 at 23 40 00" src="https://github.com/user-attachments/assets/d4a09e09-31c4-48c7-b861-855e9eb50129" />

Sebelum melakukan _profiling_ (CLI JMeter)
<img width="1092" alt="Screenshot 2025-03-13 at 23 37 10" src="https://github.com/user-attachments/assets/37ab26dc-7af0-4850-97ab-9e242da1448e" />

Setelah melakukan _profiling_ (GUI JMeter)
<img width="1191" alt="Screenshot 2025-03-13 at 23 41 03" src="https://github.com/user-attachments/assets/60ec62e2-3f86-4552-9f8a-2fe7f7cb3b46" />

Setelah melakukan _profiling_ (CLI JMeter)
<img width="1106" alt="Screenshot 2025-03-13 at 23 37 46" src="https://github.com/user-attachments/assets/300a9a9d-3207-46b6-9d2c-0a42df2da0e4" />

#### Endpoint `all-student-name`
Sebelum melakukan _profiling_ (GUI JMeter)
<img width="1089" alt="Screenshot 2025-03-13 at 23 40 15" src="https://github.com/user-attachments/assets/d1cf4fce-6804-4474-b771-6d6e5b160299" />

Sebelum melakukan _profiling_ (CLI JMeter)
<img width="1098" alt="Screenshot 2025-03-13 at 23 37 22" src="https://github.com/user-attachments/assets/0dadedac-fce3-4ca4-9bcc-efd4d2175476" />

Setelah melakukan _profiling_ (GUI JMeter)
<img width="1188" alt="Screenshot 2025-03-13 at 23 41 26" src="https://github.com/user-attachments/assets/13a7dac1-3466-4744-8b58-5e59301f84bb" />

Setelah melakukan _profiling_ (CLI JMeter)
<img width="1111" alt="Screenshot 2025-03-13 at 23 37 57" src="https://github.com/user-attachments/assets/b54f671e-0a4e-435f-88c6-da1b9e736d29" />

> Conclusion

Sebelum melakukan _profiling_ dan optimisasi, waktu yang diperlukan untuk melakukan _request_ ke 
_endpoint_ `all-student` berkisar antara 99.000 - 135.000 ms. Untuk _request_ ke _endpoint_ `all-student-name` membutuhkan
waktu sekitar 2.500-3.200 ms. Sementara _request_ untuk _endpoint_ `highest-gpa` masih dalam batas yang wajar yaitu 
membutuhkan waktu 82-138 ms.

Setelah melakukan _profiling_ dan optimisasi, terjadi penurunan waktu eksekusi yang signifikan terutama pada _endpoint_ 
`all-student` dan `all-student-name`. Waktu yang dibutuhkan untuk melakukan _request_ ke _endpoint_ `all-student` 
turun drastis menjadi 7.400 - 8.250 ms. Sementara itu, waktu yang dibutuhkan untuk _request_ ke `all-student-name` 
menjadi 85 - 160 ms. _Request_ ke _endpoint_ `highest-gpa` juga mengalami peningkatan performa dan turun menjadi 
7 - 75 ms.

Hasil ini menunjukkan bahwa dengan melakukan _profiling_ dan menerapkan optimisasi kode, waktu eksekusi dapat berkurang 
secara signifikan, sehingga dapat meningkatkan efisiensi dan kecepatan aplikasi secara keseluruhan.

> What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?

Dengan JMeter, kita bisa menguji seberapa cepat atau lambat aplikasi merespons permintaan dari banyak pengguna secara 
bersamaan. Tapi, kita tidak bisa melihat apa yang terjadi di dalam proses eksekusi kode saat permintaan diproses. JMeter hanya memberi 
tahu berapa lama waktu yang dibutuhkan untuk mendapatkan respons, sehingga kita tahu apakah ada masalah performa, tapi 
tidak tahu penyebab pastinya.

Sementara itu, IntelliJ Profiler membantu kita untuk melihat langsung bagian kode mana yang membuat aplikasi jadi lambat. 
Dengan _tool_ ini, kita bisa tahu apakah ada _query database_ yang terlalu banyak, penggunaan CPU yang berlebihan, atau kode 
yang tidak efisien. Jadi, perbedaannya yaitu JMeter memberi gambaran soal performa aplikasi sedangkan IntelliJ Profiler membantu kita 
menemukan dan memperbaiki masalahnya langsung di dalam kode.

> How does the profiling process help you in identifying and understanding the weak points in your application?

Proses _profiling_ membantu kita dalam menemukan bagian kode yang membuat aplikasi berjalan lambat tanpa harus mencari
secara manual. Dengan menjalankan seluruh kode, kita bisa langsung melihat bagian mana yang butuh waktu lama untuk 
diproses. Langkah ini jauh lebih cepat dibandingkan mengetes setiap bagian kode satu per satu, sehingga menghemat banyak 
waktu.

_Profiling_ juga memberi informasi lengkap tentang penggunaan CPU, memori, dan waktu eksekusi setiap metode. Kita bisa 
tahu apakah ada _query database_ yang lambat, _loop_ yang terlalu berat, atau objek yang memakan banyak memori. Dengan itu, 
kita bisa langsung fokus ke bagian yang bermasalah dan melakukan optimasi, tanpa harus mencari-cari penyebab aplikasi 
berjalan dengan lambat. 

> Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?

Menurut saya, IntelliJ Profiler cukup efektif dalam membantu menganalisis dan mengidentifikasi _bottleneck_ dalam kode 
saya. Saat menjalankan aplikasi sambil melakukan _profiling_ dan mengirimkan _request_ ke _endpoint_ `all-student`, 
saya bisa langsung melihat bagian mana yang membuat respons jadi lama setelah _profiling_ dihentikan. Profiler juga 
menandai metode yang berjalan lama, dan ketika diklik, saya bisa melihat berapa lama waktu eksekusinya.

> What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?

Salah satu tantangan yang saya hadapi adalah mempercepat eksekusi kode berdasarkan hasil tes _performance_ dan _profiling_. 
Awalnya, saya merasa sulit menemukan cara yang lebih efisien, seperti pada method `findStudentWithHighestGpa`, yang kelihatannya hanya bisa menggunakan for loop. 
Namun, ternyata terdapat cara optimasi yang dapat dilakukan langsung dengan mengurutkan data berdasarkan GPA dan mengambil satu hasil teratas, sehingga prosesnya menjadi lebih cepat dan optimal.

> What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?

Menggunakan IntelliJ Profiler untuk _profiling_ memiliki banyak keuntungan, terutama karena terintegrasi langsung dengan 
IntelliJ IDEA, sehingga saya tidak perlu menggunakan aplikasi tambahan atau melakukan setup lain. Seluruh proses _profiling_ 
bisa dilakukan langsung di dalam satu tempat tanpa harus berpindah ke _tools_ lain yang tentunya dapat meningkatkan 
produktivitas. Selain itu, penggunaannya juga sangat mudah. _Profiler_ langsung berjalan tanpa memerlukan konfigurasi tambahan. 
IntelliJ Profiler juga membantu saya mengidentifikasi bagian kode yang memakan banyak _resource_, seperti query database yang lambat, metode yang terlalu lama dieksekusi, atau penggunaan memori yang berlebihan. 
Dengan fitur yang jelas, saya bisa langsung melihat _bottleneck_ dalam kode dan melakukan optimasi dengan lebih cepat dan efisien. 

> How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?

Jika hasil dari _profiling_ dan _performance testing_ dengan JMeter tidak semuanya sesuai, saya akan mencoba melakukan _profiling_ ulang untuk melihat apakah perbedaannya terjadi secara konsisten atau hanya kebetulan. 
Jika hasil tetap berbeda, saya akan memeriksa kembali konfigurasi JMeter dan hasil _profiling_ di IntelliJ Profiler untuk mencari kemungkinan penyebabnya. Jika masih belum menemukan solusinya, saya akan mencari informasi maupun referensi tambahan di internet untuk mendapatkan perspektif lain dalam menyelesaikan masalah tersebut.

> What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?

Sebelumnya, pada method `getAllStudentsWithCourses`, program mengambil daftar mahasiswa terlebih dahulu. Untuk setiap mahasiswa, dilakukan query untuk mengambil daftar mata kuliah yang diambil oleh mahasiswa tersebut. Ini menyebabkan masalah di mana satu query pertama mengambil semua mahasiswa (sebanyak N query) dan untuk setiap mahasiswa ada satu query tambahan untuk mendapatkan daftar mata kuliahnya (+1 query per mahasiswa). Total query yang dikirim ke database menjadi sangat banyak saat jumlah mahasiswa besar.

Dengan perubahan ini, sekarang program langsung menggunakan `studentCourseRepository.findAll()`, yang mengambil semua hubungan antara mahasiswa dan mata kuliah dalam satu query besar. Perubahan ini menghilangkan kewajiban untuk melakukan query tambahan per mahasiswa, sehingga database hanya perlu memproses satu permintaan dibandingkan melakukan banyak query terpisah. Oleh karena itu, akses data menjadi jauh lebih cepat, mengurangi beban pada database, serta meningkatkan efisiensi dan skalabilitas aplikasi.
