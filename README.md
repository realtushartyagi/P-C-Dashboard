# Dynamic Content Aggregator

## 📋 Project Overview
An intelligent, fully-responsive web application that curates and displays personalized content streams including breaking news, entertainment recommendations, and community updates.  Built with modern React patterns and enterprise-grade state management.

## 🌐 Deployment
**Production URL**: [https://p-c-dashboard.vercel.app]

**Walkthrough Video**: [https://drive.google.com/file/d/12_YukC7BdbTD9P22sv2OgTMwtV_xuJxY/view?usp=drive_link]

## 🎨 Key Capabilities

### Essential Features ✅
- **Multi-Source Content Integration** leveraging three distinct REST APIs
- **Dynamic Card Components** featuring rich media, titles, summaries, and action buttons
- **Adaptive Layout System** with collapsible navigation and responsive header
- **Smart Search Engine** with optimized debouncing for real-time queries
- **Bookmark Management** enabling users to curate favorite content items
- **Persistent User Settings** stored locally for seamless experience

### Premium Experience ✅
- **Flexible Layout Customization** through intuitive drag-and-drop interface
- **Theme Switching System** between light and dark modes with state preservation
- **Fluid Page Transitions** using advanced animation libraries
- **Progressive Content Loading** with infinite scroll pagination
- **Skeleton Screens** and comprehensive error state management

### Application State ✅
- **Centralized Store** using Redux Toolkit architecture
- **Asynchronous Operations** handled via createAsyncThunk
- **Browser Storage Sync** for preference persistence
- **Reactive Updates** propagating across component tree

### User Access Control ✅
- **OAuth 2.0 Integration** supporting GitHub provider
- **Environment-based Configuration** for sensitive credentials
- **Session Management** with protected route guards

### Quality Assurance ✅
- **Component Testing** using Jest with React Testing Library
- **Feature Integration Tests** validating user workflows
- **Browser Automation** via Cypress for E2E scenarios
- **Mock Service Layer** for consistent test data

## 💻 Technology Foundation

- **Framework**: Next.js 14 (App Directory), TypeScript, React 18
- **UI Layer**: Tailwind CSS, Framer Motion
- **State**:  Redux Toolkit with redux-persist
- **Auth**: NextAuth.js with OAuth providers
- **Quality**: Jest, React Testing Library, Cypress
- **Data Sources**: NewsAPI, TMDB API, JSONPlaceholder
- **Hosting**: Vercel Platform
- **Development**:  ESLint, Prettier, TypeScript strict mode

## 🔧 Local Development Setup

### System Requirements
- Node.js version 18.17 or higher
- npm/yarn/pnpm package manager
- Active GitHub account
- API credentials (see configuration section)

### Quick Start Guide

1. **Clone this repository**
   ```bash
   git clone https://github.com/realtushartyagi/P-C-Dashboard.git
   cd P-C-Dashboard.git
   ```

2. **Install project dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Configure environment variables**
   
   Create `.env.local` in project root:
   ```env
   NEXTAUTH_URL=http://localhost:3000
   NEXTAUTH_SECRET=generate-a-secure-random-string
   
   GITHUB_ID=your-github-app-client-id
   GITHUB_SECRET=your-github-app-client-secret
   
   NEWS_API_KEY=your-newsapi-key-here
   TMDB_API_KEY=your-tmdb-api-key-here
   ```

4. **Obtain API credentials**
   - **News Data**: Sign up at [newsapi.org](https://newsapi.org/register)
   - **Movie Database**: Register at [themoviedb.org/settings/api](https://www.themoviedb.org/settings/api)
   - **GitHub OAuth**: Configure at [github.com/settings/developers](https://github.com/settings/developers)

5. **Start development server**
   ```bash
   npm run dev
   ```

6. **Access application**
   
   Navigate to [http://localhost:3000](http://localhost:3000)

## 🧪 Testing Framework

### Execute Test Suites
```bash
# Component & unit tests
npm test

# Generate coverage reports
npm run test:coverage

# Interactive E2E testing
npm run cypress:open

# Headless E2E execution
npm run cypress:run

# Complete CI/CD test suite
npm run test:ci
```

### Coverage Metrics
- **Unit Layer**: 85%+ coverage across components and state logic
- **Integration Layer**: Key user interaction scenarios
- **E2E Layer**: Complete authentication, search, and customization workflows

## 🎯 User Journey Mapping

### Authentication Sequence
1. User initiates sign-in via GitHub button
2. OAuth flow redirects to GitHub authorization
3. Callback processes authentication tokens
4. Dashboard loads with personalized session data

### Content Exploration
1. Browse curated feed matching user interests
2. Execute real-time search across all content types
3. Apply category filters (news/movies/social)
4. Access trending and recommended sections

### Personalization Controls
1. Mark/unmark content as favorites
2. Reorganize dashboard sections via drag-and-drop
3. Switch between light/dark themes
4. Update content preferences through settings panel

### Content Engagement
1. Access original sources through external links
2. View comprehensive details and metadata
3. Interact with social content elements
4. Continuously load more content through scroll

## 📂 Project Structure
```
.
├── app/                          # Next.js app directory
│   ├── api/                      # Backend API routes
│   │   ├── auth/[...nextauth]/   # Authentication handler
│   │   ├── news/                 # News aggregation endpoint
│   │   ├── movies/               # Entertainment data endpoint
│   │   └── social/               # Social feed endpoint
│   ├── globals.css               # Tailwind directives & global styles
│   ├── layout.tsx                # Root layout wrapper
│   ├── page. tsx                  # Dashboard entry point
│   └── providers. tsx             # Context providers
├── components/                   # React components library
│   ├── DraggableLayout.tsx       # Layout customization
│   ├── FavoritesSection.tsx      # Saved items display
│   ├── Header. tsx                # Top navigation bar
│   ├── MoviesFeed.tsx            # Entertainment grid
│   ├── NewsFeed.tsx              # Article listing
│   ├── SearchBar.tsx             # Search interface
│   └── SocialFeed.tsx            # Community content
├── lib/                          # Core utilities
│   ├── slices/                   # Redux state slices
│   │   ├── newsSlice.ts          
│   │   ├── moviesSlice.ts        
│   │   ├── socialSlice.ts        
│   │   └── preferencesSlice.ts   
│   ├── hooks. ts                  # Custom React hooks
│   └── store.ts                  # Redux store config
├── __tests__/                    # Jest test files
├── cypress/                      # E2E test specs
└── public/                       # Static resources
```

## ✅ Requirements Checklist

| Feature Category | Status | Details |
|-----------------|---------|---------|
| Content Aggregation | ✅ | Three API integrations with preference filtering |
| Card-based UI | ✅ | Media-rich components with CTAs and interactions |
| Responsive Layout | ✅ | Mobile-first approach with adaptive navigation |
| Search Capability | ✅ | Debounced universal search across categories |
| Layout Reordering | ✅ | Drag-drop with local persistence |
| Theme Toggle | ✅ | Dark/light modes with localStorage |
| State Management | ✅ | Redux Toolkit with async middleware |
| Test Coverage | ✅ | Unit, integration, and E2E suites |
| Authentication | ✅ | OAuth implementation (bonus feature) |

## ⚡ Optimization Strategies

- **Search Throttling**: Minimizes API requests during text input
- **Component Lazy Loading**: On-demand module imports
- **Next.js Image**:  Automatic format and size optimization
- **Bundle Splitting**: Intelligent code chunking
- **State Persistence**: Redux store serialization
- **Error Boundaries**: Fault-tolerant component tree

## 🔐 Security Implementation

- **Secret Management**: All keys in environment variables
- **OAuth Flow**: Industry-standard authentication
- **CSRF Tokens**: Built-in NextAuth protection
- **XSS Prevention**: Input validation and sanitization
- **HTTP Headers**: Next.js security defaults applied

## 🚀 Roadmap Considerations

- Live data streaming with WebSocket integration
- Internationalization (i18n) support
- User behavior analytics dashboard
- Browser push notification system
- Progressive Web App (PWA) capabilities
- Advanced content filtering algorithms

## 📚 Attribution

- [Next.js Documentation](https://nextjs.org/docs) - React framework
- [Redux Toolkit](https://redux-toolkit.js.org/) - State management
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS
- [NewsAPI](https://newsapi.org) - News data provider
- [TMDB](https://www.themoviedb.org) - Entertainment database
- [Vercel](https://vercel.com) - Deployment platform

---

**Developed by**: [@realtushartyagi](https://github.com/realtushartyagi)

**License**: MIT

**Last Updated**: December 2025
