# Personal Portfolio Website

A modern, responsive personal portfolio website built with HTML, CSS, and JavaScript. Features a clean design, dark/light mode toggle, smooth animations, and a working contact form.

## 🌟 Features

- **Responsive Design**: Mobile-first approach that works on all devices
- **Dark/Light Mode**: Toggle between themes with localStorage persistence
- **Smooth Animations**: Intersection Observer API for scroll-based animations
- **Contact Form**: Integrated with EmailJS for email functionality
- **SEO Optimized**: Proper meta tags, semantic HTML, and performance optimization
- **Modern UI**: Clean design with smooth transitions and hover effects
- **Accessibility**: ARIA labels, keyboard navigation, and proper contrast ratios

## 🚀 Live Demo

Open `index.html` in your browser or serve it through a local server.

## 📋 Sections

1. **Home**: Hero section with animated typing effect
2. **About Me**: Personal introduction with statistics
3. **Skills**: Animated skill bars organized by categories
4. **Projects**: Showcase of featured projects with links
5. **Contact**: Contact form with validation and social links

## 🛠️ Setup Instructions

### 1. Basic Setup
1. Download or clone this repository
2. Open `index.html` in your browser
3. The website is ready to use!

### 2. EmailJS Configuration (For Contact Form)

To enable the contact form functionality:

1. Sign up for a free account at [EmailJS](https://www.emailjs.com/)
2. Create a new email service (Gmail, Outlook, etc.)
3. Create an email template with the following variables:
   - `{{from_name}}` - Sender's name
   - `{{from_email}}` - Sender's email
   - `{{subject}}` - Email subject
   - `{{message}}` - Email message
4. Get your Service ID, Template ID, and Public Key
5. Add the EmailJS script to your HTML (already included):
   ```html
   <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
   ```
6. Update the following in `script.js`:
   ```javascript
   // Replace with your actual EmailJS credentials
   emailjs.init('YOUR_PUBLIC_KEY');
   
   // In the handleFormSubmit method:
   await emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', templateParams);
   ```

### 3. Customization

#### Personal Information
Update the following in `index.html`:
- Name and title in the header and hero section
- About me text and statistics
- Skills and proficiency levels
- Project information and links
- Contact information and social media links

#### Colors and Styling
Modify CSS variables in `styles.css`:
```css
:root {
  --primary-color: #2563eb;
  --secondary-color: #10b981;
  --accent-color: #f59e0b;
  /* Add more custom colors */
}
```

#### Images
- Add your profile picture to the `assets` folder
- Update image placeholders in the HTML with your actual images
- Add project screenshots to showcase your work

## 📁 File Structure

```
portfolio/
│
├── index.html          # Main HTML file
├── styles.css          # CSS styles and animations
├── script.js           # JavaScript functionality
├── README.md           # Project documentation
├── assets/             # Images, icons, and other assets
│   └── favicon.ico     # Website favicon
└── emailjs-guide.md    # EmailJS setup guide
```

## 🎨 Customization Guide

### Adding New Projects
1. Duplicate a project card in the HTML
2. Update the project information:
   ```html
   <div class="project-card">
       <div class="project-image">
           <!-- Add your project image -->
       </div>
       <div class="project-content">
           <h3 class="project-title">Your Project Name</h3>
           <p class="project-description">Project description...</p>
           <div class="project-technologies">
               <span class="tech-tag">React</span>
               <span class="tech-tag">Node.js</span>
           </div>
       </div>
   </div>
   ```

### Adding New Skills
1. Add a new skill item in the HTML:
   ```html
   <div class="skill-item">
       <i class="fab fa-react"></i>
       <span>React</span>
       <div class="skill-level">
           <div class="skill-bar" data-skill="90"></div>
       </div>
   </div>
   ```

### Changing Colors
1. Update CSS variables in `:root` selector
2. The entire color scheme will update automatically

## 🌐 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## 📱 Responsive Breakpoints

- Mobile: < 768px
- Tablet: 768px - 1024px
- Desktop: > 1024px

## ⚡ Performance Features

- CSS and JavaScript minification ready
- Image lazy loading support
- Intersection Observer for efficient animations
- Service Worker ready for PWA conversion

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test across different devices
5. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🎯 To-Do / Future Enhancements

- [ ] Add blog section
- [ ] Implement search functionality
- [ ] Add more animation options
- [ ] Create CMS integration
- [ ] Add analytics integration
- [ ] Implement PWA features
- [ ] Add automated testing

## 📧 Support

If you have any questions or need help setting up the portfolio, feel free to reach out!

---

**Happy coding!** 🚀

*Remember to update this README with your personal information and customize it to match your needs.*

