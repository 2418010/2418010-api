# DOKUMENTASI API NEWS PORTAL

**Nama:** Teofilu Verceli Ngamal  
**NIM:** 2418010  
**Kelas:** A  

---

## Deskripsi
Dokumentasi ini menjelaskan tentang spesifikasi API pada layanan News Portal khusus untuk data berita.

---

## BASE URL
http://localhost:8000/api/

---

## ENDPOINTS

---

### 1. GET /news
Menampilkan daftar semua berita

#### Response
**Status: 200 (OK)**
```json
{
  "status": true,
  "message": "Berhasil",
  "data": [
    {
      "id": 1,
      "judul": "Perkembangan Teknologi 2026",
      "isi": "Isi lengkap berita teknologi",
      "kategori_id": 1,
      "tanggal": "2026-04-10"
    }
  ]
}

Status: 404 (Not Found)

{
  "status": false,
  "message": "Data tidak ditemukan"
}
2. GET /news/{id}

Menampilkan detail berita berdasarkan ID

Parameter
id (integer) → ID berita
Response

Status: 200 (OK)

{
  "status": true,
  "message": "Berhasil",
  "data": {
    "id": 1,
    "judul": "Perkembangan Teknologi 2026",
    "isi": "Isi lengkap berita teknologi",
    "kategori_id": 1,
    "tanggal": "2026-04-10"
  }
}
3. POST /news

Menambahkan berita baru

Request Body
{
  "judul": "Berita Terkini",
  "isi": "Isi berita terbaru hari ini",
  "kategori_id": 2
}
Response

Status: 200 (OK)

{
  "status": true,
  "message": "Berhasil",
  "data": {
    "id": 2,
    "judul": "Berita Terkini",
    "isi": "Isi berita terbaru hari ini",
    "kategori_id": 2
  }
}
4. PUT /news/{id}

Memperbarui data berita

Parameter
id (integer) → ID berita
Request Body
{
  "judul": "Berita Update Terbaru",
  "isi": "Isi berita sudah diperbarui",
  "kategori_id": 3
}
Response

Status: 200 (OK)

{
  "status": true,
  "message": "Berhasil",
  "data": {
    "id": 1,
    "judul": "Berita Update Terbaru",
    "isi": "Isi berita sudah diperbarui",
    "kategori_id": 3
  }
}
5. DELETE /news/{id}

Menghapus berita berdasarkan ID

Parameter
id (integer) → ID berita
Response

Status: 200 (OK)

{
  "status": true,
  "message": "Berhasil",
  "data": {
    "id": 1,
    "judul": "Berita Update Terbaru",
    "isi": "Isi berita sudah diperbarui",
    "kategori_id": 3
  }
}
