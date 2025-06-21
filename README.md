# 🔐 Firebase Auth Next.js

A modern, secure, and beautifully designed authentication system built with Next.js 14, Firebase Authentication, and Tailwind CSS. This project provides a complete user authentication flow with a clean, responsive interface and enterprise-grade security.

![Next.js](https://img.shields.io/badge/Next.js-14.2.30-black?style=for-the-badge&logo=next.js&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-11.9.1-orange?style=for-the-badge&logo=firebase&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?style=for-the-badge&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4.1-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

## ✨ Features

### 🎯 **Authentication**

- **Email/Password Authentication** - Secure user registration and login
- **Protected Routes** - Automatic redirection for authenticated/unauthenticated users
- **Persistent Sessions** - User state maintained across browser sessions
- **Real-time Auth State** - Instant UI updates based on authentication status
- **Form Validation** - Client-side validation with user-friendly error messages

### 🎨 **User Interface**

- **Modern Design** - Clean, professional interface with gradient backgrounds
- **Responsive Layout** - Optimized for desktop, tablet, and mobile devices
- **Loading States** - Smooth loading indicators and transitions
- **Error Handling** - Graceful error display with actionable feedback
- **Accessibility** - ARIA labels and keyboard navigation support

### 📊 **Dashboard Features**

- **User Profile Display** - Email, user ID, account creation date, and verification status
- **Statistics Overview** - Visual cards showing account status and activity
- **Quick Actions** - Profile management, settings, and data export options
- **Secure Logout** - Safe session termination with loading states

## 🚀 Getting Started

### Prerequisites

- Node.js 18.0 or later
- npm package manager
- Firebase project with Authentication enabled

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/firebase-auth-next.git
   cd firebase-auth-next
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Set up Firebase configuration**

   Create a `.env.local` file in the root directory and add your Firebase configuration:

   ```env
   NEXT_PUBLIC_FIREBASE_API_KEY=your_api_key_here
   NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_project_id.firebaseapp.com
   NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
   NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_project_id.appspot.com
   NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
   NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id
   NEXT_PUBLIC_FIREBASE_MEASUREMENT_ID=your_measurement_id
   ```

4. **Run the development server**

   ```bash
   npm run dev
   ```

5. **Open your browser**

   Navigate to [http://localhost:3000](http://localhost:3000) to see the application.

## 🔧 Firebase Setup

### 1. Create a Firebase Project

1. Go to the [Firebase Console](https://console.firebase.google.com/)
2. Click "Create a project" and follow the setup wizard
3. Choose your project name and configure Google Analytics (optional)

### 2. Enable Authentication

1. In your Firebase project console, navigate to **Authentication**
2. Click on the **Sign-in method** tab
3. Enable **Email/Password** authentication
4. (Optional) Configure additional providers like Google, GitHub, etc.

### 3. Get Your Config Keys

1. Go to **Project Settings** (gear icon)
2. Scroll down to **Your apps** section
3. Click on the web app icon `</>`
4. Register your app and copy the configuration object
5. Add these values to your `.env.local` file

## 📁 Project Structure

```
src/
├── app/
│   ├── components/
│   │   └── ProtectedRoute.tsx    # HOC for route protection
│   ├── config/
│   │   └── firebaseConfig.ts     # Firebase initialization
│   ├── context/
│   │   └── AuthContext.tsx       # Authentication context provider
│   ├── dashboard/
│   │   └── page.tsx              # Protected dashboard page
│   ├── login/
│   │   └── page.tsx              # User login page
│   ├── signup/
│   │   └── page.tsx              # User registration page
│   ├── utils/
│   │   └── auth.ts               # Authentication helper functions
│   ├── globals.css               # Global styles and Tailwind imports
│   ├── layout.tsx                # Root layout with AuthProvider
│   └── page.tsx                  # Landing page
├── firebase-env-example.txt       # Environment variables template
└── README.md                     # Project documentation
```

## 🛡️ Security Features

- **Protected Routes**: Automatic redirection for unauthorized access
- **Input Validation**: Client-side form validation with error handling
- **Secure Sessions**: Firebase handles session management and token refresh
- **HTTPS Only**: Environment configured for secure connections
- **No Sensitive Data Exposure**: All Firebase config uses public keys only

## 🎨 Styling

This project uses **Tailwind CSS** for styling with:

- **Responsive Design**: Mobile-first approach with breakpoint-specific styles
- **Custom Color Palette**: Professional blue and gray color scheme
- **Modern Components**: Cards, buttons, forms with consistent styling
- **Smooth Animations**: Hover effects, loading spinners, and transitions

## 📱 Pages Overview

### 🏠 **Landing Page (`/`)**

- Hero section with compelling call-to-action
- Feature highlights and benefits
- Navigation to sign-up and login pages
- Auto-redirect to dashboard for authenticated users

### 🔑 **Login Page (`/login`)**

- Email and password input fields
- Remember me checkbox
- Forgot password link (UI only)
- Social login buttons (GitHub, Google - UI only)
- Link to registration page

### 📝 **Signup Page (`/signup`)**

- Full name, email, and password fields
- Password confirmation with validation
- Terms acceptance and privacy policy links
- Auto-redirect to dashboard on successful registration

### 📊 **Dashboard Page (`/dashboard`)**

- User information display
- Account statistics and status
- Quick action buttons
- Secure logout functionality

## 🔄 Authentication Flow

1. **User Registration**: Create account with email/password
2. **Email Verification**: Firebase sends verification email (optional)
3. **User Login**: Authenticate with registered credentials
4. **Session Management**: Firebase maintains secure session
5. **Protected Access**: Dashboard and user-specific content
6. **Secure Logout**: Clear session and redirect to login

## 🚀 Deployment

### Vercel (Recommended)

1. Push your code to GitHub
2. Connect your repository to [Vercel](https://vercel.com)
3. Add your environment variables in the Vercel dashboard
4. Deploy automatically on every push

### Other Platforms

- **Netlify**: Add environment variables and deploy
- **Railway**: Configure environment and deploy
- **Heroku**: Set config vars and deploy

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🛠️ Built With

- **[Next.js 14](https://nextjs.org/)** - React framework for production
- **[Firebase Authentication](https://firebase.google.com/products/auth)** - Secure authentication service
- **[TypeScript](https://www.typescriptlang.org/)** - Type-safe JavaScript
- **[Tailwind CSS](https://tailwindcss.com/)** - Utility-first CSS framework
- **[React Context API](https://reactjs.org/docs/context.html)** - State management

## 📞 Support

If you have any questions or need help with setup, please:

1. Check the [Issues](https://github.com/yourusername/firebase-auth-next/issues) page
2. Create a new issue with detailed information
3. Include your environment details and error messages

## 🎯 Roadmap

- [ ] Password reset functionality
- [ ] Social authentication (Google, GitHub)
- [ ] Email verification flow
- [ ] User profile editing
- [ ] Multi-factor authentication
- [ ] Admin dashboard
- [ ] User role management

## ⭐ Show Your Support

If this project helped you or you found it useful, please consider giving it a star! ⭐

It helps others discover this project and motivates me to keep improving it.

### 🤝 Connect With Me

- 💼 **Found a bug or have a feature request?** [Open an issue](https://github.com/mudasir45/firebase-auth-next/issues)
- 💡 **Have questions or want to collaborate?** Feel free to reach out!
- 🌟 **Enjoying this project?** Give it a star and share it with others
- 🐛 **Found this helpful?** Consider following for more awesome projects

### 📬 Get in Touch

- 📧 **Email**: [mudasiramin320@gmail.com](mailto:mudasiramin320@gmail.com)
- 💼 **LinkedIn**: [Mudassir Amin](https://www.linkedin.com/in/mudasiramin/)
- 🌐 **Website**: [imergesolutions.com](https://imergesolutions.com)

> _"Code is like humor. When you have to explain it, it's bad."_ – Cory House

---

**Made with ❤️ using Next.js and Firebase**

_Don't forget to ⭐ this repo if you found it helpful!_
