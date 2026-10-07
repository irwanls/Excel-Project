# Employee Performance Evaluation

## Project Overview

**Employee Performance Evaluation** merupakan proyek analisis data yang bertujuan untuk mengevaluasi kondisi tenaga kerja dan performa karyawan berdasarkan data historis perusahaan. Analisis difokuskan pada status karyawan, distribusi performa karyawan aktif, perbandingan performa antar-departemen, serta identifikasi departemen yang perlu menjadi prioritas evaluasi.

Proyek ini menggunakan **Microsoft Excel** untuk proses data preparation, pengolahan data, Pivot Table, serta pembuatan dashboard dan visualisasi.

---

## Problem Statement

Perusahaan memiliki data karyawan dalam jumlah besar, tetapi data tersebut perlu diolah agar dapat memberikan gambaran yang lebih jelas mengenai kondisi tenaga kerja dan performa karyawan.

Beberapa pertanyaan utama yang ingin dijawab melalui proyek ini adalah:

1. Bagaimana performa karyawan yang masih aktif?
2. Bagaimana perbandingan performa karyawan antar-departemen?
3. Departemen mana yang memiliki jumlah karyawan dengan performa rendah paling banyak sehingga perlu menjadi prioritas evaluasi?
4. Apakah terdapat indikasi perbedaan standar penilaian performa antar-departemen?

Dengan menjawab pertanyaan tersebut, analisis diharapkan dapat membantu perusahaan menentukan area yang perlu mendapatkan perhatian lebih dalam proses evaluasi karyawan.

---

## Data Understanding

Dataset yang digunakan berasal dari [**Kaggle – Employee Data**](https://www.kaggle.com/datasets/ravindrasinghrana/employeedataset) dengan periode data **Agustus 2018 hingga Agustus 2023**.

Dataset awal terdiri dari:

- **3.000 baris data**
- **26 kolom**
- Informasi mengenai identitas karyawan
- Status karyawan
- Departemen dan divisi
- Tanggal mulai dan keluar
- Jenis pekerjaan
- Status terminasi
- Performance Score
- Current Employee Rating

Data tersebut kemudian digunakan untuk melihat hubungan antara status karyawan, departemen, dan hasil penilaian performa.

---

## Data Quality

Sebelum melakukan analisis, dilakukan pemeriksaan terhadap kualitas data untuk mengidentifikasi permasalahan yang dapat memengaruhi hasil analisis.

Beberapa permasalahan yang ditemukan adalah:

- Terdapat masalah duplikasi atau ketidakkonsistenan data pada kolom **DepartmentType sebesar 3,2%**.
- Terdapat **missing value pada ExitDate dan TerminationDescription sebesar 48,9%**.
- Beberapa data kategorikal perlu dibersihkan dan dikelompokkan kembali agar lebih mudah digunakan dalam proses analisis.

Tahap **data preparation** dilakukan untuk memastikan data yang digunakan dalam Pivot Table, dashboard, dan visualisasi memiliki struktur yang lebih konsisten.

Status karyawan kemudian dikelompokkan menjadi kategori yang lebih sederhana, yaitu **Active, Not Active, dan Not Yet**. Sementara itu, performa juga digunakan untuk membedakan karyawan dengan performa baik dan karyawan yang membutuhkan perhatian lebih.

---

## Analysis

### 1. Employee Status

Analisis pertama dilakukan untuk melihat kondisi tenaga kerja perusahaan secara keseluruhan.

Dari **3.000 karyawan**, sebanyak **2.544 karyawan atau sekitar 85% masih berstatus aktif**. Selain itu, terdapat **69 karyawan atau sekitar 2% yang berstatus Future Start atau belum mulai bekerja**.

Hasil ini menunjukkan bahwa sebagian besar tenaga kerja dalam dataset masih berstatus aktif.

---

### 2. Employee Performance

Analisis selanjutnya difokuskan pada performa karyawan yang masih aktif.

Performance Score dibagi menjadi beberapa kategori:

- **Exceeds**
- **Fully Meets**
- **Needs Improvement**
- **PIP**

Secara keseluruhan, mayoritas karyawan aktif berada pada kategori **Fully Meets** dan **Exceeds**. Hal ini menunjukkan bahwa secara umum performa karyawan berada pada kondisi yang cukup baik.

Namun, distribusi performa tetap perlu dianalisis berdasarkan departemen karena jumlah dan pola penilaian dapat berbeda pada masing-masing bagian perusahaan.

---

### 3. Performance by Department

Analisis per departemen menunjukkan bahwa mayoritas karyawan di setiap departemen berada pada kategori performa baik.

Salah satu temuan yang menarik terdapat pada **Software Engineering**, di mana seluruh **92 karyawan memiliki performance score Fully Meets**.

Walaupun hal ini dapat menunjukkan performa departemen yang baik, kondisi tersebut juga dapat menjadi indikasi bahwa terdapat kemungkinan perbedaan penerapan standar penilaian performa antar-departemen. Oleh karena itu, konsistensi sistem penilaian perlu menjadi salah satu hal yang dievaluasi.

---

### 4. Underperforming Employees

Untuk menentukan prioritas evaluasi, kategori **Needs Improvement** dan **PIP** digunakan untuk mengidentifikasi karyawan yang memiliki performa di bawah standar.

Departemen **Production** memiliki jumlah karyawan dengan performa rendah paling banyak, yaitu:

- **118 karyawan – Needs Improvement**
- **46 karyawan – PIP**
- **Total 164 karyawan**

Jumlah tersebut merupakan yang terbesar dibandingkan departemen lainnya.

Dengan demikian, **Production menjadi departemen utama yang perlu mendapatkan perhatian dalam proses evaluasi performa**.

---

## Kesimpulan

Berdasarkan hasil analisis, sebagian besar tenaga kerja dalam dataset masih berstatus aktif dan secara keseluruhan memiliki performa yang cukup baik, karena mayoritas karyawan berada pada kategori **Fully Meets** dan **Exceeds**.

Namun, terdapat dua hal utama yang perlu menjadi perhatian.

Pertama, terdapat perbedaan distribusi hasil penilaian antar-departemen. Kondisi seperti **Software Engineering yang memiliki 100% karyawan dengan kategori Fully Meets** perlu diperhatikan untuk memastikan bahwa standar penilaian performa diterapkan secara konsisten di seluruh departemen.

Kedua, **Production menjadi prioritas utama dalam evaluasi performa**, karena memiliki **164 karyawan dalam kategori Needs Improvement dan PIP**, jumlah terbesar dibandingkan departemen lainnya.

Dengan demikian, hasil analisis tidak hanya menunjukkan kondisi performa karyawan secara keseluruhan, tetapi juga membantu menentukan area yang perlu mendapatkan perhatian lebih dalam proses evaluasi sumber daya manusia.

---

## Rekomendasi

Berdasarkan hasil analisis, terdapat dua rekomendasi utama:

1. **Evaluasi sistem penilaian performa karyawan**

   Perusahaan perlu memastikan bahwa indikator, standar, dan metode penilaian performa diterapkan secara konsisten antar-departemen sehingga hasil penilaian dapat dibandingkan secara lebih objektif.

2. **Memprioritaskan evaluasi pada Departemen Production**

   Karena memiliki jumlah karyawan dengan kategori **Needs Improvement dan PIP** paling banyak, perusahaan dapat melakukan evaluasi lebih lanjut terhadap faktor-faktor yang memengaruhi performa karyawan pada departemen tersebut.

---

## Project Structure

Proses analisis dalam proyek ini terdiri dari:

**Problem Statement → Data Understanding → Data Preparation → Data Analysis → Visualization → Recommendation**

Workbook proyek juga dibagi menjadi beberapa bagian utama:

- **employee_data** – dataset awal
- **Data bersih** – data setelah proses preparation
- **Pivot** – pengolahan dan agregasi data
- **Dashboard** – visualisasi hasil analisis

---

## Kontak
[**Linkedin**](https://www.linkedin.com/in/irwanls/)

[**WhatsApp**](https://wa.me/6285363679097)
