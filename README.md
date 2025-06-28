# 📥 Azure‑Framework Full Suite txAdmin Recipe

Deploy a complete **Azure‑Framework** server stack using txAdmin in under 60 seconds!  
This recipe includes MySQL support via **oxmysql**, framework resources under `[framework]`, and a customized `server.cfg` featuring ASCII‑styled branding and your Discord link.

---

## 🧩 What’s Included

- **oxmysql** (v2.13.0) – MySQL integration  
- **ox_lib** (v3.30.6) – Shared utility library  
- **Azure‑Framework** core + modules:
  - Az‑Banking, Az‑Admin, Az‑Levels, Az‑PoliceMenu  
  - Az‑Jailing, Az‑CoffeeJob, Az‑DrugTraffic  
  - Az‑GarbageJob, Az‑LogJob, Az‑Amazon  
- **OneSync** enabled  
- **Themed server.cfg** with ASCII header & Discord banner

---

## 🚀 Requirements

- txAdmin (built-in with FXServer ≥ 2524)  
- MySQL server (local or remote) — the recipe auto-imports the schema  
- Discord server (optional but recommended)

---

## 🛠️ Setup Instructions

1. Clone or download this recipe (e.g., `azure-framework-recipe.yaml`).  
2. Ensure `schema.sql` is placed at:  
   resources/[framework]/Az-Framework/db/schema.sql  
3. In txAdmin, choose **Custom Template** and paste the recipe YAML.  
4. Enter your MySQL credentials during deployment (host/user/password/db).  
5. Review the generated `server.cfg`, then click **Run Recipe**.  
6. Launch your server and confirm the Azure banner + Discord link on connect.  
7. Enjoy your Azure‑Framework server 🎉

---

## 📝 What the Recipe Does

- Downloads and extracts **oxmysql** and **ox_lib** first—required by Azure modules.  
- Fetches Azure‑Framework core and modules into `resources/[framework]/…`.  
- Auto-imports the MySQL schema.  
- Generates a themed `server.cfg` with:  
  - ASCII header  
  - Network & license setup  
  - Admin permissions tied to txAdmin group  
  - Ordered resource startup  
  - In-game `sv_banner` with Discord link

---

## 🎯 Customization Tips

- Change the `ref:` values to target specific branches or commits.  
- Customize the ASCII header or the `sv_banner` message.  
- Add extra modules by including their `download_github` step and a `start` line in `server.cfg`.  
- For advanced setups, embed DB user creation or permission logic before the `database:` block.

---

## 📘 Troubleshooting

- **Schema not imported?**  
  Ensure `schema.sql` is present and the path is correct.

- **Modules not starting?**  
  Check console logs for missing dependencies or path typos.

- **Discord link not visible?**  
  Test the invite URL and ensure network settings allow server banners.

---

## 💬 Get Support

Questions, ideas, or want to chat with the community?  
**Join our Discord:** https://discord.gg/tBg2U6CTHE


---

Thanks for using this recipe! Let your server shine 😊
