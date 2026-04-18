# 📚 शास्त्री पोर्टल v4 — Complete Setup Guide

---

## 🗂️ File Structure (सबै files)

```
shastri-v4/
│
├── index.html                    ← मुख्य website (एउटै HTML)
├── manifest.json                 ← PWA support
│
├── css/
│   └── style.css                 ← सम्पूर्ण design (7 themes, fonts, animations)
│
├── js/
│   └── main.js                   ← सम्पूर्ण features (search, notes, history...)
│
├── data/
│   ├── books.json                ← ★ किताब र समाचारको data
│   └── chapters/
│       ├── nep1_1.json           ← नेपाली साहित्य १ (प्रथम वर्ष)
│       ├── nep1_2.json           ← नेपाली साहित्य २
│       ├── san1_1.json           ← संस्कृत साहित्य १
│       ├── ... (52 files total)
│       └── HOW_TO.md             ← अध्याय थप्ने guide
│
└── images/
    ├── year1/                    ← प्रथम वर्षका cover photos
    ├── year2/                    ← द्वितीय वर्षका cover photos
    ├── year3/                    ← तृतीय वर्षका cover photos
    ├── year4/                    ← चतुर्थ वर्षका cover photos
    └── news/                     ← समाचारका photos
```

---

## 🚀 GitHub मा राख्ने — Step by Step

### Step 1: GitHub Account बनाउनुस् (पहिलो पटक मात्र)
1. **https://github.com** खोल्नुस्
2. माथि दायाँमा **"Sign up"** थिच्नुस्
3. Email, Username, Password राखेर account बनाउनुस्
4. Email verify गर्नुस्

---

### Step 2: New Repository बनाउनुस्
1. Login गरेपछि माथि दायाँमा **"+"** icon → **"New repository"**
2. Repository name: **`shastri-portal`**
3. Description: `शास्त्री कक्षा पोर्टल` (ऐच्छिक)
4. **"Public"** select गर्नुस् ✅
5. **"Add a README file"** check गर्नुस् ✅
6. **"Create repository"** थिच्नुस्

---

### Step 3: Files Upload गर्नुस् (Drag & Drop — सबैभन्दा सजिलो)
1. आफ्नो repository page खोल्नुस्
2. **"Add file"** button → **"Upload files"** थिच्नुस्
3. ZIP extract गरेको **`shastri-v4`** folder खोल्नुस्
4. **सबै files र folders** select गरेर GitHub मा drag गर्नुस्
   > ⚠️ `data/`, `css/`, `js/`, `images/` folders सहित सबै
5. तल **"Commit changes"** → **"Commit directly to the main branch"** → **"Commit changes"**

---

### Step 4: GitHub Pages Enable गर्नुस्
1. Repository मा माथि **"Settings"** tab थिच्नुस्
2. बायाँतर्फ **"Pages"** मा click गर्नुस्
3. **"Source"** → **"Deploy from a branch"** select
4. **Branch:** `main` | **Folder:** `/ (root)` → **"Save"**
5. ३–५ मिनेट पर्खनुस्

---

### Step 5: Website हेर्नुस् 🎉
```
https://YourUsername.github.io/shastri-portal/
```
> `YourUsername` को ठाउँमा आफ्नो GitHub username राख्नुस्

---

## ✏️ किताबको नाम र लेखक थप्ने

`data/books.json` खोल्नुस् र placeholder भर्नुस्:

```json
{
  "id": "nep1_1",
  "title": "नेपाली साहित्य — मेरो पाठ्यपुस्तक",
  "author": "डा. रामप्रसाद शर्मा",
  "description": "प्रथम वर्षको नेपाली साहित्यको पाठ्यपुस्तक"
}
```

**GitHub मा directly edit गर्न:**
1. Repository → `data/books.json` → ✏️ (pencil icon)
2. Edit → "Commit changes"

---

## 📖 अध्याय Content थप्ने

`data/chapters/nep1_1.json` खोल्नुस्:

```json
{
  "chapters": [
    {
      "id": 1,
      "title": "अध्याय १ — आमाको सन्सार",
      "content": "# आमाको सन्सार\n\nआमा नेपालको संसार हुन्।\n\n## परिचय\n\n**आमा** भनेको जीवनको आधार हो।\n\n- मायाको स्रोत\n- शक्तिको केन्द्र\n- परिवारको मूल"
    }
  ]
}
```

### Markdown Shortcuts:
| लेख्नुस् | Result |
|---------|--------|
| `# शीर्षक` | ठूलो heading (पहेंलो) |
| `## शीर्षक` | Medium heading |
| `**text**` | **Bold** |
| `*text*` | *Italic* |
| `- item` | Bullet list |
| `> text` | Quote box |
| `==text==` | Highlight |
| `![alt](url)` | Photo embed |

---

## 📰 समाचार थप्ने (Photo सहित)

`data/books.json` मा `"news"` array मा:

```json
{
  "id": 6,
  "title": "नयाँ परीक्षा तालिका",
  "content": "२०८१ सालको शास्त्री परीक्षाको तालिका प्रकाशित।",
  "date": "२०८१-०३-०१",
  "category": "परीक्षा",
  "image": "images/news/exam.jpg"
}
```

**Photo थप्न:** `images/news/exam.jpg` नाम राखेर upload गर्नुस्।
Photo नभए `"image": ""` छोड्नुस्।

**Categories:** `परीक्षा` | `पाठ्यक्रम` | `छात्रवृत्ति` | `कार्यक्रम` | `कार्यशाला`

---

## 🖼️ Book Cover Photo थप्ने

1. Photo को नाम: `nep1.jpg`, `eng2.jpg`, `san3.jpg` आदि
2. Folder: `images/year1/` (वर्ष अनुसार)
3. `books.json` मा: `"cover": "images/year1/nep1.jpg"`

**Photo size:** 400×300px, JPEG format राम्रो हुन्छ।

---

## 🔧 Features Quick Guide

| Feature | कहाँ |
|---------|------|
| Night Mode | ⋮ (3-dots) → 🌙 रात्रि मोड |
| 7 Themes | ⋮ (3-dots) → 🎨 Theme छान्नुस् |
| Font Change | ⋮ (3-dots) → 🔤 Font छान्नुस् |
| News Animation | ⋮ (3-dots) → 📰 Animation |
| Font Size | ⋮ (3-dots) → Slider |
| Bookmark | किताब खोल्दा 🏷️ icon |
| Notes | 📝 tab वा bottom nav |
| Backup | ⚙️ Settings → Export |

---

## ❓ Common Problems

**Website देखिएन?**
→ Settings → Pages मा "Your site is published at..." देखिनु पर्छ। ५ मिनेट पर्खनुस्।

**Chapters देखिएनन्?**
→ `data/chapters/` folder properly upload भयो कि? JSON syntax सही छ?

**Photo देखिएन?**
→ File path exactly मिल्नु पर्छ। `images/year1/nep1.jpg` ≠ `Images/Year1/Nep1.jpg`

**Night mode काम गरेन?**
→ Browser cache clear गर्नुस् (Ctrl+Shift+R)

---

## 📱 Phone मा Home Screen मा Add गर्न

**iOS (iPhone/iPad):**
1. Safari मा website खोल्नुस्
2. Share button → "Add to Home Screen"
3. "Add" थिच्नुस्

**Android:**
1. Chrome मा website खोल्नुस्
2. ⋮ menu → "Add to Home Screen"
3. "Add"

---

Made with ❤️ · शास्त्री पोर्टल v4
