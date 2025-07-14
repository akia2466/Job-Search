# 🚀 Deployment Guide - Job Search Portal

## The Problem You Encountered

The CORS error occurs because modern browsers block `file://` protocol access for security reasons. You cannot simply open `index.html` directly from your file system.

## ✅ Solution 1: Use Built-in Development Server (Recommended)

### Step 1: Install Dependencies
```bash
npm install
```

### Step 2: Build the Application
```bash
npm run build
```

### Step 3: Serve the Built Application
```bash
npm run serve
```

This will start a local server at `http://localhost:3000` where you can access your app.

## ✅ Solution 2: Use Python Simple Server

If you have Python installed:

### For Python 3:
```bash
cd dist
python -m http.server 8000
```

### For Python 2:
```bash
cd dist
python -m SimpleHTTPServer 8000
```

Then open `http://localhost:8000` in your browser.

## ✅ Solution 3: Use Node.js http-server

### Install globally:
```bash
npm install -g http-server
```

### Serve the dist folder:
```bash
cd dist
http-server -p 8000
```

Access at `http://localhost:8000`

## ✅ Solution 4: Use Live Server (VS Code Extension)

1. Install "Live Server" extension in VS Code
2. Right-click on `index.html` in the `dist` folder
3. Select "Open with Live Server"

## 🌐 Production Deployment Options

### 1. Netlify (Easiest)
1. Go to [netlify.com](https://netlify.com)
2. Drag and drop your `dist` folder
3. Get instant live URL

### 2. GitHub Pages
1. Push your code to GitHub
2. Go to repository Settings > Pages
3. Select source branch
4. Your app will be live at `username.github.io/repository-name`

### 3. Vercel
1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in your project directory
3. Follow the prompts

### 4. Any Web Hosting
Upload the contents of the `dist` folder to any web hosting service.

## 🔧 Complete Setup Instructions

### For Your Laptop (Local Development):

1. **Open Terminal/Command Prompt**
2. **Navigate to your project folder**:
   ```bash
   cd path/to/your/job-portal-project
   ```

3. **Install dependencies**:
   ```bash
   npm install
   ```

4. **Build the application**:
   ```bash
   npm run build
   ```

5. **Serve the application**:
   ```bash
   npm run serve
   ```

6. **Open your browser** and go to: `http://localhost:3000`

### Alternative Quick Method:

If you just want to run it immediately:

1. **Start development server**:
   ```bash
   npm run dev
   ```

2. **Open**: `http://localhost:5173`

## 🚨 Important Notes

- **Never open `index.html` directly** from file explorer
- **Always use a web server** (even locally)
- **The `dist` folder** contains the built application
- **CORS errors** are browser security features, not app bugs

## 📱 Mobile Testing

To test on mobile devices on the same network:

1. Find your computer's IP address
2. Use `npm run serve` with `--host` flag:
   ```bash
   npm run preview --port 3000 --host
   ```
3. Access from mobile: `http://YOUR_IP:3000`

## 🔍 Troubleshooting

### Port Already in Use
```bash
npm run preview --port 3001
```

### Permission Issues
```bash
sudo npm run serve
```

### Still Getting CORS Errors
- Make sure you're accessing via `http://` not `file://`
- Clear browser cache
- Try incognito/private mode

---

**Remember**: This web app works completely offline once loaded, but it must be served through HTTP/HTTPS protocol, not opened directly as a file.