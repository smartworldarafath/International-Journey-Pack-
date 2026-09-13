# International Journey Pack (Static Website)

This repository contains the static site **International Journey Pack** (single-page HTML). Use this repository to host the site on **GitHub Pages** or to version-control the project.

## Files included
- `index.html` — the full website (single file).
- `firebase-config.example.js` — example file you can edit to provide Firebase config before deploying.
- `README.md` — this file.
- `.gitignore` — common ignores.

## Quick setup (recommended)
1. Create a new GitHub repository (public) named e.g. `international-journey-pack`.
2. Clone locally:
```bash
git clone https://github.com/<your-username>/international-journey-pack.git
cd international-journey-pack
```

3. Copy the site files into the repo (or replace existing files).

4. **Firebase note** — the page expects a global `__firebase_config` string and `__app_id`. Before deploying, edit `firebase-config.example.js`, add your Firebase config values, then rename the file to `firebase-config.js`. The file must be included before the `<script type="module">` block in `index.html` (it's already prepared to read those globals).

`firebase-config.example.js` example contents (already included):
```js
// Rename to firebase-config.js and fill values
// __firebase_config must be a JSON string
// Example:
const __firebase_config = JSON.stringify({
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  // ...other firebase config fields
});
const __app_id = "your-app-id";
const __initial_auth_token = ""; // optional
```

5. Commit & push:
```bash
git add .
git commit -m "Initial site upload"
git push -u origin main
```

6. Enable GitHub Pages:
- Go to your repository on GitHub → Settings → Pages.
- Under "Build and deployment", choose **Branch: main** and folder **/ (root)**.
- Save. GitHub Pages will publish at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Quick development tips
- To preview locally, open `index.html` in a browser; for modules and some APIs it's best to run a simple static server:
```bash
# python 3
python -m http.server 8000
# then open http://localhost:8000
```

## Troubleshooting
- If icons or fonts fail to load, check your internet connection (they are loaded from public CDNs).
- If Firestore fails, ensure the Firebase config is correct and the Firestore rules allow the access pattern you use (or use authenticated credentials).


---

## ☕ Support / Buy Me a Coffee & Become a Sponsor

If you find **International Journey Pack** helpful and want to support ongoing development, maintenance, and new features, consider contributing through any of the options below! Your support means the world and helps keep this project open-source.

<div align="center">

<table>
  <tr>
    <td align="center" width="25%" valign="top">
      <h4>☕ SupportKori</h4>
      <a href="https://www.supportkori.com/arafathrahman" target="_blank">
        <img src="assets/supportkori-qr.jpg" alt="SupportKori QR" width="180" style="border-radius: 12px; box-shadow: 0 4px 15px rgba(0,0,0,0.15);" />
      </a><br/><br/>
      <a href="https://www.supportkori.com/arafathrahman" target="_blank">
        <img src="https://img.shields.io/badge/Support-SupportKori-FF5E5B?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white" alt="SupportKori Badge" />
      </a><br/>
      <sub>Cards / bKash / Nagad / Global</sub>
    </td>
    <td align="center" width="25%" valign="top">
      <h4>⚡ nsave</h4>
      <img src="assets/nsave-qr.jpg" alt="nsave QR" width="180" style="border-radius: 12px; box-shadow: 0 4px 15px rgba(0,0,0,0.15);" /><br/><br/>
      <img src="https://img.shields.io/badge/nsave-@arafath__rahman9-000000?style=for-the-badge&logoColor=white" alt="nsave Badge" /><br/>
      <sub>Ntag: <code>@arafath_rahman9</code></sub>
    </td>
    <td align="center" width="25%" valign="top">
      <h4>🔴 RedotPay</h4>
      <img src="assets/redotpay-qr.jpg" alt="RedotPay QR" width="180" style="border-radius: 12px; box-shadow: 0 4px 15px rgba(0,0,0,0.15);" /><br/><br/>
      <img src="https://img.shields.io/badge/RedotPay-1965421414-E51E2B?style=for-the-badge&logoColor=white" alt="RedotPay Badge" /><br/>
      <sub>ID: <code>1965421414</code></sub>
    </td>
    <td align="center" width="25%" valign="top">
      <h4>🅿️ Payoneer</h4>
      <img src="assets/payoneer-info.jpg" alt="Payoneer Info" width="180" style="border-radius: 12px; box-shadow: 0 4px 15px rgba(0,0,0,0.15);" /><br/><br/>
      <a href="mailto:arafathrahman710@gmail.com?subject=Support%20via%20Payoneer">
        <img src="https://img.shields.io/badge/Payoneer-70366820-FF4800?style=for-the-badge&logo=payoneer&logoColor=white" alt="Payoneer Badge" />
      </a><br/>
      <sub>Email: <code>arafathrahman710@gmail.com</code></sub>
    </td>
  </tr>
</table>

<br/>

| Method | Details / Direct Link |
| :--- | :--- |
| **☕ SupportKori** | [https://www.supportkori.com/arafathrahman](https://www.supportkori.com/arafathrahman) |
| **⚡ nsave** | Ntag: `@arafath_rahman9` • `Md Arafath Rahman` |
| **🔴 RedotPay** | Account ID: `1965421414` |
| **🅿️ Payoneer** | Email: `arafathrahman710@gmail.com` • Customer ID: `70366820` |

</div>

## License
You can add a license file as needed (MIT recommended for small projects).

---
If you want, I can also:
- Create a simple deploy script (`gh-pages`) and `package.json` to push automatically,
- Split `index.html` into smaller files (CSS/JS) for maintainability,
- Prepare a `CNAME` file if you want a custom domain.
