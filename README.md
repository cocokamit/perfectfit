# Perfect Fit

A one-page answer to *"Why are you a good fit for the job?"* for the AI Developer role at Prime AI. It's funny where it can be and serious where it counts.

**One HTML file. No build step.** The only dependency is three.js, loaded from a CDN. If the CDN fails, the page still works without the 3D scene.

## Personalize it (2 minutes)

Open `index.html` and find the `CONFIG` object (search for `EDIT ME`). Fill in:

- `name`, `email`, `links` (GitHub, LinkedIn, resume)
- `pitch`: two or three sentences, as specific as you can make them
- `projects`: real projects, each with a concrete impact line

The rest of the text (jokes, the workflow, the 30-day plan) is in plain HTML if you want to change it.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploy

Any static host works: GitHub Pages (Settings → Pages → deploy from branch), Netlify Drop, or Vercel.

## What's in it

- **three.js blob:** a noise-displaced shader that moves, recolors, and changes mood per section as you scroll. It goes grey and wireframe in the serious section.
- **Attention cursor:** dashed "attention" lines to nearby clickable things, weighted with a softmax over distance. It leaves a trail of code tokens, shows `> awaiting prompt` when idle, and adds `+1 commit` on click. Desktop only.
- **Scroll effects:** letter-by-letter headings, blur-in reveals, a pinned horizontal "how I ship" section, and a progress bar.
- **Humor toggle:** turns the whole site into a straight, HR-friendly version.
- **Extras:** flip cards (joke / receipts), the AI Responsibility Slider, a replayable Claude Code terminal, count-up stats, a shy "Not sure" button, confetti, and a Konami code easter egg.
- Respects `prefers-reduced-motion` and works on mobile.
