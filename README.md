<h1 align="center"> NLP With HuggingFace Transformers </h1>
<p align="center"> Berisi tentang pipeline dari HuggingFace Transformers untuk keperluan NLP (Natural Language Processing)</p>

<div align="center">

<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
<img src="https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white">

</div>

<h2 align="center"> Analisis </h2> 

## 1. Zero-Shot Classification

**Pipeline:** `pipeline("zero-shot-classification")`  
**Fungsi:** Mengklasifikasikan teks ke dalam kategori tanpa perlu pelatihan model sebelumnya.  
**Contoh:**  
- **Input:** *"This is a course about the Transformers library"*  
- **Labels:** `["education", "politics", "business"]`  
- **Hasil:** *"education"*  
**Kelebihan:** Fleksibel untuk berbagai domain.  
**Kekurangan:** Bergantung pada label kandidat.

---

## 2. Text Generation

**Pipeline:** `pipeline("text-generation")`  
**Fungsi:** Membuat teks otomatis berdasarkan prompt awal.  
**Contoh:**  
- **Input:** *"In this course, we will teach you how to"*  
- **Hasil:** *"build a machine learning model using Python."*  
**Kelebihan:** Berguna untuk chatbot dan konten otomatis.  
**Kekurangan:** Kadang menghasilkan teks yang tidak masuk akal.

---

## 3. Masked Language Modeling

**Pipeline:** `pipeline("fill-mask")`  
**Fungsi:** Mengisi teks yang hilang (dengan token `<mask>`).  
**Contoh:**  
- **Input:** *"This course will teach you all about <mask> models."*  
- **Hasil:** *"machine learning"* atau *"transformer"*  
**Kelebihan:** Ideal untuk autocomplete.  
**Kekurangan:** Prediksi bergantung pada konteks.

---

## 4. Named Entity Recognition (NER)

**Pipeline:** `pipeline("ner")`  
**Fungsi:** Mengidentifikasi entitas bernama seperti orang, tempat, atau organisasi.  
**Contoh:**  
- **Input:** *"My name is Ihsan and I work at MI6 in London."*  
- **Hasil:** Entitas seperti `{'entity': 'Ihsan', 'type': 'Person'}`  
**Kelebihan:** Mempermudah analisis data berbasis teks.  
**Kekurangan:** Kesulitan dengan entitas tidak umum.

---

## 5. Question Answering (QA)

**Pipeline:** `pipeline("question-answering")`  
**Fungsi:** Menjawab pertanyaan berdasarkan konteks.  
**Contoh:**  
- **Konteks:** Penjelasan tentang atom.  
- **Pertanyaan:** *"Apa itu atom?"*  
- **Hasil:** *"Bagian yang sangat kecil dari segala sesuatu di alam semesta."*  
**Kelebihan:** Berguna untuk chatbot dan mesin pencari.  
**Kekurangan:** Bergantung pada kelengkapan konteks.

---

## 6. Sentiment Analysis

**Pipeline:** `pipeline("sentiment-analysis")`  
**Fungsi:** Menganalisis sentimen teks (positif, negatif, netral).  
**Contoh:**  
- **Input:** *"The weather was perfect! but I think I will not go outside today."*  
- **Hasil:** *"Positive"*  
**Kelebihan:** Berguna untuk analisis media sosial.  
**Kekurangan:** Tidak akurat untuk sentimen campuran.

---

## 7. Summarization

**Pipeline:** `pipeline("summarization")`  
**Fungsi:** Merangkum teks panjang.  
**Contoh:**  
- **Input:** Penjelasan panjang tentang Perang Napoleon.  
- **Hasil:** Ringkasan singkat tentang perang dan hasilnya.  
**Kelebihan:** Menghemat waktu membaca.  
**Kekurangan:** Kadang kehilangan detail penting.

---

## 8. Translation

**Pipeline:** `pipeline("translation", model="Helsinki-NLP/opus-mt-id-en")`  
**Fungsi:** Menerjemahkan teks antar bahasa.  
**Contoh:**  
- **Input:** *"menikmati hidup adalah kesukaanku"*  
- **Hasil:** *"Enjoying life is my favorite thing."*  
**Kelebihan:** Akurat untuk teks sederhana.  
**Kekurangan:** Kesulitan dengan kalimat kompleks.

---

## Kesimpulan

HuggingFace Transformers adalah alat serbaguna untuk berbagai tugas NLP. Dengan pipeline ini, developer dapat dengan mudah mengimplementasikan fitur seperti klasifikasi, QA, dan summarization tanpa membangun model dari awal. Kinerja model tetap bergantung pada kasus penggunaan dan data yang diberikan.

Kekurangan: Kadang mengalami kesalahan untuk kalimat kompleks atau idiomatik.
Kesimpulan:
HuggingFace Transformers menyediakan pipeline serbaguna untuk berbagai tugas NLP. Dengan fleksibilitas ini, developer dapat dengan mudah mengimplementasikan fitur NLP seperti klasifikasi, QA, dan summarization tanpa harus membangun model dari awal. Namun, kinerja model tergantung pada kasus penggunaan spesifik dan data yang digunakan.
