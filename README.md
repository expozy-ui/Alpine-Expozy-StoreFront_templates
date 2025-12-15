# 🎨 Expozy Themes Collection

This repository contains **official front-end themes for the Expozy platform**.

Each theme is a **static package** consisting only of:

- HTML templates  
- TailwindCSS utility classes  
- Images and static assets  

All themes are designed to work **out-of-the-box** with the **Expozy Core Front-End Framework**, without modifying core logic or JavaScript behavior.

---

## 🧩 What Are Expozy Themes?

Expozy themes define **visual structure and layout only**.

They do **not** include:
- Backend logic
- API logic
- JavaScript framework code
- Build tools or bundlers

Themes rely entirely on:
- Expozy Core routing
- Global Alpine `data` object
- ApiData & alpineListener directives
- Dynamic TailwindCSS class generation

---

## 📦 Included Themes

Currently, the collection includes **4 official themes**:

### 🛒 E-Commerce Theme
Clean and modern online shop with full shopping functionality.

### 🏨 Hotel Theme
Hotel presentation with room listings and reservation flow.

### 📅 Reservation System Theme
External reservation management with admin control.

### 📰 Default (Content / Blog) Theme
Minimalist content-focused theme for blogs and corporate sites.

---

## 📁 Theme Structure

```
/theme-name
├── assets/
│   ├── images/
│   ├── icons/
│   └── styles/
├── pages/
├── components/
└── README.md
```

---

## 🔌 Integration With Expozy Core

Themes automatically work with Expozy Core using ApiData, alpineListener, and dynamic routing.

---

## 🌍 Language Support

Themes are language-agnostic and compatible with Expozy’s translation system.

---

## 🎨 Styling Guidelines

- TailwindCSS utilities only
- No inline styles
- No compiled CSS
- Fully responsive layouts

---

## 🚀 Getting Started

1. Copy the theme folder into your project
2. Select it from the Expozy admin panel
3. Customize content and assets
4. Deploy

---

## 🔗 Resources

- Expozy Platform: https://expozy.com  
- Documentation: https://wiki.expozy.com  
