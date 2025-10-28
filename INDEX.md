# 📚 Bookwell - Project Index

## Quick Navigation Guide

---

## 🚀 Getting Started

| Document | Description | Link |
|----------|-------------|------|
| **Quick Start** | Get up and running in 3 steps | [QUICK_START.md](QUICK_START.md) |
| **README** | Complete documentation | [README.md](README.md) |
| **Deployment** | Deploy to production | [DEPLOYMENT_GUIDE.md](DEPLOYMENT_GUIDE.md) |
| **Summary** | Project overview | [PROJECT_SUMMARY.txt](PROJECT_SUMMARY.txt) |

---

## 🏠 User Platform Pages

### Main Pages
| Page | File | Purpose |
|------|------|---------|
| Home | `index.html` | Landing page with featured books |
| Login/Signup | `login.html` | User authentication |
| Categories | `categories.html` | Browse all books |
| Search | `search.html` | Search results |
| New Releases | `new-releases.html` | Latest books |
| Best Sellers | `best-sellers.html` | Popular books |
| Offers | `offers.html` | Combo packs & deals |
| Contact | `contact.html` | Support & FAQs |

### Shopping Flow
| Page | File | Purpose |
|------|------|---------|
| Product Detail | `product-detail.html` | Book information & reviews |
| Billing | `billing.html` | Checkout form |
| Payment | `payment.html` | Payment processing |
| Order Success | `order-success.html` | Confirmation page |

### User Account
| Page | File | Purpose |
|------|------|---------|
| Profile | `profile.html` | User settings |
| Library | `library.html` | Purchased books |
| Favourites | `favourites.html` | Saved books |
| Orders | `orders.html` | Order history |

---

## 🔐 Admin Panel Pages

| Page | File | Purpose |
|------|------|---------|
| Dashboard | `admin/dashboard.html` | Overview & statistics |
| eBooks | `admin/ebooks.html` | Manage books (CRUD) |
| Users | `admin/users.html` | User management |
| Orders | `admin/orders.html` | Order management |
| Categories | `admin/categories.html` | Category management |
| Analytics | `admin/analytics.html` | Reports & charts |
| Settings | `admin/settings.html` | Platform configuration |

**Admin Login:**
- Email: `admin@bookwell.com`
- Password: `bookwell9999`

---

## 🎨 Assets & Scripts

### Stylesheets
| File | Purpose |
|------|---------|
| `css/style.css` | Main stylesheet (900+ lines) |

### JavaScript
| File | Purpose |
|------|---------|
| `js/firebase-config.js` | Firebase setup & helper functions |
| `js/auth.js` | Authentication logic |
| `js/main.js` | Core functionality |

---

## 🔑 Firebase Collections

| Collection | Purpose | Key Fields |
|------------|---------|------------|
| `ebooks` | Book catalog | title, author, price, rating, category |
| `users` | User profiles | email, library[], favourites[], totalPurchases |
| `orders` | Purchase records | userId, bookId, amount, paymentId, status |
| `reviews` | Book reviews | bookId, userId, rating, comment |
| `feedback` | Contact forms | name, email, message |
| `categories` | Book categories | name, icon, description |
| `offers` | Combo deals | title, books[], price, discount |

---

## 🎯 Key Features

### User Features
- ✅ Email/Password & Google Sign-In
- ✅ Browse by category
- ✅ Search & filter
- ✅ Add to favourites
- ✅ Purchase flow
- ✅ My library
- ✅ Order history
- ✅ Dark/light mode
- ✅ Responsive design

### Admin Features
- ✅ Dashboard with stats
- ✅ CRUD operations for books
- ✅ User management
- ✅ Order tracking
- ✅ Analytics & charts
- ✅ Category management
- ✅ Settings

---

## 🎨 Design System

### Colors
```css
Primary Green:  #9AF5B5
Dark Green:     #157A3D
Light Green:    #E8FFF0
White:          #FFFFFF
Dark Gray:      #333333
```

### Typography
- **Font:** Poppins (Google Fonts)
- **Weights:** 300, 400, 500, 600, 700

### Components
- **Buttons:** Rounded (20px radius)
- **Cards:** Soft shadows
- **Icons:** Font Awesome 6.4.0
- **Framework:** MDBootstrap 6.4.2

---

## 📱 Responsive Breakpoints

| Device | Breakpoint | Features |
|--------|-----------|----------|
| Mobile | < 768px | Bottom nav, stacked layout |
| Tablet | 768px - 991px | 2-column grid |
| Desktop | > 991px | Full layout, sidebar |

---

## 🔧 Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML5, CSS3, JavaScript (ES6+) |
| UI Framework | MDBootstrap 6.4.2 |
| Icons | Font Awesome 6.4.0 |
| Charts | Chart.js 4.4.0 |
| Backend | Firebase (Auth, Firestore, Storage) |
| Fonts | Google Fonts (Poppins) |

---

## 📊 Project Statistics

| Metric | Count |
|--------|-------|
| Total Files | 30+ |
| HTML Pages | 21 |
| CSS Files | 1 |
| JavaScript Files | 3 |
| Documentation Files | 4 |
| Total Lines of Code | ~8,500+ |

---

## 🚀 Quick Commands

### Run Locally
```bash
# Using Live Server (VS Code)
Right-click index.html → Open with Live Server

# Using Python
python -m http.server 8000

# Using Node.js
npx http-server
```

### Deploy to Firebase
```bash
firebase login
firebase init hosting
firebase deploy
```

### Deploy to Netlify
```bash
netlify login
netlify deploy --prod
```

---

## 📞 Important Links

### Documentation
- [Quick Start Guide](QUICK_START.md)
- [Full README](README.md)
- [Deployment Guide](DEPLOYMENT_GUIDE.md)
- [Project Summary](PROJECT_SUMMARY.txt)

### Firebase
- Console: https://console.firebase.google.com
- Project: bookwell-627f9
- Auth Domain: bookwell-627f9.firebaseapp.com

### External Resources
- MDBootstrap: https://mdbootstrap.com
- Font Awesome: https://fontawesome.com
- Chart.js: https://www.chartjs.org
- Firebase Docs: https://firebase.google.com/docs

---

## 🎯 User Flows

### Customer Journey
1. Visit home page
2. Browse/search books
3. View product details
4. Add to favourites (optional)
5. Purchase book
6. Access in library
7. Leave review

### Admin Journey
1. Login to admin panel
2. View dashboard
3. Add/manage books
4. Monitor users
5. Track orders
6. View analytics
7. Configure settings

---

## 🔒 Security

### Authentication
- Firebase Authentication
- Email/Password + Google Sign-In
- Admin role verification

### Data Protection
- Firestore security rules
- User data encryption
- Secure payment flow

---

## 📈 Performance

### Optimization
- Lazy loading images
- Minified CSS/JS (production)
- CDN for libraries
- Firebase caching
- Responsive images

### Monitoring
- Firebase Analytics
- Performance monitoring
- Error tracking
- User behavior analysis

---

## 🐛 Troubleshooting

### Common Issues
| Issue | Solution |
|-------|----------|
| Firebase not connecting | Check config in `js/firebase-config.js` |
| Admin login fails | Use exact credentials |
| Books not loading | Initialize sample data |
| Pages not loading | Use web server (Live Server) |

---

## 📝 To-Do (Future Enhancements)

- [ ] Email notifications
- [ ] PDF viewer integration
- [ ] Advanced search filters
- [ ] Wishlist sharing
- [ ] Social media integration
- [ ] Multi-language support
- [ ] Mobile app (React Native/Flutter)
- [ ] Subscription plans
- [ ] Affiliate program
- [ ] Book recommendations AI

---

## 🎉 Project Status

✅ **COMPLETE & PRODUCTION READY**

All features implemented, tested, and documented.
Ready for deployment and use.

---

## 📞 Support

For help:
1. Check documentation files
2. Review Firebase Console
3. Check browser console
4. Contact via contact form

---

**Built with ❤️ for Bookwell**

Last Updated: 2024
Version: 1.0.0
