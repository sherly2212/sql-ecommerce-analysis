# sql-ecommerce-analysis
# Analisis SQL: Interaksi Pengguna E-Commerce

Proyek lanjutan dari [analisis Python](https://github.com/sherly2212/ecommerce-interaction-analysis).
Data yang sama dianalisis ulang menggunakan SQL (SQLite) untuk
menunjukkan kemampuan query.

## Tools
Python, Pandas, SQLite, Google Colab

## Data
Sumber: Kaggle, dataset "e-commerce-sales-data-2024" oleh datascientist97.
- Tabel `interaksi`: 2.999 baris (setelah baris kosong dihapus)
- Tabel `produk`: 10.002 baris
- Cek integritas: 0 interaksi tanpa pasangan di tabel produk

## Pertanyaan dan Teknik SQL

| No | Pertanyaan | Teknik |
|---|---|---|
| 1 | Berapa proporsi view, like, purchase? | GROUP BY, window function (SUM OVER) |
| 2 | Subkategori mana dengan porsi purchase tertinggi? | JOIN, CASE WHEN, HAVING, INSTR/SUBSTR |
| 3 | Bagaimana tren interaksi per bulan? | STRFTIME, CASE WHEN |
| 4 | Bulan mana yang paling ramai? | CTE (WITH), RANK |

## Temuan
1. Like 39,9%, view 30,3%, purchase 29,8% (dari 2.871 interaksi
   yang punya jenis).
2. Subkategori dengan sampel besar dan porsi purchase tinggi:
   ... (isi dari hasil Query 2)
3. Interaksi memuncak pada ... (isi dari hasil Query 4), dengan
   periode Oktober-Desember 2023 paling tinggi.

## Catatan dan Keterbatasan
- Hasil SQL dicocokkan dengan hasil Pandas pada proyek sebelumnya.
- Setiap user hanya muncul sekali, sehingga conversion rate
  tidak bisa dihitung.
- 128 baris tanpa jenis interaksi dikeluarkan dari analisis.
- Data kemungkinan sintetis.
- Dataset tidak disertakan di repository, unduh dari Kaggle.
