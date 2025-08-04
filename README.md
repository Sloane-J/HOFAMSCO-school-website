# 🏫 HOFAMSCO School Website - Implementation Plan

> A modern, responsive school website built with Astro, React, and Framer Motion for HOFAMSCO School in Ghana.

[![Built with Astro](https://astro.badg.es/v2/built-with-astro/tiny.svg)](https://astro.build)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white)](https://tailwindcss.com)
[![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)](https://reactjs.org)
[![Framer Motion](https://img.shields.io/badge/Framer_Motion-black?style=flat&logo=framer&logoColor=blue)](https://www.framer.com/motion)

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/hofamsco-website.git
cd hofamsco-website

# Install dependencies
npm install

# Start development server
npm run dev
```

Open [http://localhost:4321](http://localhost:4321) to view the website.

## 🛠️ Tech Stack

| Technology | Purpose | Version |
|------------|---------|---------|
| **Astro** | Static Site Generator | 5.x |
| **React** | Interactive Components | 18.x |
| **Tailwind CSS** | Styling Framework | 4.x |
| **Framer Motion** | Animations | Latest |
| **Lenis** | Smooth Scrolling | Latest |
| **Lucide React** | Icons | Latest |

## 📁 Complete Project Structure & File Implementation

```
hofamsco-website/
├── 📁 public/
│   ├── favicon.ico
│   ├── robots.txt
│   ├── sitemap.xml
│   └── 📁 images/
│       └── 📁 hofamsco/
│           ├── 📁 logo/
│           │   ├── logo-main.png          # Main school logo
│           │   ├── logo-white.png         # White version for dark backgrounds
│           │   └── logo-icon.png          # Square icon version
│           ├── 📁 hero/
│           │   ├── hero-main.jpg          # Homepage hero image
│           │   ├── hero-students.jpg      # Students in classroom
│           │   └── hero-campus.jpg        # Campus overview
│           ├── 📁 principal/
│           │   ├── principal-portrait.jpg # Principal's professional photo
│           │   ├── principal-office.jpg   # Principal's office
│           │   └── principal-students.jpg # Principal with students
│           ├── 📁 staff/
│           │   ├── teacher-1.jpg          # Individual teacher photos
│           │   ├── teacher-2.jpg
│           │   ├── teacher-3.jpg
│           │   ├── staff-meeting.jpg      # Group staff photo
│           │   └── staff-group.jpg        # All staff photo
│           ├── 📁 facilities/
│           │   ├── classroom-kg.jpg       # Kindergarten classroom
│           │   ├── classroom-primary.jpg  # Primary classroom
│           │   ├── classroom-jhs.jpg      # JHS classroom
│           │   ├── library.jpg            # School library
│           │   ├── computer-lab.jpg       # ICT center
│           │   ├── playground.jpg         # Play area
│           │   ├── assembly-hall.jpg      # Main hall
│           │   ├── dining-hall.jpg        # Cafeteria
│           │   └── sports-field.jpg       # Sports facilities
│           ├── 📁 students/
│           │   ├── kg-students.jpg        # Kindergarten students
│           │   ├── primary-students.jpg   # Primary students
│           │   ├── jhs-students.jpg       # JHS students
│           │   ├── student-activities.jpg # Extra-curricular
│           │   ├── graduation.jpg         # Graduation ceremony
│           │   └── uniform-display.jpg    # Students in uniform
│           ├── 📁 activities/
│           │   ├── sports-day.jpg         # Annual sports day
│           │   ├── cultural-day.jpg       # Cultural activities
│           │   ├── science-fair.jpg       # Academic events
│           │   ├── prize-giving.jpg       # Award ceremonies
│           │   └── field-trip.jpg         # Educational trips
│           └── 📁 gallery/
│               ├── gallery-1.jpg          # General school photos
│               ├── gallery-2.jpg
│               ├── gallery-3.jpg
│               ├── gallery-4.jpg
│               └── gallery-5.jpg
├── 📁 src/
│   ├── 📁 components/
│   │   ├── 📁 layout/
│   │   │   ├── Header.astro              # Main navigation header
│   │   │   ├── Footer.astro              # Site footer with links
│   │   │   ├── Layout.astro              # Base page layout
│   │   │   ├── Navigation.astro          # Main navigation menu
│   │   │   └── MobileMenu.astro          # Mobile navigation
│   │   ├── 📁 ui/
│   │   │   ├── Button.astro              # Reusable button component
│   │   │   ├── Card.astro                # Card component for content
│   │   │   ├── Hero.astro          ****      # Hero section component
│   │   │   ├── Section.astro             # Page section wrapper
│   │   │   ├── ContactInfo.astro     ****    # Contact details component
│   │   │   └── WhatsAppButton.astro      # WhatsApp contact button
│   │   └── 📁 react/
│   │       ├── PrincipalIntro.jsx        # Interactive principal welcome
│   │       ├── StaffGrid.jsx             # Staff directory with filtering
│   │       ├── FacilityShowcase.jsx      # Interactive facility gallery
│   │       ├── ImageGallery.jsx          # Photo gallery with lightbox
│   │       ├── ContactForm.jsx           # Contact/inquiry forms
│   │       ├── TourBooking.jsx           # Principal tour scheduling
│   │       ├── UniformGallery.jsx        # Uniform requirements display
│   │       ├── NewsCarousel.jsx          # News and updates carousel
│   │       ├── FeeCalculator.jsx         # School fees calculator
│   │       └── SmoothScrolling.jsx       # Lenis smooth scroll setup
│   ├── 📁 pages/
│   │   ├── index.astro                   # Homepage - school overview
│   │   ├── 📁 about/
│   │   │   ├── index.astro               # About section landing
│   │   │   ├── principal.astro           # Meet the Principal page
│   │   │   ├── staff.astro               # Meet the Staff page
│   │   │   ├── mandate.astro             # School mission & vision
│   │   │   ├── facilities.astro          # School facilities tour
│   │   │   └── updates.astro             # Current projects & plans
│   │   ├── 📁 learning/
│   │   │   ├── index.astro               # Learning section overview
│   │   │   ├── vision.astro              # Educational philosophy
│   │   │   ├── areas.astro               # Learning areas & subjects
│   │   │   ├── kindergarten.astro        # KG program details
│   │   │   ├── primary.astro             # Primary school program
│   │   │   └── jhs.astro                 # Junior High School program
│   │   ├── 📁 student-life/
│   │   │   ├── index.astro               # Student life overview
│   │   │   ├── leadership.astro          # Student leadership programs
│   │   │   ├── uniform.astro             # Uniform requirements
│   │   │   ├── activities.astro          # Extra-curricular activities
│   │   │   └── gallery.astro             # Student life photo gallery
│   │   ├── 📁 enrollment/
│   │   │   ├── index.astro               # Enrollment overview
│   │   │   ├── process.astro             # How to enroll
│   │   │   ├── tours.astro               # Principal tours booking
│   │   │   ├── transition.astro          # School transition support
│   │   │   └── fees.astro                # Fees & charges breakdown
│   │   └── 📁 connect/
│   │       ├── index.astro               # Connect section overview
│   │       ├── contact.astro             # Contact information
│   │       ├── office.astro              # Principal's office hours
│   │       ├── vacancies.astro           # Job opportunities
│   │       └── news.astro                # School news & announcements
│   ├── 📁 styles/
│   │   ├── global.css                    # Global styles & CSS reset
│   │   └── components.css                # Component-specific styles
│   └── 📁 lib/
│       ├── utils.js                      # Utility functions
│       ├── constants.js                  # Site constants & config
│       └── data.js                       # Hardcoded school data
├── 📁 config files/
│   ├── astro.config.mjs                  # Astro configuration
│   ├── tailwind.config.mjs               # Tailwind CSS config
│   ├── tsconfig.json                     # TypeScript config
│   └── package.json                      # Dependencies & scripts
└── README.md
```

## 📄 File Descriptions & Content Structure

### 🏠 Homepage (`src/pages/index.astro`)
**Purpose**: School overview and first impression
**Content Includes**:
- Hero section with school motto
- Principal's welcome message
- Quick stats (students, staff, years established)
- Featured facilities preview
- Recent news highlights
- Call-to-action for enrollment

### 🏫 About Section

#### `src/pages/about/principal.astro`
**Purpose**: Principal introduction and leadership
**Content Structure**:
```javascript
const principalData = {
  name: "Dr. [Name]",
  title: "Principal",
  qualifications: ["Ph.D Education", "M.Ed Administration"],
  experience: "15+ years in education",
  message: "Welcome message...",
  achievements: [],
  image: "/images/hofamsco/principal/principal-portrait.jpg"
}
```

#### `src/pages/about/staff.astro`
**Purpose**: Staff directory and qualifications
**Content Structure**:
```javascript
const staffMembers = [
  {
    name: "Teacher Name",
    position: "Subject Teacher",
    qualifications: ["B.Ed Mathematics"],
    subjects: ["Mathematics", "Science"],
    experience: "5 years",
    image: "/images/hofamsco/staff/teacher-1.jpg"
  }
  // ... more staff
]
```

#### `src/pages/about/facilities.astro`
**Purpose**: School infrastructure showcase
**Content Structure**:
```javascript
const facilities = [
  {
    name: "Computer Laboratory",
    description: "Modern ICT center with 30 computers",
    features: ["High-speed internet", "Projector", "Air conditioning"],
    capacity: "30 students",
    image: "/images/hofamsco/facilities/computer-lab.jpg"
  }
  // ... more facilities
]
```

### 📚 Learning Section

#### `src/pages/learning/kindergarten.astro`
**Purpose**: KG program details
**Content Structure**:
```javascript
const kgProgram = {
  ageRange: "3-5 years",
  classes: ["KG1", "KG2"],
  subjects: ["Numeracy", "Literacy", "Creative Arts"],
  activities: ["Play-based learning", "Story time", "Art & crafts"],
  teacherRatio: "1:15",
  facilities: ["Playground", "KG classrooms", "Toy library"]
}
```

### 🎓 Student Life Section

#### `src/pages/student-life/uniform.astro`
**Purpose**: Uniform requirements and policies
**Content Structure**:
```javascript
const uniformRequirements = {
  boys: {
    daily: {
      shirt: "White short/long sleeve",
      trousers: "Navy blue",
      shoes: "Black leather",
      socks: "White",
      tie: "School tie"
    },
    sports: {
      shirt: "School PE shirt",
      shorts: "Navy blue",
      shoes: "White sneakers"
    }
  },
  girls: {
    // Similar structure
  },
  suppliers: [
    {
      name: "Uniform Shop Name",
      location: "Koforidua Market",
      contact: "+233XXXXXXXXX"
    }
  ]
}
```

### 📝 Enrollment Section

#### `src/pages/enrollment/fees.astro`
**Purpose**: Fee structure and payment information
**Content Structure**:
```javascript
const feeStructure = {
  kg: {
    tuition: 1200,
    books: 150,
    uniform: 200,
    transport: 300,
    total: 1850
  },
  primary: {
    tuition: 1500,
    books: 200,
    uniform: 250,
    transport: 300,
    total: 2250
  },
  jhs: {
    tuition: 1800,
    books: 250,
    uniform: 300,
    transport: 300,
    total: 2650
  },
  paymentTerms: "Per term",
  paymentMethods: ["Bank transfer", "Mobile money", "Cash"]
}
```

## 🧞 Development Commands

| Command | Action |
|---------|--------|
| `npm install` | Install dependencies |
| `npm run dev` | Start development server at `localhost:4321` |
| `npm run build` | Build production site to `./dist/` |
| `npm run preview` | Preview build locally |
| `npm run astro ...` | Run CLI commands like `astro add`, `astro check` |

## 📱 Mobile-First Implementation

### Responsive Design Strategy
- **Mobile breakpoint**: 320px - 768px
- **Tablet breakpoint**: 768px - 1024px
- **Desktop breakpoint**: 1024px+

### Ghana-Specific Optimizations
- WhatsApp integration on every contact point
- Click-to-call phone numbers
- Optimized for 3G connections
- Offline-capable service worker
- Local Ghana educational context

## 🎨 Styling & Theming

### Brand Colors (`tailwind.config.mjs`)
```javascript
colors: {
  hofamsco: {
    // Primary Colors - School Brand
    blue: {
      50: '#eff6ff',       // Very light blue background
      100: '#dbeafe',      // Light blue tint
      500: '#3b82f6',      // Main school blue
      600: '#2563eb',      // Darker blue for hover states
      700: '#1d4ed8',      // Deep blue for text
      900: '#1e3a8a'       // Very dark blue
    },
    red: {
      50: '#fef2f2',       // Very light red background
      100: '#fee2e2',      // Light red tint
      500: '#ef4444',      // Main school red
      600: '#dc2626',      // Darker red for hover states
      700: '#b91c1c',      // Deep red for accents
      900: '#7f1d1d'       // Very dark red
    },
    white: '#ffffff',      // Pure white

    // Supporting Colors
    gray: {
      50: '#f9fafb',       // Off-white background
      100: '#f3f4f6',      // Light gray
      300: '#d1d5db',      // Medium light gray
      500: '#6b7280',      // Medium gray for text
      700: '#374151',      // Dark gray for headings
      900: '#111827'       // Very dark gray/black
    },

    // Semantic Colors
    success: '#10b981',    // Green for success states
    warning: '#f59e0b',    // Amber for warnings
    info: '#0ea5e9',       // Sky blue for info

    // Background Colors
    background: {
      primary: '#ffffff',   // Main white background
      secondary: '#f8fafc', // Light gray background
      accent: '#eff6ff'     // Light blue background
    }
  }
}
```

## 🔧 Interactive Components Details

### `PrincipalIntro.jsx`
- Animated entrance
- Audio message player (optional)
- Social proof metrics
- Call-to-action buttons

### `StaffGrid.jsx`
- Filterable by department
- Search functionality
- Modal popups for detailed bios
- Responsive grid layout

### `FacilityShowcase.jsx`
- Interactive facility tour
- 360° photos (future enhancement)
- Booking system integration
- Virtual tour capabilities

### `ContactForm.jsx`
- Multi-step form for inquiries
- WhatsApp integration
- Email notifications
- Form validation

## 🚀 Deployment Strategy

### Recommended: Vercel
```bash
npm install -g vercel
vercel --prod
```

### Alternative: Netlify
```bash
npm install -g netlify-cli
netlify deploy --prod
```

### Custom Domain Setup
1. Purchase `hofamsco.edu.gh` domain
2. Configure DNS settings
3. Set up SSL certificate
4. Configure redirects

## 📊 Analytics & SEO

### SEO Implementation
- Meta tags for all pages
- Open Graph images
- Structured data markup
- Sitemap generation
- Robot.txt optimization

### Ghana Education Keywords
- "Private school Koforidua"
- "Best kindergarten Eastern Region"
- "JHS school Ghana"
- "Quality education Koforidua"

## 🔒 Security & Performance

### Performance Targets
- **First Contentful Paint**: < 1.5s
- **Largest Contentful Paint**: < 2.5s
- **Cumulative Layout Shift**: < 0.1
- **First Input Delay**: < 100ms

### Security Measures
- Content Security Policy headers
- HTTPS enforcement
- Input sanitization
- Rate limiting on forms

## 👨‍💻 Development Workflow

### Content Updates Process
1. Edit data objects in respective `.astro` files
2. Add new images to `public/images/hofamsco/`
3. Test locally with `npm run dev`
4. Build and deploy: `npm run build && vercel --prod`

### Adding New Pages
1. Create `.astro` file in appropriate directory
2. Update navigation in `src/components/layout/Navigation.astro`
3. Add route to sitemap
4. Test responsive design

---

**Built with ❤️ for HOFAMSCO School, Ghana**
*Empowering the next generation through quality education*
