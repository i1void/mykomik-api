# MyKomik API

<img src="https://file.herta.web.id/x/6bc05fb5.jpg" width="600" alt="Preview">

REST API untuk membaca Manhwa Bahasa Indonesia, bersumber dari [kiryuu.one](https://kiryuu.one/).

---

## Tech Stack

- **Node.js**
- **Express.js**

---

## Base URL

```
https://mykomik-api.vercel.app/api
```

---

## Endpoints

### 📚 Manhwa

| Method | Endpoint | Deskripsi |
|--------|----------|-----------|
| GET | `/manhwa-new` | Manhwa terbaru |
| GET | `/manhwa-popular` | Manhwa populer |
| GET | `/manhwa-ongoing` | Manhwa ongoing |
| GET | `/manhwa-recommendation` | Manhwa rekomendasi |
| GET | `/manhwa-recommend` | Manhwa rekomendasi mingguan |
| GET | `/manhwa-detail/:manhwaId` | Detail manhwa |

### 🏷️ Genres

| Method | Endpoint | Deskripsi |
|--------|----------|-----------|
| GET | `/genres` | List semua genre |
| GET | `/genre/:genreId` | Manhwa berdasarkan genre |
| GET | `/genre/:genreId/page/:pageNumber` | Manhwa berdasarkan genre dengan pagination |

### 🔍 Search

| Method | Endpoint | Deskripsi |
|--------|----------|-----------|
| GET | `/search/:searchId` | Pencarian manhwa |
| GET | `/page/:pageNumber/search/:searchId` | Pencarian manhwa dengan pagination |

### 📖 Chapter

| Method | Endpoint | Deskripsi |
|--------|----------|-----------|
| GET | `/chapter/:chapterId` | Baca chapter manhwa |

---

## Installation

```bash
git clone https://github.com/111void/mykomik-api.git
cd mykomik-api
npm install
npm start
```

---

## Example Response

```json
{
  "title": "Return of The Greatest Lancer",
  "link": "https://kiryuu.one/manga/return-of-the-greatest-lancer/",
  "imageSrc": "https://example.com/image.jpg",
  "chapters": [
    {
      "chapterLink": "https://kiryuu.one/return-of-the-greatest-lancer-chapter-151/",
      "chapterTitle": "Ch.151",
      "timeAgo": "3 jam lalu"
    }
  ]
}
```
