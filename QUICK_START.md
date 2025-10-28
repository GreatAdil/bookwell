# 🚀 Bookwell - Quick Start Guide

## ⚡ Get Started in 3 Steps

### Step 1: Open the Project
1. Navigate to the `bookwell` folder
2. Right-click on `index.html`
3. Open with your browser (or use Live Server in VS Code)

### Step 2: Explore User Platform
- **Home Page**: Browse featured eBooks
- **Sign Up**: Create a new account or use Google Sign-In
- **Browse**: Explore categories (Business, Mindset, Story, Success)
- **Purchase**: Select a book → Buy Now → Complete payment
- **Library**: Access your purchased eBooks

### Step 3: Access Admin Panel
1. Navigate to `admin/dashboard.html`
2. Login with:
   - **Email**: `admin@bookwell.com`
   - **Password**: `bookwell9999`
3. Manage eBooks, users, and orders

---

## 📱 Key Features

### 🎨 User Platform
✅ **Authentication** - Email/Password & Google Sign-In  
✅ **Browse & Search** - Filter by category, price, rating  
✅ **Favourites** - Save books for later  
✅ **Shopping Flow** - Product → Billing → Payment → Success  
✅ **My Library** - Download & read purchased books  
✅ **Profile** - Manage account settings  
✅ **Dark Mode** - Toggle theme  
✅ **Responsive** - Mobile, tablet, desktop optimized  

### 🔐 Admin Panel
✅ **Dashboard** - Real-time statistics & charts  
✅ **eBook Management** - Add, edit, delete books  
✅ **User Management** - View, suspend, activate users  
✅ **Order Management** - Track all purchases  
✅ **Analytics** - Sales trends, user growth  
✅ **Settings** - Configure platform preferences  

---

## 🔑 Firebase Configuration

**Already configured and ready to use!**

```javascript
Project ID: bookwell-627f9
Auth Domain: bookwell-627f9.firebaseapp.com
Storage: bookwell-627f9.firebasestorage.app
```

All data syncs in real-time with Firebase:
- **Authentication** - User login/signup
- **Firestore** - Database for books, users, orders
- **Storage** - eBook file storage

---

## 📁 Project Structure

```
bookwell/
├── 🏠 User Platform
│   ├── index.html              # Home page
│   ├── login.html              # Authentication
│   ├── categories.html         # Browse books
│   ├── product-detail.html     # Book details
│   ├── billing.html            # Checkout
│   ├── payment.html            # Payment
│   ├── library.html            # Purchased books
│   ├── favourites.html         # Saved books
│   ├── profile.html            # User profile
│   ├── orders.html             # Order history
│   └── contact.html            # Support
│
├── 🔐 Admin Panel
│   ├── dashboard.html          # Overview
│   ├── ebooks.html             # Manage books
│   ├── users.html              # Manage users
│   ├── orders.html             # Manage orders
│   ├── analytics.html          # Reports
│   └── settings.html           # Configuration
│
├── 🎨 Assets
│   ├── css/style.css           # Styles
│   └── js/
│       ├── firebase-config.js  # Firebase setup
│       ├── auth.js             # Authentication
│       └── main.js             # Core functions
│
└── 📄 Documentation
    ├── README.md               # Full documentation
    └── QUICK_START.md          # This file
```

---

## 🎯 User Flow

### For Customers:
1. **Sign Up** → Create account
2. **Browse** → Find books by category
3. **Add to Favourites** → Save for later
4. **Purchase** → Complete checkout
5. **Access Library** → Download/read books
6. **Leave Review** → Rate & comment

### For Admin:
1. **Login** → Access admin panel
2. **Add Books** → Upload new eBooks
3. **Manage Users** → View/suspend accounts
4. **Track Orders** → Monitor sales
5. **View Analytics** → Check performance
6. **Configure** → Update settings

---

## 🎨 Color Palette

- **Primary Green**: `#9AF5B5` (Mint Green)
- **Dark Green**: `#157A3D` (Accent)
- **Light Green**: `#E8FFF0` (Background)
- **White**: `#FFFFFF`
- **Dark Gray**: `#333333` (Text)

---

## 🔧 Tech Stack

| Component | Technology |
|-----------|-----------|
| Frontend | HTML5, CSS3, JavaScript |
| UI Framework | MDBootstrap 6.4.2 |
| Icons | Font Awesome 6.4.0 |
| Backend | Firebase (Auth, Firestore, Storage) |
| Charts | Chart.js 4.4.0 |
| Fonts | Google Fonts (Poppins) |

---

## 📊 Firebase Collections

### `ebooks`
Stores all eBook information
```javascript
{
  title, author, description, price, 
  rating, category, imageUrl, downloadUrl, 
  status, createdAt
}
```

### `users`
User profiles and data
```javascript
{
  uid, email, displayName, photoURL,
  library[], favourites[], 
  totalPurchases, totalSpent, status
}
```

### `orders`
Purchase records
```javascript
{
  userId, userEmail, userName, bookId, 
  bookTitle, amount, paymentId, 
  status, createdAt
}
```

### `reviews`
Book ratings and comments
```javascript
{
  bookId, userId, userName, 
  rating, comment, createdAt
}
```

---

## 🌐 Browser Support

✅ Chrome (Recommended)  
✅ Firefox  
✅ Safari  
✅ Edge  
✅ Mobile Browsers  

---

## 🔒 Security

- Firebase Authentication for secure login
- Admin-only routes protected
- User data encrypted by Firebase
- Input validation on all forms
- Secure payment flow

---

## 💡 Tips

### For Development:
- Use **Live Server** extension in VS Code for hot reload
- Open browser DevTools (F12) to see console logs
- Check Firebase Console for backend data

### For Testing:
- Create test user accounts
- Test payment flow (simulated)
- Try dark/light mode toggle
- Test on mobile devices

### For Admin:
- Add sample eBooks first
- Monitor user activity in dashboard
- Check analytics regularly
- Update settings as needed

---

## 🐛 Troubleshooting

**Problem**: Pages not loading properly  
**Solution**: Make sure you're using a web server (Live Server) or opening via `http://` protocol

**Problem**: Firebase not connecting  
**Solution**: Check internet connection and Firebase config in `js/firebase-config.js`

**Problem**: Admin login not working  
**Solution**: Use exact credentials:
- Email: `admin@bookwell.com`
- Password: `bookwell9999`

**Problem**: Books not displaying  
**Solution**: Initialize sample data by uncommenting `initializeSampleData()` in `js/main.js`

---

## 📞 Need Help?

- Check the full **README.md** for detailed documentation
- Review Firebase Console for backend issues
- Use the Contact page to submit feedback
- Check browser console for error messages

---

## 🎉 You're All Set!

**Start exploring Bookwell now!**

1. Open `index.html` for User Platform
2. Open `admin/dashboard.html` for Admin Panel
3. Create an account and start browsing eBooks
4. Add books as admin and test the full flow

**Enjoy building with Bookwell! 📚✨**

---

**Built with ❤️ using HTML, CSS, JavaScript, MDBootstrap & Firebase**
