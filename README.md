# 🎮 Emoji & Color Matching Game

An interactive matching game with two modes: Emoji Mode and Color Mode! Features explosions, stardust, and dynamic backgrounds!

## 🎨 Game Modes

### 😀 Emoji Mode (Default)

- Match pairs of identical emojis
- 12 different emoji pairs to match
- Each emoji has custom celebration messages

### 🎨 Color Mode

- Match color blocks with their corresponding color name labels
- 10 colors: Red, Orange, Yellow, Green, Blue, Purple, Pink, Brown, Gray, Black
- Same explosive effects and celebration messages
- Color blocks and labels stay perfectly horizontal (no rotation) for clean, easy reading

**Switch between modes** using the hamburger menu in the top-right corner!

## ✨ Features

### 🍔 Hamburger Menu

All game controls are now tucked away in a beautiful, sliding hamburger menu! No more UI clutter - just pure gameplay.

**What's in the menu:**

- **Game Modes**: Switch between Emoji and Color modes with full explanations
- **New Game**: Start fresh with one click
- **Audio Settings**: Toggle sound effects and voice announcements
- **How to Play**: Quick instructions right when you need them

Each menu item includes a detailed description of what it does - perfect for new players!

### 🎯 Matching Game

- **Click/Tap** an element to select it (it will pulse with a glow)
- **Click/Tap** its matching pair to make them both explode and disappear
- Match all pairs to win and see victory confetti! 🎉
- Wrong match? Both elements will shake and you'll hear a subtle error sound

### 🎨 Interactive Effects

- **Double-click anywhere** on the screen for a colorful explosion with pulsing rings
- **Right-click** (or long-press on mobile) for wild color background animations
- **Drag emojis** to reposition them manually - they're all draggable!

### 💫 Visual Magic

- Sparkling stardust lingers after every explosion (lasts 35-45 seconds)
- Pulsing explosion rings with random colors
- Screen flickers and particle effects
- Continuous shimmer on the background
- Random positioning on each page load
- Victory confetti celebration when you complete the game

### 🔊 Sound Effects & Music

- **Select sound**: Soft click when selecting an emoji
- **Match sound**: Satisfying "pop" when you find a pair
- **Error sound**: Quick sawtooth buzz for wrong matches
- **Explosion sound**: Soft whoosh for matched pairs
- **Victory fanfare**: Triumphant celebration when you win
- **Background sound**: Ambient tone for color explosions
- **Victory songs**: Separate MP3 songs play for Emoji Mode and Color Mode victories! 🎵
  - `victory-song.mp3` plays when you win in Emoji Mode
  - `victory-song-color.mp3` plays when you win in Color Mode
- **Toggle in menu**: Enable/disable sounds and voice in the hamburger menu

### 🎮 Game Controls (All in Hamburger Menu!)

Click the hamburger button (☰) in the top-right corner to access:

- **🎨/😀 Mode Toggle**: Switch between Emoji Mode and Color Mode (saved to browser storage)
- **🔄 New Game**: Resets the game, brings back all elements, and randomizes positions
- **🔊 Sound**: Toggle sound effects on/off (saved to browser storage)
- **🗣️ Voice**: Toggle voice announcements on/off (saved to browser storage)
- **❓ How to Play**: Quick instructions and tips

Each control has a full explanation in the menu so you always know what it does!

## 🛠️ How to Add More Emoji Pairs

It's super easy! Just add pairs to `index.html`:

```html
<h1 data-match-id="star">⭐</h1>
<h1 data-match-id="star">⭐</h1>

<h1 data-match-id="alien">👽</h1>
<h1 data-match-id="alien">👽</h1>
```

**Rules:**

1. Each pair needs **two** `<h1>` tags with the **same emoji**
2. Give them the **same** `data-match-id` (can be anything unique)
3. The game automatically detects and handles all pairs - no code changes needed!

## 🎨 Customizing Color Mode

To add or modify colors in Color Mode, edit the `colorDefinitions` and `colorMatchMessages` objects in `script.js`:

```javascript
// Add a new color
this.colorDefinitions = {
  red: "#E53935",
  // ... other colors
  turquoise: "#1ABC9C", // New color!
};

// Add custom messages for the new color
this.colorMatchMessages = {
  red: ["Red Hot Match!", "Seeing Red... Success!"],
  // ... other colors
  turquoise: ["Tropical Match!", "Teal Victory!"], // New messages!
};
```

The game will automatically create color blocks and labels for all colors in `colorDefinitions`!

## 🎵 Adding Victory Songs

The game supports separate victory songs for each mode!

**Currently configured:**

- `victory-song.mp3` - Plays when you win in Emoji Mode ✅ (you already have this!)
- `victory-song-color.mp3` - Plays when you win in Color Mode ⚠️ (add this file!)

**To add the Color Mode victory song:**

1. Find or create an MP3 file you want to use for Color Mode victories
2. Name it `victory-song-color.mp3`
3. Place it in the same directory as `index.html`
4. Done! The game will automatically play it when you win in Color Mode

**Tips:**

- Keep songs under 30 seconds for best experience
- Volume is set to 60% by default (adjustable in `script.js`)
- Songs work on all devices (iOS requires user interaction first)
- If a song file is missing, the game gracefully continues without it

You can also customize the file paths in `script.js` (search for `initVictorySongs()`).

## 📱 Device Compatibility & Responsive Design

### 🖥️ Desktop

- Works on all modern browsers (Chrome, Safari, Firefox, Edge)
- Full-size emojis (6rem) and color blocks (120px)
- Smooth animations and effects

### 📱 iPad / Tablets (768px - 1024px)

- **60% scaling** (between 1/2 and 2/3 size)
- Emojis: 3.6rem
- Color blocks: 72px
- Optimized touch targets and spacing

### 📱 iPhone / Small Screens (< 768px)

- **30% scaling** (between 1/4 and 1/3 size)
- Emojis: 1.8rem
- Color blocks: 36px
- Compact menu and controls
- Maximum screen space for gameplay

### ✨ iOS Optimizations

- Touch-optimized for smooth tapping and dragging
- iOS audio unlocking for sound effects and victory songs
- Prevents text selection and iOS callout menus
- Hardware-accelerated animations
- Backdrop blur effects on the menu

## 🎨 Customization

All styles are in `style.css`:

- Change emoji sizes, colors, animations
- Modify explosion effects, sparkles, confetti
- Adjust background shimmer and color palettes
- Customize button styles and positioning

All game logic is in `script.js`:

- Sound synthesis using Web Audio API
- Match messages and victory messages arrays
- Animation timings and durations
- Color palettes for explosions

## 🚀 Quick Start

1. Open `index.html` in a browser
2. Click emojis to match pairs
3. Double-click for explosions
4. Drag emojis to reposition
5. Have fun! 🎉

## 💾 Technical Details

- **Pure JavaScript** - no external libraries
- **Web Audio API** - synthesized sounds (no audio files needed)
- **CSS Animations** - hardware-accelerated effects
- **LocalStorage** - saves sound preferences
- **Responsive Design** - works on any screen size

---

**Enjoy the game!** 🌟
