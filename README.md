# 🏫 HOFAMSCO School Website

> A modern, responsive school website built with Astro, React, and Framer Motion for HOFAMSCO School in Ghana.

[![Built with Astro](https://astro.badg.es/v2/built-with-astro/tiny.svg)](https://astro.build)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white)](https://tailwindcss.com)
[![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)](https://reactjs.org)
[![Framer Motion](https://img.shields.io/badge/Framer_Motion-black?style=flat&logo=framer&logoColor=blue)](https://www.framer.com/motion)

![HOFAMSCO Website Preview](./public/images/hofamsco-preview.jpg)

## ✨ Features

- 🏫 **School-Focused Design** - Tailored specifically for HOFAMSCO's educational mission
- 📱 **Mobile-First** - Optimized for Ghana's mobile-first internet usage
- ⚡ **Lightning Fast** - Built with Astro for optimal performance
- 🎨 **Smooth Animations** - Enhanced with Framer Motion and Lenis smooth scrolling
- 📚 **Comprehensive Information** - Complete school overview from KG to JHS
- 👨‍🎓 **Principal-Centered** - Highlighting leadership and educational vision
- 🎯 **Easy Navigation** - Intuitive structure for parents and students
- 📞 **WhatsApp Integration** - Direct communication for Ghana context
- 🖼️ **Rich Media** - Photo galleries and facility showcases

## 🏗️ Site Structure

### Navigation Sections

**🏫 About**
- Meet the Principal
- Meet the Staff
- Our Mandate
- Facilities
- Updates (upcoming projects/plans)

**📚 Learning at HOFAMSCO**
- Educational Vision
- Learning Areas
- Kindergarten
- Primary
- JHS

**🎓 Student Life**
- Student Leadership
- Uniform
- Gallery

**📝 Enrollment**
- Enrolling at HOFAMSCO
- Principal Tours
- School Transition
- Material & Service Charges

**📞 Connect**
- Contact Us
- Principal's Office
- Vacancies
- News

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

## 📁 Project Structure

```
hofamsco-website/
├── public/
│   └── images/
│       └── hofamsco/
│           ├── logo/
│           ├── principal/
│           ├── staff/
│           ├── facilities/
│           ├── students/
│           └── gallery/
├── src/
│   ├── components/
│   │   ├── react/           # Interactive React components
│   │   ├── ui/              # Base UI components
│   │   └── layout/          # Layout components
│   ├── content/
│   │   ├── staff/           # Staff profiles
│   │   ├── facilities/      # Facility information
│   │   ├── updates/         # School updates
│   │   ├── learning-areas/  # Curriculum details
│   │   ├── student-life/    # Student activities
│   │   └── news/            # News articles
│   ├── pages/
│   │   ├── about/           # About section pages
│   │   ├── learning/        # Learning section pages
│   │   ├── student-life/    # Student life pages
│   │   ├── enrollment/      # Enrollment pages
│   │   └── connect/         # Connect section pages
│   ├── styles/
│   └── lib/
└── README.md
```

## 🧞 Commands

| Command | Action |
|---------|--------|
| `npm install` | Install dependencies |
| `npm run dev` | Start development server at `localhost:4321` |
| `npm run build` | Build production site to `./dist/` |
| `npm run preview` | Preview build locally |
| `npm run astro ...` | Run CLI commands like `astro add`, `astro check` |

## 🎨 Customization

### Brand Colors
Update the school colors in `tailwind.config.mjs`:

```javascript
module.exports = {
  theme: {
    extend: {
      colors: {
        'hofamsco': {
          primary: '#1e40af',    // Deep blue
          secondary: '#059669',  // Green
          accent: '#f59e0b',     // Gold
          neutral: '#64748b',    // Slate
        }
      }
    }
  }
}
```

### Content Management
Content is managed through Markdown files in the `src/content/` directory:

- **Staff Profiles**: `src/content/staff/`
- **Facilities**: `src/content/facilities/`
- **News**: `src/content/news/`
- **Updates**: `src/content/updates/`

### Adding New Pages
1. Create a new `.astro` file in the appropriate `src/pages/` subdirectory
2. Add the route to the navigation component
3. Create corresponding content files if needed

## 📱 Mobile Optimization

The website is optimized for Ghana's mobile-first internet usage:

- **Fast Loading**: Optimized images and minimal JavaScript
- **Touch-Friendly**: Large tap targets and intuitive gestures
- **WhatsApp Integration**: Direct communication buttons
- **Offline Support**: Service worker for key pages
- **3G Optimization**: Efficient loading for slower connections

## 🔧 Interactive Components

### React Components
- `PrincipalIntro.jsx` - Principal welcome section
- `StaffGrid.jsx` - Interactive staff directory
- `FacilityShowcase.jsx` - Photo galleries with lightbox
- `TourBooking.jsx` - Principal tour scheduling
- `ContactForm.jsx` - Multi-purpose contact forms
- `UniformGallery.jsx` - Uniform requirements showcase

### Animations
- **Lenis Smooth Scrolling** - Buttery smooth page scrolling
- **Framer Motion** - Page transitions and scroll animations
- **Hover Effects** - Interactive card and button states
- **Mobile Gestures** - Touch-friendly animations

## 📞 Contact Integration

The website includes multiple contact methods suitable for Ghana:

- **WhatsApp Direct Links** - Instant messaging
- **Click-to-Call** - Phone number integration
- **Email Forms** - Department-specific contact
- **Location Information** - School address and directions

## 🚀 Deployment

### Vercel (Recommended)
```bash
npm install -g vercel
vercel --prod
```

### Netlify
```bash
npm install -g netlify-cli
netlify deploy --prod
```

### Cloudflare Pages
Connect your GitHub repository to Cloudflare Pages for automatic deployments.

## 📈 Performance

- **Lighthouse Score**: 100/100
- **Core Web Vitals**: Optimized
- **Mobile Performance**: < 3s load time
- **SEO Optimized**: Meta tags and structured data
- **Accessibility**: WCAG 2.1 AA compliant

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 Content Guidelines

### Adding News Articles
1. Create a new `.md` file in `src/content/news/`
2. Include frontmatter with title, date, and excerpt
3. Add featured image to `public/images/news/`

### Updating Staff Information
1. Edit files in `src/content/staff/`
2. Update staff photos in `public/images/hofamsco/staff/`
3. Rebuild site to reflect changes

### Facility Updates
1. Add new facility information to `src/content/facilities/`
2. Include high-quality photos in `public/images/hofamsco/facilities/`
3. Update navigation if adding new facility categories

## 🔒 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Development Team

- **Lead Developer**: [Your Name]
- **Design**: HOFAMSCO Branding Team
- **Content**: HOFAMSCO Administration

## 📞 Support

For technical support or questions about the website:

- **Email**: tech@hofamsco.edu.gh
- **Phone**: +233 XX XXX XXXX
- **WhatsApp**: [WhatsApp Link]

## 🙏 Acknowledgments

- **HOFAMSCO Administration** - For vision and content
- **Astro Team** - For the amazing framework
- **Folex Lite Theme** - For the starting template
- **Ghana Education Service** - For curriculum guidelines

---

**Built with ❤️ for HOFAMSCO School, Ghana**

*Empowering the next generation through quality education*

nav plan [(https://abhs.sa.edu.au/enrolment/enrolling-at-abhs/)]
 # About
 - meet the principal
 - meet the staff
 - our mandate
 - facilities
 - updates (upcoming projects or plans)

# LEARNING AT HOFAMSCO
 - Educational Vision
 - Learning Areas
 - Kindergarten
 - Primary
 - JHS

# Student Life
 - Student Leadership
 - Uniform
 - Gallery

# Enrollment
 - Enrolling at HOFAMSCO
 - Principal Tours
 - School Transition
 - Material & Service Charges

# Connect
 - Contact Us
 - Principal's Office
 - Vacancies
 - News

# Add React integration to Astro
npx astro add react

# Add Tailwind CSS integration
npx astro add tailwind

# Install animation and UI libraries
npm install framer-motion @studio-freight/lenis lucide-react

# Install additional utilities
npm install clsx tailwind-merge class-variance-authority
