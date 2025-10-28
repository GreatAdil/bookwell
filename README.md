# 📚 Bookwell - Complete eBook Selling Platform

A modern, fully-functional eBook selling website with User Platform and Admin Panel, built with **HTML, CSS, JavaScript, MDBootstrap**, and **Firebase**.

## 🌟 Features

### 🎨 Design
- **Mint Green & White Color Palette** (#9AF5B5, #FFFFFF, #333333)
- **Fully Responsive** - Mobile, Tablet, and Desktop optimized
- **Dark/Light Mode** toggle
- **Modern UI** with smooth animations and transitions
- **Mobile Bottom Navigation** for better mobile UX

### 👥 User Platform Features
- ✅ **Authentication** (Email/Password & Google Sign-In)
- ✅ **Browse eBooks** by categories (Business, Mindset, Story, Success)
- ✅ **Search & Filter** functionality
- ✅ **Product Detail Pages** with reviews and ratings
- ✅ **Favourites System** - Save books for later
- ✅ **Shopping Cart & Checkout** flow
- ✅ **Payment Integration** (Card, UPI, Net Banking)
- ✅ **My Library** - Access purchased eBooks
- ✅ **Order History** - Track all purchases
- ✅ **User Profile Management**
- ✅ **Contact & Support** page with FAQs

### 🔐 Admin Panel Features
- ✅ **Admin Dashboard** with analytics
- ✅ **eBook Management** (Add, Edit, Delete)
- ✅ **User Management** (View, Suspend, Activate)
- ✅ **Order Management** with filters
- ✅ **Real-time Statistics** (Users, Books, Orders, Revenue)
- ✅ **Charts & Analytics** (Sales trends, User growth)
- ✅ **Secure Admin Login** (admin@bookwell.com / bookwell9999)

## 🔑 Firebase Integration

All data is synced in real-time with Firebase:

| Feature | Firebase Collection | Purpose |
|---------|-------------------|---------|
| eBooks | `ebooks` | Store book data |
| Users | `users` | User profiles, library, favourites |
| Orders | `orders` | Purchase records |
| Reviews | `reviews` | Book ratings & comments |
| Feedback | `feedback` | Contact form submissions |
| Categories | `categories` | Book categories |

### Firebase Configuration
```javascript
const firebaseConfig = {
  apiKey: "AIzaSyBPIA--w_vg_2yiea6SRYMN-rPhY7VPhH0",
  authDomain: "bookwell-627f9.firebaseapp.com",
  databaseURL: "https://bookwell-627f9-default-rtdb.firebaseio.com",
  projectId: "bookwell-627f9",
  storageBucket: "bookwell-627f9.firebasestorage.app",
  messagingSenderId: "459809515203",
  appId: "1:459809515203:web:6fa69ffafa490ddc636476"
};
```

## 📁 Project Structure

```
bookwell/
├── index.html              # Home page
├── login.html              # Login/Signup page
├── categories.html         # Browse all books
├── product-detail.html     # Book details page
├── billing.html            # Billing information
├── payment.html            # Payment page
├── order-success.html      # Order confirmation
├── library.html            # User's purchased books
├── favourites.html         # Saved books
├── profile.html            # User profile
├── orders.html             # Order history
├── offers.html             # Combo packs & deals
├── contact.html            # Contact & support
├── new-releases.html       # Latest books
├── best-sellers.html       # Popular books
│
├── admin/
│   ├── dashboard.html      # Admin dashboard
│   ├── ebooks.html         # Manage eBooks
│   ├── users.html          # Manage users
│   └── orders.html         # Manage orders
│
├── css/
│   └── style.css           # Main stylesheet
│
├── js/
│   ├── firebase-config.js  # Firebase setup
│   ├── auth.js             # Authentication logic
│   └── main.js             # Main functionality
│
└── README.md               # This file
```

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for Firebase and CDN resources)
- A code editor (VS Code recommended)

### Installation

1. **Download/Clone the Project**
   ```bash
   # If using Git
   git clone <repository-url>
   cd bookwell
   ```

2. **Open with Live Server**
   - Install "Live Server" extension in VS Code
   - Right-click on `index.html`
   - Select "Open with Live Server"
   - Or simply open `index.html` in your browser

3. **Firebase Setup (Already Configured)**
   - Firebase is already configured and ready to use
   - No additional setup required!

### 🔐 Admin Access

To access the Admin Panel:
- **URL:** `admin/dashboard.html`
- **Email:** `admin@bookwell.com`
- **Password:** `bookwell9999`

### 👤 Test User Account

Create a new account or use Google Sign-In to test user features.

## 📱 Pages Overview

### User Platform Pages

1. **Home Page** (`index.html`)
   - Hero banner with CTA
   - Category selection
   - Featured eBooks
   - Responsive navbar

2. **Categories** (`categories.html`)
   - Filter by category, price, rating
   - Sort options
   - Grid view of all books

3. **Product Detail** (`product-detail.html`)
   - Book information
   - Add to favourites
   - Purchase button
   - Customer reviews

4. **Billing & Payment** (`billing.html`, `payment.html`)
   - User information form
   - Payment method selection
   - Order summary

5. **My Library** (`library.html`)
   - Purchased eBooks
   - Download & read online options

6. **Profile** (`profile.html`)
   - User information
   - Edit profile
   - Quick access to library, favourites, orders

### Admin Panel Pages

1. **Dashboard** (`admin/dashboard.html`)
   - Statistics cards
   - Sales & user growth charts
   - Recent orders table

2. **eBooks Management** (`admin/ebooks.html`)
   - Add new eBooks
   - Edit existing books
   - Delete books
   - Search & filter

3. **Users Management** (`admin/users.html`)
   - View all users
   - User details & library
   - Suspend/activate users

4. **Orders Management** (`admin/orders.html`)
   - View all orders
   - Filter by status, date
   - Order details

## 🎨 Customization

### Colors
Edit `css/style.css` to change the color scheme:
```css
:root {
    --primary-green: #9AF5B5;
    --dark-green: #157A3D;
    --light-green: #E8FFF0;
    --white: #FFFFFF;
    --dark-gray: #333333;
}
```

### Firebase Configuration
To use your own Firebase project:
1. Create a new Firebase project at https://firebase.google.com
2. Enable Authentication, Firestore, and Storage
3. Replace the config in `js/firebase-config.js`

### Sample Data
To initialize sample eBooks, uncomment this line in `js/main.js`:
```javascript
// await initializeSampleData();
```

## 🔧 Technologies Used

- **Frontend:** HTML5, CSS3, JavaScript (ES6+)
- **UI Framework:** MDBootstrap 6.4.2
- **Icons:** Font Awesome 6.4.0
- **Fonts:** Google Fonts (Poppins)
- **Backend:** Firebase (Auth, Firestore, Storage)
- **Charts:** Chart.js 4.4.0

## 📊 Firebase Collections Structure

### `ebooks` Collection
```javascript
{
  title: "Book Title",
  author: "Author Name",
  description: "Book description",
  price: 99.99,
  rating: 4.5,
  category: "business",
  imageUrl: "https://...",
  downloadUrl: "https://...",
  status: "active",
  createdAt: Timestamp
}
```

### `users` Collection
```javascript
{
  uid: "user-id",
  email: "user@example.com",
  displayName: "User Name",
  photoURL: "https://...",
  library: ["book-id-1", "book-id-2"],
  favourites: ["book-id-3"],
  totalPurchases: 5,
  totalSpent: 499.95,
  status: "active",
  createdAt: Timestamp
}
```

### `orders` Collection
```javascript
{
  userId: "user-id",
  userEmail: "user@example.com",
  userName: "User Name",
  userPhone: "1234567890",
  bookId: "book-id",
  bookTitle: "Book Title",
  amount: 99.99,
  paymentId: "PAY123456",
  status: "paid",
  createdAt: Timestamp
}
```

## 🌐 Browser Support

- ✅ Chrome (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ Mobile browsers

## 📝 Features Checklist

### User Features
- [x] User Registration & Login
- [x] Google Sign-In
- [x] Browse eBooks by category
- [x] Search functionality
- [x] Product details with reviews
- [x] Add to favourites
- [x] Purchase flow (Billing → Payment → Success)
- [x] My Library (purchased books)
- [x] Order history
- [x] Profile management
- [x] Dark/Light mode
- [x] Responsive design
- [x] Mobile bottom navigation

### Admin Features
- [x] Admin authentication
- [x] Dashboard with statistics
- [x] Add/Edit/Delete eBooks
- [x] View all users
- [x] Suspend/Activate users
- [x] View all orders
- [x] Filter orders by status/date
- [x] Real-time data sync
- [x] Charts & analytics

## 🔒 Security Features

- Firebase Authentication for secure login
- Admin-only routes protected
- User data encrypted by Firebase
- Secure payment flow
- Input validation on all forms

## 📞 Support

For issues or questions:
- Check the FAQ section in `contact.html`
- Submit feedback through the contact form
- Review Firebase console for backend issues

## 📄 License

This project is open-source and available for educational purposes.

## 🎉 Credits

- **Design Inspiration:** Modern eCommerce platforms
- **Icons:** Font Awesome
- **UI Components:** MDBootstrap
- **Backend:** Firebase by Google

---

**Built with ❤️ for Bookwell**

🚀 **Ready to launch!** Just open `index.html` and start exploring!

For Admin Panel: Navigate to `admin/dashboard.html` and login with:
- Email: `admin@bookwell.com`
- Password: `bookwell9999`
