# Cherry Cheek — E-Commerce Platform

**Cherry Cheek** is a modern, responsive, plant-powered cosmetic & skincare e-commerce web application. Built with React and designed with modular styling, this project features dynamic state management via `localStorage`, role-based access flows (Customer & Admin), and a synchronized local JSON architecture.

---

## Key Features

### Client / Customer Experience
- **Dynamic Catalog & Filtering**: Browse skincare and cosmetic products with real-time category filtering and text search.
- **Product Detail View**: View detailed product specifications, ingredients, stock availability, rating summaries, and multi-size selections.
- **Cart & Wishlist Synchronization**: Real-time cross-component badge updates (`cartUpdated`, `wishlistUpdated`, and `storage` global event listeners).
- **Interactive Checkout Flow**:
  - Live summary calculation with dynamic subtotal, delivery fee, and discount codes (e.g., `BEAUTY10`).
  - Supports multiple payment methods (Card, ABA PAY, Cash on Delivery, Bank Transfer).
  - Synchronized state clearing upon order placement.
- **Responsive Layout**: Hamburger navigation for mobile viewports, sticky header, and scalable footer.

### Admin Dashboard
- **Inventory Management**: Full CRUD operations for product inventory.
- **Image File Upload**: Support for converting local image uploads to Base64 data URLs for seamless product previewing and persistence.
- **Read-Only Detail Modal**: Inspect individual product metrics (SKU, Category, Stock, Pricing).
- **Real-Time Stock Alerts**: Visual badge indicators for low stock items (< 15 units).
- **Pagination & Search**: Instant filtering by product name or SKU across paginated tables.

---

## Project Architecture

```text
src/
├── assets/
│   └── images/              # Theme logos and default fallback assets
├── components/
│   ├── common/              # Shared UI components (Button, Review, etc.)
│   ├── Footer.jsx           # Responsive footer with theme switching
│   ├── Header.jsx           # Sticky nav bar with badge counters & mobile menu
│   └── Hero.jsx             # Hero banner section
├── data/
│   ├── accounts.json        # User credentials and roles (Admin/Cashier/Customer)
│   ├── categories.json      # Product category mappings
│   ├── invoices.json        # Customer purchase records
│   └── products.json        # Initial product catalog dataset
├── pages/
│   ├── About.jsx            # Brand story, mission, and stats page
│   ├── Checkout.jsx         # Dynamic checkout & order summary page
│   ├── Contact.jsx          # Contact page with integrated map & enquiry form
│   ├── Dashboard.jsx        # Admin inventory management dashboard
│   └── ProductDetail.jsx    # Individual product showcase page
└── App.css                  # Core CSS variables, typography, and dark mode root definitions
```

---

## Theme & Design System

The application relies on CSS variables declared in `App.css` to maintain theme consistency across light and dark modes:

- **Primary Color**: `#1D4533` (Forest Green)
- **Secondary Color**: `#FAFAFA`
- **Typography**: Poppins (`--font-sans`)
- **Theme Support**: Includes `[data-theme="dark"]` attribute toggling.

---

## Getting Started

### Prerequisites
- Node.js (v16+ recommended)
- npm

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/cherry-cheek.git
   cd cherry-cheek
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. Open your browser at `http://localhost:5173` (or your Vite local port).

---

## Promo Codes & Features to Try

- **Discount Code**: Enter `BEAUTY10` at checkout to apply a 10% discount.
- **Local Storage Integration**: Add items to your cart or wishlist and notice header counter badges update instantly across all open tabs.
- **Admin Testing**: Head to the admin dashboard to upload product images directly from your device file picker!

---

## License
This project is open-source and available under the [MIT License](LICENSE).