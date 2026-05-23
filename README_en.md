# [English] | [Русский](README.md)
---

# SCP:SL Keycard Generator (v14.1+)

<div align="center">
  <img src="Academic.png" alt="SCP Foundation Logo" width="120" height="120">
  <p><strong>SECURE ACCESS MANAGEMENT SYSTEM • FOUNDATION DATABASE</strong></p>
</div>

---

## 📋 Project Description

**SCP:SL Keycard Generator** is a lightweight web interface designed specifically for server administrators of **SCP: Secret Laboratory (v14.1 and above)**. This tool allows users to quickly and flawlessly generate the in-game `ckeycard` console commands required to create custom keycards.

The UI is styled in a sleek, futuristic Zone-02 terminal aesthetic (cyberpunk / SCP-inspired) featuring responsive layout design and interactive elements.

## ✨ Features

* 📦 **Fully Autonomous:** Built entirely on a clean tech stack (HTML5, CSS3, Vanilla JS) — no heavy frameworks or external dependencies required.
* 💳 **All Card Types Supported:** Generates the precise syntax for all four in-game templates: `Standard`, `Management`, `MTF Operative`, and `Metal Case`.
* 🎨 **Automatic Styling:** Upon selecting a card type, the system automatically applies default base HEX color codes for nodes, borders, and text labels, which can still be customized manually.
* 🔢 **Smart Input Fields:** 
    * Automatically generates a unique 10-digit military serial number for advanced clearance cards.
    * Dynamic parameter visibility (fields like serial number and circle count only appear when required by the selected template).
    * Player ID validation (strict numerical inputs, capped at 5 digits).
* 📋 **Quick Copy to Clipboard:** One-click button to copy the finalized command string instantly, complete with a built-in toast notification system.
* 🔒 **Data Privacy:** Fully cleared of data persistence (no local storage or session tracking), ensuring a completely clean slate upon every page reload.

---

## 🛠️ Tech Stack

* **Markup:** HTML5
* **Styling:** CSS3 (Custom Properties, CSS Grid, Flexbox, Backdrop-filter)
* **Fonts:** Rajdhani (Google Fonts)
* **Logic:** Pure JavaScript (ES6+)

---

## 🚀 How to Run

The generator is fully deployed and accessible directly within your web browser. There is no need to download or install anything:

👉 **[Launch the SCP:SL Keycard Generator](https://academic-as.github.io/SCP-SL-KEYCARD-GENERATOR/)**

---

## 📖 Usage & Syntax Logic

The interface compiles your input parameters directly into the official SCP:SL server command format.

### Command Structure Examples:
* **Standard Keycard:** `ckeycard [ID] KeycardCustomSite02 [Inventory_Name] [SCP] [Weapon] [Admin] [Circle_Color] [Border_Color] [Overlay_Label] [Label_Color] [Owner_Name] 1`
* **MTF Operative Keycard:** Formats a specialized command tail, binding the custom serial number and mapping the selected circle count into the game's inverted index parameters (e.g., choosing 3 circles on the UI translates into index `1` within the game syntax).

> ⚠️ **Important:** To ensure the game console reads the arguments correctly, all spaces entered in text fields (*Inventory Name, Overlay Label, Owner Name*) are automatically replaced with underscores (`_`) during command generation.
