# Laporan Proyek Menyelesaikan Permasalahan Human Resources
---
## Business Understanding

Analisis Faktor Penyebab Tingginya Tingkat Attrition di Perusahaan Jaya Jaya Maju

Jaya Jaya Maju merupakan perusahaan multinasional yang telah berdiri sejak tahun 2000 dan kini menaungi lebih dari 1.000 karyawan yang tersebar di berbagai wilayah Indonesia. Meskipun telah berkembang menjadi perusahaan berskala besar, Jaya Jaya Maju menghadapi tantangan serius dalam hal pengelolaan sumber daya manusia.

Salah satu permasalahan utama yang tengah dihadapi adalah tingginya tingkat attrition atau tingkat keluar masuknya karyawan, yang saat ini telah melebihi angka 10%. Kondisi ini dapat berdampak langsung terhadap stabilitas operasional perusahaan serta efisiensi kerja secara keseluruhan.

Untuk mengantisipasi dan mengatasi permasalahan tersebut, manajemen melalui Departemen Human Resources berinisiatif melakukan analisis mendalam guna mengidentifikasi berbagai faktor yang berkontribusi terhadap tingginya tingkat attrition. Selain itu, diperlukan juga sebuah business dashboard yang komprehensif untuk memonitor dan mengevaluasi berbagai indikator kunci yang berkaitan dengan kepuasan dan retensi karyawan secara berkelanjutan.

---
## Permasalahan Bisnis

Meskipun Jaya Jaya Maju telah berkembang menjadi perusahaan multinasional dengan lebih dari 1.000 karyawan, tingkat attrition yang melebihi 10% menjadi perhatian serius bagi manajemen, khususnya Departemen Human Resources. Tingginya tingkat perputaran karyawan tidak hanya berdampak pada biaya rekrutmen dan pelatihan, tetapi juga pada kontinuitas operasional serta moral tim secara keseluruhan.

Melalui data yang tersedia, berikut adalah beberapa fokus permasalahan yang ingin dipecahkan:

1. **Apa faktor-faktor utama yang mempengaruhi attrition karyawan?**
Melalui analisis eksploratif dan statistik, perusahaan ingin mengetahui variabel mana yang paling berkontribusi terhadap keputusan karyawan untuk keluar, seperti:
    - ***OverTime*** (Lembur berlebih)
    - ***JobSatisfaction & EnvironmentSatisfaction*** (Tingkat kepuasan kerja dan lingkungan)
    - ***MonthlyIncome & PercentSalaryHike*** (Kompensasi)
    - ***YearsSinceLastPromotion*** (Jarak waktu sejak promosi terakhir)
    - ***WorkLifeBalance*** (Keseimbangan hidup-kerja)
    - ***DistanceFromHome*** (Jarak rumah ke kantor)

2. **Apakah terdapat kelompok karyawan tertentu yang lebih rentan mengalami attrition?**
Perusahaan ingin mengidentifikasi segmen karyawan yang memiliki risiko keluar lebih tinggi berdasarkan:
    - Usia (Age)
    - Departemen atau JobRole
    - Tingkat Pendidikan atau EducationField
    - Status Pernikahan (MaritalStatus)
    - Jumlah tahun bekerja di perusahaan (YearsAtCompany, TotalWorkingYears)

3. **Bagaimana hubungan antara kompensasi dan kepuasan kerja terhadap attrition?**
Perlu dianalisis apakah gaji bulanan, kenaikan gaji, dan insentif seperti stock option berkorelasi dengan:
    - JobSatisfaction
    - PerformanceRating
    - Attrition

4. **Sejauh mana peran atasan langsung mempengaruhi keputusan karyawan untuk tetap tinggal?**
Perusahaan ingin mengevaluasi pengaruh variabel berikut terhadap attrition:
    - YearsWithCurrManager (Lama bekerja dengan manajer saat ini)
    - RelationshipSatisfaction (Kepuasan terhadap relasi interpersonal di tempat kerja)
    - JobInvolvement (Tingkat keterlibatan karyawan terhadap pekerjaannya)

5. **Apakah pelatihan yang diberikan efektif dalam meningkatkan retensi karyawan?**
Variabel TrainingTimesLastYear dapat dianalisis untuk melihat apakah karyawan yang mengikuti pelatihan lebih cenderung bertahan di perusahaan.

---
## Cakupan Proyek
Proyek ini mencakup:

1. Persiapan dataset `employee_data.csv` untuk analisis data.
2. Pemrosesan dataset untuk memperbaiki dan membersihkan data agar dapat digunakan pada proses analisis data.
3. Pembuatan fitur tambahan.
4. Analisis faktor penyebab attrition berdasarkan data kategori dan nominal.
5. Pembuatan Business Dashboard agar mudah dipahami dalam memantau faktor penyebab attrition.
6. Membuat kesimpulan terhadap hasil analisis data.
7. Memberi rekomendasi untuk mengurangi attrition.

---
## Persiapan
Sumber data: [Dataset - Jaya Jaya Maju](https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee)

Setup Environment: Proyek ini membutuhkan lingkungan sederhana untuk menjalankan analisis data dan dashboard. Berikut langkah-langkah untuk mempersiapkan environment:
1. Menjalankan berkas `notebook.ipynb`
    - Pastikan dependensi, packages, library yang dibutuhkan sudah tersedia (lihat file requirements.txt untuk melihat dependensi yang dibutuhkan).
    - Jalankan seluruh isi file notebook.ipynb menggunakan Google Colab/Jupyter Notebook untuk melihat hasil analisis data, temuan, dan insight yang diperoleh.
2. Menjalankan Dashboard: Untuk melihat isi dashboard secara langsung, dapat menggunakan metabase dengan bantuan Docker (pastikan Docker sudah terinstall)
    - Jalankan perintah berikut:
        ```
        docker pull metabase/metabase:v0.46.4
        ```
    - Jalankan container Metabase menggunakan perintah:
        ```
        docker run -p 3000:3000 --name metabase metabase/metabase
        ```
    - Login ke Metabase menggunakan username dan password berikut:
        ```
        username: aflah@dicoding.com
        password: dicoding1234;
        ```

---
## Business Dashboard
![aflahazzaky-dashboard](https://github.com/user-attachments/assets/ef87347e-94a8-400c-aa4f-1c34d2b1a70c)

Berdasarkan visualisasi data attrition pada perusahaan Jaya Jaya Maju, ditemukan beberapa faktor utama yang berkontribusi terhadap tingginya tingkat pengunduran diri karyawan. Karyawan yang lebih muda dengan pengalaman kerja yang masih minim cenderung lebih rentan untuk keluar dari perusahaan. Selain itu, karyawan yang jarang mendapat promosi serta mereka yang sering melakukan perjalanan dinas juga menunjukkan tingkat attrition yang lebih tinggi. Dari sisi jabatan, peran seperti Sales Executive dan Research Scientist memiliki tingkat attrition tertinggi. Sementara itu, departemen Sales menunjukkan angka attrition yang paling tinggi dibandingkan departemen lainnya. Status pernikahan juga berpengaruh, di mana karyawan lajang memiliki kemungkinan keluar lebih besar dibandingkan yang sudah menikah atau bercerai.

---
## Conclusion
Dari visualisasi yang ditampilkan, terdapat indikasi bahwa karyawan yang lebih muda, memiliki masa kerja lebih pendek, pendapatan bulanan lebih rendah, serta jarak rumah ke tempat kerja yang relatif jauh, cenderung lebih berisiko untuk keluar dari perusahaan.

Analisis visual ini menunjukkan bahwa faktor-faktor seperti beban kerja (lembur), kepuasan kerja, hubungan sosial di kantor, dan peran pekerjaan tertentu memiliki pengaruh paling besar terhadap keputusan karyawan untuk keluar. Sementara itu, aspek seperti jenis kelamin, tingkat pendidikan, dan jarak rumah ke kantor kurang berpengaruh secara signifikan.

---
## Recomendation Action
1. Retensi Karyawan Baru: Fokus pada strategi retensi untuk karyawan dengan masa kerja di bawah 3 tahun. Misalnya, melalui program mentoring, pengembangan karier awal, atau pemberian insentif lebih awal.
2. Tinjauan Gaji: Evaluasi kembali struktur gaji terutama pada kelompok karyawan berpenghasilan menengah ke bawah.
3. Kebijakan Kerja Fleksibel: Pertimbangkan opsi kerja fleksibel atau dukungan transportasi untuk karyawan yang tinggal jauh dari kantor.
4. Analisis Lanjutan: Lakukan analisis prediktif dengan algoritma klasifikasi untuk menentukan variabel mana yang paling berpengaruh terhadap Attrition, guna mendukung intervensi yang lebih tepat sasaran.
5. Evaluasi dan atur kembali kebijakan lembur dan jam kerja.
6. Bangun budaya kerja yang positif dan suportif.
7. Tingkatkan kepuasan kerja melalui pengakuan, tantangan, dan pengembangan karier.
8. Fokuskan program retensi pada peran dengan risiko tinggi attrition.
9. Gunakan pendekatan data untuk deteksi dini karyawan berisiko tinggi keluar.
