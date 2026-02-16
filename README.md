# 📄 Invoice Application

A modern, full-featured invoice management system built with Vue.js 3 and Firebase.

## 🌐 Live Demo

**[https://invoice-2fd34-5b493.web.app](https://invoice-2fd34-5b493.web.app)**

## ✨ Features

- 📝 Create and manage invoices
- 💾 Cloud storage with Firebase Firestore
- 🎨 Modern, responsive UI
- ⚡ Real-time data synchronization
- 🔒 Secure Firebase authentication

## 🛠️ Tech Stack

- **Frontend Framework:** Vue.js 3
- **State Management:** Vuex 4
- **Routing:** Vue Router 4
- **Styling:** SASS/SCSS
- **Backend:** Firebase (Firestore)
- **Build Tool:** Vue CLI
- **Deployment:** Firebase Hosting

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v14 or higher)
- **npm** (comes with Node.js)
- **Git** (for version control)

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone <repository-url>
cd vue-invoice-app
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

1. Copy the example environment file:
```bash
cp .env.example .env
```

2. Update `.env` with your Firebase project credentials:
```env
VUE_APP_FIREBASE_API_KEY=your_api_key_here
VUE_APP_FIREBASE_AUTH_DOMAIN=your_auth_domain_here
VUE_APP_FIREBASE_PROJECT_ID=your_project_id_here
VUE_APP_FIREBASE_STORAGE_BUCKET=your_storage_bucket_here
VUE_APP_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id_here
VUE_APP_FIREBASE_APP_ID=your_app_id_here
```

### 4. Run Development Server

```bash
npm run dev
```

The app will be available at **http://localhost:8080/**

## 📦 Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server with hot-reload (recommended) |
| `npm run serve` | Alternative dev server command |
| `npm run build` | Build for production |
| `npm run lint` | Lint and fix code |

## 🏗️ Building for Production

```bash
npm run build
```

This creates an optimized production build in the `dist/` directory.

## 🚀 Deployment

### Deploy to Firebase Hosting

1. **Install Firebase CLI** (if not already installed):
```bash
npm install -g firebase-tools
```

2. **Login to Firebase**:
```bash
firebase login
```

3. **Deploy**:
```bash
firebase deploy --only hosting:invoice-2fd34-5b493
```

Your app will be deployed to: **https://invoice-2fd34-5b493.web.app**

## 📁 Project Structure

```
vue-invoice-app/
├── public/              # Static assets
├── src/
│   ├── assets/         # Images, fonts, etc.
│   ├── components/     # Vue components
│   ├── firebase/       # Firebase configuration
│   ├── router/         # Vue Router configuration
│   ├── store/          # Vuex store
│   ├── views/          # Page components
│   ├── App.vue         # Root component
│   └── main.js         # Entry point
├── dist/               # Production build (generated)
├── firebase.json       # Firebase hosting config
├── .firebaserc         # Firebase project config
└── package.json        # Dependencies and scripts
```

## 🔧 Configuration Files

- **firebase.json** - Firebase Hosting configuration
- **.firebaserc** - Firebase project settings
- **babel.config.js** - Babel configuration
- **.eslintrc.js** - ESLint rules

## 🐛 Troubleshooting

### OpenSSL Error on Node.js v20+

If you encounter an OpenSSL error, the project includes the `cross-env` package to handle this automatically. Use:

```bash
npm run dev
```

Alternatively, you can manually set the environment variable:

**PowerShell:**
```powershell
$env:NODE_OPTIONS="--openssl-legacy-provider"; npm run serve
```

**Bash/Linux/Mac:**
```bash
NODE_OPTIONS=--openssl-legacy-provider npm run serve
```

## 🔐 Firebase Setup

1. Create a Firebase project at [Firebase Console](https://console.firebase.google.com/)
2. Enable Firestore Database
3. Configure authentication (if needed)
4. Update credentials in `src/firebase/firebaseInit.js`

## 📝 License

MIT License

## 👨‍💻 Author

Built with ❤️ using Vue.js and Firebase

---

## 📞 Support

For issues or questions, please open an issue in the repository.
