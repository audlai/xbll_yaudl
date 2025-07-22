# Deployment Instructions

## Local Testing

1. **Open the application locally:**
   - Navigate to the project folder
   - Open `index.html` in any modern web browser
   - Or use a local server (recommended for better performance)

2. **Using a local server (recommended):**
   ```bash
   # Using Python 3
   cd interactive-photo-collage
   python3 -m http.server 8000
   
   # Using Node.js (if you have it installed)
   npx serve .
   
   # Using PHP (if you have it installed)
   php -S localhost:8000
   ```
   Then open `http://localhost:8000` in your browser.

## Web Hosting Deployment

### Option 1: Static Hosting Services

**Netlify (Recommended):**
1. Create a free account at [netlify.com](https://netlify.com)
2. Drag and drop the entire `interactive-photo-collage` folder to Netlify
3. Your site will be live instantly with a custom URL

**Vercel:**
1. Create a free account at [vercel.com](https://vercel.com)
2. Connect your GitHub repository or upload the folder
3. Deploy with one click

**GitHub Pages:**
1. Create a GitHub repository
2. Upload all files to the repository
3. Enable GitHub Pages in repository settings
4. Your site will be available at `https://username.github.io/repository-name`

### Option 2: Traditional Web Hosting

1. **Upload files via FTP/SFTP:**
   - Upload all files and folders to your web hosting provider
   - Ensure `index.html` is in the root directory or desired subdirectory
   - Make sure all file permissions are set correctly (644 for files, 755 for directories)

2. **cPanel File Manager:**
   - Log into your hosting control panel
   - Use File Manager to upload and extract the project files
   - Place files in the `public_html` directory (or equivalent)

## Content Management

### Adding Your Images

1. **Replace placeholder images:**
   - Upload your images to the `images/` folder
   - Use the exact filenames specified in the README.md
   - Recommended image formats: JPG, PNG, WebP
   - Optimize images for web (compress to reduce file size)

2. **Image size recommendations:**
   - Landing page images: 800x400px
   - Room overview: 1000x600px
   - Room views: 1000x600px
   - Detail images: 400x300px

### Customizing Content

1. **Edit text content:**
   - Open `index.html` in a text editor
   - Find and replace placeholder text
   - Update room labels and object descriptions

2. **Adjust interactive areas:**
   - Modify the `style` attributes on clickable areas
   - Adjust `top`, `left`, `width`, and `height` percentages
   - Test positioning after each change

## Performance Optimization

### Image Optimization
```bash
# Using ImageMagick (if available)
mogrify -resize 1000x600 -quality 85 *.jpg

# Using online tools
# - TinyPNG.com
# - Squoosh.app
# - ImageOptim (Mac)
```

### Caching Headers (for web servers)
Add to `.htaccess` file (Apache) or server configuration:
```apache
<IfModule mod_expires.c>
    ExpiresActive on
    ExpiresByType text/css "access plus 1 month"
    ExpiresByType application/javascript "access plus 1 month"
    ExpiresByType image/png "access plus 1 month"
    ExpiresByType image/jpg "access plus 1 month"
    ExpiresByType image/jpeg "access plus 1 month"
</IfModule>
```

## Troubleshooting

### Common Issues

1. **Images not loading:**
   - Check file paths and names (case-sensitive on Linux servers)
   - Ensure images are in the correct `images/` folder
   - Verify file permissions (644 for images)

2. **Interactive elements not working:**
   - Check browser console for JavaScript errors (F12)
   - Ensure all files are uploaded correctly
   - Test in different browsers

3. **Layout issues on mobile:**
   - Test on actual mobile devices
   - Use browser developer tools to simulate mobile view
   - Check viewport meta tag is present

### Browser Compatibility Testing

Test your application in:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Security Considerations

1. **File permissions:**
   - Files: 644 (readable by all, writable by owner)
   - Directories: 755 (executable/searchable by all)

2. **Content Security:**
   - Only upload trusted images
   - Avoid executable file extensions
   - Consider adding CSP headers for enhanced security

## Maintenance

1. **Regular updates:**
   - Update images as needed
   - Test functionality periodically
   - Monitor loading times and optimize if necessary

2. **Analytics (optional):**
   - Add Google Analytics or similar tracking
   - Monitor user interactions and popular content
   - Use insights to improve user experience

## Support

For technical issues:
1. Check browser console for error messages
2. Verify all files are uploaded correctly
3. Test in multiple browsers
4. Check hosting provider documentation for specific requirements

