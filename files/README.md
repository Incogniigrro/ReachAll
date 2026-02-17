# NGO WEBSITE - Complete Setup Guide

## 📋 What You've Got

A complete, professional NGO website with:
- ✅ Homepage with hero section, stats, mission, programs preview, and blog preview
- ✅ About page with story, mission/vision/values, team, and timeline
- ✅ Programs page with detailed program descriptions
- ✅ Blog page with multiple posts
- ✅ Gallery page with image grid
- ✅ Contact page with form and contact information
- ✅ Fully responsive design (works on mobile, tablet, desktop)
- ✅ Professional animations and interactions
- ✅ Contact form with validation

## 🎨 CUSTOMIZATION GUIDE

### STEP 1: Update Your Brand Colors

Open `styles.css` and find the "COLOR VARIABLES" section (around line 15):

```css
:root {
    --primary-color: #2C5F4F;    /* Change to your brand color */
    --accent-color: #E8A961;      /* Change to your accent color */
}
```

Replace these hex codes with your organization's colors!

### STEP 2: Add Your Logo and Images

1. Save your logo as `logo.png` in the `/assets` folder
2. Add your images following the naming in `assets/placeholder-images.txt`

**Quick Image Sources:**
- Free stock: Unsplash.com, Pexels.com, Pixabay.com
- Or use your own photos!

### STEP 3: Update Text Content

Search for "CUSTOMIZE" comments in all HTML files. Key areas:

**index.html:**
- Line 28: Your NGO name
- Line 53-57: Hero title and mission statement
- Line 113-123: Mission description
- All "Your NGO Name" instances

**about.html:**
- Your organization's story
- Mission, vision, values text
- Team member information
- Timeline milestones

**contact.html:**
- Email addresses
- Phone numbers
- Physical address
- Office hours

### STEP 4: Update Social Media Links

Find all social media links (look for `<a href="#">`) in the footer and replace `#` with your actual social media URLs:

```html
<a href="https://facebook.com/yourpage" aria-label="Facebook">
<a href="https://twitter.com/yourhandle" aria-label="Twitter">
<a href="https://instagram.com/yourhandle" aria-label="Instagram">
<a href="https://linkedin.com/company/yourcompany" aria-label="LinkedIn">
```

## 📁 FILE STRUCTURE

```
ngo-website/
├── index.html          # Homepage
├── about.html          # About page
├── programs.html       # Programs page
├── blog.html          # Blog page
├── gallery.html       # Gallery page
├── contact.html       # Contact page
├── styles.css         # Main stylesheet
├── pages.css          # Inner pages stylesheet
├── script.js          # JavaScript functionality
├── assets/            # Images folder
│   ├── logo.png
│   ├── mission-image.jpg
│   ├── blog-*.jpg
│   ├── gallery-*.jpg
│   └── team-*.jpg
└── README.md          # This file
```

## 🚀 STEP 2: HOSTING OPTIONS (Choose One)

### Option A: Free Hosting with GitHub Pages (Easiest!)

1. **Create GitHub Account** (if you don't have one)
   - Go to github.com
   - Click "Sign up"

2. **Create New Repository**
   - Click the "+" icon → "New repository"
   - Name it: `your-ngo-website`
   - Make it Public
   - Click "Create repository"

3. **Upload Your Files**
   - Click "uploading an existing file"
   - Drag all your website files into the upload area
   - Click "Commit changes"

4. **Enable GitHub Pages**
   - Go to repository Settings
   - Scroll to "Pages" section
   - Under "Source", select "main" branch
   - Click "Save"
   - Your site will be live at: `https://yourusername.github.io/your-ngo-website`

### Option B: Free Hosting with Netlify

1. **Go to netlify.com**
2. **Sign up** (free account)
3. **Drag & Drop Deployment**
   - Click "Add new site" → "Deploy manually"
   - Drag your entire website folder
   - Done! Your site is live instantly
4. **Custom Domain** (optional)
   - Go to "Domain settings"
   - Add your custom domain
   - Follow DNS instructions

### Option C: Paid Hosting (More Professional)

**Recommended Hosts:**
1. **Bluehost** ($3-5/month)
   - Go to bluehost.com
   - Choose "Shared Hosting"
   - Follow setup wizard
   - Upload files via File Manager or FTP

2. **SiteGround** ($4-7/month)
   - Go to siteground.com
   - Choose "StartUp" plan
   - Use their Site Tools to upload files

3. **HostGator** ($3-6/month)
   - Go to hostgator.com
   - Choose "Hatchling Plan"
   - Upload via cPanel File Manager

**How to Upload (for paid hosting):**
1. Log into your hosting control panel (cPanel)
2. Find "File Manager"
3. Navigate to `public_html` folder
4. Upload all your website files
5. Your site is live at your domain!

## 🌐 STEP 3: CONNECT A CUSTOM DOMAIN

### If Using Free Hosting (GitHub Pages/Netlify):
1. **Buy a domain** from:
   - Namecheap.com ($10-15/year)
   - Google Domains ($12/year)
   - GoDaddy.com ($12-20/year)

2. **Connect Domain:**
   - **GitHub Pages:** In repo settings → Pages → Custom domain
   - **Netlify:** Domain settings → Add custom domain
   - Follow DNS setup instructions provided

### If Using Paid Hosting:
- Domain is usually included in your hosting package!
- Just point your domain to your hosting in domain settings

## 📧 STEP 4: MAKE CONTACT FORM WORK

Your contact form currently shows a success message but doesn't send emails. Here are options:

### Option A: Use Formspree (Easiest - Free for 50 submissions/month)

1. Go to formspree.io
2. Sign up (free)
3. Create a new form
4. Copy the form endpoint
5. In `contact.html`, find the `<form>` tag and add:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
6. Done! Submissions will be emailed to you.

### Option B: Use EmailJS (Free for 200 emails/month)

1. Go to emailjs.com
2. Sign up and create email service
3. Add this to your `contact.html` before `</body>`:
   ```html
   <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
   ```
4. Update the form submission code in `script.js` (detailed instructions on EmailJS)

### Option C: Backend Integration (Advanced)

If you have a backend developer, they can create a server endpoint to handle form submissions.

## ✅ FINAL CHECKLIST

Before going live, make sure you've:

- [ ] Replaced all "Your NGO Name" with your actual name
- [ ] Updated all placeholder text with your content
- [ ] Added your logo and images
- [ ] Changed brand colors to match your organization
- [ ] Updated all email addresses
- [ ] Updated phone numbers and address
- [ ] Connected social media links
- [ ] Set up contact form email delivery
- [ ] Tested website on mobile phone
- [ ] Tested all navigation links
- [ ] Tested contact form submission

## 🎯 QUICK WINS

**Immediate Impact Changes:**
1. Update the hero title on homepage (index.html, line 53)
2. Add your logo (replace assets/logo.png)
3. Change colors in styles.css (line 15-18)
4. Update contact information (all pages footer)
5. Add real social media links

## 💡 PRO TIPS

1. **Mobile First:** Always check how it looks on mobile!
2. **Fast Images:** Compress images before uploading (use tinypng.com)
3. **Regular Updates:** Keep your blog section updated with news
4. **SEO:** Update page titles in each HTML file's `<title>` tag
5. **Google Analytics:** Add tracking code to monitor visitors

## 🆘 NEED HELP?

Common issues and solutions:

**Images not showing?**
- Check file names match exactly (case-sensitive!)
- Ensure images are in the `/assets` folder
- Try clearing browser cache (Ctrl+F5)

**Colors not changing?**
- Make sure you're editing `styles.css`
- Clear browser cache and refresh
- Check you're using hex codes like `#2C5F4F`

**Contact form not working?**
- Check you've set up Formspree or EmailJS
- Check browser console for errors (F12 → Console tab)

**Mobile menu not opening?**
- Ensure `script.js` is loading
- Check browser console for errors

## 📱 TESTING YOUR WEBSITE

Before launching:
1. Open in different browsers (Chrome, Firefox, Safari)
2. Test on mobile phone
3. Click every link
4. Submit the contact form
5. Check all images load
6. Test on slow internet connection

## 🚀 YOU'RE READY!

Your website is professional, responsive, and ready for the world!

Next steps:
1. Complete customization
2. Choose hosting
3. Upload files
4. Connect domain (optional)
5. Set up contact form
6. Launch! 🎉

---

**Remember:** You can always update content later. Don't wait for perfection - get it live and improve over time!

Good luck with your NGO's online presence! 🌟
