# 🍕 Phaellos - Roda Pizza Management System

[![Next.js](https://img.shields.io/badge/Next.js-15.3.4-000000?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19.0.0-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Sass](https://img.shields.io/badge/Sass-1.89.2-CC6699?style=for-the-badge&logo=sass&logoColor=white)](https://sass-lang.com/)
[![Axios](https://img.shields.io/badge/Axios-1.10.0-5A29E4?style=for-the-badge&logo=axios&logoColor=white)](https://axios-http.com/)

A comprehensive restaurant management system built with Next.js 15 and React 19, designed specifically for pizzerias and restaurants. Features complete order management, product catalog, category organization, and real-time dashboard updates.

## 🚀 Features

### 🔐 Authentication System
- **Secure Login/Register** with JWT token authentication
- **Session Management** with HTTP-only cookies
- **Protected Routes** with middleware validation
- **Auto-logout** functionality with toast notifications

### 📊 Dashboard Management
- **Real-time Order Tracking** with live updates
- **Order Status Management** (draft, active, completed)
- **Interactive Order Details** with modal dialogs
- **Order Completion** workflow with confirmation

### 🍕 Product Management
- **Product Registration** with image upload
- **Category-based Organization** for menu items
- **Image Preview** functionality during upload
- **Comprehensive Product Details** (name, price, description)

### 🏷️ Category Management
- **Dynamic Category Creation** for menu organization
- **Category-based Product Filtering**
- **Server-side Form Handling** with validation

### 🎨 User Experience
- **Responsive Design** optimized for all devices
- **Toast Notifications** for user feedback (Sonner)
- **Loading States** with form status indicators
- **Smooth Animations** and hover effects
- **Modern UI** with custom Sass styling

## 🛠️ Technologies Used

### Frontend Framework
- **Next.js 15.3.4** - React framework with App Router
- **React 19.0.0** - Latest React with concurrent features
- **TypeScript 5.0+** - Type-safe development

### Styling & UI
- **Sass 1.89.2** - Advanced CSS preprocessing
- **CSS Modules** - Scoped styling architecture
- **Lucide React 0.525.0** - Modern icon library
- **Responsive Design** - Mobile-first approach

### State Management & Communication
- **React Context API** - Global state management
- **Axios 1.10.0** - HTTP client for API requests
- **Cookies-next 6.0.0** - Cookie management utility
- **Server Actions** - Next.js server-side form handling

### Developer Experience
- **Sonner 2.0.6** - Toast notification system
- **ESLint & TypeScript** - Code quality and type checking
- **Custom Hooks** - Reusable stateful logic

## 📁 Project Structure

```
src/
├── app/
│   ├── dashboard/
│   │   ├── category/              # Category management
│   │   │   ├── page.tsx           # Category creation page
│   │   │   └── styles.module.scss # Category styling
│   │   ├── product/               # Product management
│   │   │   ├── components/form/   # Product form component
│   │   │   └── page.tsx           # Product page
│   │   ├── components/
│   │   │   ├── header/            # Dashboard navigation
│   │   │   ├── button/            # Reusable button component
│   │   │   ├── modal/             # Order details modal
│   │   │   └── orders/            # Orders list component
│   │   ├── layout.tsx             # Dashboard layout wrapper
│   │   └── page.tsx               # Main dashboard page
│   ├── singup/
│   │   └── page.tsx               # User registration
│   ├── globals.scss               # Global styles and variables
│   ├── layout.tsx                 # Root layout configuration
│   └── page.tsx                   # Login page
├── lib/
│   ├── cookieClient.ts            # Client-side cookie utilities
│   ├── cookieServer.ts            # Server-side cookie utilities
│   └── order.types.ts             # TypeScript type definitions
├── providers/
│   └── order.tsx                  # Order context provider
├── services/
│   └── api.ts                     # Axios API configuration
└── middleware.ts                  # Next.js middleware for auth
```

## 🎯 Key Components

### Authentication Flow
- **Login Page** (`/`) - Email/password authentication with JWT
- **Registration Page** (`/singup`) - New user account creation
- **Middleware Protection** - Automatic route protection and token validation

### Dashboard Features
- **Orders Management** - Real-time order tracking with refresh capability
- **Order Details Modal** - Complete order information with product images
- **Order Completion** - One-click order finishing with status updates

### Product & Category System
- **Dynamic Forms** - Server-side form handling with validation
- **Image Upload** - File handling with preview functionality
- **Category Selection** - Dropdown integration with real-time data

## 🔧 Installation & Setup

### Prerequisites
- Node.js (version 18 or higher)
- npm, yarn, or pnpm package manager
- Backend API server running on `localhost:3333`

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/cristovaojr/pizzaria-frontend.git
   cd pizzaria-frontend
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   # or
   pnpm dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000`

### Build for Production
```bash
npm run build
npm start
```

## 🌐 API Integration

The application integrates with a REST API backend:

- **Base URL**: `http://localhost:3333`
- **Authentication**: Bearer token (JWT)
- **Endpoints**:
  - `POST /session` - User authentication
  - `POST /users` - User registration
  - `GET /me` - Token validation
  - `GET /orders` - Fetch orders
  - `GET /order/detail` - Order details
  - `PUT /order/finish` - Complete order
  - `GET /category` - Fetch categories
  - `POST /category` - Create category
  - `POST /product` - Create product

## 🎨 Design System

### Color Palette
- **Primary Orange**: `#bb641d` (--orange-900)
- **Secondary Orange**: `#c59670` (--orange-300)
- **Success Green**: `#2aa168` (--green-900)
- **Error Red**: `#a52a2a` (--red-900)
- **Neutral Gray**: `#8a8a8a` (--gray-100)

### Typography
- **Font Family**: Geist Sans & Geist Mono
- **Responsive Scaling**: Adaptive font sizes for different screen sizes

### Layout Features
- **Mobile-First Design**: Responsive breakpoints at 720px and 1080px
- **Consistent Spacing**: Standardized margins and padding
- **Smooth Transitions**: 0.5s transition effects on interactive elements

## 🔒 Security Features

- **JWT Authentication** with secure cookie storage
- **Protected Routes** via Next.js middleware
- **Token Validation** on every protected request
- **Session Management** with automatic expiration
- **HTTPS-only Cookies** in production environment

## 📱 Responsive Design

- **Desktop-First** with mobile adaptations
- **Flexible Layouts** using CSS Grid and Flexbox
- **Optimized Images** with Next.js Image component
- **Touch-Friendly** interface for mobile devices

## 🚀 Performance Features

- **Server-Side Rendering** with Next.js App Router
- **Optimized Images** with automatic WebP conversion
- **Code Splitting** with component-level optimization
- **Efficient Re-renders** with React 19 concurrent features
- **Minimal Bundle Size** with tree-shaking

## 🔮 Future Enhancements

- Multi-restaurant support
- Advanced analytics dashboard
- Inventory management system
- Customer loyalty program
- Real-time order notifications
- Mobile app development
- Payment integration
- Multi-language support

## 📱 Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS/Android)

## 🤝 Contributing

This project demonstrates modern React/Next.js development practices. Suggestions and feedback are welcome!

1. Fork the project
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 About the Developer

**Cristóvão Junior** - Full Stack Developer

This project demonstrates expertise in:
- **Modern React Development** (React 19, Next.js 15, TypeScript)
- **Advanced State Management** (Context API, Server Actions)
- **Authentication Systems** (JWT, Middleware, Session Management)
- **Responsive Design** (Sass, CSS Modules, Mobile-First)
- **API Integration** (Axios, RESTful Services, Error Handling)
- **User Experience** (Loading States, Toast Notifications, Form Validation)

---

**📧 Contact**: cristovao.b.jr@gmail.com | **💼 LinkedIn**: [linkedin.com/in/cristóvão-borges-junior-53880a226](https://linkedin.com/in/cristóvão-borges-junior-53880a226)

> Built with ❤️ by Cristóvão Junior using Next.js 15, React 19, and TypeScript