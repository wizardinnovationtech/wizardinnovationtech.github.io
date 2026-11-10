# QR Card Studio

Live at **https://wizardinnovationtech.github.io/**

One file (`index.html`) that is both:

- **The editor**: fill in your details, upload a logo, take colours from it, style the QR code, and download a lock-screen image, a printable business card, the QR (PNG/SVG), a contact file (.vcf), a stand-alone card page (.html) or everything as a .zip.
- **The card page**: when the address ends in `#c=…`, the same file shows the digital business card (Save Contact, Email, Call, WhatsApp, buttons, socials).

## How the QR keeps working

All card details are packed **into the QR link itself**. Nothing is stored on a server, and there is no database or account.

- The card page needs no internet libraries to display (the QR tools load only in the editor).
- If the hosting ever goes away, upload the same `index.html` to the same address, and every printed QR works again.
- For a code that needs no website at all, choose **Save my contact** in the QR section. The phone reads the contact straight from the code.

## Put it online (one time)

1. Create a free GitHub account, make a public repository (for example `card`), and upload `index.html`.
2. In the repository, open Settings → Pages, and set Source to the `main` branch. After about a minute your address is `https://<username>.github.io/card/`.
3. Open that address. It is now your editor. Paste the same address into **Card page address** in section 04 (it fills in automatically when you open the editor from there).
4. Download your images and test the QR with two phones before printing.

Netlify Drop (drag the folder onto app.netlify.com/drop) or your company website also work.

## Run locally

```bash
python3 -m http.server 8765 --directory qr-card-studio
```
