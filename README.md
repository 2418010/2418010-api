# 2418010-api
# DOKUMENTASI API PORTAL BERITA

Dokumentasi ini berisi penjelasan penggunaan API Portal Berita.

---

## BASE URL
http://localhost:8000/api/

---

## API KATEGORI

### 1. Menampilkan Seluruh Kategori

**Endpoint**
GET /category

**Keterangan**
Digunakan untuk mengambil semua data kategori.

**Respon Berhasil (200)**


```json
{
  "success": true,
  "info": "Daftar kategori berhasil ditampilkan",
  "result": [
    {
      "id": 1,
      "nama": "Teknologi",
      "slug": "teknologi"
    }
  ]
}
