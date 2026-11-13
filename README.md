# Steven Wael | Red Team & Penetration Testing Portfolio

A personal portfolio website for a penetration testing trainee, built as a **single self-contained HTML file** with a hacker-terminal look. No build step, no framework, no backend.

## What's inside

- **Hero** with a typing terminal animation and a code-rain background
- **About**, with a quick fact sheet
- **Track**: an interactive walk through the stages of a real attack, from recon to the final report
- **Skills & tools**
- **Experience & activities**
- **Projects**, each linking to its GitHub repo
  - [GuidelineAI](https://github.com/stevenwael32/GuidelineAI): medical RAG chatbot for blood pressure clinical guidelines
  - [Smart Web Pentest Assistant](https://github.com/stevenwael32/Smart-Web-Pentest-Assistant-entrypoint.): automated recon, risk scoring and reporting tool
  - [Caesar Cipher](https://github.com/stevenwael32/-Caesar-Cipher): encrypt, decrypt and brute-force text in Python
- **Certifications & courses** with a click-to-zoom certificate viewer
- **Download CV** button (the PDF is embedded in the page)
- Responsive layout, and animations are turned off for visitors who prefer reduced motion

## Run it locally

No install needed. Download the repo and open the HTML file in any modern browser.

```bash
git clone https://github.com/stevenwael32/<repo-name>.git
cd <repo-name>
# then double-click the HTML file, or serve it:
python3 -m http.server 8000
# open http://localhost:8000
```

## Publish it with GitHub Pages

1. Rename the HTML file to `index.html` so Pages picks it up as the home page.
2. Push it to your repo.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and the `/ (root)` folder, then save.
5. After a minute the site goes live at `https://<username>.github.io/<repo-name>/`.

## Customize it

Everything lives in the one HTML file.

| What | Where to change it |
|------|--------------------|
| Text, sections, projects | The HTML markup, search for the section `id` (`about`, `skills`, `experience`, `projects`, `certs`, `contact`) |
| Certificates | The `CERTS` array in the script (title, issuer, date, optional link) |
| Certificate images | The `CERT_IMG` object, keyed by the same ids as `CERTS` (base64 images) |
| CV file | The `CV_B64` constant (the PDF encoded as base64) |
| Colors | The CSS variables at the top of the `<style>` block |

To replace the CV, encode the new PDF and paste the result into `CV_B64`:

```bash
base64 -w 0 Steven_Wael_CV.pdf
```

## Tech

- Plain HTML, CSS and JavaScript
- Fonts from Google Fonts (Chakra Petch, IBM Plex Mono, IBM Plex Sans), with system fallbacks
- Certificate images and the CV are embedded in the file, so the page works on its own

## Ethics

Everything on this site was practiced on labs and authorized targets only. Only test systems you own or have written permission to test.

## Contact

- GitHub: [stevenwael32](https://github.com/stevenwael32)
- LinkedIn: [steven-wael](https://www.linkedin.com/in/steven-wael)
