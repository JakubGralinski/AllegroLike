# AllegroStyle – Online Marketplace Platform

## 1. Application Name

**AllegroStyle – Online Marketplace Platform**

---

## 2. Problem Area

AllegroStyle is designed for the e-commerce sector, enabling a business to sell products online directly to customers. The system is intended for use as a web storefront for a single seller (the store owner/admin), serving individual buyers. It is suitable for retail businesses looking to establish an online presence and streamline sales to consumers.

---

## 3. Project Goals

The goal of AllegroStyle is to simplify and streamline the process of buying and selling goods online. The platform aims to provide a user-friendly interface, secure transactions, and efficient product management, supporting both buyers and sellers.

---

## 4. System Responsibilities

AllegroStyle will allow users to register, browse products, manage shopping carts, place orders, and manage their profiles. Sellers can add and manage products, while administrators oversee the platform.

---

## 5. System Users

- Guest (unregistered visitor)
- Registered Buyer (customer)
- Administrator (store owner/seller)

---

## 6. Functionalities

- User registration and authentication (for buyers)
- User profile management (for buyers)
- Product browsing and search
- Product filtering and categorization
- Product details view
- Shopping cart management
- Wishlist management
- Order placement and tracking
- Product management (CRUD for admin)
- Admin dashboard (user/product/order management)
- Ratings and reviews
- Responsive UI (desktop/mobile)
- Dark/light mode
- Product comparison
- Recently viewed items
- Address and shipping management
- Payment integration
- Inventory and stock management
- API documentation

---

## 7. User Requirements

### Part 1: Domain Structure (Entities, Properties, Relationships)

- **User**: id, name, email, password, address, role (buyer/admin), wishlist
- **Product**: id, name, description, price, stock, category, images
- **Order**: id, user_id, order_date, status, total_price, shipping_address
- **Cart**: id, user_id, items
- **CartItem**: id, cart_id, product_id, quantity
- **Review**: id, user_id, product_id, rating, comment
- **Category**: id, name, parent_category_id
- **Relationships**:
  - User has many Orders
  - User has one Cart
  - Product belongs to Category
  - Product has many Reviews
  - Order has many Products (through OrderItems)
  - Only the Admin can add/edit/delete Products

### Part 2: Expected Functionality

- Register/login/logout
- Edit profile
- Add/remove products (seller/admin)
- Search/filter products
- Add to cart/wishlist
- Place order
- Leave review
- Admin: manage users/products/orders

### Part 3: Constraints

- Must run on modern web browsers (Chrome, Firefox, Edge)
- User authentication must be secure (hashed passwords, JWT)
- System should handle at least 100 concurrent users
- Product search should return results in under 2 seconds
- Data must be backed up daily

---

## 8. Functional Requirements

- Use case diagram (to be created in a UML tool, e.g., draw.io, Lucidchart, or StarUML)
- Each use case should correspond to a functionality above

[See use case diagram](./AllegroLikeUseCase.png)

---

## 9. System Structure (Conceptual Diagram)

- Class diagram (UML) showing entities and relationships

_Placeholder: Insert class diagram image here._

---

## 10. Non-functional Requirements

| Constraint              | Metric                                                                     |
| ----------------------- | -------------------------------------------------------------------------- |
| Browser compatibility   | Must work on latest 3 versions of Chrome, Firefox, Edge (tested quarterly) |
| Authentication security | Passwords hashed with bcrypt, JWT tokens expire in 1 hour (security audit) |
| Performance             | 100 concurrent users, response time <2s (load testing)                     |
| Backup                  | Daily automated backup, retention for 30 days (backup logs)                |
| Uptime                  | 99% monthly uptime (monitoring logs)                                       |

---

## 11. Database Schema

- ERD diagram (can be made in dbdiagram.io, draw.io, etc.)
- List of tables, columns, and relationships

_Placeholder: Insert ERD diagram image here._

---

## 12. API Endpoints List

| Endpoint           | Method | Description                    |
| ------------------ | ------ | ------------------------------ |
| /api/auth/register | POST   | Register a new user            |
| /api/auth/login    | POST   | User login                     |
| /api/products      | GET    | List/search products           |
| /api/products/{id} | GET    | Get product details            |
| /api/products      | POST   | Add new product (seller/admin) |
| /api/products/{id} | PUT    | Edit product (seller/admin)    |
| /api/products/{id} | DELETE | Delete product (seller/admin)  |
| /api/cart          | GET    | Get user cart                  |
| /api/cart          | POST   | Add item to cart               |
| /api/cart/{itemId} | DELETE | Remove item from cart          |
| /api/orders        | POST   | Place order                    |
| /api/orders        | GET    | List user orders               |
| /api/reviews       | POST   | Add product review             |
| ...                | ...    | ...                            |

---

## 13. List of Used Technologies

| Technology     | Where Used   | Purpose                  |
| -------------- | ------------ | ------------------------ |
| React          | Frontend     | UI development           |
| TypeScript     | Frontend     | Type safety              |
| Spring Boot    | Backend      | REST API, business logic |
| Java           | Backend      | Core backend language    |
| PostgreSQL     | Database     | Data storage             |
| Liquibase      | Backend      | Database versioning      |
| Docker         | DevOps       | Containerization         |
| JWT            | Backend/Auth | User authentication      |
| bcrypt         | Backend/Auth | Password hashing         |
| Vite           | Frontend     | Build tool               |
| Github Actions | DevOps       | CI tool                  |

---

## 14. UI/UX Mockups

For each functionality, provide a wireframe or mockup (can use Figma, Balsamiq, or even hand-drawn and scanned)

- Example views: Home, Product List, Product Details, Cart, Checkout, Profile, Admin Panel

_Placeholder: Insert mockup images here._
