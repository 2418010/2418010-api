2418010-apinews.md
2026-04-13
Dokumentasi ini menjelaskan tentang spesifikasi API pada layanan News Portal khusus untuk data berita.
Base URL
http://localhost:8000/api/
Endpoints
GET /news
Endpoint ini untuk mendapatkan daftar berita
Response
Status: 200 (OK)
Body
{ "status": true, "message": "Berhasil", "data": [ { "id": 1, "judul": "Perkembangan Teknologi 2026", "isi": "Isi
lengkap berita teknologi", "kategori_id": 1, "tanggal": "2026-04-10" } ] }
Status: 404 (Data Not Found)
Body
{ "status": false, "message": "Data tidak ditemukan" }
GET /news/{id}
Endpoint ini untuk mendapatkan detail dari berita
Parameter (PATH)
id: integer (id berita)
Response
Status: 200 (OK)
Body
{ "status": true, "message": "Berhasil", "data": { "id": 1, "judul": "Perkembangan Teknologi 2026", "isi": "Isi
lengkap berita teknologi", "kategori_id": 1, "tanggal": "2026-04-10" } }
POST /news
Endpoint ini untuk menambah berita baru
Request Body
{ "judul": "Berita Terkini", "isi": "Isi berita terbaru hari ini", "kategori_id": 2 }
1 / 2
2418010-apinews.md
2026-04-13
Response
Status: 200 (OK)
Body
{ "status": true, "message": "Berhasil", "data": { "id": 2, "judul": "Berita Terkini", "isi": "Isi berita terbaru hari ini",
"kategori_id": 2 } }
PUT /news/{id}
Endpoint ini untuk memperbarui berita terpilih
Parameter (PATH)
id: integer (id berita)
Request Body
{ "judul": "Berita Update Terbaru", "isi": "Isi berita sudah diperbarui", "kategori_id": 3 }
Response
Status: 200 (OK)
Body
{ "status": true, "message": "Berhasil", "data": { "id": 1, "judul": "Berita Update Terbaru", "isi": "Isi berita sudah
diperbarui", "kategori_id": 3 } }
DELETE /news/{id}
Endpoint ini untuk menghapus berita terpilih
Parameter (PATH)
id: integer (id berita)
Response
Status: 200 (OK)
Body
{ "status": true, "message": "Berhasil", "data": { "id": 1, "judul": "Berita Update Terbaru", "isi": "Isi berita sudah
diperbarui", "kategori_id": 3 } }
2 / 2
