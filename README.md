# Job Search Portal - Serverless Web Application

A fully functional job search portal that runs entirely in the browser without requiring any server or backend infrastructure.

## Features

### 🔐 Authentication System
- **Public Access**: Browse and search jobs without login
- **User Registration**: Create accounts with email/password
- **Admin Panel**: Full management capabilities
- **Demo Accounts**: Pre-configured admin and user accounts

### 💼 Job Management
- **Add Jobs**: Create detailed job listings with all relevant information
- **Search & Filter**: Real-time search across all job fields
- **View Details**: Beautiful popup windows with complete job information
- **Edit/Delete**: Admin controls for job management
- **Print Support**: Print-friendly job detail views

### 👥 User Management (Admin Only)
- **User Overview**: View all registered users
- **Role Management**: Toggle between admin and user roles
- **Edit Users**: Update user information including passwords
- **Password Visibility**: Show/hide passwords for management
- **Delete Users**: Remove users (except main admin)

### 🗄️ Data Storage
- **IndexedDB**: All data stored locally in browser
- **No Server Required**: Completely client-side application
- **Data Persistence**: Information saved between sessions
- **Export/Import**: Backup and restore functionality

## Technical Architecture

### Frontend Technologies
- **React 18** with TypeScript
- **Tailwind CSS** for styling
- **Lucide React** for icons
- **Vite** for development and building

### Data Storage
- **IndexedDB** for local database
- **localStorage** for session management
- **No external dependencies** for data storage

### Browser Compatibility
- Modern browsers with IndexedDB support
- Chrome, Firefox, Safari, Edge (latest versions)
- Mobile browsers supported

## Getting Started

### Development
```bash
npm install
npm run dev
```

### Production Build
```bash
npm run build
npm run preview
```

### Deployment
The built application can be deployed to any static hosting service:
- GitHub Pages
- Netlify
- Vercel
- Any web server (Apache, Nginx, etc.)

## Demo Credentials

### Admin Account
- **Email**: admin@jobportal.com
- **Password**: admin123
- **Capabilities**: Full access to all features

### User Account
- **Email**: user@example.com
- **Password**: user123
- **Capabilities**: Add jobs, search, view details

## Data Management

### Local Storage
All data is stored locally in your browser using IndexedDB. This means:
- ✅ No server costs or maintenance
- ✅ Fast performance
- ✅ Works offline
- ⚠️ Data is browser-specific
- ⚠️ Clearing browser data will remove all information

### Backup & Restore
The application includes built-in export/import functionality to backup your data:
1. Export data as JSON file
2. Import data from backup file
3. Transfer data between browsers/devices

## Security Considerations

### Client-Side Security
- Passwords stored in plain text (suitable for demo/local use)
- No encryption (data stored locally)
- Session management via localStorage

### Production Recommendations
For production use, consider:
- Implementing password hashing
- Adding data encryption
- Using secure session management
- Regular data backups

## File Structure

```
src/
├── components/          # React components
│   ├── AuthPage.tsx    # Authentication interface
│   ├── Header.tsx      # Navigation header
│   ├── JobForm.tsx     # Job creation/editing
│   ├── JobList.tsx     # Job display and search
│   └── UserManagement.tsx # Admin user controls
├── contexts/           # React contexts
│   └── AuthContext.tsx # Authentication state
├── types/              # TypeScript definitions
│   └── index.ts        # Type definitions
├── utils/              # Utility functions
│   └── database.ts     # IndexedDB operations
└── App.tsx             # Main application component
```

## Browser Requirements

### Minimum Requirements
- IndexedDB support
- ES6+ JavaScript support
- CSS Grid and Flexbox support

### Recommended Browsers
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Troubleshooting

### Common Issues

**Popup Blocked**
- Enable popups for the site
- Hold Ctrl/Cmd when clicking "View Details"

**Data Not Saving**
- Check if IndexedDB is enabled
- Ensure sufficient storage space
- Try clearing browser cache and reloading

**Performance Issues**
- Large datasets may slow down searches
- Consider implementing pagination for 1000+ jobs
- Regular data cleanup recommended

## License

This project is open source and available under the MIT License.

## Support

For issues or questions:
1. Check browser console for errors
2. Verify IndexedDB support
3. Try in incognito/private mode
4. Clear browser data and restart

---

**Note**: This is a client-side application designed for local/demo use. For production environments with multiple users, consider implementing proper backend infrastructure with secure authentication and data storage.