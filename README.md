# 🛒 Online Resale Marketplace with Secure Payment & Role-Based Access Control
### Full-Stack MERN Application (React.js + Node.js + Express + MongoDB + Stripe)

A complete **resale marketplace** platform supporting **buyers, sellers, and admins** with secure role-based access.  
Built as a **BSc Final Year Project**, demonstrating full-stack development, API design, authentication, and real payment integration.

---

## 🔗 Live Demo & Repositories

- **Live Site:** https://resale-1.web.app/  
- **Client Repository:** https://github.com/itskawsarjamil/resale-client  
- **Server Repository:** https://github.com/itskawsarjamil/resale-server
---

## 📖 Project Summary

A full-stack resale marketplace where buyers, sellers, and admins can manage their activities using a secure, role-based system.
The application supports:
- Multi-role authentication
- Seller product management
- Buyer wishlist
- Advertisement system
- Secure payments (Stripe)
- Order tracking
- Admin verification & monitoring

This project is suitable as a BSc Final Year Project, demonstrating frontend development, backend API architecture, authentication, database design, and payment integration.

---

## 🧑‍💻 Admin Credentials (Demo)

- **Email:** abc@gmail.com  
- **Password:** 123456
---

## 📌 1. Project Overview

This platform enables users to **buy and sell** used products.  
It includes secure **login**, **role-based dashboards**, real **Stripe payments**, product management, advertisements, wishlist, and admin monitoring.

---

## 🎯 2. Features

### 🔐 Authentication & Roles  
- JWT-based authentication  
- Google login  
- Roles:
  - Buyer  
  - Seller  
  - Admin  
- Protected API routes  

### 📦 Product Management  
- Add products (seller)  
- Browse category-wise products  
- Mark product as sold  
- Delete product (seller/admin)  

### 📢 Advertisement System  
- Seller can advertise items  
- Auto-remove after item is sold  
- Admin can manage ads  

### ❤️ Wishlist  
- Add to wishlist  
- Prevent duplicate items  
- Auto-remove after purchase  

### 🛒 Orders  
- Create orders  
- Track order status  
- Mark orders as paid  

### 🧑‍💼 Admin Dashboard  
- Manage all buyers & sellers  
- Verify sellers  
- Remove inappropriate products  

### 💳 Secure Payment  
- Stripe payment integration  
- Payment intent creation  
- Store transactions  
- Auto-update:
  - Product → Sold  
  - Ads → Removed  
  - Wishlist → Updated  

---

## 🛠️ 3. Technologies Used

### Frontend
- React.js  
- React Router  
- Context API  
- Tailwind CSS  
- Axios  

### Backend
- Node.js  
- Express.js  
- MongoDB  
- JWT  
- Stripe API  

### Tools / Deployment
- Firebase (Auth + Hosting)  
- Vercel / Netlify (Frontend)  
- Render / Railway (Backend)  

---

## 📂 4. Folder Structure

### Backend (`resale-server`)
```

resale-server/
│── server.js
└── config/

```

### Frontend (`resale-client`)
```

resale-client/
│── src/
│   │── components/
│   │── pages/
│   │── hooks/
│   │── context/
│   └── styles/
└── public/

```

---

## 🔌 5. API Endpoints

### Authentication
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/jwt` | Generate JWT |
| POST | `/users` | Register user |
| POST | `/g-users` | Google user |

### User Roles
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/isseller/:email` | Check if seller |
| GET | `/isadmin/:email` | Check if admin |
| GET | `/iswhat/:email` | Get user role |

### Products
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/addbook` | Add product |
| GET | `/books` | Seller products |
| GET | `/CategoryBooks/:id` | Products by category |
| GET | `/categoryid` | Category by name |
| DELETE | `/deletebook/:id` | Delete product |

### Advertisement
| Method | Endpoint | Description |
|--------|----------|-------------|
| PUT | `/adv/:id` | Advertise product |
| PUT | `/offadv/:id` | Remove ad |
| GET | `/adv` | Get ads |

### Wishlist
| Method | Endpoint | Description |
|--------|----------|-------------|
| PUT | `/wishlist/:id` | Add wishlist item |
| GET | `/wishlist?email=` | Get wishlist |
| DELETE | `/wishlist/:id` | Remove wishlist |

### Orders
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/orders` | Create order |
| GET | `/orders?email=` | User orders |
| GET | `/order/:id` | Single order |
| GET | `/issold/:id` | Check product status |

### Payments
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/create-payment-intent` | Stripe payment intent |
| POST | `/payments` | Store payment |

---

## 🧠 6. System Architecture (Overview)

1. User registers/login → JWT generated  
2. Seller lists products  
3. Buyer views categories and products  
4. Buyer:
   - Adds to wishlist  
   - Places order  
   - Pays via Stripe  
5. After payment:
   - Product marked sold  
   - Ad removed  
   - Wishlist updated  
6. Admin monitors everything  

---

## 🚀 7. Future Improvements

- Fully custom admin panel  
- Product ratings & reviews  
- Buyer–seller real-time chat  
- Notification system  
- Image optimization  
- CI/CD deployment pipeline  

---

## 🧪 8. Testing

- Backend API tests  
- Manual UI testing  
- JWT route protection tests  
- Stripe test mode validation  

---

## 📜 9. License

This project is open-source and free to use.


