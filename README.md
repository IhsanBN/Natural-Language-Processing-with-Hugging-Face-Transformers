<h1 align="center"> NLP With HuggingFace Transformers </h1>
<p align="center"> Berisi tentang pipeline dari HuggingFace Transformers untuk keperluan NLP (Natural Language Processing)</p>

<div align="center">

<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
<img src="https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white">

</div>

<h2 align="center"> Analisis </h2> 

1. Zero-Shot Classification
Pipeline: pipeline("zero-shot-classification")

Analisis:
Fungsi: Pipeline ini digunakan untuk mengklasifikasikan teks ke dalam kategori tanpa perlu melatih model terlebih dahulu dengan label yang spesifik.
Cara Kerja: Model menggunakan pendekatan transfer learning untuk menghitung kesesuaian teks input terhadap label yang diberikan.
Contoh Kasus:
Input: "This is a course about the Transformers library"
Labels: ["education", "politics", "business"]
Hasil: Teks diklasifikasikan ke label yang paling relevan, dalam hal ini adalah "education."
Kelebihan: Sangat fleksibel untuk diterapkan pada berbagai domain tanpa pelatihan tambahan.
Kekurangan: Hasil sangat tergantung pada kandidat label yang diberikan.

2. Text Generation
Pipeline: pipeline("text-generation")

Analisis:
Fungsi: Membuat teks secara otomatis berdasarkan prompt awal.
Cara Kerja: Model seperti GPT-2 menghasilkan teks berdasarkan distribusi probabilistik kata berikutnya.
Contoh Kasus:
Input: "In this course, we will teach you how to"
Hasil: Model menghasilkan kelanjutan teks yang relevan seperti "build a machine learning model using Python."
Penggunaan Model Spesifik: Contohnya distilgpt2, yang merupakan versi ringan dari GPT-2.
Kelebihan: Berguna untuk aplikasi seperti chatbot, konten otomatis, dan pengisian teks.
Kekurangan: Kadang menghasilkan teks yang tidak masuk akal jika prompt tidak jelas.

3. Masked Language Modeling
Pipeline: pipeline("fill-mask")

Analisis:
Fungsi: Mengisi bagian teks yang hilang atau tidak lengkap (ditandai dengan token <mask>).
Cara Kerja: Model memprediksi kata yang paling mungkin menggantikan mask berdasarkan konteks.
Contoh Kasus:
Input: "This course will teach you all about <mask> models."
Hasil: Prediksi seperti "machine learning" atau "transformer."
Kelebihan: Ideal untuk tugas-tugas seperti autocomplete atau analisis teks.
Kekurangan: Bergantung pada konteks; jika ambigu, prediksi bisa salah.

4. Named Entity Recognition (NER)
Pipeline: pipeline("ner")

Analisis:
Fungsi: Mengidentifikasi entitas bernama dalam teks, seperti nama orang, tempat, atau organisasi.
Cara Kerja: Model menandai entitas tertentu berdasarkan klasifikasi yang telah dilatih sebelumnya.
Contoh Kasus:
Input: "My name is Ihsan and I work at MI6 in London."
Hasil: {'entity': 'Ihsan', 'type': 'Person'}, {'entity': 'MI6', 'type': 'Organization'}, {'entity': 'London', 'type': 'Location'}
Kelebihan: Mempermudah analisis data berbasis teks yang memerlukan struktur.
Kekurangan: Model bisa kesulitan jika entitas tidak umum atau ambigu.

5. Question Answering (QA)
Pipeline: pipeline("question-answering")

Analisis:
Fungsi: Menjawab pertanyaan berdasarkan konteks yang diberikan.
Cara Kerja: Model seperti distilbert-base-cased-distilled-squad mencari bagian teks yang paling relevan untuk menjawab pertanyaan.
Contoh Kasus:
Konteks: Penjelasan tentang atom.
Pertanyaan: "Apa itu atom?"
Hasil: "Bagian yang sangat kecil dari segala sesuatu di alam semesta."
Kelebihan: Sangat cocok untuk chatbot, mesin pencari, dan sistem penjawab pertanyaan berbasis teks.
Kekurangan: Hasil bergantung pada kelengkapan konteks.

6. Sentiment Analysis
Pipeline: pipeline("sentiment-analysis")

Analisis:
Fungsi: Menganalisis sentimen dari teks, apakah positif, negatif, atau netral.
Cara Kerja: Model menghitung skor sentimen berdasarkan kata dan frasa dalam teks.
Contoh Kasus:
Input: "The weather was perfect! but I think I will not go outside today."
Hasil: "Positive"
Kelebihan: Berguna untuk analisis media sosial, ulasan produk, dan lainnya.
Kekurangan: Tidak selalu akurat untuk teks dengan sentimen campuran.

7. Summarization
Pipeline: pipeline("summarization")

Analisis:
Fungsi: Merangkum teks panjang menjadi versi lebih singkat dan padat.
Cara Kerja: Model mengidentifikasi bagian penting teks dan menghasilkan ringkasan.
Contoh Kasus:
Input: Penjelasan panjang tentang Perang Napoleon.
Hasil: Ringkasan beberapa kalimat tentang perang dan hasilnya.
Kelebihan: Menghemat waktu dalam membaca teks panjang.
Kekurangan: Kadang kehilangan detail penting.

8. Translation
Pipeline: pipeline("translation", model="Helsinki-NLP/opus-mt-id-en")

Analisis:
Fungsi: Menerjemahkan teks dari satu bahasa ke bahasa lain.
Cara Kerja: Model menerjemahkan kata demi kata dan menyusun kembali menjadi kalimat yang bermakna.
Contoh Kasus:
Input: "menikmati hidup adalah kesukaanku"
Hasil: "Enjoying life is my favorite thing."
Kelebihan: Akurat untuk teks sederhana.
Kekurangan: Kadang mengalami kesalahan untuk kalimat kompleks atau idiomatik.
Kesimpulan:
HuggingFace Transformers menyediakan pipeline serbaguna untuk berbagai tugas NLP. Dengan fleksibilitas ini, developer dapat dengan mudah mengimplementasikan fitur NLP seperti klasifikasi, QA, dan summarization tanpa harus membangun model dari awal. Namun, kinerja model tergantung pada kasus penggunaan spesifik dan data yang digunakan.
