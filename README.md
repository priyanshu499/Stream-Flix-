# StreamFlix - Modern Movie Discovery Platform

A modern, cinematic movie website built with Next.js, featuring a Netflix-like UI/UX design with real-time movie data from TMDB API.

![Next.js](https://img.shields.io/badge/Next.js-16.2-black?style=for-the-badge&logo=next.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?style=for-the-badge&logo=typescript)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4.0-38bdf8?style=for-the-badge&logo=tailwind-css)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-11.0-ff69b4?style=for-the-badge&logo=framer-motion)

## 🎬 Features

- **Cinematic UI/UX**: Netflix-inspired dark theme with blue accent colors and glassmorphism effects
- **Hero Banner**: Full-screen hero section with trending movies, animated particles, and call-to-action buttons
- **Movie Cards**: Interactive cards with hover animations, ratings, and play button overlays
- **Movie Details**: Comprehensive movie information including cast, crew, trailers, and recommendations
- **Search System**: Advanced search with debounced input, genre filters, year filters, and sorting options
- **Category Pages**: Dedicated pages for Popular, Top Rated, Upcoming, and Now Playing movies
- **Trailer Modal**: YouTube trailer playback in a modal with smooth animations
- **Loading States**: Beautiful loading spinners for better user experience
- **Custom 404 Page**: Cinematic 404 error page with animations
- **Responsive Design**: Fully responsive across desktop, tablet, and mobile devices

### Planned Features
- User authentication (signup, login, JWT)
- User dashboard with watchlist and favorites
- Admin dashboard with analytics
- AI-powered recommendations
- Voice search
- Real-time chat during streaming

## 🚀 Tech Stack

### Frontend
- **Next.js 16.2** - React framework with App Router
- **TypeScript** - Type-safe development
- **Tailwind CSS 4.0** - Utility-first CSS framework
- **Framer Motion** - Animation library
- **ShadCN UI** - Component library
- **Lucide React** - Icon library

### API & Data
- **TMDB API** - Real movie data, posters, trailers, and metadata
- **React Server Components** - Optimized data fetching

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/moviesflix.git
   cd moviesflix
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   
   Copy `.env.example` to `.env.local`:
   ```bash
   cp .env.example .env.local
   ```
   
   Get your TMDB API key from [https://www.themoviedb.org/settings/api](https://www.themoviedb.org/settings/api)
   
   Update `.env.local`:
   ```env
   NEXT_PUBLIC_TMDB_API_KEY=your_tmdb_api_key_here
   NEXT_PUBLIC_TMDB_BASE_URL=https://api.themoviedb.org/3
   NEXT_PUBLIC_TMDB_IMAGE_BASE_URL=https://image.tmdb.org/t/p
   ```

4. **Run the development server**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   
   Navigate to [http://localhost:3000](http://localhost:3000)

## 🏗️ Project Structure

```
moviesflix/
├── src/
│   ├── app/
│   │   ├── movie/
│   │   │   └── [id]/
│   │   │       └── page.tsx          # Movie details page
│   │   ├── search/
│   │   │   └── page.tsx              # Search page with filters
│   │   ├── globals.css               # Global styles
│   │   ├── layout.tsx                # Root layout
│   │   └── page.tsx                  # Home page
│   ├── components/
│   │   ├── Hero.tsx                  # Hero banner component
│   │   ├── MovieCard.tsx             # Movie card with animations
│   │   ├── MovieRow.tsx              # Horizontal movie slider
│   │   └── Navbar.tsx                # Navigation bar
│   ├── lib/
│   │   ├── tmdb.ts                   # TMDB API utilities
│   │   └── utils.ts                  # Utility functions
│   └── types/
│       └── movie.ts                  # TypeScript interfaces
├── .env.local                        # Environment variables (gitignored)
├── .env.example                      # Environment variables template
├── package.json
├── tailwind.config.ts
└── tsconfig.json
```

## 🎨 Key Components

### Hero Component
- Full-screen backdrop with gradient overlays
- Animated particles effect
- Movie metadata display
- Call-to-action buttons with hover effects

### MovieCard Component
- Poster image with hover zoom
- Rating badge
- Play button overlay
- Smooth scale animations on hover

### MovieRow Component
- Horizontal scrolling carousel
- Navigation buttons
- Responsive grid layout

### Search System
- Debounced input (500ms delay)
- Genre filter dropdown
- Year filter dropdown
- Sort by popularity/rating/date
- Active filter chips with remove option

## 🌐 API Integration

The application uses the TMDB (The Movie Database) API to fetch:
- Trending movies
- Popular movies
- Top-rated movies
- Upcoming releases
- Movie details (cast, crew, videos)
- Search results with filters

All API calls are cached using Next.js revalidation (1 hour) for optimal performance.

## 🎯 Pages

### Home Page (`/`)
- Hero banner featuring trending movie
- Movie rows: Trending, Popular, Top Rated, Upcoming
- Navigation to all categories

### Movie Details (`/movie/[id]`)
- Large backdrop image
- Movie poster
- Overview and metadata
- Genre tags
- Director information
- Cast grid
- Similar movies
- Recommendations
- Trailer link

### Search (`/search`)
- Search input with debouncing
- Filter panel (genre, year, sort)
- Results grid
- Active filter management

## 🚧 Future Enhancements

1. **Authentication System**
   - User signup/login
   - JWT-based sessions
   - Google OAuth integration

2. **User Dashboard**
   - Personalized watchlist
   - Favorites management
   - Viewing history
   - Recommendations based on history

3. **Admin Dashboard**
   - Movie management
   - User management
   - Analytics with charts
   - Content moderation

4. **Advanced Features**
   - AI-powered recommendations
   - Voice search
   - Real-time chat
   - Multi-language support
   - Video streaming

## 📝 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## 📧 Contact

For questions or suggestions, please open an issue on GitHub.

---

Built with ❤️ using Next.js and TMDB API
