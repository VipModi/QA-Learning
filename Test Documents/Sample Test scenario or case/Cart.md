## ✅ **1. Positive Test Cases**

|Test Case ID|Description|
|---|---|
|TC_CART_POS_01|Verify user can successfully add a product to the cart.|
|TC_CART_POS_02|Verify multiple products can be added to the cart.|
|TC_CART_POS_03|Verify quantity of a product can be updated in the cart.|
|TC_CART_POS_04|Verify user can remove a product from the cart.|
|TC_CART_POS_05|Verify cart persists during the session until manually cleared or order is placed.|
|TC_CART_POS_06|Verify product details (name, price, image, quantity) are correctly shown in the cart.|
|TC_CART_POS_07|Verify cart total updates correctly when items are added or removed.|
|TC_CART_POS_08|Verify navigation from cart to checkout page.|
|TC_CART_POS_09|Verify coupon or discount codes can be applied from the cart page.|

---

## ❌ **2. Negative Test Cases**

|Test Case ID|Description|
|---|---|
|TC_CART_NEG_01|Verify cart shows appropriate message when it’s empty.|
|TC_CART_NEG_02|Verify cart does not allow adding out-of-stock items.|
|TC_CART_NEG_03|Verify user cannot add negative or zero quantity.|
|TC_CART_NEG_04|Verify cart doesn’t retain items after logout (if not designed to).|
|TC_CART_NEG_05|Verify behavior when server is down while updating cart.|
|TC_CART_NEG_06|Verify quantity can't exceed the stock available.|

---

## 🎨 **3. UI/UX Test Cases**

|Test Case ID|Description|
|---|---|
|TC_CART_UI_01|Verify cart icon and item count are displayed properly in the navigation bar.|
|TC_CART_UI_02|Verify product images, names, prices, and quantity selectors are aligned.|
|TC_CART_UI_03|Verify "Remove" and "Move to Wishlist" (if any) buttons are visible.|
|TC_CART_UI_04|Verify CTA (checkout, continue shopping) buttons are correctly labeled and positioned.|
|TC_CART_UI_05|Verify responsive design of the cart page on mobile and tablet.|

---

## 🧪 **4. Functional Edge Cases**

|Test Case ID|Description|
|---|---|
|TC_CART_EDGE_01|Verify cart behavior after session timeout or user logout.|
|TC_CART_EDGE_02|Verify behavior when product goes out-of-stock after being added to cart.|
|TC_CART_EDGE_03|Verify cart total after applying/removing coupon codes multiple times.|
|TC_CART_EDGE_04|Verify product price updates in cart if there's a price change after it's added.|
|TC_CART_EDGE_05|Verify adding the same item multiple times correctly increases quantity.|

---

## 🔒 **5. Security Test Cases**

|Test Case ID|Description|
|---|---|
|TC_CART_SEC_01|Verify cart data is encrypted when stored in cookies/localStorage.|
|TC_CART_SEC_02|Verify user A cannot see or manipulate user B’s cart items.|
|TC_CART_SEC_03|Verify that cart cannot be manipulated through URL tampering or parameter injection.|
|TC_CART_SEC_04|Verify secure APIs are used for cart operations (HTTPS, auth tokens, etc.).|

---

## 🌐 **6. Compatibility Test Cases**

|Test Case ID|Description|
|---|---|
|TC_CART_COMP_01|Verify cart functionality across different browsers (Chrome, Firefox, Safari, Edge).|
|TC_CART_COMP_02|Verify cart functionality across different devices (iOS, Android, desktop).|
|TC_CART_COMP_03|Verify cart behavior in slow internet conditions.|
|TC_CART_COMP_04|Verify cart actions in private/incognito mode.|

---

## 🚀 **7. Performance Test Cases**

|Test Case ID|Description|
|---|---|
|TC_CART_PERF_01|Verify page load time of cart with multiple items (should be under 3-5 seconds).|
|TC_CART_PERF_02|Verify adding/removing/updating cart items responds within acceptable time.|
|TC_CART_PERF_03|Verify system behavior when thousands of users perform cart operations simultaneously.|

---

## 🧾 Optional – Additional Test Ideas:

- **Email cart to self / share cart link** (if feature exists).
    
- **Cart syncing across devices after login** (useful in cross-platform experience).
    
- **Cart auto-saving and expiration policy** (some apps keep cart data for 30 days).

## 🔍 **More Edge Cases for Cart Functionality**

|Test Case ID|Description|
|---|---|
|TC_CART_EDGE_06|Add a product to cart, then delete the product from inventory (verify cart behavior).|
|TC_CART_EDGE_07|Add products in bulk (e.g., 99+ items or hundreds of SKUs) to test max capacity or handling.|
|TC_CART_EDGE_08|Add product A to cart, then change its variant (e.g., size or color) from the product page—verify cart update.|
|TC_CART_EDGE_09|Add product to cart when not logged in, then log in—verify cart merges or replaces correctly.|
|TC_CART_EDGE_10|Change address/location in the cart (if delivery/pincode impacts price or availability).|
|TC_CART_EDGE_11|Apply a coupon, then remove the eligible product from the cart—check coupon validity.|
|TC_CART_EDGE_12|Perform a cart operation while switching between tabs rapidly (concurrency behavior).|
|TC_CART_EDGE_13|Simultaneously access cart from two browser tabs and update quantities—verify sync.|
|TC_CART_EDGE_14|Add product to cart, then change system date/time and proceed to checkout—check if cart expiration affects flow.|
|TC_CART_EDGE_15|Add the same product from different pages (e.g., search vs product page)—verify quantity updates and product uniqueness.|