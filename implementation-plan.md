# HOFAMSCO School Website Implementation Plan

## Phase 1: Project Setup & Dependencies

### 1.1 Clone and Setup Base Project
```bash
git clone https://github.com/getastrothemes/folex-lite-astro.git hofamsco-website
cd hofamsco-website
npm install
```

### 1.2 Install Additional Dependencies
```bash
# Smooth scrolling
npm install @studio-freight/lenis


# React components and animations
npm install @astrojs/react react react-dom
npm install framer-motion

# Icons and UI enhancements
npm install lucide-react
npm install @headlessui/react

# Form handling (for contact forms)
npm install react-hook-form

# Image optimization
npm install @astrojs/image sharp

# Date handling
npm install date-fns

# Modal/Dialog components
npm install @radix-ui/react-dialog
```

### 1.3 Update Astro Config
```javascript
// astro.config.mjs - Add React integration
import { defineConfig } from 'astro/config';
import react from '@astrojs/react';
import tailwind from '@astrojs/tailwind';

export default defineConfig({
  integrations: [react(), tailwind()],
});
```

## Phase 2: Content Structure & Collections

### 2.1 Create HOFAMSCO-Specific Content Collections
```bash
# Create new content directories
mkdir -p src/content/staff
mkdir -p src/content/facilities
mkdir -p src/content/updates
mkdir -p src/content/learning-areas
mkdir -p src/content/student-life
mkdir -p src/content/news
mkdir -p src/content/gallery
```

### 2.2 Content Collection Schema Updates
Update `src/content.config.ts` for:
- Staff profiles (Principal, Teachers, Support Staff)
- Facilities information
- School updates/projects
- Learning areas and curriculum
- Student life activities
- News and announcements
- Gallery collections

### 2.3 Sample Content Files to Create
```
src/content/staff/
├── principal.md
├── teachers/
│   ├── kindergarten-teachers.md
│   ├── primary-teachers.md
│   └── jhs-teachers.md
└── support-staff.md

src/content/facilities/
├── classrooms.md
├── library.md
├── computer-lab.md
├── playground.md
└── dining-hall.md

src/content/updates/
├── new-science-lab.md
├── playground-renovation.md
└── ict-program.md

src/content/learning-areas/
├── kindergarten-curriculum.md
├── primary-subjects.md
└── jhs-programs.md

src/content/student-life/
├── student-leadership.md
├── uniform-policy.md
└── extracurricular.md

src/content/news/
├── term-opening.md
├── graduation-ceremony.md
└── sports-day.md
```

## Phase 3: Page Structure Based on HOFAMSCO Navigation

### 3.1 Homepage Redesign (`src/pages/index.astro`)
**HOFAMSCO homepage sections:**
- Hero: School name, motto, welcome message
- Quick overview of educational vision
- Recent news highlights
- Upcoming events/updates
- Call-to-action for enrollment
- Photo showcase

### 3.2 Create Pages According to Navigation Structure

#### About Section
```bash
src/pages/about/
├── index.astro                 # About overview
├── principal.astro             # Meet the Principal
├── staff.astro                 # Meet the Staff
├── mandate.astro               # Our Mandate
├── facilities.astro            # Facilities
└── updates.astro               # Updates (projects/plans)
```

#### Learning at HOFAMSCO Section
```bash
src/pages/learning/
├── index.astro                 # Learning overview
├── educational-vision.astro    # Educational Vision
├── learning-areas.astro        # Learning Areas
├── kindergarten.astro          # Kindergarten
├── primary.astro               # Primary
└── jhs.astro                   # JHS
```

#### Student Life Section
```bash
src/pages/student-life/
├── index.astro                 # Student Life overview
├── leadership.astro            # Student Leadership
├── uniform.astro               # Uniform
└── gallery.astro               # Gallery
```

#### Enrollment Section
```bash
src/pages/enrollment/
├── index.astro                 # Enrollment overview
├── enrolling.astro             # Enrolling at HOFAMSCO
├── tours.astro                 # Principal Tours
├── transition.astro            # School Transition
└── charges.astro               # Material & Service Charges
```

#### Connect Section
```bash
src/pages/connect/
├── index.astro                 # Connect overview
├── contact.astro               # Contact Us
├── principal-office.astro      # Principal's Office
├── vacancies.astro             # Vacancies
└── news.astro                  # News
```

### 3.3 Update Navigation (`src/components/Header.astro`)
**HOFAMSCO Navigation Structure:**
- Home
- About (dropdown: Principal, Staff, Mandate, Facilities, Updates)
- Learning at HOFAMSCO (dropdown: Educational Vision, Learning Areas, Kindergarten, Primary, JHS)
- Student Life (dropdown: Student Leadership, Uniform, Gallery)
- Enrollment (dropdown: Enrolling, Principal Tours, School Transition, Charges)
- Connect (dropdown: Contact Us, Principal's Office, Vacancies, News)

## Phase 4: React Components Development

### 4.1 Interactive Components to Build
```bash
# Create React components directory
mkdir -p src/components/react
```

**HOFAMSCO-Specific Components:**
- `PrincipalIntro.jsx` - Principal welcome message with photo
- `StaffGrid.jsx` - Interactive staff directory with filtering
- `FacilityShowcase.jsx` - 3D facility tours/photo galleries
- `UpdatesTimeline.jsx` - School projects and plans timeline
- `LearningAreasCarousel.jsx` - Subject areas showcase
- `UniformGallery.jsx` - Uniform requirements with photos
- `StudentLeadershipBoard.jsx` - Student council showcase
- `TourBooking.jsx` - Principal tour scheduling
- `ContactForm.jsx` - Multi-purpose contact form
- `NewsGrid.jsx` - Latest news with filtering
- `ChargesCalculator.jsx` - School fees calculator
- `GalleryLightbox.jsx` - Photo gallery with categories

### 4.2 Framer Motion Animations
**HOFAMSCO Animation Patterns:**
- Smooth page transitions between sections
- Principal's welcome animation on homepage
- Staff card hover effects and reveals
- Facility showcase parallax scrolling
- Timeline animations for updates/projects
- Gallery photo reveal animations
- Mobile-friendly touch gestures

## Phase 5: HOFAMSCO Brand Identity & Styling

### 5.1 Brand Colors & Typography
**HOFAMSCO Brand Guidelines:**
```css
/* Primary school colors - likely blue/green/gold */
:root {
  --hofamsco-primary: #1e40af;     /* Deep blue */
  --hofamsco-secondary: #059669;   /* Green */
  --hofamsco-accent: #f59e0b;      /* Gold */
  --hofamsco-neutral: #64748b;     /* Slate */
  --hofamsco-light: #f8fafc;       /* Light background */
}
```

### 5.2 Component Styling Updates
**HOFAMSCO-specific design elements:**
- Principal's photo and welcome section
- Staff profile cards with role badges
- Facility showcase with modern layouts
- Learning area subject cards
- Uniform requirement displays
- Fee structure tables
- Contact information cards

### 5.3 Mobile-First Design (Priority for Ghana)
```css
/* Mobile optimization for HOFAMSCO */
.hofamsco-container {
  /* Fast loading on 3G networks */
  /* Touch-friendly navigation */
  /* Optimized images */
}
```

## Phase 6: HOFAMSCO Content Management

### 6.1 Image Assets Organization
```bash
# Organize HOFAMSCO images
public/images/
├── hofamsco/
│   ├── logo/
│   ├── principal/
│   ├── staff/
│   ├── facilities/
│   │   ├── classrooms/
│   │   ├── library/
│   │   ├── computer-lab/
│   │   └── playground/
│   ├── students/
│   │   ├── uniform/
│   │   ├── leadership/
│   │   └── activities/
│   ├── learning/
│   │   ├── kindergarten/
│   │   ├── primary/
│   │   └── jhs/
│   └── updates/
└── gallery/
    ├── events/
    ├── ceremonies/
    └── daily-life/
```

### 6.2 Content Strategy for HOFAMSCO
**Key content areas to develop:**
- Principal's biography and educational philosophy
- Staff profiles with qualifications and photos
- School mandate and mission statement
- Detailed facility descriptions with photos
- Current and planned school updates/projects
- Educational vision and teaching methodology
- Curriculum details for each level (KG, Primary, JHS)
- Student leadership structure and opportunities
- Uniform requirements and policies
- Enrollment process and requirements
- Principal tour scheduling and information
- School transition support programs
- Detailed fee structure and payment information
- Contact information for different departments
- Job vacancy postings
- Regular news updates and announcements

## Phase 7: HOFAMSCO-Specific Features

### 7.1 Principal-Focused Features
- Principal's welcome video/message
- Principal tour booking system
- Principal's office contact information
- Principal's educational philosophy page

### 7.2 Student-Centered Features
- Student leadership board showcase
- Uniform gallery with detailed requirements
- Student life photo galleries
- Extracurricular activity highlights

### 7.3 Parent/Guardian Features
- Clear enrollment process walkthrough
- School transition support information
- Detailed material and service charges
- Multiple contact methods for different needs

### 7.4 Ghana Context Integration
- WhatsApp contact buttons for instant communication
- Mobile-optimized design for smartphone users
- Fast loading for slower internet connections
- Local Ghana contact number formatting
- School location and directions

## Phase 8: Forms & Communication (Frontend Only)

### 8.1 Contact & Inquiry Forms
- General contact form with department routing
- Principal tour request form
- Enrollment inquiry form
- Vacancy application form
- School feedback form

### 8.2 Communication Features (Static Implementation)
- WhatsApp direct chat buttons
- Phone number click-to-call functionality
- Email contact links
- Contact information for different departments
- Social media links (if applicable)

### 8.3 Form Handling Options (Frontend)
```bash
# For static forms, integrate with:
# - Formspree (https://formspree.io/)
# - Netlify Forms (if deploying to Netlify)
# - EmailJS for client-side email sending
npm install @emailjs/browser
```

## Phase 9: Performance & Smooth Scrolling

### 9.1 Lenis Smooth Scrolling Implementation
```javascript
// src/components/SmoothScroll.astro
---
// Lenis smooth scrolling setup for HOFAMSCO
---
<script>
import Lenis from '@studio-freight/lenis'

// Initialize Lenis with mobile-friendly settings
const lenis = new Lenis({
  duration: 1.2,
  easing: (t) => Math.min(1, 1.001 - Math.pow(2, -10 * t)),
  smoothTouch: false, // Keep native mobile scrolling
  wheelMultiplier: 0.8, // Gentle desktop scrolling
  touchMultiplier: 1.5, // Responsive touch scrolling
  infinite: false,
  gestureDirection: 'vertical'
});

// Animation frame loop
function raf(time) {
  lenis.raf(time)
  requestAnimationFrame(raf)
}
requestAnimationFrame(raf)

// Scroll to sections for navigation
window.scrollToSection = (target) => {
  lenis.scrollTo(target, { offset: -80 })
}
</script>
```

### 9.2 SEO Optimization for HOFAMSCO
```javascript
// Meta tags for each page section
const seoData = {
  about: "Learn about HOFAMSCO School - Meet our Principal, Staff, and explore our facilities",
  learning: "Educational excellence at HOFAMSCO - Kindergarten, Primary, and JHS programs",
  studentLife: "Student life at HOFAMSCO - Leadership, uniform, and school community",
  enrollment: "Enroll at HOFAMSCO School - Admissions, tours, and fee information",
  connect: "Contact HOFAMSCO School - Get in touch with our Principal's office"
}
```

## Phase 10: Testing & Deployment

### 10.1 HOFAMSCO Pre-Launch Testing
- Cross-browser compatibility (Chrome, Safari, Firefox)
- Mobile responsiveness on various devices
- Form functionality testing (contact, inquiries)
- Image loading and gallery performance
- Navigation dropdown functionality
- WhatsApp and phone link testing
- Page loading speed optimization

### 10.2 Deployment Options for HOFAMSCO
**Recommended for Ghana context:**
```bash
# Vercel (recommended - fast global CDN)
npm install -g vercel
vercel --prod

# Netlify (great for forms)
npm install -g netlify-cli
netlify deploy --prod

# Cloudflare Pages (excellent for Africa)
# GitHub Pages (free option)
```

### 10.3 Performance Optimization
```bash
# Build optimization commands
npm run build
npm run preview

# Check bundle size
npx astro build --analyze

# Image optimization
npm run astro optimize
```

## Phase 11: HOFAMSCO Launch Checklist

### 11.1 Content Verification
- [ ] Principal's biography and photo
- [ ] Complete staff directory with photos
- [ ] School mandate clearly stated
- [ ] All facilities documented with photos
- [ ] Current updates/projects listed
- [ ] Educational vision articulated
- [ ] Learning areas detailed for each level
- [ ] Student leadership structure explained
- [ ] Uniform requirements with photos
- [ ] Gallery populated with school photos
- [ ] Enrollment process clearly outlined
- [ ] Principal tour information complete
- [ ] School transition support detailed
- [ ] Material & service charges listed
- [ ] All contact information accurate
- [ ] Vacancy postings (if any)
- [ ] Recent news updated

### 11.2 Technical Verification
- [ ] All navigation dropdowns working
- [ ] Contact forms functional
- [ ] WhatsApp integration tested
- [ ] Mobile optimization verified
- [ ] Loading speed < 3 seconds
- [ ] SEO meta tags configured
- [ ] Analytics setup (optional)
- [ ] Favicon and branding complete

## Timeline Estimate

**Week 1:** Project setup, navigation structure, basic pages
**Week 2:** Content creation and React components development
**Week 3:** Styling, branding, and mobile optimization
**Week 4:** Interactive features, forms, and animations
**Week 5:** Content population and image organization
**Week 6:** Testing, performance optimization, and deployment

## Key Success Metrics for HOFAMSCO

- Clear information hierarchy matching navigation
- Mobile-first responsive design
- Fast loading times for Ghana internet speeds
- Easy-to-find contact information
- Professional presentation of school leadership
- Comprehensive enrollment information
- Engaging student life showcase
- Smooth user experience with animations

## Maintenance Plan

- Monthly news updates
- Quarterly staff/facility updates
- Annual content review and refresh
- Regular photo gallery updates
- Ongoing vacancy postings as needed
# next steps
