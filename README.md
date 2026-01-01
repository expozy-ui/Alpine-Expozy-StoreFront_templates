<p align="center">
  <img src="assets/expozy-ui-templates-logo.png" alt="Expozy Themes" width="400">
</p>

<h1 align="center">Expozy Themes Collection</h1>

<p align="center">
  <strong>Official Front-End Themes for the Expozy Platform</strong>
</p>

<p align="center">
  <a href="#themes"><img src="https://img.shields.io/badge/themes-4-red.svg" alt="Themes"></a>
  <a href="#license"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"></a>
  <a href="#styling"><img src="https://img.shields.io/badge/styling-TailwindCSS-38B2AC.svg" alt="TailwindCSS"></a>
  <a href="#integration"><img src="https://img.shields.io/badge/powered%20by-Alpine.js-8BC0D0.svg" alt="Alpine.js"></a>
</p>

---

## Overview

This repository contains **official front-end themes for the Expozy platform**. Each theme is a **static package** designed to work seamlessly with the **Expozy Core Front-End Framework**.

### What's Included

| ✅ Included | ❌ Not Included |
|-------------|-----------------|
| HTML templates | Backend logic |
| TailwindCSS utility classes | API logic |
| Images & static assets | JavaScript framework code |
| Responsive layouts | Build tools or bundlers |

> **Note:** Themes define **visual structure and layout only** — all dynamic functionality is handled by Expozy Core.

---

## 🧩 How Themes Work

Expozy themes rely entirely on the core framework:

```
┌─────────────────────────────────────────────────────────┐
│                    EXPOZY THEME                         │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐     │
│  │    HTML     │  │  Tailwind   │  │   Assets    │     │
│  │  Templates  │  │   Classes   │  │   Images    │     │
│  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘     │
└─────────┼────────────────┼────────────────┼────────────┘
          │                │                │
          ▼                ▼                ▼
┌─────────────────────────────────────────────────────────┐
│                   EXPOZY CORE                           │
│  • Routing          • Alpine.js data object             │
│  • ApiData          • alpineListener directives         │
│  • Dynamic CSS      • Translation system                │
└─────────────────────────────────────────────────────────┘
```

---

## 📦 Included Themes

### 🛒 E-Commerce Theme
Modern online shop with full shopping functionality.

| Feature | Description |
|---------|-------------|
| Product Catalog | Grid & list views with filtering |
| Shopping Cart | Add, remove, quantity management |
| Checkout Flow | Multi-step checkout process |
| User Account | Orders, wishlist, profile |

---

### 🏨 Hotel Theme
Elegant hotel presentation with booking capabilities.

| Feature | Description |
|---------|-------------|
| Room Listings | Gallery, amenities, pricing |
| Reservation Flow | Date picker, guest selection |
| Property Info | Location, facilities, contact |
| Special Offers | Promotions & packages |

---

### 📅 Reservation System Theme
External reservation management with admin control.

| Feature | Description |
|---------|-------------|
| Calendar View | Availability management |
| Booking Management | Create, edit, cancel |
| Customer Management | Guest profiles & history |
| Admin Dashboard | Overview & statistics |

---

### 📰 Default Theme (Content / Blog)
Minimalist content-focused theme for blogs and corporate sites.

| Feature | Description |
|---------|-------------|
| Blog Layout | Posts, categories, tags |
| Page Templates | About, contact, services |
| Media Support | Images, video embeds |
| SEO Optimized | Meta tags, structured data |

---

## 📁 Theme Structure

```
theme-name/
│
├── 📂 assets/
│   ├── 📂 images/          # Theme images & graphics
│   ├── 📂 icons/           # SVG icons & favicons
│   └── 📂 styles/          # Additional CSS (if needed)
│
├── 📂 pages/
│   ├── index.html          # Homepage
│   ├── product.html        # Product detail (e-commerce)
│   ├── category.html       # Category listing
│   └── ...                 # Other page templates
│
├── 📂 components/
│   ├── header.html         # Navigation header
│   ├── footer.html         # Site footer
│   ├── card.html           # Reusable card component
│   └── ...                 # Other components
│
└── 📄 README.md            # Theme documentation
```

---

## 🔌 Integration With Expozy Core

Themes automatically integrate with Expozy Core using:

| Directive | Purpose |
|-----------|---------|
| `ApiData` | Fetch and bind API data to templates |
| `alpineListener` | Handle user interactions & events |
| `x-data` | Alpine.js reactive data binding |
| `x-show` / `x-if` | Conditional rendering |
| `x-for` | List rendering & iteration |

### Example Usage

```html
<!-- Product listing with ApiData -->
<div x-data="ApiData('products')">
  <template x-for="product in items">
    <div class="bg-white rounded-lg shadow-md p-4">
      <img :src="product.image" :alt="product.name">
      <h3 x-text="product.name" class="text-lg font-bold"></h3>
      <p x-text="product.price" class="text-red-600"></p>
    </div>
  </template>
</div>
```

---

## 🌍 Language Support

Themes are **language-agnostic** and fully compatible with Expozy's translation system.

```html
<!-- Translation example -->
<h1 x-text="$t('welcome_message')"></h1>
<button x-text="$t('add_to_cart')"></button>
```

Supported features:
- RTL layout support
- Dynamic language switching
- Locale-specific formatting (dates, currencies)

---

## 🎨 Styling Guidelines

| ✅ Do | ❌ Don't |
|-------|----------|
| Use TailwindCSS utilities | Write custom CSS |
| Keep classes readable | Use inline styles |
| Design mobile-first | Ignore responsive design |
| Use CSS variables for theming | Hardcode colors |

### Color Customization

Themes use CSS variables for easy brand customization:

```css
:root {
  --color-primary: #E53E2E;
  --color-secondary: #1F2937;
  --color-accent: #F59E0B;
}
```

### Responsive Breakpoints

| Breakpoint | Prefix | Screen Width |
|------------|--------|--------------|
| Mobile | (default) | < 640px |
| Tablet | `sm:` | ≥ 640px |
| Laptop | `md:` | ≥ 768px |
| Desktop | `lg:` | ≥ 1024px |
| Large | `xl:` | ≥ 1280px |

---

## 🚀 Getting Started

### Quick Start

```bash
# 1. Clone the repository
git clone https://github.com/expozy/expozy-themes.git

# 2. Choose a theme
cd expozy-themes/ecommerce-theme

# 3. Copy to your Expozy project
cp -r . /path/to/your/expozy/themes/
```

### Installation Steps

1. **Copy Theme** — Place the theme folder in your Expozy project's `themes/` directory

2. **Select Theme** — Navigate to **Admin Panel → Appearance → Themes** and activate your theme

3. **Customize** — Modify assets, colors, and content to match your brand

4. **Deploy** — Push changes to your production environment

---

## 🛠️ Customization

### Creating a Child Theme

To customize without modifying the original theme:

```
my-custom-theme/
├── 📄 theme.json          # Extends parent theme
├── 📂 assets/
│   └── 📂 images/         # Override images
└── 📂 components/
    └── header.html        # Override header only
```

```json
// theme.json
{
  "name": "My Custom Theme",
  "extends": "ecommerce-theme",
  "version": "1.0.0"
}
```

---

## 📋 Theme Comparison

| Feature | E-Commerce | Hotel | Reservation | Default |
|---------|:----------:|:-----:|:-----------:|:-------:|
| Product Catalog | ✅ | ❌ | ❌ | ❌ |
| Shopping Cart | ✅ | ❌ | ❌ | ❌ |
| Room Booking | ❌ | ✅ | ❌ | ❌ |
| Calendar View | ❌ | ✅ | ✅ | ❌ |
| Blog Support | ✅ | ✅ | ❌ | ✅ |
| User Accounts | ✅ | ✅ | ✅ | ❌ |
| Admin Panel | ❌ | ❌ | ✅ | ❌ |

---

## 🔗 Resources

| Resource | Link |
|----------|------|
| 🌐 Expozy Platform | [expozy.com](https://expozy.com) |
| 📖 Documentation | [wiki.expozy.com](https://wiki.expozy.com) |
| 💬 Community | [Discord](https://discord.gg/expozy) |
| 🐛 Issue Tracker | [GitHub Issues](https://github.com/expozy/expozy-themes/issues) |

---

## 🤝 Contributing

We welcome contributions! Whether it's a new theme, bug fix, or improvement.

1. Fork the repository
2. Create your branch (`git checkout -b feature/my-theme`)
3. Commit changes (`git commit -m 'Add new theme'`)
4. Push to branch (`git push origin feature/my-theme`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  Made with ❤️ by the <a href="https://expozy.com">Expozy</a> Team
</p>
