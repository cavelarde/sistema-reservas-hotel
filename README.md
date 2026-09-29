# sistema-reservas-hotel
El programa para la reserva y gestión de hotel es una aplicación web interactiva desarrollada en HTML, CSS y JavaScript con un backend en Google Apps Script. Está diseñado para centralizar la recepción, el control de hospedaje y la facturación.
# 🏨 Hotel Casa Grande Chamizal - Property Management System (PMS) & Invoicing

A modern, high-performance web-based Property Management System (PMS) and Invoicing platform tailored for the hospitality industry. This solution automates room booking logic, currency exchange overhead, and cloud data synchronization for independent hotels.

🚀 **Live Demo:** [View Application in Action](https://github.io)

---

## 🛠️ Tech Stack & Architecture

- **Frontend:** Semantic HTML5, Responsive UI with native CSS Variables (Design System tokens).
- **Icons & Typography:** Lucide Icons, Plus Jakarta Sans, Playfair Display.
- **Backend Architecture:** Serverless Webhooks integrated with Google Apps Script (Google Sheets DB).
- **Distribution:** Progressive Web App (PWA) structural layers capable of native desktop wrapping (.exe via Electron).

---

## ✨ Core Features & Technical Engineering

### 1. Advanced State Machine & Modular Form Architecture
The user interface features a tabbed-state architecture (`.tab-btn` control patterns) designed for front-desk operators. It isolates sensitive transaction fields across three secure modules: Guest Metadata, Room Inventory, and Fiscal Invoicing, ensuring maximum performance without UI re-renders.

### 2. Financial Logic & Asynchronous Stay Engines
- **Date Math Calculations:** Native JavaScript engine computing millisecond differences between Check-In and Check-Out inputs, dynamically parsing stay lengths while preventing anti-patterns (e.g., negative nights).
- **Dual-Currency Reactive Engine (COP / USD):** Instantly converts single-room unit costs and overall totals without calling external layout modules, updating values across the DOM in real-time.
- **Fiscal Tax & Compliance Modules:** Dynamic calculation arrays handling general Colombian VAT (19%), Impoconsumo (8%), or Foreign Tourist tax exemptions (0%).

### 3. Serverless Cloud Sinking (Webhooks API)
Leverages asynchronous `POST` requests via the Fetch API to pipe real-time invoicing data payload (Folio, Guest Doc, Nights, Subtotal, Currency) straight into a Serverless data repository via Google Apps Script web macros.

### 4. Hardware Print Mapping & DIAN Pre-Compliance
Includes a dedicated physical invoice generator matching local fiscal ticket structures. Features an active `@media print` layout stylesheet that dynamically wipes out administrative forms, sidebars, and control dashboards during hardware printing commands, delivering a clean 80mm POS receipt layout.

---

## 🗂️ Project Structure

```text
├── index.html          # Main application UI layout and components
├── css/
│   └── styles.css      # Core Design Tokens, Responsive Grids & Dark Mode layers
├── js/
│   └── script.js       # Asynchronous calculations, API calls & State Machine logic
└── README.md           # Technical engineering documentation
```

---

## ⚙️ Local Setup and Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   ```
2. **Launch locally:**
   Open the `index.html` file in any modern web browser or use a development server extension (e.g., Live Server in VS Code).

3. **Desktop Native App Wrapping (.exe):**
   This application is architected to be packaged into a standalone installer using Node.js and Electron frameworks.
