# 🧪 Admin Panel Testing Guide

## Quick Test Checklist

### ✅ Step 1: Open Admin Dashboard
```
1. Navigate to: admin/dashboard.html
2. Login with:
   Email: admin@bookwell.com
   Password: bookwell9999
3. Press F12 to open browser console
```

**Expected Results:**
- ✅ Login successful
- ✅ Dashboard loads
- ✅ Console shows: "Loading users from Firestore..."
- ✅ Console shows: "Users loaded: X"
- ✅ Stats cards show numbers (even if 0)

---

### ✅ Step 2: Check eBooks Page
```
1. Click "eBooks" in sidebar
2. Check console for logs
```

**Expected Results:**
- ✅ Console shows: "Loading books from Firestore..."
- ✅ Console shows: "Books loaded: X"
- ✅ Either shows:
   - Table with books (if any exist)
   - OR "No eBooks found" message with icon
   - OR Error message (check Firebase connection)

---

### ✅ Step 3: Add a Test Book
```
1. Click "Add New eBook" button
2. Fill in form:
   - Title: Test Book
   - Author: Test Author
   - Description: Test description
   - Price: 99
   - Rating: 4.5
   - Category: business
   - Image URL: https://via.placeholder.com/300x400?text=Test+Book
   - Download URL: #
   - Status: active
3. Click "Save eBook"
```

**Expected Results:**
- ✅ Toast notification: "eBook added successfully!"
- ✅ Book appears in table
- ✅ Total Books count increases

---

### ✅ Step 4: Check Users Page
```
1. Click "Users" in sidebar
2. Check console for logs
```

**Expected Results:**
- ✅ Console shows: "Loading users from Firestore..."
- ✅ Console shows: "Users loaded: X"
- ✅ Either shows:
   - Table with users
   - OR "No users found" message

---

### ✅ Step 5: Create Test User
```
1. Open login.html in new tab
2. Click "Sign Up" tab
3. Fill in:
   - Name: Test User
   - Email: test@example.com
   - Password: test123
4. Click "Create Account"
5. Go back to admin/users.html
6. Refresh page
```

**Expected Results:**
- ✅ User created successfully
- ✅ User appears in admin users table
- ✅ Total Users count increases

---

### ✅ Step 6: Check Orders Page
```
1. Click "Orders" in sidebar
2. Check console for logs
```

**Expected Results:**
- ✅ Console shows: "Loading orders from Firestore..."
- ✅ Console shows: "Orders loaded: X"
- ✅ Either shows:
   - Table with orders
   - OR "No orders found" message

---

### ✅ Step 7: Create Test Order
```
1. Login as test user (test@example.com)
2. Browse to categories.html
3. Click "Buy Now" on any book
4. Complete billing form
5. Complete payment
6. Go back to admin/orders.html
7. Refresh page
```

**Expected Results:**
- ✅ Order created successfully
- ✅ Order appears in admin orders table
- ✅ Total Orders count increases
- ✅ Total Revenue updates

---

## Console Logs Reference

### ✅ Successful Logs:
```
Loading books from Firestore...
Books loaded: 1

Loading users from Firestore...
Users loaded: 1

Loading orders from Firestore...
Orders loaded: 1
```

### ⚠️ Warning Logs (OK):
```
Using fallback query (no index)
```
*This is normal - means Firestore index not created yet*

### ❌ Error Logs (Need Fixing):
```
Error loading books: [error message]
Failed to load users. Error: [error message]
```
*Check Firebase connection and rules*

---

## Troubleshooting

### Issue: "Failed to load books"

**Solutions:**
1. Check internet connection
2. Verify Firebase config in `js/firebase-config.js`
3. Check Firestore rules in Firebase Console
4. Look at browser console for specific error

---

### Issue: Stats show 0 but data exists

**Solutions:**
1. Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
2. Clear browser cache
3. Check console for errors
4. Verify data exists in Firebase Console

---

### Issue: "Permission denied"

**Solutions:**
1. Go to Firebase Console
2. Firestore Database → Rules
3. Update rules to:
```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true; // For testing only!
    }
  }
}
```
4. Click "Publish"

**⚠️ Warning:** This allows all access. For production, use proper security rules!

---

### Issue: Images not loading

**Solutions:**
1. Use valid image URLs
2. Try placeholder: `https://via.placeholder.com/300x400?text=Book`
3. Check image URL in browser
4. Fallback will show if image fails

---

## Firebase Console Checks

### 1. Verify Collections Exist:
```
Firebase Console → Firestore Database → Data

Should see collections:
- ebooks
- users
- orders
- reviews
- feedback
```

### 2. Check Authentication:
```
Firebase Console → Authentication → Users

Should see:
- Admin user (if created)
- Test users
```

### 3. Verify Storage:
```
Firebase Console → Storage

Should have bucket:
- bookwell-627f9.firebasestorage.app
```

---

## Expected Empty States

### No Books:
```
┌──────────────────────────────┐
│   📚                         │
│   No eBooks found            │
│   Click "Add New eBook"      │
│   to add your first book     │
└──────────────────────────────┘
```

### No Users:
```
┌──────────────────────────────┐
│   👥                         │
│   No users found             │
│   Users will appear here     │
│   after registration         │
└──────────────────────────────┘
```

### No Orders:
```
┌──────────────────────────────┐
│   🛒                         │
│   No orders found            │
│   Orders will appear here    │
│   after purchases            │
└──────────────────────────────┘
```

---

## Success Indicators ✅

You'll know everything works when:

1. **Dashboard:**
   - ✅ Stats show correct numbers
   - ✅ Charts display
   - ✅ Recent orders table loads

2. **eBooks Page:**
   - ✅ Books list displays
   - ✅ Can add new books
   - ✅ Can edit existing books
   - ✅ Can delete books
   - ✅ Search/filter works

3. **Users Page:**
   - ✅ Users list displays
   - ✅ Can view user details
   - ✅ Can suspend/activate users
   - ✅ Search works

4. **Orders Page:**
   - ✅ Orders list displays
   - ✅ Can filter by status/date
   - ✅ Can view order details

---

## Quick Fix Commands

### Clear All Data (Fresh Start):
```
1. Go to Firebase Console
2. Firestore Database
3. Delete all collections
4. Refresh admin panel
5. Should show empty states
```

### Add Sample Book via Console:
```javascript
// Open browser console on admin/ebooks.html
db.collection('ebooks').add({
  title: 'Sample Book',
  author: 'Sample Author',
  description: 'This is a sample book',
  price: 99,
  rating: 4.5,
  category: 'business',
  imageUrl: 'https://via.placeholder.com/300x400?text=Sample',
  downloadUrl: '#',
  status: 'active',
  createdAt: firebase.firestore.FieldValue.serverTimestamp()
}).then(() => {
  console.log('Sample book added!');
  location.reload();
});
```

---

## Final Checklist ✅

Before considering testing complete:

- [ ] Dashboard loads without errors
- [ ] All stats show numbers (even if 0)
- [ ] eBooks page loads
- [ ] Can add a new book
- [ ] Users page loads
- [ ] Orders page loads
- [ ] Console shows proper logs
- [ ] No red errors in console
- [ ] Empty states show when no data
- [ ] Error messages are helpful

---

## 🎉 Success!

If all checks pass, your admin panel is working perfectly!

**Next Steps:**
1. Add more books
2. Test user flows
3. Complete a purchase
4. Check analytics
5. Customize as needed

---

**Need Help?**
- Check `FIXES_APPLIED.md` for what was fixed
- Review browser console for errors
- Verify Firebase connection
- Check `README.md` for full documentation
