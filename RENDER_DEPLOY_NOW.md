# 🚀 Automiles - Render Deployment Instructions

## ✅ Code Status
- ✅ Repository: https://github.com/Vedanth-Rach/Automiles
- ✅ Branch: main
- ✅ Code pushed successfully
- ✅ Ready to deploy!

---

## 🎯 DEPLOY NOW - Three Options

### Option 1: Blueprint Deploy (BOTH SERVICES AT ONCE) ⭐ RECOMMENDED

**The Render Blueprint page is now open in your VS Code browser.**

**Steps:**
1. On the Render page, click **"Connect Repository"**
2. Find and select: **Vedanth-Rach/Automiles**
3. Click **"Connect"**
4. Render will detect your `render.yaml` file
5. You'll see TWO services:
   - `autimilezzz-backend` (Web Service)
   - `autimilezzz-frontend` (Static Site)
6. Add environment variable for backend:
   - **Key:** `MONGODB_URI`
   - **Value:** `mongodb+srv://vedhurach_db_user:<sT3xLKaMjWGat0F5>@cluster0.1enhqme.mongodb.net/?appName=Cluster0`
7. Click **"Apply"** to deploy both services
8. Wait 5-10 minutes

**Blueprint Link:** https://dashboard.render.com/select-repo?type=blueprint

---

### Option 2: Deploy Backend First, Then Frontend

#### Step A: Deploy Backend (Web Service)

**Link:** https://dashboard.render.com/create?type=web

**Configuration:**
```
Repository:       Vedanth-Rach/Automiles
Name:             autimilezzz-backend
Root Directory:   backend
Environment:      Node
Build Command:    npm install
Start Command:    npm start
Branch:           main

Environment Variables:
  MONGODB_URI: mongodb+srv://vedhurach_db_user:<sT3xLKaMjWGat0F5>@cluster0.1enhqme.mongodb.net/?appName=Cluster0
```

#### Step B: Deploy Frontend (Static Site)

**Link:** https://dashboard.render.com/create?type=static

**Configuration:**
```
Repository:       Vedanth-Rach/Automiles
Name:             autimilezzz-frontend
Root Directory:   frontend
Build Command:    (leave empty)
Publish Directory: .
Branch:           main
```

---

### Option 3: Use Render Dashboard Directly

1. Go to: https://dashboard.render.com/
2. Click **"New +"** button
3. Select **"Blueprint"**
4. Choose your **Automiles** repository
5. Follow the prompts

---

## 📊 Your Deployment URLs (After Deployment)

Once deployed, your services will be available at:

**Backend API:**
```
https://autimilezzz-backend.onrender.com
```

Test it:
```
https://autimilezzz-backend.onrender.com/api/posts
```

**Frontend Website:**
```
https://autimilezzz-frontend.onrender.com
```

---

## 🔐 Important: MongoDB Connection

**Don't forget to add this environment variable in Render:**

```
Key:   MONGODB_URI
Value: mongodb+srv://vedhurach_db_user:<sT3xLKaMjWGat0F5>@cluster0.1enhqme.mongodb.net/?appName=Cluster0
```

⚠️ **Without this, your backend will not start!**

---

## 📋 Deployment Checklist

- [✅] Code pushed to GitHub
- [ ] Opened Render Blueprint page (already open in VS Code)
- [ ] Selected Automiles repository
- [ ] Added MONGODB_URI environment variable
- [ ] Clicked "Apply" to deploy
- [ ] Waited for deployment (5-10 minutes)
- [ ] Got deployment URLs
- [ ] Tested backend endpoint
- [ ] Opened frontend in browser

---

## 🧪 Test Your Deployment

After deployment completes, run this command:

```powershell
.\test-deployment.ps1
```

Or test manually:

```powershell
# Test backend
curl https://autimilezzz-backend.onrender.com/

# Test frontend (opens in browser)
start https://autimilezzz-frontend.onrender.com
```

---

## 🎬 What Happens During Deployment

### Backend (5-8 minutes)
1. ✓ Render clones your repository
2. ✓ Navigates to `backend/` directory
3. ✓ Runs `npm install`
4. ✓ Starts server with `npm start`
5. ✓ Assigns URL: https://autimilezzz-backend.onrender.com

### Frontend (2-5 minutes)
1. ✓ Render clones your repository
2. ✓ Navigates to `frontend/` directory
3. ✓ Serves static files from root (`.`)
4. ✓ Assigns URL: https://autimilezzz-frontend.onrender.com

---

## ⚠️ Free Tier Notes

- **Backend:** Spins down after 15 minutes of inactivity
- **First request after spin-down:** 30-50 seconds (cold start)
- **Frontend:** Always available (static site)
- **This is normal behavior for Render's free tier**

---

## 🔄 Auto-Deployment Enabled

Once connected, every push to GitHub will automatically deploy to Render!

```powershell
# Make changes, then:
git add .
git commit -m "Your update message"
git push

# Render automatically redeploys in 2-10 minutes
```

---

## 🆘 Troubleshooting

### Backend fails to start
- ✓ Check MONGODB_URI is added in Render
- ✓ Check Render logs for errors
- ✓ Verify MongoDB Atlas allows 0.0.0.0/0

### Frontend shows 404
- ✓ Verify Publish Directory is `.` (dot)
- ✓ Check `index.html` exists in frontend folder
- ✓ Clear browser cache

### Can't find repository
- ✓ Make sure Render is connected to your GitHub
- ✓ Repository must be accessible
- ✓ Refresh the repository list

---

## 📞 Quick Links

| Resource | URL |
|----------|-----|
| **Render Dashboard** | https://dashboard.render.com/ |
| **Your GitHub Repo** | https://github.com/Vedanth-Rach/Automiles |
| **MongoDB Atlas** | https://cloud.mongodb.com/ |
| **Render Docs** | https://render.com/docs |
| **Blueprint Deploy** | https://dashboard.render.com/select-repo?type=blueprint |

---

## 🎉 Ready to Deploy!

**The Render page is open in VS Code. Follow the steps above to deploy both services!**

---

**Current Status:** ✅ Ready to deploy
**Next Step:** Select your Automiles repository in the Render page
**Time Required:** ~10 minutes total

---

*Generated: October 24, 2025*
*Repository: Vedanth-Rach/Automiles*
*Branch: main*
