# Mehar Kumar Gupta — Personal Website

A light, royal blue and silver personal website built with plain HTML, CSS and JavaScript. No framework, no build step, no paid services.

## Files

```
mehar-website/
├── index.html            Main page (all sections)
├── css/style.css         All styling, colours and typography
├── js/main.js            Mobile menu, scroll effects, automatic copyright year
├── assets/images/
│   ├── profile.jpg       Your profile photograph (replace with your own)
│   └── favicon.png       Browser tab icon placeholder (add your own)
└── README.md             This file
```

## Preview locally

Double-click `index.html` to open it in a browser. Everything works offline except the Google Fonts, which need an internet connection.

## How to edit

All content lives in `index.html`. Look for these comments and sections:

- **Hero:** the designation line, name, introduction and buttons near the top.
- **About:** the paragraphs and the three fact cards (hometown, current residence, languages).
- **Interests:** one `<li class="card">` per interest. Edit the title and text, or the icon SVG.
- **Education:** one `<li class="timeline-item">` per school.
- **Future ambition:** the paragraph and the bullet list. Keep the wording as a future aspiration.
- **Connect:** social links. Each link is an `<a>` with the account URL in `href`.
- **Footer:** name and social links. The copyright year updates itself automatically.

### Colours
Defined at the top of `css/style.css` under `:root`:

| Variable | Value | Use |
|---|---|---|
| `--navy` | `#142B52` | Primary royal navy |
| `--blue` | `#2457A7` | Secondary royal blue |
| `--pearl` | `#F8FAFD` | Page background |
| `--white` | `#FFFFFF` | Cards |
| `--silver` | `#B8C2D1` | Metallic silver details |
| `--ink` | `#17243A` | Body text |
| `--grey` | `#788397` | Muted text |

### Fonts
Loaded from Google Fonts in the `<head>` of `index.html`:
- **Playfair Display** for headings
- **Inter** for body text
- **Manrope** for navigation and buttons

## Adding your profile photograph

1. Prepare a portrait photo, ideally at least 1000 px wide, in JPG format.
2. Rename it to `profile.jpg`.
3. Replace the file at `assets/images/profile.jpg`.

The photo is shown without any retouching, and it is cropped to a 4:5 frame. If your face sits too high or low, change `object-position: center 20%;` in the `.photo-frame img` rule of `css/style.css`.

## Adding a favicon

Place a square PNG at `assets/images/favicon.png`. Until then the browser will show a default icon.

## WhatsApp

The site shows your WhatsApp **username only** (`guptamehar`). Your phone number is never published. No WhatsApp chat link is included, because one needs a phone number to work. If you want a clickable WhatsApp link later, add it yourself as `https://wa.me/<countrycode><number>`.

## Uploading to your own hosting

1. Log in to your hosting control panel (cPanel, Hostinger, Namecheap and similar).
2. Open **File Manager** and go to `public_html` (or the web root your host specifies).
3. Upload the whole `mehar-website` folder contents, so that `index.html` sits directly inside `public_html`.
4. Visit your domain in a browser to check the site.

Alternatively, use **Netlify Drop** or **GitHub Pages** (both free) by uploading the folder, then connect your own domain in their settings.

## Connecting your own domain

1. Register your domain with a registrar (for example Namecheap, GoDaddy or Google Domains successors such as Squarespace Domains).
2. In your hosting dashboard, add the domain and note the nameservers or DNS records it shows.
3. In your registrar's DNS settings, point the domain to the hosting provider using those nameservers or records.
4. Wait for DNS to propagate (usually minutes to a few hours), then enable free HTTPS (SSL) from the hosting panel.
5. Update the placeholder `https://www.example.com/` in the `canonical` and `og:url` tags of `index.html` to your real domain.

## Before going live

- Replace `https://www.example.com/` with your real domain.
- Replace `profile.jpg` with your own photo.
- Add a favicon.
- Check every social link opens the correct account.
- Test the email link on your phone.
