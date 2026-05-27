# Modern Portfolio Website

A clean, modern, and fully responsive portfolio website built with vanilla HTML, CSS, and JavaScript.

## Features

✨ **Modern Design**
- Sleek gradient color scheme
- Smooth animations and transitions
- Fully responsive layout (mobile-first design)
- Parallax scrolling effects

🎯 **Functionality**
- Responsive navigation with mobile menu
- Smooth scroll navigation
- Interactive contact form
- Intersection Observer for scroll animations
- Scroll-to-top button
- Keyboard navigation support

📱 **Sections**
- Hero section with call-to-action buttons
- About section with stats
- Featured projects showcase
- Skills and expertise grid
- Contact form with validation
- Social media links
- Footer

## Project Structure

```
portfolio/
├── index.html          # Main HTML file
├── css/
│   └── styles.css      # All styling with CSS variables
├── js/
│   └── script.js       # JavaScript interactivity
└── assets/             # Images and media (ready for use)
```

## Customization Guide

### 1. **Update Personal Information**

Edit `index.html` and replace:
- `Your Name` - Your actual name
- `Your City, Country` - Your location
- `hello@example.com` - Your email
- Social media links in contact section

### 2. **Add Your Projects**

In the Projects section, update the three project cards with your actual projects:
```html
<h3 class="project-title">Your Project Name</h3>
<p class="project-description">Your project description</p>
<div class="project-tags">
    <span class="tag">Technology1</span>
    <span class="tag">Technology2</span>
</div>
<a href="your-project-link" class="project-link">View Project →</a>
```

### 3. **Add Project Images**

Replace the placeholder `.image-placeholder` divs with actual images:
```html
<div class="project-image">
    <img src="assets/project-name.jpg" alt="Project Name">
</div>
```

Then add this CSS for proper image display:
```css
.project-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
```

### 4. **Customize Colors**

Edit the CSS variables in `css/styles.css`:
```css
:root {
    --primary-color: #6366f1;      /* Change main color */
    --secondary-color: #ec4899;    /* Change accent color */
    --text-primary: #1e293b;       /* Text color */
    --background-color: #ffffff;   /* Background */
    /* ... other variables ... */
}
```

### 5. **Update Skills**

Modify the Skills section with your actual skills:
```html
<div class="skill-category">
    <h3>Your Category</h3>
    <ul>
        <li>Your Skill 1</li>
        <li>Your Skill 2</li>
    </ul>
</div>
```

### 6. **Connect Contact Form**

Currently, the form shows a local success message. To make it functional:

**Option A: EmailJS Integration**
```javascript
// Add to js/script.js
emailjs.init("YOUR_PUBLIC_KEY");

contactForm.addEventListener('submit', (e) => {
    e.preventDefault();
    emailjs.sendForm("YOUR_SERVICE_ID", "YOUR_TEMPLATE_ID", contactForm)
        .then(() => showNotification('Email sent!', 'success'))
        .catch(() => showNotification('Error sending email', 'error'));
});
```

**Option B: Formspree**
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" id="contactForm">
    <!-- form fields -->
</form>
```

**Option C: Backend API**
Point form to your backend endpoint for email handling.

## Installation & Usage

### Local Development

1. **Open directly in browser:**
   - Double-click `index.html` to open in your default browser
   - Or drag it to your browser window

2. **Using a local server (recommended):**
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Python 2
   python -m SimpleHTTPServer 8000
   
   # Using Node.js http-server
   npx http-server
   ```
   Then visit `http://localhost:8000`

### Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Features Breakdown

### Mobile Menu
- Responsive hamburger menu on screens < 768px
- Click to toggle, click again to close
- Automatic close when link is clicked
- Keyboard support (Esc to close)

### Smooth Scrolling
- CSS smooth scroll behavior
- Active link highlighting as you scroll
- Fixed navigation bar

### Form Validation
- Validates name, email, and message fields
- Email format validation
- User feedback with notifications

### Animations
- Fade-in on page load
- Slide-up animations for cards
- Hover effects on interactive elements
- Parallax background movement

## Performance Tips

1. **Optimize Images:**
   - Use modern formats (WebP, AVIF)
   - Compress images before adding to assets/
   - Use responsive images with srcset

2. **Lazy Loading:**
   - Add `loading="lazy"` to images

3. **Code Optimization:**
   - Minify CSS and JavaScript for production
   - Remove unused animations if needed

## Deployment

### Free Hosting Options

**Vercel:**
```bash
npm install -g vercel
vercel
```

**Netlify:**
- Drag and drop folder to netlify.com
- Or use CLI: `netlify deploy`

**GitHub Pages:**
1. Create repository named `username.github.io`
2. Push files to main branch
3. Site goes live at `https://username.github.io`

**Cloudflare Pages:**
1. Connect GitHub repository
2. Build command: (leave empty for static)
3. Deploy

## Accessibility

- Semantic HTML structure
- Proper heading hierarchy
- ARIA labels on interactive elements
- Keyboard navigation support
- High contrast colors (WCAG compliant)
- Alt text ready for images

## SEO Optimization

Update meta tags in `index.html`:
```html
<meta name="description" content="Your portfolio description">
<meta name="keywords" content="portfolio, web developer, your skills">
<meta property="og:title" content="Your Portfolio">
<meta property="og:description" content="Your portfolio description">
```

## License

Free to use and modify. Attribution appreciated but not required.

## Support

For issues or questions:
1. Check browser console for errors (F12)
2. Ensure all file paths are correct
3. Test in different browsers
4. Check file permissions

---

**Happy coding! 🚀**
