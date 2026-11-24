# Streamline Plumbing: website rebuild mockup

A modern rebuild of http://streamlineplumbing.com.au, a commercial plumbing contractor at 3/31 Oxleigh Dr, Malaga WA, phone (08) 9249 4350. It uses plain HTML, CSS and JS, with no frameworks or build step.

## Pages

| File | Page | Old site equivalent |
|---|---|---|
| `index.html` | Home: hero, at-a-glance stats, what we offer, sector cards, capabilities, maintenance, photo gallery, director quote | Home (logo, menu and a photo slider only) |
| `projects.html` | All 9 project sectors on one page, each with its description, recent projects and photos, plus a sticky sector jump bar | Projects plus 9 separate sector pages |
| `maintenance.html` | Backflow prevention testing and the full maintenance list | Maintenance |
| `about.html` | What we offer, sectors, capabilities and expertise, licences and ABN | About › Streamline Plumbing |
| `team.html` | About the team, training and apprenticeships, the director | About › Our Team |
| `safety.html` | Occupational health and safety policy | About › Safety |
| `contact.html` | Phone, email, address, licences, enquiry form and map | Contact Us |

Shared files: `css/style.css` and `js/main.js`.

## What changed from the old site (pitch points)

- **The menu no longer runs off the screen on phones.** There's now a proper hamburger menu, a tap-to-call button in the header and a sticky "Call (08) 9249 4350" bar at the bottom on phones. Nothing scrolls sideways at 375px.
- **The home page now has real content.** The old home page was a logo, a menu and an image slider, with almost no text for Google to read. The new one explains who they are, the sectors they work in, 16 capabilities, maintenance services and the director's 40+ years of experience. All of the text comes from their own site.
- **The project pages are combined.** Nine thin sector pages are now one rich Projects page, which is better for SEO and quicker to browse. Each sector has its own anchor (`projects.html#health` and so on).
- **Their licences and trust signals are visible.** PL591, GF10040, "Since 1998", "Family owned" and licensed backflow testing appear in the hero, on the About and Contact pages, and in the footer. The old site buried them in small footer text.
- **Each page has its own title and meta description**, written for local search (Malaga, Perth, commercial plumbing, backflow testing, maintenance).
- **The "© 2020" footer is gone.** The copyright year now updates itself.
- **Typos are fixed.** "Family owed" is now "family owned", the "Streamline Plumbling" page title is corrected, "full compressive" is now "comprehensive", and "highly sourced plumbers" is now "highly skilled plumbers". Several project names were also corrected (see below).
- **It looks current.** Their green and gold logo colours are refreshed with modern type, cards, real project photos, and a dark mode.
- **It's fast and has no Wix lock-in.** The old Wix pages were about 800 KB of HTML each, before any scripts. The new pages are small static files that can be hosted anywhere.

## Polish features

- Dark mode follows the system setting. A sun/moon toggle in the header remembers the visitor's choice in `localStorage` (key `sp-theme`, wrapped in try/catch). The theme is set inline in `<head>` before first paint, so there's no flash. Every colour is a CSS variable. A lighter logo (`logo-dark.png`) is used in dark mode.
- Sections, cards, list items and gallery photos fade and slide up as you scroll, with a staggered delay (IntersectionObserver). Anything already on screen at load isn't hidden.
- The sticky header gains a shadow and blur once you scroll. In-page links scroll smoothly, with scroll padding so headings aren't hidden under the sticky bars.
- The mobile menu opens and closes smoothly. It closes on Escape, on a link tap or on a tap outside, and the icon animates into an X.
- Hover states on buttons, cards, nav links and capability tiles. Images zoom slightly on hover.
- A back-to-top button, lazy-loaded images below the fold, visible gold focus rings and a skip link.
- Motion is quick (180–400ms ease-out) and switched off under `prefers-reduced-motion`.
- The contact form opens the visitor's email app with the message filled in, addressed to info@streamlineplumbing.com.au, because there's no server for this mockup.

Tested at 375px, 768px and 1366px in light and dark mode. There's no horizontal overflow on any page, and the menu, theme toggle, call bar and jump links all work.

## To confirm with the owner

- **Opening hours** aren't on the old site, so none are shown. Add them if they want them.
- **What GF10040 is.** The old site shows "Plumbing licence PL591|GF10040", and the new site shows it the same way. If GF10040 is their gas fitting licence, it could be labelled that way.
- **The MPA and Waterwise Specialist badges** appear in the old site's footer and are kept here. Check that both memberships are still current.
- **Spellings that were corrected:** "Queengate Medical Centre – Canningvale" is now "Queensgate Medical Centre, Canning Vale", and "People Who Care Alterations – Guilford" is now "Guildford". "Bandyup Women Prison" is now "Bandyup Women's Prison", and school names were written out in full (PS is now Primary School, SHS is now Senior High School).
- **Photo captions are kept generic**, because the old site doesn't say which photo belongs to which project. The owner can tell us which photos match which jobs.
- **Contact form:** it currently opens an email. A real form service such as Formspree could be connected later.
- The **"9 sectors"** and **"Any size"** stats are drawn from their own page list and their line about "from large and multi-story commercial plumbing contracts down to maintenance work priced by the hour". "40+ years" is the director's experience, as stated on the Our Team page.
- Client logos from the old site (ALDI, JB Hi-Fi, BMW, Red Rooster, the school crests and so on) were **left out on purpose**, because they're other companies' trademarks. The project names are listed as text instead.

## Image sources

All images were downloaded from the old site's own Wix image host (`static.wixstatic.com/media/…`), resized to 1000px wide (1400px for banners) and re-compressed as JPEG at quality 74. The logo and badges are kept as the original PNG/JPG. `logo.png` was trimmed of empty space, and `logo-dark.png` is a lightened copy made for dark mode.

| File | Wix media ID | Found on old page |
|---|---|---|
| logo.png, logo-dark.png | 7ed995_e6ac63ba9cb94599b654128eb857470b | All pages (header) |
| mpa-badge.png | 7ed995_4808776088f54b43ac334656a6d7a375 | All pages (footer) |
| waterwise-specialist.jpg | 7ed995_4f0ee96a2bbc48a8b4a5ed5d592d1428 | All pages (footer) |
| hero-fire-services.jpg | 7ed995_9984cbfa3d644821a4cad152cde96603 | Home slider |
| civil-drainage.jpg | 7ed995_07ab32d92f524835989d3695933de60a | Home |
| fire-services-pipework.jpg | 7ed995_6057c91680fc47adb749ffd28308ba9c | Home |
| fire-tank-pipework.jpg | 7ed995_de17b41344db4ac688a28cab28b08c9e | Home |
| flue-stacks.jpg | 7ed995_91ba2f4c2c164215ba25013caf1d914b | Home |
| washroom-troughs.jpg | 7ed995_15c0a9c721414f47a0f28d27510ba299 | Home |
| ceiling-pipework.jpg | 7ed995_499c83772f274dd283da9cbc73ee7cba | Home slider |
| ensuite.jpg | 7ed995_83a60b8f5dbc438a8ebdbeb90fbfea50 | Home slider |
| accessible-washroom.jpg | 7ed995_9db0b75935a5445ca307671d0c9ab104 | Home |
| toilet-block.jpg | 7ed995_a67943d995614d92a22591d13f347858 | Home |
| commercial-kitchen.jpg | 7ed995_a9a5e26246d64ee393e637835ba8a2be | Home |
| basement-pipework.jpg | 7ed995_a9d81231418d42eab019573d28b6a34a | Home slider |
| stormwater-pipework.jpg | 7ed995_d10450c4a60a47448b5959bbd23de706 | Home slider |
| riser-pipework.jpg | 7ed995_dd5c2b1454f847a2909b533302fae830 | Home slider |
| vanity-fitout.jpg | 7ed995_ec784cd6eba345f1b352f9f1001397bb | Home |
| bathroom-fitout.jpg | 7ed995_b3092d99bd784079a8c63bd60e749a77 | Home slider |
| apartments-1.jpg, apartments-2.jpg, rialto-apartments.jpg | 7ed995_ba4d61ca…, 7ed995_5afe31a2…, 7ed995_7478bf2e… | Apartments & Multi-Residential |
| kbh-keepsafe-storage.jpg, commercial-2.jpg, commercial-3.jpg | 7ed995_350f94c6…, 7ed995_e37ce6a3…, 7ed995_e09d09d7… | Commercial |
| dorsogna.jpg, design-construct-2.jpg | 7ed995_443bce22…, 7ed995_c157c37b… | Design and Construct |
| education-1.jpg | 7ed995_42d6e5cd… | Education |
| government-1.jpg | 7ed995_ae869331… | Government and Public Buildings |
| health-1.jpg, health-3.jpg, health-4.jpg | 7ed995_1864ba1d…, 7ed995_9b56718c…, 7ed995_9e5252bf… | Health and Aged Care |
| heritage-1.jpg to heritage-3.jpg | 7ed995_27960c4c…, 7ed995_b2af57b8…, 7ed995_273f79e6… | Heritage |
| industrial-1.jpg, industrial-2.jpg, ertech-wangara.jpg | 7ed995_681e7ed8…, 7ed995_77a261f4…, 7ed995_fb590ca2… | Industrial |
| aldi-belmont.jpg | 7ed995_ac1ca7e3… | Retail |
| maintenance-tools.jpg | 7ed995_fb9b29b1… | Maintenance |
| sam-germana.jpg | 7ed995_30858d8c… | Our Team |
| about-banner.jpg | 7ed995_2d0d982e… | About › Streamline Plumbing |

## Editing note

The seven pages share the same header and footer, copied into each file. If you change the menu, phone number or footer, change it in all seven HTML files.
