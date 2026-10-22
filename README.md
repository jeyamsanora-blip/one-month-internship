# Online Election System — code from the report

This ZIP contains a cleaned, runnable reconstruction of the code shown in the **Online_Election_System_Report_Four_Border_Lines_Each_Page.pdf**, especially Section 8 (Code Implementation). The PDF's code snippets contain some formatting and syntax breaks, so these files repair those breaks and organize the modules into separate files. This is reconstructed code, not a byte-for-byte extraction of the original project.

## Files
- `server.js` — Express API, MongoDB models, registration/login, candidates, voting and results
- `public/register.html` — voter registration page
- `public/login.html` — login page
- `public/candidates.html` — candidate list, vote action and results
- `public/admin.html` — demo candidate management page
- `public/style.css` — shared styles
- `package.json` — dependencies and start script

## Run locally
1. Install Node.js and MongoDB Community Server.
2. Start MongoDB locally.
3. Open a terminal in this folder and run `npm install`.
4. Run `npm start`.
5. Open `http://localhost:5000/register.html`.

The default database is `onlineElection` at `mongodb://127.0.0.1:27017/onlineElection`. Set `MONGODB_URI` to use another MongoDB connection string.

## Important limitations
This is an educational demonstration, **not a secure or certified election system**. The admin page and candidate-management API are intentionally demo-only and have no real administrator authentication. Do not use this code for an actual election or deploy it publicly without implementing proper authentication/authorization, secure session or token handling, audit controls, and security review. Passwords are hashed in this reconstruction, unlike the plaintext password handling shown in the report.
