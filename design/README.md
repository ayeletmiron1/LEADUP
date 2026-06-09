# LEADUP Design Files

## Overview

זו תיקייה המכילה את קבצי העיצוב המלאים של אפליקציית LEADUP, כולל פרוטוטייפ, קומפוננטות ו-screenshots.

## 📁 מבנה התיקייה

```
design/
├── components/
│   └── ios-frame.jsx          # קומפוננטת מסגרת האייפון (iOS 26 Liquid Glass)
├── prototype/
│   └── leadup.html            # הפרוטוטייפ המלא עם כל הלוגיקה, עיצוב ואנימציות
├── screenshots/
│   ├── check.png              # Screenshots מבדיקות (1)
│   ├── check2.png             # Screenshots מבדיקות (2)
│   ├── check3.png             # Screenshots מבדיקות (3)
│   └── check4.png             # Screenshots מבדיקות (4)
└── README.md                  # קובץ זה
```

## 🎨 iOS Frame Component

### קבצים:
- **`components/ios-frame.jsx`** - קומפוננטת React עם:
  - Status bar מלא (זמן, WiFi, סBattery)
  - Dynamic Island
  - Navigation bar עם Liquid Glass Pills
  - Home Indicator
  - iOS Keyboard עם autocorrect bar
  - תמיכה ב-Dark Mode

### תכונות:
- **Liquid Glass Design** - Blur + Tint + Shine Effect
- **iOS 26 UI Kit** - תאום ל-Figma status bar spec
- **No Dependencies** - Pure React, No Assets
- **Fully Responsive** - Props: `width`, `height`, `dark`, `title`, `keyboard`

### שימוש:

```jsx
import { IOSDevice } from './components/ios-frame';

function App() {
  return (
    <IOSDevice title="Settings" dark keyboard>
      {/* Your screen content here */}
    </IOSDevice>
  );
}
```

## 🎬 Prototype

**File:** `prototype/leadup.html`

פרוטוטייפ מלא של האפליקציה עם:
- כל הלוגיקה של האפליקציה
- עיצוב מלא (CSS)
- אנימציות
- Interactivity

### פתיחה:
1. הורד את `leadup.html`
2. פתח בדפדפן (Chrome, Safari, Firefox)
3. הפרוטוטייפ מוכן לשימוש מיידי

## 📸 Screenshots

Testing screenshots שנוצרו בזמן פיתוח:
- `screenshots/check.png` - בדיקה 1
- `screenshots/check2.png` - בדיקה 2
- `screenshots/check3.png` - בדיקה 3
- `screenshots/check4.png` - בדיקה 4

## 🔗 חיבור ל-base44

כדי להשתמש בקבצים אלה ב-base44:

1. **העלה את הקבצים:**
   ```bash
   git clone https://github.com/ayeletmiron1/LEADUP.git
   cd LEADUP/design
   ```

2. **Import ל-base44:**
   - פתח base44
   - בחר `Import Project` או `Upload Files`
   - בחר את התיקיה `design/` או קבצים בודדים
   - ה-JSX יוכל להיות בשימוש כקומפוננטה
   - ה-HTML יוכל להיות בדיקה ישירה

3. **שימוש בקומפוננטה:**
   - העתק את `ios-frame.jsx` ל-base44
   - ייבא וך השתמש ב-`<IOSDevice />` ו-exported components

## 📋 Component Props

### `<IOSDevice />`

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `children` | ReactNode | - | תוכן המסך |
| `width` | number | 402 | רוחב ה-device |
| `height` | number | 874 | גובה ה-device |
| `dark` | boolean | false | Dark Mode |
| `title` | string | - | כותרת Navigation Bar |
| `keyboard` | boolean | false | הצג Keyboard |

### Exported Components:

```javascript
window.IOSDevice        // Main device frame
window.IOSStatusBar     // Status bar component
window.IOSNavBar        // Navigation bar
window.IOSGlassPill     // Liquid glass pill button
window.IOSList          // Grouped list
window.IOSListRow       // List row item
window.IOSKeyboard      // iOS keyboard
```

## 🎨 Color System

**Light Mode:**
- Text: `#000`
- Secondary: `rgba(60,60,67,0.6)`
- Separators: `rgba(60,60,67,0.12)`
- Background: `#F2F2F7`

**Dark Mode:**
- Text: `#fff`
- Secondary: `rgba(235,235,245,0.6)`
- Separators: `rgba(84,84,88,0.65)`
- Background: `#000`

## 📝 הערות

- כל הקומפוננטות ב-JSX משתמשות ב-Inline Styles (אין CSS files)
- ה-HTML פרוטוטייפ עצמאי לחלוטין - אין תלויות חיצוניות
- ה-Design עקבי עם iOS 26 UI Guidelines
- תמיכה מלאה ב-React 16.8+ (Hooks)

## 🚀 השלם

קבצים אלה מוכנים לשימוש מיידי ב-base44!

---

**Created:** 2026-06-09  
**Repository:** [ayeletmiron1/LEADUP](https://github.com/ayeletmiron1/LEADUP)
