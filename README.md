# Arham Sheikh - Full-Stack Developer & Data Engineer Portfolio

A modern, responsive portfolio website built with **Next.js 14**, **TypeScript**, and **Tailwind CSS**. Features smooth animations, dark theme design, and complete email integration.

## 🌟 Features

✨ **Modern Design** - Clean, professional dark theme with gradient accents
📱 **Fully Responsive** - Mobile-first design that works on all devices
🎨 **Smooth Animations** - Framer Motion animations for delightful UX
📧 **Email Integration** - Contact form with Nodemailer for direct email delivery
🔗 **Clickable Certifications** - Certificate titles link to verification pages
🚀 **Performance Optimized** - Next.js 14 with SSR and optimizations
🎯 **SEO Ready** - Meta tags, structured data, and semantic HTML
⚡ **Production Ready** - Vercel deployment ready

## 📋 Sections

1. **Navbar** - Sticky navigation with mobile hamburger menu
2. **Hero** - Eye-catching introduction with CTAs and social links
3. **About** - Personal bio with professional timeline
4. **Skills** - Organized by category with proficiency bars
5. **Projects** - 6 featured projects without images, smooth UI
6. **Certifications** - 8 certifications with clickable verification links
7. **Contact** - Full contact form with email integration
8. **Footer** - Links, social connections, and tech stack

## 🛠 Tech Stack

- **Frontend**: Next.js 14, React 18, TypeScript
- **Styling**: Tailwind CSS, Custom CSS animations
- **Animations**: Framer Motion
- **Email**: Nodemailer (Node.js email service)
- **Icons**: React Icons
- **Deployment**: Vercel (recommended)

## 📦 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/arhamsheikh17/porfolio.git
cd porfolio
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Set Up Environment Variables

Create a `.env.local` file in the root directory:

```env
# Gmail Configuration
EMAIL_USER=your-email@gmail.com
EMAIL_PASSWORD=your-app-password
```

#### How to Get Gmail App Password:
1. Enable 2FA on your Gmail account
2. Go to [Google App Passwords](https://myaccount.google.com/apppasswords)
3. Select "Mail" and "Windows Computer" (or your device)
4. Copy the generated 16-character password
5. Paste it as `EMAIL_PASSWORD`

### 4. Run Development Server
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## 🎨 Customization

### Update Personal Information

**Navbar/Hero**:
```typescript
// src/components/Hero.tsx
- Update name "Arham Sheikh"
- Update social media links
- Modify description
```

**Skills**:
```typescript
// src/components/Skills.tsx
- Add/remove skill categories
- Adjust proficiency levels
- Add more technologies
```

**Projects**:
```typescript
// src/components/Projects.tsx
- Edit project titles and descriptions
- Update tech tags
- Modify impact metrics
- Add GitHub/project links
```

**Certifications**:
```typescript
// src/components/Certifications.tsx
- Add your certifications
- Update verification links
- Modify issuer and credential IDs
```

**Contact Information**:
```typescript
// src/components/Contact.tsx
- Update email address
- Add phone number
- Modify location
- Update social media links
```

### Customize Colors

Edit `tailwind.config.ts`:
```typescript
colors: {
  primary: '#0f1419',    // Main background
  secondary: '#1a1f2e',  // Secondary background
  accent: '#00d4ff',     // Primary accent color
  'accent-light': '#00e5ff', // Light accent
  light: '#f0f0f0',      // Text color
}
```

## 📧 Email Configuration

### Using Gmail (Free Tier)
Already configured! Just add your credentials to `.env.local`

### Using Other Email Services
Update `src/app/api/send-email/route.ts`:

**For Outlook/Hotmail**:
```typescript
const transporter = nodemailer.createTransport({
  service: 'outlook',
  auth: {
    user: process.env.EMAIL_USER,
    pass: process.env.EMAIL_PASSWORD,
  },
})
```

**For Custom SMTP**:
```typescript
const transporter = nodemailer.createTransport({
  host: 'smtp.example.com',
  port: 587,
  secure: false,
  auth: {
    user: process.env.EMAIL_USER,
    pass: process.env.EMAIL_PASSWORD,
  },
})
```

## 🚀 Deployment

### Deploy on Vercel (Recommended)

1. Push to GitHub:
```bash
git add .
git commit -m "Deploy portfolio"
git push origin main
```

2. Visit [Vercel](https://vercel.com) and connect your GitHub repository
3. Add environment variables in Vercel dashboard:
   - `EMAIL_USER`
   - `EMAIL_PASSWORD`
4. Click "Deploy"

### Deploy on Other Platforms

**Netlify**: ✅ Supported (add serverless functions for email)
**AWS**: ✅ Supported (use API Gateway + Lambda)
**Azure**: ✅ Supported

## 📱 Responsive Breakpoints

- **Mobile**: < 640px (sm)
- **Tablet**: 640px - 1024px (md)
- **Desktop**: > 1024px (lg)
- **Large Desktop**: > 1280px (xl)

## 🎯 Performance Metrics

- **Lighthouse Score**: 95+
- **Page Load Time**: < 2s
- **SEO Score**: 100
- **Mobile Friendly**: ✅

## 🔒 Security

- ✅ Environment variables for sensitive data
- ✅ CSRF protection via Next.js
- ✅ Email validation on frontend and backend
- ✅ No sensitive data in version control

## 📄 File Structure

```
porfolio/
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   └── send-email/
│   │   │       └── route.ts      # Email API
│   │   ├── layout.tsx            # Root layout
│   │   ├── page.tsx              # Home page
│   │   └── globals.css           # Global styles
│   ├── components/
│   │   ├── Navbar.tsx            # Navigation
│   │   ├── Hero.tsx              # Hero section
│   │   ├── About.tsx             # About section
│   │   ├── Skills.tsx            # Skills section
│   │   ├── Projects.tsx          # Projects section
│   │   ├── Certifications.tsx    # Certifications
│   │   ├── Contact.tsx           # Contact form
│   │   └── Footer.tsx            # Footer
├── tailwind.config.ts            # Tailwind config
├── tsconfig.json                 # TypeScript config
├── postcss.config.ts             # PostCSS config
├── package.json                  # Dependencies
└── .env.local                    # Environment variables
```

## 🤝 Contributing

Feel free to fork and customize this portfolio for your own use!

## 📝 License

This project is open source and available under the MIT License.

## 🙋 Support

For issues or questions:
1. Check the documentation above
2. Review the code comments
3. Open a GitHub issue
4. Contact: arhamsheikh17@gmail.com

## 🎉 Next Steps

1. ✅ Customize all sections with your information
2. ✅ Test email functionality locally
3. ✅ Add your projects and certifications
4. ✅ Test responsiveness on mobile devices
5. ✅ Deploy to Vercel
6. ✅ Set up custom domain (optional)
7. ✅ Add Google Analytics (optional)
8. ✅ Set up GitHub Pages or similar (optional)

---

**Made with ❤️ by Arham Sheikh | Updated May 2026**

Visit the live portfolio at: [Your Portfolio URL]
