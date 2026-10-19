# 🛒 E-Commerce App (Flutter + Laravel)

A full-featured e-commerce mobile application built with **Flutter** and a **Laravel** REST API. It covers the complete shopping journey: browsing products, cart, favorites, discount coupons, secure **Stripe** payments, and live order tracking. It is connected to a companion **Delivery app**, so every order placed by a customer reaches a driver and can be followed in real time.


## ✨ Features

**Shopping experience**
- Browse products by categories, with search
- Product details with images, description, and pricing
- Add to cart, update quantities, and remove items
- Favorites (wishlist) to save products for later
- Discount coupons applied at checkout, with the total updated instantly

**Payments**
- Secure card payments with **Stripe**
- Handling of successful, failed, and cancelled payments

**Orders & tracking**
- Order summary and confirmation
- Live order tracking powered by Firebase
- Order history

**Delivery integration**
- Connected to the companion [Delivery app](https://github.com/Ahmadhamdi200015/delivery): new orders are sent to drivers, and status updates flow back to the customer

**Notifications**
- Push notifications for order updates and offers (Firebase Cloud Messaging)

## 🔄 Purchase Flow
Browse → Add to Cart / Favorites → Apply Coupon → Checkout (Stripe)
→ Order Confirmed → Driver Assigned (Delivery App) → Live Tracking → Delivered



## 🛠 Tech Stack

| Area | Technology |
|------|------------|
| Mobile app | Flutter / Dart |
| State management & routing | GetX (Bindings, Controllers, Named Routes) |
| Backend & database | Laravel REST API |
| Payments | Stripe |
| Live tracking & push notifications | Firebase (Cloud Messaging + [Firestore / Realtime Database]) |

## 🗂 Project Structure
lib/
├── binding/ # GetX dependency bindings
├── controller/ # GetX controllers (app logic and state)
├── core/ # constants, helpers, shared utilities
├── data/
│ ├── datasource/ # API calls to the Laravel backend
│ └── model/ # data models
├── view/
│ ├── screen/ # app screens
│ └── widget/ # reusable widgets
├── applink.dart # API endpoints
├── firebase_options.dart
├── main.dart
└── routes.dart

## 🚀 Getting Started

1. Clone the repository
```bash
   git clone https://github.com/Ahmadhamdi200015/e-commerce.git
   cd e-commerce
```
2. Install dependencies
```bash
   flutter pub get
```
3. Set the API base URL of your Laravel backend in `lib/applink.dart`
4. Add your own Firebase config (`google-services.json` / `GoogleService-Info.plist`) for tracking and notifications
5. Add your Stripe **test** publishable key
6. Run the app
```bash
   flutter run
```

> Use Stripe test mode with the test card `4242 4242 4242 4242`.

## 👤 Author

**Ahmad Elkahlout**, Flutter Developer
Available for freelance work on [Upwork](#) and [Mostaql](#)
📧 elkahloutahmad5@gmail.com
