# Changelog

All notable changes to ShutterCoach will be documented in this file.
Dates reflect approximate release months (no tagged releases).

## [1.3] - 2026-03-22

### Chrome Extension

- **Chrome Web Store launch** — ShutterCoach is now available as a Chrome extension
- Right-click any photo on the web for instant AI critique
- Two modes: **Study** (analyze any web photo) and **Coach** (upload your own)
- Follow-up chat with Luna after every critique
- Canvas-rendered share cards to show off your scores
- Critique history stored locally in the browser
- Aurora glass UI matching the iOS app's design language
- Clerk authentication with account management
- Stripe one-time payment ($9.99) for lifetime access
- Stripe Customer Portal for billing management
- GDPR data export and account deletion
- Datadog RUM observability integration
- EU analytics consent notice
- Post-update feature discovery notifications
- LunaOrb animated component in idle home view
- Daily photography tips and Luna messages on idle screen

### iOS App

- **Profile tab** — New dedicated user hub replacing Settings, with avatars, glass hierarchy, aurora gradients, and stats ribbon
- **iOS 26 Liquid Glass** — Progressive enhancement for the latest iOS design language
- **Aurora v2 background system** — Redesigned ambient background across all screens
- **Onboarding v3** — Premium-feeling visual overhaul with glass buttons
- **Guided 5-day onboarding journey** — Trial banner, daily notifications, Day 5 interstitial
- **Personalized paywall** — Shows trial stats (critiques taken, scores earned) in paywall header
- **Widget aurora rework** — Merged widgets with streak display and shared SPM package
- Expanded achievement and milestone system with 5 new categories
- Batch cull aurora palette blending
- App Store screenshot automation pipeline

### Backend

- **Cloudflare AI Gateway** — All LLM calls routed through AI Gateway for monitoring and caching
- **Cloudflare Queues** — Resilient webhook processing with DLQ consumer
- **Admin metrics endpoint** — Cost and conversion dashboarding via Analytics Engine
- **DAU/MAU tracking** — Session webhook handler for usage analytics
- **Tier sync via JWT claims** — Read tier from Clerk JWT to skip KV/D1 lookups
- Chat follow-up endpoint with context window management
- Permanent share URLs with OG meta tags
- Stripe webhook handler for payment confirmation
- Stripe promotion codes in Checkout
- Structured cost and error logging for extension routes
- Paid/trial daily rate limits for extension critiques

### Web

- **Migrated Vue 3 to Svelte 5** and **UnoCSS to Tailwind v4**
- Massive SEO expansion — 27 to 225+ pages
- Global ambient Canvas 2D aurora background (replacing CSS)
- JSON-LD structured data (Organization, WebSite, page-level)
- Privacy policy updated to cover both iOS app and Chrome extension
- Pricing and legal pages updated for one-time purchase model

### Security & Infrastructure

- Server-side trial validation and CSP hardening
- Mandatory Clerk auth for extension (closed trial abuse loophole)
- GlassCard ARIA accessibility audit
- D1 replication lag fallback handling
- Clerk JWT cache and CSP error handling improvements

## [1.2] - 2026-03-08

### iOS App

- **Pricing pivot** — Replaced 3-tier subscription model with 5-day free trial + $9.99 one-time lifetime purchase
- StoreKit 2 non-consumable IAP integration
- Stripped subscription tier infrastructure
- Trial and lifetime purchase migration hardening
- Post-trial glass wall UX — gates batch import, shows unlock nudge
- 5-day trial with hard paywall post-trial (0 free critiques)
- App Review rejection fixes — grandfather date and restore button alerts

### Backend

- Clerk webhook handler and user row provisioning
- D1 tier migration for binary free/paid model

### Web

- Pricing page and legal updates for one-time purchase model

## [1.1] - 2026-02-01

### Added
- Critique revision engine — compare before/after improvements
- Premium streaming feedback with Aurora morphing animations
- Luna AI mentor avatar in chat
- Challenge difficulty levels and improved streak tracking

### Improved
- Faster critique delivery with streaming responses
- Enhanced Photo DNA accuracy
- Expanded offline critique history (500 critiques)

## [1.0] - 2026-01-01

### Added
- AI-powered photo critique across 6 skills
- Photo DNA — personalized photography profile
- Daily photography challenges with streak tracking
- Interactive follow-up chat with AI mentor
- Achievements and milestones system
- 5-day free trial + $9.99 one-time purchase
- Offline critique history
- Privacy-first design (photos never stored server-side)
