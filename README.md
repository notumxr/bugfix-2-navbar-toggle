# 🐞 Bug Fix #2 – Navbar Toggle Not Working (JavaScript DOM Query Bug)

## ❗ Bug Summary
The mobile navbar toggle button did not expand or collapse the menu because the JavaScript was selecting the wrong element (`.nav-togglee` instead of `.nav-toggle`).  
As a result, clicking the toggle button did nothing.

---

## 🔧 Cause of the Bug
- Incorrect DOM selector in JavaScript.
- The script was looking for a class name that does **not exist**.
- Therefore, `addEventListener()` never attached to the button.

---

## ✅ Fixed Code Changes
- Updated the selector from:  
  ```js
  document.querySelector('.nav-togglee')
  ```
  to:
  ```js
  document.querySelector('.nav-toggle')
  ```
- Verified that the toggle now correctly adds/removes the `active` class.

---

## 📁 Files Included in This Bug Fix
- `broken/bug2.html` – original broken version  
- `fixed/bug2_fixed.html` – corrected working version  
- `README.md` – explanation of the bug and the fix

---

## ✔️ Status
**Fixed and tested.**