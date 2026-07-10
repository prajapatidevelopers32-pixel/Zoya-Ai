# 📱 Zoya AI - APK & AAB Banane Ka Sabse Aasan Tarika (Cloud Build + Local Build) 🚀

Aapki request par humne ek **100% Automated Cloud Build** system set kar diya hai! Ab aapko apne computer par **Android Studio** ya **Java** install karne ki koi zaroorat nahi padegi agar aapke paas low-end PC hai.

Niche do (2) simple tarike diye gaye hain. Hum **Method 1** recommend karte hain kyunki ye sabse aasan hai!

---

## 🔥 Method 1: GitHub Cloud Build (Sabse Aasan, No Android Studio Needed!) ☁️
Is tarike me, GitHub ka high-speed server aapke liye automatically `.apk` aur `.aab` file generate kar ke dega. Aapko bas file download karni hogi!

### Step-by-Step Kaise Karein:
1. **Zip Download Karein:** AI Studio me top-right me settings menu se project ko **"Export to ZIP"** kar ke download karein aur extract kar lein.
2. **GitHub Par Upload Karein:**
   - [github.com](https://github.com) par jayein aur apna free account banayein (agar pehle se nahi hai).
   - Ek naya repository banayein (e.g., `zoya-ai-app`).
   - Apne computer ke un-zipped project files ko GitHub Repository par upload kar dein. *(Aap directly drag-and-drop upload bhi kar sakte hain GitHub website par!)*
3. **Magic Dekhein!**
   - Jaise hi aap code upload karenge, GitHub ke **"Actions"** tab me automatic build chalne lagegi.
   - Hamein pehle se hi `.github/workflows/build-apk.yml` file create kar di hai, isliye aapko kuch configure nahi karna padega!
4. **APK Download Karein:**
   - 3-5 minutes wait karein build complete hone ka.
   - GitHub Actions me build job par click karein.
   - Niche **Artifacts** section me aapko **`ZoyaAI-APK`** (phone me install karne ke liye) aur **`ZoyaAI-AAB`** (Play Store par dalne ke liye) download link mil jayega! 🥳

---

## 💻 Method 2: Android Studio Se Build Karein (Apne Computer Par) 🛠️
Agar aap apne computer par banana chahte hain:

### Pre-requisites (Chahiye):
1. **Node.js** (LTS)
2. **Android Studio**
3. **Java JDK 17**

### Step-by-Step:
1. **Project Open Karein:** Terminal/CMD me project folder kholiye aur dependencies install karein:
   ```bash
   npm install
   ```
2. **React Web Build & Copy:** Ye command run karein jo application ko build karke Android assets folder me daal degi:
   ```bash
   npm run build:android
   ```
3. **Android Studio Open Karein:**
   ```bash
   npm run cap:open
   ```
   *(Ya manual Android Studio me ja kar project ka `android/` folder open karein).*
4. **APK Compile Karein:**
   - Android Studio fully load hone ka wait karein.
   - Top menu me jayein: **Build** ➜ **Build Bundle(s) / APK(s)** ➜ **Build APK(s)**.
   - Success notification aane par **"Locate"** par click karein. Aapko aapki **`app-debug.apk`** mil jayegi!

---

## ⚠️ Play Store Launch (AAB) Ke Liye Tip:
Play Store par upload karne ke liye hamesha **AAB (Android App Bundle)** upload kijiye jo Method 1 me automatically ban jati hai release variant ke sath!

✨ **Zoya AI Voice and Image Generator is fully ready for APK build!**
