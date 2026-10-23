Aren Kade — Animated Glassmorphism Portfolio

A dark, animated single-page portfolio website with frosted-glass UI and custom motion components. Built as a demo / concept to show the kind of personal websites I design and build for developers, designers and creators.

Note: "Aren Kade" is a fictional persona. All projects, achievements, experience and certificates on the site are placeholder content, and the certificates are marked SAMPLE.

Live demo: https://your-project.vercel.app ← replace with your Vercel URL

Features

Design

Black glassmorphism UI: frosted panels, drifting light orbs, film grain
Spotlight effect that follows the cursor across every glass panel
Anton + Instrument Sans + JetBrains Mono typography
Fully responsive, from 360px phones to wide desktops

Motion components (inspired by ObsidianUI, rewritten from scratch in vanilla JS)

Component	What it does
Discover Button	Arrow circle expands across the button on hover
Flip Text	Each heading letter lifts and spins on hover
Text Reel	Vertical word stream that speeds up or reverses with scroll
Draggable Marquee	Service cards you can fling, with momentum and infinite loop
Hover Image List	Project preview image follows the cursor over each row
Curved Gallery	Infinite grid bent into a barrel curve, draggable in any direction

Sections Hero · Services marquee · Selected work · Sky studies gallery · Achievements · Certificates (with viewer) · Experience · Lab (particle field, magnetic button, 3D tilt card) · Contact

Quality

No frameworks, no build step, one index.html file
All gallery images are generated on a canvas at load time, so there are no third-party photos to license
Keyboard accessible (arrow keys work on the marquee, the gallery and the certificate viewer; Esc closes dialogs)
Respects prefers-reduced-motion: animations switch off for users who ask for less motion
Tech stack
HTML5, CSS3 (backdrop-filter, scroll-driven animations, 3D transforms)
Vanilla JavaScript (requestAnimationFrame, Pointer Events, Canvas 2D)
Google Fonts
Hosted on Vercel
Run locally

No install needed.

bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

Then open index.html in your browser, or serve it locally:

bash
npx serve .
Deploy to Vercel
Push this folder to a GitHub repository.
Go to vercel.com/new and import the repository.
Leave every setting at its default (no framework, no build command) and click Deploy.

Every push to main redeploys automatically.

Customise it

Everything lives in index.html. Search for these to change the content:

What	Where to look
Name	Aren Kade, A.K (navbar), .bigname (footer)
Intro text	.lede in the hero
"I build" words	<ul id="reelList">
Hero stats	data-count attributes in .minis
Services	.tile blocks inside #dmqTrack
Projects	.hrow links inside #hlist, plus the art array in the script for preview images
Gallery images	skies list in the script. Replace src with your own image paths to use real photos
Achievements	#wins section
Certificates	.cert buttons in #certs
Experience	.job blocks in #exp
Email & socials	#email and .socials in #contact
Colours	CSS variables at the top of <style> (--bg, --fg, --ice, --ember)
Make the contact form send emails

The form is a demo and doesn't send anything yet. The quickest way to connect it is Formspree:

Create a free form and copy its endpoint (https://formspree.io/f/xxxxxxx).
In the form's submit handler in the script, replace the demo message with:
js
fetch('https://formspree.io/f/xxxxxxx', {
  method: 'POST',
  headers: { 'Accept': 'application/json' },
  body: new FormData(f)
}).then(r => n.textContent = r.ok ? 'Message sent.' : 'Something went wrong. Try email instead.');
Add name attributes to each input (name="name", name="email", name="message").
Want one like this?

I build custom animated portfolios and landing pages: your content, your photos, your colours, deployed on your own domain.

Fiverr: https://www.fiverr.com/deepsavvasher
Upwork: https://www.upwork.com/freelancers/~0141c01ce62dfaa4f5
Portfolio: https://deepsavvasher.vercel.app
Credits
Motion component ideas inspired by ObsidianUI (MIT). The code here is an original vanilla-JS implementation, not copied source.
Fonts: Anton, Instrument Sans, JetBrains Mono via Google Fonts.
License

MIT. Use it, change it, ship it.
