# 🚀 Manga Premium - Production Ready Manga Reader

Premium full-stack manga/manhwa reader with scraping from shinigami.asia. Dark neon theme, PWA, SEO, monetization ready.

![Screenshot](https://via.placeholder.com/1200x600/1a1a2e/00d4ff?text=Manga+Premium)

## ✨ Features
- ✅ Real-time scraping from shinigami.asia (cached)
- ✅ Latest/Trending/Search/Detail/Reader
- ✅ JWT Auth + Bookmark/History
- ✅ Admin panel + Auto-update cron
- ✅ Mobile PWA + SEO + Fast loading
- ✅ Deploy: Vercel + Railway + Supabase

## 🛠️ Quick Start (5 mins)

```bash
# 1. Clone & Install
git clone <repo> manga-premium
cd manga-premium
npm install

# 2. Start DB/Redis (Docker)
npm run docker:up

# 3. DB Setup
cp .env.example .env  # Edit DATABASE_URL if needed
npm run db:push

# 4. Dev Mode
npm run dev
# Frontend: http://localhost:3000
# Backend: http://localhost:5000
```

## 🌐 Production Deploy

### Frontend (Vercel)
```bash
cd frontend
npm i
vercel --prod
```

### Backend + DB (Railway)
1. Railway.app → New Project → Deploy from Git
2. Add vars from .env.example
3. `npx prisma db push`

### Docker Production
```bash
docker build -t manga-backend ./backend -f Dockerfile.backend
docker compose -f docker-compose.prod.yml up
```

## 📱 Test Commands
```bash
# Backend APIs
curl http://localhost:5000/api/home
curl -X POST http://localhost:5000/api/auth/register -d '{"email":"test@test.com","password":"123456"}' -H "Content-Type: application/json"

# Frontend
npm run dev --workspace=frontend
```

## 🛡️ Scraping Notice
- Uses ethical caching (10min+ TTL)
- Rate-limited requests
- For demo/personal use

## 📁 Structure
```
├── frontend/     # Next.js 15
├── backend/      # Express + Prisma
├── prisma/       # PostgreSQL schema
└── shared/       # Types
```

## 🔧 Troubleshooting
- Scraping blocked? → Change user-agent in ShinigamiProvider
- DB issues? → `npm run db:push`
- Redis? → Ensure docker up

**Enjoy reading! 🎉**

