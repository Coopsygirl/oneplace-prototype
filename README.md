## One Place — Complete Working Prototype

A **calm, visual schedule + wellbeing app** for kids and parents. Kids see only what they need to know. Parents control the information and message kids instantly.

### ✅ What's Working Now

**PARENT SIDE** (`parent-login.html` → `parent-dashboard.html`)
- ✅ Login (demo mode, no password)
- ✅ Add activities/events with simple, child-friendly descriptions
- ✅ See messages from child (feelings + what they said)
- ✅ Reply instantly to child's messages
- ✅ Delete events

**CHILD SIDE** (`index.html`)
- ✅ See calm, simple schedule (what parent added)
- ✅ Micro-checklist (brush teeth, get dressed, etc.)
- ✅ Next transport countdown
- ✅ Send feelings & messages via "How Are You Feeling?" (`helpme.html`)
- ✅ See parent replies instantly
- ✅ Installable as PWA on phone (iOS/Android)

**INSTANT MESSAGING FLOW**
1. Child: "I'm feeling 😰 worried" → sends to parent
2. Parent sees it in dashboard → clicks "Reply Now"
3. Parent: "You're safe with mum" → sends to child
4. Child sees reply appear on their Today screen in real-time

---

### 🚀 Quick Start

**Option A: Simple (no server)**
- Just double-click `index.html` in file explorer

**Option B: Better (for PWA testing on phone)**
```bash
cd oneplace-prototype
python3 -m http.server 8000
# Then open: http://localhost:8000
```

### 📱 Test on Your Phone

**iPhone (Safari):**
1. Open `http://<your-computer-ip>:8000`
2. Tap Share → Add to Home Screen
3. Opens as standalone app

**Android (Chrome):**
1. Open same URL
2. Tap Menu → Install app
3. Works as installed app

---

### 🧪 How to Test the Full Flow

1. **Open two browser windows/tabs**
   - Tab 1: `http://localhost:8000/parent-login.html` (parent)
   - Tab 2: `http://localhost:8000/index.html` (child)

2. **Parent side:**
   - Enter email + child's name → logs in
   - Clicks "+Add Event" → adds "School pickup at 3pm"
   - Event syncs to child instantly

3. **Child side:**
   - Sees the event in "Later"
   - Clicks "How Are You Feeling?"
   - Picks feeling (😰 worried) + optional message
   - Sends to parent

4. **Parent sees the message:**
   - Dashboard updates with child's feeling
   - Clicks "Reply Now" → sends calm response
   - Child sees reply instantly on Today screen

---

## 📁 File Guide

| File | Purpose |
|------|----------|
| `index.html` | Child's "Today" screen (main view) |
| `helpme.html` | Child sends feelings & messages |
| `parent-login.html` | Parent sign-in (demo mode) |
| `parent-dashboard.html` | Parent adds events, replies to messages |
| `myweek.html` | Weekly view (not fully connected yet) |
| `travel.html` | Bus/transport screen (placeholder) |
| `styles.css` | All shared styling |
| `manifest.json` | PWA config (makes it installable) |
| `SPEC.md` | Full product spec & roadmap |

---

## ⚠️ What This Is NOT (Yet)

This is a **local prototype** - everything saves in your browser's localStorage:
- ❌ No real database (data only in browser)
- ❌ No notifications (yet)
- ❌ No real login/passwords (demo mode only)
- ❌ No backend sync across devices

---

## 🎯 Next Phase: Make It Real

To turn this into a **real app**:

### Option A: Firebase + Web (Easiest, 3-4 weeks)
- Real login + cloud database
- Events & messages sync in real-time
- Push notifications to parents
- Deploy to web (Vercel/Netlify)
- **→ Works on any device, no app store needed**

### Option B: React Native (Mobile app, 6-8 weeks)
- Installable from App Store / Google Play
- Offline support
- Better native feel
- **→ Polished, premium feel**

**I recommend Option A** (web first, then mobile wrapper if needed)

---

## ❓ FAQ

**Q: How do I change colors?**  
A: Edit `styles.css` - search for `#ff69b4` (pink) and `#ffd8e6` (light pink)

**Q: Can multiple parents/kids use this?**  
A: Currently just one pair per browser. Real app will have full multi-user support.

**Q: Will messages really be instant?**  
A: In this version, yes (same browser). Real app needs Firebase/backend for cross-device.

**Q: Can I make this into an actual app?**  
A: Yes! PWA works now on iOS/Android. For App Store, you'd need React Native.

---

## 🎬 What To Do Now

1. **Test it** — Open the files, try the parent→child flow
2. **Get feedback** — Show a real parent & child, ask what works/doesn't
3. **Decide next step** — Firebase backend or polish design first?

**You're not useless.** You built the vision. Now let's make it real. 🚀