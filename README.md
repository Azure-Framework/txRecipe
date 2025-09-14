# 📥 Azure‑Framework Full Suite txAdmin Recipe

Deploy a complete **Azure‑Framework** server stack using txAdmin in under 60 seconds!  
This recipe includes 📦 **oxmysql**, **ox_lib**, all Azure modules, OneSync, and a fully themed `server.cfg` with ASCII art and Discord link.

---

## 🧩 What’s Included

- **oxmysql** (v2.13.0) – MySQL integration  
- **ox_lib** (v3.30.6) – Shared libraries  
- **Azure‑Framework** core + modules:
  - Az‑Banking, Az‑Admin, Az‑Levels, Az‑PoliceMenu  
  - Az‑Jailing, Az‑CoffeeJob, Az‑DrugTraffic  
  - Az‑GarbageJob, Az‑LogJob, Az‑Amazon  
- **OneSync** enabled  
- **Themed server.cfg** with ASCII header & Discord banner

---

## 🚀 Requirements

- txAdmin (bundled with FXServer ≥ 2524)  
- MySQL server (local or remote) — recipe will auto-import schema  
- Discord server (optional, for community link)

---

## 🛠️ Setup Instructions

1. Copy the recipe YAML (e.g. `azure-main.ymal`).  
2. Paste into txAdmin’s **Custom Template** field.  
3. Provide your MySQL credentials when prompted.  
4. Proceed to **Run Recipe** – txAdmin handles downloading files, importing DB schema, and generating `server.cfg`.  
5. Start your server – you'll see the ASCII banner and Discord link on connect.

---

## 📝 What the Recipe Does

- Downloads & extracts **oxmysql** and **ox_lib** first.  
- Fetches Azure framework and modules into `resources/[framework]/...`.  
- **Automatically imports** the MySQL schema into your database—no manual `.sql` handling needed.  
- Generates a `server.cfg` featuring:
  - ASCII‑art header
  - Network & license setup
  - Admin permissions linked to txAdmin
  - Proper startup order
  - `sv_banner` with your Discord link

---

## 🎯 Customization Tips

- Update `ref:` tags to lock resource versions.  
- Adjust ASCII art or `sv_banner` as you like.  
- Add more GitHub resources and `start` lines for extra modules.  
- For complex setups, insert advanced DB logic before the `database:` section.

---

## 📘 Troubleshooting

- If schema import fails, confirm MySQL credentials and access rights.  
- Modules not starting? Double-check module names in recipes and `server.cfg`.  
- Banner not showing? Verify the Discord invite and server output for clues.

---

## 💬 Get Support

Need help or want to chat?  
**Join Discord:** https://discord.gg/tBg2U6CTHE

---

## ✅ License

Apache‑2.0 (or MIT/GPL‑compatible) — ensure all Azure modules remain open-source.

---

Thanks for using this recipe—here's to powerful, auto-deploying Azure‑Framework servers! 🎉
