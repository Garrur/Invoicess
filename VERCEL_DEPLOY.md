# Vercel Deployment Guide

## 🚀 Deploying to Vercel

### Prerequisites
- GitHub repository (e.g., https://github.com/Garrur/Invoicess.git)
- Vercel account (sign up at [vercel.com](https://vercel.com))

### Step 1: Import Project to Vercel

1. Go to [Vercel Dashboard](https://vercel.com/dashboard)
2. Click **"Add New... → Project"**
3. Import your GitHub repository: `Garrur/Invoicess`
4. Vercel will auto-detect it as a Vue.js project

### Step 2: Configure Build Settings

**Framework Preset:** Vue.js  
**Build Command:** `npm run build`  
**Output Directory:** `dist`  
**Install Command:** `npm install`

### Step 3: Add Environment Variables

⚠️ **CRITICAL:** Add these environment variables in Vercel Project Settings → Environment Variables:

```bash
# Build Configuration (REQUIRED for Node.js v20+)
NODE_OPTIONS=--openssl-legacy-provider

# Firebase Configuration
VUE_APP_FIREBASE_API_KEY=AIzaSyAs0Q_vvmRekWXRSwBrcWTK_2N3ewSCW24
VUE_APP_FIREBASE_AUTH_DOMAIN=invoice-2fd34.firebaseapp.com
VUE_APP_FIREBASE_PROJECT_ID=invoice-2fd34
VUE_APP_FIREBASE_STORAGE_BUCKET=invoice-2fd34.firebasestorage.app
VUE_APP_FIREBASE_MESSAGING_SENDER_ID=493138830608
VUE_APP_FIREBASE_APP_ID=1:493138830608:web:f6d9b5eca19932fa2a7195
```

### Step 4: Deploy

Click **"Deploy"** and Vercel will:
1. Clone your repository
2. Install dependencies
3. Build the project with the environment variables
4. Deploy to a production URL

---

## 🔧 How to Add Environment Variables in Vercel

### Via Vercel Dashboard:

1. Go to your project in Vercel
2. Click **Settings** tab
3. Click **Environment Variables** in the sidebar
4. For each variable:
   - Enter the **Name** (e.g., `NODE_OPTIONS`)
   - Enter the **Value** (e.g., `--openssl-legacy-provider`)
   - Select environments: **Production**, **Preview**, **Development**
   - Click **Save**

### Via Vercel CLI:

```bash
# Install Vercel CLI
npm i -g vercel

# Login to Vercel
vercel login

# Add environment variable
vercel env add NODE_OPTIONS
# Then enter: --openssl-legacy-provider

# Redeploy with new environment variables
vercel --prod
```

---

## 🐛 Common Issues

### ❌ "digital envelope routines::unsupported" Error

**Solution:** Add `NODE_OPTIONS=--openssl-legacy-provider` to environment variables

### ❌ Firebase not connecting

**Solution:** Verify all Firebase environment variables are added correctly in Vercel

### ❌ Build succeeds locally but fails on Vercel

**Solution:** Ensure all environment variables from `.env` are added to Vercel

---

## 📝 Environment Variables Checklist

Make sure you've added ALL these to Vercel:

- [x] `NODE_OPTIONS`
- [x] `VUE_APP_FIREBASE_API_KEY`
- [x] `VUE_APP_FIREBASE_AUTH_DOMAIN`
- [x] `VUE_APP_FIREBASE_PROJECT_ID`
- [x] `VUE_APP_FIREBASE_STORAGE_BUCKET`
- [x] `VUE_APP_FIREBASE_MESSAGING_SENDER_ID`
- [x] `VUE_APP_FIREBASE_APP_ID`

---

## 🔄 Redeploying After Adding Variables

After adding environment variables:

1. Go to **Deployments** tab
2. Click **⋯** (three dots) on the latest deployment
3. Click **Redeploy**
4. Check **"Use existing Build Cache"** ❌ (uncheck to rebuild fresh)
5. Click **Redeploy**

---

## 🎉 Success!

Your app should now be live at: `https://your-project-name.vercel.app`
