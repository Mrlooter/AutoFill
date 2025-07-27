Here’s a `README.md` for your GitHub repository to explain how to use your Tampermonkey autofill script with a hamburger menu interface:

---

# 🧾 Autofill Script - StateTax Menu Version

Tampermonkey script designed for automating repetitive form interactions on the [Innodata LDU Dashboard](https://staging02.innodata.com/ldu-dashboard/).
This version includes a scalable hamburger-style menu that lets you trigger multiple autofill workflows easily.

## 🚀 Features

* 💡 Hamburger menu UI injected into the page
* 🧠 Multiple autofill workflows:

  * State Tax Registration
  * State Tax Renewal
  * License Upload (example function for extensibility)
* 🔁 Smooth keypress emulation with delay
* 📦 Fully self-contained – no dependencies required

---

## 🛠 Installation

1. **Install Tampermonkey**
   Make sure Tampermonkey is installed in your browser:

   * [Chrome Extension](https://chrome.google.com/webstore/detail/dhdgffkkebhmkfjojejmpbldmpobfkfo)
   * [Firefox Add-on](https://addons.mozilla.org/firefox/addon/tampermonkey/)

2. **Create New Script**

   * Open the Tampermonkey dashboard.
   * Click `➕ Create a new script`.
   * Replace the default code with the content from [`autofill-state-tax-menu.user.js`](./autofill-state-tax-menu.user.js).
   * Save it (Ctrl + S).

---

## 🧭 How to Use

1. Go to the site: `https://staging02.innodata.com/ldu-dashboard/`
2. A hamburger icon ☰ will appear in the bottom-right corner.
3. Click the icon to reveal the menu options:

   * ▶ **Run State Tax Registration**
   * 🔁 **Run State Tax Renewal**
   * 📄 **Run License Upload**
4. Click any of the options to run its associated steps. The script will automatically simulate `TAB`, `UP`, `DOWN`, and `ENTER` keypresses to fill in the form.

---

## ⚙️ Customization

You can define additional workflows by adding a new step list and referencing it in the menu:

```js
const myCustomSteps = [
  { action: 'tab', count: 3 },
  { action: 'down', count: 1 },
  { action: 'enter', count: 1 },
];

function runMyCustomSteps() {
  runSteps(myCustomSteps);
}
```

Then add it to the `actions` array:

```js
{ label: 'Run My Custom Steps', handler: runMyCustomSteps }
```

---

## 📄 License

This project is licensed under the MIT License – feel free to use, modify, or extend.

---

## 🙋 Support

If you encounter issues or have suggestions, feel free to open an [Issue](https://github.com/your-username/your-repo-name/issues) or submit a Pull Request.

---

Let me know if you’d like a `LICENSE` file or a ready-to-commit repo structure too.
