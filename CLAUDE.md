# CLAUDE.md

This file provides guidance to Claude Code when working with the Peluquería Canina Truman website.

## Project Overview

Peluquería Canina Truman is a professional dog grooming salon website for a business located in Ronda, Spain. The website is built as a **single-file HTML application** with no external dependencies or build tools, following a self-contained pattern for easy deployment and maintenance.

## Technical Architecture

### Single-File Pattern

The entire website is contained in `index.html`:
```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <style>/* All CSS embedded here */</style>
  </head>
  <body>
    <!-- HTML structure -->
  </body>
</html>
```

**IMPORTANT:** Maintain this single-file architecture. Do not split into separate CSS/JS files or introduce build tools unless explicitly requested.

### Technology Stack

- **HTML5** - Semantic markup
- **CSS3** - Embedded styles with modern features (Grid, Flexbox, gradients)
- **No JavaScript** - Static website, no client-side scripting required
- **Responsive Design** - Mobile-first approach with media queries

## Content Guidelines

### Language and Tone

- **Language:** Spanish (Spain) - "Español de España" AND English
- **Tone:** Professional, elegant, warm, and welcoming
- **Target Audience:** Pet owners in Ronda and surrounding areas (local and international tourists)

**CRITICAL: Bilingual Requirement**
- The website supports BOTH Spanish and English versions
- ANY changes to website content MUST be applied to BOTH language versions
- Language switcher in navigation allows users to toggle between 🇪🇸 Spanish and 🇬🇧 English
- Maintain content parity: updates to services, hours, descriptions, etc. must be translated
- Keep the same structure and layout for both language versions

### Visual Style

- **Color Scheme:** Purple gradient theme (#667eea to #764ba2)
- **Design:** Clean, modern, elegant with smooth transitions
- **Images:** 
  - Dog photos from Unsplash (real photos of healthy dogs)
  - Local imagery: "Ronda Spain.png" (local file showing Ronda)
  - All images should convey professionalism and pet care quality

### Sections Structure

1. **Header** - Business name and tagline
2. **Navigation** - Smooth scroll to sections
3. **Inicio** (Home) - Welcome message and introduction
4. **Galería** (Gallery) - 6 dog breeds showcasing services
5. **Servicios** (Services) - 5 service cards:
   - Corte y Peinado (Cut and Styling)
   - Baño Completo (Complete Bath)
   - Corte de Uñas (Nail Trimming)
   - Limpieza de Oídos (Ear Cleaning)
   - Tratamientos Especiales (Special Treatments)
6. **Ubicación** (Location) - Ronda section with local image
7. **Contacto** (Contact) - Contact information cards

### Contact Information

**Address:** Calle Nueva, 25, 29400 Ronda, Málaga, España  
**Phone:** +34 952 87 12 34  
**Email:** info@peluqueriatruman.es  
**Hours:**
- Lunes a Viernes: 9:00 - 19:00
- Sábados: 9:00 - 14:00
- Domingos: Cerrado

**IMPORTANT:** These contact details are part of the business identity. Only change if explicitly requested by the user.

## Assets

### Images

- **Dog Gallery Images:** Hosted on Unsplash (external URLs)
  - Golden Retriever
  - Caniche (Poodle)
  - Husky Siberiano
  - Yorkshire Terrier
  - Labrador
  - Shih Tzu

- **Local Images:**
  - `Ronda Spain.png` - Aerial/scenic view of Ronda (3.8 MB PNG file)

### Image Guidelines

When updating images:
- Prefer high-quality, professional photos
- Ensure images show healthy, well-groomed dogs
- Maintain aspect ratio and proper sizing (600x400px for gallery)
- Keep local images optimized for web (consider compression if needed)

## Deployment

### GitHub Repository

**Repository:** https://github.com/robertooya/peluqueria-canina-truman  
**Branch:** main  
**Owner:** robertooya

### GitHub Pages

**Live URL:** https://robertooya.github.io/peluqueria-canina-truman/

The website is automatically deployed via GitHub Pages from the main branch.

**Deployment Workflow:**
1. Make changes locally to `index.html` or assets
2. Commit changes: `git add .` → `git commit -m "message"`
3. Push to GitHub: `git push origin main`
4. GitHub Pages automatically rebuilds (1-2 minutes)
5. Changes are live at the public URL

### Git Workflow

All commits should include the co-author tag:
```
Co-Authored-By: Claude Sonnet 4.5 <noreply@anthropic.com>
```

**IMPORTANT:** Always sync changes to GitHub after modifications to keep the live site up to date.

## Maintenance Guidelines

### Making Changes

1. **Content Updates:**
   - Services, hours, contact info → Edit directly in `index.html`
   - **CRITICAL:** Apply ALL content changes to BOTH Spanish AND English sections
   - Always maintain professional tone in both languages
   - Verify translations are accurate and culturally appropriate

2. **Design Updates:**
   - Preserve the purple gradient theme unless requested otherwise
   - Maintain responsive design for all screen sizes
   - Keep hover effects and transitions for professional feel
   - Design changes apply globally (shared across both language versions)

3. **Image Updates:**
   - Replace Unsplash URLs if images break
   - Optimize local images if file size becomes an issue
   - Ensure new images match the professional aesthetic
   - Images are shared across both languages

### Testing

Before pushing changes:
1. Open `index.html` locally in a browser
2. Test all navigation links
3. Verify responsive design (resize browser window)
4. Check all images load correctly
5. Verify contact information is accurate

### Common Tasks

**IMPORTANT:** All content changes must be made in BOTH Spanish and English sections of the HTML.

**Update contact hours:**
- Edit the "Horario" section in the contact cards for Spanish version
- Edit the "Hours" section in the contact cards for English version

**Add a new service:**
- Duplicate a `.service-card` div in BOTH language sections
- Update the emoji, title (h3), and description (p) in Spanish
- Update the emoji, title (h3), and description (p) in English
- Ensure service offerings match across both languages

**Change images:**
- Update the `src` attribute in the gallery `<img>` tags
- Ensure new URLs are valid and images are accessible
- Images are shared across both languages (no translation needed)

**Update Ronda image:**
- Replace `Ronda Spain.png` file in the project directory
- Keep the same filename or update the `src` in HTML

## SEO Considerations

The website is designed to be discovered by search engines:
- Semantic HTML structure
- Descriptive alt tags on images
- Clear heading hierarchy (h1, h2, h3)
- Meta description in head (Spanish language)

To improve search ranking:
- Submit to Google Search Console: https://search.google.com/search-console
- Verify property: https://robertooya.github.io/peluqueria-canina-truman/
- Request indexing for faster discovery

## Browser Compatibility

The website uses modern CSS features but maintains broad compatibility:
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

All features degrade gracefully on older browsers.

## File Structure

```
Perruqueria Truman/
├── index.html              # Main website file (single-file app)
├── Ronda Spain.png         # Local image of Ronda
├── CLAUDE.md              # This file - instructions for Claude Code
├── README.md              # Project documentation
└── .git/                  # Git repository
```

## Notes

- No build process required - direct HTML deployment
- No package.json, no dependencies, no npm/node needed
- GitHub Pages serves static files directly
- Changes are immediately visible after git push + GitHub Pages rebuild
