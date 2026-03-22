# 🎵 Spotify To JioSaavn Playlist Data Exporter API

A powerful backend service that **extracts Spotify playlists** and **converts them into JioSaavn-compatible data** for use inside my custom music app **Musify** 🚀

🔗 **Frontend Project**
👉  **[Musify](https://github.com/itz-Harsh/Musify)**  

---

## ✨ What This Does

This backend acts as a **bridge between Spotify and JioSaavn** for extracting the favorite playlist of spotify.
 
You give it a **Spotify playlist URL**, and it will:
- 🔐 Authenticate with Spotify securely (no user login required)
- 🎶 Extract all playlist tracks
- 🔍 Search each track on JioSaavn
- 📦 Return a **JioSaavn-style playlist JSON**
- 🎧 Ready to plug directly into **Musify**

In short:  
**Spotify playlist → My own JioSaavn music app**

---

## 🧠 Why I Built This

Spotify doesn’t allow direct streaming outside their ecosystem.  
JioSaavn provides streamable content but lacks Spotify playlist imports.

So I built this backend to:
- Own the data flow
- Avoid frontend secrets
- Enable cross-platform playlist migration
- Power my personal music app **Musify**

This is not a scraper — it’s an **API translation layer**.

---

## ⚙️ Tech Stack

- 🐍 Python
- ⚡ FastAPI
- 🎧 Spotipy (Spotify Web API)
- 🔁 OAuth 2.0 Refresh Token Flow
- 🌐 JioSaavn Public API
- 🔐 Environment-based secrets
- ☁️ Production-ready backend design

---

## 🔐 Authentication Flow (Spotify)

- Uses **Client ID + Client Secret**
- Uses a **Refresh Token**
- Automatically fetches new access tokens
- No browser login
- No OAuth popup
- Fully backend-safe

---

## 🚀 API Endpoints

### Health Check
GET /

Response:
```
{
  "status": "API is Fine !"
}
```

### Convert Spotify Playlist → JioSaavn Playlist
GET /api/{spotify_playlist_url}

Response:
```
{
  "success": true,
  "data": {
    "type": "playlist",
    "year": "2025-01-01",
    "image": "cover_image_url",
    "songs": [ ... ]
  }
}

```
---

## 🛠️ Environment Variables

Create a `.env` file:

SPOTIPY_CLIENT_ID=your_client_id  
SPOTIPY_CLIENT_SECRET=your_client_secret  
SPOTIFY_REFRESH_TOKEN=your_refresh_token  
SPOTIPY_REDIRECT_URI=your_redirect_uri  

---

## 🎧 Musify Integration

Built specifically for **Musify — My Custom Music Streaming App**  
👉 https://github.com/itz-Harsh/Musify

---

## 🧑‍💻 Author

**Harsh**  
Computer Science Engineer | Full-Stack Developer

Music should be free to move 🎶
