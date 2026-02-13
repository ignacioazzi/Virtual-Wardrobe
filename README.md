# Virtual Wardrobe - GitHub Pages Deployment

## 🚀 Quick Deploy to GitHub Pages

### Step 1: Create GitHub Repository
1. Go to [GitHub](https://github.com) and create a new repository
2. Name it `virtual-wardrobe` (or any name you like)
3. Make it **Public**
4. Don't initialize with README (we'll upload files directly)

### Step 2: Add Your Anthropic API Key
**IMPORTANT:** Before deploying, you need to add your Anthropic API key to `index.html`

1. Open `index.html`
2. Find line with: `'x-api-key': 'YOUR_ANTHROPIC_API_KEY_HERE'`
3. Replace `YOUR_ANTHROPIC_API_KEY_HERE` with your actual API key from https://console.anthropic.com/

**⚠️ SECURITY NOTE:** 
- Your API key will be visible in the browser's source code
- This is fine for personal use but consider rate limits
- For production, you'd want a backend proxy to hide the key

### Step 3: Upload Files
1. Click "uploading an existing file" or "Add file" → "Upload files"
2. Drag and drop the `index.html` file
3. Commit the file

### Step 4: Enable GitHub Pages
1. Go to repository **Settings**
2. Click **Pages** in the left sidebar
3. Under "Source", select **main** branch
4. Click **Save**
5. Wait 1-2 minutes for deployment

### Step 5: Access Your App
Your app will be available at:
```
https://YOUR_USERNAME.github.io/virtual-wardrobe/
```

## 📱 Features

✅ Upload single or multiple outfit images  
✅ AI-powered item detection (clothes, shoes, accessories)  
✅ Automatic color extraction  
✅ Filter outfits by items  
✅ Edit item names, types, and colors  
✅ Mark items as owned/wishlist  
✅ Export/Import wardrobe data  
✅ All data stored locally in browser  
✅ Drag & drop support  
✅ Bulk upload support  

## 🔧 How It Works

- **Storage**: Uses browser's `localStorage` - data persists across sessions
- **AI Analysis**: Calls Anthropic API directly from browser to analyze outfit images
- **Images**: Stored as base64 in localStorage (note: storage limits apply)

## 💡 Tips

- **Storage Limits**: Browser localStorage typically has 5-10MB limit
- **Image Size**: Compress images before upload for better performance
- **Backup**: Use Export feature regularly to backup your wardrobe
- **API Costs**: Each image analysis uses the Anthropic API (check pricing)

## 🔒 Privacy

- All data stays in your browser
- Images are not sent anywhere except to Anthropic API for analysis
- No server-side storage
- No tracking

## 📦 Local Development

To run locally:
1. Download `index.html`
2. Add your API key
3. Open in browser (or use a local server like `python -m http.server`)

## 🐛 Troubleshooting

**Images not loading?**
- Check browser console for errors
- Verify API key is correct
- Check Anthropic API quota/limits

**Storage full?**
- Export and clear some outfits
- Compress images before upload

**Slow AI analysis?**
- Large images take longer
- Resize images to 1024px max width

## 📄 License

Free to use for personal projects!
