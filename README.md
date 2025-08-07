# ⚡ Humanoid Web App

A modern, responsive React application built with key libraries like `React Router`, `React Query`, `ShadCN UI`, and custom notification components. This project follows best practices for scalable frontend development.

---

## 📦 Tech Stack

- **React** – UI library
- **React Router DOM** – Client-side routing
- **TanStack React Query** – Server state management
- **ShadCN UI** – Customizable UI components
- **Custom Toaster/Sonner** – Notification system
- **Vite** – Build tool

---

## 🔧 Project Structure

src/
├── components/
│ └── ui/
│ ├── toaster.tsx # Notification component
│ ├── sonner.tsx # Another notification library or style
│ └── tooltip.tsx # Tooltip provider wrapper
├── pages/
│ ├── Index.tsx # Main page
│ └── NotFound.tsx # 404 fallback
├── App.tsx # Main app with routes and providers
└── main.tsx # Entry point

yaml

---

## 🚀 Features

- ✅ Toast and Sonner notification support
- ✅ Tooltip UI wrapper for hints
- ✅ Client-side routing with fallback (`NotFound`)
- ✅ Global state/query management using React Query
- ✅ Modular structure for scalable growth

---

## 🧪 Usage

### 1. Install dependencies

```bash
npm install
# or
yarn
2. Run in development
bash
npm run dev
# or
yarn dev
3. Build for production
bash
npm run build
✨ How It Works
In App.tsx:

tsx
<QueryClientProvider client={queryClient}>
  <TooltipProvider>
    <Toaster />         // Default toast messages
    <Sonner />          // Custom or alternative notifications
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Index />} />
        <Route path="*" element={<NotFound />} />
      </Routes>
    </BrowserRouter>
  </TooltipProvider>
</QueryClientProvider>
Toaster and Sonner: Used for handling different toast/alert styles.

TooltipProvider: Makes tooltips available across the app.

QueryClientProvider: React Query wrapper for API state and caching.

BrowserRouter: Enables routing.

Routes: Handles page navigation and fallback.

🛠️ Customization
You can add more pages like this:

tsx
<Route path="/dashboard" element={<Dashboard />} />
Or add API integration using useQuery() from @tanstack/react-query.

📁 Coming Soon
🧑‍⚕️ Admin & user dashboards

📊 API integration examples


🧠 Contributing
Feel free to fork this repo and submit PRs for improvements or new features.

📄 License
MIT License — free to use and modify.
